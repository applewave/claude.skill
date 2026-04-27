# bkend-auth

## 요약

bkend.ai authentication and security expert skill. Covers email signup/login, social login (Google, GitHub), magic link, JWT tokens (Access 1h, Refresh 7d), session management, RBAC (admin/user/self/guest), RLS policies, password management, and account lifecycle. Triggers: signup, login, JWT, session, social login, RBAC, RLS, password, token, 회원가입, 로그인, 토큰, 세션, 권한, 보안정책, 비밀번호, ログイン, 認証, セッション, 権限, パスワード, 登录, 认证, 会话, 权限, 密码, registro, inicio de sesion, permisos, contrasena, inscription, connexion, permissions, mot de passe, Registrierung, Anmeldung, Berechtigungen, Passwort, registrazione, accesso, permessi, password Do NOT use for: database CRUD (use bkend-data), file storage (use bkend-storage), enterprise-level security architecture (use security-architect).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/bkend-auth/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/bkend-auth-fb7693c.md` |
| 사용자 호출 | false |

## 언제 쓰나

bkend.ai authentication and security expert skill. Covers email signup/login, social login (Google, GitHub), magic link, JWT tokens (Access 1h, Refresh 7d), session management, RBAC (admin/user/self/guest), RLS policies, password management, and account lifecycle. Triggers: signup, login, JWT, session, social login, RBAC, RLS, password, token, 회원가입, 로그인, 토큰, 세션, 권한, 보안정책, 비밀번호, ログイン, 認証, セッション, 権限, パスワード, 登录, 认证, 会话, 权限, 密码, registro, inicio de sesion, permisos, contrasena, inscription, connexion, permissions, mot de passe, Registrierung, Anmeldung, Berechtigungen, Passwort, registrazione, accesso, permessi, password Do NOT use for: database CRUD (use bkend-data), file storage (use bkend-storage), enterprise-level security architecture (use security-architect).

## 주요 내용

- **진행 방식**: bkend MCP does NOT have dedicated auth tools. Use this workflow: **Search docs**: `search_docs` with query "email signup" or "social login" **Get examples**: `search_docs` with query "auth code examples" **Generate code**: AI generates REST API code based on search results Searchable Auth Docs Key Pattern User: "Add social login" → search_docs(query: "social login implementation") → Returns auth guide with REST API patterns → AI generates social login code

## 원본 문서 구조

- Auth Methods
- JWT Token Structure
- Password Policy
- MCP Auth Workflow
  - Searchable Auth Docs
  - Key Pattern
- REST Auth API (Core Endpoints)
- RBAC (Role-Based Access Control)
- RLS (Row Level Security)
- Session Management
- Official Documentation (Live Reference)

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/bkend-auth/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
