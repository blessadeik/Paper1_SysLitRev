# Reference check, group 1

Sources: Crossref API, Europe PMC abstracts and full texts (PMC10468393 Willett; PMC4464168 Herff; PMC8261053 Kostas), PMC pages for Makin (PMC10560395), Metzger (PMC10826467) and Card (PMC11328962).
Paths: S3 = sections/section3_modalities.tex, S4 = section4_architectures.tex, S5 = section5_benchmarks.tex, S6 = section6_generalization.tex, S7 = section7_discussion.tex, FT = figures_and_tables.tex, APP = appendices.tex, SUP = supplementary/supplement_table_s1.tex.

**Cross-cutting problem: hard-coded reference numbers.** The tables use hard-coded "[n]" numbers, but these do not match the IEEEtran numbering, which follows first-citation order: 1 TaskForce2010, 2 Moses2021, 3 Willett2023, 4 Card2024, 5 Metzger2023, 6 Page2021, 8 Tricco2018, 19 Herff2015, 20 Anumanchipalli2019, 21 Makin2020, 26 Wairagkar2025.
- APP:77-87: Herff "[6]" resolves to PRISMA 2020. Makin "[8]" resolves to Tricco. Moses "[5]" resolves to Metzger. Card "[2]" resolves to Moses. Anumanchipalli "[26]" resolves to Wairagkar. Only Willett "[3]" is right.
- FT:171: "[2], [3], [8]" resolves to Moses, Willett and Tricco.
- Fix: replace all of these with \cite{}.

---

## TaskForce2010
- Exists: yes. Laureys, S., Celesia, G. G., Cohadon, F., Lavrijsen, J., León-Carrión, J., Sannita, W. G., Sazbon, L., Schmutzhard, E., von Wild, K. R., Zeman, A., Dolce, G. & European Task Force on Disorders of Consciousness. Unresponsive wakefulness syndrome: a new name for the vegetative state or apallic syndrome. *BMC Med.* **8**, 68 (2010). DOI: 10.1186/1741-7015-8-68
- Bib entry errors:
  - The first author should be Laureys, S. (the key "TaskForce2010" is fine).
  - The month is Nov (published 1 Nov 2010), not Dec.
  - There is no issue "1".
- Study facts: position paper proposing a new name for the vegetative state. No data, no BCI, no AAC, no ALS. Not an empirical study.
- Manuscript claims checked:
  - main.tex:73 "each requires preserved residual motor function that late-stage ALS and locked-in patients may no longer possess" -> UNSUPPORTED. The paper is about renaming vegetative state/UWS and does not discuss AAC or ALS/LIS. Cite an AAC/ALS communication source instead (e.g. a review of AAC/BCI in ALS or LIS).
  - main.tex:73 "The clinical imperative is real and urgent" -> UNSUPPORTED/irrelevant. UWS patients are unresponsive, not the target population for speech BCIs.

## Card2024
- Exists: yes. Card, N. S., Wairagkar, M., Iacobacci, C., Hou, X., Singer-Clark, T., Willett, F. R. et al. An accurate and rapidly calibrating speech neuroprosthesis. *N. Engl. J. Med.* **391**, 609–618 (2024). DOI: 10.1056/NEJMoa2314132
- Bib entry errors: none. Metadata matches Crossref (18 authors, last author Brandman, D. M.).
- Study facts:
  - Modality: intracortical, "four microelectrode arrays into his left ventral precentral gyrus … 256 intracortical electrodes".
  - Participants: N=1, "45-year-old man with amyotrophic lateral sclerosis (ALS) with tetraparesis and severe dysarthria".
  - Task: attempted speech.
  - Vocabulary: 50 words (day 1), 125,000 words (from day 2).
  - Metrics: "99.6% accuracy with a 50-word vocabulary"; "after 1.4 additional hours of system training … 90.2% accuracy using a 125,000-word vocabulary"; "sustained 97.5% accuracy over a period of 8.4 months"; "approximately 32 words per minute for more than 248 cumulative hours".
  - Calibration: "Calibration of the neuroprosthesis required 30 minutes of cortical recordings" on day 1 only. Later recalibrations "took approximately 7.5 minutes".
  - Decoder: RNN phoneme decoder with n-gram LM plus LLM rescoring (the exact model names are in the supplement, not independently checked).
  - Primary empirical study: yes.
