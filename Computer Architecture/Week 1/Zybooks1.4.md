#### 1.4 Signed numbers in binary

**Unsigned numbers** involve only non-negative numbers, like 0 and 3.
**Signed numbers** involve both positive and negative numbers, like 3 and -3.

In binary, a **signed-magnitude representation** uses the left bit for the sign:
0 means positive, 1 means negative. Ex: For 4-bit numbers, 0011 is 3, and 1011 is
-3. Signed-magnitude representation is rarely used, because calculations involving
negative numbers, such as 5 - 3, require special circuits beyond an adder.

A more clever negative number representation uses an adder for both positive and
negative numbers. A __complement__ of an N-digit number is another number that
yields a sum of 100.00 (with N 0s) and can be used to represent the negative
of that number.

### Two's Complement Signed-Number Representation

1) Base 2:

  0011 (3)
  invert
  1100
  add 1
  1101

### Captions
1. **Intuition in base 10.**
2. **In base 2**, a complement is obtained by inverting each bit and adding 1.
3. **Subtraction** is performed by adding the complement.

The above is called the **two's-complement representation, which inverts every
bit and adds 1. One's complement also exists, but is rarely used, so one's
complement is not discussed further. This material uses "complement" to mean
two's complement.

The left bit indicates the sign. 0011 is +3. 1101 is a negative; complementing
yields the positive version: 0010 + 1 = 0011, which is 3. So 1101 is -3.

---

### 1.4.2: Two's-complement signed number representation

1) In base 10, for two digits, what is the complement of 33?
- [x] 67
- [ ] 66
- [ ] 100
- [ ] 33

#### Explanation Q1, 67
- \(33 + 67 = 100\). Base 10 is introduced here for intuition. Digital circuits use base 2.

---

2) In base 2, for 4 bits, what is the complement of 0010?
- [x] 1110
- [ ] 1101
- [ ] 1011
- [ ] 1001

#### Explanation Q2, 1110
- Invert the bits: \( 1101 \). Then add 1: \( 1101 + 1 = 1110 \).

---

3) What is -2 in 4-bit two's complement representation?
- [x] 1110
- [ ] 1100
- [ ] 1011
- [ ] 0111

#### Explanation Q3, 1110
- \( +2 \) is \( 0010 \). Complement to obtain the negative representation:
  - Invert the bits: \( 1101 \).
  - Then add 1: \( 1101 + 1 = 1110 \).
  - So, 1110 represents -2.

---

4) What is -7 in 4-bit two's complement representation?
- [x] 1001
- [ ] 1010
- [ ] 1111
- [ ] 1101

#### Explanation Q4, 1001
- \( 7 \) is \( 0111 \). Complement to obtain the negative representation:
  - Invert the bits: \( 1000 \).
  - Then add 1: \( 1000 + 1 = 1001 \).
  - So, 1001 represents -7.

---

5) Assuming 4-bit two's complement representation, is 1011 positive or negative?
- [x] Negative
- [ ] Positive

#### Explanation Q5, Negative
- Left bit is 1, so negative.

---

6) Assuming two's complement representation, what base 10 number does 1001 represent?
- [x] -7
- [ ] 7
- [ ] 8
- [ ] -8

#### Explanation Q6, -7
- Left bit is 1, so negative.
- Complement to find positive: \( 0110 + 1 = 0111 \).
- Magnitude is 7. Negate to yield -7.

---

7) Assuming two's complement representation, what base 10 number does 1111 represent?
- [x] -1
- [ ] 1
- [ ] 0
- [ ] -2

#### Explanation Q7, -1
- Left bit is 1, so negative.
- Complement to find positive: \( 0000 + 1 = 0001 \).
- Magnitude is 1. Negate to yield -1.

---

8) In base two, for 4 bits, what is the complement of 0000?
- [x] 0000
- [ ] 1111
- [ ] 1000
- [ ] 1100

#### Explanation Q8, 0000
- Invert the bits: \( 1111 \). Then add 1: \( 1111 + 1 = 10000 \), which in 4 bits is 0000.
- 0000 is an exception.

---

9) What is -3 in 8-bit two's complement representation?
- [x] 11111101
- [ ] 11111011
- [ ] 11111110
- [ ] 10000011

#### Explanation Q9, 11111101
- \( +3 \) is \( 00000011 \) in 8 bits.
- Complement to find negative:
  - \( (00000011)' + 1 = 11111100 + 1 = 11111101 \).

---

### Two's Complement Arithmetic

1) \( 6 + 2 \) is \( 0110 + ? \)
- [x] 0010
- [ ] 0100
- [ ] 1000
- [ ] 0011

#### Explanation Q1, 0010
- 2 is \( 0010 \) in binary. The leftmost 0 means positive.

