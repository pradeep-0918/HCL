---
type: concept
subject: aptitude
topic: "Binary Numbers"
parent: "01. Number System/Base Systems"
company: HCL
difficulty: medium
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - base-systems
  - binary
  - number-system
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Base Systems]]"
  - "[[Decimal Numbers]]"
  - "[[Number Base Conversion]]"
  - "[[Base-Based Problems]]"
---

# Binary Numbers

## 1. Core Concept

> [!summary] Definition
> A **binary number system** is a number system with **base 2**.
>
> It uses only two digits:
>
> $$
> \boxed{0,\ 1}
> $$
>
> Unlike the decimal system, which uses digits `0–9`, binary uses only `0` and `1`.

The binary system is widely used in:

- computers
- digital electronics
- programming
- data representation
- computer architecture

---

# 2. Decimal vs Binary

| Number System | Base | Digits |
|---|---:|---|
| Binary | `2` | `0, 1` |
| Decimal | `10` | `0–9` |
| Octal | `8` | `0–7` |
| Hexadecimal | `16` | `0–9, A–F` |

The base tells us how many different digits are available.

---

# 3. Binary Place Values

In decimal, place values are powers of `10`.

In binary, place values are powers of `2`.

From right to left:

$$
\boxed{
2^0,\ 2^1,\ 2^2,\ 2^3,\ 2^4,\ldots
}
$$

Therefore:

| Position | Power | Value |
|---|---:|---:|
| Rightmost | \(2^0\) | `1` |
| 2nd | \(2^1\) | `2` |
| 3rd | \(2^2\) | `4` |
| 4th | \(2^3\) | `8` |
| 5th | \(2^4\) | `16` |
| 6th | \(2^5\) | `32` |
| 7th | \(2^6\) | `64` |
| 8th | \(2^7\) | `128` |

---

# 4. Binary Representation

A binary number:

$$
b_nb_{n-1}\ldots b_2b_1b_0
$$

has value:

$$
\boxed{
b_n2^n+b_{n-1}2^{n-1}+\cdots+b_22^2+b_12^1+b_02^0
}
$$

where every:

$$
b_i\in\{0,1\}
$$

---

# 5. Example — Binary to Decimal

Convert:

$$
1011_2
$$

to decimal.

Write place values:

$$
2^3,\ 2^2,\ 2^1,\ 2^0
$$

Therefore:

$$
1011_2
=
1(2^3)+0(2^2)+1(2^1)+1(2^0)
$$

$$
=8+0+2+1
$$

$$
\boxed{11_{10}}
$$

---

# 6. Example — Binary `11001`

Convert:

$$
11001_2
$$

to decimal.

$$
1(2^4)+1(2^3)+0(2^2)+0(2^1)+1(2^0)
$$

$$
=16+8+0+0+1
$$

$$
\boxed{25}
$$

---

# 7. Binary to Decimal Formula

For:

$$
(b_nb_{n-1}\ldots b_0)_2
$$

the decimal value is:

$$
\boxed{
\sum_{i=0}^{n}b_i2^i
}
$$

This is the main conversion formula.

---

# 8. Decimal to Binary

To convert decimal to binary, repeatedly divide the number by `2`.

Record the remainders.

Then read the remainders:

$$
\boxed{\text{from bottom to top}}
$$

---

# 9. Example — Decimal `13` to Binary

Divide repeatedly:

$$
13\div2=6\text{ remainder }1
$$

$$
6\div2=3\text{ remainder }0
$$

$$
3\div2=1\text{ remainder }1
$$

$$
1\div2=0\text{ remainder }1
$$

Read from bottom to top:

$$
\boxed{1101_2}
$$

Therefore:

$$
13_{10}=1101_2
$$

---

# 10. Conversion Table

For decimal `13`:

| Division | Quotient | Remainder |
|---|---:|---:|
| \(13\div2\) | `6` | `1` |
| \(6\div2\) | `3` | `0` |
| \(3\div2\) | `1` | `1` |
| \(1\div2\) | `0` | `1` |

Read remainders upward:

$$
\boxed{1101}
$$

---

# 11. Important Pattern — Powers of 2

Memorize these:

$$
2^0=1
$$

$$
2^1=2
$$

$$
2^2=4
$$

$$
2^3=8
$$

$$
2^4=16
$$

$$
2^5=32
$$

$$
2^6=64
$$

