---
tags: [topic, phase-4, optional]
phase: 4
rating: "1800-2200"
est_days: 6
priority: optional
status: todo
cf_tag: "data structures"
---

# Mo's Algorithm and Sqrt Decomposition

> Handles offline range queries without a complex data structure.

| | |
|---|---|
| Phase | [[Phase 4 - Advanced to 1800]] |
| Typical rating range | 1800-2200 |
| Estimated time | 6 days |
| Priority for 1800 | Optional |
| Scheduled in | [[2027-10 October]] |
| Toph category | Algorithm Techniques > Mo's Algorithm (8), Square Root Decomposition (5) |
| Codeforces tag | data structures |

**Prerequisites:** [[Sorting and Custom Comparators]], [[Two Pointers and Sliding Window]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- Block decomposition for point update + range query.
- Mo's: sort queries by block of l, then r; add/remove elements.
- Complexity O((n + q) sqrt n).

## Resources

- [cp-algorithms: Sqrt decomposition](https://cp-algorithms.com/data_structures/sqrt_decomposition.html)
- [Toph Mo's Algorithm category](https://toph.co/problems/mos-algorithm)

## Practice plan

- [ ] Toph Mo's Algorithm: 4 easiest
- [ ] CF 1800-2200 tag sqrt: 5

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Order of add/remove operations.
- Block size choice.

## Definition of done

- [ ] You can solve 'count distinct in range' offline.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
