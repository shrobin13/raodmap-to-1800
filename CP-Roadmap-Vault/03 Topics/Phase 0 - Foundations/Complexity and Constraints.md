---
tags: [topic, phase-0, core]
phase: 0
rating: "800"
est_days: 2
priority: core
status: todo
cf_tag: "all tags"
---

# Complexity and Constraints

> Reading the constraints first tells you which algorithm class the problem expects, saving hours of wrong approaches.

| | |
|---|---|
| Phase | [[Phase 0 - Foundations]] |
| Typical rating range | 800 |
| Estimated time | 2 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-11 November]] |
| Toph category | Easy Problems (72) |
| Codeforces tag | all tags |

**Prerequisites:** [[C++ Setup and Fast IO]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- Roughly 1e8 simple operations per second in C++, so a 1-2 second limit allows about 1e8-5e8 simple steps.
- Cheat sheet: n <= 10 -> O(n!) ; n <= 20 -> O(2^n * n) ; n <= 40 -> meet in the middle ; n <= 500 -> O(n^3) ; n <= 5000 -> O(n^2) ; n <= 2e5 -> O(n log n) ; n <= 1e6 -> O(n) ; n up to 1e18 -> O(log n) or math.
- Memory: 256 MB is common; an `int` array of 1e7 is 40 MB.
- Amortized analysis: two pointers and monotonic stacks are O(n) even with nested loops.
- Before coding, write the expected complexity next to your idea; if it does not fit, throw the idea away.

## Resources

- [Competitive Programmer's Handbook, chapter 2 (Time complexity)](https://cses.fi/book/book.pdf)

## Practice plan

- [ ] For the next 20 problems you solve, write `constraints -> intended complexity` in your Problem Log.

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Counting only the outer loop and ignoring an inner `O(n)` operation such as `vector::erase` or string concatenation in a loop.

## Definition of done

- [ ] Given any constraint line, you can name two candidate complexities in 10 seconds.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
