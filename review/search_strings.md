# Database search strings (registered strategy)

Translated from the PubMed string registered with PROSPERO (CRD420261368521, protocol section "COMPLETE PUBMED SEARCH STRING"). The three concept blocks and their terms are unchanged; only the field syntax differs per database.

**Databases searched:** PubMed, Scopus, IEEE Xplore, arXiv (searches run 1 October 2026). Web of Science dropped (see section 3).

**Window:** 1 January 2015 to 13 April 2026 (registered). **Language:** English (registered).

## How to record the run (needed for the PRISMA 2020 diagram)

For each database, save:
1. The exact string pasted.
2. The date you ran it.
3. The hit count.
4. The full export (RIS, or CSV with title, abstract, authors, year, DOI).

Then import all exports into one library (Zotero, Rayyan or Covidence), deduplicate, and record:
- the duplicates removed;
- the records screened by each reviewer;
- each reviewer's include, exclude or uncertain decision per record;
- full-text reasons for exclusion;
- any records not retrieved.

Cohen's kappa is computed from the two reviewers' independent decisions on the same records.

If you re-run the search now, report the date you actually ran it in the Methods. Keep the 13 April 2026 publication-date cap so the eligible window matches the protocol.

## 1. PubMed (MEDLINE): registered string, verbatim

```
(
  ("brain-computer interface"[Title/Abstract] OR
  "brain computer interface"[Title/Abstract] OR
  "BCI"[Title/Abstract] OR
  "brain-to-speech"[Title/Abstract] OR
  "neural speech decoding"[Title/Abstract] OR
  "speech neuroprosthesis"[Title/Abstract] OR
  "neural speech prosthesis"[Title/Abstract] OR
  "electrocorticography"[Title/Abstract] OR
  "ECoG"[Title/Abstract] OR
  "intracortical"[Title/Abstract] OR
  "Utah array"[Title/Abstract] OR
  "electroencephalography"[Title/Abstract] OR
  "EEG"[Title/Abstract] OR
  "magnetoencephalography"[Title/Abstract] OR
  "MEG"[Title/Abstract] OR
  "functional MRI"[Title/Abstract] OR
  "fMRI"[Title/Abstract] OR
  "fNIRS"[Title/Abstract] OR
  "sEEG"[Title/Abstract] OR
  "stereotactic EEG"[Title/Abstract] OR
  "neural recording"[Title/Abstract] OR
  "intracranial EEG"[Title/Abstract] OR
  "iEEG"[Title/Abstract] OR
  "Brain-Computer Interfaces"[MeSH Terms] OR
  "Electroencephalography"[MeSH Terms] OR
  "Magnetoencephalography"[MeSH Terms] OR
  "Magnetic Resonance Imaging, Functional"[MeSH Terms])
)
AND
(
  ("speech decoding"[Title/Abstract] OR
  "speech synthesis"[Title/Abstract] OR
  "speech reconstruction"[Title/Abstract] OR
  "speech restoration"[Title/Abstract] OR
  "imagined speech"[Title/Abstract] OR
  "covert speech"[Title/Abstract] OR
  "inner speech"[Title/Abstract] OR
  "silent speech"[Title/Abstract] OR
  "attempted speech"[Title/Abstract] OR
  "perceived speech"[Title/Abstract] OR
  "speech neuroprosthesis"[Title/Abstract] OR
  "augmentative and alternative communication"[Title/Abstract] OR
  "AAC"[Title/Abstract] OR
  "neural speech"[Title/Abstract] OR
  "voice synthesis"[Title/Abstract] OR
  "Speech"[MeSH Terms] OR
  "Communication Aids for Disabled"[MeSH Terms] OR
  "Speech Production Measurement"[MeSH Terms])
)
AND
(
  ("deep learning"[Title/Abstract] OR
  "machine learning"[Title/Abstract] OR
  "neural network"[Title/Abstract] OR
  "convolutional neural network"[Title/Abstract] OR
  "CNN"[Title/Abstract] OR
  "recurrent neural network"[Title/Abstract] OR
  "LSTM"[Title/Abstract] OR
  "long short-term memory"[Title/Abstract] OR
  "transformer"[Title/Abstract] OR
  "self-supervised learning"[Title/Abstract] OR
  "transfer learning"[Title/Abstract] OR
  "foundation model"[Title/Abstract] OR
  "large language model"[Title/Abstract] OR
  "LLM"[Title/Abstract] OR
  "encoder-decoder"[Title/Abstract] OR
  "sequence-to-sequence"[Title/Abstract] OR
  "artificial intelligence"[Title/Abstract] OR
  "deep neural network"[Title/Abstract] OR
  "generative model"[Title/Abstract] OR
  "self supervised"[Title/Abstract] OR
  "pre-trained model"[Title/Abstract] OR
  "Deep Learning"[MeSH Terms] OR
  "Neural Networks, Computer"[MeSH Terms] OR
  "Machine Learning"[MeSH Terms])
)
AND
(
  "2015/01/01"[Date - Publication] : "2026/04/13"[Date - Publication]
)
AND
(
  "humans"[MeSH Terms]
)
AND
(
  "English"[Language]
)
```

