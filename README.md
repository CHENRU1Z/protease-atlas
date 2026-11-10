# Pan-Cancer Protease Workbench

An interactive database of protease expression in all 33 TCGA cancer types. It shows bulk RNA-seq (TCGA tumours vs GTEx and adjacent normal tissue) together with single-cell evidence from CZ CELLxGENE.

**Open it:** (https://chenru1z.github.io/protease-atlas/#nominate-COAD)

On the site you can:

- browse an atlas of every cancer type, with a gene × cancer heatmap
- re-run the protease nomination with your own thresholds
- test any gene panel by ROC / AUC
- look up a gene in any cancer type

This repository holds only the built site: `index.html` and one data file per cancer type in `data/`. The R pipeline that builds it (`pancancer_pipeline/`) fetches its inputs from UCSC Xena and the CELLxGENE API and writes this folder.

## Data sources

- **Bulk RNA-seq:** UCSC Xena Toil recompute of TCGA and GTEx (Vivian et al., *Nat Biotechnol* 2017; Goldman et al., *Nat Biotechnol* 2020).
- **Single-cell:** CZ CELLxGENE Discover, Gene Expression (CC BY 4.0).

For research use only, not for clinical decisions. The AUCs are in-sample.
