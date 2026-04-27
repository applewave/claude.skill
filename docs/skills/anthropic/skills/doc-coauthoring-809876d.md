# doc-coauthoring

## 요약

Guide users through a structured workflow for co-authoring documentation. Use when user wants to write documentation, proposals, technical specs, decision docs, or similar structured content. This workflow helps users efficiently transfer context, refine content through iteration, and verify the doc works for readers. Trigger when user mentions writing docs, creating proposals, drafting specs, or similar documentation tasks.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Anthropic Skills |
| 영역 | skills |
| 원본 경로 | `skills/skills/doc-coauthoring/SKILL.md` |
| 상세 파일 | `docs/skills/anthropic/skills/doc-coauthoring-809876d.md` |

## 언제 쓰나

Guide users through a structured workflow for co-authoring documentation. Use when user wants to write documentation, proposals, technical specs, decision docs, or similar structured content. This workflow helps users efficiently transfer context, refine content through iteration, and verify the doc works for readers. Trigger when user mentions writing docs, creating proposals, drafting specs, or similar documentation tasks.

## 주요 내용

- **진행 방식**: **Trigger conditions:** User mentions writing documentation: "write a doc", "draft a proposal", "create a spec", "write up" User mentions specific doc types: "PRD", "design doc", "decision doc", "RFC" User seems to be starting a substantial writing task **Initial offer:** Offer the user a structured workflow for co-authoring the document. Explain the three stages: **Context Gathering**: User provides all relevant context while Claude asks clarifying questions **Refinement & Structure**: Iteratively build each section through brainstorming and editing **Reader Testing**: Test the doc with a fresh Claude (no context) to catch blind spots before others read it Explain that this approach helps ensure the doc works well when others read it (including when they paste it into Claude). Ask if they want to try this workflow or prefer to work freeform. If user declines, work freeform. If user accepts, proceed to Stage 1.

## 원본 문서 구조

- When to Offer This Workflow
- Stage 1: Context Gathering
  - Initial Questions
  - Info Dumping
- Stage 2: Refinement & Structure
  - Step 1: Clarifying Questions
  - Step 2: Brainstorming
  - Step 3: Curation
  - Step 4: Gap Check
  - Step 5: Drafting
  - Step 6: Iterative Refinement
  - Quality Checking
  - Near Completion
- Stage 3: Reader Testing
  - Testing Approach
  - Step 1: Predict Reader Questions
  - Step 2: Test with Sub-Agent
  - Step 3: Run Additional Checks
  - Step 4: Report and Fix
  - Step 1: Predict Reader Questions
  - Step 2: Setup Testing
  - Step 3: Additional Checks
  - Step 4: Iterate Based on Results
  - Exit Condition (Both Approaches)
- Final Review
- Tips for Effective Guidance

## 관리 메모

- 이 문서는 원본 `skills/skills/doc-coauthoring/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
