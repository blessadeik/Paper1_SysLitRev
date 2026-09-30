# Overleaf project: AI for Brain-to-Speech Decoding (Systematic Review)

Upload: Overleaf > New Project > Upload Project > select `Paper1_overleaf.zip`
(one level up from this folder). Main document: `main.tex`. Compiler: pdfLaTeX
(Overleaf default). Bibliography: BibTeX with `IEEEtran` style (built into Overleaf).

```
main.tex                     preamble, title, abstract, Sec 1-2, limitations, conclusions
references.bib               88 cited entries (+2 uncited: PROSPERO, IntracorticalRecording2017)
sections/
  figures_and_tables.tex     Figures 1-7 and Tables 1-5
  section3_modalities.tex    Sec 3
  section4_architectures.tex Sec 4
  section5_benchmarks.tex    Sec 5
  section6_generalization.tex Sec 6
  section7_discussion.tex    Sec 7
  appendices.tex             Appendices (after bibliography)
figures/
  fig1_prisma_flow.png            Fig 1  PRISMA 2020 flow diagram
  fig2_study_distribution.png     Fig 2  studies by modality and year
  fig3_architecture_evolution.png Fig 3  AI architecture eras
  fig4_wer_trajectory.png         Fig 4  WER trajectory, landmark studies
  fig5_modality_task_heatmap.png  Fig 5  modality x task heatmap
  fig6_modality_comparison.png    Fig 6  spatial vs temporal resolution
  fig7_modality_schematics.png    Fig 7  recording modality schematics
supplementary/
  supplement_table_s1.tex    Standalone document (not part of main.tex). To compile it
                             on Overleaf: Menu > Main document > supplementary/supplement_table_s1.tex
  supplement_table_s1.pdf    Pre-compiled copy of Table S1
```

Figures 2-7 were extracted at full embedded resolution from the previously compiled
`main.pdf` and flattened onto a white background. Replace them with the original
source files (same filenames) if you have them.