---

2) \( 6 + (-2) \) is \( 0110 + ? \)
- [x] 1110
- [ ] 0011
- [ ] 1100
- [ ] 1111

#### Explanation Q2, 1110
- 2 is \( 0010 \). The negative is the complement, so \( 1101 + 1 \), or \( 1110 \).

---

3) \( 3 + (-4) \) is \( 0011 + 1100 = ? \)
- [x] 1111
- [ ] 1100
- [ ] 1011
- [ ] 1001

#### Explanation Q3, 1111
- Once represented as two's complement, numbers can be added, even if one is negative.

---

4) \( 2 - 3 \) is \( 0010 + ? \)
- [x] 1101
- [ ] 0111
- [ ] 1011
- [ ] 1001

#### Explanation Q4, 1101
- \( 2 - 3 \) is \( 2 + (-3) \).  
- \( -3 \) is \( 0011 \) complemented, so \( 1100 + 1 = 1101 \).

---

5) \( -3 + 2 \) is \( ? + 0010 \)
- [x] 1101
- [ ] 1010
- [ ] 1001
- [ ] 1110

#### Explanation Q5, 1101
- Either or both numbers can be negative. The first number is -3, represented as the complement of 3 (\( 0011 \)), so \( 1100 + 1 = 1101 \). The result is \( 1101 + 0010 = 1111 \), or -1.

---

### Additional Explanations:

- **Overflow:** The largest positive 4-bit two's-complement number is \( 0111 \), or 7. The smallest negative is \( 1000 \), or -8. Note that two's complement represents one more negative than positive. Positive 8, 9, ... cannot be represented in 4-bit two's complement. Likewise, -9, -10, ... cannot either. Adding two positives, or adding two negatives, may yield a value that can't be represented in the given number of bits, a situation known as **overflow**.
  - Example: \( 0101 \) (5) + \( 0011 \) (3) incorrectly yields \( 1000 \), which is -8 in two's complement.

---

### Overflow

#### Adding two positives
- \( 0010 + 0011 = 0101 \) (ok)
- \( 2 + 3 = 5 \)

#### Explanation:
- Adding two positives may overflow.

---

#### Adding two negatives
- \( 1111 + 1111 = (1)1110 \) (ok)
- \( -1 + -1 = -2 \)

#### Explanation:
- Adding two negatives may overflow. **Note:** Ignore the carry-out bit.

---

#### Adding a positive and negative
- \( 1000 + 0111 = 1111 \) (ok)
- \( -8 + 7 = -1 \)

#### Explanation:
- Adding a positive and negative **cannot overflow**.

---

#### Adding two numbers that overflow
- \( 0111 + 0001 = 1000 \) (overflow)
- \( 7 + 1 \neq -8 \)

- \( 1000 + 1111 = (1)0111 \) (overflow)
- \( -8 + -1 \neq 7 \)

#### Explanation:
- Overflow occurs if numbers' sign bits are 0s, but the sum's sign bit is 1, or if the numbers' sign bits are 1s but the sum's sign bit is 0.

---

### Captions
1. **Adding two positives may overflow.**
2. **Adding two negatives may overflow.** Note: Ignore the carry-out bit.
3. **Adding a positive and negative cannot overflow.**
4. **Overflow** occurs if numbers' sign bits are 0s, but the sum's sign bit is 1, or if numbers' sign bits are 1s, but the sum's sign bit is 0.

---

What is -2 in 4-bit two's-complement representation?
Expected
+6 is 0110.
Complement to obtain the negative representation:
Invert the bits: 1001
Then add 1: 1010
So 1010 represents -6.


What decimal number does the 4-bit two's complement value 1011 represent?
Correct Expected: -5
Left bit is 1, so negative.
Complement to find positive.
0100 + 1 = 0101
Magnitude is 5. Negate to yield -5.


Assume 4-bit two's-complement representation. 0011 + 1011 = 
Expected: 1110
0011 (3) + 1011 (-5) = 1110 (-2)
Once represented as two-complement, numbers can be added, even if one is negative.
So 3 - 5 = -2 which is 1110.


Assume 4-bit two's-complement representation.3 - 4 is 0011 + 1100 =
Correct Expected: 3 - 4 is 0011 + 1100 = 1111
3 - 4 is 3 + -4.
-4 is 0100 complemented, so 1011 + 1 or 1100. The result is 0011 + 1100 = 1111.
So 3 - 4 = -1 which is 1111.


Assume 4-bit two's-complement representation. Compute -7 + -1.
Expected: 1 1000, No overflow
1001 + 1111 = 1 1000.
Drop the carry bit, so 1000.
The input numbers' sign bits and the sum's sign bit match, so no overflow.