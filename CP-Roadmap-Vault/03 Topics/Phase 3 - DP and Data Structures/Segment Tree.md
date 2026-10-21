---
tags: [topic, phase-3, core]
phase: 3
rating: "1600-2000"
est_days: 7
priority: core
status: todo
cf_tag: "data structures"
---

# Segment Tree

> The segment tree is the workhorse for range queries with updates beyond what a BIT can do.

| | |
|---|---|
| Phase | [[Phase 3 - DP and Data Structures]] |
| Typical rating range | 1600-2000 |
| Estimated time | 7 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-08 August]] |
| Toph category | Data Structure > Segment Tree (44) |
| Codeforces tag | data structures |

**Prerequisites:** [[Fenwick Tree (BIT)]]

**Unlocks:** [[Segment Tree with Lazy Propagation]], [[Heavy-Light and Centroid Decomposition]]

## What to learn

- Iterative bottom-up segment tree for sum/min/max.
- Recursive version for flexibility.
- Point update, range query; descent for first index with property.
- Merging nodes (store tuples like min+count).

## Template

```cpp
struct Seg {   // sum, iterative, query [l, r)
    int n; vector<ll> t;
    Seg(int n) : n(n), t(2 * n, 0) {}
    void set(int i, ll v) { for (t[i += n] = v; i > 1; i >>= 1) t[i >> 1] = t[i] + t[i ^ 1]; }
    ll query(int l, int r) {
        ll res = 0;
        for (l += n, r += n; l < r; l >>= 1, r >>= 1) {
            if (l & 1) res += t[l++];
            if (r & 1) res += t[--r];
        }
        return res;
    }
};
```

## Resources

- [cp-algorithms: Segment tree](https://cp-algorithms.com/data_structures/segment_tree.html)
- [ITMO Academy course: Segment Tree, part 1](https://codeforces.com/edu/courses)
- [Toph Segment Tree category](https://toph.co/problems/segment-tree)

## Practice plan

- [ ] CSES Dynamic Range Minimum Queries
- [ ] CSES Range Sum Queries II
- [ ] CSES Hotel Queries
- [ ] CF data structures 1600-1900: 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Wrong identity element for min/max.
- Half-open vs closed interval confusion.

## Definition of done

- [ ] You can adapt a segment tree to a new merge operation in 10 minutes.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
