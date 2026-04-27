# karpathy-guidelines

## 요약

Behavioral guidelines to reduce common LLM coding mistakes. Use when writing, reviewing, or refactoring code to avoid overcomplication, make surgical changes, surface assumptions, and define verifiable success criteria.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Karpathy Guidelines Skills |
| 영역 | andrej-karpathy-skills |
| 원본 경로 | `andrej-karpathy-skills/skills/karpathy-guidelines/SKILL.md` |
| 상세 파일 | `docs/skills/karpathy/andrej-karpathy-skills/karpathy-guidelines-45b558f.md` |
| 라이선스 | MIT |

## 언제 쓰나

Behavioral guidelines to reduce common LLM coding mistakes. Use when writing, reviewing, or refactoring code to avoid overcomplication, make surgical changes, surface assumptions, and define verifiable success criteria.

## 주요 내용

- **Think Before Coding**: 애매한 요구사항을 조용히 추측하지 않고, 가정과 해석을 먼저 드러냅니다. 여러 해석이 가능하면 선택지를 제시하고, 불확실하면 구현 전에 질문합니다.
- **Simplicity First**: 요청 범위를 넘는 기능, 단발성 추상화, 불필요한 설정 가능성, 과한 예외 처리를 피합니다. 같은 문제를 더 짧고 직접적인 코드로 풀 수 있으면 단순한 쪽을 우선합니다.
- **Surgical Changes**: 사용자 요청과 직접 연결되는 줄만 변경합니다. 주변 코드, 포맷, 주석, 기존 죽은 코드는 임의로 정리하지 않고, 변경으로 새로 생긴 unused 항목만 정리합니다.
- **Goal-Driven Execution**: 작업을 검증 가능한 목표로 바꿉니다. 버그 수정은 재현 테스트와 통과 조건으로, 리팩터링은 전후 테스트 통과로, 기능 추가는 성공 기준과 확인 루프로 관리합니다.

## 활용 예

- 코드 작성, 리뷰, 리팩터링 작업에서 과한 설계와 범위 이탈을 줄이고 싶을 때 사용합니다.
- 작업 전 “성공 기준”을 먼저 세우고, 변경 후 테스트나 명확한 확인 절차로 완료 여부를 검증할 때 적합합니다.
- 큰 변경보다 작은 변경, 빠른 추측보다 명시적 확인, 넓은 정리보다 필요한 부분만 고치는 방식을 선호해야 하는 작업에 어울립니다.

## 원본 문서 구조

- 1. Think Before Coding
- 2. Simplicity First
- 3. Surgical Changes
- 4. Goal-Driven Execution

## 관리 메모

- 이 문서는 원본 `andrej-karpathy-skills/skills/karpathy-guidelines/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
