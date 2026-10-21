---
tags: [topic, phase-2, core]
phase: 2
rating: "1300-1800"
est_days: 4
priority: core
status: todo
cf_tag: "dsu, graphs"
---

# Disjoint Set Union

> DSU is a tiny data structure that solves connectivity, grouping and Kruskal in near-constant time.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1300-1800 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-05 May]] |
| Toph category | Data Structure (tag DisjointSets), Graph Theory |
| Codeforces tag | dsu, graphs |

**Prerequisites:** [[Graph Basics and Representation]]

**Unlocks:** [[Minimum Spanning Tree]]

## What to learn

- Union by size and path compression.
- Count components, check connectivity under merges.
- Offline tricks (process queries backwards to turn deletions into merges).
- Foundation of Kruskal ([[Minimum Spanning Tree]]).

## Template

```cpp
struct DSU {
    vector<int> p, sz;
    DSU(int n) : p(n), sz(n, 1) { iota(p.begin(), p.end(), 0); }
    int find(int x) { return p[x] == x ? x : p[x] = find(p[x]); }
    bool unite(int a, int b) {
        a = find(a); b = find(b);
        if (a == b) return false;
        if (sz[a] < sz[b]) swap(a, b);
        p[b] = a; sz[a] += sz[b];
        return true;
    }
};
```

## Resources

- [cp-algorithms: Disjoint Set Union](https://cp-algorithms.com/data_structures/disjoint_set_union.html)
- [ITMO Academy course: Disjoint Sets Union (Codeforces EDU)](https://codeforces.com/edu/courses)

## Practice plan

- [ ] CSES Road Construction
- [ ] CSES Building Roads
- [ ] CF dsu 1300-1700: solve 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Not compressing paths (slow) or forgetting to `find` before comparing.
- Using union by size and forgetting to update size.

## Definition of done

- [ ] You can write DSU in 1 minute.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
