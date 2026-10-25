# Architecture v0

## Goals
- deterministic, testable game rules
- no UI dependency in domain
- local two-player play as the first milestone **candidate**, not a confirmed requirement
- future AI/multiplayer adapters without changing rule engine

## Proposed layers

```
UI / Input
   |
Application (GameController)
   |
Domain (GameState, Rules, Move, Result)
   |
Infrastructure (persistence/network, optional)
```

## Domain API proposal
- `createGame(config) -> GameState`
- `getLegalMoves(state) -> Move[]`
- `applyMove(state, move) -> GameState | RuleError`
- `evaluateOutcome(state) -> Outcome`

The exact state shape and win logic depend on ADR-0001.

## Test contract
1. initial state invariants
2. turn alternation
3. illegal move rejection / immutable state after rejection
4. wins along all allowed axes
5. draws and terminal-state lock
6. any rule-specific forced-board behavior

## Delivery gates
- Gate 0: rules + target platform approved
- Gate 1: headless domain tests green
- Gate 2: playable local UI
- Gate 3: UX polish, release workflow

No engine/runtime selected yet.
