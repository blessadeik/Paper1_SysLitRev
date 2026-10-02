# Pre-submission review: *Nature Machine Intelligence*

Manuscript: "Artificial Intelligence for Brain-to-Speech Decoding: A Systematic Review of Methods, Performance Benchmarks, and Generalization Across Neural Recording Modalities (2015-2026)"
Reviewed: 30 September 2026, version in `overleaf/` (commit on `main`)
Evidence: per-reference verification reports in `review/reference_checks/refcheck_1.md` to `refcheck_5.md` (90 BibTeX entries, each checked against the published paper).

## Verdict

**Not ready for submission.** The limit is data integrity, not prose. The study register that the review's statistics depend on is not in the repository. The only per-study table in the repository (Supplementary Table S1) contains rows that do not correspond to real papers. Also, dozens of study-level claims in the text contradict the papers they cite. Editing for flow or length cannot fix this. The aggregate numbers have to be rebuilt from the authors' real extraction data, and the study-level claims have to be corrected against the sources.

---

## 1. What I need from you (blocking)

| # | Item | Why it blocks |
|---|------|---------------|
| 1 | **The real extraction register** for the 71 included studies (the spreadsheet or Zotero/Rayyan/Covidence export used for screening and extraction), with full citation, modality, N, population, task, vocabulary, architecture, LM use, metric/value, generalization type, code/data availability, quality score. | Every aggregate in the abstract, Results and tables (32/20/14/5 modality split; 14/71 LM use; 40/18/13 generalization split; 94% English; 3/71 data release; 45/23/3 quality) must be recomputed from it. Supplementary Table S1 cannot be used (Section 3). |
| 2 | **Screening log / PRISMA counts** per database (PubMed, Scopus, IEEE Xplore, Web of Science, arXiv), plus citation-chaining counts. | The PRISMA diagram's arithmetic does not close (Section 4). |
| 3 | **Article type decision**: *Analysis* (recommended) or *Review*. | Sets word limit, abstract, structure, display items and reference cap (Section 2). |
| 4 | **AI-tool use statement.** Springer Nature policy requires any use of LLMs in preparing the manuscript to be documented in the Methods. | Mandatory disclosure; only you can state what was used and how. |
| 5 | **PROSPERO record** CRD420261368521: confirm it is public and matches the reported methods (dates, databases, outcomes). | Editors and reviewers will check it. It could not be opened during this review. |
| 6 | **Code/data availability**: repository URL (for example, OSF, Zenodo or GitHub with DOI) for the register and analysis scripts. | NMI requires Data and Code Availability statements. "[GitHub repository URL to be provided]" and "available upon request" will not pass. |

---

## 2. Fit with NMI requirements

Source: nature.com/natmachintell/content and /submission-guidelines/aip-and-formatting (fetched 30 Sep 2026). NMI does not accept presubmission enquiries.

| Requirement | *Analysis* | *Review* | Current manuscript |
|---|---|---|---|
| Main text | ≤3,500 words | 3,000–4,000 words | **~15,000 words** (about 4× over) |
| Abstract | 100–150 words, unreferenced | (standfirst) | **~270 words** |
| Structure | Intro (no heading), Results, Discussion (no subheadings), Methods | free | Numbered sections 1–8, Methods as Section 2, subsections throughout |
| Display items | ≤6 figures/tables (Extended Data ≤10) | illustrations encouraged | **7 figures + 7 tables** |
| References | ~50 recommended | ≤100 | 88 cited |
| Original data allowed | yes | **no** (non-primary; not open-access eligible) | new extracted data, kappa, quality scores |
| Reference style | Nature numeric, titles included | same | IEEEtran |
| Final LaTeX | single .tex, article.cls, .bbl pasted in, no custom macros, compiles with no warnings | same | multi-file, custom colours/macros, 27 overfull-box warnings |

**Recommendation: submit as an *Analysis*.** The paper produces new data (screening, extraction and quality scores across 71 studies), which the *Review* type does not allow. NMI has published PRISMA systematic reviews as Analyses (for example, Roberts et al., *Nat. Mach. Intell.* 3, 199–217 (2021)). This means cutting to ~3,500 words, restructuring into Introduction/Results/Discussion/Methods, and moving the detail to Extended Data and Supplementary Information.

---

## 3. Data integrity: Supplementary Table S1

S1 is presented as the register of the 71 included studies. The reference checks show that it is not a real register:

