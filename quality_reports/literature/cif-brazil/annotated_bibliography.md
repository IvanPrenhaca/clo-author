# Annotated Bibliography — Chronic Intestinal Failure in Brazil (cif-brazil)

**Compiled by:** librarian (Discovery phase)
**Date:** 2026-07-13
**Scope:** (A) Audit of citations already in `biblio.bib` / `main.tex`; (B) newly found literature recommended for addition.
**Calibration:** Medical / public-health / clinical-nutrition venues weighted first (JPGN, Clinical Nutrition / ESPEN, Nutrients, JPEN, Nutrition in Clinical Practice, J Pediatr Surg, Intestinal Failure, Cadernos de Saúde Pública, IJPDS). Economics venues secondary.

**Note on verification method:** All central cited PDFs available in `references/` were read in full where the renderer allowed (single-column or ≤10-page files). Three multi-page PDFs (`aspen2022pif.pdf`, `caporilli2023overview.pdf`, `lezo2022chronic.pdf`) are password-protected or require a PDF page renderer not installed in this environment; those were audited from their bib metadata plus how they are quoted/cited by other verified papers (esp. Khokhar 2025). Four cited keys have **no PDF in `references/`** and could not be directly verified: `antunes2020portuguese`, `mukhopadhyay2019`, `squires2012natural`, `gattini2021trends`. These are all real, well-known papers (bib metadata is correct), but the specific numbers attributed to them in the text were not independently checked against the source — flagged below.

---

## PART A — AUDIT OF EXISTING CITATIONS

### A.1 Central references verified as accurately characterized

**khokhar2025global** — Khokhar B, Pathania V, Nazarey P, Parihar N. "Global prevalence of short bowel syndrome–associated intestinal failure in adults and children: A targeted literature review and analysis." *Nutrition in Clinical Practice* 2025;40(5):1093–1106. doi:10.1002/ncp.11314.
- **VERIFIED, with one nuance to flag.** This is correctly used as the anchor for the international-comparison framing. Global 2024 estimates: 0.09–1.67 per 100,000 children (i.e., 0.9–16.7 per million). US children 1.49/100k, UK children 1.67/100k, Central/South America mean 0.26/100k. Khokhar attributes low Latin-American figures explicitly to "lack of infrastructure for HPN" and "lack of major intestinal rehabilitation centers, affecting underreporting" — this **directly supports the manuscript's central thesis** and should be quoted in the Discussion.
- **NUANCE / caution for the writer:** Khokhar's own *Brazil-specific* extrapolated pediatric figure is **0.14 per 100,000 = 1.4 per million** (Table 2), which is *lower*, not higher, than the manuscript's estimate of 3.35/million. So the sentence in the Introduction and Discussion that the Brazilian estimate is "markedly lower than those established in the international literature" is **only correct when benchmarked against high-income countries (US 14.9, UK 16.7 per million)**, not against Khokhar's modelled Brazil/Latin-America number. Recommend the writer state the benchmark explicitly (e.g., "relative to high-income settings such as the US and UK") to avoid a referee catching an internal inconsistency: the paper's estimate actually *exceeds* the only previously published Brazil-specific figure. This is a point in the paper's favour (it shows more cases than the naïve extrapolation) and is worth making explicitly rather than glossing.

**leite2025multicenter** — Leite HP, Vincenzi R, Kieling CO, et al. "A multicenter study on enteral autonomy outcome of pediatric intestinal failure patients from a middle-income country." *Clinical Nutrition ESPEN* 2025;66:93–100. doi:10.1016/j.clnesp.2025.01.033.
- **VERIFIED.** 207 patients, 3 high-volume MIRPs, 2014–2023. SBS 85% of IF; 5-yr enteral autonomy 37%; survival 92.3%. Middle-income-country challenges (limited funding, few referral centres, training gaps, diagnostic delay, home-PN logistics) are stated verbatim — the manuscript's Discussion marginal note paraphrases these accurately.
- **CORRECTION (minor but should be fixed):** The Discussion marginal note (`main.tex` ~line 408) says the 3 centres are in "regiões Centro Sul (SP e PA)". The three centres are **Hospital de Clínicas de Porto Alegre (Rio Grande do Sul, RS)**, Hospital Sírio-Libanês/Menino Jesus (São Paulo), and Hospital Samaritano (São Paulo). So it is **SP and RS, not "PA" (Pará)**. Fix before submission.

