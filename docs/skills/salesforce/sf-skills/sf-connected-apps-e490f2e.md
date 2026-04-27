# sf-connected-apps

## 요약

Salesforce Connected Apps and OAuth configuration with 120-point scoring. TRIGGER when: user configures OAuth flows, JWT bearer auth, Connected Apps, or touches .connectedApp-meta.xml / .eca-meta.xml files. DO NOT TRIGGER when: Named Credentials for callouts (use sf-integration), permission policies (use sf-permissions), or API endpoint code (use sf-apex).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-connected-apps/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-connected-apps-e490f2e.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Connected Apps and OAuth configuration with 120-point scoring. TRIGGER when: user configures OAuth flows, JWT bearer auth, Connected Apps, or touches .connectedApp-meta.xml / .eca-meta.xml files. DO NOT TRIGGER when: Named Credentials for callouts (use sf-integration), permission policies (use sf-permissions), or API endpoint code (use sf-apex).

## 주요 내용

- **진행 방식**: 1. Choose the app model Decide whether a Connected App or ECA is the better long-term fit. 2. Choose the OAuth flow 3. Start from the right template Use the provided assets instead of building from scratch: `assets/connected-app-basic.xml` `assets/connected-app-oauth.xml` `assets/connected-app-jwt.xml` `assets/external-client-app.xml` `assets/eca-global-oauth.xml` `assets/eca-oauth-settings.xml` `assets/eca-policies.xml` If you need source-controlled ECA OAuth security metadata, retrieve it from an org first and treat the retrieved file as the schema source of truth: `sf project retrieve start --metadata ExtlClntAppOauthSecuritySettings:<AppName> --target-org <alias>` 4. Apply security hardening Favor: least-privilege scopes explicit callback URLs PKCE for public clients certificate-based auth where appropriate rotation-ready secret / key handling IP restrictions when realistic and maintainable 5. Validate deployment readiness Before handoff, confirm: metadata file naming is correct s...
- **산출물**: When finishing, report in this order: **App type chosen** **OAuth flow chosen** **Files created or updated** **Security decisions** **Next deployment / testing step** Suggested shape: App: <name> Type: Connected App | External Client App Flow: <oauth flow> Files: <paths> Security: <scopes, PKCE, certs, secrets, IP policy> Next step: <deploy, retrieve consumer key, or test auth flow>

## 원본 문서 구조

- When This Skill Owns the Task
- First Decision: Connected App or External Client App
- Required Context to Gather First
- Recommended Workflow
  - 1. Choose the app model
  - 2. Choose the OAuth flow
  - 3. Start from the right template
  - 4. Apply security hardening
  - 5. Validate deployment readiness
- High-Signal Security Rules
- Metadata Notes That Matter
  - Connected App
  - External Client App
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Migration / examples
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-connected-apps/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