- **Rows the verification could not match to any paper:** Defossez 2022/2024/2025, d'Ascoli 2023/2024, Huth 2020/2022, Anumanchipalli 2020, Degenhart 2022, Nieto 2023, Kwon 2023, Lotte 2015, Li 2025, and the WER-reporting Angrick sEEG rows (2023/2024/2025).
- **Rows not individually verified but implausible on their face:** Musk et al. 2016/2023/2024 (intracortical speech decoding), Akbari 2017/2021/2023/2024, Singer 2022, Karpul 2023, Coogan 2015, Schalk 2016, Singh 2023 (intracortical), Metzger 2025 (intracortical). The remaining rows also need checking against the real register.
- **Studies that violate the review's own eligibility criteria**: Degenhart 2020 (two monkeys, cursor control), Naselaris 2015 (visual reconstruction), Panachakel 2021 and López-Bernal 2022 (reviews; main.tex itself says these were excluded), Nieto 2022 (dataset paper, no decoding result), Huth 2016 (encoding, not decoding), Peterson 2021 (arm movement, not speech).
- **Real studies with wrong fields**, for example: Metzger 2023 given as intracortical/Transformer/4.2% WER (actually ECoG, bidirectional GRU + CTC, 25.5% median WER, 1,024 words). Moses 2021 given as intracortical (actually ECoG). Makin 2020 given as N=1 (actually 4). Willett 2023 given as Transformer (actually GRU). Ye 2025 given as intracortical, attempted speech, 8.1% WER, long-term (actually fMRI perception, 41 healthy participants, WER 0.76–0.92, no longitudinal analysis).

S1 has to be discarded and rebuilt from the real register (item 1). Without a real register, the review cannot be submitted.

## 4. Internal inconsistencies

| Quantity | Conflicting values |
|---|---|
| Modality split | Text: invasive 32 / EEG 20 / MEG+fMRI 14 / hybrid 5. Table 1: intracortical 10, ECoG 18, sEEG 4, MEG 8, fMRI 6, EEG+fNIRS 2, sEMG 3. Fig. 5 heatmap: ECoG 22, intracortical 8, sEEG 4, MEG 5, fMRI 6, hybrid/sEMG 6. Fig. 2: five groups including "foundation models" (2), MEG/fMRI = 11, hybrid = 6. |
| Invasive single-participant studies | "27 of 32 use n=1", but the listed multi-participant invasive studies alone (Herff 7, Ramsey 5, Chen 48, Singh 25, de Borman 16, Makin 4, Anumanchipalli 5) exceed 5. |
| Cross-session evidence | "exactly 1 study" (Sec. 6.1), "only 2 studies" (Sec. 6.3, Sec. 7), "18 studies" (Table 4). The single cited study (Ye 2025) has no cross-session analysis. |
| Foundation-model studies | "only 2 studies" but 4 cited, one a survey (Zhou 2025). |
| Card 2024 vocabulary | 125,000 words (text) vs 30 words (Appendix table). |
| Study period | Fig. 2 caption "2015-2025", figure shows 2026. |
| "Five modality groups" | Four are named in the Introduction. |
| Headline "2.5% WER and 78 WPM" | Two different studies (Card 2024: 2.5% WER at ~32 WPM; Metzger 2023: 78 WPM at 25% WER). They are presented together as a single achievement. |
| Hard-coded reference numbers in tables ("[2]", "[72]" ...) | Do not match the compiled bibliography; most point to the wrong paper. |

**PRISMA flow diagram (Fig. 1):**
- The per-database counts sum to 3,450, not 4,250 (Web of Science and arXiv missing).
- The title/abstract exclusion reasons sum to 3,612, not the stated 3,617, and 3,847 − 3,617 = 230, not 235.
- The full-text exclusion reasons sum to 156, not 164.
- The "other methods" column for citation chaining is missing (PRISMA 2020 requires it), as are the "reports sought / not retrieved" boxes.
- The round database counts (1,200 / 1,500 / 750) look like estimates, not exported counts.
- "Non-English publication (n = 32)" excluded at full text conflicts with an English-language filter applied at search.

## 5. Study-level claims that contradict their sources

Selected from the verification reports; the full list with source quotations is in `review/reference_checks/`.

**Headline results (abstract, introduction, conclusions)**
- **Herff 2015** 25% WER used a 10-word dictionary, not 50 words. The "10-fold improvement on comparable vocabularies" (Herff → Card) is therefore invalid.
- **Card 2024:** 2.5% WER on a 125,000-word vocabulary, ~32 WPM, 8.4 months. The 30-minute calibration was on day 1 only, not daily.
- **"LM rescoring gives 10–14 (or 10–20) pp WER reduction"** is attributed to Willett 2023, which reports no such ablation. Its improved LM reduced WER from 23.8% to 17.4%. Kaplan 2020 (text-only scaling laws) is also cited for this and says nothing about WER.
- **"Open-vocabulary EEG reaches 35–45% WER"** has no source. Wang & Ji 2022 and DeWave report only BLEU/ROUGE. Jo et al. 2024 (arXiv:2405.06459) re-evaluated Wang & Ji: WER 78% with teacher forcing, 108% without, and similar on pure-noise input. This claim, and every comparison built on it ("3–5× gap", Table 1 EEG row, Discussion), must be removed or rebuilt.

