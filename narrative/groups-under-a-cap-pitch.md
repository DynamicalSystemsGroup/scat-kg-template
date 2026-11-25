---
type: narrative
kind: architecture
status: done
title: "Groups under a cap pitch"
description: "The pitch that people enter the data as groups, clustered to fit a cap set for each instance."
timeframe: future
---

Pitch notes, as given. Source: the decision log (D-020) and the mission.

- [[groups-clustered-under-a-cap|The vault holds groups]], and [[cap-setting|an instance setting]] caps their number.
- The cap is set for each vault, in the vault's own configuration. The example vault sets it to 3.
- A group is named by its role. No group stands for one identifiable person.
- Reason given in the record: the people in the data are groups under the Chatham House rule, so [[anonymity|no individual is identifiable]].

## Edges told

| from | type | to | note |
|---|---|---|---|
| [[anonymity]] | is addressed by | [[groups-clustered-under-a-cap]] | Participants appear only as groups, so no group stands for one identifiable person. |
| [[groups-clustered-under-a-cap]] | is provided by | [[cap-setting]] | The cap setting is what fixes the number of groups. The cap is a per-instance parameter (D-020); the example vault sets it to 3. |
