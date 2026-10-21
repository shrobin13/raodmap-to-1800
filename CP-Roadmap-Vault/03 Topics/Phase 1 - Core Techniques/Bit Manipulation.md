---
tags: [topic, phase-1, core]
phase: 1
rating: "1000-1600"
est_days: 5
priority: core
status: todo
cf_tag: "bitmasks"
---

# Bit Manipulation

> Bits give compact subset representation and powerful XOR tricks.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 1000-1600 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-02 February]] |
| Toph category | Dynamic Programming > Bitmask DP (prereq) |
| Codeforces tag | bitmasks |

**Prerequisites:** [[Basic Math, Parity and Divisibility]]

**Unlocks:** [[Bitmask DP]], [[Game Theory (Nim and Grundy)]], [[Inclusion-Exclusion]]

## What to learn

- `&`, `|`, `^`, `~`, `<<`, `>>`; test, set, clear, toggle a bit.
- `x & -x` lowest set bit, `__builtin_popcountll(x)`, `__builtin_ctzll(x)`, `__lg(x)`.
- XOR properties: `a ^ a = 0`, XOR of 0..n pattern.
- Enumerate subsets and submasks: `for (int s = m; s; s = (s - 1) & m)`.
- Bitwise problems: handle each bit independently.

## Resources

- [cp-algorithms: Bit manipulation](https://cp-algorithms.com/algebra/bit-manipulation.html)
- [Codeforces problemset (bitmasks)](https://codeforces.com/problemset?tags=bitmasks)

## Practice plan

- [ ] CSES Apple Division
- [ ] CSES Gray Code
- [ ] CSES Hamming Distance
- [ ] CF bitmasks 1000-1400: solve 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Using `1 << k` instead of `1LL << k` for k >= 31.
- Operator precedence of `&` vs `==`.

## Definition of done

- [ ] You can enumerate submasks and explain its 3^n total cost.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
