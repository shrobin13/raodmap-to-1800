---
tags: [topic, phase-2, core]
phase: 2
rating: "1200-1700"
est_days: 4
priority: core
status: todo
cf_tag: "number theory"
---

# Sieve and Factorization

> A sieve lets you answer many primality, factorization and divisor-count questions in near O(1).

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1200-1700 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-03 March]] |
| Toph category | Mathematics > Number Theory |
| Codeforces tag | number theory |

**Prerequisites:** [[Number Theory Basics]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- Sieve of Eratosthenes up to 1e7.
- Smallest-prime-factor sieve for O(log n) factorization.
- Count divisors / sum of divisors using a harmonic-sum sieve.
- Prefix counts of primes for range queries.
- Segmented sieve for ranges up to 1e12 (advanced, optional).

## Template

```cpp
const int N = 1000000;
vector<int> spf(N + 1);
for (int i = 2; i <= N; i++) if (!spf[i])
    for (int j = i; j <= N; j += i) if (!spf[j]) spf[j] = i;
// factorize x
vector<int> primes;
for (int x = n; x > 1; x /= spf[x]) primes.push_back(spf[x]);
```

## Resources

- [cp-algorithms: Sieve of Eratosthenes](https://cp-algorithms.com/algebra/sieve-of-eratosthenes.html)
- [Toph tag: Sieve](https://toph.co/problems/tags/sieve)

## Practice plan

- [ ] CF number theory 1200-1600 involving sieve: solve 15
- [ ] Toph tag Sieve problems

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Sieve size off by one.
- Using `vector<bool>` with iteration order that causes cache misses (rare).

## Definition of done

- [ ] You can write both a prime sieve and an SPF sieve from memory.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
