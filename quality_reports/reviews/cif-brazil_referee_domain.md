# Domain Referee Report — JPGN

**Date:** 2026-07-13
**Manuscript:** "Chronic Intestinal Failure in Brazil: A First Estimative of Prevalence"
**Journal:** Journal of Pediatric Gastroenterology and Nutrition (JPGN)
**Referee role:** Domain expert (pediatric intestinal failure / clinical nutrition), blinded, independent of methods referee

> Persisted by the orchestrator on behalf of domain-referee (referees are read-only).

## 1. Summary
Nine years (2017–2025) of SIH-SUS/DATASUS administrative data; probable pediatric CIF identified via a PN duration proxy (>=60 daily units within 74 days), deduplicated by deterministic linkage (CEP + sex + DOB). Mean national prevalence 3.35/million (0–17y) after 1.55 private-sector scaling; cohort characterized clinically; cross-validated against a 2024 CIF-specific procedure code (only 22 patients, 2 hospitals). Framed as a lower bound reflecting underdiagnosis and access inequity.

## 2. Recommendation: **Major Revision. Score 74/100.**
Genuinely first-of-its-kind, clinically meaningful, strong/current literature positioning, honest lower-bound framing, persuasive 2024-code cross-validation. But three things a clinical reviewer holds it to are unmet: (a) PN proxy false-positive risk unquantified/unbounded; (b) NO confidence intervals on any figure; (c) internal numerical inconsistencies.

## 3. Major comments
- **M1 [ADDRESSABLE] — "daily units" (diárias) ≠ "days" not validated.** ASPEN criterion is 60 *days* within 74; paper uses 60 *diárias* (a billing unit, possibly >1/day). Single most important validity question; asserted not shown. Also PN-proxy false positives (NEC recovery, post-op ileus) unbounded. *Change my mind:* DATASUS data-dictionary citation that diária ≤ 1 PN calendar day; threshold sensitivity analysis (45/60/90; within-admission vs cumulative).
- **M2 [ADDRESSABLE, non-negotiable] — no uncertainty bounds anywhere.** 3.35/M, annual series, 9–15% mortality, 70 km, and the 1.55 factor all point estimates. *Change my mind:* exact Poisson/binomial CIs per annual prevalence + mortality; national estimate as a range under a scaling-factor sensitivity band.
- **M3 [ADDRESSABLE] — internal numerical inconsistencies.** (a) Mortality: Abstract/Results say 9–15% but the 971-cohort paragraph says 6.5% died; Table 1's 11.9–15% is for ALL PN admissions, not the CIF cohort. (b) Annual SUS counts in Table 2 sum to 1,028 vs 971 unique patients — period-prevalence double-counting of persistent patients never stated. *Change my mind:* one reconciled CIF-cohort mortality used everywhere; explicit definition of the annual prevalence unit reconciling 1,028 vs 971.
- **M4 [ADDRESSABLE] — 1.55 scaling likely upward-biasing for this condition.** Established pediatric IR programs (HCPA, HC-SP) are public SUS centers, so CIF may be MORE SUS-concentrated than average admissions → 1.55 over-corrects. *Change my mind:* present unscaled SUS-only prevalence as primary strict lower bound; 1.55 as sensitivity-flanked secondary.
- **M5 [ADDRESSABLE/TASTE] — "hidden mortality" and race/equity claims over-asserted.** Hidden-mortality is inference-on-inference → label as hypothesis. Race finding infers differential access from a variable the authors elsewhere deem too incomplete to use (internally inconsistent). *Change my mind:* down-tone; quantify race completeness or present descriptively.
- **M6 [ADDRESSABLE] — STROBE gaps.** Need participant flow diagram with exclusion counts (esp. missing-CEP drop), missing-data handling, ICD-10 code appendix for Tables 3–4, quantitative linkage-error note (twin/shared-CEP collisions).

## 4. Minor comments (selected)
1. Title "Estimative" → "Estimate."
2. Abstract mortality conflicts with 6.5% (M3a).
4. Benchmark direction now handled well — verify the "high-income" qualifier is always present.
5. Beath 2011 is HPN point-prevalence, not SBS-specific — verify not mis-cited.
8. Define "alta melhorada" (an SIH-SUS discharge code, not adjudicated outcome) for non-Brazilian readers.
10. Appendix A is a "[Final]" placeholder — populate or remove.
11. natbib/plainnat authoryear vs JPGN's numbered **Vancouver** style — will need to switch for submission.
13. Verify `sacramento2024care` (already deleted) and the `mukhopadhyay2019` 85% figure.

## 5. Score: 74/100 (Major Revision)
Contribution 88 · Literature 85 · Substantive args 60 · External validity 62 · Journal fit 80. Resolving M1–M3 → mid-80s / Minor Revision.
