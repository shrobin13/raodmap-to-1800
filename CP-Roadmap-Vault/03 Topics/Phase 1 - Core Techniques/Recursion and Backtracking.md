---
tags: [topic, phase-1, core]
phase: 1
rating: "1000-1500"
est_days: 4
priority: core
status: todo
cf_tag: "brute force, dfs and similar"
---

# Recursion and Backtracking

> Backtracking is the pattern behind generating all configurations and a gateway to DFS and DP.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 1000-1500 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-12 December]] |
| Toph category | Ad-hoc > Backtracking (2) |
| Codeforces tag | brute force, dfs and similar |

**Prerequisites:** [[Brute Force and Complete Search]]

**Unlocks:** [[Graph Basics and Representation]], [[DP Foundations]]

## What to learn

- Recursive function with state, choose / explore / undo.
- Generating subsets, permutations, N-Queens.
- Pruning with bounds and early exits.
- Convert recursion to memoized DP when states repeat (leads to [[DP Foundations]]).

## Resources

- [CSES Introductory Problems (Chessboard and Queens)](https://cses.fi/problemset/)
- [Toph Backtracking category](https://toph.co/problems/backtracking)

## Practice plan

- [ ] CSES Chessboard and Queens
- [ ] CSES Creating Strings
- [ ] CSES Apple Division

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Forgetting to undo changes before returning.
- Stack depth for deep recursion.

## Definition of done

- [ ] You can write a permutation generator and N-Queens from memory.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
