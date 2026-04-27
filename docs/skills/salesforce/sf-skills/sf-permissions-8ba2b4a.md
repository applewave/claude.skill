# sf-permissions

## 요약

Permission Set analysis, hierarchy viewer, and access auditing. TRIGGER when: user asks "who has access to X?", analyzes permission sets/groups, or touches .permissionset-meta.xml / .permissionsetgroup-meta.xml files. DO NOT TRIGGER when: creating new metadata (use sf-metadata), deploying permission sets (use sf-deploy), or Apex sharing logic (use sf-apex).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-permissions/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-permissions-8ba2b4a.md` |
| 라이선스 | MIT |

## 언제 쓰나

Permission Set analysis, hierarchy viewer, and access auditing. TRIGGER when: user asks "who has access to X?", analyzes permission sets/groups, or touches .permissionset-meta.xml / .permissionsetgroup-meta.xml files. DO NOT TRIGGER when: creating new metadata (use sf-metadata), deploying permission sets (use sf-deploy), or Apex sharing logic (use sf-apex).

## 주요 내용

- **진행 방식**: 1. Classify the request 2. Connect to the correct org Verify `sf` auth before running permission analysis. 3. Use the narrowest useful query Prefer focused analysis over broad org-wide scans unless the user explicitly wants a full audit. When choosing identifiers, prefer stable metadata names first: `PermissionSet.Name` `PermissionSetGroup.DeveloperName` `CustomPermission.DeveloperName` object and field API names such as `Account` or `Account.AnnualRevenue` `Assignee.Username` / email for user-centric checks Use Salesforce record IDs only when: the underlying object model requires `ParentId` or `SetupEntityId`, or you are drilling into records returned by a prior read-only query in the same investigation 4. Render findings clearly Use: ASCII tree or table output for terminal work Mermaid only when documentation benefit is clear concise summaries of which permission source grants access 5. Hand off creation or deployment work Use: [sf-metadata](../sf-metadata/SKILL.md) for richer metad...
- **산출물**: When finishing, report in this order: **What was analyzed** **Org / subject scope** **Which permissions grant access** **Whether access is direct or inherited** **Recommended follow-up** Suggested shape: Permission analysis: <hierarchy / detect / user / export> Scope: <org, user, permission target> Findings: <permsets / groups / access level> Source: <direct assignment or via group> Next step: <export, generate metadata, or deploy changes>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Classify the request
  - 2. Connect to the correct org
  - 3. Use the narrowest useful query
  - 4. Render findings clearly
  - 5. Hand off creation or deployment work
- High-Signal Rules
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Specialized analysis
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-permissions/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
