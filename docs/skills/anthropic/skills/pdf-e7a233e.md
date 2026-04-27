# pdf

## 요약

Use this skill whenever the user wants to do anything with PDF files. This includes reading or extracting text/tables from PDFs, combining or merging multiple PDFs into one, splitting PDFs apart, rotating pages, adding watermarks, creating new PDFs, filling PDF forms, encrypting/decrypting PDFs, extracting images, and OCR on scanned PDFs to make them searchable. If the user mentions a .pdf file or asks to produce one, use this skill.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Anthropic Skills |
| 영역 | skills |
| 원본 경로 | `skills/skills/pdf/SKILL.md` |
| 상세 파일 | `docs/skills/anthropic/skills/pdf-e7a233e.md` |
| 라이선스 | Proprietary. LICENSE.txt has complete terms |

## 언제 쓰나

Use this skill whenever the user wants to do anything with PDF files. This includes reading or extracting text/tables from PDFs, combining or merging multiple PDFs into one, splitting PDFs apart, rotating pages, adding watermarks, creating new PDFs, filling PDF forms, encrypting/decrypting PDFs, extracting images, and OCR on scanned PDFs to make them searchable. If the user mentions a .pdf file or asks to produce one, use this skill.

## 주요 내용

- **진행 방식**: For advanced pypdfium2 usage, see REFERENCE.md For JavaScript libraries (pdf-lib), see REFERENCE.md If you need to fill out a PDF form, follow the instructions in FORMS.md For troubleshooting guides, see REFERENCE.md

## 원본 문서 구조

- Overview
- Quick Start
- Python Libraries
  - pypdf - Basic Operations
    - Merge PDFs
    - Split PDF
    - Extract Metadata
    - Rotate Pages
  - pdfplumber - Text and Table Extraction
    - Extract Text with Layout
    - Extract Tables
    - Advanced Table Extraction
  - reportlab - Create PDFs
    - Basic PDF Creation
    - Create PDF with Multiple Pages
    - Subscripts and Superscripts
- Command-Line Tools
  - pdftotext (poppler-utils)
  - qpdf
  - pdftk (if available)
- Common Tasks
  - Extract Text from Scanned PDFs
  - Add Watermark
  - Extract Images
  - Password Protection
- Quick Reference
- Next Steps

## 관리 메모

- 이 문서는 원본 `skills/skills/pdf/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
