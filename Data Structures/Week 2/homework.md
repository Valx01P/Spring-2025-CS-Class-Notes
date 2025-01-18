![](./Homework/p1.png)

---

```java
import java.util.ArrayList;

class Main {
    public static void main(String[] args) {
        int[] arr = {16, 17, 4, 3, 5, 2};
        findDominantElements(arr);
    }
    
    static void findDominantElements(int[] nums) {
        ArrayList<Integer> result = new ArrayList();
        int max = nums[nums.length-1];
        result.add(max);
        
        for (int i = nums.length-1;i >= 0; i--) {
            if (nums[i] > max) {
                max = nums[i];
                result.add(max);
            }
        }
        
        System.out.println(result);
    }
}
```

Let's analyze our `findDominantElement` function, step by step in Java,

Initializing ArrayList, __*1 unit of time*__
Init max variable, __*1 unit of time*__
Add to result, __*1 unit of time*__

For loop which goes through input linearly in reverse
Constant time, if statement, let's say __*2 units of time*__
for what's done inside the if statement, still it's
constant

The for loop can be expressed as a summation with our constant \(2\),

\[
\sum^{n}_{i=1}2
\]
Using this formula for adding constant summations,
\[
\sum^{n}_{i=1}c=c*n
\]
We can analyze our time complexity, let's say when \(n = 6\), so when our
input array is of length \(6\),
\[
\sum^{6}_{i=1}2 = 2 * 6 = 12
\]
Then we can see that the loop has __*12 units of time*__ occurring,
or more specifically, **2n** units of time for any input, **n**, as the
loop is iterativing linearly, even as it's moving in reverse order

And then we simply print our arraylist of values, which is __*1 unit of time*__

---

Therefore, the total time complexity would be,
\[
O(1+1+1+2n+1)
\]
Which can be simplified to,
\[
\implies O(n)
\]

<!-- \[
\frac{n(n+1)}{2} \rightarrow \frac{6(6+1)}{2} \rightarrow \frac{6(7)}{2} \rightarrow \frac{42}{2} \rightarrow 21
\] -->

---

![](./Homework/p2.png)

---
