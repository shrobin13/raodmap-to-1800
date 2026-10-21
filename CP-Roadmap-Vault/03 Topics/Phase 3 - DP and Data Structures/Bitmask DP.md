---
tags: [topic, phase-3, core]
phase: 3
rating: "1600-2000"
est_days: 6
priority: core
status: todo
cf_tag: "dp, bitmasks"
---

# Bitmask DP

> When n <= 20, a bitmask encodes 'which items are used' and unlocks TSP-style DP.

| | |
|---|---|
| Phase | [[Phase 3 - DP and Data Structures]] |
| Typical rating range | 1600-2000 |
| Estimated time | 6 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-07 July]] |
| Toph category | Dynamic Programming > Bitmask DP (29) |
| Codeforces tag | dp, bitmasks |

**Prerequisites:** [[DP Foundations]], [[Bit Manipulation]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- `dp[mask][last]` for Hamiltonian-path style problems.
- Subset DP and assignment problems.
- SOS DP (sum over subsets) as an extension.
- Complexity O(2^n * n) or O(3^n) for submask enumeration.

## Template

```cpp
// shortest Hamiltonian path starting at 0 (dist matrix d)
vector<vector<ll>> dp(1 << n, vector<ll>(n, INF));
dp[1][0] = 0;
for (int mask = 1; mask < (1 << n); mask++)
    for (int last = 0; last < n; last++) if (mask >> last & 1)
        for (int nx = 0; nx < n; nx++) if (!(mask >> nx & 1))
            dp[mask | 1 << nx][nx] = min(dp[mask | 1 << nx][nx], dp[mask][last] + d[last][nx]);
```

## Resources

- [AtCoder DP: O (Matching)](https://atcoder.jp/contests/dp)
- [Toph Bitmask DP category](https://toph.co/problems/bitmask-dp)

## Practice plan

- [ ] CSES Elevator Rides
- [ ] CSES Hamiltonian Flights
- [ ] AtCoder DP O
- [ ] Toph Bitmask DP: 10 easiest

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Memory 2^20 * 20 * 8 bytes is too much with `long long`; use `int` where possible.

## Definition of done

- [ ] You can write TSP DP and explain its complexity.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
