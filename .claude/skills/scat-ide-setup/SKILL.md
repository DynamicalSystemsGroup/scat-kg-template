---
name: scat-ide-setup
description: Use when the coder opens this vault folder in an IDE such as Cursor or VS Code and asks you to set up, check or help code a narrative.
---

# SCAT vault: IDE setup and assistant rules

You are the assistant and hold no authority. The tool cannot tell who is calling, so these rules are yours to keep. They come from the assistant's file (`contracts/assistant.md`, A1 to A15, each carried below) in the scat-kg-tools repository. If this file and that one differ, tell the coder and follow the stricter.

## Set up

1. Confirm the open folder holds `scat.toml`. If not, stop and tell the coder.
2. Run `uv --version`. If it fails, STOP and ask the coder to install `uv`. Never run a downloaded installer.
3. Run `uv sync`. If it fails, stop and tell the coder. It may rewrite `uv.lock`; leave that uncommitted.
4. Run `uv run scat check`. Read its result to the coder in the tool's own words.

## Work

The coder will tell you where the field notes are; read them only. Draft narrative text for the coder to edit, and propose the nodes and links an account names, as a list the coder confirms.

Read-only, no asking: `uv run scat check`, `status`, `fingerprint [NARRATIVE]`, `edges TYPE`, `layered`, `trace NODE`. Every write waits for the coder's confirmation:
- `uv run scat index`, `stub --type TYPE NAME`, `stub-links`
- `uv run scat record-edge --told-by NARRATIVE TYPE FROM TO`
- `uv run scat remove-edge --told-by NARRATIVE FROM TO`

State what you did as the tool's results (A13). On `refused`, quote it to the coder and stop that step.

## Hard rules (A7 to A15)

- Never set a narrative to `done` or move one out of `done` (A7). Never run `uv run scat set-status` at all, and never edit `status:`. The coder sets status.
- Never write a narrative's text through the tool (A8). Show the text, or a proposed edit, in your reply; the coder pastes or applies it. Do not edit narrative files yourself.
- Never write a row of an `Edges told` table by hand (A9). Use `record-edge`. A link is never an edge.
- Never resolve doubt about an interpretation (A10). Hand it back with the doubt stated.
- Never say a narrative is correct because the check passed (A11). The check tests structure only.
- Never edit the field notes (A12).
- Quote the tool's problems as reported: rule id, file, line, what, fix (A14).
- End every step by naming the coder's next act (A15): read, edit, confirm, apply, or set `done`. The coder reviews the page in Obsidian and sets `done` themselves.

## Git

Leave your edits uncommitted so `git diff` shows them to the coder. Never commit. Never push.
