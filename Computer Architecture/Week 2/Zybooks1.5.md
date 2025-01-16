#### 1.5 Floating-point numbers

### Floating-point numbers and normalized scientific notation

An **integer** is a whole number, like 42, 0, or -95. A **floating-point number** is a real number, like 98.6, 0.0001, or -666.667. The term "floating-point" refers to the decimal point being able to appear anywhere ("float") in the number.

- Integers are typically used for values that can be counted, like 42 cars, 0 pizzas, or -95 days.
- Floating-point numbers are typically used for values that are measured, like 98.6 degrees, 0.0001 meters, or -666.667 grams.

To improve readability and consistency, floating-point numbers are commonly written using **normalized scientific notation**, such as \( 9.86 \times 10^1 \), \( 1.0 \times 10^{-4} \), or \( -6.66667 \times 10^2 \), where the number is written as a digit (+/- 1 to 9), decimal point, fractional part, times 10 to a power. The term "normalized" is in contrast to non-normalized where more than one digit, or a 0, may precede the decimal point, such as \( -66.6667 \times 10^{-0.1} \) or \( 0.1 \times 10^{-3} \).

The parts of scientific notation are named **significand** for the part before \( \times \) and **exponent** for the power of 10: significand \( \times 10^{exponent} \). If the exponent is 0, the power of ten part is sometimes omitted, as in 5.7.

In binary, normalized scientific notation consists of \( 1.f \times 2^{exponent} \), like \( 1.010 \times 2^5 \). \( f \) is the fractional part.


---

### 1.5.1: Normalized Scientific Notation: Decimal

Indicate which numbers are in decimal normalized scientific notation.

1) \( 2.05 \times 10^3 \)
- [x] Yes
- [ ] No

#### Explanation Q1, Yes
- All requirements of normalized scientific notation are met: The number is written as a digit (1 to 9), decimal point, fractional part, times 10 to a power.

---

2) \( 0.50 \times 10^3 \)
- [ ] Yes
- [x] No

#### Explanation Q2, No
- The digit before the decimal point must be 1 to 9. This number should have been: \( 5.0 \times 10^2 \).

---

3) \( 27.8 \times 10^3 \)
- [ ] Yes
- [x] No

#### Explanation Q3, No
- Only one digit may precede the decimal point. This number should have been: \( 2.78 \times 10^4 \).

---

4) 3.5
- [x] Yes
- [ ] No

#### Explanation Q4, Yes
- This number could have also been written as \( 3.5 \times 10^0 \). When the exponent is 0, the latter part is often omitted.

---

5) \( -5.77 \times 10^3 \)
- [x] Yes
- [ ] No

#### Explanation Q5, Yes
- The significand may be negative.

---

6) \( 2.05 \times 10^{-3} \)
- [x] Yes
- [ ] No

#### Explanation Q6, Yes
- The exponent may be negative.

---

7) 0.0
- [ ] Yes
- [x] No

#### Explanation Q7, No
- The number before the decimal point cannot be 0. As such, the value zero cannot be represented in normalized scientific notation.

---

### 1.5.2: Normalized Scientific Notation: Binary

Indicate which numbers are in binary normalized scientific notation.

1) 0.0
- [ ] Yes
- [x] No

#### Explanation Q1, No
- The number before the decimal point cannot be 0. As such, the value zero cannot be represented in normalized scientific notation.

---

2) \( 1.01 \times 2^3 \)
- [x] Yes
- [ ] No

#### Explanation Q2, Yes
- Meets all requirements for normalized scientific notation of a binary number.

---

3) \( 0.10 \times 2^3 \)
- [ ] Yes
- [x] No

#### Explanation Q3, No
- The leading digit cannot be 0. Thus, in binary, the first digit is always 1.

---

4) \( 11.10 \times 2^3 \)
- [ ] Yes
- [x] No

#### Explanation Q4, No
- More than one digit cannot precede the binary point.

---

5) \( -1.01 \times 2^3 \)
- [x] Yes
- [ ] No

#### Explanation Q5, Yes
- The significand may be negative.

