# zigzag-validator

## 요약

Validate traceability and consistency across Customer Problems, Customer Needs, and Functional Requirements domains. Use to check completeness, identify gaps, and ensure all requirements trace to real business problems.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Problem-Based SRS Skills |
| 영역 | Problem-Based-SRS |
| 원본 경로 | `Problem-Based-SRS/skills/zigzag-validator/SKILL.md` |
| 상세 파일 | `docs/skills/problem-based-srs/problem-based-srs/zigzag-validator-f82e48f.md` |
| 라이선스 | MIT |

## 언제 쓰나

Validate traceability and consistency across Customer Problems, Customer Needs, and Functional Requirements domains. Use to check completeness, identify gaps, and ensure all requirements trace to real business problems.

## 주요 내용

- **진행 방식**: This skill is used **during and after** Steps 1, 3, and 5 to validate and refine mappings between domains. It does not replace the generation skills—it complements them. > **Diagram preference:** When visualizing traceability mappings, prefer Mermaid UML diagrams (e.g., `flowchart` for hierarchy trees, `graph` for dependency maps) over ASCII art where rendering supports it. ┌─────────────────────────────────────────────────────────────────────────┐ │ ZIG ZAG DECOMPOSITION │ │ │ │ Customer Customer Functional │ │ Problems Needs Requirements │ │ Domain Domain Domain │ │ │ │ ┌─────┐ ┌─────┐ ┌─────┐ │ │ │ CP │───────▶│ CN │─────────▶│ FR │ │
- **산출물**: Coverage Matrix with Completeness Levels Use **C** (Complete) and **P** (Partial) markers to indicate how well each element addresses its source:

## 원본 문서 구조

- Position in Process
- Axiomatic Design Adaptation
- Purpose
- Zig Zag Process
  - ZAG (Left → Right): Mapping "What" to "How"
  - ZIG (Right → Left): Validation "How" traces to "What"
- Operations
  - Operation 1: ZAG-MAP (Forward Mapping)
  - Operation 2: ZIG-VALIDATE (Backward Traceability)
  - Operation 3: DECOMPOSE (Hierarchical Breakdown)
  - Operation 4: CONSISTENCY-CHECK (Full Audit)
- Rules
  - Independence Axiom
  - Completeness Rule
  - Hierarchy Alignment
- Example: Zig Zag Decomposition
  - Input
  - Zig Zag Process
  - Final Hierarchy
- Output Templates
  - Coverage Matrix with Completeness Levels
- CP → CN Coverage Matrix
  - Gap Analysis
- Gap Analysis Report
  - Uncovered Customer Problems
  - Orphan Items
  - Redundancies
- When to Use This Skill
- Quality Checklist
- References

## 관리 메모

- 이 문서는 원본 `Problem-Based-SRS/skills/zigzag-validator/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
