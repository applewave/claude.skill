# Mafia Code-Review Harness

Claude Code 기반 코드리뷰 자동화 파이프라인 플러그인입니다. 설계의도 문서화, 평가기준 생성, PR 본문 작성, 근거 기반 코드리뷰, 리뷰 반영과 QA를 하나의 흐름으로 묶습니다.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 이름 | `mafia-codereview` |
| 설명 | Claude Code 기반 코드리뷰 자동화 파이프라인. 평가기준 자동 생성, 설계의도 문서화, 근거 기반 코드리뷰를 자동화합니다. |
| 버전 | 0.1.0 |
| 작성자 | vibemafiaclub |
| 라이선스 | MIT |
| 원본 | `mafia-codereview-harness` |
| 저장소 | https://github.com/vibemafiaclub/mafia-codereview-harness |

## 설치

Claude Code에서 marketplace를 추가한 뒤 플러그인을 설치합니다.

```text
/plugin marketplace add vibemafiaclub/mafia-codereview-harness
/plugin install mafia-codereview
```

## 사전 준비

- 대상 프로젝트에 `docs/code-convention.yaml`을 준비합니다.
- 대상 프로젝트에 `docs/adr.yaml`을 준비합니다.
- 구현이 완료된 feature branch에서 실행합니다.

## 파이프라인

1. `/mafia-codereview:auto`로 전체 파이프라인을 시작합니다.
2. 현재 브랜치와 base branch, 변경 파일을 확인합니다.
3. `write-intent`가 설계의도 문서를 작성합니다.
4. `gen-criteria`가 code convention과 ADR 기반 평가기준을 만듭니다.
5. `create-pr-body`가 git diff 기반 PR 본문을 만듭니다.
6. `review`가 기준, 설계의도, PR 본문, diff를 바탕으로 코드리뷰를 수행합니다.
7. `reflect-review`가 리뷰 반영 여부를 판단하고 QA 루프를 진행합니다.

## 산출물

작업별 산출물은 대상 프로젝트의 `.review-artifacts/{branch-name}/`에 저장됩니다.

| 산출물 | 생성 단계 |
|---|---|
| `design-intent.md` | 설계의도 작성 |
| `code-quality-guide.md` | 평가기준 생성 |
| `pr-body.md` | PR 본문 생성 |
| `review-comments.md` | 코드리뷰 실행 및 리뷰 반영 |

## 커맨드 목록

| 커맨드 | 제목 | 설명 | 원본 |
|---|---|---|---|
| `/mafia-codereview:auto` | 코드리뷰 파이프라인 | 전체 코드리뷰 파이프라인을 오케스트레이션한다. | `mafia-codereview-harness/plugin/commands/auto.md` |
| `/mafia-codereview:create-pr-body` | PR 본문 생성 | 구현 완료된 코드의 git diff와 spec 변경사항을 기반으로 PR 본문을 생성한다. | `mafia-codereview-harness/plugin/commands/create-pr-body.md` |
| `/mafia-codereview:gen-criteria` | 평가기준 생성 | 작업 설계를 분석하고, `docs/adr.yaml`에서 관련 항목을 추출하여 `docs/code-convention.yaml`과 병합된 평가기준 문서를 생성한다. | `mafia-codereview-harness/plugin/commands/gen-criteria.md` |
| `/mafia-codereview:reflect-review` | 리뷰 반영 | 코드리뷰 코멘트를 검토하고, 수용 여부를 판단하여 코드를 수정한다. | `mafia-codereview-harness/plugin/commands/reflect-review.md` |
| `/mafia-codereview:review` | 코드리뷰 실행 | 평가기준, 설계의도, PR 본문, git diff를 입력받아 근거 기반 코드리뷰를 수행한다. | `mafia-codereview-harness/plugin/commands/review.md` |
| `/mafia-codereview:update-docs` | 문서 업데이트 (code-convention / ADR) | `docs/code-convention.yaml` 또는 `docs/adr.yaml`에 항목을 추가/수정/삭제한다. | `mafia-codereview-harness/plugin/commands/update-docs.md` |
| `/mafia-codereview:write-intent` | 설계의도 문서 작성 | 현재 대화에서 논의된 설계 내용을 기반으로 설계의도 문서를 작성한다. | `mafia-codereview-harness/plugin/commands/write-intent.md` |

## 상세 문서

- [커맨드 상세 색인](plugin-commands/mafia-codereview/README.md)
