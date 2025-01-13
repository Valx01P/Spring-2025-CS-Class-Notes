### For **Unsigned Numbers**:

1.  **Divide the number by 2** and note the remainder (0 or 1). This remainder is the least significant bit (LSB).
2.  **Divide the quotient by 2**, repeating the process, until the quotient becomes 0.
3.  Write the remainders from the last step to the first (bottom to top). This forms the binary equivalent.

#### Example: Convert 71 (Decimal) to Binary

-.  71 ÷ 2 = 35 remainder **1**.
-.  35 ÷ 2 = 17 remainder **1**.
-.  17 ÷ 2 = 8 remainder **1**.
-.  8 ÷ 2 = 4 remainder **0**.
-.  4 ÷ 2 = 2 remainder **0**.
-.  2 ÷ 2 = 1 remainder **0**.
-.  1 ÷ 2 = 0 remainder **1**.

Now, write the remainders from bottom to top: **71 (Decimal) = 1000111 (Binary)**.

---

### For **Signed Numbers (Two's Complement)**:

1.  Convert the **absolute value** of the number to binary using the steps above.
2.  If the number is **negative**:
    *   Add leading 0s to ensure the binary number fits the desired byte size (usually 8 bits for a `byte`).
    *   Flip all the bits (change 0 to 1 and 1 to 0).
    *   Add 1 to the flipped binary number to get the two's complement.

#### Example: Convert -84 (Decimal) to Binary (8-bit):

1. Ignore the negative sign and convert 84 to binary: 84→1010100.
2. Add leading 0 to make it 8 bits: 01010100.
3. Flip all the bits: 10101011.
4. Add 1 to the result:
10101011 + 1 = 10101100

So, **\-84 (Decimal) = 10101100 (Binary)** in 8-bit two's complement.