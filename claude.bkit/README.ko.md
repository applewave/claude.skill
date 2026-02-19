# bkit - Vibecoding Kit

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-v2.1.33+-purple.svg)](https://docs.anthropic.com/en/docs/claude-code/getting-started)
[![Version](https://img.shields.io/badge/Version-1.5.5-green.svg)](CHANGELOG.md)
[![Author](https://img.shields.io/badge/Author-POPUP%20STUDIO-orange.svg)](https://popupstudio.ai)

> **PDCA 방법론 + CTO 주도 에이전트 팀 + AI 네이티브 개발을 위한 AI 코딩 어시스턴트 마스터리**

bkit은 AI를 활용한 소프트웨어 개발 방식을 혁신하는 Claude Code 플러그인입니다. PDCA(Plan-Do-Check-Act) 방법론을 통해 체계적인 개발 워크플로우, 자동 문서화, 지능형 코드 어시스턴스를 제공합니다.

![bkit 소개](images/bkit-intro.png)

---

## 컨텍스트 엔지니어링이란?

**컨텍스트 엔지니어링(Context Engineering)**은 최적의 LLM 추론을 위한 컨텍스트 토큰의 체계적 큐레이션입니다. 단순한 프롬프트 작성을 넘어 AI 동작을 일관되게 안내하는 전체 시스템을 구축합니다.

```
기존 프롬프트 엔지니어링:
  "좋은 프롬프트를 작성하는 기술"

컨텍스트 엔지니어링:
  "프롬프트, 도구, 상태를 통합하는 시스템을 설계하여
   LLM에 최적의 추론 컨텍스트를 제공하는 기술"
```

**bkit은 컨텍스트 엔지니어링의 실용적 구현체**로, Claude Code를 위한 체계적인 컨텍스트 관리 시스템을 제공합니다.

### bkit의 컨텍스트 엔지니어링 아키텍처

![bkit 컨텍스트 엔지니어링 아키텍처](images/bkit-architecture.png)

bkit은 세 가지 상호 연결된 레이어를 통해 컨텍스트 엔지니어링을 구현합니다:

| 레이어 | 구성 요소 | 목적 |
|--------|-----------|------|
| **도메인 지식** | 27개 스킬 | 구조화된 전문 지식 (단계, 레벨, 전문 도메인) |
| **행동 규칙** | 16개 에이전트 | 모델 선택을 포함한 역할 기반 제약 조건 (opus/sonnet/haiku) |
| **상태 관리** | 241개 함수 | PDCA 상태, 의도 감지, 모호성 점수, 다중 기능 컨텍스트, 팀 조율 |

### 5단계 훅 시스템

컨텍스트 주입은 다섯 개의 개별 레이어에서 발생합니다:

```
레이어 1: hooks.json (전역)      → SessionStart, UserPromptSubmit, PreCompact, PreToolUse, PostToolUse, Stop
레이어 2: 스킬 Frontmatter       → 도메인별 훅 (v1.4.4에서 폐기, hooks.json 사용)
레이어 3: 에이전트 Frontmatter   → 제약 조건을 포함한 태스크별 훅
레이어 4: Description 트리거     → 8개 언어 의미론적 매칭
레이어 5: 스크립트 (45개 모듈)   → 통합 핸들러를 사용한 실제 Node.js 실행 로직
```

> **더 알아보기**: 자세한 구현은 [컨텍스트 엔지니어링 원칙](bkit-system/philosophy/context-engineering.md)을 참조하세요.

---

## 기능

![bkit 기능](images/bkit-features.png)

- **Plan Plus 스킬 (v1.5.5)** - 의도 발견, 대안 탐색, YAGNI 검토를 포함한 브레인스토밍 강화 PDCA 계획
- **bkend MCP 정확도 수정 (v1.5.4)** - MCP 도구 커버리지 19→28+, 정확한 도구명, 동적 Base URL, search_docs 워크플로우
- **팀 가시성 및 상태 기록기 (v1.5.3)** - Studio IPC를 위한 `.bkit/agent-state.json` 에이전트 팀 상태 관리
- **SubagentStart/SubagentStop 훅 (v1.5.3)** - 에이전트 수명주기 추적을 위한 2개의 새로운 훅 이벤트 (총 10개 훅 이벤트)
- **아웃풋 스타일 자동 검색 (v1.5.3)** - plugin.json의 `outputStyles` + 4번째 스타일 `bkit-pdca-enterprise`
- **CTO 주도 에이전트 팀 (v1.5.1)** - CTO 에이전트가 다중 에이전트 팀으로 병렬 PDCA 실행 조율 (Dynamic: 3명, Enterprise: 5명)
- **아웃풋 스타일 (v1.5.1)** - 레벨 기반 응답 포맷팅 (bkit-learning, bkit-pdca-guide, bkit-enterprise, bkit-pdca-enterprise)
- **에이전트 메모리 (v1.5.1)** - 16개 전체 에이전트의 세션 간 컨텍스트 지속성 (자동 활성화)
- **자연스러운 기능 발견 (v1.5.1)** - "자동화 우선" 철학에 맞춘 자동 트리거 통합
- **태스크 관리 + PDCA 통합 (v1.4.7)** - 태스크 체인 자동 생성, 태스크 ID 지속성, Check↔Act 반복
- **코어 모듈화 (v1.4.7)** - lib/common.js를 5개 모듈로 분리 (lib/core/, lib/pdca/, lib/intent/, lib/task/, lib/team/)
- **컨텍스트 엔지니어링 (v1.4.4)** - 7개 라이브러리 모듈과 통합 훅 시스템을 통한 체계적 컨텍스트 큐레이션
- **PDCA 방법론** - 자동 문서화를 포함한 구조화된 개발 워크플로우
- **PDCA 스킬 통합 (v1.4.4)** - 8개 액션을 가진 통합 `/pdca` 스킬 (plan, design, do, analyze, iterate, report, status, next)
- **평가자-최적화 패턴** - Anthropic 에이전트 아키텍처의 자동 반복 사이클
- **9단계 개발 파이프라인** - 스키마 설계부터 배포까지
- **3가지 프로젝트 레벨** - Starter (정적), Dynamic (풀스택), Enterprise (마이크로서비스)
- **다국어 지원** - 8개 언어 (EN, KO, JA, ZH, ES, FR, DE, IT)
- **27개 스킬** - 다양한 개발 시나리오를 위한 도메인별 지식
- **16개 에이전트** - CTO 주도 팀 에이전트를 포함한 전문 AI 어시스턴트
- **45개 스크립트** - 통합 핸들러를 사용한 훅 실행 (hooks-json-integration)
- **241개 유틸리티 함수** - 상태 관리, 의도 감지, 태스크 추적, 팀 조율을 포함한 5개 모듈 라이브러리
- **Check-Act 반복 루프** - 최대 5회 반복의 자동 갭 분석 및 수정 사이클 (90% 임계값)

---

### Claude Code가 처음이신가요?

> **Claude Code를 처음 사용하시나요?**
>
> [bkit-starter](https://github.com/popup-studio-ai/bkit-starter)로 시작하세요!
>
> - 초보자 친화적 가이드
> - 프로그래밍 경험 불필요
> - 첫 프로젝트를 직접 만들어보기
>
> ```bash
> /plugin enable bkit-starter
> ```
>
> bkit은 bkit-starter를 마스터한 사용자를 위한 고급 확장 프로그램입니다.

---

## 요구 사항

| 요구 사항 | 최소 버전 | 비고 |
|-----------|:---------:|------|
| **Claude Code** | **v2.1.33+** | 필수. bkit은 v2.1.33에서 도입된 훅 이벤트(`TeammateIdle`, `TaskCompleted`)를 사용합니다. 이전 버전에서는 `hooks.json` 로드 시 유효성 검사 오류가 발생합니다. |
| Node.js | v18+ | 훅 스크립트 실행용 |
| Agent Teams (선택) | `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1` 설정 | CTO 주도 에이전트 팀 기능에만 필요 |

> **문제 해결**: 설치 후 `"Failed to load hooks"` 오류가 표시되면 Claude Code를 최신 버전으로 업데이트하세요:
> ```bash
> claude update
> ```

---

## 빠른 시작

> **참고**: bkit은 **Claude Code**용으로 설계되었습니다. Gemini CLI의 경우 [bkit-gemini](https://github.com/popup-studio-ai/bkit-gemini)를 참조하세요.

### 옵션 1: 마켓플레이스 설치 (권장)

bkit을 설치하는 가장 쉬운 방법은 Claude Code 마켓플레이스를 통하는 것입니다.

```bash
# 1단계: bkit 마켓플레이스 추가
/plugin marketplace add popup-studio-ai/bkit-claude-code

# 2단계: bkit 플러그인 설치
/plugin install bkit
```

#### 마켓플레이스 관리

`/plugin` 명령어를 사용하고 **Marketplaces** 탭으로 이동하여 플러그인 소스를 관리하세요:

![bkit 마켓플레이스](images/bkit-marketplace.png)

- **bkit-marketplace**: bkit과 bkit-starter 플러그인 포함
- **claude-plugins-official**: Anthropic 공식 플러그인

#### 플러그인 검색

**Discover** 탭으로 이동하여 사용 가능한 플러그인을 검색하고 설치하세요:

![bkit 마켓플레이스 플러그인](images/bkit-marketplace-plugins.png)

| 플러그인 | 설명 | 대상 |
|----------|------|------|
| **bkit** | 전체 PDCA 방법론 + Claude Code 마스터리 | 숙련된 개발자 |
| **bkit-starter** | 초보자를 위한 한국어 학습 가이드 | Claude Code 입문자 |

#### 자동 업데이트 설정

설정에서 자동 업데이트를 구성하여 플러그인을 자동으로 최신 상태로 유지하세요:

```json
// ~/.claude/settings.json
{
  "plugins": {
    "autoUpdate": true
  }
}
```

**업데이트 명령어:**
- Marketplaces 뷰에서 `u`를 눌러 모든 플러그인 업데이트
- `r`을 눌러 마켓플레이스 제거
- Discover 뷰에서 `Space`를 사용하여 플러그인 선택 토글

### 플러그인 구조

```
bkit-claude-code/
├── .claude-plugin/
│   ├── plugin.json          # Claude Code 플러그인 매니페스트
│   └── marketplace.json     # 마켓플레이스 레지스트리
├── agents/                  # 전문 AI 에이전트
├── skills/                  # 도메인 지식
├── hooks/                   # 이벤트 훅 (hooks.json)
├── scripts/                 # 훅 실행 스크립트
├── lib/                     # 공유 유틸리티 (5개 모듈)
├── output-styles/           # 레벨 기반 응답 포맷팅
├── templates/               # 문서 템플릿
└── bkit.config.json         # 중앙 집중식 설정
```

---

## 커스터마이징

마켓플레이스를 통해 bkit을 설치한 후, 프로젝트의 `.claude/` 폴더에 복사하여 모든 컴포넌트를 커스터마이징할 수 있습니다.

> **종합 가이드**: 조직에 맞게 bkit을 커스터마이징하는 자세한 안내(플랫폼별 경로, 컴포넌트 예제, 라이선스 귀속 요구 사항 포함)는 **[CUSTOMIZATION-GUIDE.md](CUSTOMIZATION-GUIDE.md)**를 참조하세요.

### 동작 원리

Claude Code는 다음 우선순위로 설정 파일을 검색합니다:
1. **프로젝트 `.claude/`** (최우선 - 사용자 커스터마이징)
2. **사용자 `~/.claude/`**
3. **플러그인 설치** (기본값)

### 커스터마이징 단계

```bash
# 1단계: 플러그인 설치 위치 확인
ls ~/.claude/plugins/bkit/

# 2단계: 커스터마이징할 파일만 복사
mkdir -p .claude/skills/starter
cp ~/.claude/plugins/bkit/skills/starter/SKILL.md .claude/skills/starter/

# 3단계: 프로젝트에서 복사한 파일 편집
# 프로젝트의 .claude/skills/starter/SKILL.md가 플러그인 버전을 오버라이드합니다

# 4단계: 버전 관리에 커밋 (선택)
git add .claude/
git commit -m "feat: customize bkit starter skill"
```

### 커스터마이징 가능 컴포넌트

| 컴포넌트 | 위치 | 설명 |
|----------|------|------|
| **스킬** | `~/.claude/plugins/bkit/skills/` | 도메인 지식, 컨텍스트 및 슬래시 명령어 (예: `/pdca plan`) |
| **에이전트** | `~/.claude/plugins/bkit/agents/` | 전문 AI 어시스턴트 |
| **템플릿** | `~/.claude/plugins/bkit/templates/` | 문서 템플릿 |
| **스크립트** | `~/.claude/plugins/bkit/scripts/` | 훅 스크립트 |
| **설정** | `~/.claude/plugins/bkit/bkit.config.json` | 중앙 설정 |

### 주의 사항

- **커스터마이징된 파일은 플러그인 업데이트를 받지 않습니다.** bkit이 업데이트되면 커스터마이징된 파일은 그대로 유지되고, 커스터마이징하지 않은 파일만 자동 업데이트됩니다.
- 커스터마이징에 영향을 줄 수 있는 업데이트를 위해 **[CHANGELOG](CHANGELOG.md)**를 주기적으로 확인하세요.
- **커스터마이징된 파일을 삭제**하면 플러그인의 기본 버전으로 되돌립니다.
- **귀속 표기 필수**: 파생 플러그인을 만들 때는 [라이선스 & 귀속](CUSTOMIZATION-GUIDE.md#license--attribution) 가이드라인을 따르세요.

---

## 사용법

### 학습 시작
```bash
/claude-code-learning
```

### 프로젝트 초기화
```bash
/starter      # 정적 웹사이트 (Starter 레벨)
/dynamic      # BaaS 기반 풀스택 (Dynamic 레벨)
/enterprise   # K8s 기반 마이크로서비스 (Enterprise 레벨)
```

### PDCA 워크플로우 (v1.4.4 - 스킬 기반)
```bash
/pdca plan {기능명}     # 계획 문서 생성
/pdca design {기능명}   # 설계 문서 생성
/pdca do {기능명}       # 구현 가이드
/pdca analyze {기능명}  # 갭 분석 실행
/pdca iterate {기능명}  # 평가자-최적화 패턴으로 자동 수정
/pdca report {기능명}   # 완료 보고서 생성
/pdca status             # 현재 PDCA 상태 확인
/pdca next               # 다음 PDCA 단계 안내
```

### CTO 주도 에이전트 팀 (v1.5.1)

CTO 주도 에이전트 팀은 CTO 리드 에이전트가 조율하는 다수의 AI 에이전트로 병렬 PDCA 실행을 가능하게 합니다.

```bash
# 기능에 대한 CTO 팀 시작
/pdca team {기능명}

# 팀 진행 상황 모니터링
/pdca team status

# 팀 리소스 정리
/pdca team cleanup
```

**동작 방식:**
1. CTO 리드 에이전트(opus)가 기능을 분석하고 최적의 팀 구성을 선택
2. 팀원이 병렬로 생성됨 (Dynamic: 3명, Enterprise: 5명)
3. 각 팀원이 특정 영역을 담당 (QA, 프론트엔드, 백엔드, 보안 등)
4. CTO가 태스크 할당, 진행 모니터링, 결과 집계를 조율
5. 작업 완료 후 팀 정리

**요구 사항:**
- 환경 변수 설정: `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`
- Claude Code v2.1.32+

**사용 가능한 팀 에이전트 (신규 5개):**

| 에이전트 | 모델 | 역할 |
|----------|------|------|
| cto-lead | opus | 팀 조율, PDCA 워크플로우 관리 |
| frontend-architect | sonnet | UI/UX 설계, 컴포넌트 아키텍처 |
| product-manager | sonnet | 요구 사항 분석, 기능 우선순위 결정 |
| qa-strategist | sonnet | 테스트 전략, 품질 지표 조율 |
| security-architect | opus | 취약점 분석, 인증 설계 검토 |

---

## 프로젝트 레벨

| 레벨 | 설명 | 기술 스택 |
|------|------|-----------|
| **Starter** | 정적 웹사이트, 포트폴리오 | HTML, CSS, JS |
| **Dynamic** | 풀스택 애플리케이션 | Next.js, BaaS |
| **Enterprise** | 마이크로서비스 아키텍처 | K8s, Terraform, MSA |

---

## bkit은 개발 전용인가요?

![비개발 용도의 bkit](images/to-use-non-development.png)

bkit은 **주로 소프트웨어 개발을 위해 설계**되었습니다. 그러나 일부 컴포넌트는 코딩 외의 구조화된 워크플로우에 영감을 줄 수 있습니다:

| 컴포넌트 | 개발 외 활용 |
|----------|-------------|
| **PDCA 방법론** | 프로젝트 관리, 프로세스 개선 |
| **문서 템플릿** | 모든 구조화된 프로젝트 계획 |
| **갭 분석** | 모든 계획 대 실제 결과 비교 |

> **참고**: 일반적인 글쓰기, 연구, 비기술적 작업에는 bkit 없는 일반 Claude Code가 더 적합합니다.

---

## 문서

### 커스터마이징 가이드

- **[CUSTOMIZATION-GUIDE.md](CUSTOMIZATION-GUIDE.md)** - 조직에 맞게 bkit을 커스터마이징하는 종합 가이드
  - 플랫폼별 설정 경로 (macOS, Linux, Windows, WSL)
  - 컴포넌트 커스터마이징 (에이전트, 스킬, 명령어, 훅, 템플릿)
  - 파생 작업을 위한 라이선스 귀속 요구 사항
  - bkit 설계 철학 및 아키텍처 결정

### 현재 레퍼런스 (bkit-system/)

- **[시스템 아키텍처](bkit-system/README.md)** - 플러그인 구조 및 트리거 시스템 개요
- **[컨텍스트 엔지니어링](bkit-system/philosophy/context-engineering.md)** - LLM 컨텍스트 큐레이션 원칙 (v1.4.2)
- **[핵심 미션 & 철학](bkit-system/philosophy/core-mission.md)** - 3가지 핵심 철학 (자동화 우선, 추측 금지, 문서=코드)
- **[AI 네이티브 원칙](bkit-system/philosophy/ai-native-principles.md)** - AI 네이티브 개발과 3가지 핵심 역량
- **[PDCA 방법론](bkit-system/philosophy/pdca-methodology.md)** - PDCA 사이클과 9단계 파이프라인 관계
- **[그래프 인덱스](bkit-system/_GRAPH-INDEX.md)** - Obsidian 최적화 컴포넌트 그래프

### 컴포넌트 레퍼런스

- [개발 파이프라인](skills/development-pipeline/SKILL.md) - 9단계 파이프라인 스킬
- [스킬 레퍼런스](skills/) - 27개 도메인 스킬 (v1.4.4에서 명령어 폐기)
- [에이전트 레퍼런스](agents/) - 16개 전문 에이전트 (CTO 팀 에이전트 5개 포함)

### PDCA 문서

- [활성 PDCA](docs/pdca/) - 현재 계획/설계/분석 문서
- [아카이브](docs/archive/) - 완료된 PDCA + 레거시 문서

### 기타

- **[변경 이력](CHANGELOG.md)** - 버전 히스토리 및 릴리스 노트

### Obsidian으로 시각화

`bkit-system/` 문서는 [Obsidian](https://obsidian.md/)의 그래프 뷰에 최적화되어 있습니다:

1. `bkit-system/`을 Obsidian 볼트로 열기
2. `Ctrl/Cmd + G`를 눌러 그래프 뷰 열기
3. 컴포넌트 관계를 시각적으로 탐색

자세한 안내는 **[bkit-system/README.md](bkit-system/README.md#viewing-with-obsidian)**를 참조하세요.

---

## 언어 지원

bkit은 트리거 키워드를 통해 자동으로 언어를 감지합니다:

| 언어 | 트리거 키워드 |
|------|--------------|
| 영어 | static website, beginner, API design |
| 한국어 | 정적 웹, 초보자, API 설계 |
| 일본어 | 静的サイト, 初心者, API設計 |
| 중국어 | 静态网站, 初学者, API设计 |
| 스페인어 | sitio web estático, principiante |
| 프랑스어 | site web statique, débutant |
| 독일어 | statische Webseite, Anfänger |
| 이탈리아어 | sito web statico, principiante |

### 응답 언어 설정

Claude Code는 설정 파일의 `language` 설정을 통해 선호하는 응답 언어를 구성할 수 있습니다.

#### 설정 파일 (우선순위)

| 파일 | 범위 | Git 추적 |
|------|------|----------|
| `.claude/settings.local.json` | 프로젝트 (개인) | 아니오 (gitignore) |
| `.claude/settings.json` | 프로젝트 (공유) | 예 |
| `~/.claude/settings.json` | 사용자 (전역) | 해당 없음 |

#### 설정 방법

아무 설정 파일에나 `language` 키를 추가하세요:

```json
{
  "language": "korean"
}
```

#### 지원 언어

| 언어 | 설정 값 |
|------|---------|
| 영어 | `"english"` (기본값) |
| 한국어 | `"korean"` |
| 일본어 | `"japanese"` |
| 중국어 | `"chinese"` |
| 스페인어 | `"spanish"` |
| 프랑스어 | `"french"` |
| 독일어 | `"german"` |
| 이탈리아어 | `"italian"` |

> **참고**: 트리거 키워드는 모든 언어에서 작동합니다. `language` 설정은 Claude의 응답 언어에만 영향을 줍니다.

---

## 기여하기

기여를 환영합니다! 가이드라인은 [CONTRIBUTING.md](CONTRIBUTING.md)를 참조하세요.

### 브랜치 보호

- `admin` 팀 멤버만 `main`에 병합 가능
- 모든 변경 사항은 풀 리퀘스트 검토 필요
- 버전 릴리스는 Git 태그를 통해 관리

---

## 라이선스

Copyright 2024-2026 POPUP STUDIO PTE. LTD.

Apache License, Version 2.0에 따라 라이선스가 부여됩니다. 자세한 내용은 [LICENSE](LICENSE)를 참조하세요.

재배포 시 [NOTICE](NOTICE) 파일을 반드시 포함해야 합니다.

---

## 지원

- **이슈**: [GitHub Issues](https://github.com/popup-studio-ai/bkit-claude-code/issues)
- **이메일**: contact@popupstudio.ai

---

Made with AI by [POPUP STUDIO](https://popupstudio.ai)
