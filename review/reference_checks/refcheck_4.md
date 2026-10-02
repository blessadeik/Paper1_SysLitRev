# Reference check, group 4

Sources: Crossref API (DOI metadata), Semantic Scholar/arXiv API (abstracts), full text via PMC/Europe PMC/IOP/arXiv HTML where noted. All paths below are relative to `overleaf/`.

## Duraivel2023
- Exists: yes. Duraivel, S., Rahimpour, S., Chiang, C.-H., Trumpis, M., Wang, C., Barth, K. et al. High-resolution neural recordings improve the accuracy of speech decoding. *Nat. Commun.* **14**, 6938 (2023). DOI: 10.1038/s41467-023-42555-1
- Bib entry errors: none (the author list is only "and others", so the full list should be expanded).
- Study facts: µECoG (intraoperative) compared with standard ECoG/SEEG. 4 µECoG participants (3 having DBS surgery for movement disorders, 1 tumour resection) and **11 separate epilepsy control patients** with standard ECoG/SEEG. Task: non-word repetition (52 tokens, 9 phonemes). Abstract: "57× higher spatial resolution and 48% higher signal-to-noise ratio"; "improved phoneme decoding by 35% compared to standard intracranial signals". Vowel decoding: "ECoG: 36.7%, SEEG: 36.5%, µECoG: 71%". Primary empirical study: yes.
- Manuscript claims checked:
  - (sections/section3_modalities.tex:93) "35 percent improvement in phoneme classification accuracy" -> CORRECT (abstract).
  - same line, "from micro-ECoG versus macro-ECoG in the same four participants" -> WRONG. The comparison is between 4 µECoG patients and 11 *different* control patients with standard ECoG/SEEG.
  - same line, "57-fold increase in effective spatial sampling" -> Largely CORRECT. The paper says "57× higher spatial resolution".

## Angrick2019
- Exists: yes. Angrick, M., Herff, C., Mugler, E., Tate, M. C., Slutzky, M. W., Krusienski, D. J. & Schultz, T. Speech synthesis from ECoG using densely connected 3D convolutional neural networks. *J. Neural Eng.* **16**, 036019 (2019). DOI: 10.1088/1741-2552/ab0c59
- Bib entry errors: none substantive. Crossref gives the online date as Apr 2019, not Jun. Expand the authors.
- Study facts: ECoG; 6 participants (patients having awake craniotomy or epilepsy surgery); overt word reading; maps high-gamma ECoG to a logMel spectrogram, then a WaveNet vocoder. "correlations up to r = 0.69". Primary empirical: yes.
- Manuscript claims checked:
  - (sections/section4_architectures.tex:27) "mapped ECoG spectrograms to acoustic parameters using DenseNet-style 3-D CNNs" -> CORRECT in substance. Strictly, the method maps ECoG high-gamma features to a logMel spectrogram.

## Lawhern2018
- Exists: yes. Lawhern, V. J., Solon, A. J., Waytowich, N. R., Gordon, S. M., Hung, C. P. & Lance, B. J. EEGNet: a compact convolutional neural network for EEG-based brain–computer interfaces. *J. Neural Eng.* **15**, 056013 (2018). DOI: 10.1088/1741-2552/aace8c
- Bib entry errors: none. The month is Jul (online 27 Jul 2018), not Oct; this is minor.
- Study facts: EEG method paper (P300, ERN, MRCP, SMR paradigms). Not a speech study.
- Manuscript claims checked:
  - (sections/section4_architectures.tex:27) "compact separable-CNN baseline ... widely adopted across EEG classification" -> CORRECT.
  - (sections/section5_benchmarks.tex:27) "scalp EEG achieves 40-60 mm resolution with only 64-256 electrodes" -> UNSUPPORTED. EEGNet does not report spatial-resolution figures.

## Hochreiter1997
- Exists: yes. Hochreiter, S. & Schmidhuber, J. Long short-term memory. *Neural Comput.* **9**, 1735–1780 (1997). DOI: 10.1162/neco.1997.9.8.1735
- Bib entry errors: none.
- Manuscript claims checked:
  - (sections/section4_architectures.tex:31) "LSTM unit was introduced ... forget, input, output gates" -> PARTLY CORRECT. The 1997 paper introduced the input and output gates. The **forget gate was added later** by Gers, Schmidhuber & Cummins (2000, *Neural Comput.* 12, 2451). Consider citing that paper as well.

