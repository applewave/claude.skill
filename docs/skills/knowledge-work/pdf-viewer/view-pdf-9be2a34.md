# view-pdf

## 요약

Interactive PDF viewer. Use when the user wants to open, show, or view a PDF and collaborate on it visually — annotate, highlight, stamp, fill form fields, place signature/initials, or review markup together. Not for summarization or text extraction (use native Read instead).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | pdf-viewer |
| 원본 경로 | `knowledge-work-plugins/pdf-viewer/skills/view-pdf/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/pdf-viewer/view-pdf-9be2a34.md` |

## 언제 쓰나

Interactive PDF viewer. Use when the user wants to open, show, or view a PDF and collaborate on it visually — annotate, highlight, stamp, fill form fields, place signature/initials, or review markup together. Not for summarization or text extraction (use native Read instead).

## 주요 내용

- **진행 방식**: Collaborative annotation (AI-driven) `display_pdf` to open the document `interact` → `get_text` on relevant page range to understand content Propose a batch of annotations to the user (describe what you'll mark) On approval, `interact` → `add_annotations` + `get_screenshot` Show the user, ask for edits, iterate When done, remind them they can download the annotated PDF from the viewer toolbar Form filling (visual, not programmatic) Unlike headless form tools, this gives the user **live visual feedback** and handles forms with cryptic/unnamed fields where the label is printed on the page rather than in field metadata. `display_pdf` — inspect returned `formFields` (name, type, page, bounding box) If field names are cryptic (`Text1`, `Field_7`), `get_screenshot` the pages and match bounding boxes to visual labels Ask the user for values using the **visual** labels, or infer from context `interact` → `fill_form`, then `get_screenshot` to show the result User confirms or edits directly in...

## 원본 문서 구조

- When to use this skill
- Tools
  - `list_pdfs`
  - `display_pdf`
  - `interact`
- Annotation Types
- Interactive Workflows
  - Collaborative annotation (AI-driven)
  - Form filling (visual, not programmatic)
  - Signing (visual, not certified)
- Supported Sources
- Out of Scope

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/pdf-viewer/skills/view-pdf/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
