---
tags: [topic, phase-4, core]
phase: 4
rating: "1500-2100"
est_days: 5
priority: core
status: todo
cf_tag: "strings"
---

# KMP, Prefix Function and Z-Function

> Linear-time string matching and border/period problems.

| | |
|---|---|
| Phase | [[Phase 4 - Advanced to 1800]] |
| Typical rating range | 1500-2100 |
| Estimated time | 5 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-09 September]] |
| Toph category | String > Pattern Matching (5) |
| Codeforces tag | strings |

**Prerequisites:** [[String Basics]]

**Unlocks:** [[Suffix Array and Automaton]]

## What to learn

- Prefix function (failure function).
- Z-function.
- Borders, periods, count occurrences.

## Template

```cpp
vector<int> prefix_function(const string &s) {
    int n = s.size();
    vector<int> pi(n, 0);
    for (int i = 1; i < n; i++) {
        int j = pi[i - 1];
        while (j > 0 && s[i] != s[j]) j = pi[j - 1];
        if (s[i] == s[j]) j++;
        pi[i] = j;
    }
    return pi;
}
```

## Resources

- [cp-algorithms: Prefix function](https://cp-algorithms.com/string/prefix-function.html)
- [cp-algorithms: Z-function](https://cp-algorithms.com/string/z-function.html)

## Practice plan

- [ ] CSES String Matching
- [ ] CSES Finding Borders
- [ ] CSES Finding Periods

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Off-by-one when concatenating pattern + separator + text.

## Definition of done

- [ ] You can implement prefix function in 2 minutes.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
