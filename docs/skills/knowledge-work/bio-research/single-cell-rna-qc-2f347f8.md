# single-cell-rna-qc

## 요약

Performs quality control on single-cell RNA-seq data (.h5ad or .h5 files) using scverse best practices with MAD-based filtering and comprehensive visualizations. Use when users request QC analysis, filtering low-quality cells, assessing data quality, or following scverse/scanpy best practices for single-cell analysis.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | bio-research |
| 원본 경로 | `knowledge-work-plugins/bio-research/skills/single-cell-rna-qc/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/bio-research/single-cell-rna-qc-2f347f8.md` |

## 언제 쓰나

Performs quality control on single-cell RNA-seq data (.h5ad or .h5 files) using scverse best practices with MAD-based filtering and comprehensive visualizations. Use when users request QC analysis, filtering low-quality cells, assessing data quality, or following scverse/scanpy best practices for single-cell analysis.

## 주요 내용

- **진행 방식**: For standard QC following scverse best practices, use the convenience script `scripts/qc_analysis.py`: python3 scripts/qc_analysis.py input.h5ad or for 10X Genomics .h5 files: python3 scripts/qc_analysis.py raw_feature_bc_matrix.h5 The script automatically detects the file format and loads it appropriately. **When to use this approach:** Standard QC workflow with adjustable thresholds (all cells filtered the same way) Batch processing multiple datasets Quick exploratory analysis User wants the "just works" solution **Requirements:** anndata, scanpy, scipy, matplotlib, seaborn, numpy **Parameters:** Customize filtering thresholds and gene patterns using command-line parameters: `--output-dir` - Output directory `--mad-counts`, `--mad-genes`, `--mad-mt` - MAD thresholds for counts/genes/MT% `--mt-threshold` - Hard mitochondrial % cutoff `--min-cells` - Gene filtering threshold `--mt-pattern`, `--ribo-pattern`, `--hb-pattern` - Gene name patterns for different species Use `--help` to see...

## 원본 문서 구조

- When to Use This Skill
- Approach 1: Complete QC Pipeline (Recommended for Standard Workflows)
  - Workflow Steps
- Approach 2: Modular Building Blocks (For Custom Workflows)
- Best Practices
- Reference Materials
- Next Steps After QC

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/bio-research/skills/single-cell-rna-qc/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
