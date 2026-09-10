# Skill: handoff

STATUS: working operational rule / proposal until user adopts branch changes

## Purpose
Transfer a bounded task between Gemini, ChatGPT, Claude, or a new session without treating chat history or AI memory as canon, while minimizing manual file attachment and copy/paste mistakes.

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

## Preferred cross-AI transfer procedure: GitHub-persisted handoff
1. Produce the substantive artifact in the producing AI's `30_AI_WORK/<AI>/` area, or another explicitly authorized working path.
2. Save the actual artifact to GitHub **before** claiming completion.
3. Save a short change/evaluation memo if needed.
4. Independently compare or verify edited artifacts against their source when practical.
5. Save the HANDOFF last. In `COMPLETED`, name exact GitHub paths and include commit SHA(s) when useful.
6. Confirm that the committed files can be fetched/read from GitHub.
7. The receiving AI reads from GitHub and executes `NEXT`; the user should not need to re-upload the same files.

A handoff is not fully persisted merely because a file was generated inside an AI chat. If the producing environment cannot write to GitHub, say so explicitly.

## Read-only fallback
If the producing or receiving AI cannot reliably read/write the shared GitHub state:
1. Use a designated write-capable AI/tool to persist the outputs in GitHub when possible.
2. If direct persistence is impossible, create one temporary Markdown transfer packet containing only:
   - AGENTS
   - current STATUS
   - latest relevant HANDOFF
   - files named in READ
   - any supplementary verification note explicitly needed for NEXT
3. Mark the packet as a temporary transport copy, not source of truth.
4. After the next AI returns results, store the actual outputs and HANDOFF back in GitHub at the earliest write-capable step.

## Branch rule
- Prefer `main` as the shared synchronization surface for ordinary WIP and AI outputs so all connected AIs can see the same current state.
- Directory authority, not branch location, determines whether material is formal.
- `20_WIP/`, `30_AI_WORK/`, and `90_OTHER/` remain non-formal even on `main`.
- Use `work/*` when isolation is useful for risky/large changes or formal CANON/FINISHED candidates, not as a mandatory transport layer.

## Token discipline
- Prefer direct GitHub reads over manual multi-file attachments.
- When direct reads fail, prefer one transfer packet over many attachments.
- Do not include SESSION_ARCHIVE unless required to resolve a specific provenance question.
- Do not make the next AI reread irrelevant CANON/WIP files.
- Use lightweight models for short organization/review when they can finish reliably; use a stronger long-context model for long-form rewriting when lightweight execution stalls. This is a heuristic, not a fixed model rule.

## Safety / authority
- Never provide GitHub Personal Access Tokens in chat as a workaround.
- Do not promote WIP/AI output to CANON or FINISHED without explicit user approval.
- Never infer approval from another AI's wording such as “recommended”, “completed”, or “final”.
- If a model surfaces remembered rules not present in the current READ set, ignore them or list them as an external-context issue rather than applying them.
- If the environment has write access, do not overwrite existing files blindly; fetch/compare first and write to the intended working path.
