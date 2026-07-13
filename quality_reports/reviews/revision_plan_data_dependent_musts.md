# Revision Plan — Data-Dependent MUST Items (JPGN Major Revision)

**Date:** 2026-07-13
**Manuscript:** `paper/main.tex` — "Chronic Intestinal Failure in Brazil: A First Estimate of Prevalence"
**Source:** Editorial decision (`editorial_decision.md`) synthesizing the domain + methods referee reports.

This file documents the MUST items from the JPGN Major Revision that **cannot be done
from the manuscript alone** — they require re-running or extending the analysis on the
underlying SIH-SUS data. The `scripts/` directory is currently empty, so the analysis
that produced 3.35/million, the 971-patient cohort, and all figures is not yet in the repo.
Every item below is blocked on bringing that data/code into the project.

The text-only fixes (title, linkage-precedent softening, hidden-mortality down-tone,
race/equity reframing, "alta melhorada" definition, appendix placeholder) were already
applied in commit `ed3d7e0` and are NOT repeated here.

---

## MUST-1 — Reconcile the 1,028-vs-971 count; define the estimand

**What the paper currently says.** Results (line 153):
> "these admissions corresponded to **150,078 unique patients** … A total of **971 patients** (0.65%) had at least one admission with 60 or more daily units of PN, meeting the operational definition of CIF"

But **Table 2** (`tab:prevalencia_17anos`) lists annual "No. of SUS cases" as
148, 136, 147, 112, 86, 106, 108, 105, 80 — which **sum to 1,028** [verified], while the
text's unique-patient total is **971**.

**Referees.** Methods (m1):
> "the nine annual SUS-case counts in Table 2 … sum to **1,028**, but the text reports **971 unique CIF patients** … This is defensible but must be stated explicitly — otherwise the table appears arithmetically inconsistent with the headline N."

Domain (M3b):
> "a *period prevalence* built by summing annual counts double-counts persistent patients across years, which is conceptually inconsistent with 'unique patients.'"

**Why data is required.** The 57-patient gap is presumably patients with qualifying
admissions in ≥2 calendar years (counted once in 971, once per year in Table 2), but this
cannot be confirmed from the manuscript.

**Data operation.**
1. Query the patient-level dataset: how many unique patients have qualifying admissions in ≥2 calendar years? Confirm it explains 1,028 − 971 = 57.
2. Decide and state the **estimand** (period vs point prevalence); add one sentence to Methods + a Table 2 footnote.

---

## MUST-2 — Add confidence intervals everywhere

**What the paper currently says.** Every figure is a bare point estimate. Results (~line 155):
> "prevalence fell to 3.26 and 2.53 cases per million, reductions of approximately **23% and 40%** relative to the pre-pandemic mean"

Table 2 reports "Prevalence (per million)" as single numbers (4.20 … 2.46), no interval.

**Referees.** Methods (M1, "the single most serious defect"):
> "a Poisson 95% CI on 80 observed cases is roughly **±22%**. A clinical readership will not accept year-over-year 'declines' asserted from counts this small without at least Poisson/exact intervals."

Domain (M2, "non-negotiable for this journal"):
> "Report exact (Poisson/binomial) confidence intervals for each annual prevalence and for mortality."

**Why data is required.** CIs are computed quantities.
- Annual prevalence CIs need the case count + denominator (both in Table 2) — a short computation.
- The pandemic "23%/40% decline" should become a **rate ratio with CI** (2020 vs pre-pandemic mean).
- Mortality CIs need the CIF-cohort numerator/denominator (see MUST-5).

**Data operation.** R: `poisson.test` / `epitools::pois.exact` for each annual prevalence and mortality; rate-ratio-with-CI for the pandemic comparison. Regenerate Table 2 with interval columns.

---

## MUST-3 — Rebuild the headline as a scaling sensitivity band (editor's #1 priority)

**What the paper currently says.** Methods, scaling equation:
> "the total estimated number of cases in year *t* was obtained by scaling the observed SUS count by a factor of **1.55**:  N_total,t = N_SUS,t × 1.55"

This single scalar produces the headline **3.35/million**.

**Referees.** This is the **FATAL-as-presented** flag. Methods (M2):
> "the entire non-SUS column of Table 2 is mechanically 0.55×N_SUS … the reader cannot separate 'signal' from 'this one scalar' … 1.55 may *overstate* the private share — meaning the direction of bias is not even signed."

Editor (single most important revision):
> "Reconstruct the headline as an *honest interval rather than a point estimate* … anchor it on the unscaled SUS-only floor, flank the 1.55 with a sensitivity band."

**Why data is required.** Prevalence must be recomputed under a grid of scaling assumptions.

**Data operation.**
- **×1.0** (unscaled SUS-only) = strict lower bound → promote to *primary* estimate.
- **×1.55** = current central estimate.
- **Upper bound** from the all-cause PNS split at its plausible range.
- Ideally anchor a *disease-specific* SUS share (where RESTORE/Leite/Goldani Brazilian cohorts were treated — predominantly public centers).
- Report the national estimate as a **range**; regenerate Table 2 / the headline accordingly.

---

## MUST-4 — Validate that "diárias" (daily units) = days; resolve the 288 contradiction

**What the paper currently says.** Definition (Methods):
> "parenteral nutrition (PN) support for at least **60 days** within a consecutive 74-day interval"

Operationalization:
> "we retained only those in which the recorded duration of the PN procedure was **60 daily units (\textit{diárias}) or more**"

Table 1 reports a **"Max daily units" of 288 in 2020** — which exceeds a 74-day window.