**wales2004neonatal** — Wales PW, de Silva N, Kim J, Lecce L, To T, Moore A. "Neonatal short bowel syndrome: population-based estimates of incidence and mortality rates." *J Pediatr Surg* 2004;39(5):690–695.
- **VERIFIED.** First population-based neonatal SBS estimate: **24.5 per 100,000 live births** (Toronto/Metro), much higher in premature infants; SBS case-fatality 37.5%; etiologies NEC/atresia/abdominal-wall defects/volvulus. Correctly used to support "prematurity-related neonatal morbidity is the dominant cause." Note: the Introduction's "0.25 per 1,000 live births" is attributed to `caporilli2023overview, cole2008very, alene2022time`, not to Wales; 0.25/1,000 = 25/100,000 and is consistent with Wales' 24.5/100,000. No misattribution, but the writer could cite Wales directly for that number.

**beath2011trends** — Beath SV, Gowen H, Puntis JWL. "Trends in paediatric home parenteral nutrition and implications for service development." *Clinical Nutrition* 2011;30(4):499–502.
- **VERIFIED.** UK national point-prevalence survey of paediatric HPN: mean **13.7 per million** children, strong regional variation (1.76 in Wales to 41.4 in London per million), SBS share of cases rose 27%→63%. It is an **HPN point-prevalence survey, not an SBS-specific prevalence study** — accurate as used, but the writer should not imply it is a diagnosis-specific SBS/CIF prevalence figure. Its regional-variation and "concentration of specialist centres" findings are a good parallel to the manuscript's geographic-inequity result.

**pant2017epidemiology** — Pant C, Sferra TJ, Fischer RT, Olyaee M, Gilroy R. "Epidemiology and healthcare resource utilization associated with children with short bowel syndrome in the United States." *JPEN* 2017;41(5):878–883.
- **VERIFIED and UNDER-USED.** Currently only appears in a marginal Discussion note. **This is arguably the single closest methodological precedent to the manuscript** and should be elevated to the Methods/Introduction, not buried in the Discussion. Pant used the US Kids' Inpatient Database (KID), noted that "SBS does not have a unique ICD-9-CM code," and therefore identified cases by **combining a diagnosis code (579.3) with the parenteral-nutrition procedure code (99.15)** — the exact "procedure-code-as-proxy" logic the manuscript uses. It also explicitly flags that KID is **discharge-level, not patient-level** (cannot track readmissions) — the same limitation the manuscript solves with deterministic linkage. Findings the manuscript echoes: Black children over-represented (OR 1.4) → equity concern; care concentrated in urban teaching/children's hospitals → referral bias; high severity, high cost, CLABSI/anemia/liver disease burden. Recommend moving to Introduction + Methods as the precedent for "procedure code as proxy in the absence of a diagnosis code."

**mukhopadhyay2019** — Mukhopadhyay A, Raphael BP, Ching YA, et al. "Epidemiology of Pediatric Intestinal Failure and Evidence-Based Strategies for Management." *JPGN* 2019;69(5):S23–S32.
- **NOT DIRECTLY VERIFIED (no PDF).** Bib metadata correct. Manuscript cites it for (i) reporting prevalence per million convention, (ii) mortality claim that "survival ≥85% is achievable with adequate PN in high-income settings." That survival figure is plausible and consistent with the wider literature (Leite 92.3%, Gattini, Squires) but was not checked against this specific source. Low risk; recommend a quick confirmation of the exact 85% figure before final submission.

**aspen2022pif** / **modi2022aspen** — ASPEN Definitions in Pediatric Intestinal Failure (practice tool + Modi et al. 2022 *JPEN* 46(1):42–59).
- **VERIFIED indirectly.** The 60-days-within-a-74-consecutive-day-interval chronicity criterion is exactly as Khokhar 2025 quotes the ASPEN definition ("dependence on supplemental parenteral support for a minimum of 60 days within a 74 consecutive day interval"). The manuscript's operational definition is faithful to ASPEN. No issue.

