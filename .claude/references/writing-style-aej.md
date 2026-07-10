# AEJ House Writing Style — Governance Guide

**Target style:** American Economic Journal: Applied Economics (transfers to AER, AEJ: Economic Policy, AEJ: Macro/Micro — the shared AEA house style).
**Applies to:** `writer`, `writer-critic`, and the `/write` skill. Read this alongside `domain-profile.md` and, when present, `personal-style-guide.md`, when drafting or reviewing prose.
**Purpose:** Make the manuscript read like it was written by economists who publish in the AEJ family — in structure, phrasing, cadence, and editorial convention. This is the reusable AEA house-style reference shipped with the scaffold; a project targeting a non-AEA outlet should recalibrate against its own corpus (see `journal-profiles.md`), and an author's individual voice, once extracted, lives in `personal-style-guide.md` and overrides generic phrasing here.

This guide governs **prose, rhetoric, structure, and editorial convention.** It does **not** replace `working-paper-format.md`, which governs LaTeX/typesetting for the working-paper PDF. See "Reconciliation" at the end where the two overlap.

---

## 0. Provenance — the corpus this guide is calibrated to

Derived from close reading of three recent AEJ: Applied Economics papers (July 2026 issue, Vol. 18 No. 3) plus the official [AEJ: Applied Economics Style Guide](https://www.aeaweb.org/journals/app/style-guide). Prose was read from the authors' near-final/working-paper versions; typeset conventions come from the AEA style guide.

| Tag | Paper | Design | Why chosen |
|-----|-------|--------|-----------|
| **C&L** | Clemens & Lewis, "The Effect of Low-Skill Immigration Restrictions on US Firms and Workers: Evidence from a Randomized Lottery" | RCT / IV, pre-analysis plan | Labor, experimental, model + reduced form |
| **Ag** | Aggarwal et al., "The Dynamic Effects of Cash Transfers to Agricultural Households" | RCT, dynamic event-study | Agricultural households, dynamic treatment effects |
| **GS** | Dahis & Szerman, "Decentralizing Development: The Economic Impacts of Government Splits" | DiD + diff-in-disc, event study | Reduced-form panel DiD, the most common scaffold design |

All three are applied reduced-form micro, the lane most scaffold projects sit in. Quotes below are lightly trimmed and attributed by tag.

---

## 1. How an AEJ paper is written — the composition philosophy

Five properties define the house voice. Every rule below serves one of them.

1. **Declarative and unhedged.** The authors assert findings as facts and let magnitudes carry the caution. Confidence lives in the numbers, not in adverbs.
2. **Concrete over abstract.** Every claim is tied to a number, an exhibit, or an institution. Almost no sentence is purely conceptual.
3. **The reader is never lost.** Each section, subsection, and paragraph announces what it is about before developing it. Signposting is relentless.
4. **The introduction is the paper in miniature.** A reader who stops after the intro should know the question, the design, every main result with magnitudes, the mechanism, and the caveats.
5. **Precision without jargon inflation.** Estimator names are exact; prose is plain. They write "we compare areas with ratified requests to untreated areas whose requests were not approved," not "we exploit quasi-random assignment of the treatment."

---

## 2. Section organization

### 2.1 The canonical skeleton

All three papers follow the same backbone (subsection depth varies with complexity):

```
[Introduction]              ← UNNUMBERED, UNTITLED (AEA house rule)
Theory / Conceptual framework   (optional; C&L has it, Ag/GS fold it into intro)
Institutional Background / Setting
Data
Empirical Strategy
Results
Mechanisms / Interpretation / Heterogeneity
Robustness
Discussion  (optional; GS has it)
Conclusion
```

Observed instantiations:

- **C&L:** Intro → Model → Institutional (H-2B visa) → Randomization → Data & Pre-Analysis Plan → Results → Robustness → Interpretation (elasticity, aggregation, forensic tests) → Conclusion.
- **Ag:** Intro → Experimental Design → Results (dynamic effects → investment → other) → Conclusion. (Short, RCT — fewer sections.)
- **GS:** Intro → Institutional Background → Data → Empirical Strategy → Main Results → Drivers/Mechanisms → Discussion → Conclusion.

**Rules:**
- Put **institutional/context and data before strategy**. The reader must understand the setting before the equation.
- **Robustness is its own section** (or a clearly-flagged block), placed *after* main results, never interleaved with them.
- A **mechanisms/interpretation section** after results is expected when the design supports it (heterogeneity that tests theory, structural parameters, back-of-envelope aggregation). This is where AEJ papers earn their contribution beyond "an effect exists."
- **Discussion** is optional and used for external validity, welfare, and policy scope — not to restate results.

### 2.2 The introduction — the most important structural template

AEJ introductions are **long (roughly 3–5 pages / 8–14 paragraphs)** and follow a fixed sequence. This is the single most learnable structure in the corpus.

| # | Move | What it does | Corpus example |
|---|------|--------------|----------------|
| 1 | **Hook / stakes** | One broad sentence on why the question matters, then narrow fast | "The effect of immigration on natives hinges on how the economy adjusts." (C&L) · "While cash transfers will tautologically increase the contemporaneous consumption of any normal good, evidence on whether this effect persists is limited." (Ag) |
| 2 | **The gap** | What's unsettled or unknown — often "evidence is mixed / estimates range widely" | "estimates of their effects range widely depending on the assumptions used to approximate causal identification" (C&L) |
| 3 | **"Here we / In this paper we…"** | State the setting and design in plain words | "Here we study the economic effects of a large-scale experiment…" (C&L) · "In this paper, we combine detailed information on productive investments with…" (Ag) |
| 4 | **"We find…"** | Lead result(s), with magnitudes and units, in present tense | "We find that exogenous permission to employ immigrants for low-skill work causes the marginal firm to expand production." (C&L) |
| 5 | **Walk the results** | One paragraph per main finding, each opening with an ordinal or a pointer — "The first result…", "We also investigate…", magnitudes stated | "The first result indicates that splitting improves public service delivery… increasing by 27 and 17 percent" (GS) |
| 6 | **Mechanism as a question** | Pose the "why," then enumerate explanations | "What can explain the gains in public service delivery and economic activity? One explanation is that splitting results in higher fiscal revenues… Another non-mutually exclusive explanation…" (GS) |
| 7 | **Robustness sentence** | One paragraph asserting the results survive checks | "Our main findings are robust across various checks, including alternative outcomes, samples, and specifications…" (GS) · "The treatment effects we measure are robust to several prespecified changes…" (C&L) |
| 8 | **Contribution paragraph(s)** | Explicit, enumerated positioning vs. the literature | "This research contributes to the literature in three ways. First… A second contribution… A third contribution…" (C&L) |
| 9 | **Policy implications** (optional) | "Our findings also have policy implications. First… Second…" (GS) |
| 10 | **Roadmap** (optional, declining) | "The paper proceeds as follows. In Section 2 we…" (C&L). Ag and GS omit it. Include only in longer/model-heavy papers. |

**Governance:** our intro MUST contain moves 1–5 and 8. Moves 6–7 are required when the design has mechanisms/robustness (ours does). Move 10 is optional.

### 2.3 Subsection headings

- **Title Case, short, descriptive of the finding or task**, not generic: "Setting up New Local Governments: Impacts on Public Services" (GS), "Defining the Instrumental Variable" (C&L), "Dynamic Treatment Effects" (Ag). Avoid bare "Results" as a subsection when a content title is possible.
- **Bold run-in lead-ins** organize long subsections into labeled paragraphs: `**Bureaucracy in the Public Sector.**` then prose; `**Public Services Delivery.**` then prose (GS). Use these instead of over-splitting into many thin subsections.

---

## 3. Sentence-level phrasing

### 3.1 Voice, tense, mood
- **Active voice, first person plural.** "We find," "We estimate," "We document," "We observe," "We leverage," "We compare." The authors are agents, not passive observers.
- **Present tense for findings and for what exhibits show.** "Figure 1 plots…", "Table 3 presents…", "We observe a spike of around 40 percent." Past tense only for what was *done* during data collection ("we collected data from both winners and losers").
- **Verbs of estimation and evidence, not of belief:** find, document, observe, show, reveal, confirm, uncover, estimate, leverage, exploit. Avoid "we believe/feel/think."

### 3.2 Reporting an effect — the canonical sentence shape
**Magnitude + unit first, significance in words second, interpretation third — significance stated inline, not in parentheses.**

Carry the magnitude and the significance in the prose itself: "wages fell 1.8 percent," "a precise zero," "statistically indistinguishable from zero," "significant at the 5 percent level," "rules out effects larger than two percentage points." The standard error and stars live in the table; the sentence carries the economics. A brief parenthetical qualifier — "(significant at the 1 percent level)", "(indistinguishable from zero at conventional levels)" — is an acceptable variant, and the published corpus uses it, but **inline is preferred**: it reads less like regression output, and it matches the author's own practice, which uses the parenthetical form essentially never.

- Corpus examples of the parenthetical variant (acceptable, not the default): "increased by over 0.5 standard deviations… (statistically significant at 1 percent)" (Ag); "increases by 4.4 and 1 percentage points (with the former being significant at the 10 percent level)" (GS); "an elasticity of +0.164 for revenue… (statistically distinguishable from zero at conventional levels)" (C&L).

**Rules:**
- Never report significance without the magnitude. "The coefficient is significant" is banned (already in `writer.md`); the corpus never does it.
- **Never put a raw p-value or a standard error in a prose sentence** — no "(p<0.001)", no "(standard error 0.006)". Significance goes in words; the SE and stars live in the table.
- Phrase significance as **"significant at the 1/5/10 percent level"** or **"(statistically) distinguishable / indistinguishable from zero at conventional levels,"** woven into the sentence rather than parenthesized. Spell out *percent* in prose.
- Give the **economic** meaning alongside the statistical one: convert to a share of a baseline, a dollar figure, or an elasticity.
- Restate a pivotal result in plainer terms with **"Put differently,"** when it aids intuition (C&L).

### 3.3 Citations inside sentences
- **Author-date, Chicago.** Parenthetical clusters carry the literature: "(Card 1990; Borjas 2003; Ottaviano and Peri 2012; Dustmann et al. 2016b)." No comma before the year in parentheticals; `et al.` for 5+ authors (list all for 1–4).
- Citations are **grouped at the end of the claim**, not sprinkled mid-sentence, so the prose stays readable.
- Narrative cites carry a specific point: "Lima and Silveira Neto (2018) argue that capital expenditures tend to be initially higher…" (GS).

### 3.4 Diction — what to avoid and prefer
- **Spell out "percent"** in text (not %). Reserve `%` for tables and tight parentheticals.
- **Zero before the decimal:** 0.357, never .357 (AEA rule; also in-text).
- Plain connectives: "However," "In addition," "Consistent with…," "Following the split," "By contrast." Avoid the AI-vocabulary list in `writer.md` (delve, foster, underscore, tapestry, landscape, interplay).
- **Honest caveat, not hedge.** State a limitation as a fact and move on: "an important caveat is that we cannot directly assess pre-trends due to having only one pre-split data point" (GS). This is exactly our house preference (`framing-causal-with-caveat`): claim the result, name the caveat, don't drown it in modifiers.
- **Note on the corpus vs. our stricter rule:** published AEJ prose is *not* perfectly scrubbed — GS uses "Interestingly," and "Additionally," which our `humanizer` pass removes. Follow our stricter anti-hedging/anti-AI-vocab standard; the corpus is the target for *structure and cadence*, not a license for filler.

---

## 4. Paragraph construction

- **One idea per paragraph; topic announced in sentence one.** Results paragraphs almost always open by naming the exhibit: "Figure 2a displays results for capital expenditures per capita." (GS) · "Table 4 shows results on physical and human capital investments." (Ag)
- **The results-paragraph template:** (i) point to the exhibit and say what it contains → (ii) state the finding with magnitude + significance → (iii) interpret / tie to mechanism or a comparison figure. GS ¶ at lines 672–683 is the model: exhibit → "spike of around 40 percent… stable increase of approximately 27 percent" → institutional interpretation with a citation.
- **Paragraph length is varied but bounded** — typically 4–8 sentences. Contribution and mechanism paragraphs run longer because they enumerate; transition paragraphs run shorter.
- **Enumerate within a paragraph** with "First,… Second,… Third,… Fourth,…" when listing evidence for one claim (GS mechanism paragraph). Prefer this to bullet lists, which AEJ prose avoids in the body.
- **Section-opening orientation paragraph.** Longer sections open with a 2–4 sentence paragraph that previews the subsections: "We start by examining how new municipalities establish local governments… We then demonstrate that splitting has positive economic impacts beyond the public sector." (GS, opening of Results).

---

## 5. Prose cadence

- **Rhythm = long-short alternation.** A complex sentence establishing a result is followed by a short one that lands the point. C&L: "We find that exogenous permission to employ immigrants for low-skill work causes the marginal firm to expand production. Put differently, exogenous restrictions … cause the marginal firm to contract." Do not write paragraphs of uniform 30-word sentences (an AI tell flagged in `writer.md`).
- **Front-load the subject and verb.** "We observe…", "Splitting improves…", "The restrictions cause…". Avoid long subordinate wind-ups before the main clause.
- **Numbers are the stressed beats.** The cadence is built so the magnitude lands at a natural emphasis point, usually mid- or end-sentence, followed by the parenthetical qualifier.
- **Transitions are short and functional**, placed at the head of the sentence: "However," "By contrast," "In addition," "Finally," "Consistent with this,". No throat-clearing ("It is important to note that…", "Interestingly,").
- **Rhetorical questions** are used sparingly to open a mechanism section: "What can explain the gains…?" (GS) · "Who Applies to Split?" (GS subsection title). One or two per paper, not a habit.
- **The em dash** appears but is not leaned on — used for a genuine appositive or a policy-relevant aside ("the H-2B visa—U.S. employers' access to that visa is limited by a quota"). Do not use em dashes as a default connector (AI tell).

---

## 6. Numbering (AEA house rules)

| Element | Rule | Example |
|---------|------|---------|
| **Introduction** | **No heading, no number.** The first section after the abstract is the intro and is left untitled. | (starts directly with prose) |
| **Sections** | Roman numerals: `I.`, `II.`, `III.` | `II. Institutional Background` |
| **Subsections** | Capital letters: `A.`, `B.`, `C.` | `A. The Role of Municipal Governments` |
| **Sub-subsections** | Arabic: `1.`, `2.` (or bold run-in lead-ins) | |
| **Equations** | Arabic in parentheses at the **left margin**, numbered consecutively; referenced as "Equation (1)". | `(1)` |
| **Tables** | Consecutive Arabic; appendix tables carry a letter prefix (`Table D.4`). Referenced as "Table 3". | |
| **Figures** | Consecutive Arabic; sub-panels get lowercase letters, referenced inline as "Figure 2a", "Figure 6b". | |
| **Footnotes (text)** | Consecutive Arabic superscripts, placed at the *end* of the sentence/clause. | |
| **Footnotes (table-internal)** | Lowercase letters `a, b, c` — distinct from text footnotes. | |

> **Our working-paper PDF vs. AEJ typesetting:** we compile with the repo preamble (`working-paper-format.md`), which numbers sections `1, 2, 3` via `\section{}`. That is fine for the *working paper*. Adopt the AEJ Roman/letter scheme and the **untitled introduction** only when preparing an actual AEA submission. What always transfers: untitled intro is a *good habit* to adopt now; equation/exhibit numbering and cross-reference phrasing ("Equation (1)", "Figure 2a", "Table 3") match ours already.

---

## 7. Tables and figures — editorial conventions

The LaTeX mechanics (booktabs rules, `threeparttable`, `siunitx`) live in `working-paper-format.md`. This section governs the **editorial** content — what the exhibit says and how its note reads. These are the AEA conventions.

### 7.1 Tables
- **Self-contained.** A reader must understand the table from its title + notes without the body text. Every column defined, every sample restriction stated.
- **Title Case descriptive title**, not "Regression Results." AEA typeset form is `Table 1—Descriptive Title` (em dash between number and title).
- **Horizontal rules only.** No vertical lines, no shading (AEA rule; matches our booktabs `\toprule/\midrule/\bottomrule`). Do not abbreviate column headings.
- **Standard errors in parentheses** below each coefficient.
- **Significance:** AEA's current guide says **do not use asterisks in tables — report standard errors and let the reader infer.** In practice AEJ authors report SEs and discuss significance in the prose ("significant at the 1 percent level"). *Our house choice:* always report SEs in parentheses; significance stars are optional and, to match current AEJ practice, may be omitted. Never rely on stars alone — the prose must state the magnitude and the significance in words.
- **The notes block** (from the corpus) reads as a compact paragraph, in this order:
  1. What the table reports and from which equation/sample: *"This table reports descriptive statistics in 1991 at the municipality level."* (GS) · *"Regressions include baseline measurement of outcome and strata fixed effects."* (Ag)
  2. Fixed effects and controls included.
  3. **Clustering/inference:** *"Standard errors clustered at village level."* (Ag) — always state the clustering level.
  4. Transformations, winsorizing, units: *"All outcomes are in USD PPP and Winsorized at the 99th percentile."* (Ag)
  5. Sample timing/definition notes: *"The endline was conducted about 18–22 months after first transfers…"* (Ag)
  6. Source line last, if any.
- **Zero before decimals** in all cells (0.357).

### 7.2 Figures
- **Event-study / dynamic-effect plots are the workhorse exhibit.** Plot point estimates with **95 percent confidence intervals**, normalized to the reference period, pre-period coefficients shown to demonstrate flat pre-trends (Ag Figure 1; GS Figures 2a–2d). This matches our `domain-profile.md` event-study convention exactly.
- **Figure notes mirror table notes:** *"This figure reports the annual effects of splitting on the public sector after estimating Equation (1). We consider… Standard errors…"* (GS). State the estimating equation, the sample, the CI level, and the clustering.
- Reference sub-panels precisely in text: "Figure 2a displays… Figure 2b reports…".
- Notes begin with `Notes:` (or `Note:` for a single note — the corpus uses `Note:`). Keep the convention consistent within the paper.

---

## 8. Footnotes

- **Substantive and discursive, not citation dumps.** Footnotes carry a real nuance, caveat, or robustness pointer that would break the flow of the main text.
  - Institutional nuance: C&L fn. 1 explains why individual-level vs. firm-level randomization matters for prior work.
  - Robustness pointer: Ag fn. 19–20 point to appendix figures decomposing an index and splitting effects by transfer size.
  - Honest caveat: Ag fn. 21 concedes a pre-payment blip in the treatment group and offers two measurement explanations.
  - Definitional detail: Ag fn. 2 lists exactly what "assets" includes across cited studies.
- **Density scales with institutional/empirical complexity.** Reduced-form panel papers run footnote-heavy (GS ≈ 50+); clean RCTs run lighter (Ag moderate). Do not pad — every footnote must earn its place.
- **Placement:** at the end of the sentence or clause it qualifies, after punctuation.
- **What does NOT go in a footnote:** the main result, the identifying assumption, or anything a referee must see. If it matters to the argument, it belongs in the body.

---

## 9. Governance — writer checklist and writer-critic deductions

### 9.1 Writer pre-submission checklist (AEJ style)
- [ ] Introduction contains moves 1–5 + 8 (§2.2); results walked with magnitudes; contribution enumerated.
- [ ] Institutional/context and data precede empirical strategy.
- [ ] Robustness is a separate, clearly-flagged section after main results.
- [ ] Every reported effect has magnitude + unit + significance-in-words (§3.2); no bare "significant."
- [ ] "Percent" spelled out in prose; zero before every decimal.
- [ ] Each results paragraph opens by naming its exhibit.
- [ ] No uniform-length sentence runs; long-short cadence present (§5).
- [ ] Every table/figure is self-contained; notes state equation, FE, controls, **clustering level**, transformations.
- [ ] Standard errors in parentheses; significance also in prose (stars optional).
- [ ] Footnotes are substantive; no result or identifying assumption hidden in one.
- [ ] `humanizer` pass run (AI-vocabulary, em-dash overuse, rule-of-three, "Interestingly/Additionally/It is important to note" removed).

### 9.2 Suggested writer-critic deductions (Execution/Peer-Review severity)
| Issue | Deduction |
|-------|-----------|
| Intro missing results-walk or contribution paragraph | −10 |
| Effect reported without magnitude/units (bare "significant") | −8 each |
| Results paragraph not anchored to an exhibit | −3 each |
| Table/figure note missing clustering level or estimating equation | −5 each |
| Non-self-contained exhibit (undefined column / sample) | −5 each |
| Robustness interleaved into main results rather than separated | −5 |
| "%" in prose instead of "percent"; `.357` instead of `0.357` | −2 each |
| AI-vocabulary / hedging / em-dash overuse surviving humanizer | −3 each |
| Identifying assumption or main result buried in a footnote | −8 |
| Uniform sentence cadence across a section (AI tell) | −3 |

---

## 10. Reconciliation with existing repo rules

- **`working-paper-format.md` wins on LaTeX/typesetting** (document class, biblatex/biber, booktabs, `threeparttable`, doublespacing, JEL/keywords block). This guide does **not** override it. Where AEJ typeset form differs (Roman-numeral sections, untitled intro, lowercase-letter table footnotes, no stars), apply the AEJ form only when preparing an actual AEA submission; keep the repo preamble for the working-paper PDF.
- **`writer.md` anti-hedging + humanizer are stricter than raw AEJ prose** and stay in force. Use this corpus for *structure, cadence, and the effect-reporting sentence shape* — not as permission to reintroduce "Interestingly/Additionally."
- **`domain-profile.md` notation and event-study conventions** (95% CI, cluster at treatment level, normalize to t−1) already match the AEJ corpus — no conflict; this guide reinforces them.
- **Memory `framing-causal-with-caveat`** is consistent with §3.4: claim the result, name the caveat once as a fact, don't over-hedge.

---

*Sources:* [AEJ: Applied Economics Style Guide](https://www.aeaweb.org/journals/app/style-guide) · Clemens & Lewis, [NBER w30589](https://www.nber.org/papers/w30589) (AEJ: Applied 2026) · Aggarwal et al., [NBER w32431](https://www.nber.org/papers/w32431) (AEJ: Applied 2026) · Dahis & Szerman, [Decentralizing Development](https://www.ricardodahis.com/papers/Dahis%20and%20Szerman%20-%20Decentralizing%20Development.pdf) (AEJ: Applied 2026).
