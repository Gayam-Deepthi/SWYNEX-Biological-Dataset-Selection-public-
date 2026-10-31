# SWYNEX-Biological-Dataset-Selection

**Task 1: Biological Dataset Selection, SWYNEX Technologies Internship**

## Selected Dataset

**Transcriptional response of human airway smooth muscle cells to dexamethasone**

| Item | Details |
|---|---|
| Repository | NCBI Gene Expression Omnibus (GEO) |
| Accession | [GSE52778](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE52778) |
| Also available as | Bioconductor R package `airway` |
| Original publication | Himes BE et al., "RNA-Seq transcriptome profiling identifies CRISPLD2 as a glucocorticoid responsive gene that modulates cytokine function in airway smooth muscle cells", PLoS ONE, 2014 |
| Organism | *Homo sapiens* (human) |
| Data type | Bulk RNA-seq (gene expression) |
| Cell type | Primary human airway smooth muscle (ASM) cells |
| Experimental design | 4 independent ASM cell lines, each given 4 treatments: untreated, dexamethasone (a synthetic glucocorticoid), albuterol, and albuterol + dexamethasone (16 samples in the GEO series). This project compares untreated vs dexamethasone. |
| Size | 16 samples in the GEO series (4 per treatment). The Dex vs Untreated comparison uses 8 samples (4 untreated + 4 dexamethasone). The GEO FPKM matrix has 23,273 gene records. |
| Access | Free and public, no login required |

## Research Question

> Which genes change their expression when human airway smooth muscle cells are treated with dexamethasone?

## Why This Dataset

- Dexamethasone and related glucocorticoids are widely used to treat asthma and other airway diseases, so the biological question is meaningful.
- The paired design (the same cell line with and without treatment) makes the comparison clear and statistically sensible.
- The dataset is small and well documented, so it is easy to describe, explore and reproduce.
- It is a standard benchmark dataset for differential expression analysis.

## Why Not the Other Questions

- **Characterizing unknown protein sequences:** open-ended, and needs a custom sequence set and several tools to define a dataset.
- **Prioritizing disease-associated variants:** typically needs very large datasets (for example ClinVar, dbSNP, 1000 Genomes), which are heavier to handle for a first task.

## Planned Analysis (future tasks)

1. Quality control of the count data
2. Differential expression analysis (DESeq2 or edgeR), treated vs. untreated
3. Visualization: PCA, MA plot, volcano plot, heatmap of top genes
4. Functional enrichment (GO terms / pathways) of the responsive genes

## Limitations

- Small sample size (n = 4 per condition)
- Cultured cell lines, which may not fully reflect patient tissue
- Bulk RNA-seq averages over all cells in a sample

## References

- NCBI GEO: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE52778
- Bioconductor `airway` package: https://bioconductor.org/packages/airway/
- Himes BE et al. PLoS ONE 2014 (see title above)

## Author

Your Name | Internship: SWYNEX Technologies