## Sutskever2014
- Exists: yes. Sutskever, I., Vinyals, O. & Le, Q. V. Sequence to sequence learning with neural networks. In *Advances in Neural Information Processing Systems 27* 3104–3112 (2014). arXiv:1409.3215
- Bib entry errors: cited as an arXiv "article". It should cite the NeurIPS 2014 proceedings version.
- Manuscript claims checked:
  - (sections/section4_architectures.tex:42) encoder-decoder maximising conditional likelihood -> CORRECT.

## Chen2020
- Exists: yes. Chen, T., Kornblith, S., Norouzi, M. & Hinton, G. A simple framework for contrastive learning of visual representations. In *Proc. 37th International Conference on Machine Learning*, PMLR **119**, 1597–1607 (2020). arXiv:2002.05709
- Bib entry errors: cited as arXiv. It should cite ICML 2020 (PMLR 119).
- Manuscript claims checked:
  - (sections/section4_architectures.tex:61) "Contrastive approaches ... NT-Xent objective" -> CORRECT.

## Wang2023BrainBERT
- Exists: yes. Wang, C., Subramaniam, V., Yaari, A. U., Kreiman, G., Katz, B., Cases, I. & Barbu, A. BrainBERT: self-supervised representation learning for intracranial recordings. In *International Conference on Learning Representations (ICLR)* (2023). arXiv:2302.14367
- Bib entry errors: cited as arXiv with "and others". It should cite ICLR 2023 and give the full author list.
- Study facts: SEEG/intracranial recordings from epilepsy patients watching movies (about 10 participants, as I recall from the paper; I did not re-verify this in the full text). Transformer pretrained with masked spectrogram modelling. Downstream tasks are perceptual (sentence onset, speech vs non-speech, pitch, volume). It is **not a speech-production or brain-to-text decoding study**; it is a methods/representation paper.
- Manuscript claims checked:
  - (sections/section4_architectures.tex:65) "applied BERT-style masked pre-training to intracranial EEG" -> CORRECT.
  - (sections/section4_architectures.tex:73) "Foundation models applying SSL pre-training across large multi-participant neural corpora" -> CORRECT in broad terms.
  - (sections/section7_discussion.tex:164) counted as one of "only 2 studies explicitly using foundation models" -> Note that 4 keys are cited for "2 studies", which is internally inconsistent. BrainBERT does not decode speech.
  - (sections/section7_discussion.tex:166) "Direct application without adaptation typically underperforms custom-trained models" -> UNSUPPORTED/contradicted. BrainBERT reports that pretrained representations *improve* decoding with less data ("enables classifying complex concepts ... with higher accuracy and with much less data").

## Ye2025
- Exists: yes. Ye, Z., Ai, Q., Liu, Y., de Rijke, M., Zhang, M., Lioma, C. & Ruotsalo, T. Generative language reconstruction from brain recordings. *Commun. Biol.* **8**, 346 (2025). DOI: 10.1038/s42003-025-07731-7
- Bib entry errors: none in the metadata. Expand the authors.
- Study facts:
  - Modality: **fMRI**, non-invasive; **healthy participants perceiving** visual or auditory language.
  - Datasets: "5 participants in Pereira's dataset, 8 participants in Huth's dataset, and 28 participants in the Narratives dataset".
  - Method: BrainLLM, which feeds decoded fMRI representations into Llama-2.
  - Metrics (Table 1, BrainLLM): Huth BLEU-1 0.1899, ROUGE-1 0.1780, WER 0.8916; Pereira BLEU-1 0.3432, WER 0.7576; Narratives BLEU-1 0.1375, WER 0.9239.
  - The full text contains **no** occurrence of "week", "session", "longitudinal", "recalibrat", "retention", "daily" or "intracortical".
  - Primary empirical study: yes, but on language *perception* reconstruction, not speech production.
