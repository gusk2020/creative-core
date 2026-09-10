# HANDOFF

FROM: ChatGPT
TO: User
DATE: 2026-09-10

## GOAL
Make GitHub the reliable cross-AI synchronization point so manual attachment mistakes do not remain a normal part of the workflow.

## APPROVED
- User wants GitHub to be shared and used to prevent missed/wrong attachments during AI handoffs.
- Existing authority rule remains: only the user decides formal adoption; `00_CANON/` and `10_FINISHED/` are formal paths.

## COMPLETED
- Revised `AGENTS.md` on `work/3ai-bootstrap` so `main` is proposed as the shared synchronization surface and authority is determined by directory, not merely branch location.
- Revised `SKILLS/handoff.md` so a producing AI with write access must persist the actual artifact to GitHub before declaring handoff complete.
- Documented the rationale in `30_AI_WORK/20_CHATGPT/shared_github_handoff_design.md`.

## PROPOSALS
- Merge the current bootstrap workspace to `main` so Claude/Gemini/ChatGPT can use the default branch as the shared read surface.
- Keep WIP and AI outputs under `20_WIP/` and `30_AI_WORK/`; their presence on `main` does not make them CANON/FINISHED.
- Use `work/*` only when isolation is genuinely useful.
- For Claude stages that must save files without user attachment, use Claude Code or another trusted write-capable GitHub connector. Claude normal GitHub integration remains suitable for reading/syncing but should not be relied on as the sole persistence path.

## UNRESOLVED
- The substantive v3.1 candidate manuscript still has not been received by ChatGPT; the latest upload was the HANDOFF again. This is exactly the transport problem the new workflow is intended to eliminate.
- The bootstrap-to-main merge still requires user review/approval.

## READ
1. `30_AI_WORK/20_CHATGPT/shared_github_handoff_design.md`
2. `30_AI_WORK/00_SHARED/AGENTS.md`
3. `30_AI_WORK/00_SHARED/SKILLS/handoff.md`

## NEXT
1. Review and approve the bootstrap-to-main workflow merge.
2. After merge, use `main` as the common synchronized workspace.
3. For future Claude production stages, prefer direct GitHub persistence rather than manual file return.