$$
2^7=128
$$

$$
2^8=256
$$

$$
2^9=512
$$

$$
2^{10}=1024
$$

These are very useful for aptitude questions.

---

# 12. Binary Powers Pattern

A binary number consisting of a `1` followed by `n` zeros represents:

$$
\boxed{
2^n
}
$$

Examples:

$$
10_2=2^1=2
$$

$$
100_2=2^2=4
$$

$$
1000_2=2^3=8
$$

$$
10000_2=2^4=16
$$

Therefore:

$$
\boxed{
1\underbrace{00\ldots0}_{n\text{ zeros}}=2^n
}
$$

---

# 13. Binary All-Ones Pattern

A binary number consisting of `n` ones is:

$$
\boxed{
2^n-1
}
$$

### Examples

$$
1_2=1=2^1-1
$$

$$
11_2=3=2^2-1
$$

$$
111_2=7=2^3-1
$$

$$
1111_2=15=2^4-1
$$

Therefore:

$$
\boxed{
\underbrace{111\ldots111}_{n\text{ ones}}
=
2^n-1
}
$$

---

# 14. Example

Convert:

$$
11111_2
$$

to decimal.

Using the shortcut:

$$
2^5-1
$$

$$
=32-1
$$

$$
\boxed{31}
$$

---

# 15. Binary Range With `n` Bits

Using exactly `n` binary bits:

### Minimum

$$
\boxed{0}
$$

### Maximum

$$
\boxed{
2^n-1
}
$$

Therefore:

$$
\boxed{
0\le N\le2^n-1
}
$$

---

# 16. Number of Values With `n` Bits

Each bit has:

$$
2
$$

possibilities:

$$
0\text{ or }1
$$

For `n` bits:

$$
\boxed{
2^n
}
$$

different combinations exist.

### Example

3 bits:

$$
2^3=8
$$

possible values:

$$
000,001,010,011,100,101,110,111
$$

---

# 17. Important Pattern — `n` Bits

> [!important]

For `n` bits:

$$
\boxed{
\text{Number of values}=2^n
}
$$

and:

$$
\boxed{
\text{Maximum value}=2^n-1
}
$$

This is one of the most important binary patterns.

---

# 18. Binary Number and Parity

The last binary digit determines whether a number is even or odd.

### Last digit `0`

$$
\boxed{\text{Even}}
$$

### Last digit `1`

$$
\boxed{\text{Odd}}
$$

Therefore:

> [!important]
> **Binary last bit = parity**

---

# 19. Example

$$
10110_2
$$

ends with:

$$
0
$$

Therefore it is:

$$
\boxed{\text{Even}}
$$

while:

$$
10111_2
$$

ends with:

$$
1
$$

Therefore:

$$
\boxed{\text{Odd}}
$$

---

# 20. Binary Multiplication by 2

Appending a zero to a binary number multiplies it by `2`.

Example:

$$
101_2=5
$$

Append `0`:

$$
1010_2=10
$$

Therefore:

$$
\boxed{
N\times2
}
$$

is represented by shifting the binary number left by one position.

---

# 21. Binary Division by 2

Removing the last binary digit is equivalent to integer division by `2`.

Example:

$$
10110_2
$$

Remove last digit:

$$
1011_2
$$

Decimal:

$$
22\div2=11
$$

Therefore:

$$
\boxed{
\text{Right shift by 1}=\lfloor N/2\rfloor
}
$$

---

# 22. Binary Left Shift

A left shift by one position:

$$
N<<1
$$

means:

$$
\boxed{
N\times2
}
$$

Example:

$$
101_2
$$

left shift:

$$
1010_2
$$

Therefore:

$$
5\times2=10
$$

---

# 23. Binary Right Shift

A right shift by one position:

$$
N>>1
$$

means integer division by `2`:

$$
\boxed{
\lfloor N/2\rfloor
}
$$

Example:

$$
1011_2
$$

right shift:

$$
101_2
$$

Decimal:

$$
11\div2=5
$$

---

# 24. Binary Multiplication by Powers of 2

Appending `k` zeros multiplies by:

$$
\boxed{
2^k
}
$$

Example:

$$
101_2
$$

append two zeros:

$$
10100_2
$$

Original:

$$
5
$$

New:

$$
20
$$

Therefore:

$$
5\times2^2=20
$$

---

# 25. Binary Division by Powers of 2

