# Migration guide

_From `tryVital/vital-python@2.1.561` to the new release._

## Install the new package

<a id="install"></a>

This is a *replacement*, not a version bump — uninstall the old distribution, install `junction-api-sdk`, and update your imports from the old package name to the new one. The minimum Python version is now 3.10.

Things to watch for:

- Aliased imports (`import vital as v`, `from vital import types as vt`).
- Submodule imports across `vital.lab_tests`, `vital.user`, `vital.link`, `vital.types`, `vital.errors`, etc.
- String-literal references in dynamic loaders (`importlib.import_module("vital....")`, entry-point specs in `pyproject.toml` / `setup.py`, dependency-injection container keys).
- Lockfiles, Dockerfile pins, CI/CD scripts, and internal mirror/proxy index entries that reference the old `vital` distribution.
- Version introspection: `importlib.metadata.version("vital")` becomes `importlib.metadata.version("junction-api-sdk")`.
- Environment-variable names following the old brand (e.g. `VITAL_API_KEY`); the SDK constructor argument names are unchanged but your application's own env-var conventions may need a rename pass.

**Before:**

```bash
pip install vital
```

```python
from vital import Vital
client = Vital(api_key="YOUR_API_KEY")
```

**After:**

```bash
pip uninstall vital
pip install junction-api-sdk
```

```python
from junction import Junction
client = Junction(api_key="YOUR_API_KEY")
```

## Server base URLs and `VitalEnvironment` → `JunctionEnvironment`

<a id="rename-environment-enum"></a>

The four server URLs are replaced as follows:

| Old host                          | New host                                |
|-----------------------------------|-----------------------------------------|
| `api.tryvital.io`                 | `api.us.junction.com`                   |
| `api.eu.tryvital.io`              | `api.eu.junction.com`                   |
| `api.sandbox.tryvital.io`         | `api.sandbox.us.junction.com`           |
| `api.sandbox.eu.tryvital.io`      | `api.sandbox.eu.junction.com`           |

Things to watch for:

- Hard-coded URL strings in `base_url=`, allow-lists, monitoring dashboards, log filters, and webhook signatures.
- Outbound-egress firewall rules and proxy configurations pinned to the old hostnames.
- `VitalEnvironment` references in test fixtures and CI configuration.

**Before:**

```python
from vital import Vital
from vital.environment import VitalEnvironment

client = Vital(
    api_key="YOUR_API_KEY",
    environment=VitalEnvironment.PRODUCTION,
)

# or, when overriding with a literal URL:
client = Vital(api_key="YOUR_API_KEY", base_url="https://api.tryvital.io")
```

**After:**

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="YOUR_API_KEY",
    environment=JunctionEnvironment.PRODUCTION,
)

# or, when overriding with a literal URL:
client = Junction(api_key="YOUR_API_KEY", base_url="https://api.us.junction.com")
```

## Rename `Vital` / `AsyncVital` to `Junction` / `AsyncJunction`

<a id="rename-client-class"></a>

Things to watch for:

- Aliased imports (e.g. `from vital import Vital as VitalClient`).
- Type annotations on helpers that take a client argument (`def fn(client: Vital) -> ...`).
- String-literal references in dynamic dispatch, dependency-injection containers, or pickle/serialization layers.
- `isinstance(...)` checks against the old class.

**Before:**

```python
from vital import Vital, AsyncVital

client = Vital(api_key="YOUR_API_KEY")
async_client = AsyncVital(api_key="YOUR_API_KEY")
```

**After:**

```python
from junction import Junction, AsyncJunction

client = Junction(api_key="YOUR_API_KEY")
async_client = AsyncJunction(api_key="YOUR_API_KEY")
```

## Pass body and path fields as inline arguments

<a id="inline-request-fields"></a>

The same rule applies to every method that previously took a `request=` model: lift each body field onto the method as a keyword argument, and pass path parameters positionally (or as the keyword name shown in the new docstring). You generally no longer need to import the per-endpoint request model classes.

**Before:**

```python
from vital import Vital
from vital.types import AppointmentBookingRequest

client = Vital(api_key="YOUR_API_KEY")

client.lab_tests.book_phlebotomy_appointment(
    order_id="order_123",
    request=AppointmentBookingRequest(
        booking_key="slot_abc",
    ),
)
```

**After:**

```python
from junction import Junction

client = Junction(api_key="YOUR_API_KEY")

client.lab_tests.book_phlebotomy_appointment(
    "order_123",
    booking_key="slot_abc",
)
```

## Handle `Optional` response fields

<a id="nullable-fields"></a>

Audit any callsite that previously dereferenced a field whose schema is now nullable. The set of affected fields is whatever the API definition marks `nullable: true`; type checkers will flag the new `Optional[...]` annotations once you upgrade.

**Before:**

```python
order = client.lab_tests.get_order(order_id="order_123")
upper_name = order.shipping_recipient_name.upper()
```

**After:**

```python
order = client.lab_tests.get_order(order_id="order_123")
upper_name = order.shipping_recipient_name.upper() if order.shipping_recipient_name is not None else None
```

## Drop calls to the legacy link methods

<a id="link-removed-legacy-methods"></a>

These methods were deprecated for years and not part of the documented Junction Link integration. Customer code that didn't reference them needs no migration. If you do have call sites, replace them with the Junction Link integration described in the API reference — there isn't a one-to-one drop-in, the legacy methods wrapped retired endpoints with no published equivalents.

## Drop imports for removed public types

<a id="public-types-removed"></a>

Three names were exported from the package root in the old SDK but are not present in the new SDK:

- `AuthType` — was only used by the legacy `email_auth` flow.
- `ManualProviders` — was the parameter type for the now-removed `connectManualProvider` method.
- `ClientFacingUserKey` — callers should switch to `ClientFacingUser`. The endpoint that previously returned `ClientFacingUserKey` now returns `ClientFacingUser`.

**Before:**

```python
from vital import AuthType, ClientFacingUserKey, ManualProviders
```

**After:**

```python
# AuthType and ManualProviders have no replacement — remove the import.
# ClientFacingUserKey -> ClientFacingUser
from junction import ClientFacingUser
```
