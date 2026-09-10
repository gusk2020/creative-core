# STATUS

DATE: 2026-09-10

## CURRENT GOAL
Finish the 『碧き海狼』第一部第一話 v3.1 follow-up and migrate the 3-AI workflow toward GitHub-persisted handoffs so routine cross-AI transfer does not depend on manual attachments.

## CURRENT BRANCH
`work/3ai-bootstrap`

## CURRENT STATE
- GitHub access from ChatGPT is confirmed for private repository `gusk2020/creative-core`.
- The original 第一部第一話 v3 remains unchanged in `20_WIP`; it is not CANON or FINISHED.
- ChatGPT Round 1 audit, Claude Round 1 revision, ChatGPT delta verification, and Gemini evaluation are complete.
- The user adopted Gemini's PROPOSALS 1–4 in full.
- Claude returned the v3.1 change memo and Claude → ChatGPT/User HANDOFF, claiming exactly three additional line-level edits beyond Round 1.
- The substantive `aoki_kairo_part1_ep01_v3_1_candidate.md` file has still not reached ChatGPT; the most recent manual upload was the HANDOFF again. This confirms manual attachment transport is error-prone.
- In response, `AGENTS.md` and `SKILLS/handoff.md` were revised on this branch to prefer GitHub-persisted handoffs and to make formal authority path-based rather than branch-based.
- `30_AI_WORK/20_CHATGPT/shared_github_handoff_design.md` documents the proposed steady-state architecture.
- Pull Request #1 (`work/3ai-bootstrap` → `main`) is open to adopt `main` as the common synchronization surface. It is not merged yet.

## APPROVED / FIXED OPERATING RULES
- GitHub is the source of truth for structured text.
- Drive remains the large/unstructured material store.
- Chat history is not canon.
- `00_CANON` and `10_FINISHED` require explicit user approval for formal changes.
- AI output remains a proposal until the user adopts it.
- The user wants GitHub to be shared and used to reduce missed/wrong attachments during AI handoffs.

## USER-APPROVED EP01 REVISION DIRECTION
1. Use Claude Round 1's five edits as the base.
2. Shorten the three-shot explanation while preserving its causal basis.
3. Restore `追尾滑空型（ホーミンググライダー）`.
4. Resolve the second ambiguous `二十年` by removing the explicit number rather than adding a new timeline fact.

These approvals authorize a v3.1 candidate in the working area; they do not promote the episode to CANON or FINISHED.

## FILES IN USE
- `30_AI_WORK/00_SHARED/AGENTS.md`
- `30_AI_WORK/00_SHARED/STATUS.md`
- `20_WIP/aoki_kairo_part1_ep01_v3.md`
- `30_AI_WORK/20_CHATGPT/ep01_v3_audit_round1.md`
- `30_AI_WORK/20_CHATGPT/ep01_claude_round1_verification.md`
- `30_AI_WORK/20_CHATGPT/shared_github_handoff_design.md`
- `30_AI_WORK/30_CLAUDE/aoki_kairo_part1_ep01_v3_claude_round1.md`
- `30_AI_WORK/30_CLAUDE/claude_round1_change_memo.md`
- `30_AI_WORK/30_CLAUDE/claude_v3_1_change_memo.md`
- `30_AI_WORK/10_GEMINI/gemini_ep01_round1_evaluation.md`
- `30_AI_WORK/00_SHARED/HANDOFF/2026-09-10_ep01_v3_1_claude_to_chatgpt_user.md`
- `30_AI_WORK/00_SHARED/HANDOFF/2026-09-10_shared_github_workflow_to_user.md`
- `30_AI_WORK/00_SHARED/SKILLS/handoff.md`

## NEXT
1. User reviews/approves Pull Request #1 if they want `main` to become the common shared synchronization surface.
2. After merge, connected AIs should read ordinary shared WIP/AI outputs from `main`; formal status remains controlled by directory and explicit user approval.
3. For future producer stages that must eliminate manual return-file errors, use a write-capable GitHub environment (prefer Claude Code for Claude, or another trusted write-capable connector) so the producing AI commits its actual artifact before declaring completion.
4. Recover/persist the missing v3.1 candidate manuscript, then ChatGPT verifies its three claimed edits against Claude Round 1.
5. User decides whether the v3.1 candidate itself is adopted and whether it remains WIP or moves toward FINISHED.

## UNRESOLVED
- The substantive v3.1 candidate manuscript is still missing from ChatGPT/GitHub.
- Pull Request #1 is open and not yet merged.
- Claude normal chat's built-in GitHub integration is suitable for reading/syncing selected repository files but should not be treated as a guaranteed write/persistence path.
- No project CANON has been imported yet, so no full canon audit has been performed.
