# DASHBOARD QA V9

## Overall result
**PASS** — all automated structural, ML-governance, data-governance, scoring, API and alert-logic checks completed successfully.

## Locked current snapshot
- ESPs scored: **423**
- Operational alerts: **162**
- Snapshot month: **2026-05-01**
- Average 90-day probability: **2.391111%**

## ML governance
- Threshold sensitivity calculated row-for-row from the sealed OOT prediction artifact.
- Selected operational threshold is explicitly highlighted and compared with alternative operating points.
- Raw OOT Brier: **0.095573**
- Sigmoid-calibrated OOT Brier: **0.025790**
- Brier improvement: **0.069783**
- Calibration curve uses exact OOT rows and raw base-estimator probabilities extracted from the saved calibrated deployment model.

## Decision support
- Asset Health Card added for selected ESP.
- Local SHAP top drivers shown both as a compact decision list and detailed chart.
- Priority worklist includes the top local SHAP driver.
- SHAP is explicitly described as model explanation, not causal/root-cause diagnosis.

## Data governance
- Alias crosswalk rows: **352**
- Field groups with multiple spellings: **4**
- Facility groups with multiple spellings: **26**
- Unit registry rows: **13**
- Source/display conversion policy is documented instead of hidden.

## Email / live readiness
- Static GitHub Pages correctly reports email as unavailable without a backend.
- FastAPI backend included for scoring, upload-and-score, health/status, alert history and test email.
- First-run baseline suppression tested.
- Unchanged HIGH→HIGH duplicate suppression tested.
- MEDIUM→HIGH new alert tested.
- HIGH→CRITICAL escalation alert tested.
- API key protection tested for write endpoints.

## Structural checks
- duplicate_ids_zero: **PASS**
- missing_js_refs_zero: **PASS**
- all_chart_canvases_present: **PASS**
- v9_asset_health_present: **PASS**
- v9_threshold_present: **PASS**
- v9_calibration_present: **PASS**
- v9_email_readiness_present: **PASS**
- v9_governance_present: **PASS**
- v9_units_present: **PASS**
- esp_423: **PASS**
- alerts_162: **PASS**
- threshold_selected_once: **PASS**
- calibration_improves_brier: **PASS**
- crosswalk_nonempty: **PASS**
- units_registry_nonempty: **PASS**
