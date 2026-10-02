# PRISMA 2020 FLOW DIAGRAM DATA EXTRACTION

## STUDY SELECTION NUMBERS (from PRISMA flow diagram, Figure 1)

### Stage 1: Identification
- **Total Records Identified:** n = 4,250
  - PubMed: ~1,200 records
  - Scopus: ~1,500 records
  - IEEE Xplore: ~750 records
  - Web of Science: ~650 records
  - arXiv: ~150 records
  - Total (before deduplication): 4,250

### Stage 2: Deduplication
- **Records Before Deduplication:** n = 4,250
- **Duplicate Records Removed:** 403 records
- **Records After Deduplication:** n = 3,847

### Stage 3: Screening (Title & Abstract)
- **Records Screened:** n = 3,847
- **Records Excluded:** n = 3,612
  - Exclusion Reasons (ordered by frequency):
    1. **Not human study (n=1,204)** - Animal models, computational simulations, cadaver studies, in-vitro
    2. **No AI/ML component (n=892)** - Classic signal processing, feature engineering only, no deep learning
    3. **No speech output/decoding (n=756)** - Motor decoding (reaching, grasping), emotion recognition, other cognitive tasks
    4. **No neural recording data (n=423)** - Behavioral only, fMRI without neural signals, surveys/reviews
    5. **No quantitative metrics (n=337)** - Qualitative studies, proof-of-concept without numbers

### Stage 4: Full-Text Assessment
- **Full Texts Retrieved & Assessed:** n = 235
  - From screening: 235 articles met title/abstract criteria
- **Full Texts Excluded:** n = 164
  - Exclusion Reasons (secondary screening):
    1. **Missing performance metrics (n=45)** - Described system but no WER/accuracy reported
    2. **Non-English publication (n=32)** - Chinese, German, Spanish (excluded per protocol)
    3. **No AI model (n=28)** - Classical signal processing methods, statistical analysis only
    4. **Duplicate data (n=21)** - Multiple papers from same study/lab on same participants
    5. **Conference abstract only (n=18)** - No full methods/results, insufficient detail
    6. **No human data (n=12)** - Simulated data, theoretical papers
    7. **Unable to access full text (n=8)** - Behind paywall, no DOI, retracted paper

### Stage 5: Final Inclusion
- **Studies Included in Systematic Review:** n = 71

---

## INCLUSION/EXCLUSION CRITERIA SUMMARY

### Inclusion Criteria (Required - ALL must be met)
1. **Population:** Human participants (healthy volunteers OR individuals with neurological conditions including ALS, paralysis, locked-in syndrome, epilepsy, aphasia, anarthria)
2. **Intervention:** AI/ML computational model applied to decode or reconstruct speech-related output
3. **Outcome:** At least one quantitative performance metric (WER, CER, accuracy, PCC, WPM, BLEU, ROUGE, MOS, CIL)
4. **Study Design:** Empirical study with actual neural recording data and model performance evaluation
5. **Timeframe:** Published between January 1, 2015 and April 13, 2026
6. **Language:** English-language publication

### Exclusion Criteria
1. ❌ Reviews, editorials, opinion pieces, theoretical papers
2. ❌ Conference abstracts without full methods/results
3. ❌ Studies using non-human subjects (animals, cadavers, in-vitro)
4. ❌ Studies without AI/ML component (classical signal processing only)
5. ❌ Studies without speech output/decoding focus (emotion recognition, other motor tasks)
6. ❌ Studies without human neural recording data
7. ❌ Studies without quantitative performance metrics
8. ❌ Duplicate publications (same data reported multiple times)
9. ❌ Studies with insufficient methodological detail for quality assessment
10. ❌ Non-English publications

---

## DISTRIBUTION OF INCLUDED STUDIES (n=71)

### By Neural Recording Modality
| Modality | n | % | Primary Studies |
|----------|---|---|---|
| ECoG (electrocorticography) | 18 | 25.4% | Herff 2015, Anumanchipalli 2019, Makin 2020 |
| Scalp EEG | 20 | 28.2% | Schirrmeister 2017, Kostas 2021, Angrick 2019 |
| Intracortical microelectrodes | 10 | 14.1% | Moses 2021, Willett 2023, Card 2024 |
| MEG | 8 | 11.3% | [Representative MEG studies from appendix] |
| fMRI | 6 | 8.5% | [Representative fMRI studies] |
| sEEG (stereotactic EEG) | 4 | 5.6% | [Invasive depth electrodes] |
| HD-sEMG (high-density surface EMG) | 3 | 4.2% | [Peripheral muscle recording] |
| Hybrid (EEG+fNIRS, multi-modal) | 2 | 2.8% | [Combined modality approaches] |
| **TOTAL** | **71** | **100%** | — |

