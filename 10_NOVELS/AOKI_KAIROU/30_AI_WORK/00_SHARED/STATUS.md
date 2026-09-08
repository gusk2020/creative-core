# STATUS

DATE: 2026-09-09

## CURRENT GOAL
Run one small Gemini / ChatGPT / Claude baton-pass experiment on 『碧き海狼』 using 第一部第一話 v3, while keeping all AI outputs as proposals until the user approves them.

## CURRENT BRANCH
`work/3ai-bootstrap`

## CURRENT STATE
- GitHub access from ChatGPT confirmed for private repository `gusk2020/creative-core`.
- `main` was inspected before writing and its existing root `README.md` was not overwritten.
- Minimal shared folder skeleton exists under `10_NOVELS/AOKI_KAIROU/`.
- `AGENTS.md`, `STATUS.md`, shared `HANDOFF/`, `SKILLS/`, and `SESSION_ARCHIVE/` exist.
- User designated 『碧き海狼』第一部第一話 v3 as the first baton-test source.
- The source was copied unchanged into `20_WIP/aoki_kairo_part1_ep01_v3.md`; it is not CANON or FINISHED.
- ChatGPT completed Round 1 audit without editing the WIP source.
- A ChatGPT → Claude handoff has been created.

## APPROVED / FIXED OPERATING RULES
- GitHub is the source of truth for structured text.
- Drive remains the large/unstructured material store.
- Chat history is not canon.
- `00_CANON` and `10_FINISHED` require explicit user approval for formal changes.
- AI output remains a proposal until the user adopts it.
- New sessions read `AGENTS.md` → `STATUS.md` → latest HANDOFF → only needed project files.

## FILES IN USE
- `30_AI_WORK/00_SHARED/AGENTS.md`
- `30_AI_WORK/00_SHARED/STATUS.md`
- `20_WIP/aoki_kairo_part1_ep01_v3.md`
- `30_AI_WORK/20_CHATGPT/ep01_v3_audit_round1.md`
- `30_AI_WORK/00_SHARED/HANDOFF/2026-09-09_ep01_round1_chatgpt_to_claude.md`

## NEXT
1. Claude reads the latest HANDOFF and produces a minimal-change revision in `30_AI_WORK/30_CLAUDE/`.
2. Claude leaves a short change memo and a Claude → Gemini HANDOFF.
3. Gemini reviews structure/setting presentation and summarizes the delta rather than silently rewriting it again.
4. User decides what, if anything, to adopt.
5. After the experiment, identify repeated instructions and create only those Skills that proved necessary.

## UNRESOLVED
- No project CANON has been imported yet, so this first experiment is limited to the supplied episode's internal consistency and prose/structure.
- Do not fill missing canon from old chat history or AI memory during this experiment.
