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

## Template

```cpp
const ll MOD = 1e9 + 7;   // or 998244353

ll add(ll a, ll b) { return (a + b) % MOD; }
ll sub(ll a, ll b) { return (a - b % MOD + MOD) % MOD; }
ll mul(ll a, ll b) { return a % MOD * (b % MOD) % MOD; }
ll pw(ll a, ll b) { ll r = 1; for (a %= MOD; b; b >>= 1, a = mul(a, a)) if (b & 1) r = mul(r, a); return r; }
ll inv(ll a) { return pw(a, MOD - 2); }  // only when MOD is prime

// Precomputed factorials (up to MAXN)
const int MAXN = 2e5 + 5;
ll fact[MAXN], inv_fact[MAXN];
void precompute() {
    fact[0] = 1;
    for (int i = 1; i < MAXN; i++) fact[i] = mul(fact[i-1], i);
    inv_fact[MAXN-1] = inv(fact[MAXN-1]);
    for (int i = MAXN-2; i >= 0; i--) inv_fact[i] = mul(inv_fact[i+1], i+1);
}
ll C(int n, int k) {   // nCk mod MOD, 0 <= k <= n
    if (k < 0 || k > n) return 0;
    return mul(fact[n], mul(inv_fact[k], inv_fact[n-k]));
}
```

## Resources

- [cp-algorithms: Modular multiplicative inverse](https://cp-algorithms.com/algebra/module-inverse.html)
- [cp-algorithms: Extended Euclidean algorithm](https://cp-algorithms.com/algebra/extended-euclid-algorithm.html)

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