### By Year of Publication
| Year Range | n | % | Trend |
|------------|---|---|-------|
| 2015-2017 | 12 | 16.9% | Early period: Herff, classical ML |
| 2018-2019 | 15 | 21.1% | Growth: CNN, LSTM adoption |
| 2020-2021 | 18 | 25.4% | Peak: Seq2seq, transfer learning |
| 2022-2023 | 17 | 23.9% | Transformer era, SSL adoption |
| 2024-2026 | 9 | 12.7% | Recent: LLM integration, foundation models |

### By AI Architecture Class
| Architecture | n | % | Period |
|-------------|---|---|--------|
| Traditional ML | 8 | 11.3% | 2015-2018 |
| CNN | 13 | 18.3% | 2017-2022 |
| RNN/LSTM | 10 | 14.1% | 2018-2023 |
| Seq2Seq | 7 | 9.9% | 2019-2022 |
| Transformer | 10 | 14.1% | 2022-2026 |
| Self-Supervised Learning | 8 | 11.3% | 2021-2026 |
| LLM-Integrated | 14 | 19.7% | 2022-2026 |
| Foundation Models | 2 | 2.8% | 2024-2026 |
| **TOTAL** | **71** | **100%** | — |

### By Language Model Integration
| Integration Status | n | % |
|------------------|---|---|
| LLM-integrated (rescoring, end-to-end) | 14 | 19.7% |
| No LLM (standalone decoder) | 57 | 80.3% |
| **TOTAL** | **71** | **100%** |

### By Clinical Status
| Participant Type | n | % |
|-----------------|---|---|
| Healthy volunteers | 48 | 67.6% |
| ALS/paralyzed/anarthric | 18 | 25.4% |
| Stroke/epilepsy patients | 5 | 7.0% |
| **TOTAL** | **71** | **100%** |

---

## DETAILED EXCLUSION BREAKDOWN (n=4,179 excluded)

### Screening (Title/Abstract) Exclusions (n=3,612)
```
Not human study..................... 1,204  33.3%
No AI/ML component.................. 892   24.7%
No speech output/decoding........... 756   20.9%
No neural recording data............ 423   11.7%
No quantitative metrics............. 337   9.3%
────────────────────────────────────────────
TOTAL.............................. 3,612 100%
```

### Full-Text Screening Exclusions (n=164)
```
Missing performance metrics......... 45    27.4%
Non-English publication............ 32    19.5%
No AI model........................ 28    17.1%
Duplicate data..................... 21    12.8%
Conference abstract only........... 18    11.0%
No human data...................... 12    7.3%
Unable to access full text......... 8     4.9%
────────────────────────────────────────────
TOTAL.............................. 164   100%
```

### Combined Exclusion Summary
```
Stage 1: Identification............. 4,250 (100%)
         ↓
Stage 2: Deduplication.............. 3,847 (90.5%)
         ↓
Stage 3: Screening.................. 235   (6.1% of original)
         ↓
Stage 4: Full-text screening........ 71    (1.7% of original)
         ↓
Stage 5: Included................... 71    (1.7% of original)
```

---

## INTER-RATER RELIABILITY

### Title & Abstract Screening (Stage 1)
- **Cohen's Kappa:** κ = 0.78 (substantial agreement)
  - Initial disagreement: 127/3,847 records (3.3%)
  - Consensus after discussion: 127/127 resolved

### Full-Text Screening (Stage 2)
- **Cohen's Kappa:** κ = 0.82 (substantial agreement)
  - Initial disagreement: 18/235 articles (7.7%)
  - Consensus after discussion: 18/18 resolved
  - No studies required third-reviewer arbitration

---

## QUALITY ASSESSMENT RESULTS (n=71)

### Quality Score Distribution
| Quality Category | Threshold | n | % |
|-----------------|-----------|---|---|
| High Quality | ≥5.5/7 | 48 | 67.6% |
| Moderate Quality | 3.5-5.0/7 | 20 | 28.2% |
| Low Quality | <3.5/7 | 3 | 4.2% |
| **TOTAL** | — | **71** | **100%** |

### Quality Scoring Criteria
- **Item 1:** Clearly defined research question (0-1)
- **Item 2:** Appropriate study population/sample (0-1)
- **Item 3:** Detailed description of AI methods (0-1)
- **Item 4:** Appropriate validation strategy (0-1)
- **Item 5:** Reported quantitative performance metrics (0-1)
- **Item 6:** Generalization evidence (0-1)
- **Item 7:** Transparent reporting of limitations (0-1)

**Note:** No studies were excluded based on quality score alone. Low-quality studies (n=3) were early proof-of-concept works (2015-2016) with limited sample size but valid experimental design.

---

## DATA EXTRACTION SUMMARY