**Section 3 (modalities)**
- **Moses 2021:** ECoG, not intracortical.
- **Chartier 2018:** no r = 0.87; the neural encoding correlation is mean r ≈ 0.25.
- **Ramsey 2018:** grids at 3–4 mm pitch, not 256 channels at 1 mm.
- **Chen 2024:** PCC 0.806 (not 0.804), and models were trained per participant (not cross-subject).
- **Degenhart 2020:** 2 monkeys, cursor control, ≤5 days; not speech, not 6 months.
- **Wandelt 2024:** the participants could speak.
- **Angrick 2021:** linear model + Griffin–Lim, 1 participant.
- **Saha 2019:** 14 participants, 53.4% (11-class).
- **Zhu 2021:** 86% English / 94% Chinese.
- **Hons 2026:** EEG+fNIRS did *not* differ from EEG alone.
- **Duraivel 2023:** controls were 11 different patients, not "the same four".
- **Huth 2016:** an encoding study.
- **Hickok 2007:** phonological working memory is dorsal-stream.
- **Poeppel 2020:** not the source of the dual-stream model.

**Section 4 (architectures)**
- **Hochreiter 1997** did not introduce the forget gate (Gers et al. 2000).
- **BENDR "5–15% improvement"** is not in Kostas 2021, which has no speech task.
- **Kaplan 2020** is misused (see above).
- **Architecture counts** ("approximately 8/13/10/7/10/8/14/2") cannot be verified without the register.

