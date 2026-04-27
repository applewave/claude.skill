# Matt Pocock Skills

PRD, 이슈 분해, TDD, 코드베이스 개선 워크플로우입니다.

## 요약

- 스킬 수: 19
- 원본 위치: `mattpocock-skills`
- 스킬별 상세 문서: `docs/skills/mattpocock/`

| 영역 | 스킬 수 | 상세 |
|---|---:|---|
| mattpocock-skills | 19 | [상세 폴더](skills/mattpocock/mattpocock-skills/README.md) |

## mattpocock-skills

| 스킬 | 설명 | 상세 | 원본 |
|---|---|---|---|
| `design-an-interface` | Generate multiple radically different interface designs for a module using parallel sub-agents. Use when user wants to design an API, explore interface options, compare module shapes, or mentions "design it twice". | [상세](skills/mattpocock/mattpocock-skills/design-an-interface-b0fb0dc.md) | `mattpocock-skills/design-an-interface/SKILL.md` |
| `edit-article` | Edit and improve articles by restructuring sections, improving clarity, and tightening prose. Use when user wants to edit, revise, or improve an article draft. | [상세](skills/mattpocock/mattpocock-skills/edit-article-c9de866.md) | `mattpocock-skills/edit-article/SKILL.md` |
| `git-guardrails-claude-code` | Set up Claude Code hooks to block dangerous git commands (push, reset --hard, clean, branch -D, etc.) before they execute. Use when user wants to prevent destructive git operations, add git safety hooks, or block git push/reset in Claude Code. | [상세](skills/mattpocock/mattpocock-skills/git-guardrails-claude-code-4fd917d.md) | `mattpocock-skills/git-guardrails-claude-code/SKILL.md` |
| `github-triage` | Triage GitHub issues through a label-based state machine with interactive grilling sessions. Use when user wants to triage issues, review incoming bugs or feature requests, prepare issues for an AFK agent, or manage issue workflow. | [상세](skills/mattpocock/mattpocock-skills/github-triage-75e8f9d.md) | `mattpocock-skills/github-triage/SKILL.md` |
| `grill-me` | Interview the user relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. Use when user wants to stress-test a plan, get grilled on their design, or mentions "grill me". | [상세](skills/mattpocock/mattpocock-skills/grill-me-0ff0664.md) | `mattpocock-skills/grill-me/SKILL.md` |
| `improve-codebase-architecture` | Explore a codebase to find opportunities for architectural improvement, focusing on making the codebase more testable by deepening shallow modules. Use when user wants to improve architecture, find refactoring opportunities, consolidate tightly-coupled module... | [상세](skills/mattpocock/mattpocock-skills/improve-codebase-architecture-75a2551.md) | `mattpocock-skills/improve-codebase-architecture/SKILL.md` |
| `migrate-to-shoehorn` | Migrate test files from `as` type assertions to @total-typescript/shoehorn. Use when user mentions shoehorn, wants to replace `as` in tests, or needs partial test data. | [상세](skills/mattpocock/mattpocock-skills/migrate-to-shoehorn-f891ce5.md) | `mattpocock-skills/migrate-to-shoehorn/SKILL.md` |
| `obsidian-vault` | Search, create, and manage notes in the Obsidian vault with wikilinks and index notes. Use when user wants to find, create, or organize notes in Obsidian. | [상세](skills/mattpocock/mattpocock-skills/obsidian-vault-2adb166.md) | `mattpocock-skills/obsidian-vault/SKILL.md` |
| `prd-to-issues` | Break a PRD into independently-grabbable GitHub issues using tracer-bullet vertical slices. Use when user wants to convert a PRD to issues, create implementation tickets, or break down a PRD into work items. | [상세](skills/mattpocock/mattpocock-skills/prd-to-issues-24daae7.md) | `mattpocock-skills/prd-to-issues/SKILL.md` |
| `prd-to-plan` | Turn a PRD into a multi-phase implementation plan using tracer-bullet vertical slices, saved as a local Markdown file in ./plans/. Use when user wants to break down a PRD, create an implementation plan, plan phases from a PRD, or mentions "tracer bullets". | [상세](skills/mattpocock/mattpocock-skills/prd-to-plan-d90b855.md) | `mattpocock-skills/prd-to-plan/SKILL.md` |
| `qa` | Interactive QA session where user reports bugs or issues conversationally, and the agent files GitHub issues. Explores the codebase in the background for context and domain language. Use when user wants to report bugs, do QA, file issues conversationally, or... | [상세](skills/mattpocock/mattpocock-skills/qa-9d21ff4.md) | `mattpocock-skills/qa/SKILL.md` |
| `request-refactor-plan` | Create a detailed refactor plan with tiny commits via user interview, then file it as a GitHub issue. Use when user wants to plan a refactor, create a refactoring RFC, or break a refactor into safe incremental steps. | [상세](skills/mattpocock/mattpocock-skills/request-refactor-plan-24dff27.md) | `mattpocock-skills/request-refactor-plan/SKILL.md` |
| `scaffold-exercises` | Create exercise directory structures with sections, problems, solutions, and explainers that pass linting. Use when user wants to scaffold exercises, create exercise stubs, or set up a new course section. | [상세](skills/mattpocock/mattpocock-skills/scaffold-exercises-fc2a279.md) | `mattpocock-skills/scaffold-exercises/SKILL.md` |
| `setup-pre-commit` | Set up Husky pre-commit hooks with lint-staged (Prettier), type checking, and tests in the current repo. Use when user wants to add pre-commit hooks, set up Husky, configure lint-staged, or add commit-time formatting/typechecking/testing. | [상세](skills/mattpocock/mattpocock-skills/setup-pre-commit-f3c55a6.md) | `mattpocock-skills/setup-pre-commit/SKILL.md` |
| `tdd` | Test-driven development with red-green-refactor loop. Use when user wants to build features or fix bugs using TDD, mentions "red-green-refactor", wants integration tests, or asks for test-first development. | [상세](skills/mattpocock/mattpocock-skills/tdd-f07020a.md) | `mattpocock-skills/tdd/SKILL.md` |
| `triage-issue` | Triage a bug or issue by exploring the codebase to find root cause, then create a GitHub issue with a TDD-based fix plan. Use when user reports a bug, wants to file an issue, mentions "triage", or wants to investigate and plan a fix for a problem. | [상세](skills/mattpocock/mattpocock-skills/triage-issue-8e01cd0.md) | `mattpocock-skills/triage-issue/SKILL.md` |
| `ubiquitous-language` | Extract a DDD-style ubiquitous language glossary from the current conversation, flagging ambiguities and proposing canonical terms. Saves to UBIQUITOUS_LANGUAGE.md. Use when user wants to define domain terms, build a glossary, harden terminology, create a ubi... | [상세](skills/mattpocock/mattpocock-skills/ubiquitous-language-ae0664e.md) | `mattpocock-skills/ubiquitous-language/SKILL.md` |
| `write-a-prd` | Create a PRD through user interview, codebase exploration, and module design, then submit as a GitHub issue. Use when user wants to write a PRD, create a product requirements document, or plan a new feature. | [상세](skills/mattpocock/mattpocock-skills/write-a-prd-c88cc02.md) | `mattpocock-skills/write-a-prd/SKILL.md` |
| `write-a-skill` | Create new agent skills with proper structure, progressive disclosure, and bundled resources. Use when user wants to create, write, or build a new skill. | [상세](skills/mattpocock/mattpocock-skills/write-a-skill-b254ce2.md) | `mattpocock-skills/write-a-skill/SKILL.md` |