Removing `k` rightmost bits corresponds to integer division by:

$$
\boxed{
2^k
}
$$

Example:

$$
110100_2
$$

remove two bits:

$$
1101_2
$$

Decimal:

$$
52\div4=13
$$

---

# 26. Binary Addition Rules

Basic binary addition:

| A | B | Sum |
|---|---|---|
| `0` | `0` | `0` |
| `0` | `1` | `1` |
| `1` | `0` | `1` |
| `1` | `1` | `10` |

The important rule:

$$
\boxed{
1+1=10_2
}
$$

---

# 27. Binary Addition With Carry

For:

$$
1+1+1
$$

we get:

$$
11_2
$$

because:

$$
1+1+1=3_{10}=11_2
$$

Therefore:

$$
\boxed{
1+1+1=11_2
}
$$

---

# 28. Example — Binary Addition

Add:

$$
1011_2+0110_2
$$

Decimal values:

$$
1011_2=11
$$

$$
0110_2=6
$$

Therefore:

$$
11+6=17
$$

and:

$$
17=10001_2
$$

Answer:

$$
\boxed{10001_2}
$$

---

# 29. Binary Subtraction Rules

Basic rules:

| A | B | Result |
|---|---|---|
| `0` | `0` | `0` |
| `1` | `0` | `1` |
| `1` | `1` | `0` |
| `0` | `1` | Borrow |

The important case is:

$$
\boxed{
0-1
}
$$

which requires borrowing from the next position.

---

# 30. Binary Multiplication Rules

Binary multiplication is very simple:

$$
0\times0=0
$$

$$
0\times1=0
$$

$$
1\times0=0
$$

$$
1\times1=1
$$

Therefore:

$$
\boxed{
1\times1=1
}
$$

---

# 31. Binary and Decimal Conversion — Quick Method

For binary to decimal:

> **Multiply each bit by its power of `2` and add.**

For decimal to binary:

> **Repeatedly divide by `2` and read remainders upward.**

---

# 32. Example — `101101₂`

Convert to decimal:

$$
1(2^5)+0(2^4)+1(2^3)+1(2^2)+0(2^1)+1(2^0)
$$

$$
=32+0+8+4+0+1
$$

$$
\boxed{45}
$$

Therefore:

$$
101101_2=45_{10}
$$

---

# 33. Example — Decimal `45` to Binary

Divide by `2`:

$$
45\div2=22\ R1
$$

$$
22\div2=11\ R0
$$

$$
11\div2=5\ R1
$$

$$
5\div2=2\ R1
$$

$$
2\div2=1\ R0
$$

$$
1\div2=0\ R1
$$

Read upward:

$$
\boxed{101101_2}
$$

---

# 34. Binary to Decimal Using Set Bits

If only a few bits are `1`, add only those powers.

Example:

$$
10010101_2
$$

Set bits are at:

$$
2^7,\ 2^4,\ 2^2,\ 2^0
$$

Therefore:

$$
128+16+4+1
$$

$$
\boxed{149}
$$

This is faster than writing every term.

---

# 35. Important Pattern — Set Bits

A bit equal to `1` contributes its corresponding power of `2`.

A bit equal to `0` contributes nothing.

Therefore:

$$
\boxed{
\text{Decimal value}=\text{sum of powers of 2 at set-bit positions}
}
$$

---

# 36. Binary Representation of Decimal Powers

Important values:

| Decimal | Binary |
|---:|---:|
| `1` | `1` |
| `2` | `10` |
| `4` | `100` |
| `8` | `1000` |
| `16` | `10000` |
| `32` | `100000` |
| `64` | `1000000` |
| `128` | `10000000` |

These are powers of `2`.

---

# 37. Binary and Odd/Even Pattern

A binary number is:

### Even

if:

$$
\boxed{\text{last bit}=0}
$$

### Odd

if:

$$
\boxed{\text{last bit}=1}
$$

This is directly related to:

$$
N\bmod2
$$

---

# 38. Binary Remainder by 2

For any binary number:

$$
\boxed{
N\bmod2=\text{last bit}
}
$$

Example:

$$
110101_2
$$

last bit:

$$
1
$$

Therefore:

$$
110101_2\bmod2=1
$$

---

# 39. Binary Remainder by 4

The last two bits determine the remainder modulo `4`.

Why?

Because:

$$
2^2=4
$$

Therefore:

