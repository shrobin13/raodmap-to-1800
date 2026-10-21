---
tags: [topic, phase-2, core]
phase: 2
rating: "1300-1800"
est_days: 7
priority: core
status: todo
cf_tag: "combinatorics, math"
---

# Combinatorics (nCr mod p)

> Counting arrangements and paths shows up in every contest tier from Div 2 C up.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1300-1800 |
| Estimated time | 7 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-04 April]] |
| Toph category | Mathematics > Combinatorics (64) |
| Codeforces tag | combinatorics, math |

**Prerequisites:** [[Binary Exponentiation]], [[Modular Arithmetic]]

**Unlocks:** [[Probability and Expected Value]], [[Inclusion-Exclusion]]

## What to learn

- Addition and multiplication principles; permutations and combinations.
- Precompute `fact[]` and `inv_fact[]` to get nCr mod p in O(1).
- Stars and bars, Catalan numbers, Pascal's identity.
- Counting paths in grids with binomials.
- Link to [[Inclusion-Exclusion]] for complement counting.

## Template

```cpp
const ll MOD = 1e9 + 7;
vector<ll> fact(N + 1), ifact(N + 1);
fact[0] = 1;
for (int i = 1; i <= N; i++) fact[i] = fact[i - 1] * i % MOD;
ifact[N] = power(fact[N], MOD - 2, MOD);
for (int i = N; i > 0; i--) ifact[i - 1] = ifact[i] * i % MOD;
auto C = [&](int n, int k) -> ll {
    if (k < 0 || k > n) return 0;
    return fact[n] * ifact[k] % MOD * ifact[n - k] % MOD;
};
```

## Resources

- [cp-algorithms: Binomial coefficients](https://cp-algorithms.com/combinatorics/binomial-coefficients.html)
- [Toph Combinatorics category](https://toph.co/problems/combinatorics)
- [CSES Mathematics section](https://cses.fi/problemset/)

## Practice plan

- [ ] CSES Binomial Coefficients
- [ ] CSES Distributing Apples
- [ ] CSES Bracket Sequences I
- [ ] CF combinatorics 1300-1700: solve 20

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Computing factorials above the mod range.
- Using nCr with n >= p (needs Lucas).

## Definition of done

- [ ] You can derive counting formulas and verify them with brute force for small n.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
