---
tags: [topic, phase-2, core]
phase: 2
rating: "1400-1800"
est_days: 4
priority: core
status: todo
cf_tag: "graphs, dp"
---

# Topological Sort and DAGs

> Topological order is the evaluation order for DP on DAGs and dependency problems.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1400-1800 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-05 May]] |
| Toph category | Graph Theory > Topological Sort (0) |
| Codeforces tag | graphs, dp |

**Prerequisites:** [[Depth-First Search]], [[Breadth-First Search]]

**Unlocks:** [[Strongly Connected Components and Bridges]]

## What to learn

- Kahn's algorithm with in-degree counts.
- DFS-based topological order.
- Cycle detection as a byproduct.
- DP on a DAG (longest/shortest path, counting paths).

## Template

```cpp
vector<int> indeg(n + 1, 0), order;
for (int u = 1; u <= n; u++) for (int v : g[u]) indeg[v]++;
queue<int> q;
for (int i = 1; i <= n; i++) if (!indeg[i]) q.push(i);
while (!q.empty()) {
    int u = q.front(); q.pop(); order.push_back(u);
    for (int v : g[u]) if (--indeg[v] == 0) q.push(v);
}
// if order.size() < n -> cycle
```

## Resources

- [cp-algorithms: Topological sort](https://cp-algorithms.com/graph/topological-sort.html)

## Practice plan

- [ ] CSES Course Schedule
- [ ] CSES Longest Flight Route
- [ ] CSES Game Routes

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Missing nodes with zero in-degree and no edges.
- Not detecting a cycle (order shorter than n).

## Definition of done

- [ ] You can solve a path-counting DP on a DAG.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
