---
tags: [topic, phase-3, core]
phase: 3
rating: "1500-2000"
est_days: 6
priority: core
status: todo
cf_tag: "dp, trees"
---

# Tree DP

> Tree DP is the standard way to solve counting and optimization on rooted trees.

| | |
|---|---|
| Phase | [[Phase 3 - DP and Data Structures]] |
| Typical rating range | 1500-2000 |
| Estimated time | 6 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-08 August]] |
| Toph category | Trees > Tree DP (0), Dynamic Programming |
| Codeforces tag | dp, trees |

**Prerequisites:** [[Depth-First Search]], [[DP Foundations]]

**Unlocks:** [[Lowest Common Ancestor]], [[Heavy-Light and Centroid Decomposition]]

## What to learn

- **Subtree DP (Bottom-up DFS):** Root the tree at arbitrary node (usually 1). Recursively compute subproblems on children and combine at parent during post-order traversal.
- **Classic Subtree Problems:**
  - Subtree sizes: `sz[u] = 1 + sum(sz[v])`.
  - Tree Diameter: `max(depth1 + depth2)` across children.
  - Maximum Independent Set on trees: `dp[u][0]` (u not chosen), `dp[u][1]` (u chosen).
- **Rerooting DP (Up-and-down technique):**
  - First pass (bottom-up): compute DP considering only subtrees.
  - Second pass (top-down): pass accumulated values from parent down to children, obtaining the answer if *every* node were the root in $O(N)$ total time.

## Template (Subtree DP)

```cpp
#include <bits/stdc++.h>
using namespace std;

const int MAXN = 2e5 + 5;
vector<int> adj[MAXN];
int sz[MAXN];
long long dp[MAXN][2]; // [0] = not included, [1] = included

void dfs(int u, int p) {
    sz[u] = 1;
    dp[u][0] = 0;
    dp[u][1] = 1; // e.g. independent set weight

    for (int v : adj[u]) {
        if (v == p) continue;
        dfs(v, u);
        sz[u] += sz[v];

        // combine DP values
        dp[u][0] += max(dp[v][0], dp[v][1]);
        dp[u][1] += dp[v][0];
    }
}
```

## Resources

- [AtCoder Educational DP Contest: Task P (Independent Set)](https://atcoder.jp/contests/dp/tasks/dp_p)
- [CSES Tree Algorithms Problemset](https://cses.fi/problemset/)
- [USACO Guide - Tree DP](https://usaco.guide/gold/dp-trees)

## Practice plan

- [ ] CSES Subordinates (Subtree sizes)
- [ ] CSES Tree Matching (Classic Tree DP)
- [ ] CSES Tree Diameter
- [ ] CSES Tree Distances I
- [ ] CSES Tree Distances II (Intro to Rerooting DP)
- [ ] CSES Finding a Centroid
- [ ] AtCoder DP Task P - Independent Set
- [ ] CF 1324F - Maximum White Subtree (1800)
- [ ] CF 161D - Distance in Tree (1800)
- [ ] CF 1187E - Tree Painting (Rerooting classic) (2100)

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Recursion depth on chain-shaped trees.
- Mixing up parent and child in the combine step.

## Definition of done

- [ ] You can compute subtree sizes and diameter with DFS without notes.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
