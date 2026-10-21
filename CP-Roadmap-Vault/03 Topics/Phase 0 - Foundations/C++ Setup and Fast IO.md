---
tags: [topic, phase-0, core]
phase: 0
rating: "800"
est_days: 3
priority: core
status: todo
cf_tag: "implementation"
---

# C++ Setup and Fast IO

> Every later topic assumes you can read input fast and write code without fighting the language.

| | |
|---|---|
| Phase | [[Phase 0 - Foundations]] |
| Typical rating range | 800 |
| Estimated time | 3 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-11 November]] |
| Toph category | Easy Problems (72) |
| Codeforces tag | implementation |

**Prerequisites:** None

**Unlocks:** [[STL Essentials]], [[Complexity and Constraints]], [[Implementation]]

## What to learn

- Install g++ (C++17 or newer) and an editor (VS Code with the cph extension, or CLion). Compile with `g++ -std=c++17 -O2 -Wall -Wextra`.
- Build your personal template: `bits/stdc++.h`, fast IO (`ios::sync_with_stdio(false); cin.tie(nullptr);`), `using ll = long long;`.
- Know when `int` overflows (about 2.1e9) and when to use `long long` (about 9.2e18).
- Multiple test case pattern: read `t`, loop, reset all globals/vectors per test.
- Integer division truncates toward zero and `%` can be negative for negative operands.
- Learn debug builds: `-fsanitize=address,undefined -D_GLIBCXX_DEBUG` catches out-of-bounds and overflow bugs early.

## Template

```cpp
#include <bits/stdc++.h>
using namespace std;
using ll = long long;

void solve() {
    int n;
    cin >> n;
    vector<ll> a(n);
    for (auto &x : a) cin >> x;
    // ...
    cout << accumulate(a.begin(), a.end(), 0LL) << '\n';
}

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int t = 1;
    cin >> t;           // remove if single test
    while (t--) solve();
    return 0;
}
```

## Resources

- [cppreference (C++ language and library reference)](https://en.cppreference.com/)
- [Toph tutorials](https://blog.toph.co/tutorials)
- [Codeforces problemset](https://codeforces.com/problemset)
- [Competitive Programmer's Handbook (free PDF), chapters 1-2](https://cses.fi/book/book.pdf)

## Practice plan

- [ ] CF 4A Watermelon
- [ ] CF 71A Way Too Long Words
- [ ] CF 231A Team
- [ ] CF 158A Next Round
- [ ] CF 282A Bit++
- [ ] CF 112A Petya and Strings
- [ ] CF 50A Domino piling
- [ ] CF 263A Beautiful Matrix
- [ ] CF 339A Helpful Maths
- [ ] Toph: 20 problems from Easy Problems, sorted by least difficult

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Forgetting `long long` for sums and products.
- Using `endl` for heavy output (it flushes every time; use `'\n'`).
- Not resetting arrays or vectors between test cases.

## Definition of done

- [ ] You solve all nine CF 800-rated problems above without looking anything up.
- [ ] Your template compiles with no warnings.
- [ ] You can explain why `int` overflows on `1e5 * 1e5`.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
