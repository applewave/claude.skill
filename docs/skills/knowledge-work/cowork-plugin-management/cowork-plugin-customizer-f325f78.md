# cowork-plugin-customizer

## 요약

Customize a Claude Code plugin for a specific organization's tools and workflows. Use when: customize plugin, set up plugin, configure plugin, tailor plugin, adjust plugin settings, customize plugin connectors, customize plugin skill, tweak plugin, modify plugin configuration.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | cowork-plugin-management |
| 원본 경로 | `knowledge-work-plugins/cowork-plugin-management/skills/cowork-plugin-customizer/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/cowork-plugin-management/cowork-plugin-customizer-f325f78.md` |

## 언제 쓰나

Customize a Claude Code plugin for a specific organization's tools and workflows. Use when: customize plugin, set up plugin, configure plugin, tailor plugin, adjust plugin settings, customize plugin connectors, customize plugin skill, tweak plugin, modify plugin configuration.

## 주요 내용

- **진행 방식**: Phase 0: Gather User Intent (scoped and general customization only) For **scoped customization** and **general customization** (not generic plugin setup), check whether the user provided free-form context alongside their request (e.g., "customize the standup skill — we do async standups in #eng-updates every morning"). **If the user provided context**: Record it and use it to pre-fill answers in Phase 3 — skip asking questions that the user already answered here. **If the user did not provide context**: Ask a single open-ended question using AskUserQuestion before proceeding. Tailor the question to what they asked to customize — e.g., "What changes do you have in mind for the brief skill?" or "What would you like to change about how this plugin works?" Keep it short and specific to their request. Use their response (if any) as additional context throughout the remaining phases. Phase 1: Gather Context from Knowledge MCPs Use company-internal knowledge MCPs to collect information relev...
- **산출물**: After customization, present the user with a summary of what was learned grouped by source. Always include the MCPs sections showing which MCPs were connected during setup and which ones the user should still connect:

## 원본 문서 구조

- Determining the Customization Mode
- Customization Workflow
  - Phase 0: Gather User Intent (scoped and general customization only)
  - Phase 1: Gather Context from Knowledge MCPs
  - Phase 2: Create Todo List
  - Phase 3: Complete Todo Items
  - Phase 4: Search for Useful MCPs
- Packaging the Plugin
- Summary Output
- From searching Slack
- From searching documents
- From your answers
- Additional Resources

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/cowork-plugin-management/skills/cowork-plugin-customizer/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
