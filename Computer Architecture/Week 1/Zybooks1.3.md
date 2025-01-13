#### 1.3 Unsigned binary numbers

##### Counting in binary
Humans have then fingers so humans use a base then number system. Ex: 452 means,
4 x \(10^{2}\) + 5 x \(10^{1}\) + 2 x \(10^{0}\).

Digital systems have two-valued signals (high, low) so digitally systems use a
base two number system. Ex: 1101 means,
1 x \(2^{2}\) + 1 x \(2^{1}\) + 1 x \(2^{0}\)

A number in base ten is called a decimal number (from Latin "decem" meaning ten),
while a number in base two is called a  binary number (from Latin "bini" meaning
two together).

Base ten has ten symbols for a digit: 0, 1, ..., 9. When counting up and reaching
9, the digits resets to 0 and a 1 carries to the next digit. Ex: 008, 009, 010,
011, or 098, 099, 100, 101. Base two has only two symbols for a digit: 0 and 1.
So counting up results in frequent carries. Ex: 000, 001, 010, 011, 100, 101, 
110, 111. Each digit in a binary number is called a bit, short for "binary 
digit".

##### 1.3.1: Counting up in decimal and in binary

### Various Quantities

| Base 10 | Base 2 | Explanation |
|---------|--------|-------------|
| 0       | 0      | 0           |
| 1       | 1      | 1           |
| 2       | 10     | Reset, carry|
| 3       | 11     |             |
| 4       | 100    | Reset, carry and reset, carry |
| 5       | 101    |             |
| 6       | 110    | Reset, carry|
| 7       | 111    |             |
| 8       | 1000   | Reset, carry and reset, carry and reset, carry |
| 9       | 1001   |             |
| 10      | 1010   | Reset, carry|
| 11      | 1011   |             |
| ...     | ...    | ...         |
| 98      | 1100010|             |
| 99      | 1100011|             |
| 100     | 1100100| Reset digit to 0, carry 1 to next digit which is 9 so reset to 0, carry 1 to next digit |

---

### Captions
1. Various quantities.
2. In base ten, the first digit goes up to 9, then the digit is reset to 0 and a 1 is carried to the next digit.
3. If the carry is to a digit that is already 9, then that digit is also reset to 0 and a 1 is carried to the next digit.
4. In base two, the first digit goes up to 1, then the digit is reset to 0 and a 1 is carried to the next digit.
5. If the carry is to a digit that is already 1, then that digit is also reset to 0 and a 1 is carried to the next digit.
6. Resets and carries happen on every other count.

---

##### Converting from binary to decimal

# Binary to Decimal Conversion

Software and hardware developers benefit from being able to quickly convert between binary and decimal numbers.

Given a binary number, each digit's weight is summed to form a decimal number.  
**Example:** \(1101 = 1 \times 2^3 + 1 \times 2^2 + 0 \times 2^1 + 0 \times 2^0 = 8 + 4 + 0 + 1 = 13\).

---

#### Note:
- This section only covers unsigned binary numbers. An unsigned binary number can only represent non-negative values, such as a 4-bit binary number being 0000 (0), 0001 (1), 0010 (2), ..., 1111 (15). In contrast, a signed binary number uses the leftmost bit to represent whether a number is positive or negative.

### 1.3.2: Counting up in binary

1) 000
- [x] 001
- [ ] 010
- [ ] 011
- [ ] 100

#### Explanation Q1, 001
- Counting up always starts by trying to add 1 to the rightmost digit.

---

2) 001
- [x] 010
- [ ] 011
- [ ] 100
- [ ] 101

#### Explanation Q2, 010
- 1 can't be added to the rightmost digit due to being at the max of 1, so that digit is reset to 0, and a 1 is carried to the next digit.

---

3) 010
- [x] 011
- [ ] 100
- [ ] 101
- [ ] 110

#### Explanation Q3, 011
- Counting up always starts by trying to add 1 to the rightmost digit, from 0 to 1. The rightmost digit is currently 0, so becomes 1.

---

4) 011
- [x] 100
- [ ] 101
- [ ] 110
- [ ] 111

#### Explanation Q4, 100
- 1 can't be added to the rightmost bit, so that bit is reset to 0 and a carry is generated to the second bit.
- 1 can't be added to the second bit, so that bit is reset to 0 and a carry is generated to the third (leftmost) bit.

---

5) 111 (type a 4-bit answer)
- [x] 1000
- [ ] 1010
- [ ] 1100
- [ ] 1110

#### Explanation Q5, 1000
- The rightmost bit is reset to 0 and a carry is generated for the next bit. That bit is also reset to 0, and a carry is generated for the next bit.
- That bit is also reset to 0 and a carry is generated to the next bit. That bit isn't shown initially but is assumed 0, so becomes 1. (Akin to 99 incrementing to 100).


