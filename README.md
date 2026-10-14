# Harvard Manchester CSL

A standalone Harvard Manchester Citation Style Language (CSL) file for software
that supports CSL. The project aims to avoid repeated work and support
collaboration while preserving the Library Student Team's original credit.

**0.1.0-dev.1 — experimental source revision, 14 October 2026.**
This revision updates the August 2025 draft for review and testing; it is not a
supported or institutionally approved release. The
[University copyright notice](COPYRIGHT.md) is applied at the maintainer's
direction. No open licence is granted.
It is a general CSL style, not a Quarto extension.

## Installation

Download [harvard-manchester.csl](harvard-manchester.csl) and select/import that
single file using your application's CSL-style mechanism. No other repository
files are required for the style itself. Application metadata/export support
needs its own checks. See [rights and attribution](THIRD-PARTY.md).

## Use with Quarto

Quarto is one example of software that can use this style. Put the downloaded
file beside your document, supply your bibliography and select it:

```yaml
bibliography: references.json
csl: harvard-manchester.csl
lang: en-GB
link-citations: true
```

Keep the normal citation processor enabled. The style needs no Lua filter,
model, browser script or developer tooling. Use native citations such as
`[@key]`, `@key` and `[@key, p. 12]`; replace `key` with your bibliography ID.

From this checkout, try [example.qmd](example.qmd):

```sh
quarto render example.qmd --to html
quarto render example.qmd --to docx
```

The standalone example selects nine **fictional** records in
[examples/references.json](examples/references.json). Its URLs and DOI are
placeholders, not research evidence. Replace the records with your own facts.
[AUTHORING.md](AUTHORING.md) explains source fields and input boundaries.

## Scope and verification

Tested processor baselines are **Pandoc 3.10** through Quarto 1.11.5 pre-release
on Windows, and **citeproc-js** npm package 2.4.63 (exported processor 1.4.61).
Independent processor checks cover 15 core cases / 18 citation transactions
and 19 follow-up cases / 57 transactions. The follow-up's desired results all
pass citeproc-js; Pandoc meets 18 and has the exact page-count limitation below.
The broader native suite has 64 desired passes and that limitation among
65 cases. A known difference is not counted as a desired semantic pass.

HTML and Word are the primary tested example outputs. EPUB readback and
explicit-citeproc Typst/PDF compilation are bounded additional checks. They do
not establish reading-system, PDF-layout, assistive-technology or institutional
acceptance. No stable Quarto floor, Zotero/Mendeley application support or
universal CSL-client compatibility is inferred. Natbib, biblatex and Typst's
independent citation processor need separate evaluation.

The style handles native narrative, parenthetical and suppress-author modes;
locators; creator/title/date fallbacks; year-then-author grouped citations;
alphabetical references; and same-author/year letters in first-citation order.
It preserves parent-editor/interviewer roles, anonymous newspaper identity,
authored approximate dates and unabbreviated numeric page endpoints. DOI takes
precedence over URL; authors supply canonical DOI and edition metadata.

Layouts cover books, chapters, articles/reviews, reports/proposals, teaching
materials, media, software, legal records, maps, manuscripts, interviews and
web/database entries. Labels, translations and special facts are explicit
inputs. The style does not infer source categories or generate bibliography data.

Known boundaries:

- Pandoc 3.10 prints a singular label for total `number-of-pages` above one.
  For that processor, supply authored extent text such as
  `dimensions: "66 pp."` and omit `number-of-pages`. The workaround is tested.
- Full Act citation controls require an authored year-free `title-short` and
  known `issued` year alongside the complete official title. Legacy title-only
  Acts have a documented suppress-author limitation.
- Omit first-edition metadata and supply bare lowercase DOI values. Standard
  CSL cannot perform arbitrary value comparisons or DOI string cleanup.

The [Library guide](https://subjects.library.manchester.ac.uk/referencing/harvard)
is labelled October 2026. Its inconsistent instructions/examples require stated
choices; this candidate uses first-author “et al.” for four or more bibliography
authors. School-specific requirements and human review still apply. Composition
with Additional Citation Options requires that extension's separate style check.

## Contributions and AI transparency

The starting CSL was created by the Library Student Team at the University of
Manchester. Its original author/contributor names and roles remain in the CSL.
**Kai Prince** maintains the project and is also named as a CSL contributor.
Kai has written permission to develop the Manchester Harvard referencing CSL.

The 2025 Git history records Kai's earlier work on
[citation locators](https://github.com/kai-prince-sfhea/Harvard-Manchester-CSL/commit/a167fe0caecbc5c0acbf90016eb710135abd9f19),
[citation affixes and grouped layouts](https://github.com/kai-prince-sfhea/Harvard-Manchester-CSL/commit/e45d0125cbb5ad5ad1c80b16a9db8e15bddfc120),
[name disambiguation](https://github.com/kai-prince-sfhea/Harvard-Manchester-CSL/commit/b47db1a9a4057303feb3522f0e298277ef07a65f)
and [missing-author title fallbacks](https://github.com/kai-prince-sfhea/Harvard-Manchester-CSL/commit/1b72d62dffa2f628d53c23e6bb8ca8f7a7256cb8).
The initial import already credited the original team; repository authorship is
not a claim that Kai created all imported material.

The current 2026 revision was **materially developed with OpenAI Codex under
Kai's direction**. Assistance includes primary-source research, substantive CSL
implementation/refactoring, documentation, fictional examples and expected
results, deterministic data-preparation tools, test harnesses, performance
proposals and automated review. This disclosure covers the current development
pass. Historical commit metadata alone cannot establish earlier AI use or its
absence; no human-only or AI-free claim is made for that history.

AI-assisted checks and reviews do not replace independent human academic-style
or accessibility acceptance. Kai's direction does not imply completion of those
reviews, and no University endorsement is claimed. The CSL has no AI runtime
and never generates or completes bibliographic facts.

Developer tools, schemas, detailed research, historical examples and test
receipts live outside this user folder. They are not rendering dependencies;
the complete automated audit suite cannot be reproduced from this checkout
alone. The commands above remain usable. Historical generated files and
guide-derived examples have been removed from the current payload while the
existing Git history is retained. See [CHANGELOG.md](CHANGELOG.md),
[SECURITY.md](SECURITY.md), [COPYRIGHT.md](COPYRIGHT.md) and
[THIRD-PARTY.md](THIRD-PARTY.md).

## Original credit

The original Library Student Team credits are retained:

- Adrian Kosikowski — original CSL author.
- Lea Anderton — contributor.
- David Hirst — contributor.
- Dhruv Mistry — contributor.
- Preenal Asher — contributor.

The [University copyright notice](COPYRIGHT.md) applies to University material;
no Apache or Creative Commons licence is asserted for this candidate. A licence
selected for separate extensions does not relicense this style, the Library
guide or historical third-party resources.
