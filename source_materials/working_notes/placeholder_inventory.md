# PLACEHOLDER Inventory for Systematic Review Paper
**Paper:** Artificial Intelligence for Brain-to-Speech Decoding (2015-2026)  
**Status:** Task 3 - Content Gap Analysis  
**Total PLACEHOLDERs Found:** 9  
**Last Updated:** 2026-07-22

## SUMMARY
- **Total PLACEHOLDERs:** 9
- **Files affected:** 2 (section5_benchmarks.tex, section6_generalization.tex)
- **Total estimated completion time:** 6-8 hours
- **Criticality for Nature submission:** ESSENTIAL (core content gaps)

---

## SECTION 5: PERFORMANCE BENCHMARKS (section5_benchmarks.tex)

### PLACEHOLDER 1: Invasive Systems Detailed Benchmarks
**Location:** `sections/section5_benchmarks.tex`, line 13  
**Context Section:** Subsection "Invasive Systems: ECoG and Intracortical (n=32)"

**What Needs to Be Written:**
Detailed performance benchmarks for invasive systems (ECoG and intracortical microelectrode arrays), organized by task type. Should include:
- Performance ranges for different task types (overt speech, imagined speech, attempted speech)
- Representative performance values (WER percentages, accuracy, WPM)
- Performance by vocabulary size (closed-set vs. open-vocabulary)
- Temporal trajectory (2015-2026 progression)
- Architecture-specific performance (which architectures dominate in invasive systems)

**Current State:** Placeholder exists with stub text citing Willett 2023 (9% WER), Anumanchipalli 2019 (error-free synthesis), and Moses 2021 (78 WPM)

**Completion Strategy:**
1. Extract data from Table 1 (Modality Comparison): Best WER 2.5%-5.0% across invasive modalities
2. Reference Table 6 (Landmark Invasive Systems) in appendices: 25% WER (Herff 2015) → 2.5% WER (Card 2024)
3. Organize by task: Overt speech (most common), imagined, attempted
4. Cite invasive-dominant studies: [2], [3], [5], [8], [26]
5. Include performance trade-offs: closed-set (up to 99% accuracy) vs. open-vocabulary (2.5%-9% WER)

**Estimated Length:** 400-500 words  
**Estimated Time:** 45-60 minutes  
**Priority Tier:** TIER 1 CRITICAL

---

### PLACEHOLDER 2: EEG Systems Detailed Benchmarks
**Location:** `sections/section5_benchmarks.tex`, line 19  
**Context Section:** Subsection "Non-Invasive EEG Systems (n=20)"

**What Needs to Be Written:**
Detailed performance benchmarks for scalp EEG systems, organized by task type. Should include:
- Closed-set classification performance (70%-92.5% accuracy range)
- Open-vocabulary WER performance (35%-45% range)
- Performance degradation from invasive systems (3-5x worse on open-vocabulary)
- Task-specific performance: phoneme vs. word classification
- Subject variability in EEG signal quality

**Current State:** Placeholder exists with stub text providing performance ranges

**Completion Strategy:**
1. Reference Table 7 (Non-Invasive Systems Summary) in appendices
2. Cite EEG-focused studies: [7], [10], [37], [41], [56], [62]
3. Explain SNR (signal-to-noise ratio) limitations in scalp EEG vs. invasive
4. Discuss spatial resolution constraints (40-60 mm vs. invasive 3-10 mm)
5. Highlight growing open-vocabulary EEG work (2022-2026)
6. Include closed-set results: 70%-92.5% accuracy on phoneme/word classification

**Estimated Length:** 350-400 words  
**Estimated Time:** 40-50 minutes  
**Priority Tier:** TIER 2 RECOMMENDED

---

### PLACEHOLDER 3: MEG and fMRI Systems Detailed Benchmarks
**Location:** `sections/section5_benchmarks.tex`, line 25  
**Context Section:** Subsection "MEG and fMRI Systems (n=11)"

**What Needs to Be Written:**
Detailed performance benchmarks for MEG (n=8) and fMRI (n=6) systems, highlighting modality-specific constraints and advantages:
- MEG: Superior temporal resolution (1 ms) but degraded accuracy due to volume conduction
- fMRI: Superior spatial localization (1-3 mm) but extremely poor temporal resolution (2 seconds)
- MEG perceived vs. semantic decoding performance
- fMRI semantic reconstruction capabilities
- Why MEG/fMRI remain research-stage (cost, speed constraints)