- Manuscript claims checked:
  - main.tex:75, cited as a landmark -> CORRECT.
  - S3:33 "2.5 percent WER sustained over eight months" -> CORRECT (100 − 97.5; 8.4 months).
  - S3:33 "with a 30-minute daily calibration protocol" -> WRONG. The 30 minutes was initial day-1 calibration; later recalibrations took about 7.5 minutes.
  - S4:38 "Card … (WER 2.5 percent) … RNN decoders combined with language model rescoring" -> CORRECT.
  - S5:13 "2.5% WER on a 125,000-word vocabulary (expanded from 50 words in a second session) … approximately 32 words per minute" -> CORRECT. "Single participant" is also correct.
  - S5:17 "10-fold improvement in WER (Herff 25% → Card 2.5%)" -> MISLEADING. Herff's 25% is with a 10-word dictionary and Card's 2.5% is at 125k words, so they are not comparable.
  - S3:97 "best intracortical result (2.5 percent, Card and colleagues)" -> CORRECT.
  - FT:46 "Card et al. (2024): 2.5% WER (125k-word) with intracortical" -> CORRECT.
  - APP:87 "Card et al. 2024 | Intracortical | 1 | 30 words | WER 2.5" -> WRONG vocabulary (125,000 words; the 50-word vocabulary gave 99.6% accuracy). "[2]" is the wrong reference number.
  - APP:90 caption "10-fold improvement … on comparable vocabulary sizes" -> WRONG (10 words vs 125,000 words).
  - SUP:76, row 15: "Intracort., 1, Attempted, LLM-int., WER 2.5, Generalization None" -> modality, N and task CORRECT. "Generalization None" is questionable, because the paper reports accuracy sustained over 8.4 months (long-term use).
  - S6:36 "Only one human-participant study [Ye2025] explicitly evaluated … weeks or months later" -> CONTRADICTED by Card (8.4 months) and Moses 2021 (81 weeks).

## Willett2023
- Exists: yes. Willett, F. R., Kunz, E. M., Fan, C., Avansino, D. T., Wilson, G. H., Choi, E. Y. et al. A high-performance speech neuroprosthesis. *Nature* **620**, 1031–1036 (2023). DOI: 10.1038/s41586-023-06377-x
- Bib entry errors: none.
- Study facts:
  - Modality: intracortical Utah arrays, four in total (two in area 6v, two in area 44). Spiking activity.
  - Participants: N=1 (T12), "bulbar-onset amyotrophic lateral sclerosis".
  - Task: attempted speech, vocalized and silent.
  - Vocabulary: 50 words and 125,000 words.
  - Metrics: "9.1% word error rate on a 50-word vocabulary … and a 23.8% word error rate on a 125,000-word vocabulary"; "62 words per minute".
  - Offline results: "an improved language model could decrease word error rates from 23.8 to 17.4%, and … testing on more proximal sentences further decreased word error rates to 11.8%".
  - Decoder: "five-layer, gated recurrent-unit" RNN plus "125,000-word trigram model implemented in Kaldi".
  - Primary empirical study: yes.
