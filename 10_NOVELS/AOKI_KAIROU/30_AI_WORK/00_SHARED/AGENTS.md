# AGENTS.md

## Purpose
This file is the shared operating constitution for Gemini, ChatGPT, Claude, and other AI tools working in `gusk2020/creative-core`.

## Source of truth
- GitHub `gusk2020/creative-core` is the source of truth for structured text assets.
- Google Drive is for PDFs, images, video, MHT, Google Docs/Sheets, large files, un整理済み資料, and other material better kept outside Git.
- Do not keep two independently editable canonical copies of the same asset in GitHub and Drive.
- AI chat history, memory, imports, and model-internal copies are not canon. Treat them as cache, working context, or archive only.
- Do not infer undocumented personal information, accounts, identities, or persona settings.

## Authority levels
### Formal
- `00_CANON/`
- `10_FINISHED/`

AI must not modify, promote, or declare content in these locations final without explicit user approval.

### Working
- `20_WIP/`
- `30_AI_WORK/`
- `90_OTHER/`

AI may propose, compare, audit, rewrite, and experiment here when the task authorizes it. AI output remains a proposal until the user explicitly adopts it.

**Authority is determined by path and user approval, not merely by the Git branch that contains the file.**
A file in `20_WIP/` or `30_AI_WORK/` remains working/proposal material even when it is present on `main`.

## Other AI output
- Do not treat another AI's statement as canon merely because it exists in a file or chat.
- Separate user-approved facts from proposals and unresolved ideas.
- Preserve disagreements when useful; do not silently collapse alternatives into one answer.

## Read order for a new session
1. `AGENTS.md`
2. `STATUS.md`
3. newest relevant file in `HANDOFF/`
4. only the CANON / FINISHED / WIP / AI_WORK files needed for the current task

Do not load raw session archives unless they are actually needed.

## Branch and approval workflow
- `main` = shared synchronization surface for all AIs. It may contain both formal and working material; directory authority rules still apply.
- `work/*` = optional isolation branches for risky, large, experimental, or review-heavy changes. Do not require a working branch merely to share ordinary WIP or AI outputs.
- AI-specific branches are not required.
- Ordinary AI outputs should normally be written to the producing AI's area under `30_AI_WORK/<AI>/` and may be shared through `main` when write access is available.
- Changes to `00_CANON/` or `10_FINISHED/` should normally follow:
  1. prepare the candidate outside the formal path, or on `work/*`
  2. independent diff/review by another AI when useful
  3. user review
  4. modify/promote formal paths only after explicit user approval
- Do not self-approve formal-setting changes.
- A merge to `main` does **not** by itself promote files in `20_WIP/`, `30_AI_WORK/`, or `90_OTHER/` to formal status.

## Shared GitHub handoff rule
The goal is to avoid manual attachment mistakes between AIs.

- When the producing AI/session has GitHub write access, it must save its actual output to GitHub before declaring the handoff complete.
- Save the substantive artifact first, then any change memo, then the HANDOFF.
- HANDOFF `COMPLETED` should name the exact committed paths. Include a commit SHA when available and useful.
- The receiving AI should fetch/read the committed files from GitHub rather than asking the user to re-upload copies.
- If the producing environment is read-only, state that limitation explicitly. The handoff is not considered fully persisted until a designated write-capable step stores the outputs in GitHub.
- Manual transfer packets remain a fallback for read-only or branch-visibility failures, not the preferred steady-state workflow.
- Never ask the user to paste a GitHub Personal Access Token into chat as a workaround.

## STATUS.md
`STATUS.md` is a whiteboard, not a history log. Keep only:
- current goal
- current branch / working area
- recently approved items
- files currently in use
- next handoff / next action
- unresolved items

Move old discussion to HANDOFF or SESSION_ARCHIVE when it matters; otherwise delete it from STATUS.

## HANDOFF format
Use the following minimal packet when transferring work between sessions or AIs:

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

`APPROVED` contains only user-approved material. `PROPOSALS` remains non-canon.

## SESSION_ARCHIVE
Raw exported chats or long logs are evidence/reference, not canon. Save them only when there is a real need to preserve provenance or recover detail.

## Skills
Create a Skill only after the same operational instruction has been needed repeatedly. Do not pre-build a large Skill library.

Initial candidates, only when repetition justifies them:
- `canon-audit`
- `plot-development`
- `prose-review`
- `handoff`

## AI roles
Current tendencies are useful defaults, not hierarchy:
- Gemini: setting organization/expansion, plot and initial drafts, Notebook-based cross-document reference
- ChatGPT: setting audit, logic/science/history consistency, critique, review, app-development support
- Claude: prose drafting, Japanese-language finishing, revision, long-form writing, GitHub work via Claude Code or another write-capable connector when direct persistence is required

Choose the AI by task. Roles may change.

## General rule
The user alone decides what becomes formally adopted. When unsure whether something is approved, treat it as a proposal.
