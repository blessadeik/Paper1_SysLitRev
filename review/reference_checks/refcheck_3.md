# Reference check, group 3

Sources: Crossref API, Europe PMC abstracts, and PMC, arXiv and ISCA full texts. Paths are relative to `overleaf/`. S1 = `supplementary/supplement_table_s1.tex`.

## Summary of serious problems
1. **"35-45% WER" for open-vocabulary EEG** (sec3:55, sec3:97, sec5:27, sec5:29, appendices:106/113, figures_and_tables:112) has no support in any source checked:
   - Wang & Ji 2022 and DeWave report only BLEU/ROUGE. The DeWave text contains no WER.
   - Jo et al. 2024 re-ran Wang & Ji's BART model. They got **WER 75.3-78.1% with teacher forcing** and **99.7-110.98% without it**. Performance on pure-noise input was the same.
   - S1 row 37 ("Duan 2023, n=15, WER 38%") is fabricated.
2. **Singh2025 multi-site story is fabricated** (sec6:16, sec6:28, appendices:134):
   - The study was at one site only (UTHealth Houston). There was no UCSF/Stanford/MGH, no "18 participants from two sites" and no "50-75%".
3. **d'Ascoli2025 cross-language transfer claims are fabricated** (sec6:50, 52, 54, 56; appendices:153):
   - The paper runs no cross-language transfer test.
   - The paper studies perception (reading/listening), not motor production.
   - It used MEG+EEG, not EEG only.
   - There is no ">40% word accuracy". The paper reports top-1 = 20% at a 50-word vocabulary.
4. **Li2022 Mandarin-to-English transfer ("80%") is fabricated** (sec6:52, 56; appendices:155).
   - The study covers six Mandarin speakers only and reports CER 6.41%.
   - It is not HD-sEMG (it used standard wet Ag/AgCl electrodes).
