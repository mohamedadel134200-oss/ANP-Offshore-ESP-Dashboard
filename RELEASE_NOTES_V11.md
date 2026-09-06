# V11 Release Notes

## Release basis
- Baseline dashboard: last published V9.
- Update package: complete 6-Sep-2026 package.
- Naming migration: `Name Edit.docx`.

## Completed changes
- Reconciled old 57-file baseline against new 102-file package.
- Preserved unchanged production measures.
- Migrated ESP terminology/schema to ESP condition-monitoring naming.
- Added real Intervention Analytics from Fact_Intervention.
- Updated model architecture so future-intervention risk is the primary next model-ready target without inventing final model metrics.
- Kept the existing saved calibrated ESP XGBoost as a separate equipment-risk module.
- Corrected 429 monitoring cohort / 423 scoreable / 6 current-failure exclusions / 129 current ESP/BCS-linked semantics.
- Switched production entity counts to conformed star-schema dimensions: 134 fields, 218 facilities, 2,037 wells.
- Added animated section transitions and reduced-motion accessibility fallback.
- Fixed Executive scope-heading hierarchy so title/subtitle/badge render separately.
- Made source audit portable through an embedded old-baseline manifest + compressed critical reference tables.
- Updated Windows rebuild dependencies and six-gate runner.

## Final QA
- Source comparison: PASS.
- Latest naming violations in latest package / visible dashboard: 0.
- Dashboard QA: 49/49 PASS.
- Final integration validation: PASS.
- Saved ESP snapshot: 423 scoreable rows / 162 alerts / 2.391111% average probability.

## Browser-runtime note
This execution environment blocks Chromium navigation with `ERR_BLOCKED_BY_ADMINISTRATOR`, including localhost/file navigation. Therefore the final release is validated by source/data reconciliation, JavaScript syntax, DOM/canvas mapping, filter-code isolation, animation-source checks and integration QA. A final visual smoke test on the published GitHub Pages URL remains required after upload.

## V11.1 runtime hotfix — 2026-09-06
- Fixed startup `ReferenceError: showHistory is not defined`.
- Startup now calls the defined `renderEspHistory(...)` renderer.
- Patched both generated dashboard HTML and `build_dashboard_v11.py`, so future rebuilds preserve the fix.
- Added a dedicated QA regression check so this undefined startup reference cannot pass the release QA again.
