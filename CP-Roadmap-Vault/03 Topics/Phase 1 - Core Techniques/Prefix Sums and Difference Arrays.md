---
tags: [topic, phase-1, core]
phase: 1
rating: "900-1400"
est_days: 4
priority: core
status: todo
cf_tag: "data structures, implementation"
---

# Prefix Sums and Difference Arrays

> Range queries without updates and range updates without queries both reduce to prefix sums.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 900-1400 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-01 January]] |
| Toph category | Ad-hoc, Data Structure (Linear) |
| Codeforces tag | data structures, implementation |

**Prerequisites:** [[Implementation]]

**Unlocks:** [[Fenwick Tree (BIT)]]

## What to learn

- 1D prefix sum `p[i+1] = p[i] + a[i]`, range sum `p[r+1] - p[l]`.
- 2D prefix sums for rectangle queries.
- Difference array for many range additions followed by one read.
- Prefix XOR; prefix counts per character; prefix sum with a `map` to count subarrays with sum k.
- Prefix sums modulo m for divisibility counting.

## Template

```cpp
vector<ll> p(n + 1, 0);
for (int i = 0; i < n; i++) p[i + 1] = p[i] + a[i];
// sum of a[l..r] (0-indexed, inclusive)
ll s = p[r + 1] - p[l];
```

## Resources

- [USACO Guide (module: Prefix Sums)](https://usaco.guide/)
- [CSES Range Queries section](https://cses.fi/problemset/)

## Practice plan

- [ ] CSES Static Range Sum Queries
- [ ] CSES Range Xor Queries
- [ ] CSES Subarray Sums II
- [ ] CSES Subarray Divisibility
- [ ] CSES Forest Queries
- [ ] CF 1000-1300 tagged `data structures` or `implementation`: 15 problems that use prefix sums

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Mixing 0/1 indexing between array and prefix array.
- Not using `long long` for prefix sums.

## Definition of done

- [ ] You instinctively reach for prefix sums on any 'sum of subarray' query.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
