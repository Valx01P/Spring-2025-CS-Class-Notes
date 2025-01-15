```
int fact(int n) {
  if n = 0
    return 1
  else fact(n-1)*n
}
```

##### Recurrence Relation
times required to compute the factorial of n
\[
T(n) = 
\begin{cases} 
      \text{fact(n)} & \text{; n > 0} \\
      \text{1} & \text{; n = 1}
\end{cases}
\]

=> Backwards Substitution
=> Recursion Tree
=> Master's Theorem

T(n) = T(n-1) + 1
T(n) = 1

T(n) = T(n-1) + 1 -> Eq.1
T(n-1) = T(n-2) + 1 -> Eq.2
T(n-2) = T(n-3) + 1 -> Eq.3

T(n) = T(n-1) + 1
T(n) = T(n-1) + 1 + 1
T(n) = T(n-3) + 1 + 2
...
T(k) = T(n-k) + k

Find a value that makes n-k = 1, k is the arbitary variable

n-k = 1
k = n - 1

Substitute

T(n) = T(n-(n-1))+(n-1)
= T(1) + n - 1
= T(1) + n - 1
= 1 + n - 1 = n
=> O(n)