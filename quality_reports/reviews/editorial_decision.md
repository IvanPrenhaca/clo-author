# Editorial Decision — JPGN

**Date:** 2026-07-13
**Manuscript:** "Chronic Intestinal Failure in Brazil: A First Estimative of Prevalence"
**Journal:** Journal of Pediatric Gastroenterology and Nutrition (JPGN)
**Based on:** Domain referee (74/100, Major Revision) + Methods referee (58/100, Major Revision)

> Persisted by the orchestrator on behalf of the editor.

## 1. Decision: **MAJOR REVISION**

First national population-based pediatric CIF prevalence estimate for Brazil — clears JPGN scope and contribution comfortably; not a desk/full reject. Both referees independently recommended Major Revision and classified every serious concern as fixable with data in hand. The 74-vs-58 score gap reflects disciplinary lens (clinical contribution vs measurement machinery), not disagreement about fate. Decision does not average (66 would mislead): methods referee weighted more heavily on *what must change* (measurement rigor IS the contribution for a descriptive prevalence paper), domain referee on *whether the paper is worth saving* (clearly yes). Single condition for reconsideration: the headline must stop being a bare point estimate — it needs uncertainty, a scaling sensitivity band, and a reconciled internal count.

## 2. Convergent concerns (both referees, independently — highest priority)
- **C1** — 1,028 (Table 2 annual sum) vs 971 unique patients; estimand never defined. [Domain M3b; Methods m1] [verified]
- **C2** — `medinacoeli2025deterministic` precedent overstated (it's an obstetrics linkage study). [Methods M4]
- **C3** — No uncertainty bounds anywhere; "23%/40%" pandemic declines with no CI/test. [Domain M2; Methods M1]

## 3. Distinct concerns
**Domain (clinical):** D1 diárias≠days unvalidated (M1); D2 mortality 6.5% vs 9–15% inconsistency (M3a); D3 "hidden mortality" + race/equity over-asserted (M5).
**Methods (measurement):** E1 threshold on thin tail, untested (M3); E2 missing-CEP exclusion likely region-selective → could manufacture the headline (M5); E3 code cross-validation mis-scoped (M8); E4 scripts/ empty, nothing reproducible (m9).

## 4. FATAL-flag adjudication — the 1.55 scaling factor
Methods = FATAL-as-presented (M2); Domain = ADDRESSABLE (M4). **Verdict: revision-level, not reject-level.** The flaw is presentation, not viability ("FATAL *as presented*"); lower-bound framing cushions it; the true strict lower bound (unscaled SUS-only) already exists in Table 2. Remedy is concrete and convergent: promote unscaled SUS-only to primary, demote 1.55 to a sensitivity-flanked secondary, report a range. It is a **MUST**, but not grounds for rejection.

## 5. Prioritized action list

### MUST (required for reconsideration)
1. Reconcile 1,028 vs 971; define estimand (period vs point prevalence); note in Methods + Table 2. [Dom M3b; Meth m1/M6]
2. Exact Poisson/binomial 95% CIs on every Table 2 cell + mean + mortality; pandemic decline as rate ratio w/ CI. [Dom M2; Meth M1]
3. Rebuild headline as scaling sensitivity band: unscaled SUS-only primary lower bound; 1.0→1.55→all-cause; sign the likely over-correction; fix Eqs 1–3. [Dom M4; Meth M2 FATAL, M6]
4. Validate diárias≠days: DATASUS dictionary cite; within-admission vs cumulative; resolve 288-diárias/74-day contradiction. [Dom M1; Meth M3/m2/m5]
5. Fix mortality inconsistency: one CIF-cohort figure everywhere (6.5% vs Table 1 all-PN 11.9–15% vs abstract 9–15%). [Dom M3a]
6. Quantify missing-CEP exclusions + test regional selectivity (N/% dropped by region; best/worst-case bound). [Meth M5]
7. Soften linkage precedent; add expected false-match rate w/ twin bound (downward bias in premature population). [Dom M6; Meth M4]

### SHOULD
1. 22-patient overlap check (how many code patients does ≥60 PN flag?); reframe cross-validation. [Meth M8]
2. Threshold sensitivity grid (≥45/50/60/75/90) + FP/FN discussion. [Dom M1; Meth M3]
3. Complete STROBE: flow diagram w/ exclusion counts, missing-data handling, estimand, ICD-10 appendix for Tables 3–4. [Dom M6; Meth M7]
4. Down-tone "hidden mortality" to hypothesis; resolve race/equity contradiction (line 245 vs 109). [Dom M5; Meth m4]
5. Deposit case-finding + linkage code (scripts/ empty). [Meth m9]

### MAY
1. Title "Estimative" → "Estimate."
2. Define "alta melhorada" for non-Brazilian readers.
3. Verify Beath 2011 (HPN, not SBS-specific), mukhopadhyay2019 85%, sacramento2024care (already removed).
4. JPGN numbered Vancouver style (currently natbib authoryear); populate/remove "[Final]" Appendix A.

## 6. Bottom line
**Distance from publishable:** one well-scoped revision cycle — moderate, not large. No fatal design flaw, no missing data, no identification problem (descriptive — none required). Every MUST is a reporting/analysis fix using data in hand; resolving the core items reaches mid-80s / Minor Revision.

**Single most important revision:** reconstruct the headline as an honest interval, not a point estimate (MUST-2 + MUST-3). The paper's stance is "this is a lower bound," yet it presents that bound as one deceptively precise number (3.35/million) on an unaudited scalar with no CI. Poisson CI + unscaled SUS-only floor + 1.55 sensitivity band makes the framing and the number finally agree.
