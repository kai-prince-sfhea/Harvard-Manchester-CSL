# Bibliography authoring

This file describes the general CSL style's input contract. It does not replace
your School's instructions. Use your application's fields that map to standard
CSL data. CSL JSON and compatible bibliography converters are examples;
application/exporter support for individual fields needs its own checks.
[examples/references.json](examples/references.json)
contains fictional, schema-valid starter records.

Supply bibliographic facts, including sentence casing and proper nouns, yourself.
The style formats supplied data; it cannot establish that a record is accurate.
Keep subtitles within `title`, separated by a colon. Use `author` with
`family`/`given` for people, and `literal` for organisations or screen names.
Use `issued` and `accessed` date-parts arrays. An absent `issued` prints “no date”.
For a known approximate publication date, supply `circa: true` inside `issued`,
for example `{"date-parts": [[1648]], "circa": true}`. It prints `ca. 1648`;
date ranges retain both supplied endpoints. This flag records uncertainty you
have established; the style does not infer it from a title or missing date.

Editors lead an edited book when no author is supplied. A chapter's parent
editor and an interview's interviewer keep their own roles and do not become
the missing author. Such records use their own title as the fallback identity.
For an anonymous newspaper article, a supplied `container-title` (the newspaper)
leads the reference and citation; the quoted article title remains in the
reference. If the newspaper name is also missing, the article title is used.
Supply an organisation in `author` explicitly when it is the responsible creator.

## Common inputs

| Source | `type` | Additional fields used |
|---|---|---|
| Book; e-book; translated or edited book | `book` | `title`, `translator`, `editor`, `collection-title`, `edition`, `publisher-place`, `publisher`, `archive` (provider) |
| Chapter | `chapter` | `title`, `editor`, `container-title`, `edition`, `page`, publisher fields |
| Journal article; advance article; systematic review | `article-journal` | `title`, `container-title`, `volume`, `issue`, `page` or `number`, `status`, `medium` or `genre`, `archive`/`source` |
| Report; annual/technical/government report; grant proposal | `report` | `title`, `number`, publisher fields, `dimensions` (authored duration/extent), `number-of-pages`, `page`, `archive`, `note`, `status` |
| Webpage | `webpage` | `title`, `URL`, `accessed` |
| Blog; newspaper article | `post-weblog`; `article-newspaper` | `title`, `container-title`, complete `issued`, `page` |
| Standard | `standard` | corporate `author`, `number`, `title`, `medium`/`genre`, publisher fields |
| Thesis/dissertation | `thesis` | `title`, `genre` (degree/status), `publisher` (awarding institution), `archive` |
| Patent | `patent` | `title`, `number`, `source` |
| Conference paper | `paper-conference` | `title`, `container-title`, `event-title`, `event-place`, `event-date`, publisher fields, `page` |
| Podcast | `broadcast` with `author` | `title`, `medium: Podcast`, complete `issued`, publisher fields |
| Film/broadcast | `motion_picture`; `broadcast` without `author` | `title`, `director`, `medium`, publisher fields |
| Track; album | `song` | `composer` or `author`, `title`, optional album `container-title`, `medium`, publisher fields |
| Photograph/image | `graphic`; `figure` | `title`, authored `medium`, `page`, publisher fields |
| Software/AI tool | `software` | `title`, `version`, `medium` |
| Social post | `post` | literal `author`, `title`, `medium`, optional `note` containing only authored clock text, complete `issued` |
| Neutral-citation legal case | `legal_case` | `title` (parties), `authority`, `number`, `archive`; omit `author`/`editor` so citations use the title |
| Act | `legislation` | complete `title` including year, `URL`, `accessed`; omit `author`/`editor` |
| Wikipedia/wiki entry | `entry-encyclopedia` | `title`, `container-title`, `issued`, `URL`, `accessed`; omit `author`/`editor` |
| Entry within a database | `entry` | `title`, `container-title`, `archive` |
| Dataset/database resource | author-selected `dataset` | `title`, `version`, `medium`, publisher fields, `archive`/`source` |
| Map/GIS | `map` | `title`, `scale`, `container-title` (datafile), `source` (software), publisher fields |
| Handout/presentation/self-citation | `document` | `title`, `collection-title` (module), `medium`, `publisher` (institution), `status` |
| Microform; programme; other document | `pamphlet`; `document` | `title`, `medium`, event and publisher fields; `container-title` and `editor` (theatre group) for a programme article |
| Manuscript | `manuscript` | `title`, `collection-title`, `medium`, `archive`, `archive-place`, `call-number`, `archive_location`, `number`, `status` |
| Interview | `interview` | `author` (interviewee), `title`, `interviewer`, `container-title`, `medium`, complete `issued`, `page`, `event-place`, `note`, `status` |
| Anonymised personal communication | `personal_communication` | literal `author` (pseudonym without brackets), `title`, `medium`, `event-place`, `status`; bibliography adds brackets around the pseudonym, citations do not |

