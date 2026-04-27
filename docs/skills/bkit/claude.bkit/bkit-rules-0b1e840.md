# bkit-rules

## 요약

Core rules for bkit plugin. PDCA methodology, level detection, agent auto-triggering, and code quality standards. These rules are automatically applied to ensure consistent AI-native development. Use proactively when user requests feature development, code changes, or implementation tasks. Triggers: bkit, PDCA, develop, implement, feature, bug, code, design, document, 개발, 기능, 버그, 코드, 설계, 문서, 開発, 機能, バグ, 开发, 功能, 代码, desarrollar, función, error, código, diseño, documento, développer, fonctionnalité, bogue, code, conception, document, entwickeln, Funktion, Fehler, Code, Design, Dokument, sviluppare, funzionalità, bug, codice, design, documento Do NOT use for: documentation-only tasks, research, or exploration without code changes.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/bkit-rules/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/bkit-rules-0b1e840.md` |

## 언제 쓰나

Core rules for bkit plugin. PDCA methodology, level detection, agent auto-triggering, and code quality standards. These rules are automatically applied to ensure consistent AI-native development. Use proactively when user requests feature development, code changes, or implementation tasks. Triggers: bkit, PDCA, develop, implement, feature, bug, code, design, document, 개발, 기능, 버그, 코드, 설계, 문서, 開発, 機能, バグ, 开发, 功能, 代码, desarrollar, función, error, código, diseño, documento, développer, fonctionnalité, bogue, code, conception, document, entwickeln, Funktion, Fehler, Code, Design, Dokument, sviluppare, funzionalità, bug, codice, design, documento Do NOT use for: documentation-only tasks, research, or exploration without code changes.

## 주요 내용

- **산출물**: When project level is detected, automatically suggest the matching output style: Auto-Selection Rules On session start: Suggest output style matching detected level On `/starter init`, `/dynamic init`, `/enterprise init`: Auto-suggest style for that level On PDCA phase transitions: Suggest `bkit-pdca-guide` if not already active User can override with `/output-style` at any time Available Output Styles

## 원본 문서 구조

- 1. PDCA Auto-Apply Rules
  - Template References
- 2. Level Auto-Detection
  - Detection Order
  - Enterprise (2+ conditions met)
  - Dynamic (1+ conditions met)
  - Starter
  - Level-specific Behavior
  - Level Upgrade Signals
  - Hierarchical CLAUDE.md Rules
- 3. Agent Auto-Trigger Rules
  - Level-Based Selection
  - Task-Based Selection
  - Proactive Suggestions
  - Do NOT Auto-Invoke When
- 4. Code Quality Standards
  - Pre-coding Checks
  - Core Principles
  - Self-Check After Coding
  - When to Refactor
- 5. Task Classification
  - Classification Keywords
- 6. Output Style Auto-Selection (v1.5.1)
  - Auto-Selection Rules
  - Available Output Styles
- 7. Agent Teams Auto-Suggestion (v1.5.1)
  - Suggestion Triggers
  - Team Availability
  - Requirements
- 8. Agent Memory Awareness (v1.5.1)
  - How It Works
  - Memory Scopes
  - Proactive Mention

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/bkit-rules/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
