# VCF SNP Filtering Pipeline (Nextflow)

A small Nextflow pipeline for filtering SNP variants from VCF files and generating a basic QC summary.

The workflow extracts SNP variants using bcftools and produces simple QC metrics such as variant counts and Ts/Tv ratio. Designed for Linux and HPC environments.

## Requirements

- Nextflow
- bcftools
- Python 3

## Run

```bash
nextflow run main.nf --input sample.vcf.gz
