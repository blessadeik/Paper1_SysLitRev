# PROSPERO amendment: CRD420261368521

Prepared 1 October 2026 for the record "AI for brain-to-speech decoding: methods, performance benchmarks and generalisation across neural recording modalities (2015–2026)".

**How to submit:** log in to PROSPERO, open the record dashboard and choose **Create a major revision**. A minor amendment can't change the methods or the review team. Replace the text of each field below, matching fields by name because the new form may number them differently. Then paste section 1 into the revision note box. All authors must approve a major revision before it is published. PROSPERO keeps the earlier version in the record's history; the changes are dated and visible.

**Submit this before you start your own screening.** The second reviewer has already screened, so the amendment says so. What matters is that it goes in before any decisions are compared or analysed; then it cannot have been influenced by results.

The only item left to fill in is the date of acceptance, used in the manuscript text in section 4.

**Amended protocol documents** (upload the full protocol as version 2): every change is highlighted in yellow, and an amendment history sits at the top.
- [protocol_amended/SYSTEMATIC REVIEW PROTOCOL_v2_amended_Oct2026.docx](protocol_amended/SYSTEMATIC%20REVIEW%20PROTOCOL_v2_amended_Oct2026.docx): the full protocol attached to the PROSPERO record.
- [protocol_amended/PROSPERO PROTOCOL_v2_amended_Oct2026.docx](protocol_amended/PROSPERO%20PROTOCOL_v2_amended_Oct2026.docx): the field-by-field form text.

Your originals in `Paper 1_full docs and info/Additional docs/` are unchanged.

---

## 1. Reason for amendment (paste into the PROSPERO box)

> This amendment is submitted after the second reviewer completed independent title and abstract screening, but before the first reviewer's screening and before any comparison or reconciliation of screening decisions; no screening results have been compared or analysed. (1) The formal database searches were executed on 13 April 2026 as planned, but the exported records were lost when the storage device holding them was damaged. The searches were therefore re-executed on 1 October 2026 using the identical registered strategy and the same eligible publication window (1 January 2015 to 13 April 2026); screening is based on the re-executed searches. (2) Web of Science Core Collection was not searched because the review team does not have institutional access; PubMed, Scopus, IEEE Xplore and arXiv were searched as planned. (3) bioRxiv, named in the original record as a source of preprints, is reclassified as a supplementary source reached through citation chaining and hand-searching rather than a systematically searched database. (4) Ebenezer Adeiza Adeika has joined the review team as co-author and second independent reviewer (screening, data extraction checking, quality assessment, and writing of the manuscript); Dr. Onyema Osuagwu continues as supervisor. (5) High-density surface electromyography (HD-sEMG), listed in the original record among hybrid and peripheral modalities, is now excluded: it records muscle rather than neural activity, which conflicts with the registered population criterion (neural or neuroimaging recording), and no sEMG terms appear in the registered search strategy. Studies that use neural recordings only to evaluate or improve language models, without decoding speech, are also explicitly excluded. (6) Records identified through other methods (citation searching and hand-searching) are screened as a separate stream and reported in the PRISMA 2020 "other methods" column. (7) The anticipated completion date is revised to 30 November 2026. No other changes have been made to the review question, outcomes or synthesis methods.

---

## 2. Field-by-field changes

### Field 4: Anticipated completion date

| Registered | Amended |
|---|---|
| 31 July 2026 | 30 November 2026 |

---

### Field 5: Named contact / review team

**Registered:**
> Primary reviewer: Blessing Isoyiza Adeika. Secondary reviewer / supervisor: Dr. Onyema Osuagwu.