- Manuscript claims checked:
  - main.tex:75 -> CORRECT.
  - S3:33 "Willett … extended this [Moses 2021] to 62 words per minute at 9 percent WER for a 50-word vocabulary" -> 62 WPM and 9.1% are CORRECT. Note that Willett is intracortical while Moses is ECoG (see Moses2021).
  - S4:38 "Willett (62 WPM) … RNN decoders combined with language model rescoring" -> CORRECT (GRU RNN plus n-gram LM).
  - S4:73, S5:13, S5:138 "9.1% WER on 50-word vocabulary and 23.8% WER on 125k-word vocabulary" -> CORRECT.
  - S5:17 "language model integration (rescoring alone provides 10-14 percentage-point WER reduction \cite{Willett2023})" -> UNSUPPORTED. Willett reports no LM-vs-no-LM WER ablation. The only LM effect reported is an improved LM taking WER from 23.8% to 17.4% (−6.4 pp). The phoneme error rate before the LM is 19.7–22.1%, which is a different metric.
  - S5:138 "The 14-percentage-point gap reflects vocabulary size" -> CORRECT arithmetic (23.8 − 9.1 = 14.7).
  - S5:146 "14 percentage-point LM benefit" -> WRONG. It conflates the vocabulary gap with an LM benefit, which contradicts S5:138.
  - FT:46 "9% WER (50-word) with intracortical" -> CORRECT.
  - APP:85 "Intracortical, 1, 50 words, WER 9.0" -> CORRECT. The exact value is 9.1.
  - SUP:74, row 14: "Architecture: Transformer" -> WRONG (GRU RNN). "WER 9.0" should be 9.1. Modality, N and task are CORRECT.

## Metzger2023
- Exists: yes. Metzger, S. L., Littlejohn, K. T., Silva, A. B., Moses, D. A., Seaton, M. P., Wang, R. et al. A high-performance neuroprosthesis for speech decoding and avatar control. *Nature* **620**, 1037–1046 (2023). DOI: 10.1038/s41586-023-06443-4
- Bib entry errors: none.
- Study facts:
  - Modality: ECoG, a 253-channel high-density surface array (not intracortical).
  - Participants: N=1, anarthria and quadriplegia from a pontine (brainstem) stroke.
  - Task: "attempted to silently speak sentences".
  - Vocabulary: 1,024-word general set; 50-phrase AAC set (119 words).
  - Metrics: "median rate of 78 words per minute and median word error rate of 25%" (25.5% in the text, 78.3 WPM). The 50-phrase AAC set gave a median WER of 4.92%.
  - Decoder: 4-layer bidirectional GRU RNN with CTC loss, plus a 5-gram LM. Also speech synthesis and avatar outputs.
  - Primary empirical study: yes.
- Manuscript claims checked:
  - main.tex:75 -> CORRECT.
  - S3:27 "high-density ECoG in a participant with anarthria following brainstem stroke" -> CORRECT.
  - main.tex:63, main.tex:150 and S7:11 "2.5% WER and 78 WPM" -> MISLEADING. The 78 WPM (Metzger, ECoG) came with a 25% WER; the 2.5% WER (Card) came at about 32 WPM. No single system achieves both, so these must be attributed separately.
  - SUP:124, row 39: "Intracort." -> WRONG (ECoG).
  - SUP:124, row 39: "Transformer" -> WRONG (bidirectional GRU RNN with CTC).
  - SUP:124, row 39: "WER 4.2" -> WRONG. The paper reports 25.5% on 1,024 words and 4.92% on the 50-phrase set; no 4.2% appears.

## Moses2021
- Exists: yes. Moses, D. A., Metzger, S. L., Liu, J. R., Anumanchipalli, G. K., Makin, J. G., Sun, P. F. et al. Neuroprosthesis for decoding speech in a paralyzed person with anarthria. *N. Engl. J. Med.* **385**, 217–227 (2021). DOI: 10.1056/NEJMoa2027540
- Bib entry errors: none.
- Study facts:
  - Modality: ECoG, "a subdural, high-density, multielectrode array" (128 channels) over sensorimotor cortex.
  - Participants: N=1, "anarthria … and spastic quadriparesis caused by a brain-stem stroke".
  - Task: attempted speech.
  - Vocabulary: 50 words.
  - Metrics: "median rate of 15.2 words per minute, with a median word error rate of 25.6%"; "classified words with 47.1% accuracy using cortical signals that were stable throughout the 81-week study period".
  - Decoder: deep-learning word classifier plus a next-word language model.
  - Primary empirical study: yes.
