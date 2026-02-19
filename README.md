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
└── commands.figma/               # Figma 슬래시 커맨드
    ├── analyze.md                # /analyze — Figma 분석 + SPEC.md 생성
    ├── new-page.md               # /new-page — 새 페이지 스캐폴딩
    ├── publish.md                # /publish — 5단계 퍼블리싱 워크플로우
    └── verify.md                 # /verify — 빌드 + 스크린샷 + Figma 비교 검증
```

## Skills

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

## Commands

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

## MCP 서버 설정

Figma MCP 서버 연결이 필요합니다.

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
# OAuth 토큰 설정
export FIGMA_OAUTH_TOKEN="<your-token>"
```

## bkit 플러그인 (Vibecoding Kit)

[popup-studio-ai/bkit-claude-code](https://github.com/popup-studio-ai/bkit-claude-code) — Claude Code용 종합 개발 프레임워크입니다.

| 항목 | 내용 |
|------|------|
| 버전 | 1.5.5 |
| 개발사 | POPUP STUDIO PTE. LTD. |
| 라이선스 | Apache-2.0 |
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

### Skills (27개)

| 카테고리 | 스킬 | 설명 |
|----------|------|------|
| **핵심** | `pdca`, `bkit-rules`, `bkit-templates`, `plan-plus` | PDCA 사이클, 규칙, 템플릿 |
| **프로젝트** | `starter`, `dynamic`, `enterprise` | 프로젝트 레벨별 가이드 |
| **파이프라인** | `phase-1-schema` ~ `phase-9-deployment` | 9단계 개발 파이프라인 |
| **bkend.ai** | `bkend-quickstart`, `bkend-auth`, `bkend-data`, `bkend-storage`, `bkend-cookbook` | BaaS 플랫폼 연동 |
| **유틸리티** | `code-review`, `claude-code-learning`, `zero-script-qa`, `development-pipeline` | 코드 리뷰, 학습, QA |
| **플랫폼** | `desktop-app`, `mobile-app` | 데스크톱/모바일 앱 개발 |

### Agents (16개)

| 에이전트 | 역할 |
|----------|------|
| `cto-lead` | 프로젝트 리더, 팀 오케스트레이션 |
| `frontend-architect` | 프론트엔드 아키텍처 설계 |
| `security-architect` | 보안 검토 및 취약점 분석 |
| `code-analyzer` | 코드 품질 분석 및 리뷰 |
| `design-validator` | 디자인-구현 일치 검증 |
| `gap-detector` | 설계-구현 갭 분석 |
| `qa-strategist` | QA 전략 수립 |
| `qa-monitor` | 로그 기반 모니터링 |
| `product-manager` | 요구사항 정의 및 기능 스펙 |
| `report-generator` | 보고서 생성 |
| `starter-guide` | Starter 레벨 가이드 |
| `bkend-expert` | Dynamic 레벨 BaaS 전문가 |
| `enterprise-expert` | Enterprise 레벨 전문가 |
| `infra-architect` | 인프라 아키텍처 설계 |
| `pipeline-guide` | 개발 파이프라인 안내 |
| `pdca-iterator` | PDCA 반복 실행 |

### 프로젝트 레벨별 구성

| | Starter | Dynamic | Enterprise |
|---|---------|---------|------------|
| **용도** | 정적 웹사이트 | 풀스택 앱 | 마이크로서비스 |
| **기본 에이전트** | starter-guide | bkend-expert | enterprise-expert |
| **팀 규모** | - | 최대 3명 | 최대 5명 |
| **출력 스타일** | bkit-learning | bkit-pdca-guide | bkit-enterprise |

### Hook 이벤트

| 이벤트 | 설명 |
|--------|------|
| `SessionStart` | 세션 시작 시 컨텍스트 초기화 |
| `PreToolUse` / `PostToolUse` | 도구 사용 전후 처리 |
| `UserPromptSubmit` | 사용자 입력 시 의도 감지 |
| `PreCompact` | 컨텍스트 압축 전 스냅샷 |
| `TaskCompleted` | 태스크 완료 시 자동 진행 |
| `TeammateIdle` | 팀원 유휴 시 재할당 |
| `SubagentStart` / `SubagentStop` | 서브에이전트 생명주기 |
| `Stop` | 세션 종료 처리 |

### 설정 파일

설치 후 프로젝트 내 `.claude/settings.json`에 자동 등록됩니다.

```json
{
  "enabledPlugins": {
    "bkit@bkit-marketplace": true
  }
}
```

## License

각 스킬 디렉토리의 `LICENSE.txt`를 참고하세요.
bkit 플러그인은 Apache-2.0 라이선스입니다.
