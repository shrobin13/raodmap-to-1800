---
tags: [topic, phase-4, core]
phase: 4
rating: "1700-2200"
est_days: 5
priority: core
status: todo
cf_tag: "probabilities, math"
---

# Probability and Expected Value

> Expected-value problems rely on linearity of expectation and modular fractions.

| | |
|---|---|
| Phase | [[Phase 4 - Advanced to 1800]] |
| Typical rating range | 1700-2200 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-11 November]] |
| Toph category | Mathematics > Probability & Statistics (21) |
| Codeforces tag | probabilities, math |

**Prerequisites:** [[Combinatorics (nCr mod p)]], [[DP Foundations]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- **Linearity of expectation:** E[X + Y] = E[X] + E[Y] always (even when X, Y are dependent). Use it to decompose over elements, pairs, or events.
- **Expected value DP:** define `dp[state] = expected cost/steps to reach goal`. Build recurrences and solve (may require Gaussian elimination for cycles).
- **Fractions mod p:** any probability `a/b` becomes `a * inv(b) mod p`. Precompute inverses.
- **Indicator variables:** P(event) = E[1_{event}]; sum indicators to count expected hits.
- Geometric distribution: expected number of trials until success = 1/p.
- Know how to handle problems where you need to solve a linear system for expected values (e.g. expected steps on a random walk).

## Template

```cpp
// Modular inverse (Fermat, prime mod)
const ll MOD = 1e9 + 7;
ll pw(ll a, ll b, ll m = MOD) { ll r = 1; for (a %= m; b; b >>= 1, a = a*a%m) if (b&1) r = r*a%m; return r; }
ll inv(ll a) { return pw(a, MOD - 2); }

// Example: E[X] = sum over i of P(i hits) * value(i)
// P(i) as fraction a/b  ->  (a % MOD) * inv(b) % MOD
```

## Resources

- [cp-algorithms: Probability theory](https://cp-algorithms.com/combinatorics/probability.html)
- [Toph Probability & Statistics category](https://toph.co/problems/probability-statistics)
- [USACO Guide: Expected Value](https://usaco.guide/)

## Practice plan

- [ ] CSES Dice Probability
- [ ] CSES Two Dice
- [ ] CSES Throwing Dice
- [ ] CSES CSES graph problems requiring expected steps (Sightseeing Cities)
- [ ] Toph Probability: 5 easiest
- [ ] CF probabilities 1700-2100: solve 12
- [ ] AtCoder DP Contest problem J (Sushi) — classic linearity of expectation

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Adding probabilities of non-disjoint events.

## Definition of done

- [ ] You can compute an expected value mod p.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