**pironi2023espen**, **cuerda2021espen**, **goulet2006causes**, **squires2012natural**, **gattini2021trends**, **antunes2020portuguese**, **lezo2022chronic**, **caporilli2023overview**, **massironi2020understanding** — standard, authoritative sources; characterizations in the text are consistent with their known content. `squires2012natural`, `gattini2021trends`, `antunes2020portuguese`, `lezo2022chronic` were **not directly readable here** (no PDF or protected), but their bib entries are correct and their use in the text (etiology, European cohorts skewing toward congenital enteropathies, per-million reporting) matches their well-established findings. No misattribution detected; recommend spot-checking the exact Portuguese and Italian prevalence numbers if any are quoted numerically in the final Discussion draft.

### A.2 WEAK / NON-AUTHORITATIVE SOURCES — a medical referee will object

**elicit2025developing**, **elicit2025pediatric**, **elicit2025rehab** — "Elicit Research Report," Elicit Platform, 2025.
- **REMOVE.** These are **AI-generated research summaries from the Elicit platform**, not peer-reviewed literature, not indexed, not citable, and not independently verifiable. The bib file itself already brackets them under "% Não citar – referências internas" (do not cite — internal references), yet `elicit2025developing` **is actively cited in the Introduction** (`main.tex` line 90). A methods/domain referee at any of the target journals will treat an "Elicit Research Report" citation as a serious credibility problem. **Action:** delete `\cite{...elicit2025developing...}` from line 90 and replace with a real source. The claims it supports (sepsis and liver failure as key morbidities; prevention contingent on prompt referral) are far better supported by `caporilli2023overview`, `pironi2023espen`, `pant2017epidemiology`, or the new `hilberath2024impact` / `avitzur2024development`. The other two Elicit keys are not cited in `main.tex` and should simply be deleted from the bib.

**correio2023**, **terra2023doencasraras**, **pequenoprincipe2023** — Brazilian news / hospital-blog items on rare diseases in childhood.
- **DOWNGRADE / mostly remove.** None of these three are cited in `main.tex` (they are dead entries — see A.3). If the authors want a citation for the "9.75 million Brazilian children with rare diseases" framing or the "75% of rare diseases manifest in childhood" claim, replace the news items with a peer-reviewed or governmental source. Recommended substitutes now in the bib or newly found: `pinto2019cuidado` (Cadernos de Saúde Pública — peer-reviewed, on the burden on families of children with rare conditions) and `andrade2025paving` (RARAS registry, BMC Digital Health). News articles are acceptable only as colour, never as evidence, and are best dropped entirely from a clinical-journal submission.

**session2025nec** ("Clinical Session Materials / HFACT Project Documentation") and **unicef2019**, **unicef2025**-style grey items — acceptable as background/context only; not cited in `main.tex` (dead — see A.3). `session2025nec` is internal course material and should be removed.

### A.3 Entries in `biblio.bib` NOT cited anywhere in `main.tex` — candidates for removal or use

These bib keys never appear in a `\cite`/`\citep`/`\citet` in `main.tex` (verified against the full manuscript). They are either legacy imports or intended-but-unused. Recommend either wiring them in where relevant or deleting to keep the bib clean:

| Key | Verdict |
|-----|---------|
| `andrade2025paving` | **Keep & use** — RARAS (first Brazilian rare-disease registry). Excellent for Intro/Discussion on rare-disease under-registration in Brazil. Currently uncited. |
| `pessarelli2024epidemiology` | Optional — Italian Crohn's SBS-IF survey; tangential. Keep only if adult/IBD framing is added. |
| `sacramento2024care` | **VERIFY EXISTENCE before use.** Bib claims "Sacramento A, et al. Pediatric intestinal failure care in Brazil: current panorama and regional disparities. *Jornal de Pediatria* 2024;100(2):150–158, doi:10.1016/j.jped.2023.11.004." I could **not confirm this article exists** in searches; the author string "A. Sacramento and others" and round page range look like a possibly fabricated/placeholder entry. **Do not cite until confirmed on the Jornal de Pediatria site / DOI resolver.** If it does not resolve, delete it. Flagged as potential hallucinated citation. |
| `miller2024neurodevelopment` | **Keep & use** — real (Miller et al., *Pediatr Surg Int* 2024;40(1):120; Brazilian/HCPA single-center, neurodevelopment on prolonged PN). Good Brazilian supporting cite; currently uncited. |
| `puttonen2023pediatric` | **Keep & use** — Finnish "data lake" real-world SBS incidence/resource-use. Strong administrative-data precedent; currently uncited despite being cited-by-name-only in Intro list `\cite{...puttonen2023pediatric}` (actually it IS cited in Intro line 86 — retain). |
| `winkler2023epidemiology` | Optional — adult SBS epidemiology review. Background only. |
| `nut2023115` | Weak (conference abstract, Argentina). Superseded by the new RESTORE full paper (`rumbo2024restore`). Recommend replace. |
| `spolidoro2021international` | **Keep & use** — Latin American pediatric IF team survey (Nutrients). Good regional cite; uncited. |
| `gondolesi2020detailed` | **Keep & use** — intestinal transplantation status in Latin America. Uncited; pairs with `boteon2024multicentric`. |
| `folwarski2021trend`, `siddiqui2021short`, `muto2022overview`, `thompson2011current`, `platell2002management`, `salvia2008neonatal`, `pironi2012outcome`, `merritt2017intestinal`, `stanger2013impact`, `sparks2016necrotizing`, `batra2017epidemiology`, `o2006short`, `wales2010short` | Legacy background/clinical-management refs, uncited. Keep a curated subset; delete the rest to avoid a bloated bib. |
| `hussey2007design`, `powell2015financial`, `propper2000demand`, `zhang2025global`, `liu2025prevalence` | **Delete** — these are econometrics / unrelated-topic templates (stepped-wedge design, India cash transfers, UK private health demand, precocious puberty, US child mental health). They are leftovers from the template and have no place in this clinical paper's bib. |
| `who2025icd11`, `conitec2024`, `unicef2019`, `unicef2025` | Grey/reference material; keep only those actually cited. `conitec2024` (intestinal-transplant procedure report) is useful for the policy/Discussion framing — consider using. |

---

## PART B — NEWLY FOUND LITERATURE (recommended additions)

Proximity scale: 5 = directly competes / essential; 4 = closely related; 3 = related method/context; 2 = tangential; 1 = background.

### B.1 National / population-based prevalence from administrative or claims data (STRENGTHENS the international-comparison and methods framing)

**[Proximity 5] Ali A, Mitchell G, Gallivan M, Henderson J, Iyer K. "Epidemiology of US patients with short bowel syndrome–associated intestinal failure: A claims database analysis." *Intestinal Failure* 2025;8:100325. doi:10.1016/j.intf.2025.100325.**
Uses the Komodo Healthcare Map claims database (~100–120M enrollees, 70+ US plans, 2019–2021). Identifies SBS-IF via a **multi-part algorithm on claims** — ≥2 nutrition (PN/IV) claims ≥6 months apart, continuous nutrition ≥6 months, a malabsorption diagnosis, plus evidence of GI surgery/congenital bowel abnormality — i.e., **parenteral nutrition claims as a proxy for chronic IF, with deduplication to unique patients**, exactly the manuscript's design logic in a different health system. Reports **≈9 cases per million pediatric, 26 per million adult, 36 per million overall (US, 2021)**. This is the most current, most directly comparable administrative-data prevalence paper and the closest thing to a "scooping-adjacent" reference: it is US, not Brazil, so it does not scoop the Brazilian estimate, but it validates the whole approach and gives the strongest apples-to-apples pediatric benchmark (9/million US vs 3.35/million Brazil). **Must-cite in Methods (as precedent) and Discussion (as benchmark).**

