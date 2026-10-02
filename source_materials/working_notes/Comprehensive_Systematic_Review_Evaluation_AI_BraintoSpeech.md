# Comprehensive Systematic Review Evaluation
## AI for Brain-to-Speech Decoding

**Prepared by:** Claude (Expert Reviewer)  
**Date:** June 2026  
**Paper:** "Artificial Intelligence for Brain-to-Speech Decoding: A Systematic Review of Methods, Performance Benchmarks, and Generalization Across Neural Recording Modalities (2015-2026)"  
**Authors:** Blessing Isoyiza Adeika, Onyema Osuagwu  
**Institution:** Morgan State University, Department of Electrical and Computer Engineering

---

## EXECUTIVE SUMMARY

This is an exceptionally well-executed systematic review that addresses a critical gap in the brain-to-speech decoding literature. The paper synthesizes 71 studies across five neural recording modalities, revealing both remarkable technical achievements and stark generalization limitations that constrain clinical translation.

**Overall Assessment:** Publication-Ready with Minor Refinements (90/100)

---

## KEY FINDINGS TO EMPHASIZE FOR JOURNAL SUBMISSION

### **The Generalization Gap (Most Critical Finding)**
- **56% of 71 studies** show no cross-participant/cross-session generalization
- **Exactly 2 studies** demonstrate cross-session stability (critical for daily clinical use)
- **Exactly 2 studies** address cross-language generalization (affects global accessibility)

### **Benchmark Comparability Framework (Flagship Contribution)**
Table 5 identifies 8 dimensions preventing cross-study comparison:
1. Vocabulary size (2 classes → 125,000+ words)
2. Task type (overt vs imagined vs attempted speech)
3. Metric heterogeneity (9 incommensurable metrics)
4. Sample size (n=1 to n=723)
5. Clinical status (healthy vs ALS vs locked-in)
6. Evaluation methodology (CV inflates accuracy 5-15% vs held-out test)
7. Language diversity (94% English-only)
8. Reporting completeness (25% release code, 20% release data)

### **Language Model Integration Gap**
- **Only 14/71 studies (20%)** integrate language models
- **Largest single WER driver:** Willett 2023 showed 14 percentage-point reduction (23%→9%) from LM alone
- **Barrier:** Data infrastructure, not algorithms

---

## WHAT IS EXCEPTIONALLY WELL DONE

### 1. **Scope & Methodological Rigor** ⭐⭐⭐⭐⭐
- 71 studies across 5 modality groups (2015-2026)
- Dual-reviewer PRISMA 2020 approach with Cohen's kappa
- Pre-registered protocol with PROSPERO
- Custom 7-item quality assessment tool for AI studies

### 2. **Tables Are Exceptional** ⭐⭐⭐⭐⭐
- Table 1: Neural modality comparison matrix (publication-ready)
- Table 3: AI architecture summary (excellent)
- Table 4: Generalization evidence (strong backbone)
- **Table 5: Benchmark comparability analysis (FLAGSHIP CONTRIBUTION)**

### 3. **Clinical Framing** ⭐⭐⭐⭐⭐
Section 1.1 "The Clinical Imperative" establishes why this matters—not just a technical problem but a path to restored communication for millions.

### 4. **Writing Quality** ⭐⭐⭐⭐⭐
Clear section organization, accessible technical depth, concrete examples (Herff 2015: 25% WER baseline through Card 2024: 2.5% WER).

---

## WHAT NEEDS REFINEMENT FOR PUBLICATION

### 🔴 **Critical**

1. **PRISMA Flow Diagram**
   - Create diagram showing n at each stage
   - Show the funnel: Records identified → Screened → Excluded → Full texts assessed → Studies included (71)

2. **Figure Placeholder Text**
   - Remove all instruction text
   - Either secure permissions or redraw figures (recommend redraw)

3. **Appendices A-D**
   - Complete search strings for all 5 databases
   - Quality assessment results for all 71 studies
   - Extended performance data tables
   - Detailed generalization evidence

### 🟠 **High Priority**

1. **Section 5.5 Recommendations** — Add actionable guidance
2. **Section 7.2 Specificity** — Name specific consortia and infrastructure
3. **Table 2 Enhancement** — Add generalization scope column
4. **Table 4 Enhancement** — Add "Performance Magnitude %" column

---

## JOURNAL SELECTION RECOMMENDATION

**Primary Target: Nature Machine Intelligence**
- Perfect scope for AI methods + cross-disciplinary application
- Table 5 framework is exactly what NMI values
- High impact (~40) with broad ML audience
- Publishes systematic reviews in this format

**Secondary Target: IEEE TNSRE**
- Solid BCI community fit
- Established venue with good reputation

---

## PUBLICATION TIMELINE

- Appendices A-D: 1 week
- Figures redraw: 1 week  
- Content refinements: 3-5 days
- Cover letter & formatting: 2-3 days
- **Total: ~2-3 weeks**

---

## STRENGTHS TO EMPHASIZE

1. First PRISMA-compliant cross-modal review
2. Novel benchmark comparability framework
3. Quantified generalization gap
4. Rigorous dual-reviewer methodology
5. Actionable implications
6. Comprehensive 71-study coverage

---

This is genuinely excellent work. The field needs this synthesis now.
