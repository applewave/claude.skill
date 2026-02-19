# claude.skill

AI 코딩 에이전트에서 사용하는 **스킬, 커맨드, 플러그인** 모음입니다.
Figma MCP 연동 워크플로우와 bkit 개발 프레임워크를 포함합니다.

## 디렉토리 구조

```
claude.skill/
├── skill.figma/                  # Figma MCP 기본 스킬
│   ├── SKILL.md                  # 스킬 정의 및 통합 규칙
│   ├── LICENSE.txt
│   ├── agents/
│   │   └── openai.yaml           # OpenAI Codex 에이전트 설정
│   ├── assets/                   # 아이콘 (SVG, PNG)
│   └── references/
│       ├── figma-mcp-config.md   # MCP 서버 설정/인증/트러블슈팅
│       └── figma-tools-and-prompts.md  # 도구 카탈로그 및 프롬프트 패턴
│
├── skill.figma-implement-design/ # Figma 디자인 구현 스킬
│   ├── SKILL.md                  # 7단계 구현 워크플로우
│   ├── LICENSE.txt
│   ├── agents/
│   │   └── openai.yaml           # OpenAI Codex 에이전트 설정
│   └── assets/                   # 아이콘 (SVG, PNG)
│
├── commands.figma/               # Figma 슬래시 커맨드
│   ├── analyze.md                # /analyze — Figma 분석 + SPEC.md 생성
│   ├── new-page.md               # /new-page — 새 페이지 스캐폴딩
│   ├── publish.md                # /publish — 5단계 퍼블리싱 워크플로우
│   └── verify.md                 # /verify — 빌드 + 스크린샷 + Figma 비교 검증
│
└── claude.bkit/                  # bkit 플러그인 (Vibecoding Kit) v1.5.5
    ├── skills/                   # 27개 스킬
    ├── agents/                   # 16개 에이전트
    ├── scripts/                  # 45개 Hook 스크립트
    ├── lib/                      # 5개 라이브러리 모듈 (241 함수)
    ├── templates/                # 28개 문서 템플릿
    ├── output-styles/            # 4개 출력 스타일
    ├── hooks/                    # Hook 설정
    └── bkit.config.json          # 중앙 설정 파일
```

---

## Figma Skills

### skill.figma — Figma MCP

Figma MCP 서버를 사용하여 디자인 컨텍스트, 스크린샷, 변수, 에셋을 가져오고 코드로 변환하는 기본 스킬입니다.

**핵심 워크플로우:**

1. `get_design_context` — 노드의 구조화된 디자인 데이터 추출
2. `get_metadata` — 대형 노드의 계층 구조 파악 (필요시)
3. `get_screenshot` — 시각적 레퍼런스 캡처
4. 에셋 다운로드 후 프로젝트 컨벤션에 맞게 구현
5. Figma 시안과 1:1 비교 검증

**주요 도구:** `get_design_context`, `get_variable_defs`, `get_metadata`, `get_screenshot`, `get_code_connect_map`

### skill.figma-implement-design — 디자인 구현

Figma 디자인을 **1:1 비주얼 정확도**로 프로덕션 코드로 변환하는 구조화된 7단계 워크플로우를 제공합니다.

| 단계 | 내용 |
|------|------|
| Step 0 | Figma MCP 서버 설정 (미설정 시) |
| Step 1 | Figma URL에서 노드 ID 추출 |
| Step 2 | `get_design_context`로 디자인 데이터 수집 |
| Step 3 | `get_screenshot`으로 시각적 레퍼런스 캡처 |
| Step 4 | 에셋(이미지, SVG, 아이콘) 다운로드 |
| Step 5 | 프로젝트 컨벤션으로 코드 변환 |
| Step 6-7 | 1:1 비주얼 패리티 달성 및 검증 |

---

## Figma Commands

### /analyze `<page> [nodeId]`

Figma 시안을 분석하여 `SPEC.md`를 생성합니다.

- 데스크톱/모바일 노드 자동 검색 및 분석
- 폰트, 간격, 레이아웃, 색상 등 CSS 속성 추출
- `_variables.scss` 토큰 매핑
- 결과를 `docs/guide/design/<page>/SPEC.md`에 저장

### /new-page `<page> <korean-name> <section>`

새 페이지의 스캐폴딩을 생성합니다.

- HTML 페이지 및 섹션 파일 생성
- SCSS 파일 생성 및 `common.scss`에 import 추가
- `index.html` 페이지 목록 테이블에 행 추가
- 디자인 가이드 디렉토리 생성