- Manuscript claims checked:
  - (sections/section6_generalization.tex:36) and (sections/appendices.tex:149) "Ye et al. demonstrated >80% performance retention across 4 weeks of daily use with recalibration" -> WRONG/UNSUPPORTED, likely fabricated. There is no longitudinal or cross-session evaluation at all.
  - (sections/section6_generalization.tex:8) "Long-term cross-session stability ... appears in exactly 1 study \cite{Ye2025}" -> WRONG. Ye2025 has no cross-session analysis.
  - (supplementary/supplement_table_s1.tex:106) "Ye et al. 2025, Intracort., 1, Attempted speech, Transformer, WER 8.1%, Long-term" -> WRONG on every field. Correct values: fMRI; 41 participants (5+8+28), healthy; perceived language; LLM (Llama-2) plus fMRI encoder; WER about 0.76–0.92; no long-term evaluation. Rows 56 (Ye 2024) and 65 (Ye 2023) should also be checked.
  - (sections/section4_architectures.tex:73) "align neural encoder representations directly with LLM latent spaces, enabling continuous semantic reconstruction from fMRI" -> CORRECT.
  - (sections/section7_discussion.tex:164) counted as a foundation-model study -> ACCEPTABLE, since it uses an LLM backbone.
  - (sections/section7_discussion.tex:168) "Foundation model pre-training is not feasible ... unless using transfer from language" -> Loosely consistent. The paper uses a pretrained LLM and says it is "fully trained with only a limited amount of neurological data".
  - For a genuine long-term intracortical speech study, the likely intended paper is Card, N. S. et al. An accurate and rapidly calibrating speech neuroprosthesis. *N. Engl. J. Med.* **391**, 609–618 (2024), which reports 8 months of use (97.5% accuracy). Wairagkar et al. 2025 (*Nature*) is another option. Card2024 already appears to be in the bib.

## Yuan2024
- Exists: yes (arXiv preprint). Yuan, B. A. & Makin, J. G. Improving speech decoding from ECoG with self-supervised pretraining. Preprint at https://arxiv.org/abs/2405.18639 (2024). I found no peer-reviewed version.
- Bib entry errors: none.
- Study facts: ECoG; **4 epilepsy patients** (a–d); sentence reading aloud (MOCHA-TIMIT subsets, picture descriptions); wav2vec pretrained on unlabelled ECoG, then an encoder-decoder to text; metric is **WER**. Abstract: "wav2vec's representations decrease word error rates over the original data by upwards of 50%". Primary empirical study: yes.
- Manuscript claims checked:
  - (sections/section4_architectures.tex:73) "SSL pre-training across large multi-participant neural corpora" -> PARTLY CORRECT. It uses SSL and cross-patient pretraining helps "in some cases", but with 4 patients the corpus is not "large".
  - (supplementary/supplement_table_s1.tex:108) "Yuan et al. 2024, ECoG, 2, Phoneme class, CNN, Acc 76.5%" -> WRONG. Correct values: 4 participants; sentence-to-text decoding; WER (per-patient WER reductions of up to about 50%); wav2vec plus seq2seq. There is no 76.5% accuracy.

## Abdulghani2023
- Exists: yes. Abdulghani, M. M., Walters, W. L. & Abed, K. H. Imagined speech classification using EEG and deep learning. *Bioengineering* **10**, 649 (2023). DOI: 10.3390/bioengineering10060649
- Bib entry errors: none.
- Study facts: 8-channel low-cost EEG; "four healthy subjects"; imagined speech of 4 commands (up/down/left/right); wavelet scattering plus LSTM; "92.50% overall classification accuracy". Primary empirical study: yes. There is no LLM, BLEU or ROUGE.
- Manuscript claims checked:
  - (sections/section5_benchmarks.tex:9) "BLEU and ROUGE scores appear in emerging LLM-integrated approaches \cite{Abdulghani2023}" -> WRONG citation. The paper uses accuracy, precision, recall and F1 only. A better citation is Ye2025 (BLEU/ROUGE with an LLM) or Tang2023.
  - The "92.5%" upper bound in section5_benchmarks.tex:25 comes from this paper but is cited to Peterson2021 (see below).

