---
tags: [topic, phase-2, core]
phase: 2
rating: "1200-1700"
est_days: 4
priority: core
status: todo
cf_tag: "math, number theory"
---

# Modular Arithmetic

> Counting problems ask for answers modulo 1e9+7 or 998244353, so mod arithmetic must be reflexive.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1200-1700 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-03 March]] |
| Toph category | Mathematics > Number Theory, Combinatorics |
| Codeforces tag | math, number theory |

**Prerequisites:** [[Number Theory Basics]]

**Unlocks:** [[Binary Exponentiation]], [[Combinatorics (nCr mod p)]], [[String Hashing]], [[FFT and NTT]]

## What to learn

- `(a + b) % m`, `(a - b + m) % m`, `(a * b) % m` with `long long`.
- Modular inverse by Fermat's little theorem (prime mod) or extended Euclid.
- Division: `a / b = a * inv(b) mod p`.
- Precompute factorials and inverse factorials.

## Resources

- [cp-algorithms: Modular multiplicative inverse](https://cp-algorithms.com/algebra/module-inverse.html)

## Practice plan

- [ ] CF 1200-1600 problems with `mod 1e9+7` outputs: solve 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Negative remainders after subtraction.
- Multiplying two numbers near 1e9+7 in `int`.

## Definition of done

- [ ] You never write a mod bug in a counting problem.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
