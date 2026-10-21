<![CDATA[<div align="center">

# 🏆 CP Roadmap — Obsidian Vault

### A structured, 14-month roadmap to reach **Codeforces 1800 (Expert)** from absolute beginner.

Built as an [Obsidian](https://obsidian.md/) knowledge vault with **108 interconnected notes**, a month-by-month calendar, curated problem lists, progress tracking, and everything you need to stay consistent.

[![Obsidian](https://img.shields.io/badge/Obsidian-vault-7C3AED?logo=obsidian&logoColor=white)](#getting-started)
[![Codeforces](https://img.shields.io/badge/Target-CF%201800-1890FF?logo=codeforces&logoColor=white)](#the-goal)
[![License](https://img.shields.io/badge/License-free%20to%20use-22C55E)](#license)

</div>

---

## 📌 Who Is This For?

- You're a **complete beginner** to competitive programming (or starting fresh with C++).
- You want a **clear, opinionated plan** — not a 200-tab browser session of scattered resources.
- You learn best by **doing problems**, not watching endless tutorials.
- You want to reach **Codeforces Expert (1800)** in roughly a year.

If any of that resonates, this vault was built for you.

---

## 🎯 The Goal

> **Codeforces rating 1800 by December 2027**, starting from zero in November 2026.

The plan spans **14 months** broken into **6 phases**, each with concrete rating targets, topic lists, practice problems, and exit criteria. It prioritizes solving and contests over passive reading — roughly **60% solving, 20% learning, 20% contests & upsolving**.

### Milestone Targets

| Date | Target Rating | Phase |
|:---|:---:|:---|
| Nov 2026 | ~800 | Phase 0 — Foundations |
| Feb 2027 | ~1150 | Phase 1 — Core Techniques |
| May 2027 | ~1350 | Phase 2 — Math & Graphs |
| Aug 2027 | ~1500 | Phase 3 — DP & Data Structures |
| Dec 2027 | **1800** | Phase 4 — Advanced to 1800 |

---

## 🗂️ What's Inside

```
CP-Roadmap-Vault/
├── 00 Home.md                  ← Start here. Links to everything.
├── 01 Strategy/                ← How to practice, compete, and stay consistent
├── 02 Phases/                  ← 6 phase outlines with checklists
├── 03 Topics/                  ← 61 detailed topic notes (the core of the vault)
├── 04 Calendar/                ← 14 month-by-month plans + overview
├── 05 Resources/               ← Platforms, books, videos, tools, Toph category map
├── 06 Templates/               ← Obsidian templates for logging
└── 07 Tracking/                ← Problem log, mistake log, contest log, dashboard
```

### `01 Strategy` — The Game Plan (8 notes)

Actionable guides that shape your daily workflow:

| Note | What It Covers |
|:---|:---|
| **Goal and Milestones** | Rating targets, timeline, and 5 core principles |
| **Daily Routine** | A sample 2-hour daily block + weekly rhythm |
| **Practice Method** | The problem-solving loop, the "stuck rule" (when to read hints), and the difficulty ladder |
| **Contest Playbook** | Before / during / after contest checklists |
| **Upsolving Guide** | How to learn from unsolved problems after every contest |
| **Stress Testing** | Ready-to-use `gen.cpp` + bash script to find bugs |
| **Burnout and Consistency** | Mental health tips, rest days, and community advice |
| **How to Use This Vault** | Setup instructions and priority labels explained |

### `02 Phases` — The Progression (6 phase hubs)

Each phase note lists its topics in suggested order, estimated days per topic, priority level (`core` / `optional` / `stretch`), and clear **exit criteria** so you know when to move on.

| Phase | Focus | Rating Range | Duration |
|:---|:---|:---:|:---|
| **Phase 0** | C++, STL, brute force, basic math | 0 → 900 | ~1 month |
| **Phase 1** | Sorting, binary search, two pointers, greedy, constructive | 900 → 1200 | ~3 months |
| **Phase 2** | Number theory, modular arithmetic, BFS/DFS, DSU, Dijkstra, MST | 1200 → 1400 | ~3 months |
| **Phase 3** | DP (1D, 2D, bitmask, tree), BIT, segment tree, sparse table | 1400 → 1550 | ~3 months |
| **Phase 4** | Lazy seg tree, LCA, string algorithms, SCC, harder DP, probability | 1550 → 1800 | ~4 months |
| **Phase 5** | Flow, HLD, centroid decomposition, FFT, suffix structures | 1800+ | Post-goal |

### `03 Topics` — Deep-Dive Notes (61 notes)

Every topic note follows a consistent structure:

- **Metadata** — phase, rating, estimated days, priority, status (`todo`/`doing`/`done`)
- **Prerequisites & Unlocks** — what to learn first and what this topic enables
- **What to Learn** — concise explanation of the concept
- **Code Template** — copy-paste-ready C++ snippet
- **Resources** — links to cp-algorithms, CSES, Codeforces EDU, etc.
- **Practice Plan** — curated problem list with checkboxes (Codeforces, CSES, Toph)
- **Common Pitfalls** — mistakes to avoid
- **Definition of Done** — checkboxes to confirm mastery

<details>
<summary><b>📋 Full topic list (click to expand)</b></summary>

#### Phase 0 — Foundations
- C++ Setup and Fast IO
- STL Essentials
- Complexity and Constraints
- Implementation
- Brute Force and Complete Search
- Basic Math, Parity and Divisibility

#### Phase 1 — Core Techniques
- Sorting and Custom Comparators
- Binary Search and Search on the Answer
- Two Pointers and Sliding Window
- Prefix Sums and Difference Arrays
- Greedy Algorithms
- Constructive Algorithms
- Bit Manipulation
- String Basics
- Recursion and Backtracking
- Stack, Queue, Deque and Priority Queue

#### Phase 2 — Math & Graphs
- Number Theory Basics
- Sieve and Factorization
- Modular Arithmetic
- Binary Exponentiation
- Combinatorics (nCr mod p)
- Graph Basics and Representation
- Breadth-First Search
- Depth-First Search
- Disjoint Set Union
- Topological Sort and DAGs
- Dijkstra's Shortest Path
- Minimum Spanning Tree

#### Phase 3 — DP & Data Structures
- DP Foundations
- Knapsack DP
- DP on Grids and Sequences
- Bitmask DP
- Tree DP
- Fenwick Tree (BIT)
- Segment Tree
- Sparse Table

#### Phase 4 — Advanced to 1800
- Segment Tree with Lazy Propagation
- Lowest Common Ancestor
- Euler Tour and Tree Flattening
- String Hashing
- KMP, Prefix Function and Z-Function
- Trie (Prefix Tree)
- Mo's Algorithm and Sqrt Decomposition
- Interval DP
- Digit DP
- Strongly Connected Components and Bridges
- Bellman-Ford and Floyd-Warshall
- Probability and Expected Value
- Game Theory (Nim and Grundy)
- Inclusion-Exclusion
- Geometry Basics
- Divide and Conquer
- Meet in the Middle
- Interactive Problems
- Matrix Exponentiation

#### Phase 5 — Beyond 1800
- Flow and Bipartite Matching
- Heavy-Light and Centroid Decomposition
- 2-SAT
- FFT and NTT
- Suffix Array and Automaton
- Convex Hull Trick and Li Chao Tree

</details>

### `04 Calendar` — Month-by-Month Plan (15 notes)

14 monthly plans (November 2026 → December 2027) plus an overview. Each month links to its topics, suggests a weekly rhythm, recommends contest types, and has a checkpoint checklist.

### `05 Resources` — Curated Links (6 notes)

| Note | Highlights |
|:---|:---|
| **Platforms Hub** | Codeforces, CSES, AtCoder, Toph, USACO Guide, cp-algorithms, VisuAlgo, clist |
| **Books and Courses** | CP Handbook (free PDF), CP4, CLRS, ITMO Academy, USACO Guide |
| **Video Channels** | Errichto, Algorithms Live!, Neal Wu |
| **Tools and Extensions** | cph (VS Code), Carrot extension, sanitizer flags |
| **Toph Category Map** | Every Toph problem category mapped to the vault's topic notes |

### `06 Templates` — Obsidian Templates (4 notes)

Ready-to-use templates for the built-in Obsidian Templates plugin:
- **Problem Log Template** — one note per problem
- **Contest Review Template** — post-contest reflection
- **Weekly Review Template** — weekly check-in
- **Topic Note Template** — create your own topic notes

### `07 Tracking` — Progress Logs (6 notes)

| Note | Purpose |
|:---|:---|
| **Problem Log** | Table to record every problem solved |
| **Mistake Log** | One line per mistake — reviewed weekly |
| **Contest Log** | Contest results and rating changes |
| **Rating Tracker** | Monthly target vs. actual rating |
| **Weak Spots** | Checklist of all 61 topics — tick what you struggle with |
| **Dashboard** | Dataview-powered summary of topic status (optional plugin) |

---

## 🚀 Getting Started

### 1. Download

```bash
git clone https://github.com/shrobin13/raodmap-to-1800.git
```
Or download the ZIP and extract it.

### 2. Open in Obsidian

1. Install [Obsidian](https://obsidian.md/) (free).
2. **Open folder as vault** → select the `CP-Roadmap-Vault` folder.
3. Open `00 Home.md` — that's your launchpad.

### 3. Explore the Graph

Press `Ctrl + G` (or `Cmd + G` on Mac) to open **Graph View**. The vault comes with preconfigured colors:

| Color | What It Represents |
|:---|:---|
| 🟡 Yellow | Hub notes (Home, Phases, Resources) |
| 🟢 Teal | Strategy notes |
| 🔵 Per-phase colors | Topic notes grouped by phase |
| 🩷 Pink | Resource notes |

### 4. Start Learning

1. Read **Goal and Milestones** and **How to Use This Vault**.
2. Set up your C++ environment with **C++ Setup and Fast IO**.
3. Follow the **Calendar Overview** month by month.

---

## 💡 Core Principles

1. **Solve > Read.** 60% solving, 20% learning, 20% contests.
2. **Practice at the edge.** Problems rated 100–200 above your current level.
3. **Upsolve everything.** Most growth happens after the contest ends.
4. **Consistency wins.** 2 hours every day beats 10 hours on Sunday.
5. **Only core topics for 1800.** Optional and stretch topics can wait.

---

## 🔧 Customization

This vault is **yours to edit**. The notes are plain Markdown with wikilinks — reorder topics, change dates, delete what you don't need, and add your own notes.

### Priority Labels

| Label | Meaning |
|:---|:---|
| `core` | Required for 1800 |
| `optional` | Helps but not required |
| `stretch` | For after the goal (Phase 5) |

### Topic Status

Each topic note has a `status` property in its YAML frontmatter:
- `todo` — haven't started
- `doing` — currently working on it
- `done` — mastered

Change the status as you progress. The **Dashboard** note summarizes everything if you install the [Dataview](https://github.com/blacksmithgu/obsidian-dataview) community plugin.

---

## 🌐 Platforms Used

| Platform | Link | Use Case |
|:---|:---|:---|
| Codeforces | [codeforces.com](https://codeforces.com/) | Main target — rated rounds + problemset |
| CSES | [cses.fi/problemset](https://cses.fi/problemset/) | Structured topic practice |
| AtCoder | [atcoder.jp](https://atcoder.jp/) | Clean problems + Educational DP Contest |
| Toph | [toph.co/problems](https://toph.co/problems) | Beginner-friendly practice with categories |
| USACO Guide | [usaco.guide](https://usaco.guide/) | Curriculum with explanations |
| cp-algorithms | [cp-algorithms.com](https://cp-algorithms.com/) | Algorithm reference |

---

## 📖 Recommended Reading

- [**Competitive Programmer's Handbook**](https://cses.fi/book/book.pdf) by Antti Laaksonen (free PDF) — the best first book
- **Competitive Programming 4** by Steven & Felix Halim — broad reference
- **ITMO Academy** on [Codeforces EDU](https://codeforces.com/edu/courses) — interactive courses

---

## 🤝 Contributing

Found a broken link, have a better problem suggestion, or want to add a topic note? PRs and issues are welcome.

---

## 📜 License

This vault is free to use, modify, and share. If you find it helpful, give it a ⭐ and share it with someone who's starting their CP journey.

---

<div align="center">

**Start with `00 Home.md`. Solve problems. Stay consistent. See you at 1800.** 🚀

</div>
]]>
