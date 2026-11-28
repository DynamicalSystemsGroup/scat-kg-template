---
type: narrative
kind: architecture
status: done
title: "Two branches and tags pitch"
description: "The pitch that two branches and archive tags give approved work, a safe rollback and kept findings."
timeframe: future
---

Pitch notes, as given.

- One branch, [[main-and-dev-branches|main]], holds approved missions and releases only. A second, dev, integrates the work. Work happens on short-lived branches off dev.
- [[gated-approval|Approval is a merge into main]]. A mission is approved when the project leads merge it.
- When work must be undone, [[revert-with-history-kept|dev is reverted to the approved state. History is kept]], no force-push.
- Abandoned work is [[archive-tags|tagged under archive/]] before it goes. The tags keep the findings available without seeding the restart.
- Branch tidy-up is periodic and advisory.

## Edges told

| from | type | to | note |
|---|---|---|---|
| [[intent-without-drift]] | is addressed by | [[gated-approval]] | A gate before approval keeps the work tied to the intent that was approved. |
| [[intent-without-drift]] | is addressed by | [[revert-with-history-kept]] | Rolling back to the approved state removes drift, and the history stays. |
| [[gated-approval]] | is provided by | [[main-and-dev-branches]] | The approval gate is provided by the main and dev branches. Dev integrates, main holds approved missions and releases only, and a merge into main is the approval. |
| [[revert-with-history-kept]] | is provided by | [[archive-tags]] | The archive tags keep what a rollback sets aside. Abandoned work is tagged under archive/ first, so findings stay available without seeding the restart. |