## Peterson2021
- Exists: yes. Peterson, S. M., Steine-Hanson, Z., Davis, N., Rao, R. P. N. & Brunton, B. W. Generalized neural decoders for transfer learning across participants and recording modalities. *J. Neural Eng.* **18**, 026014 (2021). DOI: 10.1088/1741-2552/abda0b
- Bib entry errors: none. The issue date is Mar/Apr 2021.
- Study facts:
  - Modality: ECoG (12 epilepsy patients) plus EEG (15 participants), 27 total.
  - Task: **upper-limb "move" vs "rest" classification. No speech at all.**
  - Method: HTNet, a CNN with a Hilbert transform and a projection onto brain regions. No manifold alignment, autoencoder or adversarial training.
  - Accuracy: tailored HTNet 84% ± 8%; unseen ECoG participant 72% ± 10%. It was the only decoder above chance for ECoG-to-EEG transfer. Fine-tuning with "as few as 50 ECoG or 20 EEG events".
  - Primary speech study: **no** (non-speech motor BCI methods paper).
- Manuscript claims checked:
  - (sections/section5_benchmarks.tex:25) "EEG ... achieves 70-92.5% accuracy \cite{Peterson2021}" on closed-set speech -> WRONG/UNSUPPORTED. Not a speech study; 92.5% is Abdulghani2023.
  - (sections/section5_benchmarks.tex:31) "transfer learning across 20-28 EEG participants retains 60-80% of single-participant performance" -> WRONG. There were 15 EEG participants and no speech. The retention figures are not in the paper (the closest is 72% vs 84% ECoG accuracy).
  - (sections/section6_generalization.tex:14) "28 EEG participants ... 80% retention on vowel classification, 4-class ... 60% on continuous speech, 125K vocabulary" -> WRONG/fabricated. There is no speech, vowel or 125K-vocabulary task.
  - (sections/section6_generalization.tex:16) "applied manifold alignment ... achieving 60-80% transfer" -> WRONG. No manifold alignment.
  - (sections/section6_generalization.tex:20) "naive splits ... inflate generalization estimates by 5-15 percentage points \cite{Peterson2021}" -> UNSUPPORTED.
  - (sections/section6_generalization.tex:26) whole paragraph ("28 EEG participants", "imagined and overt speech", "autoencoders", "transformation matrices", "leave-one-participant-out", "60-80% vowel, 50-70% consonant, 50% continuous word") -> WRONG/fabricated. The only true elements are cross-participant transfer and the use of EEG.
  - (sections/section6_generalization.tex:62) cross-modal transfer -> CORRECT in principle (ECoG to EEG), but the task is arm movement, not speech.
  - (sections/section6_generalization.tex:68) "adversarial training to learn modality-invariant representations" -> WRONG. It uses a brain-region projection layer plus fine-tuning.
  - (sections/appendices.tex:132) "28; 60-80% vs single-participant baseline; Manifold alignment" -> WRONG. Correct values: 27 (12 ECoG + 15 EEG); arm-movement decoding; HTNet projection layer plus fine-tuning.
  - (supplementary/supplement_table_s1.tex:68) "ECoG, 28, Event detection, Acc 70.0" -> WRONG. Correct values: N=27, move/rest; 72% unseen-participant accuracy. It should arguably be **excluded** from a speech-decoding register.

## deBorman2024
- Exists: yes. de Borman, A., Wittevrongel, B., Dauwe, I., Carrette, E., Meurs, A., Van Roost, D., Boon, P. & Van Hulle, M. M. Imagined speech event detection from electrocorticography and its transfer between speech modes and subjects. *Commun. Biol.* **7**, 818 (2024). DOI: 10.1038/s42003-024-06518-6
- Bib entry errors: none. Expand the authors.
- Study facts:
  - Modality: ECoG, in **16 analysed epilepsy patients** (19 recruited). "Ten of 16" showed above-chance imagined-speech detection.
  - Task: performed, perceived and imagined speech of 20 Dutch sentences.
  - Method: binary speech-event vs silence detection with a linear model.
  - Best single-electrode accuracy: performed 93.23%, perceived 93.98%, imagined 86.81%.
  - Transfer: "Performance above chance level could be obtained for subjects with electrodes in similar brain regions". There is **no "70%" figure** and no "85-90% retention" figure.
  - "Speech modes" here means performed/perceived/imagined, **not recording modalities**.
  - Primary empirical study: yes (speech detection, not decoding).
