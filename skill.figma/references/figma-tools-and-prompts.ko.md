# Figma MCP 도구 및 프롬프트 패턴

Figma MCP 도구 세트에 대한 빠른 참조, 각 도구의 사용 시점, 그리고 출력을 사용자의 기술 스택에 맞게 조정하기 위한 프롬프트 예시입니다.

## 핵심 도구
- `get_design_context` (Figma Design, Figma Make): 기본 도구. 구조화된 디자인 데이터와 기본 React + Tailwind 코드를 반환합니다. 선택 기반 프롬프팅은 데스크톱에서 작동하며, 원격 서버는 프레임/레이어 링크를 사용하여 노드 ID를 추출합니다.
- `get_variable_defs` (Figma Design): 선택 항목에 사용된 변수/스타일(색상, 스페이싱, 타이포그래피)을 나열합니다. 토큰 정렬에 유용합니다.
- `get_metadata` (Figma Design): 레이어 ID/이름/유형/위치/크기의 간략한 XML 개요. 큰 노드에서 잘림을 방지하기 위해 `get_design_context`를 다시 호출하기 전에 사용합니다.
- `get_screenshot` (Figma Design, FigJam): 시각적 충실도 확인을 위한 선택 항목의 스크린샷.
- `get_figjam` (FigJam): FigJam 다이어그램(아키텍처, 플로우)용 XML + 스크린샷.
- `create_design_system_rules` (파일 컨텍스트 불필요): 사용자의 기술 스택에 맞는 디자인-투-코드 가이던스 규칙 파일을 생성합니다. 에이전트가 읽을 수 있는 위치에 저장하세요.
- `get_code_connect_map` (Figma Design): Figma 노드 ID와 코드 컴포넌트(`codeConnectSrc`, `codeConnectName`) 간의 매핑을 반환합니다. 기존 컴포넌트 재사용에 활용합니다.
- `add_code_connect_map` (Figma Design): Figma 노드와 코드 컴포넌트 간의 매핑을 추가/업데이트하여 재사용성을 향상시킵니다.
- `get_strategy_for_mapping` (알파, 로컬 전용): 노드를 코드 컴포넌트에 연결하기 위한 매핑 전략을 결정하는 Figma 프롬프트 도구.
- `send_get_strategy_response` (알파, 로컬 전용): `get_strategy_for_mapping` 이후 응답을 전송합니다.
- `whoami` (원격 전용): 인증된 Figma 사용자 ID(이메일, 플랜, 시트 유형)를 반환합니다.

## 프롬프트 패턴 (디자인 컨텍스트)
- 프레임워크 변경: "내 Figma 선택 항목을 Vue로 생성해줘" 또는 "순수 HTML + CSS로" 또는 "iOS용으로".
- 내 컴포넌트 사용: "`src/components/ui`의 컴포넌트를 사용하여 내 Figma 선택 항목을 생성해줘".
- 조합: "`src/ui`의 컴포넌트를 사용하고 Tailwind로 스타일링하여 내 Figma 선택 항목을 생성해줘".
- 참고: 원격 서버에서 선택 기반 프롬프팅은 프레임/레이어 링크가 필요합니다. 서버가 URL에서 노드 ID를 추출합니다.

## 프롬프트 패턴 (변수/스타일)
- "내 Figma 선택 항목에 사용된 변수를 가져와줘"
- "내 Figma 선택 항목에 사용된 색상 및 스페이싱 변수는 뭐야?"
- "내 Figma 선택 항목에 사용된 변수 이름과 값을 나열해줘"

## 프롬프트 패턴 (코드 연결)
- "이 선택 항목의 코드 연결 맵을 보여줘"
- "이 노드를 `src/components/ui/Button.tsx`에 `Button`이라는 이름으로 매핑해줘"

## 베스트 프랙티스 플로우 안내
`get_design_context` → (큰 노드의 경우 선택적으로 `get_metadata`) → `get_screenshot` 순서를 사용하고, 생성된 출력을 적용할 때 `SKILL.md`의 프로젝트 규칙을 항상 염두에 두세요.