**[Proximity 3] Puttonen M, Tuominen S, Ukkola-Vuoti L, et al. "Pediatric Short Bowel Syndrome: Real-World Evidence on Incidence and Hospital Resource Use From a Finnish Data Lake." *JPGN* 2023;77(4):479–485.** *(Already in bib as `puttonen2023pediatric` and cited — listed here for completeness because it is the European administrative-data analogue: incidence ~24/100,000 live births; national registry/data-lake method.)* No new entry needed; ensure it is used to support the administrative-data approach, not just the incidence number.

### B.2 Latin American / middle-income evidence (STRENGTHENS the regional framing)

**[Proximity 5] Rumbo C, Solar H, Ortega M, et al. "Short bowel syndrome related intestinal failure outcomes in Latin America: Insights from the RESTORE Registry." *JPEN J Parenter Enteral Nutr* 2024;48(8):956–964. doi:10.1002/jpen.2693.**
Prospective multicenter registry, **20 centres across Latin America**, May 2020–Jul 2023, **167 patients (115 adults, 52 children; 52% of children premature)**. Pediatric etiologies: intestinal atresia 25%, NEC 23%, gastroschisis 21% — closely mirrors the manuscript's prematurity/NEC-dominated Brazilian profile. Explicitly motivated by "the scant information available about intestinal failure in Latin America." This is the **definitive regional reference** and directly supports the "data are scarce in Latin America / middle-income settings" argument. It supersedes the weak Argentine conference abstract `nut2023115`. **Must-cite in Introduction and Discussion.**

**[Proximity 3] Goldani HAS, Ceza MR, Godoy LL, et al. "Outcomes of the First 54 Pediatric Patients on Long-Term Home Parenteral Nutrition from a Single Brazilian Center." *JPGN* 2022;75(1):104–109. doi:10.1097/MPG.0000000000003473.**
Retrospective analysis of 54 children with IF on PN >60 days, **Hospital de Clínicas de Porto Alegre (HCPA), 2014–2020**, in the public SUS. HPN feasible/safe in Brazil; 15 achieved enteral autonomy, 4 deaths. **Directly relevant to the manuscript's cross-validation finding**: HCPA is one of the two hospitals that account for *all* admissions under the new CIF-specific procedure code (56 of 86). Citing Goldani explains *why* HCPA dominates the CIF-code data (it runs the country's most established pediatric MIRP) and grounds the "care concentrated in 2 centres" observation in a documented program. **Recommend for Discussion.**

**[Proximity 2] Gondolesi GE, Pattín F, Nikkoupur H. "Management of intestinal failure in middle-income countries, for children and adults." *Curr Opin Organ Transplant* 2018;23(2):212–218.** *(Distinct from `gondolesi2020detailed` already in bib.)* Frames the systemic barriers (funding, referral, HPN logistics) in middle-income settings; useful background for the Discussion's structural-barriers argument. Optional.

### B.3 Methods precedents — administrative data + record linkage + procedure-code proxy (STRENGTHENS Methods, pre-empts referee objections)

**[Proximity 5] Medina Coeli C, Soares Madeira Domingues RM, Meijinhos L, et al. "Using a deterministic matching computer routine to identify hospital episodes in a Brazilian de-identified administrative database for the analysis of obstetrics hospitalisations." *International Journal of Population Data Science* 2025;10(1). doi:10.23889/ijpds.v10i1.2467.**
The single most on-point **methods** citation found. It solves the *identical* problem the manuscript faces: the SIH-SUS has **no unique patient identifier**, so the authors build a **deterministic matching routine using date of birth, municipality of residence, and postal code (CEP)** to link records into episodes/individuals. This is essentially the manuscript's linkage algorithm (CEP + sex + DOB) validated in a peer-reviewed methods venue on the *same database*. **Must-cite in Methods** — it directly supports the legitimacy of the deterministic-linkage strategy and answers the obvious referee question "is this a valid way to deduplicate SIH-SUS?"

**[Proximity 4] Pant et al. 2017** (see A.1) — already in bib; the key precedent for "procedure code (PN) as a proxy for a diagnosis that lacks a unique code." Elevate from Discussion to Methods.

### B.4 COVID-19 disruption to chronic/rare pediatric care (STRENGTHENS the pandemic-dip interpretation)

