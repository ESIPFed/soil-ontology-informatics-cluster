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
description:
  The authoritative description of USDA soil survey practice; the source of the
  field terminology most US soil datasets encode.
resource: https://www.nrcs.usda.gov/resources/guides-and-instructions/soil-survey-manual
citation:
  Soil Science Division Staff. (2017). *Soil survey manual* (C. Ditzler, K. Scheffe,
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

| Field         | Required | Notes                                                                                                                                                                                                                                               |
| ------------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type`        | yes      | Always `publication`.                                                                                                                                                                                                                               |
| `title`       | yes      | Title of the publication as published.                                                                                                                                                                                                              |
| `description` | yes      | **Why this publication is in the landscape.** Say what it contributes or which other cards lean on it. Do not summarize the abstract.                                                                                                               |
| `resource`    | yes      | A URL-formatted DOI (`https://doi.org/10.xxxx/yyyy`) when the publication has one. If it has no DOI, use any stable URL for the publication — a publisher landing page, agency page, or repository record. Bare DOIs (`10.xxxx/yyyy`) are not used. |
| `citation`    | yes      | Human-readable citation in APA 7th edition (suggested). Use this format for every card so the set stays consistent.                                                                                                                                 |
| `tags`        | no       | YAML list of short keywords, per OKF §4.1.                                                                                                                                                                                                          |
| `timestamp`   | no       | ISO 8601 datetime of the last meaningful change to the card, per OKF §4.1 — e.g. `2026-07-20T00:00:00Z`. This is the card's modification time, not the publication date.                                                                            |

## The Citation section

`# Citation` is the only required section in the card body, and it must contain a
BibTeX entry in a fenced `{bibtex}` code block. Everything else is optional: notes,
context, cross-links to actors and data resources.

The BibTeX entry and the `citation:` frontmatter field describe the same work twice. Write
`citation` for someone reading the card, and the BibTeX block for someone importing the
bibliography into Zotero or a LaTeX paper.

Brace every BibTeX field value (`title = {Soil survey manual}`), including numbers, so
the entries parse cleanly.

Filenames are `<first-author>-<year>.md`, kebab-case.

## Cards

### Journal articles, technical reports, publications

- [Data Standards for Soil: Why aren't they taking root?](onerhime-2021.md) — Onerhime 2021. Surveys many of the actors and soil data resources listed here, then asks why so few of the published soil data standards get used.
- [Exploring a Dynamic Soil Information System: Proceedings of a Workshop](nasem-2021.md) — NASEM 2021. Records what US soil scientists and agencies say a soil information system should do, including the gaps they found in existing holdings.
- [Exposing vocabularies for soil as Linked Open Data](labate-2015.md) — L'Abate et al. 2015. Documents an early attempt to republish existing soil vocabularies as Linked Open Data.
- [Ten simple rules for making a vocabulary FAIR](cox-2021.md) — Cox et al. 2021. Gives ten concrete criteria for whether a vocabulary is FAIR.

### Manuals, references, and methods

- [Kellogg Soil Survey Laboratory Methods Manual](usda-2022.md) — Soil Survey Staff 2022. Defines the methods for USDA-NRCS soil laboratory data and operational procedures.
- [Soil Chemical Methods: Australasia](rayment-2011.md) — Rayment & Lyons 2011. The method reference behind the CSIRO Australian soil vocabularies.
- [World Reference Base for Soil Resources 2014, Update 2015](iuss-2015.md) — IUSS Working Group WRB 2015. The international soil classification system that national datasets are correlated against.
- [Guidelines for Soil Description](fao-2006.md) — FAO 2006. Supplies the controlled field-description terminology that WRB classification uses.
- [Manuel du Réseau de Mesures de la Qualité des Sols (RMQS)](jolivet-2006.md) — Jolivet et al. 2006. Sampling and measurement protocol for the first French national monitoring campaign.
- [Manuel du Réseau de mesures de la qualité des sols, RMQS2](jolivet-2018.md) — Jolivet et al. 2018. Protocol for the second French campaign, 2016 to 2027.
- [Cahier des charges pour la cartographie des sols au 1/50 000](inra-2019.md) — INRA InfoSol 2019. How French 1:50 000 soil maps must be produced under IGCS.
- [Référentiel Régional Pédologique: Cahier des Clauses Techniques Générales](inra-2014.md) — INRA InfoSol 2014. How French 1:250 000 regional soil databases are built and certified.
- [Georeferenced Soil Database for Europe: Manual of Procedures](esb-2001.md) — European Soil Bureau 2001. Procedures and attribute coding behind the European Soil Database.
- [Specifications: Tiered GlobalSoilMap Products, Release 2.4](globalsoilmap-2015.md) — GlobalSoilMap Science Committee 2015. Depth intervals, properties, and uncertainty reporting for GlobalSoilMap products.