**Referees.** Domain (M1, "the single most important validity question for the whole paper"):
> "In SIH-SUS the 'diária' is a billing/reimbursement unit, not a guaranteed one-per-calendar-day count. If a patient can accrue more than one PN diária per day … then the count is not a clean day-count and the 60-diária threshold does not map 1:1 to the 60-day ASPEN criterion."

Methods (m5):
> "Table 1 'Max daily units' of 288 in 2020 … **exceeds the number of days that could plausibly accrue in a 74-day window**; if daily units accumulate across a full year or across linked admissions, the 74-day-window definition is again ambiguous."

**Why data is required.** Requires the DATASUS codebook + inspection of raw records.

**Data operation.**
1. Confirm from the DATASUS data dictionary whether one AIH ever bills >1 PN diária/calendar day; cite it (or correct the mapping). The 288 value suggests diárias accumulate across multiple linked admissions.
2. State precisely, from the actual code, whether the 60/74 criterion is applied **within a single admission** or **cumulatively across linked admissions**, and how the 74-day window is enforced.

---

## MUST-5 — Fix the mortality inconsistency (which figure is the CIF cohort's?)

**What the paper currently says.** Three different numbers a reader takes as the same thing:
- **Abstract:** "In-hospital mortality ranged from **9% to 15%**"
- **Results, 971-cohort (line 153):** "**6.5%** died during hospitalization"
- **Table 1** (`tab:pn_17anos`, "% Deaths"): 11.9%–15.0% — but for **all 198,769 PN admissions**, not the 971 CIF patients.

**Referees.** Domain (M3a):
> "the '9–15%' quoted for CIF appears to be borrowing the all-PN mortality column … a reader cannot tell whether CIF-cohort mortality is ~6.5% or ~9–15%, and the Discussion's comparison to high-income survival (≥85%) hinges on getting this right."

**Why data is required.** The correct cohort-specific mortality must be computed from the patient-level data. Figure `fig:obito` appears to show all-PN mortality, not CIF-cohort mortality, and may need regenerating.

**Data operation.** Compute in-hospital mortality for the 971-patient CIF cohort (overall + annual for `fig:obito`); use that single figure consistently in abstract, Results, Discussion.

---

## MUST-6 — Quantify the missing-CEP exclusion and test for regional selectivity

**What the paper currently says.** Methods:
> "Admissions with missing postal code information were excluded from the analysis, as the absence of this field precludes reliable patient matching."

No count is given for how many admissions/patients this removes.

**Referees.** Methods (M5, "potentially large"; the most consequential distinct concern):
> "missing CEP is unlikely to be random — it plausibly correlates with the North/Northeast/Central-West underserved regions the paper's central argument concerns. If missingness is concentrated in exactly the regions claimed to be underrepresented, **the exclusion mechanically reinforces the paper's headline conclusion**, and the 'lower bound' framing may be partly an artifact of the exclusion."

**Why data is required.** Purely empirical; requires the pre-exclusion dataset.

**Data operation.**
1. Count admissions/patients dropped for missing CEP — **overall and by region**.
2. Compare CEP-present vs CEP-absent admissions on observables (region, age, death).
3. A best/worst-case bound on the headline under assumptions about the excluded cases.

---

## MUST-7 (data half) — False-match / twin-collision rate estimate

**Note.** The *text* half (softening the linkage-precedent overclaim, flagging twin risk) was
already applied in commit `ed3d7e0`. The **data half** remains.

**Referees.** Methods (M4):
> "Twins are the specific concern: same CEP, same DOB, often same sex — the deterministic rule will merge them into one 'patient,' **biasing the count downward** in exactly the prematurity-driven population that constitutes the sample."

Suggested internal validation:
> "agreement between the deterministic linkage and the CIF-specific-code deduplication on the 22 code-identified patients"

**Why data is required.** Both are direct data cross-tabulations.

**Data operation.**
1. Count CIF triplets (CEP + sex + DOB) that plausibly represent multiple births merged into one record (same-DOB/CEP/sex clusters); bound the count treating each as 1 vs 2 patients.
2. **22-patient overlap check (SHOULD-1):** of the 22 CIF-code patients, how many does the ≥60 PN rule independently flag?

---

## Summary table

| MUST | One-line need | Data operation |
|------|---------------|----------------|
| 1 | Explain 1,028 vs 971 | Count patients appearing in ≥2 years |
| 2 | Confidence intervals | Poisson/binomial CIs on counts (+ rate ratio for pandemic) |
| 3 | Scaling band | Recompute prevalence at ×1.0 / ×1.55 / upper |
| 4 | diárias = days? | Inspect codebook + confirm windowing logic |
| 5 | Correct mortality | Compute mortality on the 971 cohort |
| 6 | Missing-CEP bias | Count exclusions by region; compare observables |
| 7 (data) | Twin/false-match rate | Count same-DOB/CEP/sex clusters; 22-patient overlap |

## Blocker
`scripts/` is empty and no SIH-SUS extract is in `data/`. Every item above needs either the
analysis code or the underlying data extract brought into the project. Once present, the
`coder` + `data-engineer` agents can implement all seven MUSTs and regenerate the affected
tables (`tab:pn_17anos`, `tab:prevalencia_17anos`) and figures (esp. `fig:obito`).

## Related files
- `quality_reports/reviews/editorial_decision.md` — full MUST/SHOULD/MAY list
- `quality_reports/reviews/cif-brazil_referee_domain.md`
- `quality_reports/reviews/cif-brazil_referee_methods.md`
- Text fixes already applied: commit `ed3d7e0`
