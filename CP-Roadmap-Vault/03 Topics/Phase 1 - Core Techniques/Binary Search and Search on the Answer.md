---
tags: [topic, phase-1, core]
phase: 1
rating: "1000-1600"
est_days: 7
priority: core
status: todo
cf_tag: "binary search"
---

# Binary Search and Search on the Answer

> One of the highest-return techniques: whenever the answer is monotonic, you can search it instead of constructing it.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 1000-1600 |
| Estimated time | 7 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-12 December]] |
| Toph category | Algorithm Techniques > Binary Search (63), Ternary Search (9) |
| Codeforces tag | binary search |

**Prerequisites:** [[Sorting and Custom Comparators]]

**Unlocks:** [[Greedy Algorithms]], [[DP Foundations]], [[Meet in the Middle]], [[Interactive Problems]]

## What to learn

- Binary search on a sorted array: `lower_bound`, `upper_bound`.
- Binary search on the answer: define `ok(x)` that is monotonic, find the first true.
- Floating-point binary search (iterate 100 times instead of using epsilon).
- Ternary search for unimodal functions (see Toph Ternary Search).
- Checking feasibility is often a greedy or a linear scan.

## Template

```cpp
// smallest x in [lo, hi] with ok(x) == true (ok is monotone: false...false true...true)
ll lo = 0, hi = 1e18;
while (lo < hi) {
    ll mid = lo + (hi - lo) / 2;
    if (ok(mid)) hi = mid;
    else lo = mid + 1;
}
// answer: lo
```

## Resources

- [cp-algorithms: Binary search](https://cp-algorithms.com/num_methods/binary_search.html)
- [cp-algorithms: Ternary search](https://cp-algorithms.com/num_methods/ternary_search.html)
- [ITMO Academy course: Binary Search (Codeforces EDU)](https://codeforces.com/edu/courses)
- [USACO Guide (module: Binary Search)](https://usaco.guide/)

## Practice plan

- [ ] CSES Factory Machines
- [ ] CSES Array Division
- [ ] CSES Sum of Two Values (after sorting)
- [ ] CF binary search 1100-1500: solve 25
- [ ] Toph Binary Search: 20 easiest

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Infinite loops when `lo = mid` without rounding up.
- Predicate that is not actually monotonic.
- Overflow in `lo + hi`; use `lo + (hi - lo) / 2`.

## Definition of done

- [ ] You can write search-on-answer from memory and justify monotonicity for each problem.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
