# ADR-0001 — Rules and target platform

- Status: **Proposed / unresolved**
- Date: 2026-10-25

## Context
“9×9 Tic Tac Toe” has multiple incompatible game rules.

## Options
1. **Ultimate Tic-Tac-Toe**: nine 3×3 local boards; moves constrain next board; claim three local boards in a line.
2. **9×9 grid alignment**: one grid; winning run length (e.g. 5) must be specified.
3. Custom ruleset.

## Platform options
- Browser (HTML/CSS/TypeScript)
- Unity (C#)
- Other

## Decision
Pending product clarification. No implementation should hardcode a ruleset before approval.

## Consequences
Use a replaceable domain rule module; keep UI input and rendering independent.
