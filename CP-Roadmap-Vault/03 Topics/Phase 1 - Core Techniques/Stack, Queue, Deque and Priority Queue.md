---
tags: [topic, phase-1, core]
phase: 1
rating: "1000-1700"
est_days: 6
priority: core
status: todo
cf_tag: "data structures, greedy"
---

# Stack, Queue, Deque and Priority Queue

> Monotonic stacks, deques and heaps give O(n) or O(n log n) solutions to many 'nearest' and 'window' problems.

| | |
|---|---|
| Phase | [[Phase 1 - Core Techniques]] |
| Typical rating range | 1000-1700 |
| Estimated time | 6 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-01 January]] |
| Toph category | Data Structure > Linear Data Structure (9) |
| Codeforces tag | data structures, greedy |

**Prerequisites:** [[STL Essentials]]

**Unlocks:** [[Breadth-First Search]], [[Dijkstra's Shortest Path]]

## What to learn

- Bracket matching with a stack.
- Monotonic stack: next greater/smaller element.
- Sliding window maximum with a deque.
- Priority queue: top-k, scheduling, Dijkstra later.
- Queue simulation and Josephus-style problems.

## Template

```cpp
// next smaller element index (or -1)
vector<int> nxt(n, -1);
stack<int> st;
for (int i = 0; i < n; i++) {
    while (!st.empty() && a[st.top()] > a[i]) { nxt[st.top()] = i; st.pop(); }
    st.push(i);
}
```

## Resources

- [USACO Guide (modules: Stacks, Queues)](https://usaco.guide/)
- [Toph Linear Data Structure category](https://toph.co/problems/linear-data-structure)

## Practice plan

- [ ] CSES Nearest Smaller Values
- [ ] CSES Josephus Problem I
- [ ] Toph: Neat Brackets
- [ ] Toph: Matching Brackets
- [ ] Toph: StackLang
- [ ] CF 1200-1500 problems with tag `data structures`: 10

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Popping from an empty stack/queue.
- Using the wrong ordering for `priority_queue`.

## Definition of done

- [ ] You can write a monotonic stack for next-smaller in 2 minutes.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
