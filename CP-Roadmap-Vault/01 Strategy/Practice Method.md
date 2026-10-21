---
tags: [strategy]
---

# Practice Method

## The problem-solving loop

1. Read the statement twice. Rewrite it in your own words.
2. Check constraints and note the intended complexity ([[Complexity and Constraints]]).
3. Work through the sample by hand.
4. Write a brute force idea first.
5. Look for the property that speeds it up (sorting, monotonicity, math, graph model).
6. Prove or stress test the idea ([[Stress Testing]]).
7. Code carefully and test edge cases (n = 1, all equal, maximum values).
8. **Debug before giving up:** compile with `-fsanitize=address,undefined`, add `cerr` prints, test the smallest failing case by hand. Most WA is a code bug, not a wrong idea.

## Debugging toolkit

- Compile: `g++ -std=c++17 -O2 -Wall -Wextra -fsanitize=address,undefined -D_GLIBCXX_DEBUG`
- Print all variables in the failing test case with `cerr`.
- Shrink the failing input to the smallest possible case.
- Check: off-by-one, uninitialized variables, wrong answer for n=1 or n=2.

## The stuck rule

- 0-30 minutes: try on your own.
- 30-45 minutes: re-read the statement, try small cases, draw it.
- After 45 minutes: read a hint (the tags or the first line of the editorial).
- After another 20 minutes: read the editorial, close it, re-implement from scratch, then redo the problem again in 2-3 days.

## Difficulty ladder

Solve problems rated 100-200 above your current rating. If you solve more than 80% of them, move the ladder up by 100. If less than 40%, move it down.

## Sources

- Codeforces problemset filtered by tag and rating ([[Platforms Hub]]).
- CSES for structured topic sets.
- Toph categories ([[Toph Category Map]]).

Related: [[Upsolving Guide]], [[Daily Routine]]