### /publish `<page>`

분석부터 커밋까지 5단계 퍼블리싱 워크플로우를 실행합니다.

1. **분석** — Figma 시안에서 실측값 추출
2. **문서화** — SPEC.md에 분석 결과 저장
3. **구현** — HTML/SCSS 코드 작성 (데스크톱 + 모바일)
4. **검증** — 빌드, Puppeteer 스크린샷, Figma 비교
5. **커밋** — git add, commit, push

### /verify `<page>`

구현된 페이지를 Figma 시안과 비교 검증합니다.

- `npm run build`로 빌드
- Puppeteer로 데스크톱(1920px)/모바일(375px) 스크린샷 캡처
- Figma 시안과 레이아웃, 폰트, 색상, 간격 비교
- 차이 발견 시 수정 후 재검증 반복

---

## Figma MCP 서버 설정

```toml
# ~/.codex/config.toml
[features]
rmcp_client = true

[mcp_servers.figma]
url = "https://mcp.figma.com/mcp"
bearer_token_env_var = "FIGMA_OAUTH_TOKEN"
http_headers = { "X-Figma-Region" = "us-east-1" }
```

```bash
export FIGMA_OAUTH_TOKEN="<your-token>"
```

---

## bkit 플러그인 (Vibecoding Kit)

[popup-studio-ai/bkit-claude-code](https://github.com/popup-studio-ai/bkit-claude-code) — Claude Code용 종합 AI 네이티브 개발 프레임워크입니다.

| 항목 | 내용 |
|------|------|
| 버전 | 1.5.5 |
| 개발사 | POPUP STUDIO PTE. LTD. |
| 라이선스 | Apache-2.0 |
| 요구사항 | Claude Code v2.1.33+, Node.js v18+ |
| 언어 지원 | 한국어, 영어, 일본어, 중국어, 스페인어, 프랑스어, 독일어, 이탈리아어 |

### 설치

```bash
# 마켓플레이스 등록
/plugin marketplace add popup-studio-ai/bkit-claude-code

# 플러그인 설치
/plugin install bkit
```

### 핵심 개념

- **PDCA 워크플로우** — Plan-Do-Check-Act 방법론 기반 개발 사이클
- **프로젝트 레벨** — Starter(정적), Dynamic(풀스택), Enterprise(마이크로서비스)
- **CTO-Led Agent Teams** — 최대 5개 에이전트가 병렬로 협업하는 팀 오케스트레이션
- **9단계 개발 파이프라인** — 스키마 정의부터 배포까지 구조화된 개발 프로세스
- **Context Engineering** — 5계층 Hook 시스템을 통한 체계적 컨텍스트 관리

### 프로젝트 레벨별 구성

| | Starter | Dynamic | Enterprise |
|---|---------|---------|------------|
| **용도** | 정적 웹사이트, 포트폴리오 | 풀스택 앱 (BaaS) | 마이크로서비스 |
| **기술 스택** | HTML/CSS/JS, Next.js | Next.js + bkend.ai | FastAPI + K8s + Terraform |
| **기본 에이전트** | starter-guide | bkend-expert | enterprise-expert |
| **팀 규모** | - | 최대 3명 | 최대 5명 |
| **출력 스타일** | bkit-learning | bkit-pdca-guide | bkit-enterprise |
| **오케스트레이션** | - | leader→swarm→council | leader→council→swarm→watchdog |

---

### Skills (27개)

#### 핵심 스킬

| 스킬 | 설명 |
|------|------|
| `pdca` | PDCA 사이클 통합 관리 (plan, design, do, analyze, iterate, report, archive) |
| `bkit-rules` | 핵심 규칙 — PDCA 자동 적용, 레벨 감지, 에이전트 자동 트리거, 코드 품질 기준 |
| `bkit-templates` | PDCA 문서 템플릿 (Plan, Design, Analysis, Report) |
| `plan-plus` | 브레인스토밍 강화 PDCA 계획 — 의도 발견, 대안 탐색, YAGNI 검토 |

#### 프로젝트 레벨 스킬

| 스킬 | 설명 |
|------|------|
| `starter` | 정적 웹 개발 가이드 — HTML/CSS/JS 또는 Next.js + Tailwind, GitHub Pages/Vercel 배포 |
| `dynamic` | 풀스택 개발 — Next.js + bkend.ai BaaS, 인증, 데이터 페칭, 보호된 라우트 |
| `enterprise` | 엔터프라이즈 — 마이크로서비스(FastAPI), K8s, Terraform IaC, 모노레포(Turborepo) |

#### 9단계 개발 파이프라인

| 스킬 | 단계 | 설명 |
|------|------|------|
| `phase-1-schema` | 스키마 | 용어 정의, 엔티티/관계, 데이터 구조 설계 |
| `phase-2-convention` | 컨벤션 | 네이밍 규칙, 폴더 구조, Clean Architecture 4계층 |
| `phase-3-mockup` | 목업 | UI/UX 프로토타이핑 (2025-2026 트렌드: bento grid, glassmorphism) |
| `phase-4-api` | API | RESTful API 설계, Zero Script QA, OpenAPI/Swagger 문서화 |
| `phase-5-design-system` | 디자인 시스템 | 3계층 토큰 시스템, shadcn/ui, Style Dictionary |
| `phase-6-ui-integration` | UI 통합 | 3계층 API 클라이언트, 서비스 레이어 패턴, 에러 핸들링 |
| `phase-7-seo-security` | SEO/보안 | 메타 태그, Open Graph, OWASP Top 10, XSS/CSRF 방어 |
| `phase-8-review` | 리뷰 | 크로스 페이즈 검증, Clean Architecture 준수, SOLID 원칙 |
| `phase-9-deployment` | 배포 | CI/CD (GitHub Actions), 환경 변수 관리, Secrets 관리 |
| `development-pipeline` | 개요 | 9단계 파이프라인 전체 가이드, 레벨별 적용 흐름 |

#### bkend.ai BaaS 스킬

| 스킬 | 설명 |
|------|------|
| `bkend-quickstart` | 플랫폼 온보딩 — 리소스 계층(Org→Project→Environment), MCP 설정 |
| `bkend-auth` | 인증/보안 — Email/OAuth/Magic Link, JWT(1h/7d), RBAC, RLS |
| `bkend-data` | 데이터베이스 — 7개 컬럼 타입, CRUD, 필터(8종 연산자), 관계/조인/인덱스 |
| `bkend-storage` | 파일 스토리지 — Presigned URL, 4가지 가시성(public/private/protected/shared) |
| `bkend-cookbook` | 쿡북 — 10개 싱글 프로젝트 + 4개 풀 가이드 (블로그, 레시피, 쇼핑몰, SNS) |

#### 유틸리티 스킬

| 스킬 | 설명 |
|------|------|
| `code-review` | 코드 품질 분석 — 중복, 복잡도, 보안 취약점, 성능, PDCA Check 페이즈 연동 |
| `claude-code-learning` | Claude Code 학습 — 5단계 레벨 (기초→자동화→특화→팀 최적화→PDCA) |
| `zero-script-qa` | 테스트 스크립트 없는 QA — 구조화된 JSON 로깅, Docker 실시간 모니터링 |

#### 플랫폼 스킬

| 스킬 | 설명 |
|------|------|
| `desktop-app` | 데스크톱 앱 — Electron, Tauri(Rust), IPC, 시스템 트레이, 자동 업데이트 |
| `mobile-app` | 모바일 앱 — React Native/Expo, Flutter, 네비게이션, EAS Build |

---

### Agents (16개)

#### 리더십 에이전트

| 에이전트 | 역할 | 상세 |
|----------|------|------|
| `cto-lead` | CTO 팀 오케스트레이터 | PDCA 전체 워크플로우 조율, 품질 기준(90% Match Rate) 관리, 10개 에이전트 조율 |
| `product-manager` | 프로덕트 매니저 | 요구사항 분석, MoSCoW 우선순위, 유저 스토리, Plan 문서 생성 |

#### 아키텍처 에이전트

| 에이전트 | 역할 | 상세 |
|----------|------|------|
| `enterprise-expert` | Enterprise 전문가 | AI Native 개발, 모노레포 vs 멀티레포, 10일 엔터프라이즈 패턴 |
| `frontend-architect` | 프론트엔드 아키텍트 | 컴포넌트 계층, 상태 관리, 디자인 시스템, React/Next.js 전문 |
| `infra-architect` | 인프라 아키텍트 | AWS/EKS/RDS, Terraform, Kubernetes Kustomize, CI/CD 파이프라인 |
| `security-architect` | 보안 아키텍트 | OWASP Top 10 스캔, 인증/인가 아키텍처, 취약점 분석 (읽기 전용) |

#### 품질 보증 에이전트

| 에이전트 | 역할 | 상세 |
|----------|------|------|
| `code-analyzer` | 코드 분석기 | 코드 품질/보안/성능 이슈 감지, Clean Architecture 검증 (읽기 전용) |
| `design-validator` | 디자인 검증기 | 디자인 문서 완전성/일관성 검증, 페이즈별 필수 섹션 확인 (읽기 전용) |
| `gap-detector` | 갭 분석기 | 설계-구현 비교, Match Rate 산출(목표 ≥ 90%), 자동 태스크 생성 (읽기 전용) |
| `qa-strategist` | QA 전략가 | 테스트 전략 수립, qa-monitor/gap-detector/code-analyzer 조율 (읽기 전용) |
| `qa-monitor` | QA 모니터 | Docker 로그 실시간 감시, Request ID 추적, 느린 응답(>1s) 감지 |

#### 워크플로우 에이전트

| 에이전트 | 역할 | 상세 |
|----------|------|------|
| `pdca-iterator` | PDCA 반복기 | Evaluator-Optimizer 패턴, Match Rate < 90% 시 자동 수정 (최대 5회) |
| `report-generator` | 보고서 생성기 | 기능 완료/스프린트/프로젝트 보고서, 체인지로그 자동 업데이트 |
| `pipeline-guide` | 파이프라인 가이드 | 9단계 파이프라인 안내, 현재 페이즈/진행률 파악, 초보자 가이드 |

#### 레벨별 가이드 에이전트

| 에이전트 | 역할 | 상세 |
|----------|------|------|
| `starter-guide` | Starter 가이드 | 비개발자 친화적 설명, HTML/CSS/JS 기초, 단계별 안내 |
| `bkend-expert` | Dynamic BaaS 전문가 | bkend.ai 인증/데이터/스토리지, CRUD, MCP 연동 |

---

### Hook 시스템

5계층 이벤트 기반 아키텍처로 10개 Hook 이벤트를 처리합니다.

```
Layer 1: hooks.json (전역)         → 10개 Hook 이벤트 정의
Layer 2: Skill Frontmatter         → 스킬별 컨텍스트 주입
Layer 3: Agent Frontmatter         → 에이전트별 태스크 Hook
Layer 4: Description Triggers      → 8개 언어 시맨틱 매칭
Layer 5: Scripts (45개 모듈)       → Node.js 실행 로직
```

#### Hook 이벤트 (10개)

| 이벤트 | 설명 | 주요 스크립트 |
|--------|------|---------------|
| `SessionStart` | 세션 초기화 — PDCA 상태, 컨텍스트 계층, 레벨 감지, 언어 감지 | `session-start.js` |
| `PreToolUse` | Write/Edit/Bash 실행 전 가드레일 — 태스크 분류, 권한 검사, 컨벤션 힌트 | `pre-write.js`, `unified-bash-pre.js` |
| `PostToolUse` | Write/Bash/Skill 실행 후 처리 — 태스크 업데이트, PDCA 상태 진행 | `unified-write-post.js`, `unified-bash-post.js`, `skill-post.js` |
| `Stop` | 스킬/에이전트 종료 시 정리 — 결과 통합, 다음 단계 안내 | `unified-stop.js` + 15개 전용 핸들러 |
| `UserPromptSubmit` | 사용자 입력 시 의도 감지, 암묵적 트리거 매칭, 모호성 분석 | `user-prompt-handler.js` |
| `PreCompact` | 컨텍스트 압축 전 스냅샷 보존 (최대 10개) | `context-compaction.js` |
| `TaskCompleted` | 태스크 완료 시 PDCA 페이즈 자동 진행 | `pdca-task-completed.js` |
| `SubagentStart` | 서브에이전트 초기화 추적 | `subagent-start-handler.js` |
| `SubagentStop` | 서브에이전트 종료 추적 | `subagent-stop-handler.js` |
| `TeammateIdle` | 유휴 팀원 감지 및 태스크 재할당 | `team-idle-handler.js` |

#### 주요 스크립트 (45개)

**세션 관리:** `session-start.js` — PDCA 페이즈/레벨 감지, 8개 언어 자동 감지, 온보딩

**Write/Edit 처리:**
- `pre-write.js` — 태스크 분류 (quick_fix < 50줄, minor_change < 200줄, feature < 1000줄, major_feature)
- `unified-write-post.js` — 태스크 생성/업데이트, 갭 분석 트리거

**Bash 처리:**
- `unified-bash-pre.js` — 배포 안전 검사 (kubectl delete, terraform destroy 차단)
- `unified-bash-post.js` — 결과 로깅

**PDCA 워크플로우:**
- `pdca-task-completed.js` — 페이즈 자동 진행
- `pdca-skill-stop.js` — 최종 리포트 생성
- `phase-transition.js` — 멀티 페이즈 전환 검증

**에이전트 핸들러:**
- `gap-detector-stop.js` — 갭 분석 결과 통합, Match Rate < 90% 시 자동 개선 제안
- `iterator-stop.js` — 반복 결과 검증, 90% 임계치 확인
- `cto-stop.js` — CTO 세션 정리

**페이즈별 핸들러:** `phase1-schema-stop.js` ~ `phase9-deploy-stop.js` (각 페이즈 종료 처리)

**팀 조율:** `subagent-start-handler.js`, `subagent-stop-handler.js`, `team-idle-handler.js`, `team-stop.js`

---

### 라이브러리 시스템 (241 함수, 5개 모듈)

#### lib/core/ — 플랫폼 & I/O (41 함수)

| 파일 | 역할 |
|------|------|
| `platform.js` | 플랫폼 감지 (Claude Code, Gemini CLI), 플러그인 루트/프로젝트 경로 |
| `cache.js` | 인메모리 캐싱 (TTL 기본 5초) |
| `io.js` | Hook 입출력 — `readStdinSync()`, `outputAllow()`, `outputBlock()`, XML 이스케이프 |
| `debug.js` | 구조화된 디버그 로깅 (`.bkit/debug.log`) |
| `config.js` | 설정 로딩 우선순위: 프로젝트 → 사용자 → 플러그인 |
| `file.js` | 파일 분류 — `isSourceFile()`, `isCodeFile()`, `isUiFile()`, `extractFeature()` |

#### lib/pdca/ — PDCA 워크플로우 (54 함수)

| 파일 | 역할 |
|------|------|
| `tier.js` | 기술 티어 감지 (Tier 1 Basic ~ Tier 4 Expert) |
| `level.js` | 프로젝트 레벨 자동 감지 (디렉토리 구조 기반) |
| `phase.js` | PDCA 페이즈 관리, 디자인/플랜 문서 검색, 전환 검증 |
| `status.js` | `.pdca-status.json` 영속화, 기능별 상태/이력/Match Rate 추적 |
| `automation.js` | 자동 진행 판단, 페이즈 전환 프롬프트 생성 |

#### lib/intent/ — 의도 감지 & 언어 (24 함수)

| 파일 | 역할 |
|------|------|
| `language.js` | 8개 언어 자동 감지 (키워드 기반) |
| `trigger.js` | 암묵적 에이전트/스킬 트리거 매칭 |
| `ambiguity.js` | 모호성 점수 산출 (0-100), 명확화 질문 생성 |

#### lib/task/ — 태스크 관리 (19 함수)

| 파일 | 역할 |
|------|------|
| `classification.js` | 태스크 크기 분류 (줄 수 기반) |
| `creator.js` | PDCA 페이즈별 태스크 체인 자동 생성 |
| `tracker.js` | `.bkit/tasks.json` 영속화 (최대 50개 링 버퍼) |
| `context.js` | 활성 태스크 컨텍스트 관리 |

#### lib/team/ — Agent Teams 조율 (23 함수)

| 파일 | 역할 |
|------|------|
| `state-writer.js` | `.bkit/agent-state.json` — 원자적 쓰기 (tmp + rename) |
| `orchestrator.js` | 팀 구성 선택 (Dynamic: 3명, Enterprise: 5명) |
| `cto-logic.js` | CTO 의사결정 — 기능 분해, 최적 팀 선택 |
| `strategy.js` | 오케스트레이션 패턴 (leader, council, swarm, watchdog) |
| `communication.js` | 팀 비동기 메시지 큐 |
| `coordinator.js` | 팀 생명주기 관리 |
| `task-queue.js` | 우선순위 기반 태스크 할당, 워크로드 밸런싱 |

#### 기타 라이브러리

| 파일 | 역할 |
|------|------|
| `context-hierarchy.js` | 4계층 컨텍스트 (Plugin → User → Project → Session) |
| `context-fork.js` | 격리된 실행 컨텍스트 포크/머지 |
| `import-resolver.js` | 템플릿 import 해석, `${PLUGIN_ROOT}` / `${PROJECT_ROOT}` 치환 |
| `memory-store.js` | 에이전트별 크로스 세션 메모리 영속화 |
| `permission-manager.js` | 접근 제어 — deny(0), ask(1), allow(2) 패턴 매칭 |
| `skill-orchestrator.js` | 스킬 프론트매터 파싱, next-skill/pdca-phase 연결 |

---

### 템플릿 (28개)

#### PDCA 핵심 템플릿

| 템플릿 | 용도 |
|--------|------|
| `plan.template.md` | 기능 계획서 |
| `plan-plus.template.md` | 브레인스토밍 강화 계획서 |
| `design.template.md` | 기술 설계서 (Dynamic) |
| `design-starter.template.md` | 간단 설계서 (Starter, HTML/CSS) |
| `design-enterprise.template.md` | 복잡 시스템 설계서 (마이크로서비스/K8s) |
| `analysis.template.md` | 갭 분석 및 코드 리뷰 |
| `report.template.md` | 완료 보고서 및 회고 |
| `do.template.md` | 구현 가이드 |
| `iteration-report.template.md` | Evaluator-Optimizer 반복 보고서 |

#### 9단계 파이프라인 템플릿

`pipeline/phase-1-schema.template.md` ~ `pipeline/phase-9-deployment.template.md` + `pipeline/zero-script-qa.template.md`

#### 유틸리티 템플릿

| 템플릿 | 용도 |
|--------|------|
| `CLAUDE.template.md` | CLAUDE.md 프로젝트 설정 생성 |
| `convention.template.md` | 코딩 컨벤션 문서 |
| `schema.template.md` | 데이터 스키마 문서 |
| `_INDEX.template.md` | 폴더 문서 인덱스 |
| `shared/api-patterns.md` | 재사용 API 패턴 라이브러리 |
| `shared/bkend-patterns.md` | bkend.ai 패턴 라이브러리 |
| `shared/error-handling-patterns.md` | 에러 핸들링 전략 |
| `shared/naming-conventions.md` | 네이밍 컨벤션 레퍼런스 |

---

### 출력 스타일 (4개)

| 스타일 | 대상 레벨 | 설명 |
|--------|-----------|------|
| `bkit-learning` | Starter | 초보자 친화적, 단계별 교육적 안내 |
| `bkit-pdca-guide` | Dynamic | PDCA 워크플로우 시각화, 페이즈 진행 추적 |
| `bkit-enterprise` | Enterprise | 고급 아키텍처, 확장성/보안 고려사항 |
| `bkit-pdca-enterprise` | Enterprise+ | PDCA + Enterprise 통합, CTO-Led Agent Teams 연동 |

---

### 설정 (bkit.config.json)

#### PDCA 설정

```json
{
  "matchRateThreshold": 90,
  "maxIterations": 5,
  "autoIterate": true
}
```

#### 태스크 분류

| 분류 | 기준 |
|------|------|
| Quick Fix | < 50줄 |
| Minor Change | 50 ~ 200줄 |
| Feature | 200 ~ 1000줄 |
| Major Feature | > 1000줄 |

#### 레벨 자동 감지

| 레벨 | 감지 기준 |
|------|-----------|
| Enterprise | `kubernetes/`, `terraform/`, `k8s/`, `infra/` 디렉토리 존재 |
| Dynamic | `lib/bkend/`, `supabase/`, `api/`, `docker-compose.yml` 존재 |
| Starter | 기본값 |

#### 코딩 컨벤션

| 대상 | 규칙 |
|------|------|
| 컴포넌트 | PascalCase |
| 함수 | camelCase |
| 상수 | UPPER_SNAKE_CASE |
| 파일 | kebab-case |

#### 권한 관리

| 도구 | 권한 |
|------|------|
| Write / Edit / Read | allow |
| Bash | allow |
| `Bash(rm -rf*)` | **deny** |
| `Bash(rm -r*)` | ask |
| `Bash(git push --force*)` | **deny** |
| `Bash(git reset --hard*)` | ask |

#### 팀 오케스트레이션 패턴

| PDCA 페이즈 | Dynamic | Enterprise |
|-------------|---------|------------|
| Plan | leader | leader |
| Design | leader | council |
| Do | swarm | swarm |
| Check | council | council |
| Act | leader | watchdog |

---

### 프로젝트 설정

설치 후 `.claude/settings.json`에 자동 등록됩니다.

```json
{
  "enabledPlugins": {
    "bkit@bkit-marketplace": true
  }
}
```

---

## License

- Figma 스킬: 각 디렉토리의 `LICENSE.txt` 참고
- bkit 플러그인: Apache-2.0
