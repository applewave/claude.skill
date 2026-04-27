# sf-ai-agentforce

## 요약

Agentforce Builder metadata path for Builder-managed topics/actions, Prompt Builder templates, GenAiFunction/GenAiPlugin, Models API, and custom Lightning types. TRIGGER when: user maintains or configures Builder metadata agents, creates topics/actions, works with Prompt Builder templates, or touches .genAiFunction, .genAiPlugin, or .genAiPromptTemplate metadata XML files. DO NOT TRIGGER when: Agent Script DSL .agent files (use sf-ai-agentscript), agent testing (use sf-ai-agentforce-testing), or persona design (use sf-ai-agentforce-persona).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-ai-agentforce/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-ai-agentforce-2757e91.md` |
| 라이선스 | MIT |

## 언제 쓰나

Agentforce Builder metadata path for Builder-managed topics/actions, Prompt Builder templates, GenAiFunction/GenAiPlugin, Models API, and custom Lightning types. TRIGGER when: user maintains or configures Builder metadata agents, creates topics/actions, works with Prompt Builder templates, or touches .genAiFunction, .genAiPlugin, or .genAiPromptTemplate metadata XML files. DO NOT TRIGGER when: Agent Script DSL .agent files (use sf-ai-agentscript), agent testing (use sf-ai-agentforce-testing), or persona design (use sf-ai-agentforce-persona).

## 주요 내용

- **진행 방식**: Confirm this is a **Builder / Setup UI** project Pick Service Agent vs Employee Agent For Service Agents, provision the running user (prefer `sf org create agent-user`) For Employee Agents, plan visibility with a Permission Set containing `<agentAccesses>` Define topics with strong descriptions, scope, and instructions Prepare supporting actions (Flow, Apex, Prompt Builder template) Configure inputs / outputs carefully Validate dependencies and template status Publish, then activate Expanded workflow: [references/builder-workflow.md](references/builder-workflow.md)

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Two Agentforce Paths
- Builder Workflow Summary
- Key Platform Rules
  - Topic quality matters
  - Actions are wrappers around real targets
  - Prompt Template vs GenAiPromptTemplate
  - Supporting metadata deploys first
  - Service Agent running user
  - Employee Agent visibility
  - Publish does not activate
- Metadata Guidance
  - GenAiFunction
  - GenAiPlugin
  - GenAiPromptTemplate
  - Models API
  - Custom Lightning Types
- Cross-Skill Integration
  - Recommended Orchestration Order
  - Required delegations
- High-Signal Failure Patterns
- Reference Map
  - Start here
  - Terminology and template planning
  - Rubric
  - Cross-skill reads
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-ai-agentforce/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
