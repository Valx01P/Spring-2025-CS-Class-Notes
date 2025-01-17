##### Loops
```
for (i = 1; i <= n; i++)
  //statement
```

To calculate the time complexity, we must evaluate
how many times the statement has been executed

The loop executes n times, so to does the statement,
because the statement is within the for loop

The loop runs from 1 to n, so it is clear
the total time will be O(n), assuming the
statement is taking a constant amount of time

##### Nested Loops
```
for (i = 1; i <= n; i++) {
  for (j = 1; j <= n; j++) {
    //statement
  }
}
```

The outer loop runs from 1 to n, and the
inner loop also runs from 1 to n, when
i is at 1, j will run from 1 to n, when
i is at 2, j again will run from 1 to n
and this will continue until i completes
the loop

So the outer and inner loop execute n times
Therefore, the total time complexity is

Total time = \(n * n = O(n^2)\)

So the growth is quadratic, for each value
of i, this will execute n times

---

##### Consecutive Statements

``` java
int x = 2;
int i;
x = x + 1;

for (i = 1; i <= n; i++) {
  //statement
}

for (i = 1; i <= n; i++) {
  for (j = i; j <= n; j++) {
    //statement
  }
}
```

The first 3 lines will take a total time of
3 units, the first loop will execute n times,
the nested loop will run n^2^ units

For consecutive statements, you should add
all these times

Total time = \(n^2 + n + 3 = O(n^2)\)

---

##### Summation Formula Reference

\[
\begin{array}{|c|c|}
\hline
\textbf{Summation} & \textbf{Formula} \\
\hline
\sum_{i=1}^n ar^{i-1} & a \left( \frac{1 - r^n}{1 - r} \right) \\
\hline
\sum_{i=m}^n c & c \left( n + 1 - m \right) \\
\hline
\sum_{i=m}^n i & \frac{n(n+1)}{2} - \frac{m(m-1)}{2} \\
\hline
\end{array}
\]

What is the running time of the following
code fragment?

``` java
int count = 0;

for (int i = 3; i < n; i++)
  for (int j = 0; j < i; j++)
    count++;
```

*__*c*__ for some constant amount of time*
*__*n*__ is the end of summation*
*__*m*__ is the start of summation*

T(n) = \(\sum^{n-1}_{i=3}\sum^{i-1}_{j=0}c\)

__*outer loop*__

= \(\sum^{n-1}_{i=3}(c(i-1+1-0))\)

__*n = j-1*__
__*m = 0*__

= \(\sum^{n-1}_{i=3}ci\)

= \(c * \sum^{n-1}_{i=3}i\)

= \(c * (\frac{(n-1)(n-1+1)}{2} - \frac{3(3-1)}{2})\)

= \(c * (\frac{(n-1)(n)}{2} - 3)\)

= \(c * (\frac{n^2-n}{2}-\frac{6}{2})\)

= \(c * (\frac{n^2-n-6}{2})\)

\(\implies O(n^2)\)