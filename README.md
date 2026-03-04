# VCF SNP Filtering Pipeline (Nextflow)

A small Nextflow pipeline for filtering SNP variants from VCF files and generating a basic QC summary.

The workflow extracts SNP variants using bcftools and produces simple QC metrics such as variant counts and Ts/Tv ratio. Designed for Linux and HPC environments.

## Pipeline Overview

```mermaid
graph TD
    A[VCF Input] --> B[SNP Filtering]
    B --> C[QC Statistics]
    C --> D[Summary Report]

## Requirements

- Nextflow
- bcftools
- Python 3

## Input

- `--input` : compressed VCF file (`.vcf.gz`)

## Run

```bash
nextflow run main.nf --input sample.vcf.gz
```

## Output

The pipeline generates:

- `filtered.snps.vcf.gz` : SNP-only filtered VCF file  
- `qc_summary.txt` : simple QC summary including variant counts and Ts/Tv ratio