5. **Tang2023 is called MEG** (sec5:37). Also on that line:
   - "41% top-1" is misattributed to Tang (it is Défossez's number).
   - ">50% text recovery" is unsupported (Tang's WER is 0.92-0.94).
6. **Wrong numbers:**
   - Saha2019: real values are 14 participants, 53.36% (11-class) and 83.42% (binary). The manuscript says 70-75% and 10 participants.
   - Zhu2021: real values are 86% English and 94% Chinese with 10 optimal electrodes. The manuscript says 87-90%.
   - Kwon2024 in S1: real values are n=4 healthy participants and a PCC metric. S1 says n=12 and "Acc 58%".
7. **Hons2026 misrepresented:** the paper found that the hybrid EEG+fNIRS result did not differ significantly from EEG alone. The manuscript says it confirms complementarity.
8. **Song2023Silent:** the first author is Chen, X., not "Song".
9. **Poeppel2020 misattributed** to the dual-stream model. It is a review of speech rhythms.
10. **Huth2016** is an encoding/mapping study with 7 subjects. S1 row 27 lists it as a decoding study with 8 subjects and "Corr 0.72".

---

## Singh2025
- **Exists:** yes. Singh, A., Thomas, T., Li, J., Hickok, G., Pitkow, X. & Tandon, N. Transfer learning via distributed brain recordings enables reliable speech decoding. *Nat. Commun.* **16**, 8749 (2025). DOI: 10.1038/s41467-025-63825-0 (PMC12488916).
- **Bib entry errors:** none.
- **Study facts:**
  - Modality: sEEG (3,641 depth electrodes) at a single site (UTHealth Houston).
  - Participants: 25 patients with intractable epilepsy.
  - Task: overt tongue-twister production. Vocabulary: 128 stimuli with 218 unique words.
  - Headline metrics:
    - "median PER of 27% ... articulatory periods, and 34% ... pre-articulatory"
    - variable-length sequences: "44% PER"
    - group transfer: "PER from 57% in the within-subject model to 49%"
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:43 "25 participants": CORRECT.
  - sec3:43 "group decoder ... outperforms any individual participant decoder": OVERSTATED. The source says "The group-derived decoder significantly outperformed models trained on individual data alone."
  - sec3:43 "largest sEEG speech decoding cohort reported": UNSUPPORTED superlative. The paper says "a large cohort".
  - sec6:16 "domain adaptation ... eliminate ... electrode noise, impedance, individual alpha frequency": UNSUPPORTED. The method is transfer learning with shared latent manifolds.
  - sec6:16 "25 participants at multiple clinical sites achieved 50-75% of single-site performance": WRONG. There was one site and no such figure.
  - sec6:28 "three different clinical sites (UCSF, Stanford, MGH) ... harmonization ... trained on 18 participants from two sites achieved 50-75%": WRONG / FABRICATED. None of this appears in the paper.
  - sec5:19 "Singh n=25": CORRECT. "Transfer learning retains 50-80%" (for this study): UNSUPPORTED.
  - appendices:134 "50-75% vs individual; Cross-site harmonization": WRONG.
  - S1 row 17 "Phoneme class, Acc 62.5%": UNSUPPORTED. The paper reports PER. S1 row 55 ("Singh et al. 2023, intracortical, WER 8.9") could not be matched.

## Lotte2018
- **Exists:** yes. Lotte, F., Bougrain, L., Cichocki, A., Clerc, M., Congedo, M., Rakotomamonjy, A. & Yger, F. A review of classification algorithms for EEG-based brain-computer interfaces: a 10 year update. *J. Neural Eng.* **15**, 031005 (2018). DOI: 10.1088/1741-2552/aab2f2.
- **Bib entry errors:** "and others" should give the full author list (7 authors).
- **Study facts:** review of EEG-BCI classifiers from 2007-2017, not specific to speech. Primary empirical study: no.
- **Claims checked:**
  - sec4:13 (handcrafted features fed to SVM/LDA/HMM, citing Lotte2018): CORRECT in general (the review covers LDA, SVM and similar classifiers). The review is about motor-imagery/P300 BCIs, not speech.
  - appendices:31 "Quality assessment tool (7-item checklist adapted from Lotte et al.)": UNSUPPORTED. Lotte 2018 contains no quality checklist.
  - appendices:54 and S1 row 2 "Lotte et al. 2015, EEG, n=3, imagined speech, 85%": no such Lotte 2015 imagined-speech study could be matched. This is a possibly fabricated included study.

## Saha2019
- **Exists:** yes. Saha, P., Abdul-Mageed, M. & Fels, S. SPEAK YOUR MIND! Towards imagined speech recognition with hierarchical deep learning. In *Proc. Interspeech 2019* 141-145 (ISCA, 2019). DOI: 10.21437/Interspeech.2019-3041.
- **Bib entry errors:** none.
- **Study facts:**
  - Modality: EEG, using the KARA ONE dataset.
  - Participants: "14 participants" (healthy).
  - Task: imagined speech, 11 tokens (7 phonemes/syllables and 4 words).
  - Headline metrics: "average accuracy of 83.42% across the six different binary phonological classification tasks, and 53.36% for the individual token identification task".
  - Main results use a random 80/10/10 split pooled across subjects. Leave-one-subject-out results are also given.
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:53 "approximately 70-75 percent accuracy across ten participants": WRONG. The source gives 14 participants and 83.42% (binary) / 53.36% (11-class).
  - "subject-independent": PARTLY. It is the stated aim, but the headline numbers come from pooled random splits.

## Agarwal2022
- **Exists:** yes. Agarwal, P. & Kumar, S. Electroencephalography-based imagined speech recognition using deep long short-term memory network. *ETRI J.* **44**, 672-685 (2022). DOI: 10.4218/etrij.2021-0118.
- **Bib entry errors:** none significant.
- **Study facts:** 32-channel EEG; 13 subjects; imagined speech of 4 words and 1 phrase (5 classes); "maximum accuracy of 73.56%"; subject-independent. Primary empirical study: yes.
- **Claims checked:**
  - sec3:53 "73.56 percent, five-class, subject-independent LSTM, 13 participants": CORRECT.

## Wang2022
- **Exists:** yes. Wang, Z. & Ji, H. Open vocabulary electroencephalography-to-text decoding and zero-shot sentiment classification. *Proc. AAAI Conf. Artif. Intell.* **36**, 5350-5358 (2022). DOI: 10.1609/aaai.v36i5.20472.
- **Bib entry errors:** issue (5) is missing. Otherwise correct.
- **Study facts:**
  - Modality: EEG, using ZuCo 1.0/2.0 (healthy readers).
  - Task: natural reading, open vocabulary.
  - Model: BART.
  - Headline metrics: "40.1% BLEU-1 score on EEG-To-Text decoding and a 55.6% F1 score on zero-shot ... sentiment classification". No WER is reported.
  - Primary empirical study: yes (method).
- **Claims checked:**
  - sec3:55 "first open-vocabulary EEG-to-text system using BART": CORRECT.
  - sec3:55 "above-chance sentence reconstruction": UNSUPPORTED/CONTESTED. The paper has no chance or noise baseline. Jo et al. 2024 show that teacher-forced evaluation inflated the results and that noise input performs the same.
  - sec5:29 and "35-45% WER": WRONG. See the Summary and Duan2023.
  - sec4:57 (EEG-to-text as evidence of transformer "scalability"): weak.
- **Critique to cite:** Jo, H., Yang, Y., Han, J., Duan, Y., Xiong, H. & Lee, W. H. Are EEG-to-text models working? Preprint at https://arxiv.org/abs/2405.06459 (2024).
  - Their Table 2 (BART with teacher forcing, EEG to EEG): BLEU-1 39.31, WER 78.08%.
  - Same model with random noise input: WER 78.09%.
  - Without teacher forcing: WER 108.43%.
  - Their conclusion: "model performance on noise data can be comparable to that on EEG data."

## Duan2023
- **Exists:** yes. It was published at NeurIPS under a changed title. Duan, Y., Zhou, J., Wang, Z., Wang, Y.-K. & Lin, C.-T. DeWave: discrete encoding of EEG waves for EEG to text translation. In *Adv. Neural Inf. Process. Syst.* **36**, 9907-9918 (2023). DOI: 10.52202/075280-0432. The arXiv version is 10.48550/arXiv.2309.14030.
- **Bib entry errors:** should cite the NeurIPS version. Give the full author list instead of "others". The title differs from the NeurIPS version.
- **Study facts:**
  - Modality: EEG, using ZuCo (healthy readers).
  - Task: reading, open vocabulary.
  - Headline metrics: "41.35 BLEU-1 and 33.71 Rouge-F" (with markers); "20.5 BLEU-1 and 29.5 Rouge-1" without markers. No WER.
  - The authors state: "this paper uses a teacher-forcing setting in evaluation."
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:55 "no explicit time-marker alignment ... improved BLEU and ROUGE": CORRECT. Caveats: the marker-free BLEU-1 is much lower (20.5), and evaluation used teacher forcing.
  - sec3:55, sec5:29 "WER approximately 35-45%": WRONG / UNSUPPORTED.
  - S1 row 37 "n=15, WER 38.0%": WRONG. There is no WER, and ZuCo is not n=15.

## Defossez2023
- **Exists:** yes. Défossez, A., Caucheteux, C., Rapin, J., Kabeli, O. & King, J.-R. Decoding speech perception from non-invasive brain recordings. *Nat. Mach. Intell.* **5**, 1097-1107 (2023). DOI: 10.1038/s42256-023-00714-5.
- **Bib entry errors:** none.
- **Study facts:**
  - Modality: MEG and EEG; 175 healthy volunteers; 4 public datasets.
  - Task: perceived speech (listening).
  - Metric: segment identification among more than 1,000 candidates.
  - Abstract: "up to 41% accuracy out of more than 1,000 distinct possibilities on average across participants, and with up to 80% in the best participants".
  - arXiv full text: "top-1 accuracy up to 41.3%". This is MEG (Gwilliams dataset); EEG results are much lower.
  - Method: contrastive learning onto self-supervised wav2vec 2.0 speech representations.
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:63 "175 participants, four public datasets, 41% top-1, perceived speech segment": CORRECT. Note that 41% is MEG only and is the best dataset.
  - sec4:65 "extended [SSL] to MEG and EEG across 175 participants achieving top-1 41%": CORRECT with the same caveat. The model is contrastive and uses SSL speech targets; it is not SSL pretraining on the brain data.
  - S1 row 25 "MEG, 175": PARTLY. It is MEG+EEG.
  - S1 rows 48, 66 and 71 ("Defossez 2022 MEG n=50 38%", "Defossez 2024 MEG n=40 48%", "Defossez 2025 MEG n=60 52%") could not be matched to any paper. They may be fabricated or duplicate entries.

## Kwon2024
- **Exists:** yes. Kwon, J., Harwath, D., Dash, D., Ferrari, P. & Wang, J. Direct speech synthesis from non-invasive, neuromagnetic signals. In *Proc. Interspeech 2024* 412-416 (ISCA, 2024). DOI: 10.21437/Interspeech.2024-2153.
- **Bib entry errors:** none.
- **Study facts:**
  - Modality: MEG (306-channel; gradiometers used).
  - Participants: "Four right-handed healthy individuals".
  - Task: overt production of 5 AAC phrases.
  - Model: Squeezeformer plus Bi-LSTM Mel generator, then BigVGAN vocoder.
  - Headline metric: "average correlation coefficient of 0.95"; "grand average across all participants was 0.954 ± 0.014".
  - Uses 5-fold cross-validation within participants. No formal intelligibility test.
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:63 "first intelligible speech synthesis from MEG, transformer + BigVGAN, PCC ≈ 0.95": CORRECT (the "first" is the authors' own claim). Add that the vocabulary is 5 phrases, n=4 and the task is overt.
  - S1 row 26 "n=12, Speech class, Acc 58.0%": WRONG. The study has n=4 and reports Mel-spectrogram PCC 0.95.
  - S1 row 54 "Kwon et al. 2023 EEG n=9 WER 41%": could not be matched.

## dAscoli2025
- **Exists:** yes. d'Ascoli, S., Bel, C., Rapin, J., Banville, H., Benchetrit, Y., Pallier, C. & King, J.-R. Towards decoding individual words from non-invasive brain recordings. *Nat. Commun.* **16**, 10521 (2025). DOI: 10.1038/s41467-025-65499-0 (PMC12658044).
- **Bib entry errors:** give the full author list (7 authors).
- **Study facts:**
  - Modality: EEG and MEG.
  - Participants: "723 participants reading or listening to five million words in three languages" (Dutch, English, French).
  - Data: "seven public datasets and two datasets which we collect ourselves".
  - Metric: top-10 accuracy at a 250-word vocabulary.
  - "given a vocabulary of 50 words, we reach a top-1 decoding accuracy of 20%".
  - "the present study focuses on language perception and not on language production".
  - "MEG and reading are easier to decode than EEG and listening". Performance increases with the amount of data.
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:63 "723 participants, English/French/Dutch, performance scales with data": CORRECT.
  - sec3:63 "seven datasets": WRONG. The source gives 9 (7 public + 2 new).
  - sec3:63 "MEG word decoding": PARTLY. The study covers both EEG and MEG.
  - sec4:57 "CNN-transformer achieved top 1 accuracy across 723 participants": VAGUE/MISLEADING. The main metric is top-10, and top-1 is 20% at 50 words.
  - sec6:50 ">40% word-level accuracy ... partial cross-language transfer ... language-invariant motor-phonetic mappings": WRONG / UNSUPPORTED. There is no cross-language transfer experiment ("a single model across languages" is used only for the embeddings). The study concerns perception, not motor mappings.
  - sec6:52, 54, 56 "40% transfer on cortical EEG": WRONG.
  - appendices:153: WRONG for the same reason.
  - sec5:66 "n=723 (large EEG consortia)": PARTLY. It is a pool of public EEG and MEG datasets.
  - S1 row 24 "EEG, continuous speech, Acc 45%, cross-lang": WRONG.
  - S1 rows 41 ("d'Ascoli 2024 EEG 200, 42%") and 61 ("d'Ascoli 2023 MEG 35, r=0.71") could not be matched. They may be preprint duplicates or fabricated.

## Poeppel2020
- **Exists:** yes. Poeppel, D. & Assaneo, M. F. Speech rhythms and their neural foundations. *Nat. Rev. Neurosci.* **21**, 322-334 (2020). DOI: 10.1038/s41583-020-0304-4.
- **Bib entry errors:** none.
- **Study facts:** review of 2-8 Hz speech rhythms and audio-motor interaction. Primary empirical study: no.
- **Claims checked:**
  - sec3:11 "The dual-stream model \cite{Hickok2007,Poeppel2020}": UNSUPPORTED for Poeppel2020. The dual-stream model comes from Hickok & Poeppel (2004, 2007). Remove Poeppel2020 or replace it with Hickok, G. & Poeppel, D. Dorsal and ventral streams. *Cognition* **92**, 67-99 (2004).
  - The sentence also says the ventral stream goes "to the frontal lobe via the temporal lobe" and supports "phonological working memory". Both are inaccurate descriptions of the model.

## Tang2023Semantic
- **Exists:** yes. Tang, J., LeBel, A., Jain, S. & Huth, A. G. Semantic reconstruction of continuous language from non-invasive brain recordings. *Nat. Neurosci.* **26**, 858-866 (2023). DOI: 10.1038/s41593-023-01304-9.
- **Bib entry errors:** none.
- **Study facts:**
  - Modality: fMRI.
  - Participants: 3 healthy subjects (S1-S3) in the main decoding; up to 7 in the cross-subject control.
  - Tasks: perceived speech, imagined speech and silent video.
  - Model: GPT-1 language model with an encoding model and beam search.
  - Perceived-speech WER 0.92-0.94; BLEU-1 about 0.23-0.25.
  - Story identification: "we correctly identified the story that the subject was imagining ... (100% identification accuracy)". This was imagined speech, with 5 one-minute candidate stories.
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:71 "fMRI, GPT-based, 100% story identification": CORRECT. Add the context: imagined speech, 5 candidate stories.
  - sec4:73 (align encoder representations directly with LLM latent spaces): LOOSE. It uses an LM prior with an encoding model, not latent alignment.
  - sec5:37 "Representative MEG studies achieve 15% WER ... and 41% top-1 accuracy on semantic reconstruction \cite{Tang2023Semantic}": WRONG. Tang is fMRI, it has no 15% WER (WER ≈ 0.93), and it has no 41% top-1 (that is Défossez).
  - sec5:37 "Two landmark MEG studies ... 100% story identification and >50% text recovery": WRONG modality (fMRI). ">50% text recovery" is UNSUPPORTED. The paper instead says "72-82%" of time-points were significantly decoded, which is a different measure.
  - appendices:108 (MEG row "100% story ID; >50% text recovery", refs [48],[49]): WRONG modality. The rows cited (Defossez 2022, Huth 2020) are not the source of this number.

## Huth2016
- **Exists:** yes. Huth, A. G., de Heer, W. A., Griffiths, T. L., Theunissen, F. E. & Gallant, J. L. Natural speech reveals the semantic maps that tile human cerebral cortex. *Nature* **532**, 453-458 (2016). DOI: 10.1038/nature17637.
- **Bib entry errors:**
  - "W. A. De Heer" should be de Heer.
  - "F. Theunissen" should be F. E. Theunissen.
  - "J. Gallant" should be J. L. Gallant.
- **Study facts:** fMRI voxel-wise encoding (semantic atlas). "Seven subjects listened to more than two hours of stories". Not a decoding study. Primary empirical study: yes, but not brain-to-speech decoding.
- **Claims checked:**
  - sec3:71 "semantic maps revealed by fMRI": CORRECT.
  - S1 row 27 "fMRI, n=8, Semantic recon., Corr 0.72, cross-part": WRONG. The study has n=7 and does no reconstruction or decoding, so it should not be an included decoding study.
  - appendices:138 lists it among the included studies: questionable.
  - S1 rows 49/64 ("Huth et al. 2020", "Huth 2022") could not be matched.

## Tang2025Semantic
- **Exists:** yes. Tang, J. & Huth, A. G. Semantic language decoding across participants and stimulus modalities. *Curr. Biol.* **35**, 1023-1032.e6 (2025). DOI: 10.1016/j.cub.2025.01.024.
- **Bib entry errors:** the page range should end with ".e6".
- **Study facts:**
  - Modality: fMRI.
  - Participants: n=3 goal participants, with separate reference participants.
  - Method: decoders trained on reference participants and transferred through functional alignment using story or movie data.
  - Finding: "Cross-participant decoder predictions were semantically related to the stimulus words, even when functional alignment was performed using movies with no linguistic content".
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:73 "cross-participant decoding across story- and movie-based stimuli": CORRECT. More precisely, the movies were used for functional alignment; the decoded target is still language.
  - sec5:39 "fMRI is fundamentally restricted to semantic-level decoding": UNSUPPORTED as an attribution. The paper does not claim this; at most it is an inference.

## Cooney2022
- **Exists:** yes. Cooney, C., Folli, R. & Coyle, D. A bimodal deep learning architecture for EEG-fNIRS decoding of overt and imagined speech. *IEEE Trans. Biomed. Eng.* **69**, 1983-1994 (2022). DOI: 10.1109/TBME.2021.3132861.
- **Bib entry errors:** none.
- **Study facts:**
  - Modality: EEG+fNIRS; 19 healthy participants.
  - Task: overt and imagined speech, 4 classes (chance 25%).
  - Headline metrics: "46.31% and 34.29% for overt and imagined speech"; "significant improvement on EEG ... for imagined speech (p = 0.020) while tending towards significance for overt speech (p = 0.098)".
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:81 "bimodal CNN outperforms unimodal EEG for both overt and imagined, 19 participants": PARTLY WRONG. It is significant only for imagined speech; for overt speech it is not significant (p = 0.098). Accuracies were low (34-46%).

## Hons2026
- **Exists:** yes. Hons, M., Kober, S. E., Wriessnegger, S. C. & Wood, G. Hybrid EEG-fNIRS phoneme classification based on imagined and perceived speech. *Front. Neuroergon.* **7**, 1696865 (2026). DOI: 10.3389/fnrgo.2026.1696865.
- **Bib entry errors:** none.
- **Study facts:**
  - Modality: EEG+fNIRS; 22 healthy right-handed participants.
  - Task: 4 phonemes (/a/, /i/, /b/, /k/), imagined and perceived.
  - Classifier: features ranked by mutual information and classified with a conventional classifier, 10-fold cross-validation.
  - Headline metrics: "77.29% and 76.05% regarding imagined and perceived speech".
  - Key finding: "hybrid and EEG-based classification performances did not differ significantly".
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:81 "confirming the complementarity of the combined signal": WRONG. The paper found the hybrid did not beat EEG alone and that the result was "primarily driven by EEG features".

## Song2023Silent
- **Exists:** yes, but the key and the manuscript name the wrong author. Chen, X., Zhang, X., Chen, X. & Chen, X. Decoding silent speech based on high-density surface electromyogram using spatiotemporal neural network. *IEEE Trans. Neural Syst. Rehabil. Eng.* **31**, 2069-2078 (2023). DOI: 10.1109/TNSRE.2023.3266299.
- **Bib entry errors:** authors are correct, but the key "Song2023Silent" is misleading.
- **Study facts:**
  - Modality: HD-sEMG (4 × 64-channel arrays).
  - Participants: 15 subjects.
  - Task: subvocalizing 33 Chinese phrases (82 syllables).
  - Headline metrics: "97.17 ± 1.53%" phrase accuracy and "character error rate (3.11 ± 1.46%)".
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:87 "Song and colleagues": WRONG. It should be "Chen and colleagues".
  - sec3:87 "97.17% phrase accuracy, 3.11% CER, 33 Chinese phrases": CORRECT.
  - sec3:87 "CNN-RNN": the abstract says "spatio-temporal end-to-end neural network". Acceptable, but verify against the full text.

## Zhu2021
- **Exists:** yes. Zhu, M., Zhang, H., Wang, X., Wang, X., Yang, Z., Wang, C., Samuel, O. W., Chen, S. et al. Towards optimizing electrode configurations for silent speech recognition based on high-density surface electromyography. *J. Neural Eng.* **18**, 016005 (2021). DOI: 10.1088/1741-2552/abca14.
- **Bib entry errors:** none significant.
- **Study facts:**
  - Modality: HD-sEMG with 120 electrodes.
  - Task: 10 digits spoken silently in English and in Chinese.
  - Headline metric: "Using only ten optimal electrodes could achieve a classification accuracy of 86% for English and 94% for Chinese".
  - Number of participants: not verified.
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:87 "87-90 percent digit classification accuracy for both English and Chinese using an optimized 120-electrode configuration": WRONG. The source gives 86% (English) and 94% (Chinese) with 10 optimally selected electrodes; 120 is the full grid.

## Li2022
- **Exists:** yes. Li, H., Lin, H., Wang, Y., Wang, H., Zhang, M., Gao, H., Ai, Q., Luo, Z. & Li, G. Sequence-to-sequence voice reconstruction for silent speech in a tonal language. *Brain Sci.* **12**, 818 (2022). DOI: 10.3390/brainsci12070818 (PMC9312762).
- **Bib entry errors:** give the full author list.
- **Study facts:**
  - Modality: multi-channel sEMG "using standard wet surface Ag/AgCl electrodes". It is not described as high-density.
  - Participants: "six Mandarin Chinese speakers".
  - Task: silent speech to voice synthesis (Seq2Seq plus vocoder).
  - Headline metrics: "character error rate (CER) of 6.41%"; tone classification 96.07%.
  - Language: Mandarin only; no English.
  - Primary empirical study: yes.
- **Claims checked:**
  - sec3:87 "extended HD-sEMG to Mandarin tonal speech synthesis using encoder-decoder": PARTLY. Encoder-decoder and Mandarin are correct; "HD-sEMG" is wrong.
  - sec6:52 "trained on Mandarin ... tested on English ... retained 80% of single-language performance": WRONG / FABRICATED. The paper has no English data and no transfer test. It lists transfer learning only as future work.
  - sec6:54 (phoneme-inventory claim, "Mandarin 21 consonants, 5 vowels, 4 tones = 22 units", citing Li2022): WRONG. Li2022 says the number of "tonemes ... is 139 in Mandarin Chinese" and "44" phonemes in English.
  - sec6:56 "80% transfer on sEMG": WRONG.
  - appendices:155: WRONG.
  - S1 row 29 "HD-sEMG, n=6, Phoneme speech, Acc 80%, Cross-lang": n=6 is CORRECT. The rest is WRONG (the metric is CER 6.41% and there is no cross-language test).
  - S1 row 63 "Li et al. 2025 HD-sEMG n=3 82% cross-lang": could not be matched.