- Manuscript claims checked:
  - main.tex:75 -> CORRECT.
  - S3:33 lists Moses under "The clinical results from the intracortical modality" -> WRONG MODALITY (ECoG).
  - S3:33 "first real-time sentence decoding in a person with anarthria at 15 words per minute" -> CORRECT (15.2).
  - S5:13 "Moses et al. (using subdural ECoG) achieved 15.2 words per minute" -> CORRECT.
  - FT:46 "Moses et al. (2021): 15.2 WPM with intracortical" -> WRONG MODALITY.
  - APP:83 "Intracortical, 1, 50 words, WPM 15.0" -> modality WRONG (ECoG), and the value should be 15.2. Its "[5]" resolves to Metzger.
  - SUP:72, row 13: "Intracort." -> WRONG (ECoG).
  - SUP:72, row 13: "Generalization None" -> questionable. The paper reports signals stable over 81 weeks, which also contradicts S6:36.
  - SUP:72, row 13: "LSTM" -> UNVERIFIED. The paper says only "deep-learning algorithms"; I believe it is GRU-based but did not confirm.

## Herff2015
- Exists: yes. Herff, C., Heger, D., de Pesters, A., Telaar, D., Brunner, P., Schalk, G. & Schultz, T. Brain-to-text: decoding spoken phrases from phone representations in the brain. *Front. Neurosci.* **9**, 217 (2015). DOI: 10.3389/fnins.2015.00217
- Bib entry errors: none. Consider expanding the author list.
- Study facts:
  - Modality: ECoG.
  - Participants: 7, "Seven epileptic patients at Albany Medical Center".
  - Task: overt speech ("read the text aloud").
  - Vocabulary: WER was evaluated as a function of dictionary size. "word error rates as low as 25%"; "With 10 words in the dictionary, 75% of all words are recognized correctly".
  - Decoder: GMM-HMM ASR with an n-gram LM and Viterbi decoding.
  - Primary empirical study: yes.
- Manuscript claims checked:
  - S3:23 "approximately 25 percent WER on continuous spoken phrases from seven participants … classical hidden Markov model" -> PARTLY CORRECT. The 25% is a best-case figure ("as low as") with a 10-word dictionary, not an average across all 7 participants. The HMM detail is correct.
  - S4:19 "WER of approximately 25 percent using HMM-based acoustic models on ECoG" -> CORRECT, with the same 10-word caveat.
  - S5:17 "Herff 25% WER" as the baseline for a "10-fold improvement" -> MISLEADING (vocabulary not comparable).
  - FT:46 "25% WER on ECoG with 7 participants" -> CORRECT, with the caveat above.
  - APP:77 "ECoG, 7, 50 words, WER 25.0" -> WRONG vocabulary (25% corresponds to a 10-word dictionary). Its "[6]" resolves to Page2021.
  - SUP:48, row 1: "ECoG, 7, Overt speech, Trad. ML, WER 25.0" -> CORRECT.
  - S5:19 "multi-participant invasive studies (Herff n=7 …) demonstrate that cross-participant transfer learning retains 50-80%" -> UNSUPPORTED. Herff trained per participant; no transfer is reported.
  - APP:53 quality score and critique -> reviewer judgment, not checkable.

## Schirrmeister2017
- Exists: yes. Schirrmeister, R. T., Springenberg, J. T., Fiederer, L. D. J., Glasstetter, M., Eggensperger, K., Tangermann, M., Hutter, F., Burgard, W. & Ball, T. Deep learning with convolutional neural networks for EEG decoding and visualization. *Hum. Brain Mapp.* **38**, 5391–5420 (2017). DOI: 10.1002/hbm.23730
- Bib entry errors:
  - The last author is wrong: "A. Lienkamp" should be **T. Ball**.
  - "M. Eggensperger" should be **K. Eggensperger**.
  - The month is Aug (published online 7 Aug 2017; issue Nov) — acceptable as is.