$$
\boxed{
N\bmod4
}
$$

depends only on the last two binary bits.

Example:

$$
110110_2
$$

last two bits:

$$
10_2=2
$$

Therefore:

$$
\boxed{
N\bmod4=2
}
$$

---

# 40. Binary Remainder by 8

Similarly, the last three bits determine the remainder modulo `8`.

$$
\boxed{
N\bmod8
}
$$

depends only on the last three bits.

Example:

$$
101101_2
$$

last three bits:

$$
101_2=5
$$

Therefore:

$$
\boxed{
N\bmod8=5
}
$$

---

# 41. Important Pattern — Powers of 2

For modulus:

$$
2^k
$$

only the last `k` binary bits matter.

Therefore:

$$
\boxed{
N\bmod2^k
=
\text{value of last }k\text{ bits}
}
$$

This is extremely useful.

---

# 42. Binary Number of Digits

For a positive integer `N`, the number of binary digits is:

$$
\boxed{
\lfloor\log_2N\rfloor+1
}
$$

This is the binary equivalent of the decimal digit formula.

---

# 43. Example

Find the number of binary digits in:

$$
25
$$

Since:

$$
2^4=16
$$

and:

$$
2^5=32
$$

we have:

$$
16\le25<32
$$

Therefore:

$$
\boxed5
$$

binary digits.

Indeed:

$$
25=11001_2
$$

---

# 44. Binary Range With `n` Digits

An `n`-digit binary number has:

$$
\boxed{
2^{n-1}\le N\le2^n-1
}
$$

### Example

A 5-bit positive number ranges from:

$$
2^4=16
$$

to:

$$
2^5-1=31
$$

Therefore:

$$
\boxed{16\le N\le31}
$$

---

# 45. Number of Positive `n`-Bit Numbers

If leading zero is not allowed, the number of positive `n`-bit binary numbers is:

$$
\boxed{
2^{n-1}
}
$$

### Example

3-bit positive binary numbers:

$$
100,101,110,111
$$

There are:

$$
\boxed4=2^{3-1}
$$

---

# 46. Important Distinction — Exactly `n` Bits

If leading zeros are allowed, there are:

$$
\boxed{
2^n
}
$$

possible binary strings of length `n`.

If the first bit must be `1`, there are:

$$
\boxed{
2^{n-1}
}
$$

positive `n`-bit numbers.

---

# 47. Binary Complement

For a fixed number of bits, changing:

$$
0\leftrightarrow1
$$

is called taking the **bitwise complement**.

Example:

$$
10110
$$

complement:

$$
01001
$$

Therefore:

$$
\boxed{
0\leftrightarrow1
}
$$

---

# 48. One's Complement

The **one's complement** of a binary number is obtained by flipping every bit.

$$
0\rightarrow1
$$

$$
1\rightarrow0
$$

Example:

$$
10101
$$

becomes:

$$
\boxed{01010}
$$

---

# 49. Two's Complement

Two's complement is obtained by:

1. Find one's complement.
2. Add `1`.

Example:

$$
0101
$$

One's complement:

$$
1010
$$

Add `1`:

$$
1011
$$

Therefore:

$$
\boxed{1011}
$$

is the 4-bit two's complement of `0101`.

> [!note]
> Two's complement is mainly a computer representation of signed integers, but basic aptitude questions may test the procedure.

---

# 50. Binary Base Representation

Binary can be written using:

$$
\boxed{(N)_2}
$$

Decimal:

$$
\boxed{(N)_{10}}
$$

Example:

$$
(1011)_2=(11)_{10}
$$

The subscript tells you the base.

---

# 51. General Base Formula

For a number:

$$
(a_na_{n-1}\ldots a_1a_0)_b
$$

its decimal value is:

$$
\boxed{
\sum_{i=0}^{n}a_i b^i
}
$$

For binary:

$$
b=2
$$

For decimal:

$$
b=10
$$

---

# 52. Binary Base Rule

In base `2`, every digit must satisfy:

$$
\boxed{
0\le d<2
}
$$

Therefore only:

$$
\boxed{0,1}
$$

are valid.

Numbers such as:

$$
102_2
$$

are invalid because binary cannot contain digit `2`.

---

# 53. Common Trap — Invalid Binary Number

The following is valid:

$$
101101_2
$$

The following is invalid:

$$
102101_2
$$

because:

$$
2
$$

