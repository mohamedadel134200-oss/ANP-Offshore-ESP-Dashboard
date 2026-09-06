# DASHBOARD QA V11

**Result: PASS — 50/50 checks passed.**

| Check | Status | Detail |
|---|---|---|
| HTML IDs unique | PASS | 140 IDs / 0 duplicates |
| JavaScript DOM references resolved | PASS | 95 refs / missing [] |
| Chart canvases mapped | PASS | 33 chart refs / 33 canvas; missing=[] unused=[] |
| Navigation page mapping | PASS | 9 nav sections: ['guide', 'overview', 'production', 'assets', 'injection', 'interventions', 'maintenance', 'model', 'reports'] |
| JavaScript syntax | PASS | node --check PASS |
| Section transition animation installed | PASS | page + card entrance motion |
| Executive scope heading hierarchy installed | PASS | title and explanatory subtitle render on separate lines |
| Navigation motion replay installed | PASS | animation replay + smooth top reset |
| Reduced-motion accessibility | PASS | motion disabled for reduced-motion users |
| ESP history startup function resolved | PASS | renderEspHistory is defined and used; retired showHistory reference absent |
| Embedded production row count | PASS | 138,358 / 138,358 |
| Embedded measure reconciliation: oil_production_m3 | PASS | 1349274641.17446 vs 1349274641.17446 |
| Embedded measure reconciliation: condensate_production_m3 | PASS | 1620462.2270300002 vs 1620462.2270300002 |
| Embedded measure reconciliation: water_production_m3 | PASS | 723341114.31629 vs 723341114.31629 |
| Embedded measure reconciliation: gas_injection_thousand_m3 | PASS | 174487771.75351 vs 174487771.75351 |
| Embedded measure reconciliation: co2_injection_thousand_m3 | PASS | 48056355.186814606 vs 48056355.186814606 |
| Embedded measure reconciliation: nitrogen_injection_thousand_m3 | PASS | 2978.5200000000004 vs 2978.5200000000004 |
| Conformed dimension count: fields | PASS | dashboard=134 source=134 |
| Conformed dimension count: facilities | PASS | dashboard=218 source=218 |
| Conformed dimension count: wells | PASS | dashboard=2037 source=2037 |
| Conformed dimension count: basins | PASS | dashboard=9 source=9 |
| Conformed dimension count: states | PASS | dashboard=8 source=8 |
| Intervention event count | PASS | 2840 |
| Intervention matched count | PASS | 2161 |
| Intervention unmatched retained | PASS | 679 |
| Intervention matched wells | PASS | 972 |
| Intervention quality review count | PASS | 1 |
| Intervention filters are independent/reactive | PASS | local intervention filter scope |
| ESP condition-monitoring feature rows | PASS | 33,868 |
| ESP latest monitoring rows | PASS | 429 |
| ESP current-failure scoring exclusion | PASS | 6 excluded |
| ESP scoreable snapshot | PASS | 423 scoreable |
| Saved ESP model reproduces current predictions | PASS | 423 aligned / max diff 9.714e-17 |
| Saved alert count unchanged | PASS | 162 alerts |
| Primary model-ready rows | PASS | 75,032 |
| Primary positive labels | PASS | 1,454 |
| Primary deployment maturity honest | PASS | not final-trained |
| Secondary model-ready rows | PASS | 75,181 |
| Existing ESP metrics kept separate | PASS | no metric mixing |
| Production filters do not rescore ESP/model | PASS | const f=productionFilters(),err=$('filterError');if(f.from&&f.to&&f.from>f.to){err.textContent='From month cannot be after To month.';err.classList.add('show');return}err.textContent='';err.classList.remove('show');PROD= |
| Production filters update production + raw table | PASS | production scope only |
| Basin share = top 3 + Others | PASS | max 4 segments |
| Production/liquid mix <=3 segments | PASS | 3 segments |
| ESP risk = 4 governed bands | PASS | {'LOW': 203, 'MEDIUM': 58, 'HIGH': 152, 'CRITICAL': 10} |
| KPI value font enlarged | PASS | 43px |
| Responsive mobile breakpoint | PASS | mobile composition present |
| Visible latest naming has no legacy labels | PASS | {} |
| Latest ESP domain label visible | PASS | new domain terminology |
| Latest star-schema QA status | PASS | 57/58 PASS; 1 WARN; 0 FAIL |
| Source integrity status | PASS | 120/120 rehashed; 0 mismatch |

## Runtime-browser note
The execution environment blocks Chromium navigation/runtime rendering. Therefore the release was validated through exact source/data reconciliation, JavaScript syntax, complete DOM/canvas/reference mapping, filter-code isolation, and motion/accessibility source checks. The final GitHub Pages browser smoke test should still be performed after upload.