- Study facts:
  - Modality: EEG motor imagery and motor execution (not speech).
  - Metrics: "mean decoding accuracies 82.1% FBCSP, 84.0% deep ConvNets". ConvNets "learned to use spectral power modulations in the alpha, beta, and high gamma frequencies".
  - Type: methods paper with empirical EEG data. No ECoG comparison.
- Manuscript claims checked:
  - S3:51 "signal-to-noise ratio is substantially lower than ECoG across all frequency bands" -> UNSUPPORTED (the paper has no ECoG comparison).
  - S3:51, next clause "high-gamma … effectively inaccessible" -> CONTRADICTED IN PART. This paper reports that ConvNets exploit high-gamma information in scalp EEG.
  - S5:27 "scalp EEG achieves 40-60 mm resolution with only 64-256 electrodes" -> UNSUPPORTED.
  - S5:27 "attenuate neural signals by 10-100x … due to volume conduction" -> UNSUPPORTED. These are biophysics claims; cite a volume-conduction or EEG-vs-ECoG source instead (e.g. Buzsáki, Anastassiou & Koch 2012 *Nat. Rev. Neurosci.*, or Ball et al. 2009 *NeuroImage*).

## Makin2020
- Exists: yes. Makin, J. G., Moses, D. A. & Chang, E. F. Machine translation of cortical activity to text with an encoder–decoder framework. *Nat. Neurosci.* **23**, 575–582 (2020). DOI: 10.1038/s41593-020-0608-8
- Bib entry errors: none.
- Study facts:
  - Modality: ECoG, "~250 electrodes distributed over peri-Sylvian cortices".
  - Participants: **4** epilepsy patients at UCSF.
  - Task: **overt**, "read sentences aloud".
  - Vocabulary: MOCHA-1 is "50 sentences, about 250 unique words"; the picture descriptions are "30 sentences … about 125 words".
  - Metrics: "Average word error rates across a held-out repeat set are as low as 3%" (best participant); picture descriptions below 8% WER.
  - Decoder: temporal convolution plus encoder RNN plus decoder RNN (seq2seq). Transfer learning across participants was used.
  - Primary empirical study: yes.
- Manuscript claims checked:
  - S3:23 "encoder-decoder … approximately 3 percent WER on a constrained corpus" -> CORRECT.
  - S4:46 "WER approximately 3 percent on constrained corpora, the first genuinely end-to-end brain-to-text system" -> WER CORRECT. "First end-to-end" is the authors' interpretation.
  - S5:13 "3.0% WER on a 250-word vocabulary" -> CORRECT (best participant).
  - APP:81 "ECoG, N=1, 250 words, 3.0" -> N WRONG (4 participants). Its "[8]" resolves to Tricco.
  - SUP:62, row 8: "N 1" -> WRONG (4).
  - SUP:62, row 8: "Attempted speech" -> WRONG (overt, read aloud).
  - SUP:62, row 8: "Generalization None" -> WRONG. The paper uses cross-participant transfer learning: "training certain layers of the network under multiple participants' data".

## Vaswani2017
- Exists: yes. Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł. & Polosukhin, I. Attention is all you need. In *Advances in Neural Information Processing Systems 30* (NeurIPS 2017), 5998–6008 (2017). arXiv:1706.03762
- Bib entry errors: it is entered as @article with journal "arXiv". It should be @inproceedings, NeurIPS 30, pp. 5998–6008.
- Study facts: ML methods paper (machine translation). Not a neural decoding study.
- Manuscript claims checked:
  - S4:50 "replaces recurrence with scaled dot-product self-attention, enabling global dependency modeling … in parallel" -> CORRECT.

