# EXPLANATION: What is "n" in Each Table?

**"n"** is a standard research abbreviation for **sample size** or **count**. Here's what it means in each table:

---

## TABLE 1: Modality Comparison
**Column "n"** = Number of studies using each modality

| Modality | n | Meaning |
|----------|---|---------|
| Intracortical arrays | 10 | 10 studies used intracortical microelectrodes |
| ECoG | 18 | 18 studies used electrocorticography |
| Scalp EEG | 20 | 20 studies used scalp EEG |
| MEG | 8 | 8 studies used magnetoencephalography |
| fMRI | 6 | 6 studies used functional MRI |
| sEEG | 4 | 4 studies used stereotactic (depth) EEG |
| HD-sEMG | 3 | 3 studies used high-density surface EMG |
| **(Total across all modalities) = 71 studies** |

---

## TABLE 2: Architecture Summary
**Column "n"** = Number of studies using each AI architecture class

| Architecture | n | Meaning |
|-------------|---|---------|
| Traditional ML | 8 | 8 studies used classical machine learning (SVM, Random Forest, etc.) |
| CNN | 13 | 13 studies used Convolutional Neural Networks |
| RNN/LSTM | 10 | 10 studies used Recurrent/LSTM architectures |
| Seq2Seq | 7 | 7 studies used Sequence-to-Sequence models |
| Transformer | 10 | 10 studies used Transformer architectures |
| Self-Supervised | 8 | 8 studies used self-supervised learning pre-training |
| LLM-Integrated | 14 | 14 studies integrated language models |
| Foundation Models | 2 | 2 studies used foundation model approaches (e.g., BrainBERT) |
| **(Total) = 71 studies** |

---

## TABLE 3: Benchmark Comparability
**No "n" column** — This is a methodological recommendations table, not a data count table.

Each row shows a dimension affecting benchmark comparison and cites studies supporting that recommendation.

---

## TABLE 4: Generalization Evidence
**Column "n"** = Number of studies showing each type of generalization

| Generalization Type | n | Meaning |
|------------------|---|---------|
| No generalization | 40 | **40 studies showed NO cross-participant or cross-session generalization** (single-participant only) |
| Cross-session | 18 | 18 studies tested performance across different sessions/days |
| Cross-participant | 13 | 13 studies tested transfer across different participants |
| Cross-modal | 5 | 5 studies tested transfer across different neural recording modalities |
| Cross-language | 2 | 2 studies tested transfer across different languages |
| **(Total) = 71 studies** |

**⚠️ CRITICAL FINDING:** 56.3% of all studies (40/71) showed NO generalization — this is the main barrier to clinical translation!

---

## TABLE 5: Performance Metrics
**Column "n Studies"** = Number of studies using each performance metric

| Metric | n | Meaning |
|--------|---|---------|
| WER | 31 | 31 studies reported Word Error Rate |
| CER | 8 | 8 studies reported Character Error Rate |
| Accuracy | 24 | 24 studies reported classification accuracy |
| Pearson r | 12 | 12 studies reported correlation with actual speech |
| WPM | 6 | 6 studies reported Words Per Minute (communication rate) |
| BLEU | 4 | 4 studies reported BLEU scores (NLP translation metric) |
| ROUGE | 3 | 3 studies reported ROUGE scores (text similarity) |
| MOS | 2 | 2 studies reported Mean Opinion Scores (subjective quality ratings) |
| CIL | 1 | 1 study reported information-theoretic Channel Information Loss |
| **(Total) = 91 studies** |

**Note:** Some studies reported multiple metrics, so total > 71

---

## TABLE 6: Landmark Invasive Systems
**Column "N"** = Sample size (number of participants in that specific study)

| Study | N | Meaning |
|-------|---|---------|
| Herff et al. 2015 | 7 | Study included 7 participants with ECoG electrodes |
| Anumanchipalli et al. 2019 | 1 | Single patient case study |
| Makin et al. 2020 | 1 | Single patient case study |
| Moses et al. 2021 | 1 | Single patient case study (intracortical) |
| Willett et al. 2023 | 1 | Single patient case study (intracortical) |
| Card et al. 2024 | 1 | Single patient case study (intracortical) |

**Key insight:** Most recent breakthrough studies (n=1) are proof-of-concept with single patients. Earlier studies had larger samples (n=7).

---

## TABLE 7: Non-Invasive Systems Summary
**Column "n"** = Number of studies in each category

| Modality & Task | n | Meaning |
|-----------------|---|---------|
| EEG Closed-set (4-10 class) | 12 | 12 studies tested closed-set classification with EEG |
| EEG Open-vocabulary | 5 | 5 studies tested open-vocabulary word decoding with EEG |
| MEG Perceived speech | 3 | 3 studies used MEG to decode perceived (heard) speech |
| MEG Semantic reconstruction | 2 | 2 studies used MEG for semantic/meaning-level decoding |

**Total (non-invasive modalities) = 22 studies**

---

## TABLE 8: Cross-Participant Generalization Detail
**Column "N"** = Sample size (number of participants in cross-participant study)

| Study | N | Meaning |
|-------|---|---------|
| Peterson et al. 2021 | 28 | Transfer learning tested on 28 EEG participants |
| Singh et al. 2025 | 25 | Group decoder tested on 25 sEEG participants across sites |
| deBorman et al. 2024 | 8 | Event detection tested on 8 ECoG participants |

**+10 additional studies** (specific N values listed in full text)

**Key insight:** Cross-participant studies require large multi-participant datasets (N=8-28), which are rare. Most brain-to-speech work is single-participant (N=1).

---

## SUMMARY: How to Interpret "n"

✅ **In modality/architecture/metric tables (1, 2, 5):** n = COUNT OF STUDIES using that approach
- Example: "n=20 for EEG" means 20 different papers used EEG

✅ **In generalization table (4):** n = COUNT OF STUDIES showing that type of generalization
- Example: "n=40 No generalization" means 40 studies didn't test generalization

✅ **In detailed study tables (6, 7, 8):** N = SAMPLE SIZE (participants) in that specific study
- Example: "N=28" for Peterson et al. = that study included 28 brain-imaging participants

---

## Why This Matters for Your Review

The distinction is critical:
- **Small n (study counts)** = Limited evidence base (e.g., only 2 cross-language studies!)
- **Small N (sample sizes)** = Single-participant proof-of-concept (limited generalization)
- **Large n (study counts)** = Robust evidence across many research groups
- **Large N (sample sizes)** = Evidence of real-world applicability

Your paper's key finding: Most studies (n=71) use single participants (N=1), so 56% show NO generalization. This is why clinical deployment is limited!