## 2. Scopus (Advanced search)

```
TITLE-ABS-KEY(("brain-computer interface" OR "brain computer interface" OR "BCI" OR "brain-to-speech" OR "neural speech decoding" OR "speech neuroprosthesis" OR "neural speech prosthesis" OR "electrocorticography" OR "ECoG" OR "intracortical" OR "Utah array" OR "electroencephalography" OR "EEG" OR "magnetoencephalography" OR "MEG" OR "functional MRI" OR "fMRI" OR "fNIRS" OR "sEEG" OR "stereotactic EEG" OR "neural recording" OR "intracranial EEG" OR "iEEG") AND ("speech decoding" OR "speech synthesis" OR "speech reconstruction" OR "speech restoration" OR "imagined speech" OR "covert speech" OR "inner speech" OR "silent speech" OR "attempted speech" OR "perceived speech" OR "speech neuroprosthesis" OR "augmentative and alternative communication" OR "AAC" OR "neural speech" OR "voice synthesis") AND ("deep learning" OR "machine learning" OR "neural network" OR "convolutional neural network" OR "CNN" OR "recurrent neural network" OR "LSTM" OR "long short-term memory" OR "transformer" OR "self-supervised learning" OR "self supervised" OR "transfer learning" OR "foundation model" OR "large language model" OR "LLM" OR "encoder-decoder" OR "sequence-to-sequence" OR "artificial intelligence" OR "deep neural network" OR "generative model" OR "pre-trained model")) AND PUBYEAR > 2014 AND PUBYEAR < 2027 AND LANGUAGE(english) AND ORIG-LOAD-DATE BEF 20260414
```

`ORIG-LOAD-DATE BEF 20260414` keeps only records loaded before 14 April 2026. If your Scopus rejects it, drop that clause and remove anything published after 13 April 2026 during screening.

## 3. Web of Science Core Collection: NOT SEARCHED (protocol deviation)

Web of Science was dropped on 1 October 2026 because the review team did not have institutional access. Record this as a PROSPERO amendment, and report it in the Methods and Limitations. The string below is kept for the record only.

```
TS=("brain-computer interface" OR "brain computer interface" OR "BCI" OR "brain-to-speech" OR "neural speech decoding" OR "speech neuroprosthesis" OR "neural speech prosthesis" OR "electrocorticography" OR "ECoG" OR "intracortical" OR "Utah array" OR "electroencephalography" OR "EEG" OR "magnetoencephalography" OR "MEG" OR "functional MRI" OR "fMRI" OR "fNIRS" OR "sEEG" OR "stereotactic EEG" OR "neural recording" OR "intracranial EEG" OR "iEEG") AND TS=("speech decoding" OR "speech synthesis" OR "speech reconstruction" OR "speech restoration" OR "imagined speech" OR "covert speech" OR "inner speech" OR "silent speech" OR "attempted speech" OR "perceived speech" OR "speech neuroprosthesis" OR "augmentative and alternative communication" OR "AAC" OR "neural speech" OR "voice synthesis") AND TS=("deep learning" OR "machine learning" OR "neural network" OR "convolutional neural network" OR "CNN" OR "recurrent neural network" OR "LSTM" OR "long short-term memory" OR "transformer" OR "self-supervised learning" OR "self supervised" OR "transfer learning" OR "foundation model" OR "large language model" OR "LLM" OR "encoder-decoder" OR "sequence-to-sequence" OR "artificial intelligence" OR "deep neural network" OR "generative model" OR "pre-trained model")
```

## 4. IEEE Xplore (Command Search)

```
("All Metadata":"brain-computer interface" OR "All Metadata":"brain computer interface" OR "All Metadata":"BCI" OR "All Metadata":"brain-to-speech" OR "All Metadata":"neural speech decoding" OR "All Metadata":"speech neuroprosthesis" OR "All Metadata":"neural speech prosthesis" OR "All Metadata":"electrocorticography" OR "All Metadata":"ECoG" OR "All Metadata":"intracortical" OR "All Metadata":"Utah array" OR "All Metadata":"electroencephalography" OR "All Metadata":"EEG" OR "All Metadata":"magnetoencephalography" OR "All Metadata":"MEG" OR "All Metadata":"functional MRI" OR "All Metadata":"fMRI" OR "All Metadata":"fNIRS" OR "All Metadata":"sEEG" OR "All Metadata":"stereotactic EEG" OR "All Metadata":"neural recording" OR "All Metadata":"intracranial EEG" OR "All Metadata":"iEEG") AND ("All Metadata":"speech decoding" OR "All Metadata":"speech synthesis" OR "All Metadata":"speech reconstruction" OR "All Metadata":"speech restoration" OR "All Metadata":"imagined speech" OR "All Metadata":"covert speech" OR "All Metadata":"inner speech" OR "All Metadata":"silent speech" OR "All Metadata":"attempted speech" OR "All Metadata":"perceived speech" OR "All Metadata":"speech neuroprosthesis" OR "All Metadata":"augmentative and alternative communication" OR "All Metadata":"AAC" OR "All Metadata":"neural speech" OR "All Metadata":"voice synthesis") AND ("All Metadata":"deep learning" OR "All Metadata":"machine learning" OR "All Metadata":"neural network" OR "All Metadata":"convolutional neural network" OR "All Metadata":"CNN" OR "All Metadata":"recurrent neural network" OR "All Metadata":"LSTM" OR "All Metadata":"long short-term memory" OR "All Metadata":"transformer" OR "All Metadata":"self-supervised learning" OR "All Metadata":"self supervised" OR "All Metadata":"transfer learning" OR "All Metadata":"foundation model" OR "All Metadata":"large language model" OR "All Metadata":"LLM" OR "All Metadata":"encoder-decoder" OR "All Metadata":"sequence-to-sequence" OR "All Metadata":"artificial intelligence" OR "All Metadata":"deep neural network" OR "All Metadata":"generative model" OR "All Metadata":"pre-trained model")
```

