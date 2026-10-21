---
tags: [topic, phase-1, core]
phase: 1
rating: "800-1300"
est_days: 4
priority: core
status: todo
cf_tag: "strings"
---

# String Basics

> Strings are the most common data type in A/B problems; solid basics avoid silly losses.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 800-1300 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-12 December]] |
| Toph category | String, Implementation |
| Codeforces tag | strings |

**Prerequisites:** [[Implementation]], [[STL Essentials]]

**Unlocks:** [[String Hashing]], [[KMP, Prefix Function and Z-Function]], [[Trie (Prefix Tree)]]

## What to learn

- Frequency arrays of 26 letters, substring vs subsequence, palindromes.
- Building strings efficiently with `+=`, not `s = s + c` in loops.
- Lexicographic comparison; sorting strings; counting distinct characters.
- Simple parsing: split by spaces, digits, parentheses.

## Resources

- [Codeforces problemset (strings)](https://codeforces.com/problemset?tags=strings)
- [Toph String category](https://toph.co/problems/string)

## Practice plan

- [ ] CSES Repetitions
- [ ] CSES Palindrome Reorder
- [ ] CSES Creating Strings
- [ ] CF strings 800-1200: solve 25

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Mixing `char` arithmetic with `int` (use `c - 'a'`).
- Using `substr` in a loop (O(n) each).

## Definition of done

- [ ] You can solve a 1200 string problem without library lookups.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
