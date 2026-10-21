---
tags: [topic, phase-4, core]
phase: 4
rating: "1800-2200"
est_days: 7
priority: core
status: todo
cf_tag: "data structures"
---

# Segment Tree with Lazy Propagation

> Range updates plus range queries are common in 1800+ problems.

| | |
|---|---|
| Phase | [[Phase 4 - Advanced to 1800]] |
| Typical rating range | 1800-2200 |
| Estimated time | 7 days |
| Priority for 1800 | Core |
| Scheduled in | [[2027-10 October]] |
| Toph category | Data Structure > Segment Tree |
| Codeforces tag | data structures |

**Prerequisites:** [[Segment Tree]]

**Unlocks:** Nothing further in this roadmap

## What to learn

- Lazy tags carry deferred operations down only when you recurse into a child.
- **Push-down rule:** call `push(node)` before descending into left or right child.
- Two common lazy types: range-add (compose by summing tags) and range-assign (assign overrides add).
- Know how to compose two lazy operations: assign ∘ add = assign with new value; add ∘ add = add their sum.
- After any update or query that changes children, pull up: `t[v] = t[2v] + t[2v+1]`.

## Template

```cpp
// Range-add, Range-sum  (recursive, 1-indexed [1..n])
struct LazySegTree {
    int n;
    vector<ll> sum, lazy;
    LazySegTree(int n) : n(n), sum(4 * n, 0), lazy(4 * n, 0) {}

    void build(vector<ll>& a, int v, int l, int r) {
        if (l == r) { sum[v] = a[l]; return; }
        int m = (l + r) / 2;
        build(a, 2*v, l, m); build(a, 2*v+1, m+1, r);
        sum[v] = sum[2*v] + sum[2*v+1];
    }
    void push(int v, int l, int r) {
        if (!lazy[v]) return;
        int m = (l + r) / 2;
        apply(2*v,   l,   m, lazy[v]);
        apply(2*v+1, m+1, r, lazy[v]);
        lazy[v] = 0;
    }
    void apply(int v, int l, int r, ll val) {
        sum[v] += val * (r - l + 1);
        lazy[v] += val;
    }
    void update(int v, int l, int r, int ql, int qr, ll val) {
        if (qr < l || r < ql) return;
        if (ql <= l && r <= qr) { apply(v, l, r, val); return; }
        push(v, l, r);
        int m = (l + r) / 2;
        update(2*v, l, m, ql, qr, val);
        update(2*v+1, m+1, r, ql, qr, val);
        sum[v] = sum[2*v] + sum[2*v+1];
    }
    ll query(int v, int l, int r, int ql, int qr) {
        if (qr < l || r < ql) return 0;
        if (ql <= l && r <= qr) return sum[v];
        push(v, l, r);
        int m = (l + r) / 2;
        return query(2*v, l, m, ql, qr) + query(2*v+1, m+1, r, ql, qr);
    }
    // Convenience wrappers (1-indexed)
    void update(int l, int r, ll val) { update(1, 1, n, l, r, val); }
    ll query(int l, int r) { return query(1, 1, n, l, r); }
};
```

## Resources

- [ITMO Academy course: Segment Tree, part 2](https://codeforces.com/edu/courses)
- [cp-algorithms: Segment tree (lazy section)](https://cp-algorithms.com/data_structures/segment_tree.html)
- [USACO Guide: Lazy Segment Tree](https://usaco.guide/)

## Practice plan

- [ ] CSES Range Updates and Sums
- [ ] CSES Polynomial Queries
- [ ] CSES Range Update Queries (range assign)
- [ ] CF data structures 1800-2100: solve 10 with range updates
- [ ] Toph Segment Tree: 5 requiring lazy

Log every attempt in [[Problem Log]]. Failed problems go to [[Mistake Log]].

## Common pitfalls

- Forgetting to push before recursing.
- Wrong composition of assign and add.

## Definition of done

- [ ] You can implement range-add range-sum from memory.
- [ ] I wrote the template or a similar solution from memory.
- [ ] I solved at least 8 problems on this topic without hints.

## Notes

(Write what you learn here.)

See also: [[Toph Category Map]], [[Resources Hub]], [[00 Home]]