`archive` takes precedence over `source` for provider display; omit duplicate
provider strings. On a map, `source` specifically identifies the GIS software.
`medium` takes precedence over `genre` when a bracketed description is needed.
Write the label itself, without square brackets. These are explicit data
contracts: the style does not infer a source category from prose or a label's
spelling. Anonymised identifiers must be authored without identifying the person.
Do not put private information in a bibliography that will be published.

## Input boundaries

- Omit `edition` for a first edition. Use a number such as `2` for `2nd edn.`,
  or `rev` for `rev edn.`. Standard CSL cannot compare a value with `1`.
- Supply a **bare, lowercase DOI**, for example `10.5555/fixture`, without a
  DOI URL prefix. DOI takes precedence over URL and suppresses the access date.
  For URL-only sources, supply `accessed`; the style never invents it.
- Omit a report's `publisher` when it duplicates its corporate author. CSL
  cannot compare arbitrary author and publisher strings.
- `number-of-pages` is a total count, separate from a cited `page` range. Its
  CSL label is contextual (`1 p.`, `2 pp.`). Pandoc 3.10 has a reproduced
  processor defect that prints a singular label for larger counts. For that
  processor, supply explicit extent text such as `dimensions: "66 pp."` and
  omit `number-of-pages`. This uses a known fact without guessing or changing it.
- Give complete page endpoints (`123-129`). The style expands supported numeric
  ranges. Roman page locators omit the page label; other locator labels use
  native Quarto syntax, for example `[@key, chap. 3]`.
- For non-Roman work, put an **authored** translation in square brackets in
  `title` after the original title. The style cannot translate or distinguish
  an original title from a translation automatically.
- `note` is a public display field on social posts, reports, documents/pamphlets,
  personal communications, interviews and manuscripts. Unlisted item types also
  use the generic document layout. Keep private scratch notes elsewhere. A social
  post's optional clock is authored note text; no clock is inferred from a year
  or extracted from prose.

For a programme, supply `event-date` explicitly. The whole-programme route puts
the date before its medium; a contribution additionally supplies a parent
`container-title` and optional theatre-group `editor`. Venue/location use
`event-title`/`event-place`, falling back to `publisher`/`publisher-place`.
Teaching-module `collection-title` takes precedence over programme containers.

The original bibliography and example files are historical authoring material,
preserved byte-for-byte outside the current user folder and in existing Git
history. They include nonstandard `database`, `institution` and `subtitle` inputs
that need individual review; changing them all to one type or field can change
their meaning. Use the fictional starter bibliography for new examples.
Developer-only preparation tools can create a separately audited copy from an
explicit mapping; they are not a rendering dependency.

## Quarto citation examples and tested outputs

Use `@key` for narrative citations, `[@key]` for parenthetical citations,
`[-@key]` to suppress the author, and `[@key, pp. 12-15]` for locators. Secondary
references require you to identify the source you actually read; do not invent
an unseen source's bibliographic details. Repeated citations remain author-date;
this style does not produce ibid.

An Act's complete `title` includes its year. For full native citation controls,
also supply a year-free `title-short` and the known `issued` year, for example
`title: Fixture Act 2024`, `title-short: Fixture Act`, and `issued` year `2024`.
Then `@act` gives *Fixture Act* (2024), `[@act]` gives (*Fixture Act* 2024), and
`[-@act, sec. 3]` gives (2024, sec. 3). The reference keeps the complete title.
No short title or year is extracted automatically.

Without `title-short`, the complete title is treated as one citation identity:
`@act` displays it and `[@act]` puts it in parentheses. Avoid suppress-author
syntax on that legacy route: there is no separate printed year, and the current
processor can leave a leading separator before a locator or warn about an empty
citation. Wiki entries and legal cases retain a separate year and support the
ordinary year-only form.

Tested processors include Pandoc citeproc and bounded offline citeproc-js
checks; the style is designed for other CSL applications too. Quarto Word output
contains formatted references, not live Zotero/Mendeley fields. Natbib/biblatex,
Typst's independent processor and reference-manager applications need their own
compatibility checks. Additional Citation Options has a separate admission
check for changed styles; use native citation syntax unless that combination
has been verified.
