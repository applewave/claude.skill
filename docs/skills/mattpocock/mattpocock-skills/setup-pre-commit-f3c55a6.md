# setup-pre-commit

## 요약

Set up Husky pre-commit hooks with lint-staged (Prettier), type checking, and tests in the current repo. Use when user wants to add pre-commit hooks, set up Husky, configure lint-staged, or add commit-time formatting/typechecking/testing.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/setup-pre-commit/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/setup-pre-commit-f3c55a6.md` |

## 언제 쓰나

Set up Husky pre-commit hooks with lint-staged (Prettier), type checking, and tests in the current repo. Use when user wants to add pre-commit hooks, set up Husky, configure lint-staged, or add commit-time formatting/typechecking/testing.

## 주요 내용

- **진행 방식**: 1. Detect package manager Check for `package-lock.json` (npm), `pnpm-lock.yaml` (pnpm), `yarn.lock` (yarn), `bun.lockb` (bun). Use whichever is present. Default to npm if unclear. 2. Install dependencies Install as devDependencies: husky lint-staged prettier 3. Initialize Husky npx husky init This creates `.husky/` dir and adds `prepare: "husky"` to package.json. 4. Create `.husky/pre-commit` Write this file (no shebang needed for Husky v9+): npx lint-staged npm run typecheck npm run test **Adapt**: Replace `npm` with detected package manager. If repo has no `typecheck` or `test` script in package.json, omit those lines and tell the user. 5. Create `.lintstagedrc` { "*": "prettier --ignore-unknown --write" } 6. Create `.prettierrc` (if missing) Only create if no Prettier config exists. Use these defaults: { "useTabs": false, "tabWidth": 2, "printWidth": 80, "singleQuote": false, "trailingComma": "es5", "semi": true, "arrowParens": "always" } 7. Verify [ ] `.husky/pre-commit` exists an...

## 원본 문서 구조

- What This Sets Up
- Steps
  - 1. Detect package manager
  - 2. Install dependencies
  - 3. Initialize Husky
  - 4. Create `.husky/pre-commit`
  - 5. Create `.lintstagedrc`
  - 6. Create `.prettierrc` (if missing)
  - 7. Verify
  - 8. Commit
- Notes

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/setup-pre-commit/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
