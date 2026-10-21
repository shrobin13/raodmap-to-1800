---
tags: [topic, phase-4, core]
phase: 4
rating: "1900-2300"
est_days: 5
priority: core
status: todo
cf_tag: "graphs, dfs and similar"
---

# Strongly Connected Components and Bridges

> SCCs condense a directed graph into a DAG; bridges and articulation points solve connectivity under failure.

| | |
|---|---|
| Phase | [[Phase 4 - Advanced to 1800]] |
| Typical rating range | 1900-2300 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-10 October]] |
| Toph category | Graph Theory > Strongly Connected Components (3) |
| Codeforces tag | graphs, dfs and similar |

**Prerequisites:** [[Depth-First Search]], [[Topological Sort and DAGs]]

**Unlocks:** [[2-SAT]]

## What to learn

- **Kosaraju's algorithm:** two DFS passes (forward on G, reverse on G^T), each SCC discovered in the second pass.
- **Tarjan's algorithm:** single DFS using `disc` and `low` arrays; an SCC is finalized when stack top equals root.
- **Condensation:** replace each SCC with a single node → result is always a DAG.
- **Bridges and articulation points:** use low-link. A bridge is edge (u,v) where `low[v] > disc[u]`. An articulation point is a vertex whose removal disconnects the graph.
- After condensation, problems often reduce to DP on a DAG ([[DP Foundations]], [[Topological Sort and DAGs]]).
- 2-SAT uses SCC on the implication graph ([[2-SAT]]).

## Template

```cpp
// Kosaraju's SCC — O(V + E)
vector<vector<int>> g, rg;  // original and reversed graph
vector<int> order, comp;
vector<bool> visited;

void dfs1(int v) {
    visited[v] = true;
    for (int u : g[v]) if (!visited[u]) dfs1(u);
    order.push_back(v);
}
void dfs2(int v, int c) {
    comp[v] = c;
    for (int u : rg[v]) if (comp[u] == -1) dfs2(u, c);
}
int kosaraju(int n) {
    visited.assign(n, false);
    for (int i = 0; i < n; i++) if (!visited[i]) dfs1(i);
    comp.assign(n, -1);
    int num = 0;
    for (int i = n - 1; i >= 0; i--)
        if (comp[order[i]] == -1) dfs2(order[i], num++);
    return num;  // number of SCCs
}
```

> ⚠️ Use **iterative DFS** for large n (recursion depth can hit stack limit).

## Resources

- [cp-algorithms: Strongly connected components](https://cp-algorithms.com/graph/strongly-connected-components.html)
- [cp-algorithms: Bridge searching](https://cp-algorithms.com/graph/bridge-searching.html)
- [cp-algorithms: Articulation points](https://cp-algorithms.com/graph/cutpoints.html)

## Practice plan

- [ ] CSES Planets and Kingdoms
- [ ] CSES Coin Collector
- [ ] CSES Flight Routes Check
- [ ] CSES Reachability Queries (condensation + DAG reachability)
- [ ] CF graphs/SCC 1700-2100: solve 10
- [ ] Implement Kosaraju on an undirected graph to find bridges

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Recursion depth on large graphs.

## Definition of done

- [ ] You can compress SCCs and run DP on the DAG.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
