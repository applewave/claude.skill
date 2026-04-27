# sf-diagram-mermaid

## 요약

Salesforce architecture diagrams using Mermaid with ASCII fallback. TRIGGER when: user says "diagram", "visualize", "ERD", or asks for sequence diagrams, flowcharts, class diagrams, or architecture visualizations in Mermaid. DO NOT TRIGGER when: user wants PNG/SVG image output (use sf-diagram-nanobananapro), or asks about non-Salesforce systems.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-diagram-mermaid/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-diagram-mermaid-824f5ad.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce architecture diagrams using Mermaid with ASCII fallback. TRIGGER when: user says "diagram", "visualize", "ERD", or asks for sequence diagrams, flowcharts, class diagrams, or architecture visualizations in Mermaid. DO NOT TRIGGER when: user wants PNG/SVG image output (use sf-diagram-nanobananapro), or asks about non-Salesforce systems.

## 주요 내용

- **진행 방식**: 1. Pick the right diagram structure use `sequenceDiagram` for time-ordered interactions use `flowchart LR` for ERDs and capability maps keep a single primary story per diagram when possible 2. Gather data For ERDs and grounded diagrams: use [sf-metadata](../sf-metadata/SKILL.md) when real schema discovery is needed optionally use the local metadata helper script for counts / relationship context when appropriate 3. Generate Mermaid first Apply: accurate labels simple readable node text consistent relationship notation restrained styling that renders cleanly in markdown viewers 4. Add ASCII fallback when useful Provide an ASCII version when the user wants terminal compatibility or plaintext documentation. 5. Explain the diagram briefly Call out the key relationships, flow direction, and any assumptions.

## 원본 문서 구조

- When This Skill Owns the Task
- Supported Diagram Families
- Required Context to Gather First
- Recommended Workflow
  - 1. Pick the right diagram structure
  - 2. Gather data
  - 3. Generate Mermaid first
  - 4. Add ASCII fallback when useful
  - 5. Explain the diagram briefly
- High-Signal Rules
  - For sequence diagrams
  - For ERDs
  - For ASCII output
- Output Format
- <Diagram Title>
  - Mermaid Diagram
  - ASCII Fallback
  - Notes
- Cross-Skill Integration
- Reference Map
  - Start here
  - Styling / ERD specifics
  - Preview
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-diagram-mermaid/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
