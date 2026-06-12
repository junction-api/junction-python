## [2.0.0] - 2026-06-12
### Breaking Changes
- **`LabReportResultIsSensitive`** — removed; replace all references with the new **`LabReportResultSensitivity`** enum (same `sensitive` / `insensitive` / `unknown` values).
- **`LabReportResult.is_sensitive`** — field renamed to `sensitivity` (type is now `Optional[LabReportResultSensitivity]`); update all attribute access and keyword-argument usage.
- **`ParsingJobFailureReason.visit()`** — gains a new required `too_many_pages` keyword argument; callers that pass `visit()` arguments positionally or by keyword must add this parameter.

### Added
- **`AlignExpr`**, **`AlignExprCarry`**, **`AlignExprCarry_CarryForward`**, **`AlignExprCarry_CarryBackward`**, **`AlignExprCarry_CarryNearest`** — new types representing a post-aggregation alignment clause that materialises and fills missing datetime buckets.
- **`CarryForwardExpr`**, **`CarryBackwardExpr`**, **`CarryNearestExpr`** — standalone carry-operator models with optional `max_age` / `span` period caps.

### Changed
- **`Query.align`** — new optional field accepting an `AlignExpr`; omitting it preserves existing honest-null behaviour.
- **`OAuthProviders`** and **`Providers`** — new `GOOGLE_HEALTH` enum value added to both enums; `visit()` gains a corresponding required `google_health` parameter.

## 1.3.0 - 2026-06-05
### Added
* **`AlignExpr`** — new public symbol
* **`AlignExprCarry`** — new public symbol
* **`CarryBackwardExpr`** — new public symbol
* **`CarryForwardExpr`** — new public symbol
* **`CarryNearestExpr`** — new public symbol
### Changed
* **`Query`** — new optional field(s): align
### Beta
* **`LabReportResult`** — field(s) removed: is_sensitive
* **`LabReportResultIsSensitive`** — public symbol removed
* **`LabReportResultSensitivity`** — new public symbol
* **`ParsingJobFailureReason.visit()`** — new required parameter(s): too_many_pages

## 1.2.0 - 2026-05-27
### Added
* **`LabTestsClient.update_order()`** and **`AsyncLabTestsClient.update_order()`** — new methods to update a modifiable order's scheduled activation date (`activate_by`) via `PATCH v3/order/{order_id}`; supports rescheduling to a future date or clearing the schedule for immediate dispatch.
* **`GetOrderCommunicationSettingsResponse`**, **`PatchOrderCommunicationSettingsBody`**, and **`PatchOrderCommunicationSettingsResponse`** — new model types supporting order-level SMS communication settings management.
* **`LabReportResultIsSensitive`** and **`LabReportResultLoincMatchStatus`** — new non-exhaustive enums for classifying lab result sensitivity and LOINC match status, respectively.
* **`LabReportResult.is_sensitive`** and **`LabReportResult.loinc_match_status`** — new optional fields on `LabReportResult` using the new enum types above.

## 1.1.0 - 2026-05-07
### Added
* **`max_retries`** — new optional constructor parameter on `Junction` and `AsyncJunction` that sets the client-level default retry count (defaults to `2`); per-request `max_retries` in `request_options` still takes precedence.
### Changed
* **`pydantic-core`** dependency upper bound widened from `<2.44.0` to `<3.0.0`, allowing compatibility with newer pydantic-core releases.
* **SSE streaming** (`iter_sse` / `aiter_sse`) now uses incremental codec decoding and normalizes `\r\n` and bare `\r` line endings per the SSE specification, improving reliability with chunked streams.

## 1.0.0 - 2026-05-06
* Initial SDK generation
* 🌿 Generated with Fern