**Amended:**
> Named contact and first reviewer: Blessing Isoyiza Adeika, Department of Electrical and Computer Engineering, Morgan State University, Baltimore, MD, USA (blade3@morgan.edu).
>
> Review team:
> - Blessing Isoyiza Adeika (Department of Electrical and Computer Engineering, Morgan State University): protocol development, searching, screening, data extraction, quality assessment, synthesis and writing.
> - Ebenezer Adeiza Adeika (co-author), BSc Psychology (University of Ilorin); Department of Internal Medicine, Federal Teaching Hospital, Gombe, Nigeria: independent title/abstract and full-text screening, independent cross-checking of data extraction, independent quality assessment, drafting and revising manuscript sections, and approval of the final version.
> - Dr. Onyema Osuagwu (Department of Electrical and Computer Engineering, Morgan State University): supervision and manuscript review.

---

### Field 7: Searches

**Registered (databases):**
> The following five electronic databases will be systematically searched: PubMed (MEDLINE), IEEE Xplore, Scopus, Web of Science (Core Collection), arXiv (via arXiv Search API: cs.HC, eess.AS, q-bio.NC subject categories).

**Amended:**
> Formal searches were first executed on 13 April 2026. The exported records were subsequently lost through damage to the storage device, and the searches were re-executed on 1 October 2026 with the identical registered strategy. Four electronic databases were searched: PubMed (MEDLINE), Scopus, IEEE Xplore, and arXiv (via the arXiv API; categories cs.HC, eess.AS and q-bio.NC). The eligible publication window remains 1 January 2015 to 13 April 2026, applied through each database's date filters and confirmed at screening. Web of Science Core Collection, listed in the original protocol, was not searched because the review team does not have institutional access. The registered three-block Boolean strategy (neural recording terms AND speech-output terms AND AI-method terms) was applied unchanged, adapted only for each database's field syntax. Database-specific strings will be reported in full in the Supplementary Information.

**Registered (supplementary methods):** backward citation tracing, forward citation tracking via Google Scholar for landmark papers, hand-searching of key journals, and screening of NeurIPS/ICLR/ICML/Interspeech/AAAI proceedings (2022–2026). **Keep these, and add:**
> Records identified through supplementary methods (backward and forward citation chaining, hand-searching of key journals and conference proceedings, and bioRxiv preprints identified through these routes) will be screened against the same eligibility criteria and reported separately in the "identification via other methods" column of the PRISMA 2020 flow diagram, with counts for records identified, screened, assessed and included.

**Registered (unpublished studies), text to replace:**
> "...systematic searching of arXiv (cs.HC, eess.AS, q-bio.NC categories) and bioRxiv."

**Amended:**
> Unpublished and grey literature will be identified through systematic searching of arXiv (cs.HC, eess.AS, q-bio.NC) and, for bioRxiv, through citation chaining and hand-searching. Preprints meeting all eligibility criteria will be included and explicitly labelled as preprints in the synthesis.

---

### Field 9: Participants / population

**Keep the registered inclusion and exclusion text, and add to the exclusion list:**
> Studies recording only peripheral physiological signals (for example, surface electromyography of articulatory muscles) without neural or neuroimaging data.

---

### Field 10: Intervention(s) / exposure(s)

**Registered (modalities covered):**
> Hybrid and peripheral: Combined EEG-fNIRS systems, high-density surface electromyography (HD-sEMG) for silent speech

**Amended:**
> Hybrid: combined EEG-fNIRS systems. (Amended October 2026: high-density surface electromyography (HD-sEMG), listed originally, is excluded because it records muscle rather than neural activity and is not covered by the population criterion or the search strategy.)

This is a real change: the original record listed HD-sEMG as a covered modality. Also replace "hybrid/sEMG" with "hybrid EEG-fNIRS" wherever the modality groups are listed (Field 15 extraction variables and Field 19 subgroups). EEG+fNIRS hybrid studies remain eligible, because both signals are recorded from the brain.

---

### Field 12: Types of study to be included

**Keep the registered text, and add to the exclusion list** (also listed in the reason for amendment):
> Studies that use neural recordings only to evaluate or improve language models (encoding or brain–model alignment analyses), without decoding a speech-related output from neural signals.

