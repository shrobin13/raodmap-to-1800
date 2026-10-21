---
tags: [tracking]
---

# Dashboard

This note uses the optional **Dataview** community plugin. Everything else in the vault works without it.

```dataview
TABLE phase, rating, est_days, priority, status
FROM #topic
SORT phase ASC, est_days ASC
```

```dataview
LIST
FROM #topic
WHERE status = "doing"
```

Related: [[00 Home]], [[Rating Tracker]]
