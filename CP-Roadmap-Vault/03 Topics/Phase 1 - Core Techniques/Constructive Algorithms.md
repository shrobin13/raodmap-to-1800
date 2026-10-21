---
tags: [topic, phase-1, core]
phase: 1
rating: "900-1700"
est_days: 10
priority: core
status: todo
cf_tag: "constructive algorithms"
---

# Constructive Algorithms

> Constructive problems make up a big share of Div 2 B/C; they reward pattern finding.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 900-1700 |
| Estimated time | 10 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-02 February]] |
| Toph category | Ad-hoc |
| Codeforces tag | constructive algorithms |

**Prerequisites:** [[Greedy Algorithms]], [[Basic Math, Parity and Divisibility]]

**Unlocks:** [[Game Theory and Minimax]], [[Phase 3 - DP and Data Structures]], Div 2 C/D Ad-hoc Reasoning

## What to learn

- **Brute-force small n:** Write a script or test manually on $n = 1, 2, 3, 4, 5$ to detect cyclic, parity, or recursive patterns.
- **Common structural archetypes:**
  - Alternating signs / colors: $(+1, -1, +1, -1)$ or chessboard coloring.
  - Pairing / complementary sums: Pair $i$ with $n - i + 1$.
  - Extreme values first: Place maximums and minimums at boundaries.
  - Powers of two / binary decomposition: Deconstruct constraints bit-by-bit.
  - Block partitioning: Solve for block size $k$ and replicate.
- **Invariants & monovariants:** Quantities that remain constant (parity, sum mod $k$) or monotonically change.
- **Impossibility criteria:** Always identify and handle the impossible case first (e.g., odd sum with all even operations).
- **Stress-test checker:** Always write a small local validation script to test your construction on hundreds of small inputs before submitting.

## Resources

- [Codeforces problemset (constructive algorithms)](https://codeforces.com/problemset?tags=constructive+algorithms)
- [CSES Introductory Problems](https://cses.fi/problemset/)
- [USACO Guide - Ad-Hoc / Constructive](https://usaco.guide/)

## Practice plan

- [ ] CSES Permutations
- [ ] CSES Gray Code
- [ ] CSES Tower of Hanoi
- [ ] CSES Grid Paths
- [ ] CF 1388B - Reverse Binary Strings (1100)
- [ ] CF 1472D - Even-Odd Game (1200)
- [ ] CF 1352E - Special Elements (1300)
- [ ] CF 1537C - Challenging Cliffs (1200)
- [ ] CF 1618D - Array and Operations (1300)
- [ ] CF 1515C - Phoenix and Towers (1400)
- [ ] CF 1627C - Not Assigning (1400)
- [ ] CF constructive 1200-1500: solve 20
- [ ] CF constructive 1500-1700: solve 15

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Proving only that your construction works for the samples.
- Missing the 'impossible' answer.

## Definition of done

- [ ] You can build and self-check a construction with a small checker program.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