The registered exclusions are applied as written at screening. For example:
- "Studies reporting exclusively animal data" excludes non-human primate studies such as Degenhart et al. 2020.
- "Non-speech BCI studies (motor imagery, P300 spellers, cursor control)" excludes spelling and movement-decoding studies such as Vansteensel et al. 2016, Chaudhary et al. 2022 and Peterson et al. 2021.

These are not changes, so they do not go into the amendment text.

---

### Field 16: Data extraction (selection and coding)

**Registered:**
> Stage 1: All records retrieved from database searches will be screened independently by both reviewers... Disagreements will be resolved by discussion and, where necessary, by consultation with a third reviewer. Data extraction will be performed by the primary reviewer and independently cross-checked by the secondary reviewer.

**Amended:**
> Title and abstract screening and full-text assessment are performed independently by two reviewers (B.I.A. and E.A.A.), each blinded to the other's decisions, using a standardised screening workbook with pre-specified exclusion reasons. Each reviewer screens a pilot set of 30 randomly selected records before their main screening; the reviewers then compare pilot decisions and agree on how the criteria apply. The second reviewer completed the pilot and main screening before this calibration discussion; the first reviewer's main screening follows it. Main-screening decisions are not revised after calibration, and pilot records are excluded from the agreement statistics. At title/abstract stage, any record marked Include or Unsure by either reviewer proceeds to full-text assessment. At full-text stage, disagreements are resolved by discussion, and any that remain unresolved are referred to the supervising author (O.O.) for a final decision. Agreement is reported as Cohen's kappa at both stages. Data extraction is performed by B.I.A. and independently cross-checked against the source publications by E.A.A.; discrepancies are resolved by discussion.

**Only if you will use AI-assisted checking** (Springer Nature requires disclosure), add:
> A large language model (Claude, Anthropic) is used after both reviewers have completed independent screening, as an additional check that flags records for re-examination, and to pre-fill extraction fields with quoted source text for reviewer verification. All inclusion, exclusion and extraction decisions are made by the human reviewers.

---

### Field 17: Risk of bias (quality assessment)

**Replace "both reviewers" with:**
> Quality assessment is performed independently by two reviewers (B.I.A. and E.A.A.) using the seven-dimension checklist described above; disagreements are resolved by discussion, with unresolved cases referred to the supervising author (O.O.).

Score against the registered seven dimensions exactly. The manuscript will be aligned to the protocol.

---

### Field 28: Stage of review at time of amendment

| Stage | Status |
|---|---|
| Preliminary searches | Completed |
| Formal searches | Completed (executed 13 April 2026; re-executed 1 October 2026 after loss of exports) |
| Piloting of study selection | Started (second reviewer completed; first reviewer not started) |
| Formal screening of search results | Started (second reviewer completed title/abstract screening; first reviewer not started; no decisions compared) |
| Data extraction | Not started |
| Risk of bias assessment | Not started |
| Data analysis | Not started |

**Also correct:** the registered Field 28 note gives the search date as "10 April 2026", while the rest of the record says 13 April 2026. The correct date is 13 April 2026.

---

## 3. What stays the same

- Review question and the three research questions (methods, performance, generalisation).
- Publication window: 1 January 2015 to 13 April 2026.
- English-language restriction.
- The registered search terms (all three blocks).
- arXiv categories (cs.HC, eess.AS, q-bio.NC).
- Outcomes (Fields 14–15), synthesis strategy (Field 18) and subgroup plans (Field 19).
- The quality checklist dimensions.

---

## 4. Matching text for the manuscript's Methods

> The review protocol was registered with PROSPERO (CRD420261368521) and amended on [date of acceptance], after the second reviewer had completed independent title and abstract screening but before the first reviewer's screening and before any comparison of decisions. Searches executed on 13 April 2026 were re-run on 1 October 2026 with the identical strategy and publication window after the original exports were lost to a storage-device failure. The amendment also recorded the omission of Web of Science owing to lack of institutional access, the addition of a second independent reviewer, the exclusion of surface-electromyography studies (listed originally among peripheral modalities) and of encoding-only studies, and a revised completion date. No other deviations from the protocol occurred.
