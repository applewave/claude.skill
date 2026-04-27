# sf-docs

## 요약

Official Salesforce documentation retrieval guidance. Use when you need authoritative Salesforce docs from developer.salesforce.com or help.salesforce.com, especially when pages are JS-heavy, shell-rendered, or hard to extract with naive fetching.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-docs/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-docs-466a4e2.md` |
| 라이선스 | MIT |

## 언제 쓰나

Official Salesforce documentation retrieval guidance. Use when you need authoritative Salesforce docs from developer.salesforce.com or help.salesforce.com, especially when pages are JS-heavy, shell-rendered, or hard to extract with naive fetching.

## 주요 내용

- **진행 방식**: 1. Classify the request first Before fetching anything, identify the likely doc family. 2. Identify the exact concept Extract the real target before you search: exact API/class/method name exact feature name exact product phrase exact setup concept Examples: `Lightning Message Service` `Wire Service` `System.StubProvider` `Agentforce Actions` `Messaging for In-App and Web allowed domains` 3. Prefer targeted official retrieval Do **not** broad-crawl Salesforce docs. Instead: identify the most likely official guide root or article if search is needed, restrict it to official Salesforce domains only fetch that official page check whether the **exact concept actually appears on the page** if not, inspect and follow the most relevant **1–3 official child links** stop once you have grounded evidence 4. Do not stop at broad landing pages A guide landing page is **not enough** unless it clearly contains the exact requested concept. This is especially important for: LWC docs Agentforce docs br...

## 원본 문서 구조

- Core Goal
- When to Use
- Official Sources Only
- Retrieval Workflow
  - 1. Classify the request first
  - 2. Identify the exact concept
  - 3. Prefer targeted official retrieval
  - 4. Do not stop at broad landing pages
  - 5. For `developer.salesforce.com`
  - 6. For `help.salesforce.com`
- Acceptance Rules
- Rejection Rules
- Grounding Requirements
- Examples
  - Example: Lightning Message Service
  - Example: Wire Service
  - Example: Agentforce Actions
  - Example: Messaging for In-App and Web allowed domains
  - Example: System.StubProvider
- Non-Goals
- Cross-Skill Role

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-docs/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