Filters: Year 2015 to 2026; remove anything after 13 April 2026 at screening. IEEE Xplore limits the number of terms in one command search. If the string is rejected, split Block 3 (the AI terms) into two or three parts, run and export each part, and let deduplication merge them. Report it as one IEEE Xplore search with N unique records.

## 5. arXiv (API query; categories as registered: cs.HC, eess.AS, q-bio.NC)

```
((abs:"brain-computer interface" OR abs:"brain computer interface" OR abs:"BCI" OR abs:"brain-to-speech" OR abs:"neural speech decoding" OR abs:"speech neuroprosthesis" OR abs:"neural speech prosthesis" OR abs:"electrocorticography" OR abs:"ECoG" OR abs:"intracortical" OR abs:"Utah array" OR abs:"electroencephalography" OR abs:"EEG" OR abs:"magnetoencephalography" OR abs:"MEG" OR abs:"functional MRI" OR abs:"fMRI" OR abs:"fNIRS" OR abs:"sEEG" OR abs:"stereotactic EEG" OR abs:"neural recording" OR abs:"intracranial EEG" OR abs:"iEEG") AND (abs:"speech decoding" OR abs:"speech synthesis" OR abs:"speech reconstruction" OR abs:"speech restoration" OR abs:"imagined speech" OR abs:"covert speech" OR abs:"inner speech" OR abs:"silent speech" OR abs:"attempted speech" OR abs:"perceived speech" OR abs:"speech neuroprosthesis" OR abs:"augmentative and alternative communication" OR abs:"AAC" OR abs:"neural speech" OR abs:"voice synthesis") AND (abs:"deep learning" OR abs:"machine learning" OR abs:"neural network" OR abs:"convolutional neural network" OR abs:"CNN" OR abs:"recurrent neural network" OR abs:"LSTM" OR abs:"long short-term memory" OR abs:"transformer" OR abs:"self-supervised learning" OR abs:"self supervised" OR abs:"transfer learning" OR abs:"foundation model" OR abs:"large language model" OR abs:"LLM" OR abs:"encoder-decoder" OR abs:"sequence-to-sequence" OR abs:"artificial intelligence" OR abs:"deep neural network" OR abs:"generative model" OR abs:"pre-trained model")) AND (cat:cs.HC OR cat:eess.AS OR cat:q-bio.NC) AND submittedDate:[201501010000 TO 202604132359]
```

**Tested link:** [search_exports/arxiv_registered_query_URL.txt](search_exports/arxiv_registered_query_URL.txt) contains the full API URL, already encoded. Paste it into a browser and it returns the results as XML (the record count is in `<opensearch:totalResults>`). The arXiv web form cannot handle this much nesting, so use the API.

**Run on 1 October 2026:** 53 records with the registered categories, saved as [arxiv_registered_categories_run2026-10-01.ris](search_exports/arxiv_registered_categories_run2026-10-01.ris) for import into Zotero or Rayyan (CSV alongside). Widening to cs.LG, cs.CL, cs.AI, eess.SP, cs.NE and cs.SD gives 74 records (`arxiv_broader_*`). The broader run is a deviation from the protocol; use it only if you report it as one.

Four included arXiv studies are not returned by either version: DeWave (2309.14030), BrainBERT (2302.14367), Yuan & Makin (2405.18639) and Yin et al. (2405.11597). Their abstracts lack the Block 2 speech terms. Report them as identified through other methods (citation chaining).

## Notes on the registered strategy

- **sEMG is not in Block 1.** The surface-EMG silent-speech studies in the register (studies 65 to 68) would not be found by the registered database search. If they stay in the review, report how they were identified (for example, citation chaining). Also state that peripheral (non-neural) signals were included, and record this as a deviation from the protocol.
- **arXiv categories.** The registered categories are cs.HC, eess.AS and q-bio.NC. An earlier Methods draft listed cs.LG, cs.NE, eess.SP and q-bio.NC. Use the registered set, or report the change as a deviation.
- **Supplementary searches** (citation chaining of 15 landmark papers, hand-searching of key journals, conference proceedings) must be counted separately: records identified, screened and included. PRISMA 2020 reports these in its right-hand "Identification of studies via other methods" column.
