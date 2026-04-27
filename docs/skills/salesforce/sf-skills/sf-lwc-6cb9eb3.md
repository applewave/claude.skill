# sf-lwc

## 요약

Lightning Web Components with PICKLES methodology and 165-point scoring. TRIGGER when: user creates/edits LWC components, touches lwc/**/*.js, .html, .css, .js-meta.xml files, or asks about wire service, SLDS, or Jest LWC tests. DO NOT TRIGGER when: Apex classes (use sf-apex), Aura components, or Visualforce.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-lwc/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-lwc-6cb9eb3.md` |
| 라이선스 | MIT |

## 언제 쓰나

Lightning Web Components with PICKLES methodology and 165-point scoring. TRIGGER when: user creates/edits LWC components, touches lwc/**/*.js, .html, .css, .js-meta.xml files, or asks about wire service, SLDS, or Jest LWC tests. DO NOT TRIGGER when: Apex classes (use sf-apex), Aura components, or Visualforce.

## 주요 내용

- **진행 방식**: 1. Choose the right architecture Use the **PICKLES** mindset: prototype integrate the right data source compose component boundaries define interaction model use platform libraries optimize execution enforce security 2. Choose the right data access pattern 3. Start from an asset when useful Use provided assets for: basic component bundles datatables modal patterns Flow screen components GraphQL components LMS message channels Jest tests TypeScript-enabled components 4. Validate for frontend quality Check: accessibility SLDS 2 / dark mode compliance event contracts performance / rerender safety Jest coverage when required 5. Hand off supporting backend or deploy work Use: [sf-apex](../sf-apex/SKILL.md) for controllers / services [sf-deploy](../sf-deploy/SKILL.md) for deployment [sf-testing](../sf-testing/SKILL.md) only for Apex-side test loops, not Jest
- **산출물**: When finishing, report in this order: **Component(s) created or updated** **Data access pattern chosen** **Files changed** **Accessibility / styling / testing notes** **Next implementation or deploy step** Suggested shape: LWC work: <summary> Pattern: <wire / apex / graphql / lms / flow-screen> Files: <paths> Quality: <a11y, SLDS2, dark mode, Jest> Next step: <deploy, add controller, or run tests>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Choose the right architecture
  - 2. Choose the right data access pattern
  - 3. Start from an asset when useful
  - 4. Validate for frontend quality
  - 5. Hand off supporting backend or deploy work
- High-Signal Rules
- Output Format
- Local Development Server
- Cross-Skill Integration
- Reference Map
  - Start here
  - Accessibility / performance / state
  - Integration / advanced features
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-lwc/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
