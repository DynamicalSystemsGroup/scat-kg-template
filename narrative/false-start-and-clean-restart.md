---
type: narrative
kind: scenario
status: done
title: "False start and clean restart"
description: "Notes on the false start, the halt, the rollback and the clean restart of this project."
timeframe: past
---

Facilitator's notes, as told. Source: the decision log, D-017 to D-022.

- Mission approved. First work packages (the ontology research and the toolchain spike) under way.
- The [[project-leads|project leads]] shared a stakeholder conversation as intent information. The new intent: the second kind in the model fits better as affordances than as properties. The acronym becomes SCAT, which the leads accepted.
- The decision was to rename everything to the new acronym, roll back, amend the mission and restart.
- Work in flight stopped before anything merged.
- The integration branch reverted to the approved mission. History kept, no force-push.
- Earlier findings kept as tags, so they stay available and do not seed the restart.
- Mission revised as an amendment. The amendment approved by the project leads' merge.
- Work restarted clean from the revised mission.
- The work was rolled back, the mission was amended, and the restart followed once the amendment was approved.
- Concerns in the telling: [[intent-without-drift|staying faithful to intent, and avoiding drift]].
- Affordances in the telling: [[gated-approval|a gated mission]]; halting before anything merges; [[revert-with-history-kept|reverting without losing history]]; tags that keep findings available without seeding the restart.

## Edges told

| from | type | to | note |
|---|---|---|---|
| [[project-leads]] | holds | [[intent-without-drift]] | The log gives these as the concerns of the false-start story, which it places with project leads (D-020). |
| [[intent-without-drift]] | is addressed by | [[gated-approval]] | The log names a gated mission among the affordances of the false-start story (D-020). |
| [[intent-without-drift]] | is addressed by | [[revert-with-history-kept]] | Halting before anything merges and reverting without losing history are both in D-020. |
