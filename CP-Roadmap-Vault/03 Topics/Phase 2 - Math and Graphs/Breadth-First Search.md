---
tags: [topic, phase-2, core]
phase: 2
rating: "1200-1700"
est_days: 6
priority: core
status: todo
cf_tag: "graphs, shortest paths, dfs and similar"
---

# Breadth-First Search

> BFS gives shortest paths in unweighted graphs and grids, the most common graph task below 1700.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1200-1700 |
| Estimated time | 6 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-04 April]] |
| Toph category | Graph Theory > Graph Traversal (59) |
| Codeforces tag | graphs, shortest paths, dfs and similar |

**Prerequisites:** [[Graph Basics and Representation]], [[Stack, Queue, Deque and Priority Queue]]

**Unlocks:** [[Topological Sort and DAGs]], [[Dijkstra's Shortest Path]], [[Flow and Bipartite Matching]]

## What to learn

- Queue-based BFS with distance array.
- Grid BFS with direction arrays.
- Multi-source BFS (push all sources first).
- 0-1 BFS with a deque.
- Path reconstruction via a parent array.
- BFS on states (position + extra info).

## Template

```cpp
vector<int> dist(n + 1, -1);
queue<int> q;
dist[s] = 0; q.push(s);
while (!q.empty()) {
    int u = q.front(); q.pop();
    for (int v : g[u]) if (dist[v] == -1) {
        dist[v] = dist[u] + 1;
        q.push(v);
    }
}
```

## Resources

- [cp-algorithms: Breadth-first search](https://cp-algorithms.com/graph/breadth-first-search.html)
- [USACO Guide (module: Breadth First Search)](https://usaco.guide/)

## Practice plan

- [ ] CSES Message Route
- [ ] CSES Labyrinth
- [ ] CSES Monsters
- [ ] CSES Building Teams
- [ ] CF graphs/BFS 1200-1600: solve 20
- [ ] Toph Graph Traversal: 20 easiest

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Marking visited when popping instead of pushing (duplicate pushes).
- Using DFS where shortest path is needed.

## Definition of done

- [ ] You can write grid BFS with path reconstruction in 5 minutes.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
