# Reference check - group 5

Sources: Crossref API (DOI resolution), arXiv API, Europe PMC full text (Vansteensel PMC9971103; Ma PMC10446822), ACL Anthology, bioRxiv/Crossref (Levin et al.), ICLR 2026 listing, Springer chapter abstract (Fon 2020).
Note: none of these 18 keys appear in supplementary/supplement_table_s1.tex or as uncited name mentions in figures_and_tables.tex/appendices.tex.

## Hemodynamic2007
- Exists: yes. The key name is generic and misleading: the entry is Buxton et al. 2004, not a 2007 paper. Correct: Buxton, R. B., Uludağ, K., Dubowitz, D. J. & Liu, T. T. Modeling the hemodynamic response to brain activation. *NeuroImage* **23**, S220–S233 (2004). DOI: 10.1016/j.neuroimage.2004.07.013
- Bib entry errors: pages should be S220–S233 (Suppl. 1), not 220–233; "number = {1}" should be Suppl. 1; the diacritic in Uludağ is missing; the key year (2007) does not match the paper (2004).
- Study facts: a review/modelling paper on BOLD/CBF haemodynamics. Not a speech-decoding study.
- Manuscript claims checked:
  - section3_modalities.tex:69 "haemodynamic response peaks approximately 4-5 seconds after the neural event" -> CORRECT in substance. The textbook HRF peaks at about 4–6 s and Buxton models this. I did not extract an exact quote.
  - section5_benchmarks.tex:39 "hemodynamic response ... integrates neural activity over 4-5 seconds post-stimulus" -> CORRECT in substance, same as above.

