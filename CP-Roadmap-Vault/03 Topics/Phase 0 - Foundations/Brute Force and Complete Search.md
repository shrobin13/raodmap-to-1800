---
tags: [topic, phase-0, core]
phase: 0
rating: "800-1200"
est_days: 5
priority: core
status: todo
cf_tag: "brute force"
---

# Brute Force and Complete Search

> Brute force is the correct answer for small constraints and is also how you validate smarter solutions.

| | |
|---|---|
| Phase | [[Phase 0 - Foundations]] |
| Typical rating range | 800-1200 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-11 November]] |
| Toph category | Ad-hoc > Brute Force (51) |
| Codeforces tag | brute force |

**Prerequisites:** [[Implementation]]

**Unlocks:** [[Recursion and Backtracking]], [[Meet in the Middle]]

## What to learn

- Nested loops over all candidates; check constraints first to confirm it fits.
- Enumerate subsets with bitmasks `for (int mask = 0; mask < (1 << n); mask++)`.
- Enumerate permutations with `next_permutation` (sort first).
- Prune early: stop the loop as soon as the answer cannot improve.
- Write a brute force for every problem you are unsure about and compare outputs (stress testing, see [[Stress Testing]]).

## Resources

- [Codeforces problemset (brute force)](https://codeforces.com/problemset?tags=brute+force)
- [Toph Brute Force category](https://toph.co/problems/brute-force)

## Practice plan

- [ ] CSES Apple Division
- [ ] CSES Creating Strings
- [ ] CF brute force 800-1100: solve 20
- [ ] Toph Brute Force: 15 easiest

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Underestimating the loop count (n^3 with n = 2e3 is too slow).
- Forgetting to consider the empty set or single element.

## Definition of done

- [ ] You can enumerate subsets and permutations without looking up syntax.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
