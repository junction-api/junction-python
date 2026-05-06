# Changelog

_Major release. Baseline: `tryVital/vital-python@2.1.561`._

## Breaking changes

- **Minimum Python is now 3.10** — [migration steps](MIGRATION.md#install)
  The new distribution requires Python 3.10 or newer (previously 3.8). Older interpreters can no longer install or import the SDK. Bump your project's runtime, your CI matrix, your Dockerfile base images, and any tooling that pins the interpreter (e.g. `tool.poetry.dependencies.python`, `setup.cfg python_requires`, `pyenv` files).
- **Package renamed: `vital` → `junction-api-sdk`** — [migration steps](MIGRATION.md#install)
  The PyPI distribution name has changed. Uninstall the old package and install `junction-api-sdk`, then update every import path in your codebase from `vital` to `junction`. This is a *replacement*, not a version bump — the old `vital` distribution is no longer published with new releases.
- **Tighter `pydantic-core` upper bound (`<2.44.0`)** — [migration steps](MIGRATION.md#install)
  The dependency on `pydantic-core` is now pinned to `>=2.18.2,<2.44.0`. If your application or another dependency requires `pydantic-core >= 2.44.0`, the install will fail to resolve. Audit your lockfile and any sibling packages that pull in newer `pydantic-core` versions before upgrading.
- **Server base URLs replaced (Environment enum also renamed)** — [migration steps](MIGRATION.md#rename-environment-enum)
  The SDK now talks to the rebranded Junction hosts. The four server URLs have been replaced: `api.tryvital.io` → `api.us.junction.com`, `api.eu.tryvital.io` → `api.eu.junction.com`, `api.sandbox.tryvital.io` → `api.sandbox.us.junction.com`, and `api.sandbox.eu.tryvital.io` → `api.sandbox.eu.junction.com`. This affects any caller that passes a literal URL string for the `base_url` argument or otherwise references the old hosts (allow-lists, monitoring, log filters). The environment enum has also been renamed: `VitalEnvironment` → `JunctionEnvironment`. Callers that use the enum (e.g. `JunctionEnvironment.PRODUCTION`) automatically pick up the new URL because the enum's underlying value changed alongside the rename.
- **Top-level client class renamed to `Junction` / `AsyncJunction`** — [migration steps](MIGRATION.md#rename-client-class)
  The synchronous and asynchronous client classes have been renamed. `Vital` is now `Junction`, and `AsyncVital` is now `AsyncJunction`. Update every construction site and every type annotation that references the old names. The constructor keyword arguments (`api_key`, `base_url`, `environment`, `timeout`, `httpx_client`, …) are unchanged.
- **Request bodies and path parameters are now inline keyword arguments** — [migration steps](MIGRATION.md#inline-request-fields)
  Methods that used to take a single `request=<RequestModel>` object alongside path parameters now expose every body field and path parameter directly on the method signature. Construct the call by passing each field as a keyword argument (or, for path parameters, as a positional argument) instead of building a request model. The change applies uniformly across the SDK — for example `lab_tests.book_phlebotomy_appointment(order_id, request=AppointmentBookingRequest(booking_key=...))` becomes `lab_tests.book_phlebotomy_appointment(order_id, booking_key=...)`. Required body fields become required keyword arguments; optional body fields become optional keyword arguments with the same names.
- **Some response and request fields are now `Optional`** — [migration steps](MIGRATION.md#nullable-fields)
  Fields whose schemas are marked nullable in the API definition are now exposed as `Optional[...]` in Python types and may legitimately be `None`. If you have type-checked code that previously relied on these fields being non-`None`, add a guard (or update your type hints) before dereferencing them. This affects both response model attributes and the corresponding request inputs; the wire format is unchanged.

## New & improved

- **New top-level resources**
  The SDK now exposes the `compendium`, `lab_account`, `order_transaction` resource clients on the root client. See the API reference for the full endpoint list.
- **Raw response shapes formalized — `*V2InDb` types are now `*Raw`**
  Endpoints whose responses were previously typed as `*V2InDb` now use `*Raw` types. The values are unchanged; only the type names differ:
  
  - `ActivityV2InDb` → `ActivityRaw` (for `activity.get_raw`)
  - `BodyV2InDb` → `BodyRaw` (for `body.get_raw`)
  - `DeviceV2InDb` → `DevicesRaw` (for `devices.get_raw`)
  - `SleepV2InDb` → `SleepRaw` (for `sleep.get_raw`)
  - `WorkoutV2InDb` → `WorkoutRaw` (for `workouts.get_raw`)
  
  Additionally, the standalone `RawDevices` wrapper from the old SDK is replaced by `RawDevicesResponse`.
  
  If you imported one of the old type names directly (e.g. `from junction.types.activity_v_2_in_db import ActivityV2InDb`), switch to the new `Raw` type.
- **Configurable SDK logging**
  Both `Junction` and `AsyncJunction` accept a new `logging` keyword argument (`LogConfig` or a custom `Logger`). Pass a `LogConfig` to set the log level (`debug` / `info` / `warn` / `error`) and toggle silent mode, or supply your own `Logger` implementation to integrate with an existing application logger. By default the SDK is silent.
- **Optional `aiohttp` async transport**
  An opt-in `aiohttp` extra is available: `pip install "junction-api-sdk[aiohttp]"`. Installing it pulls in `aiohttp` and `httpx-aiohttp`, and lets you pass `httpx_client=DefaultAioHttpClient(...)` from `junction._default_clients` to the async client to use an aiohttp-backed transport. Existing users do not need to install the extra.

## Removed

- **Legacy link methods removed** — [migration steps](MIGRATION.md#link-removed-legacy-methods)
  These six methods have been deprecated for over two years and were never part of the documented Junction Link integration path; they should not have been in the SDK in the first place. They are removed in this release:
  
  - `email_auth`
  - `password_auth`
  - `start_connect`
  - `connect_manual_provider`
  - `token_state`
  - `is_token_valid`
  
  If you have call sites referencing these methods, see the Junction Link API reference for the documented integration path. The supporting request/body classes that backed them are also removed.
  
  The supporting request/body classes that backed these methods are also removed: `BeginLinkTokenRequest`, `EmailAuthLink`, `PasswordAuthLink`, `LinkTokenValidationRequest`, `ManualConnectionData`.
- **`team.get_link_config` removed** — [migration steps](MIGRATION.md#team-removed-get-link-config)
  `team.TeamClient.get_link_config` and its async/raw counterparts have been removed. The endpoint it wrapped (`GET /v2/team/link/config`) was previously deprecated. Read team-level link configuration through the team configuration surface (see the API reference for the current shape) or rely on the configuration values you pass when issuing link tokens via `link.token(...)`.
- **Public types removed** — [migration steps](MIGRATION.md#public-types-removed)
  Three top-level type re-exports were removed from the SDK with no equivalent. If you imported any of these from the package root, drop the import:
  
  - `AuthType` — was used by the legacy `email_auth` flow only.
  - `ManualProviders` — was the parameter type for the now-removed `connectManualProvider` method (one of the legacy link methods, see above). With that method gone, this enum is removed too.
  - `ClientFacingUserKey` — the endpoint that used to return this model now returns `ClientFacingUser` instead. If you depended on the user-key shape, switch to reading the user fields off `ClientFacingUser` directly.
