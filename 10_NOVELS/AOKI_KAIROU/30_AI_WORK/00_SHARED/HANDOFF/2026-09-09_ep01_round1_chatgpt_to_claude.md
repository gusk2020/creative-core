# HANDOFF

FROM: ChatGPT
TO: Claude
DATE: 2026-09-09

## GOAL
『碧き海狼』第一部第一話 v3 を使って、小規模な3AIバトンタッチ運用を1回検証する。

今回は既存原稿があるため、ChatGPTが先に監査し、Claudeがその監査を材料に必要最小限の文章修整を行う。次段でGeminiに、原稿の構成・設定提示・変更点の整理を依頼する想定。

## APPROVED
- この第一話 v3 を今回のバトンタッチ実験素材として使うこと。
- GitHub上では正式稿ではなく `20_WIP` として扱う。
- CANON / FINISHED はユーザー承認なしに変更しない。

## COMPLETED
- 元原稿を `20_WIP/aoki_kairo_part1_ep01_v3.md` に保存。
- ChatGPT監査を `30_AI_WORK/20_CHATGPT/ep01_v3_audit_round1.md` に保存。
- ChatGPTは原稿自体を改稿していない。

## PROPOSALS
ChatGPT監査では以下を優先修正候補とした。
1. `螃蟹` の定義と「一匹残らず潰す」命令が、子供救出と衝突して見える点の明確化。
2. 追撃船で読んだ三連射パターンをアマルティアにも適用する根拠の明確化。
3. 「二十年かけて学んでいる」が異世界船上生活20年にも読める曖昧さの解消。
4. 第3〜5節の新兵器・新概念の説明密度を、種類は減らさず整理。
5. 三つのクライマックスを削らず、第5→6節で戦闘から終幕へ呼吸を切り替える。

## UNRESOLVED
- 上記提案はユーザー未承認。Claudeは「採用決定」として扱わず、試作改稿として実施する。
- 原稿全体の設定正史との照合は今回まだ行っていない。GitHubのCANONが未投入のため、外部の過去会話記憶で補完しない。

## READ
1. `10_NOVELS/AOKI_KAIROU/30_AI_WORK/00_SHARED/AGENTS.md`
2. `10_NOVELS/AOKI_KAIROU/30_AI_WORK/00_SHARED/STATUS.md`
3. `10_NOVELS/AOKI_KAIROU/20_WIP/aoki_kairo_part1_ep01_v3.md`
4. `10_NOVELS/AOKI_KAIROU/30_AI_WORK/20_CHATGPT/ep01_v3_audit_round1.md`

## NEXT
Claudeは原稿の全面書き換えを避け、上記1〜5だけを対象に「必要最小限の改稿版」を作る。

出力先候補：
`10_NOVELS/AOKI_KAIROU/30_AI_WORK/30_CLAUDE/aoki_kairo_part1_ep01_v3_claude_round1.md`

改稿時の保持条件：
- プロット順を変えない。
- 主要事件を削らない。
- カリンのCA／現場管理者／ゲーム的な内面語彙を残す。
- 海洋生物兵器の体系を残す。
- ティナノ、ゲルマ、イルトの役割を消さない。
- 「碧き海狼」の呼称成立と「マルハバ」命名を残す。
- 修正理由を本文に注釈として混ぜない。

作業後、Claude自身の短い変更メモと、次のGemini向けHANDOFFを残す。
