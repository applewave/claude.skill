# zoom-meeting-sdk-windows

## 요약

Zoom Meeting SDK for Windows - Native C++ SDK for embedding Zoom meetings into Windows desktop applications. Supports custom UI architecture with raw video/audio data, headless bots, and deep integration with meeting features. Includes SDK architecture patterns and Windows message loop handling.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/meeting-sdk/windows/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/zoom-meeting-sdk-windows-0405cc4.md` |
| 사용자 호출 | false |

## 언제 쓰나

Zoom Meeting SDK for Windows - Native C++ SDK for embedding Zoom meetings into Windows desktop applications. Supports custom UI architecture with raw video/audio data, headless bots, and deep integration with meeting features. Includes SDK architecture patterns and Windows message loop handling.

## 주요 내용

- **진행 방식**: ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ │ InitSDK │───►│ AuthSDK │───►│ JoinMeeting │───►│ Raw Data │ │ │ │ (JWT) │ │ │ │ Subscribe │ └─────────────┘ └─────────────┘ └─────────────┘ └─────────────┘ │ │ ▼ ▼ OnAuthComplete onInMeeting callback callback **⚠️ CRITICAL**: Add Windows message loop or callbacks won't fire! while (!done) { MSG msg; while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) { TranslateMessage(&msg); DispatchMessage(&msg); } std::this_thread::sleep_for(std::chrono::milliseconds(100)); } See: [Windows Message Loop Guide](troubleshooting/windows-message-loop.md)

## 원본 문서 구조

- New to Zoom SDK? Start Here!
- Prerequisites
- Project Preferences & Learnings
  - Do NOT use CMake — Use native Visual Studio `.vcxproj`
  - `config.json` must be visible in Solution Explorer
- Overview
  - Key Architectural Insight
- Quick Start
  - 1. Download Windows SDK
  - 2. Setup Project Structure
  - 3. Install Dependencies (vcpkg)
  - 4. Configure Visual Studio Project
  - 5. Configure Credentials
  - 6. Build & Run
- Core Workflow
- Code Examples
  - Important: Include Order
  - 1. Initialize SDK
  - 2. Authenticate with JWT
  - 3. Join Meeting
  - 4. Subscribe to Raw Video
  - 5. Subscribe to Raw Audio
  - 6. Main Message Loop (CRITICAL!)
- Common Issues & Solutions
- How to Implement Any Feature
- Available Examples
- Detailed References
  - 🎯 Core Concepts (START HERE!)
  - 📚 Complete Examples
  - 🔧 Troubleshooting Guides
  - 📖 References
  - 🎨 Feature-Specific Guides
- Sample Repositories
- Playing Raw Video/Audio Files
  - Play Raw YUV Video
  - Convert YUV to MP4

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/meeting-sdk/windows/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
