# Publications

Papers, manuals, and reports that the
[ESIP Soil Ontology and Informatics Cluster](https://wiki.esipfed.org/Soil_Ontology_and_Informatics_Cluster)
cites when building the [Soil Data Landscape](../../Soil_data_landscape.md).

Each publication gets one card. Cards live in this folder as `<slug>.md`.

## Card structure

````markdown
---
type: publication
title: Soil Survey Manual
description: The authoritative description of USDA soil survey practice; the source of the
  field terminology most US soil datasets encode.
resource: https://www.nrcs.usda.gov/resources/guides-and-instructions/soil-survey-manual
citation: Soil Science Division Staff. (2017). *Soil survey manual* (C. Ditzler, K. Scheffe,
  & H. C. Monger, Eds.; USDA Handbook 18). Government Printing Office.
tags: [manual, usda, soil-survey]
timestamp: 2026-07-20T00:00:00Z
---

Free-text notes. Link to other cards with wiki links, e.g. [[organization_USDA]].

# Citation

```{bibtex}
@techreport{USDA2017,
  author = {Soil Science Division Staff},
  year = {2017},
  title = {Soil survey manual},
  editor = {C. Ditzler and K. Scheffe and H. C. Monger},
  type = {USDA Handbook},
  number = {18},
  publisher = {Government Printing Office},
  address = {Washington, D.C.}
}
```
````

(The Soil Survey Manual has no DOI, so `resource` falls back to the NRCS landing page.
A card for a journal article would use `resource: https://doi.org/10.xxxx/yyyy`.)

## Fields

| Field | Required | Notes |
|---|---|---|
| `type` | yes | Always `publication`. |
| `title` | yes | Title of the publication as published. |
| `description` | yes | **Why this publication is in the landscape.** Say what it contributes or which other cards lean on it. Do not summarize the abstract. |
| `resource` | yes | A URL-formatted DOI (`https://doi.org/10.xxxx/yyyy`) when the publication has one. If it has no DOI, use any stable URL for the publication — a publisher landing page, agency page, or repository record. Bare DOIs (`10.xxxx/yyyy`) are not used. |
| `citation` | yes | Human-readable citation in **APA 7th edition**. Use this format for every card so the set stays consistent. |
| `tags` | no | YAML list of short keywords, per OKF §4.1. |
| `timestamp` | no | ISO 8601 datetime of the last meaningful change to the card, per OKF §4.1 — e.g. `2026-07-20T00:00:00Z`. This is the card's modification time, not the publication date. |

## The Citation section

`# Citation` is the only required section in the card body, and it must contain a
BibTeX entry in a fenced `{bibtex}` code block. Everything else is optional: notes,
context, cross-links to actors and data resources.

The BibTeX entry and the `citation:` frontmatter field describe the same work twice. Write
`citation` for someone reading the card, and the BibTeX block for someone importing the
bibliography into Zotero or a LaTeX paper.

Brace every BibTeX field value (`title = {Soil survey manual}`), including numbers, so
the entries parse cleanly.

Filenames are `<first-author>-<year>-<short-title>.md`, kebab-case.

## Cards

* [Data Standards for Soil: Why aren't they taking root?](onerhime-2021-data-standards-for-soil.md) — Onerhime 2021. Surveys many of the actors and soil data resources listed here, then asks why so few of the published soil data standards get used.
* [Exploring a Dynamic Soil Information System: Proceedings of a Workshop](nasem-2021-dynamic-soil-information-system.md) — NASEM 2021. Records what US soil scientists and agencies say a soil information system should do, including the gaps they found in existing holdings.
* [Exposing vocabularies for soil as Linked Open Data](labate-2015-soil-vocabularies-linked-open-data.md) — L'Abate et al. 2015. Documents an early attempt to republish existing soil vocabularies as Linked Open Data.
* [Ten simple rules for making a vocabulary FAIR](cox-2021-ten-simple-rules-vocabulary-fair.md) — Cox et al. 2021. Gives ten concrete criteria for whether a vocabulary is FAIR.
