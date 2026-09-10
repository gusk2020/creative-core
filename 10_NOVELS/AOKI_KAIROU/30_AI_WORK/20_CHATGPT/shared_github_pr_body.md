# PR body draft

## Purpose
Adopt `main` as the shared synchronization surface for the 3-AI workflow while keeping formal authority path-based.

## Key rule
- `00_CANON/`, `10_FINISHED/`: formal, user approval required.
- `20_WIP/`, `30_AI_WORK/`, `90_OTHER/`: working/proposal even on `main`.
- `work/*`: optional isolation, not mandatory transport.

## Why
Claude normal chat exposed only the default branch reliably, and manual attachment handoffs already produced missing/wrong-file errors. Shared GitHub persistence should replace routine attachment transfer whenever a write-capable AI/tool is available.
