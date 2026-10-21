---
tags: [topic, phase-1, core]
phase: 1
rating: "900-1300"
est_days: 5
priority: core
status: todo
cf_tag: "sortings, greedy"
---

# Sorting and Custom Comparators

> Sorting unlocks greedy, binary search, two pointers and sweep-line ideas.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 900-1300 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-12 December]] |
| Toph category | Algorithm Techniques > Sorting (37) |
| Codeforces tag | sortings, greedy |

**Prerequisites:** [[STL Essentials]], [[Implementation]]

**Unlocks:** [[Binary Search and Search on the Answer]], [[Two Pointers and Sliding Window]], [[Greedy Algorithms]], [[Minimum Spanning Tree]], [[Mo's Algorithm and Sqrt Decomposition]], [[Divide and Conquer]]

## What to learn

- `sort`, `stable_sort`, sort by key, sort pairs, sort indices instead of values.
- Custom comparators must be a strict weak ordering (use `<`, never `<=`).
- Coordinate compression: sort + unique + lower_bound.
- Sort + greedy; sort + two pointers; sort + binary search.
- Counting sort for small value ranges.

## Template

```cpp
// coordinate compression
vector<int> vals = a;
sort(vals.begin(), vals.end());
vals.erase(unique(vals.begin(), vals.end()), vals.end());
for (auto &x : a) x = lower_bound(vals.begin(), vals.end(), x) - vals.begin();
```

## Resources

- [cp-algorithms: Sorting overview (see algorithms index)](https://cp-algorithms.com/)
- [USACO Guide (module: Sorting)](https://usaco.guide/)
- [Toph Sorting category](https://toph.co/problems/sorting)

## Practice plan

- [ ] CSES Apartments
- [ ] CSES Movie Festival
- [ ] CSES Stick Lengths
- [ ] CSES Collecting Numbers
- [ ] CSES Tasks and Deadlines
- [ ] CF sortings 900-1300: solve 20

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- A comparator using `<=` causes a runtime error or undefined behavior.
- Sorting a copy of the data and losing original indices.

## Definition of done

- [ ] You can sort by two keys and explain why your comparator is valid.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
