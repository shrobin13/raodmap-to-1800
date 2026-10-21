---
tags: [topic, phase-2, core]
phase: 2
rating: "1100-1500"
est_days: 3
priority: core
status: todo
cf_tag: "graphs"
---

# Graph Basics and Representation

> Everything in graph theory starts with modelling the problem as vertices and edges.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1100-1500 |
| Estimated time | 3 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-04 April]] |
| Toph category | Graph Theory (134) |
| Codeforces tag | graphs |

**Prerequisites:** [[STL Essentials]], [[Recursion and Backtracking]]

**Unlocks:** [[Breadth-First Search]], [[Depth-First Search]], [[Disjoint Set Union]]

## What to learn

- Adjacency list `vector<vector<int>> g(n)` is the default; edge list for Kruskal; matrix only when n <= 500.
- Directed vs undirected, weighted vs unweighted, multi-edges, self-loops.
- Grids as implicit graphs; states as nodes.
- Connected components, degrees, trees as graphs with n-1 edges.

## Template

```cpp
int n, m;
cin >> n >> m;
vector<vector<int>> g(n + 1);
for (int i = 0; i < m; i++) {
    int u, v;
    cin >> u >> v;
    g[u].push_back(v);
    g[v].push_back(u);   // remove for directed
}
```

## Resources

- [CSES Graph Algorithms](https://cses.fi/problemset/)
- [Toph Graph Theory category](https://toph.co/problems/graph-theory)
- [VisuAlgo (graph visualizations)](https://visualgo.net/)

## Practice plan

- [ ] CF graphs 1000-1300: read the statements and just model them (draw the graph) for 15 problems

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Forgetting that input may be 1-indexed.
- Adding edges once for an undirected graph.

## Definition of done

- [ ] You can turn any 'cities and roads' statement into code in minutes.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
