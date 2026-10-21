---
tags: [topic, phase-2, core]
phase: 2
rating: "1100-1700"
est_days: 7
priority: core
status: todo
cf_tag: "number theory, math"
---

# Number Theory Basics

> GCD, divisors and primes appear in a large fraction of 1200-1800 problems.

| | |
|---|---|
| Phase | [[Phase 2 - Math and Graphs]] |
| Typical rating range | 1100-1700 |
| Estimated time | 7 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-03 March]] |
| Toph category | Mathematics > Number Theory (131) |
| Codeforces tag | number theory, math |

**Prerequisites:** [[Basic Math, Parity and Divisibility]]

**Unlocks:** [[Sieve and Factorization]], [[Modular Arithmetic]]

## What to learn

- Euclid's algorithm, `std::gcd`, `lcm = a / gcd * b`.
- Divisors in O(sqrt n); primality test in O(sqrt n); trial-division factorization.
- Extended Euclid and Bezout identity (for modular inverse).
- Euler's totient function (intro).
- Useful facts: number of divisors of n <= 1e9 is at most 1344.

## Template

```cpp
ll gcd_(ll a, ll b) { return b ? gcd_(b, a % b) : a; }
bool is_prime(ll n) {
    if (n < 2) return false;
    for (ll i = 2; i * i <= n; i++) if (n % i == 0) return false;
    return true;
}
```

## Resources

- [cp-algorithms: Euclidean algorithm](https://cp-algorithms.com/algebra/euclid-algorithm.html)
- [cp-algorithms: Integer factorization](https://cp-algorithms.com/algebra/factorization.html)
- [cp-algorithms: Euler's totient function](https://cp-algorithms.com/algebra/phi-function.html)
- [Toph Number Theory category](https://toph.co/problems/number-theory)

## Practice plan

- [ ] CSES Common Divisors
- [ ] CSES Counting Divisors
- [ ] CF number theory 1100-1500: solve 25
- [ ] Toph Number Theory: 20 easiest

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Overflow in `a * b` before dividing by gcd.
- Looping to n instead of sqrt(n).

## Definition of done

- [ ] You can factorize a number up to 1e12 in your head-code (trial division to 1e6).
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
