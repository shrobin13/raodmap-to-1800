---
tags: [topic, phase-4, core]
phase: 4
rating: "1400-2200"
est_days: 2
priority: core
status: todo
cf_tag: "interactive"
---

# Interactive Problems

> Interactive problems appear in most rounds; flush and query limits are the traps.

| | |
|---|---|
| Phase | [[Phase 4 - Advanced to 1800]] |
| Typical rating range | 1400-2200 |
| Estimated time | 2 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-11 November]] |
| Toph category | Interactive (11) |
| Codeforces tag | interactive |

**Prerequisites:** [[Binary Search and Search on the Answer]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- **Always flush** after every output line: use `cout << endl` (slower) or `cout << '\n' << flush`. Never `ios::sync_with_stdio(false)` without adding `cout.flush()` after each query.
- Binary search with limited queries: think about how many bits you need (e.g. 30 queries → up to 2^30).
- Never output extra newlines or debug prints during submission.
- Read the judge's response before printing the next query.
- Pattern: `print query -> flush -> read response -> decide next query`.

## Template

```cpp
// Interactive template
#include <bits/stdc++.h>
using namespace std;

int query(int x) {
    cout << "? " << x << '\n';
    cout.flush();      // NEVER FORGET THIS
    int response;
    cin >> response;
    return response;
}

void answer(int x) {
    cout << "! " << x << '\n';
    cout.flush();
}

void solve() {
    int lo = 1, hi = 1e9;
    while (lo < hi) {
        int mid = lo + (hi - lo) / 2;
        if (query(mid) == 1) hi = mid;   // adapt condition to problem
        else lo = mid + 1;
    }
    answer(lo);
}

int main() {
    int t; cin >> t;
    while (t--) solve();
}
```

## Resources

- [Toph Interactive category](https://toph.co/problems/interactive)
- [Codeforces: interactive problems tag](https://codeforces.com/problemset?tags=interactive)

## Practice plan

- [ ] Toph Interactive: 3 easiest
- [ ] CF interactive 1200-1600: solve 8
- [ ] CF 862B: Mahmoud and Ehab and the bipartiteness (interactive, classic)
- [ ] Practice writing and testing with local stdin/stdout swaps

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Forgetting flush; exceeding query limit.

## Definition of done

- [ ] You can solve a guess-the-number problem with a binary search.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
