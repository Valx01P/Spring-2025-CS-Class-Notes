#### Notes

Numerical data (both integer and real values) are representable in a "language"
known as a **base**. The base determines the ___digits___ we can use; which always
run from ___0 to the base-1___.

When declaring an integer variable in Java, we most often use type 'int':

int x;

This makes **x** a 32-bit ____signed____ integer (all Java ints are 32 bits, and
x can clearly be set to a positive or negative value so it needs a sign).

- Signed integers use a notation called Two's Complement, in the case of int it
would be a 32-bit Two's Complement.

- Some languages let you explicitly declare an integer as unsigned, meaning the
value is zero or positive (so no sign is required):

  - ___unsigned int x;___

  Unsigned integers do not use Two's Complement, they use the normal unsigned
  binary representation (without the leftmost bit being negative)

An eight-bit integer can be declared in Java using type __byte__:

  - ___byte x;___

C also has type __"unsigned byte"__, which you can use to declare unsigned
eight-bit integers. One Byte is equal to eight bits. An int is 32 bits, or 4 Bytes
