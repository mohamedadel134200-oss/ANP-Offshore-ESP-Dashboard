# Dashboard QA V4 — Clarity + Requirement Audit

## Primary objective
A first-time viewer should understand, without external explanation:
1. What business problem the project addresses.
2. Which data are real ANP data and which ESP domains are synthetic.
3. What the dashboard analyzes versus what the ML model predicts.
4. That the prediction target is ESP failure risk within approximately 90 days.
5. That the website is a static last-scored snapshot, not live inference.
6. How risk bands and alerts should be interpreted operationally.
7. What the project explicitly does not predict.

## Original-request coverage
- Executive oil KPI + same-period YoY: PASS
- Gas KPI (associated + non-associated): PASS
- Produced water + volumetric water cut: PASS
- Unique fields / wells / facilities: PASS
- ESPs evaluated + alerts: PASS
- Average 90-day failure probability: PASS
- Risk distribution donut: PASS
- Monthly oil trend: PASS
- Annual oil trend with 2026 partial-year disclosure: PASS
- Production by basin / field: PASS
- Production by state: PASS
- Direct Oil vs Gas vs Water comparison: PASS (added V4)
- Water-cut trend: PASS
- Gas / water / CO2 / nitrogen injection trends: PASS
- Top 10 fields: PASS
- Operating-environment scope: PASS (added V4; supplied layer is 100% OFFSHORE)
- ESP risk donut: PASS
- Priority ESP searchable / filterable / paginated worklist: PASS
- Temperature vs vibration scatter: PASS
- Alerts by risk: PASS
- Days-since-maintenance histogram: PASS
- TEST vs OOT model table: PASS
- Global feature importance: PASS
- PoC claim boundary: PASS and elevated in UI
- Full production table with year / basin / field / state / facility / well filters + text search: PASS
- CSV exports: PASS
- Dark/light theme: PASS
- Single-file static HTML / GitHub Pages compatible: PASS
- Python scoring remains separate from static website: PASS

## Clarity corrections added in V4
- Added Project Guide as the first page.
- Added explicit Problem vs Solution explanation.
- Added end-to-end workflow from ANP data to ML risk worklist.
- Added Real / Synthetic / Static data-provenance cards.
- Added What the dashboard answers / What it does NOT claim.
- Explicitly states there is no future production forecast and no well-depletion-date prediction in this version.
- Added dynamic risk-band threshold explanation on the ESP page.
- Added model interpretation explaining the OOT recall (~78.1%) / precision (~5.1%) trade-off.
- Alerts are described as screening / prioritization signals, not confirmed failures.

## Structural QA
- Embedded production rows: 138,358 / source 138,358.
- Embedded oil total: 1,349,274,641.17446 m3 / exact source match.
- Embedded water total: 723,341,114.31629 m3 / exact source match.
- Duplicate HTML IDs: 0.
- JavaScript DOM references missing: 0.
- Chart canvases: 27.
- Chart references: 27.
- Missing/unused chart canvases: 0.
- Inline JavaScript syntax: PASS.
- ML pipeline rescoring: 423 ESPs, 162 alerts, May-2026 snapshot.

## Scientific boundary
ANP production context is real / real-derived. ESP sensor-condition variables, maintenance events and failure labels are synthetic / synthetic-derived for this academic Proof of Concept. The current model predicts probability of ESP failure within approximately 90 days; it does not provide a field-certified failure diagnosis.
