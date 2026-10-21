---
tags: [topic, phase-3, core]
phase: 3
rating: "1400-1900"
est_days: 5
priority: core
status: todo
cf_tag: "dp"
---

# Knapsack DP

> Knapsack is the template for choose/skip problems with a capacity.

| | |
|---|---|
| Phase | [[Phase 3 - DP and Data Structures]] |
| Typical rating range | 1400-1900 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-06 June]] |
| Toph category | Dynamic Programming > Knapsack DP (0) |
| Codeforces tag | dp |

**Prerequisites:** [[DP Foundations]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- 0/1 knapsack with 1D array and reverse loop.
- Unbounded knapsack with forward loop.
- Subset sum and counting variants.
- Binary splitting for bounded items (optional).

## Template

```cpp
// 0/1 knapsack: maximize value with capacity W
vector<ll> dp(W + 1, 0);
for (int i = 0; i < n; i++)
    for (int w = W; w >= wt[i]; w--)
        dp[w] = max(dp[w], dp[w - wt[i]] + val[i]);
```

## Resources

- [AtCoder Educational DP: D (Knapsack 1), E (Knapsack 2)](https://atcoder.jp/contests/dp)
- [CSES Dynamic Programming section](https://cses.fi/problemset/)

## Practice plan

- [ ] CSES Book Shop
- [ ] CSES Money Sums
- [ ] AtCoder DP D
- [ ] AtCoder DP E
- [ ] CF dp 1400-1700 (knapsack-like): 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Looping capacity forward in 0/1 knapsack (reuses items).
- Capacity dimension too large for memory.

## Definition of done

- [ ] You can tell 0/1 vs unbounded from the loop direction.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
