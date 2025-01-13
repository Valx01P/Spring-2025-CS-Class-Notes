#### 1.1 Introduction
Computer words are composed of bits; thus, words
can be represented as binary numbers. Integers can
be represented either in decimal or binary form,
but what about the other numbers the commonly
occur? For example:

- What about fractions and other real numbers?
- What happens if an operation creates a number
bigger than can be represented?
- And underlying these questions is a mystery: How
does hardware really multiply or divide numbers?

The goal of this chapter is to unravel these
mysteries including representation of real numbers,
arithmetic algorithms, hardware that follows these
algorithms, and the implications of all this for
instruction sets. These insights may explain quirks
that you have already encountered with computers.
Moreover, we show how to use this knowledge to make
arithmetic-intensive programs go much faster.

___________________________________

1) Integers can be represented as bits.
- [x] True
- [ ] False

2) Instructions can be represented as bits.
- [x] True
- [ ] False

___________________________________

#### Explanation Q1, True
- Information is kept in computer hardware as a
series of high and low electronic signals, so a
base 2 representation is a natural way to represent
integers. Ex. \(12_{10} \text{ can be represented as } 1100_{2}\)
#### Explanation Q2, True
- The binary language that a machine understands
is called machine language. An assembler converts
a symbolic version of an instruction into the
binary version. Ex. `add $t0, $s1, $s2` becomes
`00000010001100100100000000100000`