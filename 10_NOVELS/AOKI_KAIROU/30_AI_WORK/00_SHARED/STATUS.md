# STATUS

DATE: 2026-09-10

## CURRENT GOAL
Produce a tightly scoped v3.1 candidate for 『碧き海狼』第一部第一話 based on the user-approved Gemini proposals, while keeping CANON / FINISHED unchanged until later approval.

## CURRENT BRANCH
`work/3ai-bootstrap`

## CURRENT STATE
- GitHub access from ChatGPT confirmed for private repository `gusk2020/creative-core`.
- Minimal shared folder skeleton exists under `10_NOVELS/AOKI_KAIROU/`.
- The original 第一部第一話 v3 remains unchanged in `20_WIP`; it is not CANON or FINISHED.
- ChatGPT completed Round 1 audit without editing the WIP source.
- Claude Sonnet completed a minimal-change Round 1 revision, plus change memo and Claude → Gemini HANDOFF.
- ChatGPT independently checked the Claude delta and found the dropped `追尾滑空型（ホーミンググライダー）` label.
- Gemini completed the requested non-rewrite evaluation.
- The user adopted Gemini's PROPOSALS 1–4 in full.
- A new User / ChatGPT → Claude HANDOFF has been created for the v3.1 micro-fix pass.
- The first 3AI baton test itself is operationally complete; this is now the approved follow-up revision pass.

## APPROVED / FIXED OPERATING RULES
- GitHub is the source of truth for structured text.
- Drive remains the large/unstructured material store.
- Chat history is not canon.
- `00_CANON` and `10_FINISHED` require explicit user approval for formal changes.
- AI output remains a proposal until the user adopts it.
- New sessions read `AGENTS.md` → `STATUS.md` → latest HANDOFF → only needed project files.

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
- `30_AI_WORK/30_CLAUDE/aoki_kairo_part1_ep01_v3_claude_round1.md`
- `30_AI_WORK/30_CLAUDE/claude_round1_change_memo.md`
- `30_AI_WORK/10_GEMINI/gemini_ep01_round1_evaluation.md`
- `30_AI_WORK/00_SHARED/HANDOFF/2026-09-10_ep01_v3_1_user_approved_to_claude.md`
- `30_AI_WORK/00_SHARED/SKILLS/handoff.md`

## NEXT
1. Claude reads the v3.1 HANDOFF and produces a complete v3.1 candidate with only the three approved micro-fixes beyond Round 1.
2. Claude outputs the complete candidate text, a short change memo, and a HANDOFF back to ChatGPT / user.
3. ChatGPT verifies the delta against Claude Round 1 and records the result.
4. User decides whether the v3.1 candidate itself is adopted and whether it should remain WIP or move toward FINISHED.
5. Separately, user decides whether the bootstrap branch structure and `handoff` Skill should be adopted/merged as the ongoing 3AI workflow.

## UNRESOLVED
- The v3.1 candidate has not yet been produced or approved.
- No project CANON has been imported yet, so no full canon audit has been performed.
- The observed Claude normal-chat difficulty reading the working branch may be UI/tool-specific; the transfer-packet fallback worked and remains a practical heuristic.
- `SKILLS/handoff.md` is still a working draft on the bootstrap branch and is not yet a formally adopted workflow.
