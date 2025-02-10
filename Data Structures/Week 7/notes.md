#### Trees

- Collection of \(n\) nodes with \(n - 1\) edges

---

##### Number of nodes of full tree

\(N = 2^{h+1}-1\)

##### Height of a full tree with n nodes

\(2^h - 1 = N\)
\(\implies 2^h = N + 1\)
\(\implies h = log(N+1) \rightarrow O(log N)\)

---

The height, h, is important because it determines the time
complexity of many tree operations (insert, delete, etc.)
