# zoom-meeting-sdk-web

## 요약

Zoom Meeting SDK for Web - Embed Zoom meeting capabilities into web applications. Two integration options: Client View (full-page, familiar Zoom UI) and Component View (embeddable, Promise-based API). Includes SharedArrayBuffer setup for HD video, gallery view, and virtual backgrounds.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/meeting-sdk/web/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/zoom-meeting-sdk-web-a7806d2.md` |
| 사용자 호출 | false |

## 언제 쓰나

Zoom Meeting SDK for Web - Embed Zoom meeting capabilities into web applications. Two integration options: Client View (full-page, familiar Zoom UI) and Component View (embeddable, Promise-based API). Includes SharedArrayBuffer setup for HD video, gallery view, and virtual backgrounds.

## 주요 내용

- **진행 방식**: ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐ │ Get Signature │───►│ init() │───►│ join() │ │ (from backend)│ │ (SDK setup) │ │ (enter mtg) │ └─────────────────┘ └─────────────────┘ └─────────────────┘ │ │ ▼ ▼ success/error success/error callback callback (or Promise resolve) (or Promise resolve)

## 원본 문서 구조

- How to Implement a Custom Video User Interface for a Zoom Meeting in a Web App
- Hard Routing Rule
- New to Web SDK? Start Here!
- Prerequisites
- Optional Preflight Gate (Probe SDK)
- Client View vs Component View
  - When to Use Which
- Installation
  - NPM (Recommended)
  - CDN
- Quick Start (Client View)
- Quick Start (Component View)
- Authentication Endpoint (Required)
  - Signature Generation
- Core Workflow
- Client View API Reference
  - ZoomMtg.init() - Key Options
  - ZoomMtg.join() - Key Options
  - Event Listeners (Client View)
  - Common Methods (Client View)
- Component View API Reference
  - client.init() - Key Options
  - client.join() - Key Options
  - Event Listeners (Component View)
  - Common Methods (Component View)
- SharedArrayBuffer (CRITICAL for HD)
  - Enable with HTTP Headers
  - Verify in Browser
  - Platform-Specific Setup
  - Development Setup (Two-Server Pattern)
- Common Issues & Solutions
- Browser Support Matrix
- Authorization Requirements (2026 Update)
  - Options
- Zoom for Government (ZFG)
  - Option 1: ZFG-specific NPM Package

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/meeting-sdk/web/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