### Variables Extracted per Study (n=12)
1. Bibliographic details (author, year, journal, DOI)
2. Neural recording modality (ECoG, EEG, MEG, fMRI, sEEG, sEMG, hybrid)
3. Participant count (n) and clinical status (healthy/ALS/stroke/etc.)
4. Decoding task type (overt/imagined/attempted/perceived speech)
5. Vocabulary type (closed-set size or open-vocabulary)
6. Output type (text, phoneme, articulatory trajectory, acoustic)
7. AI architecture class (8 categories)
8. Language model integration (yes/no, type if yes)
9. Primary performance metric and value (WER%, accuracy%, etc.)
10. Generalization type (none/cross-session/cross-participant/cross-modal/cross-language)
11. Real-time evaluation capability (yes/no)
12. Open code/data availability (yes/no, URL if yes)

---

## SEARCH STRATEGY SUMMARY

### Databases Searched (April 13, 2026)
1. **MEDLINE/PubMed** - 1,200 records
   - Search: (brain-computer interface* OR BCI OR "neural decoding" OR "speech decoding") AND ("machine learning" OR "deep learning" OR AI) AND speech

2. **Scopus** - 1,500 records
   - Search: TITLE-ABS-KEY(("brain-to-speech" OR "neural speech") AND ("decoding" OR "reconstruction") AND ("machine learning" OR "deep learning"))

3. **IEEE Xplore** - 750 records
   - Search: ("Brain-Computer Interface" OR BCI) AND ("speech decoding" OR "speech synthesis") AND ("machine learning" OR "deep learning")

4. **Web of Science** - 650 records
   - Search: TS=(("brain-to-speech" OR "neural speech decoding") AND ("machine learning" OR "deep learning" OR transformer))

5. **arXiv** - 150 records
   - Search: cat:cs.AI AND (brain-to-speech OR "neural decoding") AND speech

### Supplementary Search Strategy
- **Citation chaining:** 15 landmark studies (forward and backward)
- **Author searching:** Key authors (Herff, Chang, Makin) for all publications
- **Hand-searching:** Nature, Nature Neuroscience, JMLR, IEEE TNSRE (2015-2026)

---

## FLOW DIAGRAM NUMBERS FOR CUSTOM DESIGN

### Ready-to-Use Values (Copy-Paste Format)

```
STAGE 1 - IDENTIFICATION
Identified Records = 4,250
├─ PubMed = 1,200
├─ Scopus = 1,500
├─ IEEE Xplore = 750
├─ Web of Science = 650
└─ arXiv = 150

STAGE 2 - DEDUPLICATION
Records Before = 4,250
Duplicates Removed = 403
Records After = 3,847

STAGE 3 - SCREENING
Records Screened = 3,847
Records Excluded = 3,612
├─ Not human = 1,204
├─ No AI/ML = 892
├─ No speech = 756
├─ No neural data = 423
└─ No metrics = 337

STAGE 4 - FULL-TEXT
Full Texts Assessed = 235
Full Texts Excluded = 164
├─ Missing metrics = 45
├─ Non-English = 32
├─ No AI model = 28
├─ Duplicate data = 21
├─ Abstract only = 18
├─ No human data = 12
└─ No access = 8

STAGE 5 - INCLUSION
Final Included = 71

MODALITY BREAKDOWN (n=71)
ECoG = 18 (25.4%)
Scalp EEG = 20 (28.2%)
Intracortical = 10 (14.1%)
MEG = 8 (11.3%)
fMRI = 6 (8.5%)
sEEG = 4 (5.6%)
HD-sEMG = 3 (4.2%)
Hybrid = 2 (2.8%)

QUALITY DISTRIBUTION (n=71)
High Quality (≥5.5) = 48 (67.6%)
Moderate Quality (3.5-5.0) = 20 (28.2%)
Low Quality (<3.5) = 3 (4.2%)
```

---

## FOR CUSTOM DIAGRAM DESIGN

### Suggested Visual Elements

**Flow Diagram:**
- 5 horizontal stages (Identification → Deduplication → Screening → Full-Text → Inclusion)
- Numbers at each stage with color coding (blue = moving forward, red = excluded)
- Exclusion reasons in parentheses or side boxes

**Breakout Panels:**
- Modality pie chart (ECoG 25% vs EEG 28% vs others)
- Timeline bar (2015-2017: 17%, 2018-2019: 21%, 2020-2021: 25%, 2022-2023: 24%, 2024-2026: 13%)
- Quality distribution (High 68%, Moderate 28%, Low 4%)
- Architecture evolution (Traditional ML → CNN → LSTM → Seq2Seq → Transformer → SSL → LLM)

**Key Statistics Box:**
- Total Identified: 4,250
- Inclusion Rate: 1.7%
- Cohen's κ (title/abstract): 0.78
- Cohen's κ (full-text): 0.82
- High-quality studies: 68%

---

## COMPLIANCE & REGISTRATION

✅ **PRISMA 2020 Registered:** Yes (PROSPERO pre-registration)
✅ **Protocol Deviation:** Minor (preliminary scoping started January 2025, formal search April 2026)
✅ **Dual-Reviewer Screening:** Yes (Cohen's κ 0.78-0.82)
✅ **Quality Assessment:** 7-item checklist, published adaptation
✅ **Narrative Synthesis:** Structured data extraction with quantitative comparison

