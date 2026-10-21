---
tags: [topic, phase-2, core]
phase: 2
rating: "1200-1700"
est_days: 6
priority: core
status: todo
cf_tag: "dfs and similar, graphs, trees"
---

# Depth-First Search

> DFS powers components, cycles, trees, topological sort, SCC and most tree algorithms.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1200-1700 |
| Estimated time | 6 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-04 April]] |
| Toph category | Graph Theory > Graph Traversal (59) |
| Codeforces tag | dfs and similar, graphs, trees |

**Prerequisites:** [[Graph Basics and Representation]]

**Unlocks:** [[Topological Sort and DAGs]], [[Tree DP]], [[Lowest Common Ancestor]], [[Euler Tour and Tree Flattening]], [[Strongly Connected Components and Bridges]], [[Flow and Bipartite Matching]]

## What to learn

- Recursive DFS with `visited`; track parent in undirected graphs.
- Connected components, flood fill, bipartite check.
- Cycle detection (colors for directed, parent check for undirected).
- Entry/exit times `tin`/`tout`.
- Deep recursion (n = 2e5 chain) may overflow the stack; use iterative DFS or increase the stack.

## Template

```cpp
vector<int> vis(n + 1, 0);
function<void(int, int)> dfs = [&](int u, int p) {
    vis[u] = 1;
    for (int v : g[u]) if (v != p && !vis[v]) dfs(v, u);
};
for (int i = 1; i <= n; i++) if (!vis[i]) dfs(i, 0);
```

## Resources

- [cp-algorithms: Depth-first search](https://cp-algorithms.com/graph/depth-first-search.html)

## Practice plan

- [ ] CSES Counting Rooms
- [ ] CSES Building Roads
- [ ] CSES Round Trip
- [ ] CF dfs 1200-1600: solve 20

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Parent check missing in an undirected cycle test.
- Recursion depth crashes.

## Definition of done

- [ ] You can write DFS for components, cycle detection and tin/tout from memory.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
