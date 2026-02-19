# claude.skill

AI 코딩 에이전트(OpenAI Codex 등)에서 사용하는 **Figma 연동 스킬 및 커맨드** 모음입니다.
Figma MCP 서버를 통해 디자인 시안을 분석하고, 프로덕션 코드로 변환하는 워크플로우를 제공합니다.

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

## License

각 스킬 디렉토리의 `LICENSE.txt`를 참고하세요.