**Current State:** Placeholder exists with stub text

**Completion Strategy:**
1. Reference Table 7 (Non-Invasive Systems Summary) appendix section on MEG
2. Cite MEG studies: [23], [29], [48], [49] for perceived/semantic tasks
3. Discuss MEG tradeoff: temporal resolution advantage offset by volume conduction
4. Explain fMRI limitations: 2-second temporal resolution incompatible with real-time decoding
5. Emphasize MEG semantic reconstruction success (100% story ID, >50% text recovery per Table 7)
6. Compare cost and clinical deployability vs. ECoG/intracortical

**Estimated Length:** 300-350 words  
**Estimated Time:** 35-45 minutes  
**Priority Tier:** TIER 3 OPTIONAL

---

### PLACEHOLDER 4: Language Model Integration Underutilization Analysis
**Location:** `sections/section5_benchmarks.tex`, line 124  
**Context Section:** Subsection "Language Model Integration Underutilization"

**What Needs to Be Written:**
Detailed analysis of why language models remain underutilized despite being the single largest driver of WER reduction. Should address:
- Magnitude of LM benefit: 14 percentage-point reduction (Willett 2023: 23%→9% WER)
- Adoption rate: Only 14/71 studies (20%) use LM rescoring
- Technical barriers: Computational infrastructure, real-time latency constraints
- Architectural barriers: Not integrated into training pipelines, used only in post-processing
- Institutional barriers: Expertise required, proprietary LM dependencies
- What infrastructure changes would enable broader adoption

**Current State:** Placeholder exists with context about Willett study

**Completion Strategy:**
1. Quantify LM impact from Table 2: LLM-Integrated category (n=14) shows 9% WER with rescoring
2. Identify barrier categories: (a) computational cost, (b) latency incompatibility, (c) lack of training-time integration
3. Cite LM-integrated papers: [62], [63]
4. Discuss vocabulary mismatch: Brain decoder trained on 50-word vocab vs. LM trained on 125K-word corpus
5. Propose solutions: (a) joint training frameworks, (b) on-device LM optimization, (c) standardized LM benchmarks
6. Connect to clinical deployment: Real-time constraints differ between laboratory and clinical settings

**Estimated Length:** 500-600 words  
**Estimated Time:** 60-75 minutes  
**Priority Tier:** TIER 1 CRITICAL

---

## SECTION 6: GENERALIZATION EVIDENCE (section6_generalization.tex)

### PLACEHOLDER 5: Cross-Participant Generalization Detailed Analysis
**Location:** `sections/section6_generalization.tex`, line 12  
**Context Section:** Subsection "The Generalization Gap: A Quantitative Overview" (leading into "Cross-Participant Generalization")

**What Needs to Be Written:**
Detailed analysis of the 13 cross-participant studies, including:
- Transfer learning approaches used (manifold alignment, domain adaptation, shared representations)
- Performance retention rates (50%-80% vs. single-participant baseline)
- Which architectures enable best transfer (Transformers vs. RNN/LSTM)
- Participant-invariant neural features identified across studies
- Domain adaptation strategies effective in brain-to-speech
- Performance degradation patterns when deploying on new participants
- Dataset size requirements for successful transfer (Table 8: N=8-28 participants)

**Current State:** Placeholder exists with bulleted guidance

**Completion Strategy:**
1. Reference Table 8 (Cross-Participant Generalization Detail) appendix: Peterson et al. 2021 [65], Singh et al. 2025 [37], deBorman et al. 2024 [66]
2. Cite cross-participant studies: [65], [37], [66] as primary representatives
3. Discuss manifold alignment: How Peterson et al. aligns neural manifolds across participants
4. Explain cross-site harmonization: Singh et al. approach to distributed sEEG networks
5. Cover domain adaptation: deBorman et al. event detection approach
6. Address dataset requirements: Why N=8-28 participants needed for transfer learning
7. Quantify performance loss: Typical 50%-80% retention vs. single-participant models
8. Discuss clinical implications: Transfer learning critical for deployment but requires large multi-site datasets

**Estimated Length:** 600-700 words  
**Estimated Time:** 60-75 minutes  
**Priority Tier:** TIER 1 CRITICAL

