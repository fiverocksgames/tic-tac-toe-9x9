# Tic Tac Toe 9×9

9×9 틱택토 게임 프로젝트.

## Status
**Bootstrap** — 저장소 구조와 설계 원칙 수립. 게임 룰/플랫폼/기술 스택은 미확정.

## Working agreements
- 게임 규칙(Game Domain)과 화면/입력(UI)을 분리한다.
- 게임 상태는 단일 데이터 모델로 관리하고, 매 수를 순수한 상태 전이로 처리한다.
- 합법 수, 승리, 무승부, 턴 전환은 자동화 테스트 대상으로 삼는다.
- 미확정 요구사항은 추측하여 구현하지 않고 ADR에 기록한다.

## Layout
- `docs/`: 요구사항·아키텍처·결정 기록
- `src/domain/`: 게임 엔진(기술 스택 결정 후 추가)
- `src/ui/`: 프레젠테이션(기술 스택 결정 후 추가)
- `tests/`: 규칙·상태 전이 테스트(기술 스택 결정 후 추가)

## Key pending decision
9×9 규칙: **Ultimate Tic-Tac-Toe(3×3 보드 9개)** 또는 **일반 9×9 격자 연속 N목** 등 중 선택 필요.

See [architecture](docs/architecture.md) and [ADR-0001](docs/adr/0001-game-rules-and-platform.md).
