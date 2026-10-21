---
tags: [topic, phase-3, core]
phase: 3
rating: "1500-1900"
est_days: 4
priority: core
status: todo
cf_tag: "data structures"
---

# Fenwick Tree (BIT)

> A Fenwick tree gives point-update and prefix-query in O(log n) with tiny code.

| | |
|---|---|
| Phase | [[Phase 3 - DP and Data Structures]] |
| Typical rating range | 1500-1900 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-07 July]] |
| Toph category | Data Structure > Fenwick Tree (13) |
| Codeforces tag | data structures |

**Prerequisites:** [[Prefix Sums and Difference Arrays]]

**Unlocks:** [[Segment Tree]], [[Euler Tour and Tree Flattening]]

## What to learn

- Point update, prefix sum, range sum.
- Range update + point query via difference array.
- Counting inversions with coordinate compression.
- Find k-th element via binary lifting on the tree (optional).

## Template

```cpp
struct BIT {
    int n; vector<ll> t;
    BIT(int n) : n(n), t(n + 1, 0) {}
    void add(int i, ll v) { for (++i; i <= n; i += i & -i) t[i] += v; }
    ll sum(int i) { ll s = 0; for (++i; i > 0; i -= i & -i) s += t[i]; return s; }   // prefix [0..i]
    ll range(int l, int r) { return sum(r) - (l ? sum(l - 1) : 0); }
};
```

## Resources

- [cp-algorithms: Fenwick tree](https://cp-algorithms.com/data_structures/fenwick.html)
- [Toph Fenwick Tree category](https://toph.co/problems/fenwick-tree)

## Practice plan

- [ ] CSES Dynamic Range Sum Queries
- [ ] CSES Range Update Queries
- [ ] CSES Salary Queries (needs compression)
- [ ] CF data structures 1500-1800: 12

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- BIT is 1-indexed; index 0 loops forever.
- Overflow: use `long long`.

## Definition of done

- [ ] You can count inversions in O(n log n) from memory.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