---

### PLACEHOLDER 6: Cross-Participant Representative Case Studies
**Location:** `sections/section6_generalization.tex`, line 22  
**Context Section:** Subsection "Cross-Participant Generalization (n=13)"

**What Needs to Be Written:**
Representative case studies from the 13 cross-participant studies. Should provide:
- 2-3 detailed examples of successful cross-participant transfer
- Methodological details specific to each example
- Performance metrics and comparison to single-participant baseline
- What made these studies succeed where most others fail
- Generalization scope: Was it 2-participant pairs? 28-participant consortium? Clinical site transfer?

**Current State:** Placeholder only

**Completion Strategy:**
1. Use Table 8 primary examples: Peterson 2021 [65], Singh 2025 [37], deBorman 2024 [66]
2. Peterson et al. 2021: Manifold alignment across 28 participants
   - Method: Neural manifold alignment between participants
   - Performance: 60-80% vs. baseline
   - Novel aspect: Participant-invariant features
3. Singh et al. 2025: Distributed sEEG network (25 participants across sites)
   - Method: Cross-site harmonization, group decoder
   - Performance: 50-75% vs. individual performance
   - Clinical relevance: Multi-site deployment
4. deBorman et al. 2024: ECoG event detection (8 participants)
   - Method: Domain adaptation approach
   - Performance: 70% accuracy vs. baseline
   - Simpler task: Event detection vs. continuous decoding
5. Frame why these succeeded: Participant-invariant features, proper cross-validation, held-out test sets

**Estimated Length:** 400-500 words  
**Estimated Time:** 45-60 minutes  
**Priority Tier:** TIER 1 CRITICAL

---

### PLACEHOLDER 7: Cross-Session Generalization Analysis
**Location:** `sections/section6_generalization.tex`, line 28  
**Context Section:** Subsection "Cross-Session Generalization (n=2)"

**What Needs to Be Written:**
Detailed analysis of the two studies showing cross-session generalization, and mechanisms for performance retention:
- Study 1: Likely Ye et al. 2025 - what methods maintained stability?
- Study 2: Likely Yuan et al. 2024 - what approaches prevented signal drift?
- Performance retention mechanisms: Recalibration, adaptive learning, periodic re-training
- Neural signal drift: Why performance degrades over time (electrode movement, inflammation, neural plasticity)
- Time scales: Days? Weeks? Months? How long before recalibration needed?
- Clinical implications: What recalibration schedule would be feasible?

**Current State:** Placeholder exists; context text mentions "70-90% retention" but lacks detail

**Completion Strategy:**
1. Identify two studies: Ye et al. 2025 and Yuan et al. 2024 (both appear in section6_generalization line 8 citations [Ye2025,Yuan2024])
2. For each study: Extract (a) follow-up duration, (b) performance retention rate, (c) recalibration approach
3. Discuss neural signal drift mechanisms: Electrode micromotion, glial scarring, neural plasticity
4. Compare retention approaches: Recalibration (retraining subset of model), adaptive learning (online updates), periodic re-training
5. Quantify timescale: Stability evidence up to 1 month (from section 6.4 implications)
6. Clinical implications: Daily recalibration likely required for deployed systems
7. Gap identification: Only 2 studies; long-term (>6 months) stability unknown

**Estimated Length:** 350-400 words  
**Estimated Time:** 40-50 minutes  
**Priority Tier:** TIER 2 RECOMMENDED

---

### PLACEHOLDER 8: Cross-Language Generalization Analysis
**Location:** `sections/section6_generalization.tex`, line 34  
**Context Section:** Subsection "Cross-Language Generalization (n=2)"

**What Needs to Be Written:**
Detailed analysis of cross-language transfer challenges and successes in the two studies demonstrating cross-language generalization:
- Study 1: d'Ascoli et al. 2025 - CNN-Transformer trained on 723 participants across English, French, Dutch
  - Results: >40% word decoding accuracy in all three languages (above-chance)
  - Method: Large multi-language dataset, Transformer architecture
- Study 2: Li et al. 2022 - HD-sEMG encoder-decoder extended from Mandarin to English
  - Results: 80% of single-language accuracy (strong phoneme-motor mapping transfer)
  - Method: HD-sEMG (peripheral), phoneme-level features
