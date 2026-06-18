# Projekat iz predmeta Genomska informatika

### Single-Cell Analysis of Immune Response to Nanoplastic Particles
Nanoplastics that enter the bloodstream interact directly with immune cells, and particle size appears to shape the response. You will use single-cell RNA sequencing (scRNA-seq)to investigate how nanoplastics of different sizes affect human peripheral blood immune cells.

#### Dataset
Source: https://zenodo.org/records/15866724 (DOI:10.5281/zenodo.15866724)

Four samples from one donor, exposed to carboxylated polystyrene nanoparticles (PSNPs):
● Sample 1, 40 nm PSNPs
● Sample 2, 200 nm PSNPs
● Sample 3, 40 nm + 200 nm mixture
● Sample 4, control (no exposure)

Use the .h5ad files (AnnData format). The *_CoDi_KLD.csv files are used as a reference for
potential comparison with the obtained results.

#### Tasks
1. QC & preprocessing — filter cells, normalise, select variable genes. Justify thresholds.
2. Integration & clustering - combine all four samples with a batch-correction method of
your choice; compute UMAP and clusters.
3. Cell type annotation - assign immune cell types (T, B, NK, monocytes, etc.) using
marker genes and the Azimuth PBMC reference (RDS) dataset.
4. Composition analysis - compare cell type proportions across the four samples.
5. Differential expression - for each major cell type, compare each exposed sample
against the control; run pathway enrichment (GO/Reactome/KEGG).
6. Size-specific effects - identify responses that are unique to 40 nm, unique to 200 nm,
shared, or emerge only in the mixture. Interpret biologically.

#### Deliverables
● Github Code repository with an environment file and a README explaining how to
reproduce results (20 points).
● Propose and implement 3-5 additional insights or analyses to the dataset (10 points)
● PowerPoint slides explaining all the results with visualisations (also saved on GitHub)
(10 points)
● Video presentation (5-10 minutes) of the results uploaded to YouTube or other video
platform (20 points)

#### Installing pre-commit

```bash
pip install pre-commit==2.13
pre-commit install
```
