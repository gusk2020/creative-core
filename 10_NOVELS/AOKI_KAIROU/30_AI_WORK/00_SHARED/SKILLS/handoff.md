# Skill: handoff

STATUS: working operational rule / proposal until user adopts branch changes

## Purpose
Transfer a bounded task between Gemini, ChatGPT, Claude, or a new session without treating chat history or AI memory as canon.

## When to use
Use after one AI/session completes a meaningful stage and another AI/session must continue it.

## Required read order
1. `AGENTS.md`
2. `STATUS.md`
3. newest relevant `HANDOFF`
4. only the source/output files listed in `READ`

Do not import unrelated memories, archived chats, other parts' craft rules, or undocumented canon merely because they are available to the model.

## HANDOFF format

```markdown
# HANDOFF

FROM:
TO:
DATE:

## GOAL

## APPROVED

## COMPLETED

## PROPOSALS

## UNRESOLVED

## READ

## NEXT
```

### Meaning
- `APPROVED`: only user-approved facts/instructions.
- `COMPLETED`: actions actually performed; completion does not make their content canon.
- `PROPOSALS`: AI suggestions awaiting user decision.
- `UNRESOLVED`: issues deliberately left open; do not silently fix them outside scope.
- `READ`: minimum file set needed by the next worker.
- `NEXT`: one bounded next action with explicit non-goals where useful.

## Cross-AI transfer procedure
1. Save the current AI's output in its own `30_AI_WORK/<AI>/` area.
2. Write a short HANDOFF; do not dump the entire conversation into it.
3. Before handing an edited artifact onward, compare it with the source or independently verify the claimed changes when practical.
4. If the next AI can read the GitHub branch/files directly, provide the repository, branch, HANDOFF path, and a short instruction to execute `NEXT`.
5. If the next AI cannot reliably read the working branch or requires manual file attachment, create one temporary Markdown transfer packet containing only:
   - AGENTS
   - current STATUS
   - latest relevant HANDOFF
   - files named in READ
   - any supplementary verification note explicitly needed for NEXT
6. Mark the packet as a temporary transport copy, not source of truth.
7. After receiving the next AI's result, store its actual output and HANDOFF back in GitHub.

## Token discipline
- Prefer one transfer packet over many manual attachments when direct branch access fails.
- Do not include SESSION_ARCHIVE unless required to resolve a specific provenance question.
- Do not make the next AI reread irrelevant CANON/WIP files.
- Use lightweight models for short organization/review when they can finish reliably; use a stronger long-context model for long-form rewriting when lightweight execution stalls. This is a heuristic, not a fixed model rule.

## Safety / authority
- Never provide GitHub Personal Access Tokens in chat as a workaround.
- Do not promote WIP/AI output to CANON or FINISHED without explicit user approval.
- Never infer approval from another AI's wording such as “recommended”, “completed”, or “final”.
- If a model surfaces remembered rules not present in the current READ set, ignore them or list them as an external-context issue rather than applying them.