**[Proximity 4] Hilberath J, Mast A-S, Scherer S, et al. "Impact of COVID-19 on paediatric chronic intestinal failure: A tertiary care children's hospital experience." *JPGN* 2024;78(5):1171–1179. doi:10.1002/jpn3.12158. (PMID 38477361).**
Tertiary-centre study documenting how the pandemic disrupted care specifically for **paediatric chronic intestinal failure** patients (appointments, PN supply, service access). This is the best available citation to support the manuscript's key interpretive claim that the 2020–2021 prevalence dip reflects **pandemic-driven disruption of access to prolonged PN**, not a fall in true incidence. **Must-cite in Results (interpretation of the dip) and Discussion.** Currently the manuscript makes this argument with no supporting citation.

**[Proximity 2] (Supporting, optional) Bering J, DiBaise JK, et al. / international HPN-during-COVID clinician and patient surveys (e.g., *JPEN* 2021 international clinician survey; *Clin Nutr ESPEN* HPN patient-experience surveys).** These document PN-supply and service disruption during COVID for HPN patients broadly. Useful as secondary support if the writer wants more than one citation for the disruption mechanism. Exact citations should be pulled and verified before inclusion; listed here as a pointer, not a confirmed entry.

### B.5 International benchmark registry (context for the "gap vs. international benchmarks" claim)

**[Proximity 3] Avitzur Y, Pahl E, Venick R, et al. (International Intestinal Failure Registry). "The Development of the International Intestinal Failure Registry and an Overview of its Results." *Eur J Pediatr Surg* 2024;34(2):172–181. doi:10.1055/a-2212-6874.**
IIFR: 362 pediatric IF patients across 26 centres worldwide; 5-yr enteral autonomy 47%, IFALD 18–24%. Provides the contemporary international outcomes benchmark against which the manuscript's mortality (9–15% in-hospital) and the Brazilian EA/survival figures (via Leite) can be positioned. Referenced inside Leite 2025; worth citing directly. **Recommend for Discussion.**

**[Proximity 3] Mutanen A, Engstrand Lilja H, Wester T, et al. "A Nordic multicenter study on contemporary outcomes of pediatric short bowel syndrome in 208 patients." *Clinical Nutrition* 2023;42(7):1095–1103.**
Etiology benchmark: NEC 49%, gastroschisis±atresia 14%, atresia 12%, volvulus 11%. Useful counterpoint for the manuscript's claim that Brazilian CIF is prematurity/NEC-dominated vs. European cohorts skewing toward congenital enteropathies — Mutanen shows Nordic cohorts are *also* NEC-dominated, so the writer should frame the "European congenital-enteropathy" contrast carefully (it is truer of the Lezo/Antunes cross-sectional registries than of surgical SBS cohorts). **Recommend for Discussion; also a useful check against over-claiming the contrast.**

---

## Summary of required actions for the writer
1. **Remove** `elicit2025developing` from Introduction line 90; replace with `caporilli2023overview` / `pironi2023espen` / new `hilberath2024impact`. Delete all three Elicit keys and `session2025nec` from the bib.
2. **Verify or delete** `sacramento2024care` (possible non-existent citation) and confirm the `mukhopadhyay2019` 85% survival figure.
3. **Fix** the "SP e PA" → "SP e RS" error in the Leite Discussion note.
4. **Elevate** `pant2017epidemiology` to Methods/Intro as the procedure-code-proxy precedent.
5. **Add** the 6 must-cite new papers: `ali2025epidemiology`, `rumbo2024restore`, `medinacoeli2025deterministic`, `hilberath2024impact`, `goldani2022outcomes`, `avitzur2024iifr` (BibTeX in `references.bib`).
6. **State the benchmark explicitly** when claiming the estimate is "lower than international literature" (vs. high-income settings; note it *exceeds* Khokhar's modelled Brazil figure of 1.4/million).
7. **Clean** the bib of econ-template leftovers (`hussey2007design`, `powell2015financial`, `propper2000demand`, `zhang2025global`, `liu2025prevalence`) and unused legacy news items.
