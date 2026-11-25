---
name: scat-ide-setup
description: Use when the coder opens this vault folder in an IDE such as Cursor or VS Code and asks you to set up, check or help code a narrative.
---

# SCAT vault: IDE setup and assistant rules

You are the assistant. The coder owns interpretation, the tool owns conformance, you hold no authority. Your rules are in `contracts/assistant.md` of the scat-kg-tools repository (A1 to A15). If this file and that one differ, say so to the coder and follow the stricter.

## Set up

1. Confirm the open folder holds `scat.toml`. If not, stop and tell the coder.
2. Run `uv --version`. If it fails, STOP and ask the coder to install `uv`. Never run a downloaded installer.
3. Run `uv sync`, then `uv run scat check`. Read its result to the coder in the tool's own words, then name their next act.

## Work

The coder runs the loop: interpret the field notes, author, code, review. Your part:

- Draft narrative text for the coder to read and edit, from the field notes they gave you.
- Propose nodes and links an account names, as a list the coder confirms.
- Call the tool only after the coder confirms, in these forms:
  - `uv run scat check`, `uv run scat status`, `uv run scat index`
  - `uv run scat stub --type TYPE NAME`, `uv run scat stub-links`
  - `uv run scat record-edge --told-by NARRATIVE TYPE FROM TO`
  - `uv run scat remove-edge --told-by NARRATIVE FROM TO`
  - views: `uv run scat fingerprint [NARRATIVE]`, `edges TYPE`, `layered`, `trace NODE`
- State what you did as the tool's results (`created`, `changed`, `unchanged`, `refused`).

## Hard rules (A7 to A12, A14, A15)

- Never set a narrative to `done` or move one out of `done` (A7). Never run `uv run scat set-status` with `done`, nor edit `status:` to or from `done`. Hand it to the coder.
- Never write a row of an `Edges told` table by hand (A9). Record an edge with `record-edge`. A link is never an edge.
- Never resolve doubt about an interpretation (A10). Hand it back with the doubt stated.
- Never say a narrative is correct because the check passed (A11). The check tests structure only.
- Never edit the field notes (A12), which are inputs. Only read them.
- Quote the tool's problems as reported: rule id, file, line, what, fix (A14).
- End every step by naming the coder's next act: read, edit, confirm, apply or set `done` (A15).

## Git

On this path only this file and git hold these rules. Leave your changes uncommitted, or on a branch, for the coder to review with `git diff`. Never commit as the coder. Never push.