is not a binary digit.

---

# 54. Binary Addition Shortcut

Remember:

$$
1+1=10_2
$$

$$
1+1+1=11_2
$$

These are the only carry cases you usually need.

---

# 55. Binary Multiplication by 2

Appending zero:

$$
1011\rightarrow10110
$$

means:

$$
11\times2=22
$$

Therefore:

$$
\boxed{
N<<1=2N
}
$$

---

# 56. Binary Division by 2

Removing the last bit:

$$
10110\rightarrow1011
$$

means:

$$
22\div2=11
$$

Therefore:

$$
\boxed{
N>>1=\lfloor N/2\rfloor
}
$$

---

# 57. Important Pattern — Binary and Powers of 2

If:

$$
N=2^k
$$

then binary representation is:

$$
\boxed{
1\underbrace{00\ldots0}_{k\text{ zeros}}
}
$$

Example:

$$
32=2^5
$$

so:

$$
\boxed{32=100000_2}
$$

---

# 58. Important Pattern — One Less Than a Power of 2

If:

$$
N=2^k-1
$$

then binary representation consists of `k` ones:

$$
\boxed{
111\ldots111
}
$$

Example:

$$
31=2^5-1
$$

therefore:

$$
\boxed{31=11111_2}
$$

---

# 59. Common Aptitude Question

### Question

What is the maximum value represented by 8 bits?

Use:

$$
2^8-1
$$

$$
=256-1
$$

$$
\boxed{255}
$$

---

# 60. Common Aptitude Question

### Question

How many different values can be represented using 6 bits?

Each bit has two possibilities:

$$
2^6
$$

Therefore:

$$
\boxed{64}
$$

---

# 61. Common Aptitude Question

### Question

What is the minimum number of bits required to represent `100`?

Find:

$$
2^6=64
$$

$$
2^7=128
$$

Since:

$$
64\le100<128
$$

we need:

$$
\boxed7
$$

bits.

---

# 62. Minimum Bits Formula

For a positive integer `N`:

$$
\boxed{
\lfloor\log_2N\rfloor+1
}
$$

bits are required.

Equivalent pattern:

> Find the smallest `k` such that:

$$
\boxed{
2^k>N
}
$$

---

# 63. Example

Minimum bits required for `255`:

$$
2^8-1=255
$$

Therefore:

$$
\boxed8
$$

bits.

For `256`:

$$
2^8=256
$$

so it requires:

$$
\boxed9
$$

bits.

This boundary is a common trap.

---

# 64. Binary Conversion Shortcut

For small numbers, memorize:

