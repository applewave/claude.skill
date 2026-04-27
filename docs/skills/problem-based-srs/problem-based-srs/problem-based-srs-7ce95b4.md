# problem-based-srs

## 요약

Complete Problem-Based Software Requirements Specification methodology following Gorski & Stadzisz research. Use when you need to perform requirements engineering from business problems to functional requirements with full traceability.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Problem-Based SRS Skills |
| 영역 | Problem-Based-SRS |
| 원본 경로 | `Problem-Based-SRS/skills/problem-based-srs/SKILL.md` |
| 상세 파일 | `docs/skills/problem-based-srs/problem-based-srs/problem-based-srs-7ce95b4.md` |
| 라이선스 | MIT |

## 언제 쓰나

Complete Problem-Based Software Requirements Specification methodology following Gorski & Stadzisz research. Use when you need to perform requirements engineering from business problems to functional requirements with full traceability.

## 주요 내용

- **사용 방식**: Pattern 1: Full Process (New Project) Start with Step 0 (Business Context) and progress through all steps sequentially. **Remember:** Ask where to save files, establish business context first. Pattern 2: Jump In (Existing Artifacts) Detect what artifacts exist, skip completed steps, resume at current step. **Remember:** Check for existing SRS folder and read current files. Pattern 3: Iterative Refinement Complete initial pass, then iterate on specific steps as understanding improves. **Remember:** Update existing files rather than creating new ones. Pattern 4: Validation Only Use zigzag-validator skill to check existing artifacts without generating new ones. Pattern 5: Independent Development After Step 5, engineers can pick up individual FR files and develop independently. Each FR file contains all context needed (traceability, acceptance criteria). Pattern 6: Agile/Sprint Integration...
- **진행 방식**: Step 0: Business Context (BC) **Purpose:** Establish structured business context and project principles **Input:** Stakeholder conversations, project briefs, existing documentation **Output:** Business context document with identity, principles, stakeholders, boundaries, constraints, success criteria **Save to:** `00-business-context.md` **Skill:** business-context Step 1: Customer Problems (CP) **Purpose:** Identify and document business problems **Input:** Business Context (Step 0) **Output:** List of CPs classified as Obligation/Expectation/Hope **Syntax:** `[Subject] [must/expects/hopes] [Object] [Penalty]` **Save to:** `01-customer-problems.md` **Skill:** customer-problems Step 2: Software Glance (SG) **Purpose:** Create initial abstract solution view **Input:** Customer Problems **Output:** High-level system description with boundaries and components **Save to:** `02-software-glance.md` **Skill:** software-glance Step 3: Customer Needs (CN) **Purpose:** Specify outcomes software...

## 원본 문서 구조

- Methodology Overview
- Available Skills
- 📁 Saving Progress (CRITICAL)
  - ⚠ File Creation Rule: ONE FILE AT A TIME
  - First Time Setup
  - Artifact File Structure
  - Why Individual FR/NFR Files?
  - FR File Template (FR-XXX.md)
- Requirement
- Traceability
- Acceptance Criteria
- Notes
  - NFR File Template (NFR-XXX.md)
- Requirement
- Traceability
- Acceptance Criteria
- Measurement Method
  - Save After Each Step
  - Business Context File (00-business-context.md)
- How to Use This Skill
  - Starting Fresh
  - Continuing Work
  - Validation
- Detection Heuristics
- The Steps (Quick Reference)
  - Step 0: Business Context (BC)
  - Step 1: Customer Problems (CP)
  - Step 2: Software Glance (SG)
  - Step 3: Customer Needs (CN)
  - Step 4: Software Vision (SV)
  - Step 5: Functional Requirements (FR) & Non-Functional Requirements (NFR)
- Quality Gates
  - After Step 0 (BC)
  - After Step 1 (CPs)
  - After Step 2 (SG)
  - After Step 3 (CNs)

## 관리 메모

- 이 문서는 원본 `Problem-Based-SRS/skills/problem-based-srs/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
