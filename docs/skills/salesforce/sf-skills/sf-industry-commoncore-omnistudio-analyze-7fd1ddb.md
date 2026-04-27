# sf-industry-commoncore-omnistudio-analyze

## 요약

Cross-cutting OmniStudio analysis skill for namespace detection, dependency visualization, and impact analysis across OmniScripts, FlexCards, Integration Procedures, and Data Mappers. TRIGGER when: user asks about OmniStudio dependencies, wants namespace detection (Core vs vlocity_cmt vs vlocity_ins), needs impact analysis, or requests dependency diagrams. DO NOT TRIGGER when: authoring OmniScripts (use sf-industry-commoncore-omniscript), building FlexCards (use sf-industry-commoncore-flexcard), creating Integration Procedures (use sf-industry-commoncore-integration-procedure), or configuring Data Mappers (use sf-industry-commoncore-datamapper).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-industry-commoncore-omnistudio-analyze/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-industry-commoncore-omnistudio-analyze-7fd1ddb.md` |
| 라이선스 | MIT |

## 언제 쓰나

Cross-cutting OmniStudio analysis skill for namespace detection, dependency visualization, and impact analysis across OmniScripts, FlexCards, Integration Procedures, and Data Mappers. TRIGGER when: user asks about OmniStudio dependencies, wants namespace detection (Core vs vlocity_cmt vs vlocity_ins), needs impact analysis, or requests dependency diagrams. DO NOT TRIGGER when: authoring OmniScripts (use sf-industry-commoncore-omniscript), building FlexCards (use sf-industry-commoncore-flexcard), creating Integration Procedures (use sf-industry-commoncore-integration-procedure), or configuring Data Mappers (use sf-industry-commoncore-datamapper).

## 주요 내용

- **진행 방식**: Phase 1: Namespace Detection **Purpose**: Determine which OmniStudio namespace the org uses before querying any component metadata. **Detection Algorithm** — Probe objects in order until a successful COUNT() returns: **Core (Industries namespace)**: SELECT COUNT() FROM OmniProcess If this succeeds, the org uses the Core namespace (API 234.0+ / Spring '22+). **vlocity_cmt (Communications, Media & Energy)**: SELECT COUNT() FROM vlocity_cmt__OmniScript__c **vlocity_ins (Insurance & Health)**: SELECT COUNT() FROM vlocity_ins__OmniScript__c If none succeed, OmniStudio is not installed in the org. **CLI Commands for namespace detection**: Core namespace probe sf data query --query "SELECT COUNT() FROM OmniProcess" --target-org myorg --json 2>/dev/null vlocity_cmt namespace probe sf data query --query "SELECT COUNT() FROM vlocity_cmt__OmniScript__c" --target-org myorg --json 2>/dev/null vlocity_ins namespace probe sf data query --query "SELECT COUNT() FROM vlocity_ins__OmniScript__c" --targe...

## 원본 문서 구조

- Core Responsibilities
- Key Insights
- Workflow (4-Phase Pattern)
  - Phase 1: Namespace Detection
  - Phase 2: Component Discovery
  - Phase 3: Dependency Analysis
    - Algorithm: BFS with Circular Detection
    - Element Type → Dependency Extraction
    - FlexCard Data Source Parsing
    - Data Mapper Object Dependencies
  - Phase 4: Visualization & Reporting
    - Output Format 1: Mermaid Dependency Diagram
    - Output Format 2: JSON Summary
    - Output Format 3: Human-Readable Report
- Namespace Object/Field Mapping
  - Primary Objects
  - Key Fields
- CLI Commands Reference
  - Namespace Detection
  - Component Inventory (Core Namespace)
  - Dependency Data Extraction (Core Namespace)
- Cross-Skill Integration
- Edge Cases
- Notes
- License

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-industry-commoncore-omnistudio-analyze/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
