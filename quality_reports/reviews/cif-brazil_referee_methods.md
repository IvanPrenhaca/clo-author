# Methods Referee Report — JPGN

**Date:** 2026-07-13
**Manuscript:** "Chronic Intestinal Failure in Brazil: A First Estimative of Prevalence"
**Journal:** Journal of Pediatric Gastroenterology and Nutrition (JPGN)
**Referee role:** Methods / epidemiology / biostatistics, blinded, independent of domain referee
**Paper type:** Descriptive / measurement (no causal estimand)

> Persisted by the orchestrator on behalf of methods-referee (referees are read-only).

## 1. Summary
First national pediatric CIF prevalence from SIH-SUS/DATASUS (2017–2025); PN ≥60 daily-units/74-day proxy; deterministic linkage (CEP + sex + DOB); SUS counts × 1.55 (reciprocal of 64.6% SUS share, PNS 2019); headline 3.35/million; 2024 CIF-code cross-validation.

## 2. Recommendation: **Major Revision. Score 58/100.**
Strong motivation, reasonable case-finding, coherent underreporting narrative. But a disqualifying measurement gap as presented: every prevalence figure is a point estimate with no CI, no sensitivity analysis, and no error propagation for the two biggest sources (the threshold and the 1.55 scalar). All fixable with data the authors hold.

## 3. Major comments
- **M1 [ADDRESSABLE, most serious] — no uncertainty quantification.** Eqs 1–3, Table 2, all point estimates; year-over-year "23%/40% declines" asserted with no CI/test. Poisson 95% CI on 80 cases ≈ ±22%. *Fix:* exact Poisson/binomial CIs on every Table 2 cell + mean; pandemic comparison as rate ratio with CI.
- **M2 [FATAL as presented] — 1.55 scalar unaudited, drives headline, no sensitivity.** All-cause split applied to a rare high-complexity condition; held constant 9 years; never varied; whole non-SUS column is mechanically 0.55×N_SUS. Direction of bias unsigned (tertiary CIF care disproportionately SUS → 1.55 may overstate private). *Fix:* sensitivity band (1.0 SUS-only lower bound → 1.55 → all-cause); any disease-specific payer anchor; report as a range if no anchor.
- **M3 [ADDRESSABLE] — threshold untested; FP/FN structure uncharacterized.** ≥60 is a thin tail (0.42–0.78%/yr) where cut placement dominates; no neighboring-cutoff counts; within-admission vs cross-admission accumulation ambiguous. *Fix:* threshold grid (≥45/50/60/75/90); unambiguous 60/74 operationalization; FP/FN discussion.
- **M4 [ADDRESSABLE] — linkage error unquantified; precedent overstated.** CEP+sex+DOB over-collapses twins (overrepresented in this premature population → downward bias); `medinacoeli2025deterministic` is an OBSTETRICS study, doesn't transfer. *Fix:* expected false-match rate w/ multiple-birth bound; validate against the 22 code-identified patients; soften the medinacoeli claim.
- **M5 [ADDRESSABLE, potentially large] — missing-CEP exclusion unquantified, likely selective.** Dropped admissions never counted; missing CEP plausibly concentrated in the underserved N/NE/CW regions central to the paper's thesis → exclusion could mechanically manufacture the headline conclusion. *Fix:* report N/% excluded overall + by region; compare CEP-present vs absent; best/worst-case bound.
- **M6 [ADDRESSABLE] — numerator/denominator mismatch.** Scaled numerator (×1.55) over full IBGE population; consistent only if scaling perfectly reconstructs private cases (loops to M2). Define estimand (period vs point prevalence); report unscaled SUS-only prevalence as explicit lower bound.
- **M7 [ADDRESSABLE] — STROBE incomplete.** No flow diagram, no quantified exclusions, no missing-data accounting, estimand unstated.
- **M8 [TASTE→ADDRESSABLE] — CIF-code cross-validation mis-scoped.** Low uptake of a 2024 code validates "coding incomplete," NOT the PN proxy's *level*. *Fix:* report overlap — of the 22 code patients, how many does the ≥60 PN rule flag?

## 4. Minor comments (selected)
- **m1.** Table 2 annual counts sum to **1,028** vs **971** unique patients (line 153) — state the period-prevalence recurrence explicitly. [verified]
- **m2.** "daily units" (diárias) vs "days" used interchangeably — unify (INV-7).
- **m4.** Race excluded from linkage for missingness but then interpreted substantively (equity claim) — report missingness first, temper.
- **m5.** Table 1 "Max daily units" 288 (2020) exceeds a 74-day window → windowing ambiguity again.
- **m9.** `scripts/` empty at review — none of the numbers reproducible; deposit case-finding + linkage code.
- **m8 (title).** "Estimative" → "Estimate."
- Mean-prevalence arithmetic verified: nine annual values average 3.356 ≈ 3.35. [verified]

## 5. Score: 58/100 (Major Revision)
Construct validity 62 · Construction/replicability 50 · Validation 60 · Analysis 58 · Replication readiness 40.
**Editor bottom line:** real contribution, credible story, but headline rests on an unaudited scalar (M2) + untested threshold (M3), no uncertainty bounds (M1), no STROBE exclusion accounting (M5/M7). Resolvable with: Poisson CIs, scaling sensitivity band, threshold grid, quantified missing-CEP + linkage error, flow diagram, the 22-patient overlap check.