- Why cross-language transfer is difficult (phoneme inventories differ, motor cortex language-specific organization)
- Implications for linguistic universality vs. language-specificity of motor planning

**Current State:** Placeholder exists; section 6.3 explicitly notes only 2 studies with 2.8% (n=2)

**Completion Strategy:**
1. Cite cross-language studies: [45], [54] mentioned in section5 for language diversity
2. Identify d'Ascoli et al. 2025: 723-participant multi-language study
   - Method: CNN-Transformer architecture
   - Data: English, French, Dutch
   - Results: >40% above-chance performance
   - Insight: Large dataset + Transformer enables language transfer
3. Identify Li et al. 2022: HD-sEMG Mandarin→English transfer
   - Method: Encoder-decoder architecture
   - Modality: Peripheral (not cortical)
   - Results: 80% retention when transferring languages
   - Insight: Motor-phoneme mapping partially language-invariant
4. Discuss phoneme inventory differences: How they affect transfer
5. Discuss cortical language organization: Is motor planning universal across languages?
6. Gap: Only 2 studies (2.8%); commercial products don't demonstrate this

**Estimated Length:** 400-450 words  
**Estimated Time:** 45-60 minutes  
**Priority Tier:** TIER 3 OPTIONAL

---

### PLACEHOLDER 9: Cross-Modal Generalization Analysis
**Location:** `sections/section6_generalization.tex`, line 40  
**Context Section:** Subsection "Cross-Modal Generalization (n=5)"

**What Needs to Be Written:**
Analysis of why inter-modality transfer is challenging and where it succeeds among the 5 studies attempting cross-modal generalization. Should address:
- Why inter-modality transfer fails: Different spatial resolutions (intracortical 10μm vs. ECoG 4-10mm), temporal characteristics, signal-to-noise ratios
- Where it succeeds: What modality pairs show partial transfer?
- Domain adaptation strategies specific to modality differences
- Feature alignment challenges across modalities
- Performance retention rates for cross-modal transfer
- Clinical implications: Can you train on invasive data and deploy on non-invasive? Likely not.

**Current State:** Placeholder exists; section 6.4 briefly mentions domain adaptation, feature alignment, multi-modal encoders

**Completion Strategy:**
1. Identify 5 cross-modal studies (not explicitly named in provided sections; likely in full paper references)
2. Discuss modality mismatch problem:
   - Spatial resolution gap: 10 μm (intracortical) vs. 40-60 mm (scalp EEG) = 1000x difference
   - Temporal characteristics: Similar (1 ms) but different noise profiles
   - SNR variation: Invasive 10-100x higher SNR than non-invasive
3. Discuss which combinations attempted:
   - ECoG → EEG (more common than intracortical → EEG)
   - fMRI → invasive (very rare, temporal mismatch too severe)
   - sEMG → cortical (different signal source entirely)
4. Feature alignment strategies: What features transfer across modalities?
5. Performance retention: Typically 50-70% for modality pairs with similar signal characteristics
6. Gap: Cross-modal transfer remains largely unsolved; most clinical deployments stick to single modality
7. Implication: Modularity and cross-modality transfer not practical research direction for near-term deployment

**Estimated Length:** 350-400 words  
**Estimated Time:** 40-50 minutes  
**Priority Tier:** TIER 3 OPTIONAL

---

---

## COMPLETION TIMELINE AND PRIORITY STRUCTURE

### TIER 1 - CRITICAL (Essential for review acceptance)
**Total Estimated Time:** 3-4 hours
1. **PLACEHOLDER 1** - Invasive Systems Benchmarks (60 min)
2. **PLACEHOLDER 4** - Language Model Underutilization (70 min)
3. **PLACEHOLDER 5** - Cross-Participant Analysis (70 min)
4. **PLACEHOLDER 6** - Cross-Participant Case Studies (60 min)

**Rationale:** These four sections address the paper's highest-priority findings: (1) invasive systems achieving landmark performance, (2) underutilized LM potential, (3) cross-participant generalization bottleneck, (4) evidence supporting deployment scenarios.

### TIER 2 - RECOMMENDED (Strengthens narrative, improves reviewer reception)
**Total Estimated Time:** 1.5-2 hours
5. **PLACEHOLDER 2** - EEG Systems Benchmarks (45 min)
6. **PLACEHOLDER 7** - Cross-Session Analysis (45 min)

