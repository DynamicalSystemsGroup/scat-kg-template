# Instructions for an assistant in this vault

This folder is a SCAT vault: pages in git, checked by the `scat` tool. Before you do anything else, read
`.claude/skills/scat-ide-setup/SKILL.md` and follow it. It sets out how to start (`uv sync`, `uv run scat check`),
what you may run, and what you must never do. Its "Stage" section says how to find the project's stage and keep to it.

Three actors work here:

- The coder owns interpretation: what the field notes mean, what the narrative says, and when it is `done`.
- The tool owns conformance: `uv run scat check` decides whether the vault is well formed, not you.
- You help and hold no authority. Draft and propose; the coder decides. Never set a narrative to `done`, never run
  `uv run scat set-status`, never say a narrative is correct because the check passed, and leave your edits
  uncommitted so the coder can read `git diff`.
