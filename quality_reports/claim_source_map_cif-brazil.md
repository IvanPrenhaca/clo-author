# Claim–Source Map — Chronic Intestinal Failure in Brazil (cif-brazil)

Traceability record per INV-22. Maps every numerical/empirical claim in the
manuscript to its source: either a Results table/figure/paragraph in `paper/main.tex`,
or a cited reference in `biblio.bib`. Focus is the newly written Discussion and
Conclusions; core Results figures they rely on are traced back to their origin in the
Results section.

**Note on provenance:** This is a descriptive paper built from SIH-SUS/DATASUS
administrative data. Analysis scripts have not yet been added to `scripts/`
(the numbers originate from the imported manuscript's prior analysis). Where a
number's script line cannot yet be cited, the source is the manuscript Results
table/figure that reports it; these should be re-linked to script output when the
replication code is deposited.

---

## Paper-internal claims (Discussion / Conclusions → Results origin)

| Claim (Discussion/Conclusions) | Value | Source in main.tex |
|---|---|---|
| Mean annual prevalence 2017–2025 | 3.35 per million | Results, Table `tab:prevalencia_17anos` (Mean row); text §Results |
| Prevalence range (high) | 4.25 (2019) | Table `tab:prevalencia_17anos`, 2019 row |
| Prevalence range (low) | 2.46 (2025) | Table `tab:prevalencia_17anos`, 2025 row |
| Total PN-related admissions | 198,769 | Table `tab:pn_17anos` (Total); Results ¶1 |
| Unique patients | 150,078 | Results ¶1 |
| CIF cases (≥60 daily units) | 971 (0.65%) | Results ¶1 |
| In-hospital mortality range | 9–15% | Figure `fig:obito`; Results §Healthcare Utilisation |
| Mean travel distance | ~70 km | Figure `fig:distancia`; Results §Geographic |
| Patients travelling outside municipality | >50% | Figure `fig:deslocamento`; Results §Geographic |
| CIF-specific code (2024) unique patients | 22 | Results §Complementary Analysis ¶2 |
| CIF-code admissions total | 86 | Results §Complementary Analysis ¶2 |
| CIF-code admissions concentrated in | 2 hospitals (HCPA 56, HC-SP 30) | Results §Complementary Analysis ¶3 |
| Predominant aetiology | prematurity / neonatal morbidity | Results §Clinical Profile; Tables `tab:diagnosticos`, `tab:procedimentos` |

## External benchmark claims (Discussion → cited source)

| Claim | Value | Citation | Verification status |
|---|---|---|---|
| US paediatric SBS-IF (survey/registry benchmark) | ~14.9 per million | `khokhar2025global` | From librarian audit (Khokhar Table 2, US 1.49/100k). Author to confirm exact figure vs PDF before submission. |
| UK paediatric SBS-IF prevalence | ~16.7 per million | `khokhar2025global` | Khokhar (UK 1.67/100k). NOTE: `beath2011trends` now cited separately as HPN point-prevalence, NOT as the SBS-IF prevalence source (writer-critic fix #2). |
| Prior modelled Brazil paediatric figure | ~1.4 per million | `khokhar2025global` | Khokhar Table 2 modelled Brazil/LatAm (0.14/100k). Basis of the "estimate exceeds prior modelled figure" framing. |
| US claims-based paediatric SBS-IF | ~9 per million | `ali2025epidemiology` | Komodo claims database, PN-proxy + dedup; from librarian audit + source note. |
| Leite multicentre study | 207 patients, 3 centres (SP + RS) | `leite2025multicenter` | Verified by librarian (PDF read). Location corrected SP/RS. |
| RESTORE registry | 20 LatAm centres | `rumbo2024restore` | Verified by librarian against JPEN/PubMed. |
| HCPA rehabilitation programme | first 54 paediatric HPN patients | `goldani2022outcomes` | Verified (JPGN, PMID 35578384). |
| Nordic SBS cohort (NEC-dominated) | 208 patients | `mutanen2023nordic` | Verified (Clinical Nutrition, PMID 37270343). |
| IIFR outcomes benchmark | 362 paediatric IF patients, 26 centres | `avitzur2024iifr` | Verified (Eur J Pediatr Surg). |
| RARAS registry (Brazil rare disease) | first national registry | `andrade2025paving` | In biblio.bib; BMC Digital Health 2025. |

## Open items for the authors before submission
1. Confirm the exact Khokhar figures (14.9, 16.7, 1.4 per million) against the source PDF (`references/khokhar2025global.pdf`).
2. Confirm the `mukhopadhyay2019` ≥85% survival figure used in Results §Healthcare Utilisation.
3. When replication scripts are deposited to `scripts/`, re-link each paper-internal value above to a specific script line + output file.