**Rationale:** Completes the modality landscape and explains why long-term clinical stability remains uncertain. Adds critical context for clinical deployment discussion.

### TIER 3 - OPTIONAL (Completes paper comprehensiveness)
**Total Estimated Time:** 2-2.5 hours
7. **PLACEHOLDER 3** - MEG/fMRI Benchmarks (40 min)
8. **PLACEHOLDER 8** - Cross-Language Analysis (50 min)
9. **PLACEHOLDER 9** - Cross-Modal Analysis (45 min)

**Rationale:** These address research-stage modalities and transfer problems. While thorough, they're less critical to core clinical translation narrative than Tiers 1-2.

---

## WRITING GUIDELINES FOR COMPLETION

### Style and Tone
- Match existing paper voice: Technical, precise, evidence-based, no overclaiming
- Cite evidence: Every benchmark claim should reference a table or specific study [#]
- Quantify findings: Use ranges, percentages, participant counts (e.g., "50-80% performance retention" not "some performance loss")
- Highlight gaps: Explicitly note where evidence is limited (e.g., "Only 2 studies evaluate cross-session stability")

### Citation Integration
- Use existing citations from references.bib [1]-[73]
- Tables 1-8 contain citation references in [Ref] columns; use these as starting points
- For each subsection, ensure at least 3-5 citations supporting claims
- Avoid: "The literature shows..." (too vague); prefer "Three studies using manifold alignment [65,37,66] achieved 50-80% cross-participant transfer"

### Data Sourcing
- **Tables 1-5** (main paper): Provide high-level summary data
- **Tables 6-8** (appendices): Provide detailed study-level breakdown for writing detailed analyses
- **Table 2** shows architecture-specific performance; use to discuss what enables invasive/EEG performance differences
- **Section 3-4** (written sections) provide context on modalities and architectures

### Common Pitfalls to Avoid
1. **Overclaiming:** Don't say "systems achieve X performance" if only 1-2 studies show it. Say "Landmark results include..."
2. **Vague metrics:** Always specify vocabulary size when citing WER. "2.5% WER" is meaningless without "on 50-word vocabulary"
3. **Ignoring gaps:** If only 2/71 studies address something, lead with that scarcity. It's a key finding, not a failure.
4. **Disconnected facts:** Connect each benchmark to its constraints. Why does EEG achieve 35-45% WER? Because of SNR/resolution limitations.
5. **Missing clinical angle:** Every technical finding should connect to clinical deployment feasibility

---

## FILE LOCATIONS FOR REFERENCE

**Main Paper Structure:**
- `main.tex` - Master document, bibliography style IEEEtran, 73 references
- `sections/section5_benchmarks.tex` - Contains PLACEHOLDERs 1-4
- `sections/section6_generalization.tex` - Contains PLACEHOLDERs 5-9
- `sections/figures_and_tables.tex` - Tables 1-5 with all citation data

**Appendix Data Tables:**
- `sections/appendices.tex` - Tables 6-8 with detailed study-level data
  - Table 6: Landmark Invasive Systems (Herff 2015 - Card 2024)
  - Table 7: Non-Invasive Systems Summary (EEG, MEG)
  - Table 8: Cross-Participant Generalization Detail (Peterson, Singh, deBorman)

**Bibliography:**
- `references.bib` - 73 complete references with DOI fields in IEEE format

---

## CHECKLIST FOR COMPLETION

Use this checklist as you complete each PLACEHOLDER section:

- [ ] Section written and reaches target word count
- [ ] All claims cite specific references [#] or tables
- [ ] Vocabulary sizes specified for all WER figures
- [ ] Task types explicitly stated where relevant
- [ ] Performance metrics include ranges with units
- [ ] Participant counts and N values clearly reported
- [ ] Clinical implications or deployment constraints mentioned
- [ ] Gaps in literature explicitly noted (e.g., "Only 2 studies...")
- [ ] Technical approaches explained (not just results cited)
- [ ] Connection to systematic review narrative clear (not standalone facts)
- [ ] Proofreading complete: Grammar, citations formatted [#], no placeholder text remaining

---

**Status:** All 9 PLACEHOLDERs identified, catalogued, and ready for content completion.  
**Next Step:** Begin with TIER 1 sections to ensure paper acceptance priority.

