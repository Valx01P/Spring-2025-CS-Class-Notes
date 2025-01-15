```
A (n) {
  int sum = 0;
  for (int i = 0; i <= n; i++)
    sum += i
}
```
T(n) =
\[
\sum_{i=0}^{n}1
\]
= n - 0 + 1
= n + 1 => O(n)

---

```
A (n) {
  for (int i = n; i >= 1; i--) {
    print('hello')
  }
}
```
T(n) = 
<!-- \(\sum_{i=0}^{n}1\) -->
\[
\sum_{i=0}^{n}1
\]
= O(n)

---
```
A (n) {
  int sum = 0;
  for (int i = 0; i <= n; i++)
    for (int j = 0; i<= n; j++)
      sum += i
}
```
T(n) =

\[
\sum_{i=0}^{n}\sum_{j=0}^{n}1
\]

=

\[
\sum_{i=0}^{n}n+1
\]

=

\[
n+1\sum_{i=0}^{n}1
\]

= n+1(n+1) = \(n^2\)+2n+2 => O(\(n^2\))



```
A (n) {
  int sum = 0;
  for (int i = 0; i <= n; i++)
    for (int j = 0; i<= n; j++)
      for (int k = 0; k <= n; k++)
        sum += i
}
```

T(n) = \(\sum_{i=0}^{n}\sum_{j=0}^{n}\sum_{k=0}^{n}1\)
= \(\sum_{i=0}^{n}\sum_{j=0}^{n}(n+1)\)
= (n+1) \(\sum_{i=0}^{n}\sum_{j=0}^{n}1\)
=(n+1)\(\sum_{i=0}^{n}(n+1)\)
= (n+1)\(^2\sum_{i=0}^{n}1\)
= \((n+1)^2(n+1)\)
= \((n+1)^3 => O(n^3)\)

---

```
A (n) {
  int sum = 0;
  for (int i = 0; i <= n; i++)
    for (int j = 0; i<= n; j++)
      for (int k = 0; k <= n; k++)
        print('hello')
}
```

T(n) = \(\sum_{i=1}^{n}\sum_{j=1}^{n}\sum_{k=1}^{100}1\)
= \(\sum_{i=1}^{n}\sum_{j=1}^{n}100\)
= 100\(\sum_{i=1}^{n}\sum_{j=1}^{n}1\)
= 100\(\sum_{i=1}^{n}n\)

T(n) = 100n\(\sum_{i=1}^{n}1\)
= 100 n x n
= 100\(n^2 => O(n^2)\)

---

// code
A(n) {
  int sum = 0
  for (int i=1; \(i^2\)<= n; i++)
    sum += 1
}

T(n) = \(\sum_{i=0}^{\sqrt{n}}1\)
= \(\sqrt{n}-1+1\)
=> O\((\sqrt{n})\)

---


A (n) {
  for (int i = 1; i <= n; i++)
    for (int j = 1; j <= \(i^2\); j++)
      for (int k = 1; k <= \(\frac{n}{2}\); k++)
        print('hello')
}

T(n) = \(\sum_{i=1}^{n}\sum_{j=1}^{i^2}\sum_{k=1}^{\frac{n}{2}}1\)
= \(\sum_{i=1}^{n}\sum_{j=1}^{i^2}\frac{n}{2}\)
=> \(\frac{n}{2}\sum_{i=1}^{n}\sum_{j=1}^{i}1\)

T(n) = \(\frac{n}{2}\sum_{i=1}^{n}\) \(i^2\)
= \(\frac{n}{2}\sum_{i=1}^{n}i^2\)
= \(\frac{n}{2}(\frac{n(n+1)(2n+1)}{6})\)
=> O\((n^4)\)

---
// cant directly use sum equation

A(n) {
  int sum = 0
  for (int i = 1; i < n; i = ix2) // depending on what is multiplied, the base is different
    sum += i
}

i = 1, 2, 3, 4, 5, 6, ... n
= \(2^0, 2^1, 2^2, 2^3, 2^4, ... 2^k => log_n\)

\(n = 2^k\)
\(k = log_n\)
=> \(O(log_2 n)\)

---

A(n) {
  for (int i = \(\frac{n}{2}\); i <= n; i++)
    for (int j = 1; j <= \(\frac{n}{2}\);j++)
      for (int k = 1; k <= n; k = k * 2)
        print("hello")
}


// for regular equations you can just choose the higher order polynomials,
// but when there are logs you cannot

// tip
// start from inner loop to outer

---