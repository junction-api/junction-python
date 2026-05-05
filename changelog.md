## 0.1.0 - 2026-05-05
### Added
* **`LabReportResultMeasurementKind`** — new enum type representing how a lab result value was derived (e.g. `direct`, `calculated`, `ratio`).
* **`LabReportResultSampleType`** — new enum type representing the biological sample used for a lab result (e.g. `urine`, `serum_plasma_blood`, `capillary_blood`).
* **`LabReportResult.sample_type`** and **`LabReportResult.measurement_kind`** — new optional fields on `LabReportResult` exposing the sample type and measurement kind for a lab result.
* **`MealInDbBaseClientFacingSource.calendar_date`** — new field providing the meal date in `YYYY-MM-DD` format, useful for providers that only expose a date rather than a full timestamp.
### Changed
* **`JunctionEnvironment`** base URLs updated from `tryvital.io` to `junction.com` for all environments (PRODUCTION, PRODUCTION_EU, SANDBOX, SANDBOX_EU).

## 0.0.1 - 2026-05-01
* Initial SDK generation
* 🌿 Generated with Fern