| Decimal | Binary |
|---:|---:|
| `0` | `0` |
| `1` | `1` |
| `2` | `10` |
| `3` | `11` |
| `4` | `100` |
| `5` | `101` |
| `6` | `110` |
| `7` | `111` |
| `8` | `1000` |
| `9` | `1001` |
| `10` | `1010` |
| `11` | `1011` |
| `12` | `1100` |
| `13` | `1101 |
| `14` | `1110` |
| `15` | `1111` |
| `16` | `10000` |

---

# 65. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Using powers of `10` for binary place values.
- ❌ Reading decimal-to-binary remainders from top to bottom.
- ❌ Forgetting that binary digits are only `0` and `1`.
- ❌ Thinking `10₂` means decimal ten.
- ❌ Forgetting that `10₂ = 2₁₀`.
- ❌ Confusing number of bits with number of values.
- ❌ Forgetting the maximum `n`-bit value is `2^n-1`.
- ❌ Using `2^n` as the maximum value instead of the number of possible values.
- ❌ Forgetting that the last bit determines parity.
- ❌ Forgetting that leading zeros can be used when a fixed bit-width is specified.

---

# 66. Formula Sheet

> [!important] Must Remember

### Binary to Decimal

$$
\boxed{
N=\sum_{i=0}^{n}b_i2^i
}
$$

### Decimal to Binary

$$
\boxed{
\text{Repeated division by }2
}
$$

Read remainders:

$$
\boxed{\text{bottom}\rightarrow\text{top}}
$$

### `n` Bits — Number of Values

$$
\boxed{
2^n
}
$$

### Maximum `n`-Bit Value

$$
\boxed{
2^n-1
}
$$

### Minimum Positive `n`-Bit Value

$$
\boxed{
2^{n-1}
}
$$

### Binary Digits of `N`

$$
\boxed{
\lfloor\log_2N\rfloor+1
}
$$

### Binary Number With `n` Ones

$$
\boxed{
2^n-1
}
$$

### Binary `1` Followed by `n` Zeros

$$
\boxed{
2^n
}
$$

### Left Shift

$$
\boxed{
N<<k=N\times2^k
}
$$

### Right Shift

$$
\boxed{
N>>k=\left\lfloor\frac{N}{2^k}\right\rfloor
}
$$

---

# 67. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Binary Place Values

$$
\boxed{
1,2,4,8,16,32,64,\ldots
}
$$

### Pattern 2 — `n` Bits

$$
\boxed{
2^n\text{ possible values}
}
$$

### Pattern 3 — Maximum

$$
\boxed{
2^n-1
}
$$

### Pattern 4 — Power of 2

$$
\boxed{
2^n=100\ldots0_2
}
$$

### Pattern 5 — One Less Than Power of 2

$$
\boxed{
2^n-1=111\ldots1_2
}
$$

### Pattern 6 — Parity

$$
\boxed{
\text{Last bit}=0\Rightarrow\text{even}
}
$$

$$
\boxed{
\text{Last bit}=1\Rightarrow\text{odd}
}
$$

### Pattern 7 — Modulo `2^k`

$$
\boxed{
\text{Last }k\text{ bits determine }N\bmod2^k
}
$$

### Pattern 8 — Left Shift

$$
\boxed{
<<k\Rightarrow\times2^k
}
$$

### Pattern 9 — Right Shift

$$
\boxed{
>>k\Rightarrow\div2^k
}
$$

### Pattern 10 — Minimum Bits

$$
\boxed{
\lfloor\log_2N\rfloor+1
}
$$

---

# 68. HCL Preparation Priority

**Priority:** 🔥🔥 High

For aptitude, focus especially on:

1. Binary-to-decimal conversion
2. Decimal-to-binary conversion
3. Powers of `2`
4. `n`-bit range
5. Maximum value
6. Number of possible values
7. Minimum bits required
8. Binary parity
9. Binary shifts
10. Remainder using last bits
11. Binary addition
12. Basic complements

---

# 69. Practice Checklist

- [ ] Binary place values
- [ ] Binary → decimal
- [ ] Decimal → binary
- [ ] Powers of `2`
- [ ] All-ones binary numbers
- [ ] `n`-bit maximum
- [ ] `n`-bit possible values
- [ ] Minimum bits
- [ ] Binary parity
- [ ] Binary addition
- [ ] Binary subtraction
- [ ] Binary multiplication
- [ ] Left shift
- [ ] Right shift
- [ ] Binary remainder
- [ ] One's complement
- [ ] Two's complement
- [ ] Binary-based aptitude problems

---

# 70. Related Topics

- [[Base Systems]]
- [[Decimal Numbers]]
- [[Number Base Conversion]]
- [[Base-Based Problems]]
- [[Number Formation]]
- [[Remainders]]
- [[Unit Digit]]
- [[Bit Manipulation]]

---

# 71. Quick Revision

> [!summary] One-Minute Revision

### Binary Base

$$
\boxed{
\text{Base}=2
}
$$

Digits:

$$
\boxed{0,1}
$$

### Place Values

$$
\boxed{
1,2,4,8,16,32,\ldots
}
$$

### Binary → Decimal

$$
\boxed{
\sum b_i2^i
}
$$

### `n` Bits

$$
\boxed{
2^n\text{ values}
}
$$

### Maximum

$$
\boxed{
2^n-1
}
$$

### Power of 2

$$
\boxed{
2^n=1\underbrace{00\ldots0}_{n}
}
$$

### All Ones

$$
\boxed{
2^n-1=\underbrace{11\ldots1}_{n}
}
$$

### Even / Odd

$$
\boxed{
\text{Last bit }0=\text{even}
}
$$

$$
\boxed{
\text{Last bit }1=\text{odd}
}
$$

### Shift

$$
\boxed{
N<<k=N\times2^k
}
$$

$$
\boxed{
N>>k=\left\lfloor N/2^k\right\rfloor
}
$$

### Golden Memory Trick

> **Binary → powers of `2`. Every `1` means "include that power"; every `0` means "skip it".**

### One-Line Recognition

> **Binary question → think `base 2`, powers of `2`, last bit, and `2^n - 1`.**