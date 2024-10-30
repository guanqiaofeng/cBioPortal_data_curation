# cBioPortal_data_curation
This repository document curation of WES variant calls (vcf files) and RNA-seq (expression) for cBioPortal upload

## Curation of VCF files
Each sample contains a indel VCF and snv VCF. The two VCFs need to be 1) concated and 2) converted to MAF. Now each sample will contain a MAF, which will be further 3) merged into a single MAF file.

```
conda install -n base -c conda-forge mamba
mamba create -n bcftools -c bioconda bcftools
mamba create -n bcftools_vcf2maf -c bioconda bcftools vcf2maf
```
