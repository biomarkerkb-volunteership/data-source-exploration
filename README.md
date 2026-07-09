# Data Source Exploration for BiomarkerKB Expansion

**Duration:** 2 weeks
**Time commitment:** 20 hours/week (40 hours total)
**Wiki reference:** [BiomarkerKB Resource Integration](https://wiki.biomarkerkb.org/BiomarkerKB_Resource_Integration#Resources_for_Exploration)

## Goal

Identify opportunities for expansion of BiomarkerKB by evaluating candidate biomarker data sources and comparing their features against BiomarkerKB's data model.

## Tasks

- Evaluate new biomarker data sources
- Compare features across biomarker resources

## Outputs

- Source evaluation reports (one per source)
- Feature comparison table
- Feature recommendations for BiomarkerKB

## Target Schema

Each evaluation should assess whether a source can populate the following fields. `biomarker`, `assessed_biomarker_entity`/`_id`, and `condition` are **critical fields** - sources that can't support these are lower priority.

| Field | Example |
|---|---|
| biomarker_id | AN6278-1 |
| biomarker | increased IL6 level |
| assessed_biomarker_entity | Interleukin-6 |
| assessed_biomarker_entity_id | UPKB:P05231 |
| assessed_entity_type | protein |
| condition | prostate cancer |
| condition_id | DOID:10283 |
| exposure_agent | |
| exposure_agent_id | |
| best_biomarker_role | prognostic |
| specimen | blood |
| specimen_id | UBERON:0000178 |
| loinc_code | 26881-3 |
| evidence_source | PubMed:10914713 |
| evidence | (supporting text excerpt) |

## Sources to Evaluate

1. [Marker Database](https://themarker.idrblab.cn/)
2. ResMarkerDB *(no link on wiki - needs to be located)*
3. SalivaDB *(no link on wiki - needs to be located)*
4. [GlycanAge Publications](https://glycanage.com/publications)
5. [Cancer Genome Interpreter (Biomarkers)](https://www.cancergenomeinterpreter.org/biomarkers)
6. [Glycan Biomarkers](https://github.com/issues/assigned?issue=clinical-biomarkers%7Cbiomarker-issue-repo%7C248) ([CarboCurator code](https://github.com/glygener/CarboCurator))
7. [Alliance Genome](https://www.alliancegenome.org/)

## Schedule

### Week 1 - Source-by-source evaluation (20h)

- **Kickoff (~1h):** Review target schema, review existing Data Sources page.
- **Evaluations (~17h):** For each of the 7 sources, produce an evaluation report covering:
  - Description / what it covers
  - Access method (API, bulk download, scrape, manual)
  - License
  - Field mapping: can it populate the critical fields and the rest of the schema above?
  - Data volume/scope estimate
  - Recommended integration status: *Direct integration* / *Sample integration* / *Cross-reference* / *Not viable*
  - Open questions/blockers
- **Buffer + check-in (~2h):** Flag any inaccessible or low-value sources so scope can be adjusted before week 2.

### Week 2 - Synthesis (20h)

- **Finish evaluations (~4h):** Wrap up any remaining source reports.
- **Feature comparison table (~8h):** Rows = sources, columns = schema fields + license + access method + integration status.
- **Recommendations (~5h):** Which sources to prioritize for integration, what gaps they'd fill relative to already-integrated sources, any new fields/entity types worth adding to the schema.
- **Write-up + review (~3h):** Final pass, incorporate feedback.

## Deliverables Checklist

- [ ] 7 source evaluation reports
- [ ] Feature comparison table
- [ ] Recommendations memo
