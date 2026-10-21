---
tags: [topic, phase-0, core]
phase: 0
rating: "800"
est_days: 4
priority: core
status: todo
cf_tag: "implementation, data structures"
---

# STL Essentials

> The STL replaces hundreds of lines of hand-written code; knowing it well is a free speed-up.

| | |
|---|---|
| Phase | [[Phase 0 - Foundations]] |
| Typical rating range | 800 |
| Estimated time | 4 days |
| Priority for 1800 | Core |
| Scheduled in | [[2026-11 November]] |
| Toph category | Easy Problems (72), Linear Data Structure (9) |
| Codeforces tag | implementation, data structures |

**Prerequisites:** [[C++ Setup and Fast IO]]

**Unlocks:** [[Implementation]], [[Sorting and Custom Comparators]], [[String Basics]], [[Stack, Queue, Deque and Priority Queue]], [[Graph Basics and Representation]]

## What to learn

- `vector`, `string`, `array`, `pair`, `tuple`, structured bindings (`auto [a, b] = p;`).
- `set`, `multiset`, `map`, `unordered_map` (beware anti-hash tests on Codeforces; prefer `map` or a custom hash).
- `stack`, `queue`, `deque`, `priority_queue` (max-heap by default, `greater<>` for min-heap).
- Algorithms: `sort`, `reverse`, `unique`, `lower_bound`, `upper_bound`, `min_element`, `max_element`, `accumulate`, `iota`, `next_permutation`, `count`, `fill`.
- Lambdas for comparators: `sort(v.begin(), v.end(), [](auto &a, auto &b){ return a.second < b.second; });`
- Iterators: `end()` is one past the last element; `set::erase(value)` on a multiset erases all copies, `erase(iterator)` erases one.

## Resources

- [cppreference algorithms library](https://en.cppreference.com/w/cpp/algorithm)
- [CSES Problem Set](https://cses.fi/problemset/)
- [Competitive Programmer's Handbook, chapter 4 (Data structures)](https://cses.fi/book/book.pdf)

## Practice plan

- [ ] CSES Distinct Numbers
- [ ] CSES Apartments
- [ ] CSES Ferris Wheel
- [ ] CSES Concert Tickets (multiset)
- [ ] CSES Restaurant Customers
- [ ] CF problemset: tag `implementation`, rating 800-900, solve 15 using STL containers

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Erasing from a container while iterating over it.
- `unordered_map` hacked into O(n) operations.
- Using `v.size() - 1` when `v` is empty (unsigned underflow).

## Definition of done

- [ ] You can write a custom comparator from memory.
- [ ] You know which container gives O(log n) k-th/lower_bound behavior and which does not.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