## Kostas2021
- Exists: yes. Kostas, D., Aroca-Ouellette, S. & Rudzicz, F. BENDR: using transformers and a contrastive self-supervised learning task to learn from massive amounts of EEG data. *Front. Hum. Neurosci.* **15**, 653659 (2021). DOI: 10.3389/fnhum.2021.653659
- Bib entry errors: none.
- Study facts:
  - Modality: EEG. Pre-trained on the TUEG corpus.
  - Downstream tasks: motor imagery (MMI, BCIC), ERN, P300 and sleep staging. **No speech task.**
  - Best results (Table 2): MMI BAC 86.7, BCIC accuracy 42.6, ERN AUROC 0.65, SSC BAC 0.72, P300 AUROC 0.72.
  - Authors: "these results were not necessarily state of the art … aside from the SSC dataset, consistently here outperforms the fully supervised counterparts".
  - Type: methods paper. Not a speech-decoding study.
- Manuscript claims checked:
  - S4:65 "BENDR achieved 5-15 percent accuracy improvement over supervised baselines across multiple downstream tasks" -> UNSUPPORTED. No such range is stated, and there was no improvement on SSC.
  - Also note that BENDR does not decode speech, so it should not be counted among the "approximately 8 included" SSL speech studies if it is counted there.

## Panachakel2021
- Exists: yes. Panachakel, J. T. & Ramakrishnan, A. G. Decoding covert speech from EEG—a comprehensive review. *Front. Neurosci.* **15**, 642251 (2021). DOI: 10.3389/fnins.2021.642251
- Bib entry errors: none (the title dash is a cosmetic difference).
- Study facts: a **review article** ("This review article puts together all the relevant works … on decoding imagined speech from EEG"). No participants. Not a primary empirical study.
- Manuscript claims checked:
  - S3:57, cited within "The EEG modality accounts for 20 of the 71 included studies … spanning imagined speech classification" -> INCONSISTENT. It is a review, and main.tex:95 states Panachakel 2021 was **excluded** as a review.
  - S5:29 "Early EEG studies (2015-2019) focused primarily on closed-set classification" -> CORRECT as a review-level statement.
  - SUP:84, row 19: "Panachakel et al. 2021, EEG, N=12, Imagined speech, CNN, Acc 78.5%" -> WRONG / APPARENTLY FABRICATED. The 2021 paper is a review with no participants or accuracy, and it contradicts the exclusion in main.tex:95. If a different Panachakel empirical paper was meant, it needs its own bib entry. Rows 50 and 67 (Panachakel 2022 and 2023) should also be verified; they are outside group 1.

## LopezBernal2022
- Exists: yes. Lopez-Bernal, D., Balderas, D., Ponce, P. & Molina, A. A state-of-the-art review of EEG-based imagined speech decoding. *Front. Hum. Neurosci.* **16**, 867281 (2022). DOI: 10.3389/fnhum.2022.867281
- Bib entry errors: none.
- Study facts: a **review** ("we offer a review article that sums the main findings of the most relevant studies on this subject since 2009"). Not empirical.
- Manuscript claims checked:
  - S3:57, cited as among the 20 included EEG studies -> INCONSISTENT. It is a review, excluded per main.tex:95. The citation is acceptable only if the sentence makes clear it is background, not an included study.
  - S5:29 "Early EEG studies focused primarily on closed-set classification" -> CORRECT (the review focuses on small target vocabularies).
  - main.tex:95, "excluded as review" -> CORRECT.

## Rabbani2019
- Exists: yes. Rabbani, Q., Milsap, G. & Crone, N. E. The potential for a speech brain–computer interface using chronic electrocorticography. *Neurotherapeutics* **16**, 144–165 (2019). DOI: 10.1007/s13311-018-00692-2
- Bib entry errors: none.
- Study facts: a review, not empirical.
- Manuscript claims checked:
  - S3:11 "the modality employed determines which parts of this network are accessible" -> CORRECT/SUPPORTED. The abstract says: "neural representations for speech and language are widely distributed … the mesoscopic scale of population activity captured by ECoG … may have distinct advantages".