## IntracorticalRecording2017
- Exists: yes. The DOI resolves to a real paper, but the authors in the bib are WRONG. Correct: Szostak, K. M., Grand, L. & Constandinou, T. G. Neural interfaces for intracortical recording: requirements, fabrication methods, and characteristics. *Front. Neurosci.* **11**, 665 (2017). DOI: 10.3389/fnins.2017.00665
- Bib entry errors: the bib lists "M. D. Serruya and R. A. Gaunt", who are not the authors. These names look fabricated or confused with another paper.
- Study facts: a review of electrode technology. Not an empirical speech study.
- Manuscript claims checked: the key is not cited anywhere in main.tex, sections/*.tex or the supplement. It is an orphan entry, and there is no \nocite. Delete it or fix the authors.

## GlialScar2014
- Exists: yes, but the key is misleading: the entry is a 2008 paper, not 2014. Correct: Cogan, S. F. Neural stimulation and recording electrodes. *Annu. Rev. Biomed. Eng.* **10**, 275–309 (2008). DOI: 10.1146/annurev.bioeng.10.061807.160518
- Bib entry errors: the metadata matches Crossref. Only the key year is inconsistent.
- Study facts: a review of electrode materials and electrochemistry. It is not mainly about glial scarring. Not a speech study.
- Manuscript claims checked:
  - section6_generalization.tex:38 "Glial scarring ... (weeks 1-3 proliferation phase, week 6 stabilization with 200 µm capsule formation) and increases electrode impedance and reduces signal amplitude" -> UNSUPPORTED/UNVERIFIABLE. I could not find these specific timeline or thickness figures in Cogan, which is an electrode-materials review. The co-cited Vansteensel2023 contains no glial or scar content (full text checked). A better source is Polikov, V. S., Tresco, P. A. & Reichert, W. M. Response of brain tissue to chronically implanted neural electrodes. *J. Neurosci. Methods* **148**, 1–18 (2005), DOI 10.1016/j.jneumeth.2005.08.015. Even then, check the "200 µm" and "week 6" figures against it.

## Mandarin2020
- Exists: the entry AS WRITTEN is NO. There is no paper by "W. S. Y. Wang and J. Sun" in *Journal of Chinese Linguistics* (2015) with this title, and the entry has no DOI, volume or pages. The title matches a real 2020 book chapter by a different author: Fon, J. The phonetic realizations of the Mandarin phoneme inventory: the canonical and the variants. In *Speech Perception, Production and Acquisition* (eds Liu, H.-M., Tsao, F.-M. & Li, P.) 11–36 (Springer, 2020). DOI: 10.1007/978-981-15-7606-5_2
- Bib entry errors: wrong authors, venue and year. The entry is effectively fabricated metadata attached to a real title.
- Study facts: a phonetics chapter. Not a neural study.
- Manuscript claims checked:
  - section6_generalization.tex:54 "Mandarin has 21 consonants, 5 vowels, and 4 tones forming 22 total phoneme units with tone" -> WRONG. Fon's chapter abstract says: "The phoneme inventory includes five vowels and 19 consonants, along with four lexical tones." The sentence is also internally inconsistent: 21 + 5 is not 22.
  - "English has 44 phonemes" -> UNSUPPORTED by this source. It is a common approximate figure only.

## ArchitectureComparison2020
- Exists: yes, but the key is misleading: the entry is a 2014 acoustic ASR paper. Correct: Sak, H., Senior, A. & Beaufays, F. Long short-term memory based recurrent neural network architectures for large vocabulary speech recognition. Preprint at https://arxiv.org/abs/1402.1128 (2014). DOI: 10.48550/arXiv.1402.1128. The Interspeech 2014 version is titled "Long short-term memory recurrent neural network architectures for large scale acoustic modeling".
- Bib entry errors: "K. Beaufays" should be "F. Beaufays" (Françoise). The key year 2020 is wrong.
- Study facts: acoustic-speech ASR (Google Voice Search). It compares LSTM, RNN and DNN acoustic models. There is no brain data and no Seq2Seq.
- Manuscript claims checked:
  - section5_benchmarks.tex:17 "LSTM and Seq2Seq models outperformed traditional machine learning by 15-25 percentage points" (said of brain-to-speech decoders) -> UNSUPPORTED/WRONG SOURCE. The paper has no neural decoding and no Seq2Seq, and reports no 15–25 point gain over "traditional ML". Its abstract says only that "LSTM models converge quickly and give state of the art speech recognition performance for relatively small sized models".

## Baillet2001
- Exists: yes. Correct: Baillet, S., Mosher, J. C. & Leahy, R. M. Electromagnetic brain mapping. *IEEE Signal Process. Mag.* **18**, 14–30 (2001). DOI: 10.1109/79.962275
- Bib entry errors: none.
- Study facts: a methods review of MEG/EEG source imaging. Not a speech study.
- Manuscript claims checked:
  - section3_modalities.tex:61 "femtotesla" field magnitudes -> CORRECT (standard content of the review).
  - "MEG ... spatial source localization ... on the order of 2-3 mm for superficial cortical sources" -> UNVERIFIABLE/likely overstated. I did not locate a 2–3 mm figure in Baillet et al. MEG localisation accuracy is more usually quoted as a few mm to about 1 cm, depending on source depth and SNR. Soften the claim or cite a specific validation study.

## Vansteensel2023
- Exists: yes. Correct: Vansteensel, M. J., Klein, E., van Thiel, G., Gaytant, M., Simmons, Z., Wolpaw, J. R. & Vaughan, T. M. Towards clinical application of implantable brain–computer interfaces for people with late-stage ALS: medical and ethical considerations. *J. Neurol.* **270**, 1323–1336 (2023). DOI: 10.1007/s00415-022-11464-6
- Bib entry errors: "others" hides 6 co-authors. Otherwise correct.
- Study facts: a narrative review of the medical and ethical aspects of implanted BCIs in ALS. It covers EEG, ECoG, intracortical, sEEG and endovascular recording. Not a primary empirical study.
- Manuscript claims checked (Europe PMC full text searched for cost, $, MEG, fMRI, glia, scar, micromotion, internet, impedance, inflammation):
  - section3_modalities.tex:37 "Signal loss and electrode failure are significant concerns for long-term clinical deployment" -> CORRECT in substance. Quote: "the available evidence suggests that signal quality degrades over the course of time".
  - section5_benchmarks.tex:33 "EEG ... costs $5,000-$50,000 per system" -> UNSUPPORTED. The paper gives no cost figures. It says only "The technology is expensive..." about implanted BCI trials.
  - section5_benchmarks.tex:43 "MEG systems cost $1-5 million ...; fMRI systems cost $2-3 million" -> UNSUPPORTED. The paper does not mention MEG or fMRI at all.
  - section5_benchmarks.tex:140 "patient populations ... have limited device access and unreliable internet" -> UNSUPPORTED. The paper does not discuss internet or connectivity. It does mention limited trial access in urban academic centres.
  - section6_generalization.tex:38 "Electrode micromotion ... causes gradual signal attenuation" -> UNSUPPORTED. The paper does not mention micromotion; only general signal degradation is supported.
  - section6_generalization.tex:38 glial scarring and impedance (co-cited) -> UNSUPPORTED. There is no glial or scar content.

## Boto2018
- Exists: yes. Correct: Boto, E., Holmes, N., Leggett, J., Roberts, G., Shah, V., Meyer, S. S. et al. Moving magnetoencephalography towards real-world applications with a wearable system. *Nature* **555**, 657–661 (2018). DOI: 10.1038/nature26147
- Bib entry errors: none, apart from "others".
- Study facts: a demonstration of OPM-MEG in a wearable helmet (healthy humans, motor and other tasks). Not a speech-decoding study.
- Manuscript claims checked:
  - section3_modalities.tex:65 "requirement for a magnetically shielded room and the prohibitive cost of the cryogenic infrastructure ... OPM ... operate at room temperature and can be worn as a helmet" -> CORRECT. This is the stated motivation of Boto et al. Caveat: their OPM system itself still ran inside a magnetically shielded room, with field-nulling coils.

## Kaplan2020
- Exists: yes. Correct: Kaplan, J., McCandlish, S., Henighan, T., Brown, T. B., Chess, B., Child, R. et al. Scaling laws for neural language models. Preprint at https://arxiv.org/abs/2001.08361 (2020).
- Bib entry errors: none, apart from "others".
- Study facts: text-only language-model scaling laws (cross-entropy loss against parameters, data and compute). No speech, no WER, no rescoring.
- Manuscript claims checked:
  - section4_architectures.tex:73 "This simple post-hoc [LM interpolation] integration yields substantial WER reductions [Kaplan2020]" -> UNSUPPORTED/WRONG SOURCE. The abstract covers only "empirical scaling laws for language model performance on the cross-entropy loss". Replace it with Willett 2023 or Card 2024, which report WER with and without the LM, or with an ASR shallow-fusion reference.

## Watanabe2018
- Exists: yes. Correct: Watanabe, S., Hori, T., Karita, S., Hayashi, T., Nishitoba, J., Unno, Y. et al. ESPnet: end-to-end speech processing toolkit. In *Proc. Interspeech 2018* 2207–2211 (2018). DOI: 10.21437/Interspeech.2018-1456 (arXiv:1804.00015)
- Bib entry errors: prefer the Interspeech version over the arXiv one. The authors match.
- Study facts: an ASR software toolkit. Not neural.
- Manuscript claims checked:
  - section5_benchmarks.tex:142 "standard software libraries (OpenSeq2Seq, ESPnet)" -> CORRECT.

## Watanabe2020
- Exists: yes. Correct: Watanabe, S., Boyer, F., Chang, X., Guo, P., Hayashi, T., Higuchi, Y. et al. The 2020 ESPnet update: new features, broadened applications, performance improvements, and future plans. Preprint at https://arxiv.org/abs/2012.13006 (2020). A version was also published at IEEE DSLW 2021.
- Bib entry errors: none. The author list matches arXiv exactly.
- Manuscript claims checked:
  - section5_benchmarks.tex:142 -> CORRECT (same sentence as Watanabe2018).

## Ma2023
- Exists: yes. Correct: Ma, X., Rizzoglio, F., Bodkin, K. L., Perreault, E., Miller, L. E. & Kennedy, A. Using adversarial networks to extend brain computer interface decoding accuracy over time. *eLife* **12**, e84296 (2023). DOI: 10.7554/eLife.84296
- Bib entry errors: none.
- Study facts: intracortical (96-channel Utah array in M1). Participants were 6 MONKEYS, not humans. The task is grasping and reaching, decoding EMG and hand trajectories across days. It aligns data across days (sessions) with Cycle-GAN or ADAN. It is NOT speech and NOT cross-modal. Quote: "We trained six monkeys to perform five tasks: power and key grasping, center-out target reaching using isometric wrist torque, and center-out and random-target reaching movements". Primary empirical: yes, but not speech.
- Manuscript claims checked:
  - section6_generalization.tex:68 listed among "the five cross-modal studies" with "Feature alignment using adversarial training to learn modality-invariant representations" -> WRONG. The adversarial alignment is across recording days (session drift) in monkey motor iBCI, not across modalities, and there is no speech. If the "five cross-modal studies" come from the included set, Ma2023 is not an eligible included study.

## Zhang2026Align
- Exists: yes (arXiv, 18 Mar 2026). Correct: Zhang, Z., Li, S., Sabatini, B. L., Aoi, M. & Mishne, G. ALIGN: adversarial learning for generalizable speech neuroprosthesis. Preprint at https://arxiv.org/abs/2603.18299 (2026).
- Bib entry errors: none.
- Study facts: intracortical human speech decoding (public intracortical speech data). It uses multi-domain adversarial training for semi-supervised CROSS-SESSION adaptation. Headline, from the abstract: "generalizes consistently better to previously unseen sessions, improving both phoneme error rate and word error rate relative to baselines". The abstract gives no numbers. Primary empirical: yes, but it is a method study on existing data.
- Manuscript claims checked:
  - section6_generalization.tex:68 counted as a cross-modal study, "modality-invariant representations" -> WRONG. The paper is session-invariant within one modality (intracortical): "a session-invariant learning framework ... for semi-supervised cross-session adaptation".
  - "None achieved dramatic success (>80% retention)" -> UNVERIFIABLE. The paper reports no retention metric.

## Yang2026Corteg
- Exists: yes (arXiv, 11 May 2026). Correct: Yang, L., Sun, Q., Van Dyck, B., Calvo Merino, E. & Van Hulle, M. M. CORTEG: foundation models enable cross-modality representation transfer from scalp to intracranial brain recordings. Preprint at https://arxiv.org/abs/2605.10337 (2026).
- Bib entry errors: none.
- Study facts: a pretrained scalp-EEG foundation model adapted to ECoG. Tasks: "public finger trajectory regression (n=9) and private audio envelope regression (n=16)". The audio envelope task is speech/audio-related regression, not speech decoding to text. Result: "CORTEG matches or exceeds the strongest task-specific baselines on both tasks ... with larger and statistically significant gains on the audio task". Primary empirical: yes.
- Manuscript claims checked:
  - section6_generalization.tex:68 "(3) Multi-task learning to identify shared structure across modalities" -> WRONG characterisation. The method is foundation-model pretraining on EEG with fine-tuning and a spatial adapter on ECoG (transfer learning), not multi-task learning.
  - section6_generalization.tex:68 "None achieved dramatic success" -> CONTRADICTED IN SPIRIT. CORTEG reports that cross-modality transfer matches or beats the baselines.
  - section6_generalization.tex:70 "cannot ... deploy it on non-invasive EEG ... cross-modal transfer ... remains unachieved" -> MISREPRESENTED. CORTEG transfers in the opposite direction (EEG to ECoG) and reports that it succeeded. It does not test invasive-to-EEG deployment.

## Zhang2025CrossSpecies
- Exists: yes. Correct: Zhang, Y., He, L., Fan, C., Liu, T., Yu, H., Le, T. et al. A cross-species neural foundation model for end-to-end speech decoding. In *Proc. International Conference on Learning Representations (ICLR 2026)* (2026). arXiv:2511.21740.
- Bib entry errors: it should cite the ICLR 2026 version, not only arXiv 2025.
- Study facts: intracortical. It uses human Brain-to-Text '24/'25 benchmark participants, with cross-species (monkey) pretraining. The tasks are attempted and imagined speech to text. Quote: "BIT reduces the word error rate (WER) of the prior end-to-end method from 24.69% to 10.22%". Primary empirical: yes.
- Manuscript claims checked:
  - section7_discussion.tex:164 "This review identified only 2 studies explicitly using foundation models [4 refs]" -> INCONSISTENT. Four references are cited for "2 studies", and one of them (Zhou2025BrainFM) is a survey. Zhang2025 itself is correctly a foundation-model speech study.

## Zhou2025BrainFM
- Exists: yes. Correct: Zhou, X., Liu, C., Chen, Z., Wang, K., Ding, Y., Jia, Z. & Wen, Q. Brain foundation models: a survey on advancements in neural signal processing and brain discovery. Preprint at https://arxiv.org/abs/2503.00580 (2025).
- Bib entry errors: none.
- Study facts: a SURVEY. Not a primary study.
- Manuscript claims checked:
  - section7_discussion.tex:164 counted among "studies explicitly using foundation models" -> WRONG. It is a review, not an included study.
  - section7_discussion.tex:170 "Maximum realistic multi-participant study size is approximately 500-2000 individuals (constrained by patient recruitment, surgical risk, long-term follow-up)" -> UNSUPPORTED. The abstract gives no such figure. It mentions only "improving the quality of brain data".

## Yin2025CrossSubject
- Exists: yes. Correct: Yin, C., Yu, Q., Fang, Z., Peng, C. & Li, P. Rethinking cross-subject data splitting for brain-to-text decoding. In *Proc. 2025 Conference on Empirical Methods in Natural Language Processing* 5686–5700 (ACL, 2025). DOI: 10.18653/v1/2025.emnlp-main.289
- Bib entry errors: it cites arXiv (first posted 2023) with year 2025. It should cite the EMNLP 2025 proceedings with the DOI above.
- Study facts: non-invasive fMRI and EEG to text. It is a methodological paper on data leakage in cross-subject splits and re-evaluates existing models. Quote: "all current splitting methods suffer from data leakage problem ... resulting in significant overfitting and overestimation of decoding models".
- Manuscript claims checked:
  - section7_discussion.tex:170 "500-2000 individuals ... constrained by patient recruitment, surgical risk" -> UNSUPPORTED. The paper is about data splitting in non-invasive datasets and says nothing about surgical recruitment ceilings. A paper on data leakage in splits deserves citation elsewhere, for example on evaluation rigour.

## Liu2026CrossBrain
- Exists: yes, but the key and DOI are WRONG. The first author is Levin, not Liu, and the bib DOI 10.1101/2026.01.12.699110 returns 404 at doi.org. Correct: Levin, A. D., Avansino, D. T., Kamdar, F. B., Card, N. S., Wairagkar, M., Jacques, B. G. et al. Cross-brain transfer of high-performance intracortical speech and handwriting BCIs. Preprint at *bioRxiv* https://doi.org/10.64898/2026.01.12.699110 (2026). The senior author is Willett, F. R.
- Bib entry errors: author = {others} (no names), a key that implies a first author "Liu", and a non-resolving DOI prefix. The correct prefix is 10.64898.
- Study facts: intracortical. Participants are 5 human BrainGate2 participants (T12, T15, T16 and others). Tasks are speech and handwriting decoding. It performs CROSS-SUBJECT transfer within one modality. Quote: "cross-brain transfer improved decoding performance when training data from the target user was limited (< 200 sentences)". Primary empirical: yes.
- Manuscript claims checked:
  - section6_generalization.tex:68 "(4) Transfer learning with fine-tuning on small cross-modal datasets" and counted among the "five cross-modal studies" -> WRONG. The transfer is cross-participant within intracortical recording, not cross-modal.
  - section6_generalization.tex:70 "cannot ... deploy it on non-invasive EEG" -> UNSUPPORTED. The paper includes no EEG.
