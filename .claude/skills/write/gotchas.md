# Write Skill -- Gotchas

Known failure points and edge cases for paper drafting.

- If `personal-style-guide.md` is still the template, the writer now defaults to the shipped AEA house style (`.claude/references/writing-style-aej.md`) rather than a generic academic voice — but run `/write style-guide` on the author's papers for an individualized match. **Symptom of the old failure it prevents:** regression-dump prose with raw `(p<0.001)` / standard errors in sentences, "%" instead of "percent", em-dash overuse. Those are house-style violations; the writer-critic deducts on them (see `writing-style-aej.md` §9.2).
- Writer will draft results from strategy memo predictions if tables don't exist yet -- the hard gate catches this, but watch for it in partial drafts.
- `\citet` vs `\citep` confusion is the most common LaTeX citation issue. `\citet` for "Author (Year)" in prose, `\citep` for "(Author, Year)" parenthetical.
- Writer sometimes invents citation keys not in `Bibliography_base.bib`. Always verify generated `\cite{}` keys against the actual bib file.
- The cleanup pass catches AI patterns but can over-correct domain-specific hedging that's actually appropriate (e.g., "may" in describing potential mechanisms is fine).
- Section ordering varies by paper type. Don't force reduced-form structure on structural papers.
- Abstract word count (150 max per INV-5) is a hard constraint -- the writer sometimes produces 200+ word abstracts on first pass.
