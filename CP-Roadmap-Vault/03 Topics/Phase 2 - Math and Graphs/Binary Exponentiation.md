---
tags: [topic, phase-2, core]
phase: 2
rating: "1200-1600"
est_days: 2
priority: core
status: todo
cf_tag: "math, number theory"
---

# Binary Exponentiation

> Fast power is the building block for modular inverses and matrix exponentiation.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1200-1600 |
| Estimated time | 2 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-03 March]] |
| Toph category | Mathematics > Number Theory |
| Codeforces tag | math, number theory |

**Prerequisites:** [[Modular Arithmetic]]

**Unlocks:** [[Combinatorics (nCr mod p)]], [[Sparse Table]], [[Matrix Exponentiation]], [[FFT and NTT]]

## What to learn

- Compute `a^b mod m` in O(log b).
- Use it to get inverses when m is prime.
- Generalizes to matrices ([[Matrix Exponentiation]]).

## Template

```cpp
ll power(ll b, ll e, ll m) {
    ll r = 1; b %= m;
    while (e) { if (e & 1) r = r * b % m; b = b * b % m; e >>= 1; }
    return r;
}
ll inv(ll a, ll p) { return power(a, p - 2, p); }   // p prime
```

## Resources

- [cp-algorithms: Binary exponentiation](https://cp-algorithms.com/algebra/binary-exp.html)

## Practice plan

- [ ] CSES Exponentiation
- [ ] CSES Exponentiation II

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Not reducing `b` modulo m on entry.
- Overflow when `m` is near 1e18 (use `__int128`).

## Definition of done

- [ ] You can write modpow in under 1 minute.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
