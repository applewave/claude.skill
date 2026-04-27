# pdca

## 요약

Unified skill for managing the entire PDCA cycle. Auto-triggered by keywords: "plan", "design", "analyze", "report", "status". Replaces legacy /pdca-* commands. Use proactively when user mentions PDCA cycle, planning, design documents, gap analysis, iteration, or completion reports. Triggers: pdca, 계획, 설계, 분석, 검증, 보고서, 반복, 개선, plan, design, analyze, check, report, status, next, iterate, gap, 計画, 設計, 分析, 検証, 報告, 计划, 设计, 分析, 验证, 报告, planificar, diseño, analizar, verificar, planifier, conception, analyser, vérifier, rapport, planen, Entwurf, analysieren, überprüfen, Bericht, pianificare, progettazione, analizzare, verificare, rapporto Do NOT use for: simple queries without PDCA context, code-only tasks.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/pdca/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/pdca-c18c6c7.md` |
| 입력 힌트 | `[action] [feature]` |
| 사용자 호출 | true |

## 언제 쓰나

Unified skill for managing the entire PDCA cycle. Auto-triggered by keywords: "plan", "design", "analyze", "report", "status". Replaces legacy /pdca-* commands. Use proactively when user mentions PDCA cycle, planning, design documents, gap analysis, iteration, or completion reports. Triggers: pdca, 계획, 설계, 분석, 검증, 보고서, 반복, 개선, plan, design, analyze, check, report, status, next, iterate, gap, 計画, 設計, 分析, 検証, 報告, 计划, 设计, 分析, 验证, 报告, planificar, diseño, analizar, verificar, planifier, conception, analyser, vérifier, rapport, planen, Entwurf, analysieren, überprüfen, Bericht, pianificare, progettazione, analizzare, verificare, rapporto Do NOT use for: simple queries without PDCA context, code-only tasks.

## 주요 내용

- **진행 방식**: plan (Plan Phase) Check if `docs/01-plan/features/{feature}.plan.md` exists If not, create based on `plan.template.md` If exists, display content and suggest modifications Create Task: `[Plan] {feature}` Update .bkit-memory.json: phase = "plan" **Output Path**: `docs/01-plan/features/{feature}.plan.md` > **Tip**: For features with ambiguous requirements or multiple implementation approaches, > use `/plan-plus {feature}` instead. Plan Plus adds brainstorming phases (intent discovery, > alternatives exploration, YAGNI review) before document generation for higher-quality plans. design (Design Phase) Verify Plan document exists (required - suggest running plan first if missing) Create `docs/02-design/features/{feature}.design.md` Use `design.template.md` structure + reference Plan content Create Task: `[Design] {feature}` (blockedBy: Plan task) Update .bkit-memory.json: phase = "design" **Output Path**: `docs/02-design/features/{feature}.design.md` do (Do Phase) Verify Design document ex...
- **산출물**: PDCA workflows benefit from the `bkit-pdca-guide` output style: /output-style bkit-pdca-guide This provides PDCA-specific response formatting: Phase status badges: `[Plan] -> [Design] -> [Do] -> [Check] -> [Act]` Gap analysis suggestions after code changes Next-phase guidance with checklists Feature usage report integration When running PDCA commands, suggest this style if not already active.

## 원본 문서 구조

- Arguments
- Action Details
  - plan (Plan Phase)
  - design (Design Phase)
  - do (Do Phase)
  - analyze (Check Phase)
  - iterate (Act Phase)
  - report (Completion Report)
  - team (Team Mode) - v1.5.1
    - team [feature] - Start Team Mode
    - team status - Show Team Status
    - team cleanup - Cleanup Team Resources
  - archive (Archive Phase)
  - cleanup (Cleanup Phase) - v1.4.8
  - status (Status Check)
  - next (Next Phase)
- Template References
- Task Integration
- Agent Integration
- Usage Examples
- Legacy Commands Mapping
- Output Style Integration (v1.5.1)
- Agent Teams Integration (v1.5.1)
- Auto Triggers

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/pdca/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
