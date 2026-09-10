# Shared GitHub handoff design — first baton-test lesson

STATUS: working workflow proposal
DATE: 2026-09-10

## Problem observed
The first 3-AI baton test exposed two transport failures:

1. Claude normal chat could see the repository default branch but did not reliably expose `work/3ai-bootstrap`, forcing manual transfer packets.
2. Manual attachment is error-prone: a producing AI can generate multiple output files, but a user may omit or accidentally attach the wrong one during handoff.

The second failure occurred immediately in the v3.1 handoff: the HANDOFF and memo arrived, while the substantive candidate manuscript did not. A repeated HANDOFF attachment then arrived instead of the candidate. This should be fixed by workflow design rather than by asking the user to be more careful.

## Adopted direction from user
The user wants GitHub to function as the shared synchronization point so cross-AI work does not depend on remembering manual attachments.

## Recommended steady-state architecture
### 1. `main` is the shared synchronization surface
All AIs should be able to read the same current structured workspace from the default branch.

Formal authority is determined by directories and explicit user approval, not by branch membership:
- `00_CANON/`, `10_FINISHED/` = formal; AI must not change/promote without user approval.
- `20_WIP/`, `30_AI_WORK/`, `90_OTHER/` = working/proposal material even when present on `main`.

### 2. `work/*` becomes optional isolation, not the transport bus
Use work branches for risky or large experiments and CANON/FINISHED candidates. Do not require ordinary AI output to live only on a branch that another AI cannot see.

### 3. Producer persists before handoff
When an AI has GitHub write access, it must commit the actual output artifact before declaring completion. Then commit memo/HANDOFF and name exact paths.

A chat-generated file that is not persisted in GitHub is not considered a completed cross-AI handoff.

### 4. Receiver reads GitHub, not user attachments
The receiving AI should fetch the exact paths in HANDOFF `READ`. Manual transfer packets remain only a fallback for read-only environments or connector failures.

### 5. Read-only Claude chat is not enough to eliminate attachment errors
Claude's standard GitHub integration is useful for reading/syncing selected repository files, but a write-capable environment is needed if Claude is expected to persist its own outputs without user transfer. Prefer Claude Code for direct GitHub persistence; a trusted write-capable connector can be considered later if needed.

## Migration
The bootstrap branch can be merged to `main` after user review. This merge does not promote WIP/AI_WORK content to CANON or FINISHED; it only makes the shared working state available on the synchronization branch.
