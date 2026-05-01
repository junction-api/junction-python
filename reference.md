# Reference
## Link
<details><summary><code>client.link.<a href="src/junction/link/client.py">list_bulk_ops</a>(...) -> BulkOpsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.list_bulk_ops(
    next_cursor="next_cursor",
    page_size=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">bulk_import</a>(...) -> BulkImportConnectionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, OAuthProviders, ConnectionRecipe
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.bulk_import(
    provider=OAuthProviders.OURA,
    connections=[
        ConnectionRecipe(
            user_id="user_id",
            access_token="access_token",
            refresh_token="refresh_token",
            provider_id="provider_id",
            expires_at=1,
        )
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**provider:** `OAuthProviders` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**connections:** `typing.List[ConnectionRecipe]` 
    
</dd>
</dl>

<dl>
<dd>

**wait_for_completion:** `typing.Optional[bool]` 


Whether or not the endpoint should wait for the Bulk Op to complete before responding.

When `wait_for_completion` is enabled, the endpoint may respond 200 OK if the Bulk Op takes less than 20 seconds to complete.

Otherwise, the endpoint always responds with 202 Created once the submitted data have been enqueued successfully. You can use
the [List Bulk Ops](https://docs.tryvital.io/api-reference/link/list-bulk-ops) endpoint to inspect the progress of the Bulk Op.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">bulk_trigger_historical_pull</a>(...) -> typing.Any</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, OAuthProviders
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.bulk_trigger_historical_pull(
    user_ids=[
        "user_ids"
    ],
    provider=OAuthProviders.OURA,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_ids:** `typing.List[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `OAuthProviders` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**wait_for_completion:** `typing.Optional[bool]` 


Whether or not the endpoint should wait for the Bulk Op to complete before responding.

When `wait_for_completion` is enabled, the endpoint may respond 200 OK if the Bulk Op takes less than 20 seconds to complete.

Otherwise, the endpoint always responds with 202 Created once the submitted data have been enqueued successfully. You can use
the [List Bulk Ops](https://docs.tryvital.io/api-reference/link/list-bulk-ops) endpoint to inspect the progress of the Bulk Op.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">bulk_export</a>(...) -> BulkExportConnectionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, OAuthProviders
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.bulk_export(
    provider=OAuthProviders.OURA,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**provider:** `OAuthProviders` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**user_ids:** `typing.Optional[typing.List[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**next_token:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">bulk_pause</a>(...) -> typing.Any</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, OAuthProviders
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.bulk_pause(
    user_ids=[
        "user_ids"
    ],
    provider=OAuthProviders.OURA,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_ids:** `typing.List[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `OAuthProviders` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">token</a>(...) -> LinkTokenExchangeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Endpoint to generate a user link token, to be used throughout the vital
link process. The vital link token is a one time use token, that
expires after 10 minutes. If you would like vital-link widget to launch
with a specific provider, pass in a provider in the body. If you would
like to redirect to a custom url after successful or error connection,
pass in your own custom redirect_url parameter.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.token(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` — User id returned by vital create user request. This id should be stored in your database against the user and used for all interactions with the vital api.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[Providers]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**redirect_url:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**filter_on_providers:** `typing.Optional[typing.List[Providers]]` 

An allowlist of providers dictating what Vital Link Widget should show to the end user.
If unspecified, all linkable providers are shown.

This has no effect on programmatic Vital Link API usage.
    
</dd>
</dl>

<dl>
<dd>

**on_error:** `typing.Optional[typing.Literal]` 

By default, Vital Link Widget input forms for password and email providers have in-built error handling.

Specifying `on_error=redirect` disables this Vital Link Widget UI behaviour — it would
instead redirect to your `redirect_url`, with Link Error parameters injected.

This has no effect on OAuth providers — they always redirect to your `redirect_url`. This also has
no effect on programmatic Vital Link API usage.
    
</dd>
</dl>

<dl>
<dd>

**on_close:** `typing.Optional[typing.Literal]` 

By default, Vital Link Widget closes the window or tab when the user taps the Close button.

Specifying `on_close=redirect` would change the Close button behaviour to redirect to your `redirect_url`
with the `user_cancelled` error specified.

This has no effect on programmatic Vital Link API usage.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">code_create</a>(...) -> VitalTokenCreatedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate a token to invite a user of Vital mobile app to your team
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment
import datetime

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.code_create(
    user_id="user_id",
    expires_at=datetime.datetime.fromisoformat("2024-01-15T09:30:00+00:00"),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**expires_at:** `typing.Optional[datetime.datetime]` — When the link code should expire. Defaults to server time plus 1 hour.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">generate_oauth_link</a>(...) -> Source</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint generates an OAuth link for oauth provider
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, OAuthProviders
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.generate_oauth_link(
    oauth_provider=OAuthProviders.OURA,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**oauth_provider:** `OAuthProviders` 
    
</dd>
</dl>

<dl>
<dd>

**vital_link_token:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">connect_password_provider</a>(...) -> ProviderLinkResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This connects auth providers that are password based.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, PasswordProviders
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.connect_password_provider(
    provider=PasswordProviders.WHOOP,
    username="username",
    password="password",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**provider:** `PasswordProviders` 
    
</dd>
</dl>

<dl>
<dd>

**username:** `str` — Username for provider
    
</dd>
</dl>

<dl>
<dd>

**password:** `str` — Password for provider
    
</dd>
</dl>

<dl>
<dd>

**vital_link_token:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**region:** `typing.Optional[Region]` — Provider region to authenticate against. Only applicable to specific providers. ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">complete_password_provider_mfa</a>(...) -> ProviderLinkResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This connects auth providers that are password based.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, PasswordProviders
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.complete_password_provider_mfa(
    provider=PasswordProviders.WHOOP,
    mfa_code="mfa_code",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**provider:** `PasswordProviders` 
    
</dd>
</dl>

<dl>
<dd>

**mfa_code:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**vital_link_token:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">connect_email_auth_provider</a>(...) -> typing.Any</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This connects auth providers that are email based.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.connect_email_auth_provider(
    email="email",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**provider:** `EmailProviders` 
    
</dd>
</dl>

<dl>
<dd>

**email:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**vital_link_token:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**email_provider_auth_link_provider:** `typing.Optional[Providers]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**region:** `typing.Optional[Region]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">get_all_providers</a>(...) -> typing.List[SourceLink]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET List of all available providers given the generated link token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.get_all_providers()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vital_link_token:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.link.<a href="src/junction/link/client.py">connect_demo_provider</a>(...) -> DemoConnectionStatus</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST Connect the given Vital user to a demo provider.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, DemoProviders
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.link.connect_demo_provider(
    user_id="user_id",
    provider=DemoProviders.APPLE_HEALTH_KIT,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` — Vital user ID
    
</dd>
</dl>

<dl>
<dd>

**provider:** `DemoProviders` — Demo provider. For more information, please check out our docs (https://docs.tryvital.io/wearables/providers/test_data) ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Electrocardiogram
<details><summary><code>client.electrocardiogram.<a href="src/junction/electrocardiogram/client.py">get</a>(...) -> ClientFacingElectrocardiogramResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get electrocardiogram summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.electrocardiogram.get(
    user_id="user_id",
    start_date="start_date",
    end_date="end_date",
    provider="provider",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SleepCycle
<details><summary><code>client.sleep_cycle.<a href="src/junction/sleep_cycle/client.py">get</a>(...) -> ClientSleepCycleResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get sleep cycle for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.sleep_cycle.get(
    user_id="user_id",
    start_date="start_date",
    end_date="end_date",
    provider="provider",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Profile
<details><summary><code>client.profile.<a href="src/junction/profile/client.py">get</a>(...) -> ClientFacingProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get profile for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.profile.get(
    user_id="user_id",
    provider="provider",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.profile.<a href="src/junction/profile/client.py">get_raw</a>(...) -> RawProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw profile for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.profile.get_raw(
    user_id="user_id",
    provider="provider",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Devices
<details><summary><code>client.devices.<a href="src/junction/devices/client.py">get_raw</a>(...) -> RawDevicesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Devices for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.devices.get_raw(
    user_id="user_id",
    provider="provider",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Activity
<details><summary><code>client.activity.<a href="src/junction/activity/client.py">get</a>(...) -> ClientActivityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get activity summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.activity.get(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.activity.<a href="src/junction/activity/client.py">get_raw</a>(...) -> RawActivityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw activity summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.activity.get_raw(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Workouts
<details><summary><code>client.workouts.<a href="src/junction/workouts/client.py">get</a>(...) -> ClientWorkoutResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get workout summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.workouts.get(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workouts.<a href="src/junction/workouts/client.py">get_raw</a>(...) -> RawWorkoutResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw workout summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.workouts.get_raw(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workouts.<a href="src/junction/workouts/client.py">get_by_workout_id</a>(...) -> ClientFacingStream</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.workouts.get_by_workout_id(
    workout_id="workout_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workout_id:** `str` — The Vital ID for the workout
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Sleep
<details><summary><code>client.sleep.<a href="src/junction/sleep/client.py">get</a>(...) -> ClientSleepResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get sleep summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.sleep.get(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sleep.<a href="src/junction/sleep/client.py">get_raw</a>(...) -> RawSleepResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw sleep summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.sleep.get_raw(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sleep.<a href="src/junction/sleep/client.py">get_stream_by_sleep_id</a>(...) -> ClientFacingSleepStream</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Sleep stream for a user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.sleep.get_stream_by_sleep_id(
    sleep_id="sleep_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sleep_id:** `str` — The Vital Sleep ID
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Body
<details><summary><code>client.body.<a href="src/junction/body/client.py">get</a>(...) -> ClientBodyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Body summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.body.get(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.body.<a href="src/junction/body/client.py">get_raw</a>(...) -> RawBodyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get raw Body summary for user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.body.get_raw(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Meal
<details><summary><code>client.meal.<a href="src/junction/meal/client.py">get</a>(...) -> ClientFacingMealResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get user's meals
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.meal.get(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## MenstrualCycle
<details><summary><code>client.menstrual_cycle.<a href="src/junction/menstrual_cycle/client.py">get</a>(...) -> MenstrualCycleResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.menstrual_cycle.get(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Vitals
<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">workout_swimming_stroke_grouped</a>(...) -> GroupedWorkoutSwimmingStrokeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.workout_swimming_stroke_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">workout_distance_grouped</a>(...) -> GroupedWorkoutDistanceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.workout_distance_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">heart_rate_recovery_one_minute_grouped</a>(...) -> GroupedHeartRateRecoveryOneMinuteResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.heart_rate_recovery_one_minute_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">waist_circumference_grouped</a>(...) -> GroupedWaistCircumferenceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.waist_circumference_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">lean_body_mass_grouped</a>(...) -> GroupedLeanBodyMassResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.lean_body_mass_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">body_mass_index_grouped</a>(...) -> GroupedBodyMassIndexResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.body_mass_index_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">basal_body_temperature_grouped</a>(...) -> GroupedBasalBodyTemperatureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.basal_body_temperature_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">handwashing_grouped</a>(...) -> GroupedHandwashingResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.handwashing_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">daylight_exposure_grouped</a>(...) -> GroupedDaylightExposureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.daylight_exposure_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">uv_exposure_grouped</a>(...) -> GroupedUvExposureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.uv_exposure_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">fall_grouped</a>(...) -> GroupedFallResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.fall_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">inhaler_usage_grouped</a>(...) -> GroupedInhalerUsageResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.inhaler_usage_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">peak_expiratory_flow_rate_grouped</a>(...) -> GroupedPeakExpiratoryFlowRateResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.peak_expiratory_flow_rate_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">forced_vital_capacity_grouped</a>(...) -> GroupedForcedVitalCapacityResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.forced_vital_capacity_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">forced_expiratory_volume1grouped</a>(...) -> GroupedForcedExpiratoryVolume1Response</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.forced_expiratory_volume_1_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">wheelchair_push_grouped</a>(...) -> GroupedWheelchairPushResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.wheelchair_push_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">sleep_breathing_disturbance_grouped</a>(...) -> GroupedSleepBreathingDisturbanceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.sleep_breathing_disturbance_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">sleep_apnea_alert_grouped</a>(...) -> GroupedSleepApneaAlertResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.sleep_apnea_alert_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">stand_duration_grouped</a>(...) -> GroupedStandDurationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.stand_duration_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">stand_hour_grouped</a>(...) -> GroupedStandHourResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.stand_hour_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">heart_rate_alert_grouped</a>(...) -> GroupedHeartRateAlertResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.heart_rate_alert_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">afib_burden_grouped</a>(...) -> GroupedAFibBurdenResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.afib_burden_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">workout_duration_grouped</a>(...) -> GroupedWorkoutDurationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.workout_duration_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">vo2max_grouped</a>(...) -> GroupedVo2MaxResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.vo_2_max_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">stress_level_grouped</a>(...) -> GroupedStressLevelResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.stress_level_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">mindfulness_minutes_grouped</a>(...) -> GroupedMindfulnessMinutesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.mindfulness_minutes_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">caffeine_grouped</a>(...) -> GroupedCaffeineResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.caffeine_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">water_grouped</a>(...) -> GroupedWaterResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.water_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">steps_grouped</a>(...) -> GroupedStepsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.steps_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">floors_climbed_grouped</a>(...) -> GroupedFloorsClimbedResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.floors_climbed_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">distance_grouped</a>(...) -> GroupedDistanceResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.distance_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">calories_basal_grouped</a>(...) -> GroupedCaloriesBasalResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.calories_basal_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">calories_active_grouped</a>(...) -> GroupedCaloriesActiveResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.calories_active_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">respiratory_rate_grouped</a>(...) -> GroupedRespiratoryRateResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.respiratory_rate_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">note_grouped</a>(...) -> GroupedNoteResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.note_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">insulin_injection_grouped</a>(...) -> GroupedInsulinInjectionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.insulin_injection_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">ige_grouped</a>(...) -> GroupedIgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.ige_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">igg_grouped</a>(...) -> GroupedIggResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.igg_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">hypnogram_grouped</a>(...) -> GroupedHypnogramResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.hypnogram_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">hrv_grouped</a>(...) -> GroupedHrvResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.hrv_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">heartrate_grouped</a>(...) -> GroupedHeartRateResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.heartrate_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">glucose_grouped</a>(...) -> GroupedGlucoseResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.glucose_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">cholesterol_grouped</a>(...) -> GroupedCholesterolResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.cholesterol_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">carbohydrates_grouped</a>(...) -> GroupedCarbohydratesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.carbohydrates_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">body_temperature_delta_grouped</a>(...) -> GroupedBodyTemperatureDeltaResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.body_temperature_delta_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">body_temperature_grouped</a>(...) -> GroupedBodyTemperatureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.body_temperature_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">body_weight_grouped</a>(...) -> GroupedBodyWeightResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.body_weight_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">body_fat_grouped</a>(...) -> GroupedBodyFatResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.body_fat_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">blood_oxygen_grouped</a>(...) -> GroupedBloodOxygenResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.blood_oxygen_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">electrocardiogram_voltage_grouped</a>(...) -> GroupedElectrocardiogramVoltageResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.electrocardiogram_voltage_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">blood_pressure_grouped</a>(...) -> GroupedBloodPressureResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.blood_pressure_grouped(
    user_id="user_id",
    cursor="cursor",
    next_cursor="next_cursor",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">vo2max</a>(...) -> typing.List[ClientFacingVo2MaxTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.vo_2_max(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">stress_level</a>(...) -> typing.List[ClientFacingStressLevelTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.stress_level(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">mindfulness_minutes</a>(...) -> typing.List[ClientFacingMindfulnessMinutesTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.mindfulness_minutes(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">caffeine</a>(...) -> typing.List[ClientFacingCaffeineTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.caffeine(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">water</a>(...) -> typing.List[ClientFacingWaterTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.water(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">steps</a>(...) -> typing.List[ClientFacingStepsTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.steps(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">floors_climbed</a>(...) -> typing.List[ClientFacingFloorsClimbedTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.floors_climbed(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">distance</a>(...) -> typing.List[ClientFacingDistanceTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.distance(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">calories_basal</a>(...) -> typing.List[ClientFacingCaloriesBasalTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.calories_basal(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">calories_active</a>(...) -> typing.List[ClientFacingCaloriesActiveTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.calories_active(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">respiratory_rate</a>(...) -> typing.List[ClientFacingRespiratoryRateTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.respiratory_rate(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">ige</a>(...) -> typing.List[ClientFacingIgeTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.ige(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">igg</a>(...) -> typing.List[ClientFacingIggTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.igg(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">hypnogram</a>(...) -> typing.List[ClientFacingHypnogramTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.hypnogram(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">hrv</a>(...) -> typing.List[ClientFacingHrvTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.hrv(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">heartrate</a>(...) -> typing.List[ClientFacingHeartRateTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.heartrate(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">glucose</a>(...) -> typing.List[ClientFacingGlucoseTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.glucose(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">cholesterol_triglycerides</a>(...) -> typing.List[ClientFacingCholesterolTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.cholesterol_triglycerides(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">cholesterol_total</a>(...) -> typing.List[ClientFacingCholesterolTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.cholesterol_total(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">cholesterol_ldl</a>(...) -> typing.List[ClientFacingCholesterolTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.cholesterol_ldl(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">cholesterol_hdl</a>(...) -> typing.List[ClientFacingCholesterolTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.cholesterol_hdl(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">cholesterol</a>(...) -> typing.List[ClientFacingCholesterolTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.cholesterol(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">body_weight</a>(...) -> typing.List[ClientFacingBodyWeightTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.body_weight(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">body_fat</a>(...) -> typing.List[ClientFacingBodyFatTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.body_fat(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">blood_oxygen</a>(...) -> typing.List[ClientFacingBloodOxygenTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.blood_oxygen(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">electrocardiogram_voltage</a>(...) -> typing.List[ClientFacingElectrocardiogramVoltageTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.electrocardiogram_voltage(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.vitals.<a href="src/junction/vitals/client.py">blood_pressure</a>(...) -> typing.List[ClientFacingBloodPressureTimeseries]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.vitals.blood_pressure(
    user_id="user_id",
    provider="provider",
    start_date="start_date",
    end_date="end_date",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `str` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[str]` — Provider oura/strava etc
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[str]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## User
<details><summary><code>client.user.<a href="src/junction/user/client.py">get_all</a>(...) -> PaginatedUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET All users for team.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_all(
    offset=1,
    limit=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**offset:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">create</a>(...) -> ClientFacingUser</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST Create a Vital user given a client_user_id and returns the user_id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.create(
    client_user_id="client_user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**client_user_id:** `str` — A unique ID representing the end user. Typically this will be a user ID from your application. Personally identifiable information, such as an email address or phone number, should not be used in the client_user_id.
    
</dd>
</dl>

<dl>
<dd>

**fallback_time_zone:** `typing.Optional[str]` 


    Fallback time zone of the user, in the form of a valid IANA tzdatabase identifier (e.g., `Europe/London` or `America/Los_Angeles`).
    Used when pulling data from sources that are completely time zone agnostic (e.g., all time is relative to UTC clock, without any time zone attributions on data points).
    
    
</dd>
</dl>

<dl>
<dd>

**fallback_birth_date:** `typing.Optional[str]` — Fallback date of birth of the user, in YYYY-mm-dd format. Used for calculating max heartrate for providers that don not provide users' age.
    
</dd>
</dl>

<dl>
<dd>

**ingestion_start:** `typing.Optional[str]` — Starting bound for user [data ingestion bounds](https://docs.tryvital.io/wearables/providers/data-ingestion-bounds).
    
</dd>
</dl>

<dl>
<dd>

**ingestion_end:** `typing.Optional[str]` — Ending bound for user [data ingestion bounds](https://docs.tryvital.io/wearables/providers/data-ingestion-bounds).
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_team_metrics</a>() -> MetricsResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET metrics for team.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_team_metrics()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_connected_providers</a>(...) -> typing.Dict[str, typing.List[ClientFacingProviderWithStatus]]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET Users connected providers
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_connected_providers(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_latest_user_info</a>(...) -> UserInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_latest_user_info(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">create_insurance</a>(...) -> ClientFacingInsurance</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, ResponsibleRelationship, VitalCoreSchemasDbSchemasLabTestInsurancePersonDetails, Gender, Address
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.create_insurance(
    user_id="user_id",
    payor_code="payor_code",
    member_id="member_id",
    relationship=ResponsibleRelationship.SELF,
    insured=VitalCoreSchemasDbSchemasLabTestInsurancePersonDetails(
        first_name="first_name",
        last_name="last_name",
        gender=Gender.FEMALE,
        address=Address(
            first_line="first_line",
            country="country",
            zip="zip",
            city="city",
            state="state",
        ),
        dob="dob",
        email="email",
        phone_number="phone_number",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**payor_code:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**member_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**relationship:** `ResponsibleRelationship` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**insured:** `VitalCoreSchemasDbSchemasLabTestInsurancePersonDetails` 
    
</dd>
</dl>

<dl>
<dd>

**group_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**guarantor:** `typing.Optional[GuarantorDetails]` 
    
</dd>
</dl>

<dl>
<dd>

**is_primary:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_latest_insurance</a>(...) -> ClientFacingInsurance</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_latest_insurance(
    user_id="user_id",
    is_primary=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**is_primary:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">upsert_user_info</a>(...) -> UserInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, UserAddress
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.upsert_user_info(
    user_id="user_id",
    first_name="first_name",
    last_name="last_name",
    email="email",
    phone_number="phone_number",
    gender="gender",
    dob="dob",
    address=UserAddress(
        first_line="first_line",
        country="country",
        zip="zip",
        city="city",
        state="state",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**first_name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**last_name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**email:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**phone_number:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**gender:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**dob:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**address:** `UserAddress` 
    
</dd>
</dl>

<dl>
<dd>

**medical_proxy:** `typing.Optional[GuarantorDetails]` 
    
</dd>
</dl>

<dl>
<dd>

**race:** `typing.Optional[Race]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**ethnicity:** `typing.Optional[Ethnicity]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**sexual_orientation:** `typing.Optional[SexualOrientation]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**gender_identity:** `typing.Optional[GenderIdentity]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_by_client_user_id</a>(...) -> ClientFacingUser</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET user_id from client_user_id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_by_client_user_id(
    client_user_id="client_user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**client_user_id:** `str` — A unique ID representing the end user. Typically this will be a user ID number from your application. Personally identifiable information, such as an email address or phone number, should not be used in the client_user_id.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">deregister_provider</a>(...) -> UserSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, Providers
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.deregister_provider(
    user_id="user_id",
    provider=Providers.OURA,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `Providers` — Provider slug. e.g., `oura`, `fitbit`, `garmin`.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get</a>(...) -> ClientFacingUser</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">delete</a>(...) -> UserSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.delete(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">patch</a>(...)</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.patch(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**fallback_time_zone:** `typing.Optional[str]` 


    Fallback time zone of the user, in the form of a valid IANA tzdatabase identifier (e.g., `Europe/London` or `America/Los_Angeles`).
    Used when pulling data from sources that are completely time zone agnostic (e.g., all time is relative to UTC clock, without any time zone attributions on data points).
    
    
</dd>
</dl>

<dl>
<dd>

**fallback_birth_date:** `typing.Optional[str]` — Fallback date of birth of the user, in YYYY-mm-dd format. Used for calculating max heartrate for providers that don not provide users' age.
    
</dd>
</dl>

<dl>
<dd>

**ingestion_start:** `typing.Optional[str]` — Starting bound for user [data ingestion bounds](https://docs.tryvital.io/wearables/providers/data-ingestion-bounds).
    
</dd>
</dl>

<dl>
<dd>

**ingestion_end:** `typing.Optional[str]` — Ending bound for user [data ingestion bounds](https://docs.tryvital.io/wearables/providers/data-ingestion-bounds).
    
</dd>
</dl>

<dl>
<dd>

**client_user_id:** `typing.Optional[str]` — A unique ID representing the end user. Typically this will be a user ID from your application. Personally identifiable information, such as an email address or phone number, should not be used in the client_user_id.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">undo_delete</a>(...) -> UserSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.undo_delete(
    user_id="user_id",
    client_user_id="client_user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `typing.Optional[str]` — User ID to undo deletion. Mutually exclusive with `client_user_id`.
    
</dd>
</dl>

<dl>
<dd>

**client_user_id:** `typing.Optional[str]` — Client User ID to undo deletion. Mutually exclusive with `user_id`.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">refresh</a>(...) -> UserRefreshSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Trigger a manual refresh for a specific user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.refresh(
    user_id="user_id",
    timeout=1.1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**timeout:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_devices</a>(...) -> typing.List[ClientFacingDevice]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_devices(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_device</a>(...) -> ClientFacingDevice</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_device(
    user_id="user_id",
    device_id="device_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**device_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">get_user_sign_in_token</a>(...) -> UserSignInTokenResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.get_user_sign_in_token(
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="src/junction/user/client.py">create_portal_url</a>(...) -> CreateUserPortalUrlResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment
from junction.user import CreateUserPortalUrlBodyContext

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.user.create_portal_url(
    user_id="user_id",
    context=CreateUserPortalUrlBodyContext.LAUNCH,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**context:** `CreateUserPortalUrlBodyContext` 

`launch`: Generates a short-lived (minutes) portal URL that is intended for launching a user from your
authenticated web context directly into the Junction User Portal. This URL is not suitable for asynchronous
communications due to its verbosity as well as short-lived nature.

`communications`: Generates a long-lived (weeks) but shortened portal URL that is suitable for Emails, SMS
messages and other communication channels. Users may be asked to verify their identity with Email and SMS
authentication, e.g., when they open a short link on a new device. ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**order_id:** `typing.Optional[str]` — If specified, the generated URL will deeplink to the specified Order.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Team
<details><summary><code>client.team.<a href="src/junction/team/client.py">get</a>(...) -> ClientFacingTeam</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get team.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.team.get(
    team_id="team_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/junction/team/client.py">get_user_by_id</a>(...) -> typing.List[ClientFacingUser]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search team users by user_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.team.get_user_by_id(
    query_id="query_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**query_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/junction/team/client.py">get_svix_url</a>() -> typing.Dict[str, typing.Any]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.team.get_svix_url()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/junction/team/client.py">get_source_priorities</a>(...) -> typing.List[typing.Dict[str, typing.Any]]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET source priorities.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, PriorityResource
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.team.get_source_priorities(
    data_type=PriorityResource.WORKOUTS,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**data_type:** `typing.Optional[PriorityResource]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/junction/team/client.py">update_source_priorities</a>() -> typing.List[typing.Dict[str, typing.Any]]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Patch source priorities.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.team.update_source_priorities()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/junction/team/client.py">get_physicians</a>(...) -> typing.List[ClientFacingPhysician]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.team.get_physicians(
    team_id="team_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Providers
<details><summary><code>client.providers.<a href="src/junction/providers/client.py">get_all</a>(...) -> typing.List[ClientFacingProviderDetailed]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Provider list
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.providers.get_all(
    source_type="source_type",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**source_type:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Introspect
<details><summary><code>client.introspect.<a href="src/junction/introspect/client.py">get_user_resources</a>(...) -> UserResourcesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, Providers
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.introspect.get_user_resources(
    user_id="user_id",
    provider=Providers.OURA,
    user_limit=1,
    cursor="cursor",
    next_cursor="next_cursor",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `typing.Optional[str]` — Filter by user ID.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[Providers]` 
    
</dd>
</dl>

<dl>
<dd>

**user_limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.introspect.<a href="src/junction/introspect/client.py">get_user_historical_pulls</a>(...) -> UserHistoricalPullsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, Providers
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.introspect.get_user_historical_pulls(
    user_id="user_id",
    provider=Providers.OURA,
    user_limit=1,
    cursor="cursor",
    next_cursor="next_cursor",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `typing.Optional[str]` — Filter by user ID.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[Providers]` 
    
</dd>
</dl>

<dl>
<dd>

**user_limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` — The cursor for fetching the next page, or `null` to fetch the first page.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## LabTests
<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get</a>(...) -> typing.List[ClientFacingLabTest]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET all the lab tests the team has access to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, LabTestGenerationMethodFilter, LabTestCollectionMethod, LabTestStatus
from junction.environment import JunctionEnvironment
from junction.lab_tests import GetLabTestsRequestOrderKey, GetLabTestsRequestOrderDirection

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get(
    generation_method=LabTestGenerationMethodFilter.AUTO,
    lab_slug="lab_slug",
    collection_method=LabTestCollectionMethod.TESTKIT,
    status=LabTestStatus.ACTIVE,
    marker_ids=[
        1
    ],
    provider_ids=[
        "provider_ids"
    ],
    name="name",
    order_key=GetLabTestsRequestOrderKey.PRICE,
    order_direction=GetLabTestsRequestOrderDirection.ASC,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**generation_method:** `typing.Optional[LabTestGenerationMethodFilter]` — Filter on whether auto-generated lab tests created by Vital, manually created lab tests, or all lab tests should be returned.
    
</dd>
</dl>

<dl>
<dd>

**lab_slug:** `typing.Optional[str]` — Filter by the slug of the lab for these lab tests.
    
</dd>
</dl>

<dl>
<dd>

**collection_method:** `typing.Optional[LabTestCollectionMethod]` — Filter by the collection method for these lab tests.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[LabTestStatus]` — Filter by the status of these lab tests.
    
</dd>
</dl>

<dl>
<dd>

**marker_ids:** `typing.Optional[typing.Union[typing.Optional[int], typing.Sequence[typing.Optional[int]]]]` — Filter to only include lab tests containing these marker IDs.
    
</dd>
</dl>

<dl>
<dd>

**provider_ids:** `typing.Optional[typing.Union[typing.Optional[str], typing.Sequence[typing.Optional[str]]]]` — Filter to only include lab tests containing these provider IDs.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — Filter by the name of the lab test (a case-insensitive substring search).
    
</dd>
</dl>

<dl>
<dd>

**order_key:** `typing.Optional[GetLabTestsRequestOrderKey]` 
    
</dd>
</dl>

<dl>
<dd>

**order_direction:** `typing.Optional[GetLabTestsRequestOrderDirection]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">create</a>(...) -> ClientFacingLabTest</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, LabTestCollectionMethod
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.create(
    name="name",
    method=LabTestCollectionMethod.TESTKIT,
    description="description",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**method:** `LabTestCollectionMethod` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**marker_ids:** `typing.Optional[typing.List[int]]` 
    
</dd>
</dl>

<dl>
<dd>

**provider_ids:** `typing.Optional[typing.List[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**fasting:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**lab_slug:** `typing.Optional[Labs]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_by_id</a>(...) -> ClientFacingLabTest</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET all the lab tests the team has access to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_by_id(
    lab_test_id="lab_test_id",
    lab_account_id="lab_account_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab_test_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` — The lab account ID. This lab account is used to determine the availability of markers and lab tests.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">update_lab_test</a>(...) -> ClientFacingLabTest</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.update_lab_test(
    lab_test_id="lab_test_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab_test_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**active:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_markers</a>(...) -> GetMarkersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List active and orderable markers for a given Lab. Note that reflex markers are not included.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_markers(
    lab_id=[
        1
    ],
    lab_slug="lab_slug",
    name="name",
    a_la_carte_enabled=True,
    lab_account_id="lab_account_id",
    page=1,
    size=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab_id:** `typing.Optional[typing.Union[typing.Optional[int], typing.Sequence[typing.Optional[int]]]]` — The identifier Vital assigned to a lab partner.
    
</dd>
</dl>

<dl>
<dd>

**lab_slug:** `typing.Optional[str]` — The slug of the lab for these markers. If both lab_id and lab_slug are provided, lab_slug will be used.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — The name or test code of an individual biomarker or a panel.
    
</dd>
</dl>

<dl>
<dd>

**a_la_carte_enabled:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` — The lab account ID. This lab account is used to determine the availability of markers and lab tests.
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**size:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_markers_for_order_set</a>(...) -> GetMarkersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_markers_for_order_set(
    page=1,
    size=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `OrderSetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**size:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_markers_for_lab_test</a>(...) -> GetMarkersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all markers for a given Lab Test, as well as any associated reflex markers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_markers_for_lab_test(
    lab_test_id="lab_test_id",
    lab_account_id="lab_account_id",
    page=1,
    size=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab_test_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` — The lab account ID. This lab account is used to determine the availability of markers and lab tests.
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**size:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_markers_by_lab_and_provider_id</a>(...) -> ClientFacingMarker</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET a specific marker for the given lab and provider_id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_markers_by_lab_and_provider_id(
    provider_id="provider_id",
    lab_id=1,
    lab_account_id="lab_account_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**provider_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**lab_id:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` — The lab account ID. This lab account is used to determine the availability of markers and lab tests.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_labs</a>() -> typing.List[ClientFacingLab]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET all the labs.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_labs()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_paginated</a>(...) -> LabTestResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET lab tests the team has access to as a paginated list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, LabTestGenerationMethodFilter, LabTestCollectionMethod, LabTestStatus
from junction.environment import JunctionEnvironment
from junction.lab_tests import GetPaginatedLabTestsRequestOrderKey, GetPaginatedLabTestsRequestOrderDirection

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_paginated(
    lab_test_limit=1,
    next_cursor="next_cursor",
    generation_method=LabTestGenerationMethodFilter.AUTO,
    lab_slug="lab_slug",
    collection_method=LabTestCollectionMethod.TESTKIT,
    status=LabTestStatus.ACTIVE,
    marker_ids=[
        1
    ],
    provider_ids=[
        "provider_ids"
    ],
    name="name",
    order_key=GetPaginatedLabTestsRequestOrderKey.PRICE,
    order_direction=GetPaginatedLabTestsRequestOrderDirection.ASC,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab_test_limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**generation_method:** `typing.Optional[LabTestGenerationMethodFilter]` — Filter on whether auto-generated lab tests created by Vital, manually created lab tests, or all lab tests should be returned.
    
</dd>
</dl>

<dl>
<dd>

**lab_slug:** `typing.Optional[str]` — Filter by the slug of the lab for these lab tests.
    
</dd>
</dl>

<dl>
<dd>

**collection_method:** `typing.Optional[LabTestCollectionMethod]` — Filter by the collection method for these lab tests.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[LabTestStatus]` — Filter by the status of these lab tests.
    
</dd>
</dl>

<dl>
<dd>

**marker_ids:** `typing.Optional[typing.Union[typing.Optional[int], typing.Sequence[typing.Optional[int]]]]` — Filter to only include lab tests containing these marker IDs.
    
</dd>
</dl>

<dl>
<dd>

**provider_ids:** `typing.Optional[typing.Union[typing.Optional[str], typing.Sequence[typing.Optional[str]]]]` — Filter to only include lab tests containing these provider IDs.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — Filter by the name of the lab test (a case-insensitive substring search).
    
</dd>
</dl>

<dl>
<dd>

**order_key:** `typing.Optional[GetPaginatedLabTestsRequestOrderKey]` 
    
</dd>
</dl>

<dl>
<dd>

**order_direction:** `typing.Optional[GetPaginatedLabTestsRequestOrderDirection]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_lab_test_collection_instruction_pdf</a>(...) -> typing.Iterator[bytes]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_lab_test_collection_instruction_pdf(
    lab_test_id="lab_test_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab_test_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_orders</a>(...) -> GetOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET many orders with filters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, OrderLowLevelStatus, LabTestCollectionMethod, Interpretation, OrderActivationType
from junction.environment import JunctionEnvironment
import datetime
from junction.lab_tests import GetOrdersLabTestsRequestOrderKey, GetOrdersLabTestsRequestOrderDirection

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_orders(
    search_input="search_input",
    start_date=datetime.datetime.fromisoformat("2024-01-15T09:30:00+00:00"),
    end_date=datetime.datetime.fromisoformat("2024-01-15T09:30:00+00:00"),
    updated_start_date=datetime.datetime.fromisoformat("2024-01-15T09:30:00+00:00"),
    updated_end_date=datetime.datetime.fromisoformat("2024-01-15T09:30:00+00:00"),
    status=[
        OrderLowLevelStatus.ORDERED
    ],
    order_key=GetOrdersLabTestsRequestOrderKey.CREATED_AT,
    order_direction=GetOrdersLabTestsRequestOrderDirection.ASC,
    order_type=[
        LabTestCollectionMethod.TESTKIT
    ],
    is_critical=True,
    interpretation=Interpretation.NORMAL,
    order_activation_types=[
        OrderActivationType.CURRENT
    ],
    user_id="user_id",
    patient_name="patient_name",
    shipping_recipient_name="shipping_recipient_name",
    order_ids=[
        "order_ids"
    ],
    order_transaction_id="order_transaction_id",
    page=1,
    size=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**search_input:** `typing.Optional[str]` — Search by order id, user id, patient name, shipping dob, or shipping recipient name.
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `typing.Optional[datetime.datetime]` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**end_date:** `typing.Optional[datetime.datetime]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 23:59:59
    
</dd>
</dl>

<dl>
<dd>

**updated_start_date:** `typing.Optional[datetime.datetime]` — Date from in YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**updated_end_date:** `typing.Optional[datetime.datetime]` — Date to YYYY-MM-DD or ISO formatted date time. If a date is provided without a time, the time will be set to 00:00:00
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Union[typing.Optional[OrderLowLevelStatus], typing.Sequence[typing.Optional[OrderLowLevelStatus]]]]` — Filter by low level status.
    
</dd>
</dl>

<dl>
<dd>

**order_key:** `typing.Optional[GetOrdersLabTestsRequestOrderKey]` — Order key to sort by.
    
</dd>
</dl>

<dl>
<dd>

**order_direction:** `typing.Optional[GetOrdersLabTestsRequestOrderDirection]` — Order direction to sort by.
    
</dd>
</dl>

<dl>
<dd>

**order_type:** `typing.Optional[typing.Union[typing.Optional[LabTestCollectionMethod], typing.Sequence[typing.Optional[LabTestCollectionMethod]]]]` — Filter by method used to perform the lab test.
    
</dd>
</dl>

<dl>
<dd>

**is_critical:** `typing.Optional[bool]` — Filter by critical order status.
    
</dd>
</dl>

<dl>
<dd>

**interpretation:** `typing.Optional[Interpretation]` — Filter by result interpretation of the lab test.
    
</dd>
</dl>

<dl>
<dd>

**order_activation_types:** `typing.Optional[typing.Union[typing.Optional[OrderActivationType], typing.Sequence[typing.Optional[OrderActivationType]]]]` — Filter by activation type.
    
</dd>
</dl>

<dl>
<dd>

**user_id:** `typing.Optional[str]` — Filter by user ID.
    
</dd>
</dl>

<dl>
<dd>

**patient_name:** `typing.Optional[str]` — Filter by patient name.
    
</dd>
</dl>

<dl>
<dd>

**shipping_recipient_name:** `typing.Optional[str]` — Filter by shipping recipient name.
    
</dd>
</dl>

<dl>
<dd>

**order_ids:** `typing.Optional[typing.Union[typing.Optional[str], typing.Sequence[typing.Optional[str]]]]` — Filter by order ids.
    
</dd>
</dl>

<dl>
<dd>

**order_transaction_id:** `typing.Optional[str]` — Filter by order transaction ID
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**size:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_phlebotomy_appointment_availability</a>(...) -> AppointmentAvailabilitySlots</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the available time slots to book an appointment with a phlebotomist
for the given address and order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_phlebotomy_appointment_availability(
    start_date="start_date",
    first_line="first_line",
    city="city",
    state="state",
    zip_code="zip_code",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `UsAddress` — At-home phlebotomy appointment address.
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `typing.Optional[str]` — Start date for appointment availability
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">book_phlebotomy_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Book an at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.book_phlebotomy_appointment(
    order_id="order_id",
    booking_key="booking_key",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request:** `AppointmentBookingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">request_phlebotomy_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Request an at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, UsAddress, AppointmentProvider
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.request_phlebotomy_appointment(
    order_id="order_id",
    address=UsAddress(
        first_line="first_line",
        city="city",
        state="state",
        zip_code="zip_code",
    ),
    provider=AppointmentProvider.GETLABS,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**address:** `UsAddress` — At-home phlebotomy appointment address.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `AppointmentProvider` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**appointment_notes:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">reschedule_phlebotomy_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Reschedule a previously booked at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.reschedule_phlebotomy_appointment(
    order_id="order_id",
    booking_key="booking_key",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request:** `AppointmentRescheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">cancel_phlebotomy_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a previously booked at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.cancel_phlebotomy_appointment(
    order_id="order_id",
    cancellation_reason_id="cancellation_reason_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**cancellation_reason_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**notes:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_phlebotomy_appointment_cancellation_reason</a>() -> typing.List[ClientFacingAppointmentCancellationReason]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the list of reasons for cancelling an at-home phlebotomy appointment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_phlebotomy_appointment_cancellation_reason()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_phlebotomy_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the appointment associated with an order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_phlebotomy_appointment(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_area_info</a>(...) -> AreaInfo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET information about an area with respect to lab-testing.

Information returned:
* Whether a given zip code is served by our Phlebotomy network.
* List of Lab locations in the area.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, AllowedRadius, ClientFacingLabs
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_area_info(
    zip_code="zip_code",
    radius=AllowedRadius.TEN,
    lab=ClientFacingLabs.QUEST,
    labs=[
        ClientFacingLabs.QUEST
    ],
    lab_account_id="lab_account_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**zip_code:** `str` — Zip code of the area to check
    
</dd>
</dl>

<dl>
<dd>

**radius:** `typing.Optional[AllowedRadius]` — Radius in which to search in miles
    
</dd>
</dl>

<dl>
<dd>

**lab:** `typing.Optional[ClientFacingLabs]` — Lab to check for PSCs
    
</dd>
</dl>

<dl>
<dd>

**labs:** `typing.Optional[typing.Union[typing.Optional[ClientFacingLabs], typing.Sequence[typing.Optional[ClientFacingLabs]]]]` — List of labs to check for PSCs
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` — Lab Account ID to use for availability checks
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_psc_info</a>(...) -> PscInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, AllowedRadius, LabLocationCapability
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_psc_info(
    zip_code="zip_code",
    lab_id=1,
    radius=AllowedRadius.TEN,
    capabilities=[
        LabLocationCapability.STAT
    ],
    lab_account_id="lab_account_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**zip_code:** `str` — Zip code of the area to check
    
</dd>
</dl>

<dl>
<dd>

**lab_id:** `int` — Lab ID to check for PSCs
    
</dd>
</dl>

<dl>
<dd>

**radius:** `typing.Optional[AllowedRadius]` — Radius in which to search in miles. Note that we limit to 30 PSCs.
    
</dd>
</dl>

<dl>
<dd>

**capabilities:** `typing.Optional[typing.Union[typing.Optional[LabLocationCapability], typing.Sequence[typing.Optional[LabLocationCapability]]]]` — Filter for only locations with certain capabilities
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` — Lab Account ID to use for availability checks
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_order_psc_info</a>(...) -> PscInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, AllowedRadius, LabLocationCapability
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_order_psc_info(
    order_id="order_id",
    radius=AllowedRadius.TEN,
    capabilities=[
        LabLocationCapability.STAT
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**radius:** `typing.Optional[AllowedRadius]` — Radius in which to search in miles
    
</dd>
</dl>

<dl>
<dd>

**capabilities:** `typing.Optional[typing.Union[typing.Optional[LabLocationCapability], typing.Sequence[typing.Optional[LabLocationCapability]]]]` — Filter for only locations with certain capabilities
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_result_pdf</a>(...) -> typing.Iterator[bytes]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint returns the lab results for the order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_result_pdf(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_result_metadata</a>(...) -> LabResultsMetadata</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return metadata related to order results, such as lab metadata,
provider and sample dates.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_result_metadata(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_result_raw</a>(...) -> LabResultsRaw</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return both metadata and raw json test data
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_result_raw(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_labels_pdf</a>(...) -> typing.Iterator[bytes]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint returns the printed labels for the order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment
import datetime

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_labels_pdf(
    order_id="order_id",
    collection_date=datetime.datetime.fromisoformat("2024-01-15T09:30:00+00:00"),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**collection_date:** `datetime.datetime` — Collection date
    
</dd>
</dl>

<dl>
<dd>

**number_of_labels:** `typing.Optional[int]` — Number of labels to generate
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_psc_appointment_availability</a>(...) -> AppointmentAvailabilitySlots</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, AppointmentPscLabs, AllowedRadius
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_psc_appointment_availability(
    lab=AppointmentPscLabs.QUEST,
    start_date="start_date",
    site_codes=[
        "site_codes"
    ],
    zip_code="zip_code",
    radius=AllowedRadius.TEN,
    allow_stale=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab:** `AppointmentPscLabs` — Lab to check for availability
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `typing.Optional[str]` — Start date for appointment availability
    
</dd>
</dl>

<dl>
<dd>

**site_codes:** `typing.Optional[typing.Union[typing.Optional[str], typing.Sequence[typing.Optional[str]]]]` — List of site codes to fetch availability for
    
</dd>
</dl>

<dl>
<dd>

**zip_code:** `typing.Optional[str]` — Zip code of the area to check
    
</dd>
</dl>

<dl>
<dd>

**radius:** `typing.Optional[AllowedRadius]` — Radius in which to search in miles
    
</dd>
</dl>

<dl>
<dd>

**allow_stale:** `typing.Optional[bool]` — If true, allows cached availability data to be returned.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">book_psc_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.book_psc_appointment(
    order_id="order_id",
    booking_key="booking_key",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request:** `AppointmentBookingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**idempotency_key:** `typing.Optional[str]` — [!] This feature (Idempotency Key) is under closed beta. Idempotency Key support for booking PSC appointment.
    
</dd>
</dl>

<dl>
<dd>

**idempotency_error:** `typing.Optional[typing.Literal]` — If `no-cache`, applies idempotency only to successful outcomes.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">reschedule_psc_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.reschedule_psc_appointment(
    order_id="order_id",
    booking_key="booking_key",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request:** `AppointmentRescheduleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">cancel_psc_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.cancel_psc_appointment(
    order_id="order_id",
    cancellation_reason_id="cancellationReasonId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**cancellation_reason_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**note:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_psc_appointment_cancellation_reason</a>() -> typing.List[ClientFacingAppointmentCancellationReason]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_psc_appointment_cancellation_reason()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_psc_appointment</a>(...) -> ClientFacingAppointment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the appointment associated with an order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_psc_appointment(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_order_collection_instruction_pdf</a>(...) -> typing.Iterator[bytes]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET collection instructions for an order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_order_collection_instruction_pdf(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_order_requistion_pdf</a>(...) -> typing.Iterator[bytes]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET requisition pdf for an order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_order_requistion_pdf(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_order_abn_pdf</a>(...) -> typing.Iterator[bytes]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET ABN pdf for an order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_order_abn_pdf(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">get_order</a>(...) -> ClientFacingOrder</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

GET individual order by ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.get_order(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">create_order</a>(...) -> PostOrderResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, PatientDetailsWithValidation, Gender, PatientAddressWithValidation
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.create_order(
    user_id="user_id",
    patient_details=PatientDetailsWithValidation(
        first_name="first_name",
        last_name="last_name",
        dob="dob",
        gender=Gender.FEMALE,
        phone_number="phone_number",
        email="email",
    ),
    patient_address=PatientAddressWithValidation(
        first_line="first_line",
        city="city",
        state="state",
        zip="zip",
        country="country",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**patient_details:** `PatientDetailsWithValidation` 
    
</dd>
</dl>

<dl>
<dd>

**patient_address:** `PatientAddressWithValidation` 
    
</dd>
</dl>

<dl>
<dd>

**idempotency_key:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**idempotency_error:** `typing.Optional[typing.Literal]` 
    
</dd>
</dl>

<dl>
<dd>

**lab_test_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**order_set:** `typing.Optional[OrderSetRequest]` 
    
</dd>
</dl>

<dl>
<dd>

**collection_method:** `typing.Optional[LabTestCollectionMethod]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**physician:** `typing.Optional[PhysicianCreateRequest]` 
    
</dd>
</dl>

<dl>
<dd>

**health_insurance:** `typing.Optional[HealthInsuranceCreateRequest]` 
    
</dd>
</dl>

<dl>
<dd>

**priority:** `typing.Optional[bool]` — Defines whether order is priority or not. For some labs, this refers to a STAT order.
    
</dd>
</dl>

<dl>
<dd>

**billing_type:** `typing.Optional[Billing]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**icd_codes:** `typing.Optional[typing.List[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**consents:** `typing.Optional[typing.List[Consent]]` 
    
</dd>
</dl>

<dl>
<dd>

**activate_by:** `typing.Optional[str]` — Schedule an Order to be processed in a future date.
    
</dd>
</dl>

<dl>
<dd>

**aoe_answers:** `typing.Optional[typing.List[AoEAnswer]]` 
    
</dd>
</dl>

<dl>
<dd>

**passthrough:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**clinical_notes:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**creator_member_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">import_order</a>(...) -> PostOrderResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, Billing, OrderSetRequest, LabTestCollectionMethod, PatientDetailsWithValidation, Gender, PatientAddress
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.import_order(
    user_id="user_id",
    billing_type=Billing.CLIENT_BILL,
    order_set=OrderSetRequest(),
    collection_method=LabTestCollectionMethod.TESTKIT,
    patient_details=PatientDetailsWithValidation(
        first_name="first_name",
        last_name="last_name",
        dob="dob",
        gender=Gender.FEMALE,
        phone_number="phone_number",
        email="email",
    ),
    patient_address=PatientAddress(
        receiver_name="receiver_name",
        first_line="first_line",
        city="city",
        state="state",
        zip="zip",
        country="country",
    ),
    sample_id="sample_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**billing_type:** `Billing` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**order_set:** `OrderSetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**collection_method:** `LabTestCollectionMethod` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**patient_details:** `PatientDetailsWithValidation` 
    
</dd>
</dl>

<dl>
<dd>

**patient_address:** `PatientAddress` 
    
</dd>
</dl>

<dl>
<dd>

**sample_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**physician:** `typing.Optional[PhysicianCreateRequest]` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">cancel_order</a>(...) -> PostOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

POST cancel order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.cancel_order(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">simulate_order_process</a>(...) -> typing.Any</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get available test kits.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, OrderStatus, SimulationFlags
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.simulate_order_process(
    order_id="order_id",
    final_status=OrderStatus.RECEIVED_WALK_IN_TEST_ORDERED,
    delay=1,
    request=SimulationFlags(),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**final_status:** `typing.Optional[OrderStatus]` 
    
</dd>
</dl>

<dl>
<dd>

**delay:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request:** `typing.Optional[SimulationFlags]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">update_on_site_collection_order_draw_completed</a>(...) -> PostOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

PATCH update on site collection order when draw is completed
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.update_on_site_collection_order_draw_completed(
    order_id="order_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_id:** `str` — Your Order ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_tests.<a href="src/junction/lab_tests/client.py">validate_icd_codes</a>(...) -> ValidateIcdCodesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_tests.validate_icd_codes(
    codes=[
        "codes"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**codes:** `typing.List[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Compendium
<details><summary><code>client.compendium.<a href="src/junction/compendium/client.py">search</a>(...) -> SearchCompendiumResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, SearchMode
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.compendium.search(
    mode=SearchMode.CANONICAL,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**mode:** `SearchMode` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**query:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**cpt_codes:** `typing.Optional[typing.List[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**loinc_set_hash:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**labs:** `typing.Optional[typing.List[CompendiumSearchLabs]]` 
    
</dd>
</dl>

<dl>
<dd>

**include_related:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.compendium.<a href="src/junction/compendium/client.py">convert</a>(...) -> ConvertCompendiumResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, CompendiumSearchLabs
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.compendium.convert(
    target_lab=CompendiumSearchLabs.LABCORP,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**target_lab:** `CompendiumSearchLabs` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**lab_test_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider_ids:** `typing.Optional[typing.List[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## LabAccount
<details><summary><code>client.lab_account.<a href="src/junction/lab_account/client.py">get_team_lab_accounts</a>(...) -> GetTeamLabAccountsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, LabAccountStatus
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_account.get_team_lab_accounts(
    lab_account_id="lab_account_id",
    status=LabAccountStatus.ACTIVE,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[LabAccountStatus]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## OrderTransaction
<details><summary><code>client.order_transaction.<a href="src/junction/order_transaction/client.py">get_transaction</a>(...) -> GetOrderTransactionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.order_transaction.get_transaction(
    transaction_id="transaction_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**transaction_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.order_transaction.<a href="src/junction/order_transaction/client.py">get_transaction_result</a>(...) -> LabResultsRaw</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.order_transaction.get_transaction_result(
    transaction_id="transaction_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**transaction_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.order_transaction.<a href="src/junction/order_transaction/client.py">get_transaction_result_pdf</a>(...) -> typing.Iterator[bytes]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.order_transaction.get_transaction_result_pdf(
    transaction_id="transaction_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**transaction_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Testkit
<details><summary><code>client.testkit.<a href="src/junction/testkit/client.py">register</a>(...) -> PostOrderResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, PatientDetailsWithValidation, Gender, PatientAddressWithValidation
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.testkit.register(
    sample_id="sample_id",
    patient_details=PatientDetailsWithValidation(
        first_name="first_name",
        last_name="last_name",
        dob="dob",
        gender=Gender.FEMALE,
        phone_number="phone_number",
        email="email",
    ),
    patient_address=PatientAddressWithValidation(
        first_line="first_line",
        city="city",
        state="state",
        zip="zip",
        country="country",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sample_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**patient_details:** `PatientDetailsWithValidation` 
    
</dd>
</dl>

<dl>
<dd>

**patient_address:** `PatientAddressWithValidation` 
    
</dd>
</dl>

<dl>
<dd>

**user_id:** `typing.Optional[str]` — The user ID of the patient.
    
</dd>
</dl>

<dl>
<dd>

**physician:** `typing.Optional[PhysicianCreateRequestBase]` 
    
</dd>
</dl>

<dl>
<dd>

**health_insurance:** `typing.Optional[HealthInsuranceCreateRequest]` 
    
</dd>
</dl>

<dl>
<dd>

**consents:** `typing.Optional[typing.List[Consent]]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.testkit.<a href="src/junction/testkit/client.py">create_order</a>(...) -> PostOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates an order for an unregistered testkit
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, ShippingAddressWithValidation
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.testkit.create_order(
    user_id="user_id",
    lab_test_id="lab_test_id",
    shipping_details=ShippingAddressWithValidation(
        receiver_name="receiver_name",
        first_line="first_line",
        city="city",
        state="state",
        zip="zip",
        country="country",
        phone_number="phone_number",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**lab_test_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**shipping_details:** `ShippingAddressWithValidation` 
    
</dd>
</dl>

<dl>
<dd>

**passthrough:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**lab_account_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Order
<details><summary><code>client.order.<a href="src/junction/order/client.py">resend_events</a>(...) -> ResendWebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Replay a webhook for a given set of orders
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.order.resend_events()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**order_ids:** `typing.Optional[typing.List[str]]` 
    
</dd>
</dl>

<dl>
<dd>

**start_at:** `typing.Optional[datetime.datetime]` 
    
</dd>
</dl>

<dl>
<dd>

**end_at:** `typing.Optional[datetime.datetime]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Insurance
<details><summary><code>client.insurance.<a href="src/junction/insurance/client.py">search_get_payor_info</a>(...) -> typing.List[ClientFacingPayorSearchResponse]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, PayorCodeExternalProvider
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.insurance.search_get_payor_info(
    insurance_name="insurance_name",
    provider=PayorCodeExternalProvider.CHANGE_HEALTHCARE,
    provider_payor_id="provider_payor_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**insurance_name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[PayorCodeExternalProvider]` 
    
</dd>
</dl>

<dl>
<dd>

**provider_payor_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.insurance.<a href="src/junction/insurance/client.py">search_payor_info</a>(...) -> typing.List[ClientFacingPayorSearchResponseDeprecated]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.insurance.search_payor_info()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**insurance_name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[PayorCodeExternalProvider]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**provider_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.insurance.<a href="src/junction/insurance/client.py">search_diagnosis</a>(...) -> typing.List[ClientFacingDiagnosisInformation]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.insurance.search_diagnosis(
    diagnosis_query="diagnosis_query",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**diagnosis_query:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Payor
<details><summary><code>client.payor.<a href="src/junction/payor/client.py">create_payor</a>(...) -> ClientFacingPayor</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, Address
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.payor.create_payor(
    name="name",
    address=Address(
        first_line="first_line",
        country="country",
        zip="zip",
        city="city",
        state="state",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**address:** `Address` 
    
</dd>
</dl>

<dl>
<dd>

**provider:** `typing.Optional[PayorCodeExternalProvider]` — ℹ️ This enum is non-exhaustive.
    
</dd>
</dl>

<dl>
<dd>

**provider_payor_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## LabReport
<details><summary><code>client.lab_report.<a href="src/junction/lab_report/client.py">parser_create_job</a>(...) -> ParsingJob</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a parse job, uploads the file(s) to provider, persists the job row,
and starts the ParseLabReport. Returns a generated job_id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_report.parser_create_job(
    file=["example_file"],
    user_id="user_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**file:** `typing.List[core.File]` 
    
</dd>
</dl>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**needs_human_review:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.lab_report.<a href="src/junction/lab_report/client.py">parser_get_job</a>(...) -> ParsingJob</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves the parse job status and stored result if completed.

Returns:
    ParseLabResultJobResponse with job status and parsed data (if complete)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.lab_report.parser_get_job(
    job_id="job_id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**job_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Aggregate
<details><summary><code>client.aggregate.<a href="src/junction/aggregate/client.py">query_one</a>(...) -> AggregationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction, RelativeTimeframe, Period, PeriodUnit, Query, AggregateExpr, SleepColumnExpr, SleepColumnExprSleep, AggregateExprFunc
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.aggregate.query_one(
    user_id="user_id",
    accept="*/*",
    timeframe=RelativeTimeframe(
        type="relative",
        anchor="anchor",
        past=Period(
            unit=PeriodUnit.MINUTE,
        ),
    ),
    queries=[
        Query(
            select=[
                AggregateExpr(
                    arg=SleepColumnExpr(
                        sleep=SleepColumnExprSleep.ID,
                    ),
                    func=AggregateExprFunc.MEAN,
                )
            ],
        )
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**accept:** `typing.Literal` 
    
</dd>
</dl>

<dl>
<dd>

**timeframe:** `QueryBatchTimeframe` 
    
</dd>
</dl>

<dl>
<dd>

**queries:** `typing.List[Query]` 
    
</dd>
</dl>

<dl>
<dd>

**config:** `typing.Optional[QueryConfig]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.aggregate.<a href="src/junction/aggregate/client.py">get_result_table_for_continuous_query</a>(...) -> AggregationResult</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.aggregate.get_result_table_for_continuous_query(
    user_id="user_id",
    query_id_or_slug="query_id_or_slug",
    accept="*/*",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**query_id_or_slug:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**accept:** `typing.Literal` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.aggregate.<a href="src/junction/aggregate/client.py">get_task_history_for_continuous_query</a>(...) -> ContinuousQueryTaskHistoryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from junction import Junction
from junction.environment import JunctionEnvironment

client = Junction(
    api_key="<value>",
    environment=JunctionEnvironment.PRODUCTION,
)

client.aggregate.get_task_history_for_continuous_query(
    user_id="user_id",
    query_id_or_slug="query_id_or_slug",
    next_cursor="next_cursor",
    limit=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**query_id_or_slug:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**next_cursor:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