## Page2021
- Exists: yes. Page, M. J., McKenzie, J. E., Bossuyt, P. M., Boutron, I., Hoffmann, T. C., Mulrow, C. D. et al. The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. *BMJ* **372**, n71 (2021). DOI: 10.1136/bmj.n71
- Bib entry errors: volume **372** is missing.
- Manuscript claims checked:
  - main.tex:89 and APP:162 "reported in accordance with the PRISMA 2020 statement" -> CORRECT use.
  - APP:162 "Full checklist completed and available upon request" -> inconsistent with main.tex:164, which says the checklist is "available in the supplementary materials". NMI requires it to be submitted.

## Shamseer2015
- Exists: yes. Shamseer, L., Moher, D., Clarke, M., Ghersi, D., Liberati, A., Petticrew, M., Shekelle, P., Stewart, L. A. & PRISMA-P Group. Preferred reporting items for systematic review and meta-analysis protocols (PRISMA-P) 2015: elaboration and explanation. *BMJ* **349**, g7647 (2015). DOI: 10.1136/bmj.g7647
- Bib entry errors: none per Crossref/BMJ (vol. 349). PubMed lists it as 350:g7647 (there is also an erratum, BMJ 2016;354:i4086). Either is acceptable.
- Manuscript claims checked:
  - main.tex:89 "PRISMA-P 2015 protocol checklist" -> ACCEPTABLE. The checklist statement itself is Moher, D. et al. *Syst. Rev.* **4**, 1 (2015), DOI 10.1186/2046-4053-4-1; consider citing it alongside.
  - Co-cited Tricco2018 (PRISMA-ScR, a scoping-review extension) is not a PRISMA-P source. That key is outside this group, but the pairing is wrong.

## PROSPERO
- Exists: yes (a register, not a paper). Suggested citation: Centre for Reviews and Dissemination, University of York. PROSPERO: International Prospective Register of Systematic Reviews. https://www.crd.york.ac.uk/PROSPERO/ (funded by NIHR).
- Bib entry errors:
  - The author/publisher should be CRD, University of York (NIHR is the funder).
  - The access date and year are missing.
  - **The key is never \cite'd** (only plain-text mentions at main.tex:63, main.tex:89 and APP:166), so the entry will not appear in the IEEEtran bibliography.
- Manuscript claims checked:
  - main.tex:89 "Registration Number: CRD420261368521" -> UNVERIFIABLE. The record page is JavaScript-rendered and could not be fetched; the ID format is plausible. The authors must confirm the record is public.
  - main.tex:89 also says it was registered "after preliminary scoping", which conflicts with APP:166 "Pre-registered protocol".

## Richardson1995
- Exists: yes. Richardson, W. S., Wilson, M. C., Nishikawa, J. & Hayward, R. S. The well-built clinical question: a key to evidence-based decisions. *ACP J. Club* **123**, A12–A13 (1995). DOI: 10.7326/ACPJC-1995-123-3-A12 (PMID 7582737)
- Bib entry errors: the DOI is missing; everything else is fine.
- Manuscript claims checked:
  - main.tex:93 and APP:168 "PICOS framework \cite{Richardson1995}" -> PARTLY CORRECT. Richardson introduced PICO; the "S" (study design) extension comes from later sources (e.g. the PRISMA 2009 explanation paper, Liberati et al. 2009). Write "PICO(S)" or add a citation for the S.

## Cohen1960
- Exists: yes. Cohen, J. A coefficient of agreement for nominal scales. *Educ. Psychol. Meas.* **20**, 37–46 (1960). DOI: 10.1177/001316446002000104
- Bib entry errors: none.
- Manuscript claims checked:
  - main.tex:99 "Inter-rater reliability was quantified using Cohen's kappa" -> CORRECT.
  - main.tex:99 "κ = 0.78 … 0.85 … with values indicating substantial agreement" -> NOT FROM Cohen1960. The verbal benchmarks come from Landis & Koch (1977, *Biometrics* 33:159–174), under which 0.85 is "almost perfect", not "substantial". Cite Landis & Koch and fix the wording.
  - The κ values themselves are the authors' own data and cannot be checked.
