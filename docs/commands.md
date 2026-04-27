# Commands

이 저장소에 포함된 slash command 문서입니다.

| 이름 | 설명 | 경로 |
|---|---|---|
| `/analyze` | **인자**: `$ARGUMENTS` = `<page> [nodeId]` (예: `login 525:678`, `mypage`) | `commands.figma/analyze.md` |
| `/new-page` | **인자**: `$ARGUMENTS` = `<page> <korean-name> <section>` (예: `login 로그인 member`, `mypage 마이페이지 member`) | `commands.figma/new-page.md` |
| `/publish` | **인자**: `$ARGUMENTS` = `<page>` (예: `login`, `mypage`) | `commands.figma/publish.md` |
| `/verify` | **인자**: `$ARGUMENTS` = `<page>` (예: `main`, `plp`, `pdp`, `cart`, `offline`) | `commands.figma/verify.md` |
| `/analyze` | **인자**: `$ARGUMENTS` = `<page> [nodeId]` (예: `login 525:678`, `mypage`) | `commands/analyze.md` |
| `/new-page` | **인자**: `$ARGUMENTS` = `<page> <korean-name> <section>` (예: `login 로그인 member`, `mypage 마이페이지 member`) | `commands/new-page.md` |
| `/publish` | **인자**: `$ARGUMENTS` = `<page>` (예: `login`, `mypage`) | `commands/publish.md` |
| `/verify` | **인자**: `$ARGUMENTS` = `<page>` (예: `main`, `plp`, `pdp`, `cart`, `offline`) | `commands/verify.md` |

## Plugin Commands

### mafia-codereview

| 이름 | 제목 | 설명 | 경로 |
|---|---|---|---|
| `/mafia-codereview:auto` | 코드리뷰 파이프라인 | 전체 코드리뷰 파이프라인을 오케스트레이션한다. | `mafia-codereview-harness/plugin/commands/auto.md` |
| `/mafia-codereview:create-pr-body` | PR 본문 생성 | 구현 완료된 코드의 git diff와 spec 변경사항을 기반으로 PR 본문을 생성한다. | `mafia-codereview-harness/plugin/commands/create-pr-body.md` |
| `/mafia-codereview:gen-criteria` | 평가기준 생성 | 작업 설계를 분석하고, `docs/adr.yaml`에서 관련 항목을 추출하여 `docs/code-convention.yaml`과 병합된 평가기준 문서를 생성한다. | `mafia-codereview-harness/plugin/commands/gen-criteria.md` |
| `/mafia-codereview:reflect-review` | 리뷰 반영 | 코드리뷰 코멘트를 검토하고, 수용 여부를 판단하여 코드를 수정한다. | `mafia-codereview-harness/plugin/commands/reflect-review.md` |
| `/mafia-codereview:review` | 코드리뷰 실행 | 평가기준, 설계의도, PR 본문, git diff를 입력받아 근거 기반 코드리뷰를 수행한다. | `mafia-codereview-harness/plugin/commands/review.md` |
| `/mafia-codereview:update-docs` | 문서 업데이트 (code-convention / ADR) | `docs/code-convention.yaml` 또는 `docs/adr.yaml`에 항목을 추가/수정/삭제한다. | `mafia-codereview-harness/plugin/commands/update-docs.md` |
| `/mafia-codereview:write-intent` | 설계의도 문서 작성 | 현재 대화에서 논의된 설계 내용을 기반으로 설계의도 문서를 작성한다. | `mafia-codereview-harness/plugin/commands/write-intent.md` |
