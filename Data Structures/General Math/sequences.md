1, 2, 3, 4...

##### natural numbers

each term = \(a_n\)
sequence = {\(a_n\)}

\({a_n} = n\)

\(a_1 = 1\)
\(a_2 = 2\)
\(a_3 = 3\)

---

2, 4, 6, 8...

##### even numbers

\({a_n} = 2n\)

\(a_1 = 2(1) = 2\)
\(a_2 = 2(2) = 4\)
\(a_3 = 2(3) = 6\)

---

2, 3, 4, 5...

##### natural numbers from 2

\({a_n} = n + 1\)

\(a_1 = (1) + 1 = 2\)
\(a_2 = (2) + 1 = 3\)
\(a_3 = (3) + 1 = 4\)

---

##### Generating Arithmetic Sequences

\({a_n} = 2n + 3\)

\(a_1 = 2(1) + 3 = 5\)
\(a_2 = 2(2) + 3 = 7\)
\(a_3 = 2(3) + 3 = 9\)
\(a_4 = 2(4) + 3 = 11\)
\(a_5 = 2(5) + 3 = 13\)

Sequences like this are called arithmetic sequences
because each term differs from the previous by a
constant amount, in this case, by two, but not all
sequences work this way

---

##### Generating Geometric Sequences

\({a_n} = 2 * 3^{n-1}\)

2, 6, 18, 54...

There are also geometric sequences, where each term 
can be obtained, not by adding a constant to the 
previous term, but by multiplying the previous term 
by a constant, something like 2, 6, 18, 54 can be
obtained by multiplying the previous term by 3

---

##### Generating Other Sequences

\({a_n} = 2^n - 1\)

\(a_1 = 2^1 - 1 = 1\)
\(a_2 = 2^2 - 1 = 3\)
\(a_3 = 2^3 - 1 = 7\)
\(a_4 = 2^4 - 1 = 15\)
\(a_5 = 2^5 - 1 = 31\)

Some sequences fall into neither of these categories

If a sequence has a domain that includes all positive
integers, meaning that starting from 1, you can keep
plugging in numbers all the way to infinity, this is
called an infinite sequence, all the examples we've
looked at are examples of infinite sequences

**domain** = all positive integers
this is an __*infinite sequence*__

**domain** = finite interval
it would be a __*finite sequence*__

---

##### Generating Other Sequences

\(a_n = a_{n-1}+a_{n-1}\)

\({a_n} = 1, 1, 2, 3, 5, 8, 13, 21, 34...\)

There are also sequences derived exclusively from
the previous terms of the sequence, a famous example
is the fibonacci sequence, this one starts with a one
and then another one, and then every term after that
is the sum of the previous two terms

This sequence uses a __*Recursion Formula*__
meaning we can define any term \(a_n\)
by **previous terms**

In this case,

\(a_n = a_{n-1}+a_{n-1}\)

---

###### Understanding Factorial Notation

n! = n(n - 1)(n - 1)(n - 3)...1

Another type of sequence that does this, can be
found in factorial notation, the sequence n factorial
with factorial being represented by an exclamation
mark is equal to n times n - 1, times n - 2, and so
on, until we get to 1

For example,

1! = 1
2! = (2)(1) = 2
3! = (3)(2)(1) = 6
4! = (4)(3)(2)(1) = 24
5! = (5)(4)(3)(2)(1) = 120

The values of n factorial for the first few natural
numbers, factorials are similar to exponents in how
they only operate on the number they directly follow

\[
 a_n = \frac{3}{(n + 1)!} 
\]

\(a_1 = 3/(1 + 1)! = 3/2\)
\(a_2 = 3/(2 + 1)! = 1/2\)
\(a_3 = 3/(3 + 1)! = 1/8\)
\(a_4 = 3/(4 + 1)! = 1/40\)

---

##### Understanding Summation Notation

\[
\sum^{5}_{i = 1}a_i = a_1 + a_2 + a_3 + a_4 + a_5
\]

= 1 + 2 + 3 + 4 + 5 = 15

In this case, we say 1 is the lower limit of
summation and 5 is the upper limit of summation

---

1 + 4 + 9 + 16 + 25...

These are the **perfect squares**
they can be re-written as,

\(1^2 + 2^2 + 3^2 + 4^2 + 5^2...\)

That means we can write this as the sum of
n squared, from one to infinity

\[
\sum^{\infty}_{n = 1}n^2
\]

We can also truncate it at any particular term,
like after the fifth one and then make the upper
limit five

1 + 4 + 9 + 16 + 25

\(1^2 + 2^2 + 3^2 + 4^2 + 5^2\)

\[
\sum^{5}_{n = 1}n^2
\]

---

\[
\frac{1}{2} + \frac{2}{3} + \frac{3}{4} + \frac{4}{5} + \frac{5}{6} ...
\]

\[
\sum^{\infty}_{n = 1}\frac{n}{n + 1}
\]

---

\[
\frac{3}{4} + \frac{6}{5} + \frac{9}{6} + \frac{12}{7} + \frac{15}{8} ...
\]

\[
\sum^{\infty}_{n = 1}\frac{3n}{n + 3}
\]

---

##### Deriving Euler's Number (e)

\[
1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \frac{1}{4!} + \frac{1}{5!} ...
\]

The natural base, e
If we start adding the first few terms

\[
1 + 1 + \frac{1}{2}
\]

e = 2.5


\[
1 + 1 + \frac{1}{2} + \frac{1}{6}
\]

e = 2.667


\[
1 + 1 + \frac{1}{2} + \frac{1}{6} + \frac{1}{24}
\]

e = 2.708


\[
1 + 1 + \frac{1}{2} + \frac{1}{6} + \frac{1}{24} + \frac{1}{120}
\]

e = 2.717


##### And by now, we already have e to a few decimals

This infinite series has a finite sum (e), this is
different from other infinite series, like the
sequence of natural numbers, which has an
infinite sum (\(\infty\))

This brings up the notion of limits

---

##### Understanding Series and Limits

\[
1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \frac{1}{4!} + \frac{1}{5!} ...
\]

as **n** approaches **infinity** this *series*
approaches *e*

---

A __*sequence*__ is a list
A __*series*__ results from adding the numbers in the
list together

---

Sequences in sequence notation

2, 5, 8, 11, 14, 17 ...
\({a_n} = 3n - 1\)

2, 8, 18, 32, 50, 72 ...
\({a_n} = 2n^2\)

1, 2, 6, 24, 120, 720 ...
\({a_n} = n!\)