---

6) \( 1.01 \times 2^{-3} \)
- [x] Yes
- [ ] No

#### Explanation Q6, Yes
- The exponent may be negative.

---

Write the number in normalized scientific notation.Use ^ for exponents. Ex: 10^4 for 
.175.987 =
1.75987x10^2

1.81435x10^2

Correct Expected: 1.75987x10^2
In normalized scientific notation, the number is written as a digit, decimal point, fractional part, then multiplied by 10 to a power.

---

To convert a decimal number like 0.6 into binary using two fraction bits, you can follow these steps:

### Steps for Conversion:

1.  **Start with the fractional part** (0.6 in this case).
2.  **Multiply the fractional part by 2**.
    *   0.6×2\=1.20.6 \\times 2 = 1.20.6×2\=1.2
3.  **Take the integer part** (1) as the first binary digit after the decimal point.
4.  **Take the fractional part** (0.2) and multiply it by 2.
    *   0.2×2\=0.40.2 \\times 2 = 0.40.2×2\=0.4
5.  **Take the integer part** (0) as the next binary digit.
6.  **Take the fractional part** (0.4) and multiply it by 2.
    *   0.4×2\=0.80.4 \\times 2 = 0.80.4×2\=0.8
7.  **Take the integer part** (0) as the next binary digit.
8.  **Take the fractional part** (0.8) and multiply it by 2.
    *   0.8×2\=1.60.8 \\times 2 = 1.60.8×2\=1.6
9.  **Take the integer part** (1) as the next binary digit.
10.  **Repeat the process**, but since the problem only asks for two fraction bits, you stop here.

### Binary Representation for 0.6:

*   0.60.60.6 in binary (to two fraction bits) is approximately **0.11**.

So, the final answer would be:

markdown

Copy code

`0.6 decimal = 0.11 binary, using two fraction bits.` 

This method approximates the number in binary, and further precision would involve more fraction bits.

---

Yes, IEEE single-precision binary floating-point format essentially represents numbers in a form similar to scientific notation, but specifically for binary numbers. It consists of three parts:

1.  **Sign bit**: This indicates whether the number is positive or negative.
    
    *   0 represents positive.
    *   1 represents negative.
2.  **Exponent**: This part contains the exponent of the number, but it uses **biased representation**. In single-precision (32-bit), the bias is 127. The exponent is stored as an 8-bit value, and the actual exponent is the value stored minus the bias (127).
    
3.  **Significand (Mantissa)**: This represents the fractional part of the number. The first digit is implicitly 1 for normalized numbers (not explicitly stored), and the rest of the digits (23 bits) represent the fractional part.
    

### Scientific Notation in Binary

This representation makes it easy to express a number in scientific notation, similar to how numbers are written with powers of 10 in decimal scientific notation. For example:

*   888 can be written as 1.0×231.0 \\times 2^31.0×23.
*   −20\-20−20 can be written as −1.25×24\-1.25 \\times 2^4−1.25×24.

### Explanation of the Example

In your image:

*   For the number **8**:
    
    *   The **sign bit** is 0 (indicating positive).
    *   The **exponent** is 130 (which is 130−127\=3130 - 127 = 3130−127\=3).
    *   The **significand** is 1.0 (with 0 bits for the fractional part, because it’s a whole number).
    *   The number 888 is represented as 1.0×231.0 \\times 2^31.0×23.
*   For the number **\-20**:
    
    *   The **sign bit** is 1 (indicating negative).
    *   The **exponent** is 131 (which is 131−127\=4131 - 127 = 4131−127\=4).
    *   The **significand** is 1.25 (which is 1.0+0.251.0 + 0.251.0+0.25 for the fractional part 0.25).
    *   The number −20\-20−20 is represented as −1.25×24\-1.25 \\times 2^4−1.25×24.

### Final Note

IEEE single-precision format does not only store the number in a normalized scientific notation but also adds a bias to the exponent, and the leading 1 in the significand is implied, making it efficient in storing values. Thus, it can express very large and very small numbers in a standardized way for computation.