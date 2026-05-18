## 1.2.0 - 2026-05-18
### Added
* **`LabTestsClient.update_order()`** and **`AsyncLabTestsClient.update_order()`** — new methods to reschedule or clear the `activate_by` date on an existing order in `ordered` or `awaiting_registration` status.
* **`LabReportResultLoincMatchStatus`** — new non-exhaustive `StrEnum` (`auto_match`, `needs_review`, `no_match`) exported from `junction` and `junction.types`.
* **`LabReportResult.loinc_match_status`** — new optional field on `LabReportResult` carrying the LOINC match status for a result.

## 1.1.0 - 2026-05-07
### Added
* **`max_retries`** — new optional constructor parameter on `Junction` and `AsyncJunction` that sets the client-level default retry count (defaults to `2`); per-request `max_retries` in `request_options` still takes precedence.
### Changed
* **`pydantic-core`** dependency upper bound widened from `<2.44.0` to `<3.0.0`, allowing compatibility with newer pydantic-core releases.
* **SSE streaming** (`iter_sse` / `aiter_sse`) now uses incremental codec decoding and normalizes `\r\n` and bare `\r` line endings per the SSE specification, improving reliability with chunked streams.

## 1.0.0 - 2026-05-06
* Initial SDK generation
* 🌿 Generated with Fern
