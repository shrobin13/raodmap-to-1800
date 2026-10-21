---
tags: [topic, phase-1, core]
phase: 1
rating: "1000-1500"
est_days: 4
priority: core
status: todo
cf_tag: "two pointers"
---

# Two Pointers and Sliding Window

> Converts many O(n^2) scans into O(n) when the condition is monotone in the window.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 1000-1500 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-01 January]] |
| Toph category | Algorithm Techniques > Two Pointer (10) |
| Codeforces tag | two pointers |

**Prerequisites:** [[Sorting and Custom Comparators]]

**Unlocks:** [[Mo's Algorithm and Sqrt Decomposition]]

## What to learn

- Window `[l, r]`: advance `r`, shrink `l` while the constraint is violated.
- Sorted array pair problems (sum = target, closest pair).
- Count subarrays with a property (count windows ending at each `r`).
- Merging two sorted lists.

## Resources

- [ITMO Academy course: Two Pointers Method (Codeforces EDU)](https://codeforces.com/edu/courses)
- [USACO Guide (module: Two Pointers)](https://usaco.guide/)

## Practice plan

- [ ] CSES Sum of Two Values
- [ ] CSES Subarray Sums I
- [ ] CSES Playlist
- [ ] CSES Distinct Values Subarrays
- [ ] CSES Sum of Three Values
- [ ] CF two pointers 1000-1500: solve 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Shrinking window incorrectly when the condition is not monotone (negative numbers).
- Counting windows twice.

## Definition of done

- [ ] You can tell whether a problem is two-pointers-friendly in under a minute.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
