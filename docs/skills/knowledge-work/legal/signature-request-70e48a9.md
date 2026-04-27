# signature-request

## 요약

Prepare and route a document for e-signature — run a pre-signature checklist, configure signing order, and send for execution. Use when a contract is finalized and ready to sign, when verifying entity names, exhibits, and signature blocks before sending, or when setting up an envelope with sequential or parallel signers.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | legal |
| 원본 경로 | `knowledge-work-plugins/legal/skills/signature-request/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/legal/signature-request-70e48a9.md` |
| 입력 힌트 | `<document or contract to send>` |

## 언제 쓰나

Prepare and route a document for e-signature — run a pre-signature checklist, configure signing order, and send for execution. Use when a contract is finalized and ready to sign, when verifying entity names, exhibits, and signature blocks before sending, or when setting up an envelope with sequential or parallel signers.

## 주요 내용

- **사용 방식**: /signature-request $ARGUMENTS Prepare for signature: @$1
- **진행 방식**: Step 1: Accept the Document Accept the document in any format: **File upload**: PDF, DOCX **URL**: Link to a document in ~~cloud storage or ~~CLM **Reference**: "The Acme Corp MSA we finalized yesterday" Step 2: Pre-Signature Checklist Before routing for signature, verify:

## 원본 문서 구조

- Usage
- Workflow
  - Step 1: Accept the Document
  - Step 2: Pre-Signature Checklist
- Pre-Signature Checklist
  - Step 3: Configure Signing
  - Step 4: Route for Signature
- Output
- Signature Request: [Document Title]
  - Document Details
  - Pre-Signature Check: [PASS / ISSUES FOUND]
  - Signing Configuration
  - CC Recipients
  - Status
  - Next Steps
- Tips

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/legal/skills/signature-request/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
