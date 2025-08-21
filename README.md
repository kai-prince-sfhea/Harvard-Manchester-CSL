# Harvard Manchester CSL

This is a repository for developing and maintaining the Harvard Manchester citation style for use with software that are not compatible with EndNote Styles (.ens).

For example:

- Quarto (open-source scientific and technical publishing system)
- Any other Pandoc-based tool
- Zotero
- Mendeley

The reason behind hosting this CSL on GitHub is to enable collaboration and version control, making it easier for contributors to propose improvements and for specific changes to be tracked.

The reason that I am hosting this GitHub repository is that I am currently working on a Quarto project that requires the Harvard Manchester citation style, and I want to avoid repeated efforts.

## Original Credit

Before starting this project, I used the CSL created by the Library Student Team at the University of Manchester. The CSL is based on the Harvard Manchester style guide, which is available [here](https://subjects.library.manchester.ac.uk/referencing/harvard).

Those involved in the creation of the original CSL include:

- Adrian Kosikowski
- Lea Anderton
- David Hirst
- Dhruv Mistry
- Preenal Asher

## Preview

You can see the render output of the CSL in index.html within the _site folder.

## Development Progress

- [x] Get the current draft CSL created by the Library Student Team.
- [ ] Get the in-text citations working in Quarto.
  - [x] Get citation locators (e.g., page numbers) working.
  - [x] Get citation prefixes and suffixes working.
  - [x] Merge single citation of multiple authors supporting the same argument with year-author ordering.
  - [x] Get disambiguation of multiple authors with the same surname working.
  - [x] Have citations with no author use the title of the work italicised.
  - [x] Get no parenthesis citations working (I've created an additional-citation-options Quarto extension to do this).
- [ ] Get the reference citations working in Quarto.
- [ ] Get the style working in Zotero and Mendeley.