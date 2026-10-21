---
tags: [strategy]
---

# Stress Testing

Compare your solution with a slow but correct brute force on thousands of random small inputs.

Files: `sol.cpp` (your solution), `brute.cpp` (brute force), `gen.cpp` (random input generator).

```cpp
// gen.cpp
#include <bits/stdc++.h>
using namespace std;
int main(int argc, char **argv) {
    mt19937 rng(atoi(argv[1]));
    int n = rng() % 8 + 1;
    cout << n << "\n";
    for (int i = 0; i < n; i++) cout << rng() % 10 + 1 << " ";
    cout << "\n";
}
```

```bash
#!/bin/bash
g++ -O2 -o sol sol.cpp && g++ -O2 -o brute brute.cpp && g++ -O2 -o gen gen.cpp
for ((i = 1; i <= 2000; i++)); do
    ./gen $i > in.txt
    ./sol < in.txt > out1.txt
    ./brute < in.txt > out2.txt
    if ! diff -q out1.txt out2.txt > /dev/null; then
        echo "Difference on seed $i"; break
    fi
done
```

Use it on greedy and constructive problems especially ([[Greedy Algorithms]], [[Constructive Algorithms]]).

Related: [[Practice Method]], [[Brute Force and Complete Search]]
