# zoom-oauth

## 요약

Reference skill for Zoom authentication. Use after routing to an auth workflow when choosing app credentials, grant types, scopes, token refresh behavior, or debugging Zoom OAuth failures.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/oauth/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/zoom-oauth-f0e43c3.md` |
| 사용자 호출 | false |

## 언제 쓰나

Reference skill for Zoom authentication. Use after routing to an auth workflow when choosing app credentials, grant types, scopes, token refresh behavior, or debugging Zoom OAuth failures.

## 주요 내용

- 원본 설명과 문서 구조를 기준으로 필요한 시점에 참조합니다.

## 원본 문서 구조

- 📖 Complete Documentation
- Prerequisites
- Four Authorization Use Cases
  - Industry Terminology
  - Which Flow Should I Use?
- Account Authorization (Server-to-Server OAuth)
  - Request Access Token
  - Response
  - Refresh
- User Authorization (Authorization Code Flow)
  - Step 1: Redirect User to Authorize
  - Step 2: User Authorizes
  - Step 3: Exchange Code for Token
  - Response
  - Refresh Token
  - User-Level vs Account-Level Apps
- Device Authorization (Device Flow)
  - Prerequisites
  - Step 1: Request Device Code
  - Response
  - Step 2: User Authorization
  - Step 3: Poll for Token
  - Response
  - Polling Responses
  - Polling Implementation
  - Refresh
- Client Authorization (Chatbot)
  - Request Token
  - Response
  - Refresh
- Using Access Tokens
  - Call API
  - Me Context
- Revoke Access Token
  - Response
- PKCE (Proof Key for Code Exchange)

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/oauth/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