---

### Binary to Decimal Tool

| Binary Digits | \(2^7\) | \(2^6\) | \(2^5\) | \(2^4\) | \(2^3\) | \(2^2\) | \(2^1\) | \(2^0\) |
|----------------|--------|--------|--------|--------|--------|--------|--------|--------|
| 0              | 128    | 64     | 32     | 16     | 8      | 4      | 2      | 1      |
| Binary         | 0      | 0      | 0      | 0      | 1      | 1      | 1      | 1      |
| Decimal Value  | 0      | 0      | 0      | 0      | 8      | 4      | 2      | 1      |
| Total = 7      |        |        |        |        |        |        |        |        |

### Steps:
- The binary number \(00001111_2\) converts to decimal by summing the products of each binary digit and its corresponding power of 2:
  \[
  0 \times 128 + 0 \times 64 + 0 \times 32 + 0 \times 16 + 1 \times 8 + 1 \times 4 + 1 \times 2 + 1 \times 1 = 7
  \]

---

### Binary Addition Questions

1) 0010 + 0010
- [x] 0100
- [ ] 0110
- [ ] 1000
- [ ] 1010

#### Explanation Q1, 0100
- Counting up always starts by trying to add 1 to the rightmost digit.

---

2) 0110 + 0010
- [x] 1000
- [ ] 1100
- [ ] 1110
- [ ] 1010

#### Explanation Q2, 1000
- So 6 + 2 = 8. Multiple columns can carry a 1.

---

3) 0101 + 0111
- [x] 1100
- [ ] 1010
- [ ] 1110
- [ ] 1000

#### Explanation Q3, 1100
- So 5 + 7 = 12.

---

### Decimal to Binary Conversion

1) 3
- [x] 0011
- [ ] 0100
- [ ] 0110
- [ ] 1000

#### Explanation Q1, 0011
- 3 in decimal is represented as \(0011_2\), where each binary digit (bit) represents a power of 2: \(2^1 + 2^0 = 3\).

---

2) 4
- [x] 0100
- [ ] 1000
- [ ] 1100
- [ ] 0011

#### Explanation Q2, 0100
- 4 in decimal is represented as \(0100_2\), where \(2^2 = 4\).

---

3) 5
- [x] 0101
- [ ] 1001
- [ ] 0110
- [ ] 1010

#### Explanation Q3, 0101
- 5 in decimal is represented as \(0101_2\), where \(2^2 + 2^0 = 5\).

---

4) 13
- [x] 1101
- [ ] 1011
- [ ] 1110
- [ ] 1001

#### Explanation Q4, 1101
- 13 in decimal is represented as \(1101_2\), where \(2^3 + 2^2 + 2^0 = 13\).

---

### Overflow Detection for Four-Bit Binary Numbers

1) 0001 + 0010
- [ ] Overflow
- [x] No overflow

#### Explanation Q1, No overflow
- Sum is simply 0011.

---

2) 0111 + 0111
- [ ] Overflow
- [x] No overflow

#### Explanation Q2, No overflow
- Sum is 1110. The leftmost digits did not generate a carry.  
  (In base 10, 7 + 7 is 14, which is representable in 4 bits as 1110).

---

3) 1000 + 0111
- [ ] Overflow
- [x] No overflow

#### Explanation Q3, No overflow
- Sum is 1111. Close, but no overflow.

---

4) 1000 + 1000
- [x] Overflow
- [ ] No overflow

#### Explanation Q4, Overflow
- Leftmost digits generate a carry, meaning overflow.  
  Sum would be 10000, requiring more than four bits. (In base 10, 8 + 8 is 16, which is 10000, requiring 5 bits).

---

5) 1100 + 0111
- [ ] Overflow
- [x] No overflow

#### Explanation Q5, No overflow
- First (rightmost) bit: 0 + 1 = 1  
- Second bit: 0 + 1 = 1  
- Third bit: 1 + 1 = 0, carry 1  
- Fourth bit: 1 + 0 + carry 1 = 0, carry 1  
- Leftmost digits generated a carry. Overflow. (In base 10, 12 + 7 is 19, which is 10011, requiring 5 bits).

---

6) 1111 + 1111
- [x] Overflow
- [ ] No overflow

#### Explanation Q6, Overflow
- Obviously! (In base 10, 15 + 15 is 30, which is 11110, requiring 5 bits).

---

7) In base 10, for 2 digit numbers:  
50 + 70
- [x] Overflow
- [ ] No overflow

#### Explanation Q7, Overflow
- The leftmost digits of 5 + 7 yield 2 carry 1 (12). If only two digits are available, the resulting 120 cannot fit and is an overflow.
