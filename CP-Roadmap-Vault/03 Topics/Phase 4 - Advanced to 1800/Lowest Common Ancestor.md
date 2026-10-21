---
tags: [topic, phase-4, core]
phase: 4
rating: "1600-2000"
est_days: 5
priority: core
status: todo
cf_tag: "trees, graphs"
---

# Lowest Common Ancestor

> LCA is the key to tree distances and path queries.

| | |
|---|---|
| Phase | [[Phase 4 - Advanced to 1800]] |
| Typical rating range | 1600-2000 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-09 September]] |
| Toph category | Trees > Lowest Common Ancestor (7) |
| Codeforces tag | trees, graphs |

**Prerequisites:** [[Depth-First Search]], [[Sparse Table]]

**Unlocks:** [[Heavy-Light and Centroid Decomposition]]

## What to learn

- Binary lifting in O(log n) per query.
- Euler tour + sparse table for O(1).
- Distance `d(u,v) = dep[u] + dep[v] - 2 * dep[lca]`.

## Template

```cpp
const int LOG = 20;
vector<array<int, LOG>> up(n + 1);
vector<int> dep(n + 1);
// dfs fills up[v][0] = parent, dep[v]
for (int k = 1; k < LOG; k++) for (int v = 1; v <= n; v++) up[v][k] = up[up[v][k - 1]][k - 1];
auto lca = [&](int a, int b) {
    if (dep[a] < dep[b]) swap(a, b);
    int d = dep[a] - dep[b];
    for (int k = 0; k < LOG; k++) if (d >> k & 1) a = up[a][k];
    if (a == b) return a;
    for (int k = LOG - 1; k >= 0; k--) if (up[a][k] != up[b][k]) { a = up[a][k]; b = up[b][k]; }
    return up[a][0];
};
```

## Resources

- [cp-algorithms: LCA](https://cp-algorithms.com/graph/lca.html)
- [cp-algorithms: LCA with binary lifting](https://cp-algorithms.com/graph/lca_binary_lifting.html)

## Practice plan

- [ ] CSES Company Queries I
- [ ] CSES Company Queries II
- [ ] CSES Distance Queries

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Not lifting both nodes to the same depth first.

## Definition of done

- [ ] You can answer path-distance queries on a tree.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
