# Single-Cell Analysis of Immune Response to Nanoplastic Particles

### Dataset Description

**Source:** [Zenodo](https://zenodo.org/records/15866724) (DOI:10.5281/zenodo.15866724)

Use the .h5ad files (AnnData format)

**Samples:**

- **Sample 1:** 40 nm carboxylated polystyrene nanoparticles (PSNPs)
- **Sample 2:** 200 nm PSNPs
- **Sample 3:** 40 nm + 200 nm mixture
- **Sample 4:** Control (no exposure)

## Analysis Workflow

1. **QC & Preprocessing**: Load data, calculate QC metrics, filter cells/genes, normalize
2. **Integration & Clustering**: Merge samples, batch correction, PCA, UMAP, clustering
3. **Cell Type Annotation**: Identify cell types using marker genes
4. **Composition Analysis**: Compare cell type proportions across samples
5. **Differential Expression**: Find genes differentially expressed between conditions
6. **Size-Specific Effects**: Analyze particle size-specific responses

## Reproducing the environment

From the project root:

```bash
conda env create -f environment.yml
conda activate immune-response-nanoplastic
```

## Running the analysis

From the project folder:

Run **project.ipynb**

This script generates plots interactively and prints QC summaries, PCA diagnostics, cluster statistics, and marker-gene analysis output.

## Project structure

- project.ipynb: main analysis pipeline
- [requirements.txt](requirements.txt): pip dependencies
- [environment.yml](environment.yml): conda environment definition
- [data](data): input AnnData files
