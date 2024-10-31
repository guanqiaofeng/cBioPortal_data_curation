# cBioPortal_data_curation
This repository document curation of WES variant calls (vcf files) and RNA-seq (expression) for cBioPortal upload

## Curation of VCF files
Each sample contains a indel VCF and snv VCF. The two VCFs need to be 1) concated and 2) converted to MAF. Now each sample will contain a MAF, which will be further 3) merged into a single MAF file.

```
conda install -n base -c conda-forge mamba
mamba create -n bcftools -c bioconda bcftools
mamba create -n bcftools_vcf2maf -c bioconda bcftools vcf2maf ensembl-vep
```

```
This package installs only the variant effect predictor (VEP) library
code. To install data libraries, you can use the 'vep_install' command
installed along with it. For example, to install the VEP library for human
GRCh38 to a directory

vep_install -a cf -s homo_sapiens -y GRCh38 -c /output/path/to/GRCh38/vep --CONVERT

(note that vep_install is renamed from INSTALL.pl
 to avoid having generic script names in the PATH)

The --CONVERT flag is not required but improves lookup speeds during
runs. See the VEP documentation for more details

http://www.ensembl.org/info/docs/tools/vep/script/vep_cache.html
```