- Manuscript claims checked:
  - (sections/section6_generalization.tex:30) "8 participants" -> WRONG (16 analysed).
  - same line, "Detect motor intention onset (did the participant attempt to speak?)" -> PARTLY WRONG. It detects speech events in 3 modes, with imagined speech as the focus.
  - same line, "70% accuracy ... retaining 85-90% of within-participant accuracy" -> UNSUPPORTED. Neither number appears in the paper.
  - (sections/appendices.tex:136) "8; 70% accuracy; Domain adaptation" and (supplementary/supplement_table_s1.tex:82) "ECoG, 8, Acc 70.0" -> WRONG N and UNSUPPORTED accuracy. Transfer is by direct model transfer between similar electrode locations, not "domain adaptation".
  - (sections/section6_generalization.tex:8, :16) cross-participant generalization -> CORRECT (qualitative).
  - (sections/section6_generalization.tex:62, :68) cited as **cross-modal** (recording-modality) transfer -> WRONG. Its transfer is across speech *modes* within ECoG.

## Panayotov2015
- Exists: yes. Panayotov, V., Chen, G., Povey, D. & Khudanpur, S. Librispeech: an ASR corpus based on public domain audio books. In *Proc. IEEE ICASSP* 5206–5210 (2015). DOI: 10.1109/ICASSP.2015.7178964
- Bib entry errors: none.
- Study facts: ASR speech corpus (about 1000 h). Not neural data.
- Manuscript claims checked:
  - (sections/section5_benchmarks.tex:9) cited for "nine distinct performance metrics, creating a fundamental comparability problem" -> UNSUPPORTED/irrelevant. This is an ASR dataset paper. It could be retained only as an example of a standard benchmark.
  - (sections/section5_benchmarks.tex:142) "benchmark against community leaderboards" -> ACCEPTABLE (LibriSpeech is the standard ASR benchmark).

