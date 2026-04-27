# sf-flex-estimator

## 요약

Salesforce Flex Credit estimation for Agentforce and Data Cloud workloads. TRIGGER when: user needs cost projections, scenario planning, budget sizing, or architecture tradeoff analysis for Agentforce prompts/actions, Data Cloud meters, or monthly Flex Credit usage. DO NOT TRIGGER when: user is building Agentforce metadata or .agent files themselves (use sf-ai-agentforce or sf-ai-agentscript), implementing Data Cloud assets (use sf-datacloud-*), or asking for contract-specific commercial approval that depends on non-public pricing terms.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-flex-estimator/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-flex-estimator-8b5ff25.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Flex Credit estimation for Agentforce and Data Cloud workloads. TRIGGER when: user needs cost projections, scenario planning, budget sizing, or architecture tradeoff analysis for Agentforce prompts/actions, Data Cloud meters, or monthly Flex Credit usage. DO NOT TRIGGER when: user is building Agentforce metadata or .agent files themselves (use sf-ai-agentforce or sf-ai-agentscript), implementing Data Cloud assets (use sf-datacloud-*), or asking for contract-specific commercial approval that depends on non-public pricing terms.

## 주요 내용

- **진행 방식**: 1. Baseline the structure Model the agent and Data Cloud footprint first. Useful starting templates: [assets/templates/basic-agent-template.json](assets/templates/basic-agent-template.json) [assets/templates/hybrid-agent-template.json](assets/templates/hybrid-agent-template.json) [assets/templates/data-cloud-template.json](assets/templates/data-cloud-template.json) 2. Calculate the per-invocation cost For Agentforce, estimate: per-invocation FC = prompt FC + action FC + token overage FC 3. Calculate Data Cloud base FC Map each monthly meter volume to the current public rate card, then apply cumulative tiering. 4. Generate scenarios Use the standard scenario set unless the user provides a better one: Low: 1K invocations / month Medium: 10K / month High: 100K / month Enterprise: 500K / month 5. Validate assumptions and recommend optimizations Check for: too many prompts or actions unnecessary streaming usage likely token overages missing Private Connect handling unrealistic volume assum...
- **산출물**: When the estimate is complete, present: workload summary per-invocation Agentforce cost monthly scenario table Data Cloud tiering impact top optimization recommendations confidence / validation notes Suggested shape: Flex Credit estimate: <name> Agentforce per invocation: <fc> FC ($<cost>) Data Cloud monthly base: <fc> FC Scenarios: <low / medium / high / enterprise> Optimization priorities: <1-3 bullets> Confidence: <high / medium / low>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Pricing Model
  - Agentforce
  - Data Cloud
  - Other rules
- Recommended Workflow
  - 1. Baseline the structure
  - 2. Calculate the per-invocation cost
  - 3. Calculate Data Cloud base FC
  - 4. Generate scenarios
  - 5. Validate assumptions and recommend optimizations
- Scripts and Templates
  - Calculator
  - Validation helper
  - Example commands
- High-Signal Estimation Rules
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Pricing references
  - Validation and scoring

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-flex-estimator/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