**Section 5 (benchmarks)**
- **Tang 2023** is fMRI (not MEG) and is wrongly given "41% top-1" (Défossez's number) and ">50% text recovery".
- **"MEG 15% WER"** has no source.
- **Makin 2020:** 4 participants, overt speech, with cross-participant transfer.
- **ArchitectureComparison2020** (actually Sak et al. 2014, acoustic ASR) is cited for "LSTM/Seq2Seq outperform traditional ML by 15–25 pp in brain decoding".
- **Cost figures** ($5k–50k EEG, $1–5M MEG, $2–3M fMRI) are attributed to Vansteensel 2023, which contains none of them.
- **Willett 2024 Benchmark:** the BibTeX entry is a placeholder (bad DOI). The real paper (arXiv:2412.17227) describes a public leaderboard, which contradicts "no public leaderboard".
- **Borrowed ASR details:** "SRUS", "Milvus for vector search" and "OpenSeq2Seq" are either not real ASR benchmark initiatives or are irrelevant.

**Section 6 (generalization): most of this section must be rewritten**
- **Peterson 2021:** HTNet, arm-movement decoding in 12 ECoG + 15 EEG participants. There is no speech and no manifold alignment or autoencoders. The vowel/consonant/125K results, 60–80% retention and 5–15 pp inflation are not in the paper.
- **Singh 2025:** a single site (UTHealth Houston), 25 epilepsy patients, phoneme error rate 57% → 49%. The "UCSF/Stanford/MGH", "18 participants from two sites" and "50–75%" details are not in the paper.
- **de Borman 2024:** 16 ECoG patients (not 8), with transfer between speech *modes* (performed/perceived/imagined), not between recording modalities. The "70%" and "85–90% retention" figures are absent.
- **Ye 2025:** fMRI, no longitudinal analysis. The ">80% retention over 4 weeks" is not in the paper.
- **d'Ascoli 2025:** no cross-language transfer test. Top-1 is 20% at 50 words, not ">40%". It pools 9 datasets and studies perception, not motor production.
- **Li 2022:** 6 Mandarin speakers, standard sEMG, CER 6.41%. The Mandarin→English "80% transfer" is not in the paper.
- **Cross-modal studies:** Ma 2023 (monkeys), Zhang 2026 (intracortical cross-session) and Levin 2026 (intracortical cross-subject) are not cross-modal. Yang 2026 reports *successful* EEG→ECoG transfer, which contradicts "cross-modal transfer remains unachieved".
- **Unsupported mechanisms:** "10–30% per month degradation", the "weeks 1–3 / week 6 / 200 µm glial capsule" timeline, and the "Mandarin 21 consonants, 5 vowels = 22 units" figure are not supported by their sources.
- **Omitted evidence:** Card 2024 (8.4 months) and Moses 2021 (81 weeks) provide long-term human evidence that the section overlooks.

**Section 7 (discussion)**
- **Uncited or unsupported specifics** include:
  - costs ($3–5M, $500K–1M, $2–3M);
  - named "candidate lead institutions" (e.g. "Max Planck Institute for Empirical Aesthetics", "MIT Media Lab");
  - the regulatory timelines and device examples (e.g. "Clarion system");
  - "one study demonstrated 72% → 91% with 5 minutes of fine-tuning";
  - "500–2000 participants" as a ceiling.
- **Institutional prescriptions:** telling named journals and funders what to require (including NMI itself) is not appropriate in the manuscript.
- **Misused citations:** BrainBERT is cited for "direct application underperforms custom models", but that paper shows the opposite. Zhou 2025 is a survey.

**Methods (main.tex)**
- **Sterne 2019** (RoB 2, for randomised trials) is cited for "criteria for evaluating AI-based biomedical studies". PROBAST/PROBAST+AI or QUADAS-AI would be appropriate if used.
- **Tricco 2018** is PRISMA-ScR (scoping reviews), not PRISMA-P.
- **κ = 0.85 described as "substantial"** needs Landis & Koch 1977, and by that scale 0.85 is "almost perfect".
- **"Registered prior to formal screening" / "no deviations"** conflicts with the Limitations section, which reports late registration after scoping.
- **Extraction method:** "single extraction with 10% spot-check" (Limitations) conflicts with "dual-reviewer" framing elsewhere and with the author contributions.

## 6. Reference list

- 88 entries are cited; all but one correspond to real publications (Willett2024Benchmark is a placeholder).
- **Wrong authors/venue/year:** Mandarin2020 (Fon 2020), IntracorticalRecording2017 (Szostak et al.; uncited), Liu2026CrossBrain (first author Levin; bad DOI), Song2023Silent (first author Chen), Logothetis2010 (2004 paper; co-author B. A. Wandell), Schirrmeister2017 (author list), GlialScar2014 (Cogan 2008).
- **Superseded arXiv versions:** Vaswani, Sutskever, Chen 2020, BrainBERT, Common Voice, Yin 2025, Zhang 2025 should cite the proceedings versions.
- **Missing volumes/pages:** Page2021 (372), Sterne2019 (366), Buxton (S220–S233).
- **Uncited in text:** PROSPERO (the registration should be cited).
- **Style:** convert to Nature style (numbered, titles included, journal abbreviations) and paste the .bbl into the .tex for final submission.

## 7. Language and style

- **Promotional or loaded wording** throughout: "landmark", "undeniable", "extraordinary", "heroic", "catastrophically poor", "the defining open question", "unacceptable", "urgently needs", "the intellectual core is solid", "infrastructure will". NMI copy-editors remove such language, and reviewers read it as advocacy.
- **Buzzwords and jargon:** "AI revolution", "foundation model trajectory", "highest-leverage technical lever", "Brain LLM Hub", "one-line integration", "efficiency loss", "clinical business models", "market".
- **Speculation stated as fact**, e.g. "closed-set classification is a solved problem", "fundamental limits ... cannot be overcome by architectural innovation", "truly modality-invariant features may not exist", "all motor cortices implement similar intention-detection circuits".
- **Repetition:** the same paragraph appears twice in Sec. 6.1 ("highest-priority bottleneck").
- **Structure:** bulleted "Recommendation:" blocks, numbered priority lists, and a regulatory primer read as a white paper, not a research analysis.
- **Inconsistent spelling:** British/American mixed ("whilst", "haemodynamic" vs "generalization", "modeling").
- **Unnecessary equations:** WER, LSTM gates, attention, NT-Xent and log-linear LM fusion are textbook material and add length without evidence.

## 8. Plan once items 1–6 arrive

1. Rebuild the register as a CSV (Supplementary Data 1) and generate every count, percentage, figure and table from it with a script, so numbers cannot drift again.
2. Redraw the PRISMA 2020 diagram from the screening log (both columns).
3. Rewrite as an NMI *Analysis*, about 3,500 words:
   - Introduction (no heading).
   - Results: study landscape; recording modality and task; decoder design and language-model use; comparability of reported benchmarks; generalization evidence; reporting quality and risk of bias.
   - Discussion (no subheadings, including limitations).
   - Methods: protocol and registration; eligibility; search; selection; extraction; quality assessment; synthesis; use of AI tools.
   - Data availability, Code availability, Author contributions, Competing interests.
4. Six display items:
   - Fig. 1: PRISMA flow.
   - Fig. 2: studies by year and modality.
   - Fig. 3: best reported result by modality and task, with vocabulary size shown.
   - Fig. 4: generalization evidence.
   - Table 1: modality characteristics.
   - Table 2: landmark studies with full context (N, population, task, vocabulary, metric, LM, evaluation).
   - The remaining items go to Extended Data or Supplementary Information.
5. Correct every study-level claim against the verification reports. Remove claims that no source supports.
6. Convert references to Nature style, keep ≤ ~60 in the main list, and cite included studies not discussed in the text in Supplementary Table 1.
7. Produce the final single-file .tex (article.cls, .bbl inlined) that compiles with no warnings, plus a cover letter.
