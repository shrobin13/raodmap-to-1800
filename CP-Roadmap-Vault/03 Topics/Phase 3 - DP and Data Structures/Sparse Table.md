---
tags: [topic, phase-3, core]
phase: 3
rating: "1500-1900"
est_days: 2
priority: core
status: todo
cf_tag: "data structures"
---

# Sparse Table

> O(1) range-minimum queries on static data and the engine for LCA via Euler tour.

| | |
|---|---|
| Phase | [[Phase 3 - DP and Data Structures]] |
| Typical rating range | 1500-1900 |
| Estimated time | 2 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-08 August]] |
| Toph category | Data Structure > Sparse Table (2) |
| Codeforces tag | data structures |

**Prerequisites:** [[Binary Exponentiation]]

**Unlocks:** [[Lowest Common Ancestor]]

## What to learn

- Build `st[k][i]` for ranges of length 2^k.
- Query min of two overlapping blocks.
- Works only for idempotent operations (min, max, gcd).

## Template

```cpp
int K = __lg(n) + 1;
vector<vector<int>> st(K, vector<int>(n));
st[0] = a;
for (int k = 1; k < K; k++)
    for (int i = 0; i + (1 << k) <= n; i++)
        st[k][i] = min(st[k - 1][i], st[k - 1][i + (1 << (k - 1))]);
auto query = [&](int l, int r) {   // inclusive
    int k = __lg(r - l + 1);
    return min(st[k][l], st[k][r - (1 << k) + 1]);
};
```

## Resources

- [cp-algorithms: Sparse table](https://cp-algorithms.com/data_structures/sparse-table.html)

## Practice plan

- [ ] CSES Static Range Minimum Queries

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Using sparse table for sum (not idempotent).

## Definition of done

- [ ] You can build a sparse table with `__lg`.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
