# Analysis outputs — chemo curls social listening study

Generated deliverables for the research letter. Corpus n = 1,467 posts
(two-model consensus screen), 16 subreddits.

## manuscript/
- `chemo_curls_letter.tex` — research letter, 596 words (Introduction unchanged
  from the prior draft). One table, one figure, one supplemental figure.
  Figures are referenced by artifact marker; to compile locally, place the PNGs
  from `figures/` alongside the .tex and change the two `\includegraphics`
  paths to `fig1_comention_heatmap.png` and `efig1_umap.png`.

## figures/
- `fig1_comention_heatmap.png` — Figure 1. Phenotype mention rate by therapy
  class. Rows = therapy class, columns = phenotype. Single scale, 5-point bins,
  color steps widened below 20% so low-range differences remain visible.
  Brain and scalp radiotherapy combined (n=129).
- `efig1_umap.png` — eFigure. UMAP of post embeddings; six unsupervised
  clusters and a phenotype overlay.
- `fig_luna_vs_human_kappa.png` — validation figure, model vs human adjudicator.
- `optA_heatmap_linear.png`, `optB_dotplot.png`, `optC_small_multiples.png` —
  alternative encodings of the Figure 1 data, not used in the letter.

## tables/
- `table1_corpus_distribution.csv` — source for Table 1 (44 rows, 8 sections).
- `comention_rates.csv` — Figure 1 cell values, oriented as displayed.
- `umap_coordinates.csv` — per-post UMAP coordinates and cluster assignment.

## validation/
- `luna_vs_human_kappa_77.csv` — per-label agreement against the blinded
  77-post human-adjudicated reference standard. Median kappa 0.75 across the 16
  informative labels; mean raw agreement 93.5%. Degenerate and low-n cells are
  flagged in the file.
- `variable_readiness.csv` — fill rates for every extracted variable.

## data/
- `analysis_dataset_consensus.csv` — the analysis dataset, one row per post.

## Notes
Percentages throughout are post-level mention rates, not clinical prevalence.
Curl direction is coded only where the author stated a pre-treatment baseline
(n = 177), which is the analytic denominator for that outcome.
