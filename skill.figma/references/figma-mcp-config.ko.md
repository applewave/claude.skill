# Figma MCP 설정 참조

이 스니펫을 사용하여 `~/.codex/config.toml`에 Figma MCP 서버를 스트리밍 가능한 HTTP 서버로 등록합니다. 인증은 환경 변수에서 가져온 Bearer 토큰을 사용합니다.

```toml
[mcp_servers.figma]
url = "https://mcp.figma.com/mcp"
bearer_token_env_var = "FIGMA_OAUTH_TOKEN"
http_headers = { "X-Figma-Region" = "us-east-1" }
```

## 참고 사항 및 옵션
- Bearer 토큰은 Codex를 실행하는 환경에서 `FIGMA_OAUTH_TOKEN`으로 사용 가능해야 합니다.
- 리전 헤더를 Figma 리전에 맞게 유지하세요. 조직에서 다른 리전을 사용하는 경우 `X-Figma-Region`을 일관되게 업데이트하세요.
- 스트리밍 가능한 HTTP에서의 OAuth는 RMCP 클라이언트가 필요합니다: `config.toml` 최상위 레벨에서 `[features].rmcp_client = true` (또는 이전 빌드의 경우 `experimental_use_rmcp_client = true`)를 설정하세요.
- 선택적 서버별 타임아웃: 필요한 경우 `[mcp_servers.figma]` 내에 `startup_timeout_sec` (기본값 10)과 `tool_timeout_sec` (기본값 60)을 설정할 수 있습니다.

## 환경 변수 설정 (누락된 경우)
- 현재 셸에 일회성 설정: `export FIGMA_OAUTH_TOKEN="<토큰>"`
- 향후 세션을 위해 영구 설정: 셸 프로필(예: `~/.zshrc` 또는 `~/.bashrc`)에 export 라인을 추가한 후 셸 또는 IDE를 재시작하세요.
- Codex 실행 전 확인: `echo $FIGMA_OAUTH_TOKEN`이 비어있지 않은 토큰을 출력해야 합니다.

## 설정 및 검증 체크리스트
- 위 스니펫을 `~/.codex/config.toml`의 `[mcp_servers.figma]` 아래에 추가하고, `[features].rmcp_client = true` (또는 이전 릴리스의 경우 `experimental_use_rmcp_client = true`)를 활성화하세요.
- 설정 및 환경 변수 업데이트 후 Codex(CLI/IDE)를 재시작하세요.
- Codex에 Figma 도구 목록을 요청하거나 간단한 호출을 실행하여 서버에 연결 가능한지 확인하세요.

## 문제 해결
- 토큰이 인식되지 않는 경우: Codex를 실행하는 동일한 셸에서 `FIGMA_OAUTH_TOKEN`을 export하거나, 셸 프로필에 추가한 후 재시작하세요.
- OAuth 오류: `rmcp_client`가 활성화되어 있고 Bearer 토큰이 유효한지 확인하세요. Figma에서 복사한 토큰에 따옴표가 포함되어서는 안 됩니다.
- 네트워크/헤더: `X-Figma-Region` 헤더를 유지하세요. 조직에서 다른 리전을 사용하는 경우 설정과 요청 전반에 걸쳐 헤더를 일관되게 업데이트하세요.

## 사용 안내
- 서버는 링크 기반입니다: Figma 프레임 또는 레이어 링크를 복사한 후 MCP 클라이언트에 해당 URL의 구현을 요청하세요. 클라이언트는 링크에서 노드 ID를 추출합니다 (페이지를 탐색하지 않습니다).
- 출력이 일반적으로 느껴지면, 메인 스킬의 프로젝트별 규칙을 다시 명시하고 필수 플로우(get_design_context → 필요 시 get_metadata → get_screenshot)를 따르고 있는지 확인하세요.
