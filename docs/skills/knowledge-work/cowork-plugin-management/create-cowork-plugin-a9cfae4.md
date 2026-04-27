# create-cowork-plugin

## 요약

Guide users through creating a new plugin from scratch in a cowork session. Use when users want to create a plugin, build a plugin, make a new plugin, develop a plugin, scaffold a plugin, start a plugin from scratch, or design a plugin. This skill requires Cowork mode with access to the outputs directory for delivering the final .plugin file.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | cowork-plugin-management |
| 원본 경로 | `knowledge-work-plugins/cowork-plugin-management/skills/create-cowork-plugin/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/cowork-plugin-management/create-cowork-plugin-a9cfae4.md` |

## 언제 쓰나

Guide users through creating a new plugin from scratch in a cowork session. Use when users want to create a plugin, build a plugin, make a new plugin, develop a plugin, scaffold a plugin, start a plugin from scratch, or design a plugin. This skill requires Cowork mode with access to the outputs directory for delivering the final .plugin file.

## 주요 내용

- **진행 방식**: When you ask the user something, use AskUserQuestion. Don't assume "industry standard" defaults are correct. Note: AskUserQuestion always includes a Skip button and a free-text input box for custom answers, so do not include `None` or `Other` as options. Phase 1: Discovery **Goal**: Understand what the user wants to build and why. Ask (only what is unclear — skip questions if the user's initial request already answers them): What should this plugin do? What problem does it solve? Who will use it and in what context? Does it integrate with any external tools or services? Is there a similar plugin or workflow to reference? Summarize understanding and confirm before proceeding. **Output**: Clear statement of plugin purpose and scope. Phase 2: Component Planning **Goal**: Determine which component types the plugin needs. Based on the discovery answers, determine: **Skills** — Does it need specialized knowledge that Claude should load on-demand, or user-initiated actions? (domain expertise...

## 원본 문서 구조

- Overview
- Plugin Architecture
  - Directory Structure
  - plugin.json Manifest
  - Component Schemas
  - Customizable plugins with `~~` placeholders
- How tool references work
- Connectors for this plugin
  - ${CLAUDE_PLUGIN_ROOT} Variable
- Guided Workflow
  - Phase 1: Discovery
  - Phase 2: Component Planning
  - Phase 3: Design & Clarifying Questions
  - Phase 4: Implementation
  - Phase 5: Review & Package
- Best Practices
- Additional Resources

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/cowork-plugin-management/skills/create-cowork-plugin/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
