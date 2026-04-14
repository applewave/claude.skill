# Skill Catalog

이 프로젝트에 수집된 스킬/플러그인 저장소 목록과 주요 스킬 가이드.

---

## 클론된 저장소

| 디렉토리 | 출처 | 설명 |
|----------|------|------|
| `skills/` | https://github.com/anthropics/skills | Anthropic 공식 스킬 모음 |
| `knowledge-work-plugins/` | https://github.com/anthropics/knowledge-work-plugins | Anthropic 공식 지식 업무 플러그인 |
| `Problem-Based-SRS/` | https://github.com/RafaelGorski/Problem-Based-SRS | 문제 기반 SRS 방법론 |
| `spec-kit-brownfield-extensions/` | https://github.com/wcpaxx/spec-kit-brownfield-extensions | Brownfield 확장용 spec kit |
| `sf-skills/` | https://github.com/Jaganpro/sf-skills | Salesforce 관련 스킬 |
| `mattpocock-skills/` | https://github.com/mattpocock/skills | Matt Pocock의 스킬 모음 |

---

## 추천 스킬: 화면 → 개발 요구사항 변환

화면(스크린샷/Figma)을 개발 가능한 문서로 바꾸는 워크플로우. 아래 순서로 사용하면 효과적.

### Step 1. design-critique — 빠진 요구사항 먼저 잡기

- **경로**: `knowledge-work-plugins/design/skills/design-critique/SKILL.md`
- **입력**: 스크린샷 또는 Figma
- **출력**: usability, hierarchy, consistency, accessibility 관점 구조화 피드백
- **언제 쓰나**: 본격적인 명세 작성 전에 "이 상태값이 빠졌네", "예외 케이스가 없네", "CTA 우선순위가 애매하네" 같은 문제를 먼저 발견할 때

### Step 2. handoff — 화면을 개발 스펙으로 변환

- **경로**: `knowledge-work-plugins/design/skills/handoff/SKILL.md`
- **입력**: 화면 설명, 스크린샷 (Figma URL 없어도 됨)
- **출력**: developer handoff spec
  - layout, design tokens, component props
  - interaction states, responsive breakpoints
  - edge cases, accessibility
- **언제 쓰나**: 화면을 보고 개발 요구사항으로 바꿀 때 가장 직접적

### Step 3. write-spec — PRD/요구사항 문서로 정리

- **경로**: `knowledge-work-plugins/product-management/skills/write-spec/SKILL.md`
- **입력**: problem statement 또는 feature idea (handoff 결과를 입력으로 쓸 수 있음)
- **출력**: structured PRD
  - goals, non-goals
  - user stories
  - requirements + acceptance criteria
  - success metrics, open questions, timeline
- **언제 쓰나**: 화면 분석 결과를 제품 요구사항 문서로 고정할 때

---

## 추천 스킬: 기획 → 개발 파이프라인 (mattpocock-skills)

PRD 작성부터 이슈 분해, TDD 개발, 코드베이스 개선까지 이어지는 워크플로우.

### /grill-me — 계획/설계 스트레스 테스트

- **경로**: `mattpocock-skills/grill-me/SKILL.md`
- **용도**: 계획이나 설계안에 대해 집요하게 질문받으며 허점을 찾는 인터뷰
- **특징**: 결정 트리의 각 분기를 하나씩 해소. 코드베이스에서 답을 찾을 수 있는 질문은 직접 탐색
- **언제 쓰나**: PRD 작성 전이나 설계 리뷰 때 "이거 진짜 맞나?" 확인하고 싶을 때

### /write-a-prd — PRD 작성

- **경로**: `mattpocock-skills/write-a-prd/SKILL.md`
- **용도**: 사용자 인터뷰 + 코드베이스 탐색 → PRD → GitHub 이슈 등록
- **출력**: Problem Statement, Solution, User Stories, Implementation Decisions, Testing Decisions, Out of Scope
- **특징**: deep module 설계(작은 인터페이스, 큰 구현)를 지향. 사용자와 모듈 단위로 합의 후 작성
- **언제 쓰나**: 새 기능을 체계적으로 정의하고 GitHub 이슈로 남길 때

### /prd-to-issues — PRD를 이슈로 분해

- **경로**: `mattpocock-skills/prd-to-issues/SKILL.md`
- **용도**: PRD를 vertical slice(tracer bullet) 방식으로 GitHub 이슈로 분해
- **특징**:
  - 수평(레이어별)이 아니라 수직(end-to-end) 슬라이스
  - HITL(사람 필요) vs AFK(자동 진행) 구분
  - 의존 관계 명시, blocker 순서대로 이슈 생성
- **언제 쓰나**: PRD 승인 후 실제 작업 단위로 쪼갤 때

### /tdd — 테스트 주도 개발

- **경로**: `mattpocock-skills/tdd/SKILL.md`
- **용도**: Red-Green-Refactor 루프로 기능 구현
- **핵심 원칙**:
  - 테스트는 public interface의 behavior만 검증 (구현 아님)
  - 수평 슬라이스 금지 (테스트 몰아 쓰고 구현 몰아 쓰기 X)
  - 한 번에 테스트 하나 → 구현 하나 → 반복
- **언제 쓰나**: 이슈 하나를 실제로 구현할 때

### /improve-codebase — 코드베이스 아키텍처 개선

- **경로**: `mattpocock-skills/improve-codebase-architecture/SKILL.md`
- **용도**: shallow module을 deep module로 리팩터링할 기회 탐색
- **프로세스**: 코드베이스 탐색 → 후보 제시 → 3개 이상 인터페이스 병렬 설계 → 비교 추천 → GitHub RFC 이슈 생성
- **언제 쓰나**: "이 코드 구조가 뭔가 불편한데" 싶을 때. 테스트하기 어렵거나 파일 간 결합이 심한 부분 개선

### 파이프라인 흐름

```
/grill-me → /write-a-prd → /prd-to-issues → /tdd (이슈별 반복) → /improve-codebase
   ↓              ↓               ↓                ↓                    ↓
 허점 발견     PRD 작성      이슈 분해        구현+테스트        아키텍처 개선
```

---

## 사용 예제: 화면 → handoff → PRD 전체 흐름

실제로 스크린샷 하나를 가지고 Step 2 → Step 3을 순서대로 실행하는 예시.

### 예제 프롬프트 1: handoff spec 작성

```
이 화면 스크린샷을 기준으로 design-handoff 방식으로 개발 handoff spec을 작성해줘.
출력은 화면 목적, UI 섹션, 상태/액션 매트릭스, 데이터 필드, validation,
empty/loading/error, responsive, accessibility, open questions 순서로 정리해줘.
```

> 스크린샷 파일 경로 또는 이미지를 함께 첨부한다.

### 예제 프롬프트 2: PRD 변환

```
방금 결과를 write-spec 방식으로 PRD로 변환해줘.
Goals, Non-goals, User stories, P0/P1/P2 requirements, acceptance criteria,
success metrics, timeline까지 포함해줘.
```

### 워크플로우 요약

```
[스크린샷] → design-critique(선택) → handoff spec → write-spec PRD
                 ↓                       ↓                ↓
          빠진 요구사항 발견      개발 스펙 문서       제품 요구사항 문서
```
