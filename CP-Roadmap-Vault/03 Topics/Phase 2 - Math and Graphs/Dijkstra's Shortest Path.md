---
tags: [topic, phase-2, core]
phase: 2
rating: "1500-1900"
est_days: 6
priority: core
status: todo
cf_tag: "shortest paths, graphs"
---

# Dijkstra's Shortest Path

> Weighted shortest path with non-negative weights shows up in nearly every serious contest.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1500-1900 |
| Estimated time | 6 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-05 May]] |
| Toph category | Graph Theory > Shortest Path (7) |
| Codeforces tag | shortest paths, graphs |

**Prerequisites:** [[Breadth-First Search]], [[Stack, Queue, Deque and Priority Queue]]

**Unlocks:** [[Bellman-Ford and Floyd-Warshall]]

## What to learn

- Priority queue Dijkstra in O((n + m) log n).
- Path reconstruction, counting shortest paths, Dijkstra on states.
- Why negative edges break it (use [[Bellman-Ford and Floyd-Warshall]]).
- Use `long long` for distances and a large INF.

## Template

```cpp
vector<ll> dijkstra(int s, const vector<vector<pair<int, ll>>> &g) {
    const ll INF = LLONG_MAX / 4;
    vector<ll> d(g.size(), INF);
    priority_queue<pair<ll, int>, vector<pair<ll, int>>, greater<>> pq;
    d[s] = 0; pq.push({0, s});
    while (!pq.empty()) {
        auto [du, u] = pq.top(); pq.pop();
        if (du != d[u]) continue;
        for (auto [v, w] : g[u]) if (d[v] > du + w) {
            d[v] = du + w; pq.push({d[v], v});
        }
    }
    return d;
}
```

## Resources

- [cp-algorithms: Dijkstra](https://cp-algorithms.com/graph/dijkstra.html)
- [Toph Shortest Path category](https://toph.co/problems/shortest-path)

## Practice plan

- [ ] CSES Shortest Routes I
- [ ] CSES Flight Discount
- [ ] CSES Investigation
- [ ] CF shortest paths 1500-1900: solve 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- INF too small or overflow when adding to INF.
- Not skipping stale queue entries.

## Definition of done

- [ ] You can write Dijkstra without looking it up and extend it to states.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
