# nextflow-development

## 요약

Run nf-core bioinformatics pipelines (rnaseq, sarek, atacseq) on sequencing data. Use when analyzing RNA-seq, WGS/WES, or ATAC-seq data—either local FASTQs or public datasets from GEO/SRA. Triggers on nf-core, Nextflow, FASTQ analysis, variant calling, gene expression, differential expression, GEO reanalysis, GSE/GSM/SRR accessions, or samplesheet creation.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | bio-research |
| 원본 경로 | `knowledge-work-plugins/bio-research/skills/nextflow-development/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/bio-research/nextflow-development-fbe29c1.md` |

## 언제 쓰나

Run nf-core bioinformatics pipelines (rnaseq, sarek, atacseq) on sequencing data. Use when analyzing RNA-seq, WGS/WES, or ATAC-seq data—either local FASTQs or public datasets from GEO/SRA. Triggers on nf-core, Nextflow, FASTQ analysis, variant calling, gene expression, differential expression, GEO reanalysis, GSE/GSM/SRR accessions, or samplesheet creation.

## 주요 내용

- **진행 방식**: [ ] Step 0: Acquire data (if from GEO/SRA) [ ] Step 1: Environment check (MUST pass) [ ] Step 2: Select pipeline (confirm with user) [ ] Step 3: Run test profile (MUST pass) [ ] Step 4: Create samplesheet [ ] Step 5: Configure & run (confirm genome with user) [ ] Step 6: Verify outputs
- **산출물**: Check completion ls results/multiqc/multiqc_report.html grep "Pipeline completed successfully" .nextflow.log Key outputs by pipeline **rnaseq:** `results/star_salmon/salmon.merged.gene_counts.tsv` - Gene counts `results/star_salmon/salmon.merged.gene_tpm.tsv` - TPM values **sarek:** `results/variant_calling/*/` - VCF files `results/preprocessing/recalibrated/` - BAM files **atacseq:** `results/macs2/narrowPeak/` - Peak calls `results/bwa/mergedLibrary/bigwig/` - Coverage tracks

## 원본 문서 구조

- Workflow Checklist
- Step 0: Acquire Data (GEO/SRA Only)
- Step 1: Environment Check
  - Docker issues
  - Nextflow issues
  - Java issues
- Step 2: Select Pipeline
- Step 3: Run Test Profile
- Step 4: Create Samplesheet
  - Generate automatically
  - Validate existing samplesheet
  - Samplesheet formats
- Step 5: Configure & Run
  - 5a. Check genome availability
  - 5b. Decision points
  - 5c. Run pipeline
- Step 6: Verify Outputs
  - Check completion
  - Key outputs by pipeline
- Quick Reference
  - Resume failed run
- References
- Disclaimer
- Attribution
- Licenses

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/bio-research/skills/nextflow-development/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
