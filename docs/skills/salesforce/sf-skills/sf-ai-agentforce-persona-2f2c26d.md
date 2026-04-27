# sf-ai-agentforce-persona

## 요약

Deep persona design for Agentforce agents with 50-point scoring. TRIGGER when: user designs agent personas, defines agent personality/identity, creates persona documents, encodes persona into Agentforce Builder fields or Agent Script, translates brand guidelines to agent voice, or asks about agent tone/voice/register. DO NOT TRIGGER when: building agent metadata (use sf-ai-agentforce), testing agents (use sf-ai-agentforce-testing), or Agent Script DSL (use sf-ai-agentscript).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-ai-agentforce-persona/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-ai-agentforce-persona-2f2c26d.md` |
| 라이선스 | MIT |

## 언제 쓰나

Deep persona design for Agentforce agents with 50-point scoring. TRIGGER when: user designs agent personas, defines agent personality/identity, creates persona documents, encodes persona into Agentforce Builder fields or Agent Script, translates brand guidelines to agent voice, or asks about agent tone/voice/register. DO NOT TRIGGER when: building agent metadata (use sf-ai-agentforce), testing agents (use sf-ai-agentforce-testing), or Agent Script DSL (use sf-ai-agentscript).

## 주요 내용

- **산출물**: The skill produces up to four Markdown files: **Persona document** (`_local/generated/[agent-name]-persona.md`) — follows the `assets/persona-template.md` structure. The design artifact defining who the agent is, how it sounds, and what it never does. **Sample dialog** (`_local/generated/[agent-name]-sample-dialog.md`) — follows the `assets/sample-dialog-template.md` structure. Validation artifact demonstrating the persona in conversation. **Scorecard** (`_local/generated/[agent-name]-persona-scorecard.md`) — 50-point rubric evaluation. Generated on request. **Encoding output** (`_local/generated/[agent-name]-persona-encoding.md`) — follows the `assets/persona-encoding-template.md` structur...

## 원본 문서 구조

- How to Use
- When to Use This Skill
- Framework Reference
- Entry Point Detection
- Design Flow
  - Phase 1: Essentials
    - Step 1: Input
    - Step 2: Minimal Context
    - One-Shot vs. Wizard
    - Step 3: Draft
    - Step 4: Present the Persona
    - Step 5: Sample Dialog
  - Phase 2: Electives
    - Refine
    - Other (free-text additions)
    - Lexicon
    - Done
- Scoring
- Encode Flow
  - Encoding Context
  - Generation
    - If Agent Script
    - If Agentforce Builder
    - Output
- Output

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-ai-agentforce-persona/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