## Willett2024Benchmark
- Exists: the bib entry as written is **no** (placeholder). DOI 10.48550/arXiv.2401.00000 returns HTTP 404, and the title "Brain-to-Text Benchmark 2024: Lessons Learned" is inexact. The real paper is: Willett, F. R., Li, J., Le, T., Fan, C., Chen, M., Shlizerman, E. et al. Brain-to-Text Benchmark '24: lessons learned. Preprint at https://arxiv.org/abs/2412.17227 (2024). DOI: 10.48550/arXiv.2412.17227
- Bib entry errors: fake DOI and arXiv ID; wrong title ("2024" should be "'24"); "and others".
- Study facts: competition summary (intracortical data from participant T12). The largest gains came from "an ensembling approach, where the output of multiple independent decoders was merged using a fine-tuned large language model". Transformers and state-space models did "not yet" beat the RNN baseline. The benchmark "will remain open indefinitely". This is a benchmark/competition report, not a primary study.
- Manuscript claims checked:
  - (sections/section5_benchmarks.tex:9) "progress is locally measurable but globally incoherent" -> UNSUPPORTED as a paraphrase. The paper concerns a single standardized benchmark.
  - (sections/section5_benchmarks.tex:144) and sections/section5_benchmarks.tex:120-126 and sections/section7_discussion.tex:22 call for a "Brain-to-Text Benchmark 2025+ initiative" and public leaderboards, claiming brain-to-speech has "no public leaderboard" (sections/section5_benchmarks.tex:142) -> WRONG/misleading. The cited work itself *is* a public brain-to-text benchmark with a leaderboard (Brain-to-Text '24, EvalAI, remaining open). A '25 edition also exists (Card et al. data).

## Berezutskaya2022
- Exists: yes. Berezutskaya, J., Vansteensel, M. J., Aarnoutse, E. J., Freudenburg, Z. V., Piantoni, G., Branco, M. P. & Ramsey, N. F. Open multimodal iEEG-fMRI dataset from naturalistic stimulation with a short audiovisual film. *Sci. Data* **9**, 91 (2022). DOI: 10.1038/s41597-022-01173-0
- Bib entry errors: none. Expand the authors.
- Study facts: dataset paper; iEEG from 51 participants and fMRI from 30 (18 had both); film watching (perception). Not speech decoding.
- Manuscript claims checked:
  - (sections/section5_benchmarks.tex:9) cited for the metric-heterogeneity problem -> UNSUPPORTED. It is a dataset paper and says nothing about metrics across studies.

## Gwilliams2023
- Exists: yes. Gwilliams, L., Flick, G., Marantz, A., Pylkkänen, L., Poeppel, D. & King, J.-R. Introducing MEG-MASC a high-quality magneto-encephalography dataset for evaluating natural speech processing. *Sci. Data* **10**, 862 (2023). DOI: 10.1038/s41597-023-02752-5
- Bib entry errors: none.
- Study facts: MEG dataset of "27 English speakers who listened to two hours of naturalistic stories". Dataset, not a decoding study.
- Manuscript claims checked:
  - (sections/section3_modalities.tex:63) cited as one of "four public datasets" used by Défossez et al. (175 participants) -> CORRECT. Gwilliams (MEG-MASC) is one of the four datasets (the others are Schoffelen MEG, Broderick EEG and Brennan EEG). Note that Défossez used an earlier release of this data. The "41 percent top-1" figure belongs to Defossez2023, not this reference.

## Ardila2020
- Exists: yes. Ardila, R., Branson, M., Davis, K., Henretty, M., Kohler, M., Meyer, J. et al. Common Voice: a massively-multilingual speech corpus. In *Proc. 12th Language Resources and Evaluation Conference (LREC)* 4218–4222 (2020). arXiv:1912.06670
- Bib entry errors: cited as arXiv. It should cite LREC 2020. The arXiv year is 2019 (submitted Dec 2019; v2 Mar 2020).
- Study facts: crowdsourced ASR corpus (29 languages, 2,500 h at the time). Not neural data.
- Manuscript claims checked:
  - (sections/section5_benchmarks.tex:9) cited for the metric-heterogeneity problem -> UNSUPPORTED/irrelevant.
  - Uncited mentions (sections/section5_benchmarks.tex:96,108,125; sections/section7_discussion.tex:27,61,65), e.g. "Common Voice English vocabulary, 10K" and "100-200 hours ... comparable to Common Voice scope" -> The scale comparison is inaccurate. Common Voice had 2,500 h in 2019 and far more now, so 100–200 h is not comparable. Mention SRUS/Milvus analogies (sections/section5_benchmarks.tex:122,144) as dubious. "SRUS" is not a recognised ASR benchmark initiative.

## Logothetis2010
- Exists: yes, but the key and year are inconsistent. Logothetis, N. K. & Wandell, B. A. Interpreting the BOLD signal. *Annu. Rev. Physiol.* **66**, 735–769 (2004). DOI: 10.1146/annurev.physiol.66.082602.092845
- Bib entry errors: the co-author is "**B. A.** Wandell", not "J. D. Wandell". The key says 2010 but the paper is 2004. This is fine if intentional; otherwise the author may have meant Logothetis, N. K. The underpinnings of the BOLD functional magnetic resonance imaging signal. *J. Neurosci.* 23, 3963 (2003), or Logothetis 2008 *Nature* 453, 869.
- Study facts: review of the neural basis of BOLD. Not speech.
- Manuscript claims checked:
  - (sections/section3_modalities.tex:69) "haemodynamic response peaks approximately 4-5 seconds after the neural event" -> Broadly CORRECT. The HRF typically peaks about 4–6 s; I did not verify an exact quote.
  - (sections/section5_benchmarks.tex:39) "integrates neural activity over 4-5 seconds post-stimulus" -> Loosely supported. The wording conflates peak latency with the integration window.
