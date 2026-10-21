---
tags: [topic, phase-3, core]
phase: 3
rating: "1400-1900"
est_days: 7
priority: core
status: todo
cf_tag: "dp"
---

# DP on Grids and Sequences

> Grid paths, LIS, LCS, edit distance and Kadane cover most 2D/sequence DP.

| | |
|---|---|
| Phase | [[Phase 3 - DP and Data Structures]] |
| Typical rating range | 1400-1900 |
| Estimated time | 7 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-07 July]] |
| Toph category | Dynamic Programming |
| Codeforces tag | dp |

**Prerequisites:** [[DP Foundations]]

**Unlocks:** [[Interval DP]]

## What to learn

- Grid path counting and min-cost paths.
- LIS in O(n log n) with `lower_bound`.
- LCS and edit distance in O(nm).
- Maximum subarray (Kadane).

## Template

```cpp
// strictly increasing LIS length
vector<int> tail;
for (int x : a) {
    auto it = lower_bound(tail.begin(), tail.end(), x);
    if (it == tail.end()) tail.push_back(x); else *it = x;
}
int lis = tail.size();
```

## Resources

- [AtCoder DP: F (LCS), L, M](https://atcoder.jp/contests/dp)
- [CSES Dynamic Programming section](https://cses.fi/problemset/)

## Practice plan

- [ ] CSES Grid Paths
- [ ] CSES Edit Distance
- [ ] CSES Increasing Subsequence
- [ ] CSES Maximum Subarray Sum
- [ ] AtCoder DP F
- [ ] CF dp 1400-1700: 20

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Confusing subsequence with substring.
- LIS: `lower_bound` vs `upper_bound` for non-strict increase.

## Definition of done

- [ ] You can write LIS and LCS from memory.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
