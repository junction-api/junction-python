## [1.5.0] - 2026-09-12
### Added
- **`CheckoutClient`** and **`AsyncCheckoutClient`** — new `checkout` sub-clients on `Junction` and `AsyncJunction` supporting the full quote-to-session lifecycle (`create_quote`, `refine_quote`, `get_quote`, `create_checkout_session`, `get_checkout_session`, `confirm_checkout_session`).
- **`RawCheckoutClient`** and **`AsyncRawCheckoutClient`** — low-level checkout clients returning raw `HttpResponse`-wrapped results for all checkout and quote operations.
- **`LabTestsClient.estimate_order_set_pricing()`** and **`AsyncLabTestsClient.estimate_order_set_pricing()`** — estimate pricing for one or more order sets given a collection modality, US state, and optional billing type.
- **Checkout and pricing models** — new types including `CheckoutQuote`, `CheckoutSession`, `CheckoutSessionStatus`, `CheckoutSessionPayment`, `EstimateOrderSetPricingResponse`, `OrderSetPricing`, and related component/condition types for detailed pricing breakdowns.
- **`ReliabilityColumnExpr`** and **`ReliabilityColumnExprReliability`** — new expression types for querying source-level data reliability metrics, usable in `QuerySelectItem`, `QueryGroupByItem`, and `UnnestExprUnnest`.
- **`WalkInCollectionNetworkSlug`** — new non-exhaustive enum identifying walk-in collection networks (`quest`, `sonora_quest`, `labcorp`, `bioreference`).
- **`ClientFacingCheckoutQuoteCreated`** — new webhook event model for checkout quote creation; `MatchReviewStatus.PENDING_CUSTOMER_REVIEW_IN_PROGRESS` enum value and `is_stale` field on `UnmatchedResult` also added.

## 1.4.0 - 2026-08-14

### Added

* **Orderable-test search** — added sync and async `CompendiumClient.search_orderable_tests()` methods and the related request and response models.
* **Unmatched lab-result management** — added sync and async methods for listing, testing, reviewing, accepting, and resolving unmatched results, together with match-review webhook models.
* **Lab-test pricing** — added pricing models and optional `include_pricing` and `lab_account_id` request fields.
* **Provider and lab coverage** — added Google Health provider and OAuth values and the MTL lab value.
* **Lab metadata** — added optional source interpretation, lab logo URL, and lab-location website fields.

### Changed

* **SSE reliability** — resumable event streams now reconnect transparently, with client- and request-level controls for enabling reconnection and limiting attempts.

### Beta

* **Aggregate and lab-report states** — added the result-table resource and processing-error parsing state without affecting the stable-surface SemVer calculation.

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
