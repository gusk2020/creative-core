# HANDOFF

FROM: ChatGPT
TO: Gemini / Claude / next ChatGPT session
DATE: 2026-09-09

## GOAL
Bootstrap the shared 3AI working environment in `gusk2020/creative-core` and prepare for one small baton-pass experiment using 『碧き海狼』.

## APPROVED
- GitHub `gusk2020/creative-core` is the structured-text source of truth.
- Google Drive remains the large/unstructured material store.
- AI chat history is not canon.
- `00_CANON` and `10_FINISHED` require explicit user approval for formal changes.
- AI output remains a proposal until the user adopts it.
- New sessions should read `AGENTS.md` → `STATUS.md` → latest HANDOFF → only needed project files.

## COMPLETED
- Confirmed ChatGPT can read the private repository.
- Inspected `main` before writing; it contained only the existing root `README.md`.
- Created work branch `work/3ai-bootstrap` from `main`.
- Added the initial shared `AGENTS.md`.
- Added the initial shared `STATUS.md`.
- Began the minimal 『碧き海狼』 folder skeleton without modifying `main` or existing files.

## PROPOSALS
- Use the first experiment to test the handoff mechanism itself rather than attempting a large creative task.
- Keep the experiment deliberately small: one bounded WIP source, one clearly defined task per AI, and one final user decision.

## UNRESOLVED
- No 『碧き海狼』 CANON/WIP source file existed in `creative-core/main` at bootstrap time.
- Therefore no actual content baton-pass should begin until the user places or designates a small source item in WIP (or explicitly asks an AI to create a WIP test input).
- Do not reconstruct CANON from chat memory solely to populate the repository.

## READ
1. `10_NOVELS/AOKI_KAIROU/30_AI_WORK/00_SHARED/AGENTS.md`
2. `10_NOVELS/AOKI_KAIROU/30_AI_WORK/00_SHARED/STATUS.md`
3. This file
4. The user-designated WIP source for the first baton experiment, once present

## NEXT
1. Complete the remaining minimal folder placeholders if needed.
2. User designates or supplies one small 『碧き海狼』 WIP source item.
3. Run one small baton-pass experiment, e.g. Gemini prepares/organizes → ChatGPT audits → Claude rewrites, with the user deciding what is adopted.
4. Record only the instructions that actually repeated.
5. Create a Skill only if repetition was demonstrated by the experiment.