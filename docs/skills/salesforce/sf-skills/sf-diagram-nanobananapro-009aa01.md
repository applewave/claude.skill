# sf-diagram-nanobananapro

## 요약

AI-powered image generation for Salesforce visuals via Nano Banana Pro. TRIGGER when: user asks for PNG/SVG output, UI mockups, wireframes, visual ERDs, or says "generate image" / "create mockup". DO NOT TRIGGER when: text-based Mermaid diagrams (use sf-diagram-mermaid), or non-visual documentation tasks.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-diagram-nanobananapro/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-diagram-nanobananapro-009aa01.md` |
| 라이선스 | MIT |

## 언제 쓰나

AI-powered image generation for Salesforce visuals via Nano Banana Pro. TRIGGER when: user asks for PNG/SVG output, UI mockups, wireframes, visual ERDs, or says "generate image" / "create mockup". DO NOT TRIGGER when: text-based Mermaid diagrams (use sf-diagram-mermaid), or non-visual documentation tasks.

## 주요 내용

- **진행 방식**: Unless the user explicitly asks for **quick/simple/just generate**, ask clarifying questions first. Minimum question set Question bank: [references/interview-questions.md](references/interview-questions.md) Quick mode defaults If the user says “quick”, “simple”, or “just generate”, default to: professional style 1K draft output legend included when helpful one image first, then iterate
- **산출물**: After generating, do one of these: open the file in Preview for visual inspection attach/read the image in the coding session for multimodal review ask the user whether to iterate on layout, labeling, or color before finalizing Keep the first pass cheap; only spend on high-res output after the composition is right.

## 원본 문서 구조

- Hard Gate: Prerequisites First
- When This Skill Owns the Task
- Required Context to Gather First
- Interview-First Workflow
  - Minimum question set
  - Quick mode defaults
- Recommended Workflow
  - 1. Gather inputs
  - 2. Build a concrete prompt
  - 3. Generate a fast draft first
  - 4. Iterate before final
  - 5. Use the Python script for controlled final output
- Default Style Guidance
- Common Patterns
- Output / Review Guidance
- Cross-Skill Integration
- Reference Map
  - Start here
  - Visual style / examples
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-diagram-nanobananapro/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
