# MakeTeam Task Workflow Policy

## Goal

Keep planning lightweight in Backlog, and require explicit user confirmation before committing execution detail.

## Status Definitions

- **Backlog**
  - Idea capture only.
  - Title should be short and outcome-oriented (one line).
  - No detailed scope/estimate required.

- **Todo**
  - Approved, ready-to-plan work.
  - Must include a concrete execution plan:
    - objective
    - scope (in/out)
    - implementation steps
    - definition of done
    - risks/rollback (if applicable)
  - **Requires user confirmation** before moving from Backlog → Todo.

- **Doing**
  - Active implementation.
  - Must have owner + explicit DoD.

- **Done**
  - Implementation complete + validation evidence captured.

## Transition Rules

1. **Backlog → Todo**
   - Draft detailed plan in Chat.
   - Ask user for explicit approval.
   - Move only after approval.

2. **Todo → Doing**
   - Confirm DoD exists.
   - Confirm dependencies are clear.

3. **Doing → Done**
   - Verify result and provide proof (screenshot/log/commit).

## Chat ↔ Task Relationship

- **Task** = source of truth for priority and state.
- **Chat** = planning and execution log.
- Every state change should be explainable in Chat.

## Conversation-driven Operation (default)

- In Chat, the assistant should naturally discuss "what to do next" with the user.
- In background, board state is continuously maintained to match the conversation.
- Transition protocol:
  1. Propose plan in chat
  2. Get explicit user approval
  3. Move Backlog -> Todo
  4. Move Todo -> Doing on actual start
  5. Move Doing/Review -> Done with evidence

This keeps chat natural for the user while preserving strict execution state on the board.
