---
tags: [strategy]
---

# Contest Playbook

A structured playbook for Codeforces, AtCoder, and local contests. Follow these protocols methodically before, during, and after every round.

---

## 1. Before the Contest (T - 30 to 0 min)

- **Physical state:** Hydrate, take a 5-minute walk, ensure a quiet room. Avoid heavy meals right before contest time.
- **Environment setup:**
  - Open terminal with your pre-tested C++ template ready.
  - Compile a hello-world or test solution with debug flags (`-fsanitize=address,undefined -Wall`).
  - Keep scratch paper and a pen ready (thinking on paper prevents 80% of blind coding mistakes).
- **Format awareness:**
  - **Div 3 / Div 4:** Speed & clean implementation matter most. Solve A through D fast without WA penalties.
  - **Div 2:** Focus on accuracy and patience. Problems C & D determine rating jumps up to 1800.
  - **Educational Rounds:** Usually standard math, DP, or data structures with 2-hour duration.

---

## 2. During the Contest: Operational Routine

### Problem Selection & Reading
1. **Never code immediately.** Read the problem statement twice.
2. **Translate to math/abstractions:** Write down the given inputs, operations allowed, and what is asked in 1-2 bullet points on paper.
3. **Verify bounds:** Look at $N$ and time limit first ([[Complexity and Constraints]]). $N \le 2000 \implies O(N^2)$; $N \le 2 \cdot 10^5 \implies O(N \log N)$ or $O(N)$.
4. **Work through sample cases on paper:** Compute the sample output by hand. If your manual trace doesn't match the sample, you misunderstood the statement.

### Time Budget & Stuck Protocol (The 20-Minute Rule)
- **Problem A:** $\le 10$ minutes.
- **Problem B:** $\le 20$ minutes.
- **Problem C:** $\le 35$ minutes.
- **Problem D:** $\le 50$ minutes.

> [!WARNING]
> **If stuck on any problem for > 20 minutes without progress:**
> 1. **Step away from the screen for 60 seconds.** Breathe and drink water.
> 2. **Check the scoreboard:** Are hundreds of people solving the next problem instead? If yes, immediately read the next problem.
> 3. **Change perspective:**
>    - Is the answer monotonic? Can we binary search on the answer?
>    - Can we rephrase it as a graph or greedy choice?
>    - What happens if we sort the input first?
>    - What happens for tiny $N$ ($1, 2, 3$)? Look for invariants or parity.

### Pre-Submission Checklist (Run this every single time)
Before clicking Submit:
- [ ] **Data types:** Does any product or sum exceed $2 \cdot 10^9$? Use `long long` for accumulators, answers, and loop bounds.
- [ ] **Array bounds:** Did you size arrays to $N + 5$ or $2 \cdot 10^5 + 5$ (avoid exact $N$ or $1$-indexing off-by-one)?
- [ ] **Multiple test cases:** Are **all** global variables, adjacency lists, and vectors cleared per testcase?
- [ ] **Corner cases:** Have you checked $N = 1$, $N = 2$, all elements equal, all zeros, empty string, maximum possible $N$?
- [ ] **Interactive problems:** Did you include `cout << endl` or `cout << '\n' << flush`?

### Handling In-Contest Verdicts
- **Wrong Answer (WA):**
  - Do NOT make random edits and resubmit blindly.
  - Check whether you printed `YES`/`NO` with correct casing.
  - Re-read constraints: can negative numbers appear? Can $k = 0$?
  - Test the smallest edge case on paper.
- **Time Limit Exceeded (TLE):**
  - Check if fast I/O is present (`cin.tie(NULL)`).
  - Use `'\n'` instead of `endl` in non-interactive problems.
  - Check for infinite loops (e.g. `while(l < r)` without incrementing or decreasing pointers).
- **Runtime Error (RE):**
  - Array index out of bounds (check negative indices or $> MAXN$).
  - Division or modulo by zero.
  - Recursion stack overflow on chain trees.

---

## 3. After the Contest: Upsolving & Logging

1. **Log Contest in [[Contest Log]]:** Record your rating, solved problems, and rank using [[Contest Review Template]].
2. **The 1-Problem Rule:** Within 24-48 hours, upsolve **at least one** problem that you couldn't solve in-contest ([[Upsolving Guide]]).
3. **Capture Traps:** If a bug cost you rating, log it into [[Mistake Log]] with the exact test case that failed you.

---

See also: [[Practice Method]], [[Stress Testing]], [[Mock Contest Guide]], [[00 Home]]
