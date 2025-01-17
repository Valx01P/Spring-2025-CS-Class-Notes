##### Summations and a collection of data

i = [1  2  3  4  5]
x = [3, 6, 11, 9, 17]

1 indexed in summations, not 0 indexed like in
programming languages

\[
\sum^{5}_{i = 1}x_i = x_1 + x_2 + x_3 + x_4 + x_5
\]

Start and end are inclusive, so start 2, and end 4
would sum the values 2, 3, and 4

---

You could also just use the index variable

\[
\sum^{5}_{i = 1}i = 1 + 2 + 3 + 4 + 5
\]

---

By performing a summation or product on a full
collection you can implicitly remove the bounds
which implies you are summing all of the elements
together

\[
\sum x^{2}_{i}(x_{i} - 1)
\]

and you can actually remove the summation symbol
altogether with an index variable like \(x_i\),
this is "Einstein Notation"


\[
x^{2}_{i}(x_{i} - 1)
\]

again it is implied it is a full summation of
all \(x_i\) elements in the collection

---

The capital pi symbol works the same as the capital
sigma symbol for summation, except it's for product
notation, not summation notation

x = [3, 6, 29, 4, 7]

\[
\prod^{5}_{i = 1}x_i = 3 * 6 * 29 * 4 * 7
\]

---

A summation next to a summation is basically just
a double loop, so sum all the values of the inner
summation as many times as the outer summation
goes on for

\[
\sum^{3}_{i = 1}\sum^{8}_{j = 6}i + j
\]

=

\[
\sum^{3}_{i = 1}(i + 6) + (i + 7) + (i + 8)
\]

=

(1 + 6) + (1 + 7) + (1 + 8)
(2 + 6) + (2 + 7) + (2 + 8)
(3 + 6) + (3 + 7) + (3 + 8)

```java
public class SummationExample {
    public static void main(String[] args) {
        int sum = 0;

        // Outer summation: i ranges from 1 to 3
        for (int i = 1; i <= 3; i++) {
            // Inner summation: j ranges from 6 to 8
            for (int j = 6; j <= 8; j++) {
                sum += (i + j); // Add i + j to the sum
            }
        }

        System.out.println("The result of the summation is: " + sum);
    }
}
```