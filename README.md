# SWYNEX Biological Dataset Selection

**Task 1, SWYNEX Technologies Internship**

## Selected Dataset
**1000 Genomes Project (Phase 3), Chromosome 22**

## Source
- Project site: https://www.internationalgenome.org/
- Data (FTP, open access): https://ftp.1000genomes.ebi.ac.uk/vol1/ftp/release/20130502/
- Genotype file: ALL.chr22.phase3_shapeit2_mvncht_integrated_v5a.20130502.genotypes.vcf.gz
- Sample metadata (population labels): integrated_call_samples_v3.20130502.ALL.panel
- Access: free and public, no registration required
- Reference: The 1000 Genomes Project Consortium (2015), Nature 526:68-74

## Dataset Description
The 1000 Genomes Project is one of the largest public catalogs of human
genetic variation. It sequenced the genomes of people from many regions of
the world and recorded where their DNA differs from the human reference
genome. The data are stored in VCF format: each row is a variant position,
and each column is a person's genotype at that position.

## Size
- Individuals: 2,504 (Phase 3)
- Populations: 26, grouped into 5 super-populations
  (African, American, East Asian, European, South Asian)
- Chromosome 22 variants: about 1.1 million
- File size: roughly 200 MB compressed (chr22 only, chosen to keep the
  analysis manageable on a laptop)

## Research Question
Can genetic variation on a single human chromosome (chr22) separate
individuals by ancestry, and which genomic regions and variants contribute
most to the differences between populations?

## Why This Dataset
- Real human genomic data from a landmark research project
- Standard VCF format, used throughout professional bioinformatics
- Clear metadata for validating results (known population labels)
- Supports PCA, population structure, allele frequency, and selection analysis

## Planned Workflow (Next Tasks)
1. Download chr22 VCF and the sample panel file
2. Inspect and summarize the VCF (variants, samples, variant types)
3. Quality filtering (biallelic SNPs, minor allele frequency)
4. Convert genotypes to a numeric matrix
5. Run PCA and plot PC1 vs PC2 colored by population
6. Compare allele frequencies between populations (e.g. Fst)
7. Identify variants that differ most between groups
8. Summarize findings

## Tools
Python (scikit-allel, NumPy, pandas, scikit-learn, matplotlib),
bcftools, optionally PLINK

## Limitations
- One chromosome only, so results are a subset of the full genome
- Sample sizes differ across populations (about 100 per population)
- Phase 3 uses the GRCh37 reference genome

## Citation
The 1000 Genomes Project Consortium. A global reference for human genetic
variation. Nature 526, 68-74 (2015). https://doi.org/10.1038/nature15393
