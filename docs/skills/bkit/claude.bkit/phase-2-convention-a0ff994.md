# phase-2-convention

## 요약

Skill for defining coding rules and conventions. Ensures consistent code style and specifies coding standards for AI collaboration. Use proactively when starting a new project or when coding standards are needed. Triggers: convention, coding style, naming rules, 컨벤션, コンベンション, 编码风格, convención, estilo de código, reglas de nombrado, convention, style de codage, règles de nommage, Konvention, Coding-Stil, Namensregeln, convenzione, stile di codice, regole di denominazione Do NOT use for: existing projects with established conventions, deployment, or testing.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/phase-2-convention/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/phase-2-convention-a0ff994.md` |
| 사용자 호출 | false |

## 언제 쓰나

Skill for defining coding rules and conventions. Ensures consistent code style and specifies coding standards for AI collaboration. Use proactively when starting a new project or when coding standards are needed. Triggers: convention, coding style, naming rules, 컨벤션, コンベンション, 编码风格, convención, estilo de código, reglas de nombrado, convention, style de codage, règles de nommage, Konvention, Coding-Stil, Namensregeln, convenzione, stile di codice, regole di denominazione Do NOT use for: existing projects with established conventions, deployment, or testing.

## 주요 내용

- **진행 방식**: Why Define at Design Stage? Clean Architecture = Code resilient to change ❌ Developing without architecture → Spaghetti code, multiple file changes for each modification ✅ Define layers at design stage → Separation of concerns, easy testing, easy maintenance 4-Layer Architecture (Recommended) src/ ├── presentation/ # or app/, pages/ │ ├── components/ # UI components │ ├── hooks/ # State management hooks │ └── pages/ # Page components │ ├── application/ # or services/, features/ │ ├── use-cases/ # Business use cases │ └── services/ # API service wrappers │ ├── domain/ # or types/, entities/ │ ├── entities/ # Domain entities │ ├── types/ # Type definitions │ └── constants/ # Domain constants │ └── infrastructure/ # or lib/, api/ ├── api/ # API clients ├── db/ # Database connections └── external/ # External services Layer Responsibilities and Rules Dependency Rule
- **산출물**: Project Root/ ├── CONVENTIONS.md # Full conventions └── docs/01-plan/ ├── naming.md # Naming rules └── structure.md # Structure rules

## 원본 문서 구조

- Purpose
- What to Do in This Phase
- Deliverables
- PDCA Application
- Level-wise Application
- Core Convention Items
  - Naming
  - Folder Structure
- Environment Variable Convention
  - Why Define at Design Stage?
  - Environment Variable Naming Rules
  - .env File Structure
  - .env.example Template
  - Environment-wise Value Classification
  - Environment Variable Validation
  - Environment Variable Checklist
- Clean Architecture Principles
  - Why Define at Design Stage?
  - 4-Layer Architecture (Recommended)
  - Layer Responsibilities and Rules
  - Dependency Rule
  - File Import Rules
  - Level-wise Application
  - Starter Level Folder Structure
  - Dynamic Level Folder Structure
  - Enterprise Level Folder Structure
- Phase Connection
- Template
- Next Phase
- 6. Reusability Principles
  - 6.1 Function Design
    - Creating Generic Functions
    - Parameter Generalization
  - 6.2 Component Design
    - Composable Components
    - Props Extensibility

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/phase-2-convention/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
