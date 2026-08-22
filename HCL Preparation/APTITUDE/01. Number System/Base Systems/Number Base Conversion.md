---
type: concept
subject: aptitude
topic: "Number Base Conversion"
parent: "01. Number System/Base Systems"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - base-systems
  - number-base-conversion
  - binary
  - decimal
  - octal
  - hexadecimal
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Base Systems]]"
  - "[[Binary Numbers]]"
  - "[[Decimal Numbers]]"
  - "[[Base-Based Problems]]"
---

# Number Base Conversion

## 1. Core Concept

> [!summary] Definition
> **Number base conversion** means representing the same numerical value in different number systems.
>
> Common bases:
>
> - Binary → Base `2`
> - Decimal → Base `10`
> - Octal → Base `8`
> - Hexadecimal → Base `16`

The value remains the same; only its representation changes.

Example:

$$
13_{10}=1101_2
$$

The value is the same:

$$
\boxed{13}
$$

---

# 2. Common Number Systems

| System | Base | Valid Digits |
|---|---:|---|
| Binary | `2` | `0, 1` |
| Octal | `8` | `0–7` |
| Decimal | `10` | `0–9` |
| Hexadecimal | `16` | `0–9, A–F` |

For hexadecimal:

$$
A=10
$$

$$
B=11
$$

$$
C=12
$$

$$
D=13
$$

$$
E=14
$$

$$
F=15
$$

---

# 3. General Base Representation

For a number:

$$
(d_nd_{n-1}\ldots d_1d_0)_b
$$

its decimal value is:

$$
\boxed{
d_n b^n+d_{n-1}b^{n-1}+\cdots+d_1b+d_0
}
$$

or:

$$
\boxed{
\sum_{i=0}^{n}d_i b^i
}
$$

This is the most important general formula.

---

# 4. Valid Digit Rule

For base `b`, every digit must satisfy:

$$
\boxed{
0\le d<b
}
$$

### Examples

Binary:

$$
0\le d<2
$$

so only:

$$
0,1
$$

are allowed.

Octal:

$$
0\le d<8
$$

so:

$$
0,1,2,3,4,5,6,7
$$

are allowed.

Hexadecimal:

$$
0\le d<16
$$

so:

$$
0-9,A-F
$$

are allowed.

---

# 5. Base `b` to Decimal

To convert from base `b` to decimal:

> **Multiply every digit by the corresponding power of the base and add.**

Formula:

$$
\boxed{
N_{10}=\sum d_i b^i
}
$$

---

# 6. Binary to Decimal

For binary:

$$
b=2
$$

Therefore:

$$
\boxed{
N_{10}=\sum d_i2^i
}
$$

### Example

Convert:

$$
1011_2
$$

to decimal.

$$
1(2^3)+0(2^2)+1(2^1)+1(2^0)
$$

$$
=8+0+2+1
$$

$$
\boxed{11_{10}}
$$

---

# 7. Octal to Decimal

For octal:

$$
b=8
$$

### Example

Convert:

$$
347_8
$$

to decimal.

$$
3(8^2)+4(8^1)+7(8^0)
$$

$$
=3(64)+4(8)+7
$$

$$
=192+32+7
$$

$$
\boxed{231_{10}}
$$

---

# 8. Hexadecimal to Decimal

For hexadecimal:

$$
b=16
$$

### Example

Convert:

$$
2A_{16}
$$

to decimal.

Since:

$$
A=10
$$

we get:

$$
2(16)+10
$$

$$
=32+10
$$

$$
\boxed{42_{10}}
$$

---

# 9. Decimal to Another Base

To convert a decimal integer to base `b`:

1. Divide by `b`.
2. Record the remainder.
3. Divide the quotient by `b`.
4. Continue until quotient becomes `0`.
5. Read the remainders from bottom to top.

Therefore:

$$
\boxed{
\text{Decimal}\rightarrow\text{Base }b:
\text{Repeated division by }b
}
$$

---

# 10. Decimal to Binary

Convert:

$$
25_{10}
$$

to binary.

$$
25\div2=12\ R1
$$

$$
12\div2=6\ R0
$$

$$
6\div2=3\ R0
$$

$$
3\div2=1\ R1
$$

$$
1\div2=0\ R1
$$

Read remainders upward:

$$
\boxed{11001_2}
$$

Therefore:

$$
\boxed{25_{10}=11001_2}
$$

---

# 11. Decimal to Octal

Convert:

$$
83_{10}
$$

to octal.

$$
83\div8=10\ R3
$$

$$
10\div8=1\ R2
$$

$$
1\div8=0\ R1
$$

Read upward:

$$
\boxed{123_8}
$$

Therefore:

$$
\boxed{83_{10}=123_8}
$$

---

# 12. Decimal to Hexadecimal

Convert:

$$
254_{10}
$$

to hexadecimal.

$$
254\div16=15\ R14
$$

`14 = E`.

Then:

$$
15\div16=0\ R15
$$

`15 = F`.

Read upward:

$$
\boxed{FE_{16}}
$$

Therefore:

$$
\boxed{254_{10}=FE_{16}}
$$

---

# 13. Important Conversion Direction

> [!important]

### Any Base → Decimal

Use:

$$
\boxed{
\text{Place-value expansion}
}
$$

### Decimal → Any Base

Use:

$$
\boxed{
\text{Repeated division}
}
$$

Memorize this distinction.

---

# 14. Binary to Octal

Binary and octal have a special relationship:

$$
8=2^3
$$

Therefore:

> **Group binary digits in sets of 3 from the right.**

Then convert each group to one octal digit.

---

# 15. Binary to Octal Example

Convert:

$$
110101_2
$$

Group from right:

$$
110\quad101
$$

Convert each group:

$$
110_2=6
$$

$$
101_2=5
$$

Therefore:

$$
\boxed{65_8}
$$

---

# 16. Binary to Octal With Padding

Suppose:

$$
10111_2
$$

Group from right:

$$
10\quad111
$$

Pad the left group with zero:

$$
010\quad111
$$

Now:

$$
010_2=2
$$

$$
111_2=7
$$

Therefore:

$$
\boxed{27_8}
$$

---

# 17. Octal to Binary

Each octal digit corresponds to exactly **3 binary bits**.

Memorize:

| Octal | Binary |
|---:|---:|
| `0` | `000` |
| `1` | `001` |
| `2` | `010` |
| `3` | `011` |
| `4` | `100` |
| `5` | `101` |
| `6` | `110` |
| `7` | `111` |

---

# 18. Example — Octal to Binary

Convert:

$$
57_8
$$

Convert each digit:

$$
5=101
$$

$$
7=111
$$

Therefore:

$$
\boxed{57_8=101111_2}
$$

---

# 19. Binary to Hexadecimal

Binary and hexadecimal have a special relationship:

$$
16=2^4
$$

Therefore:

> **Group binary digits in sets of 4 from the right.**

Then convert each group to one hexadecimal digit.

---

# 20. Binary to Hexadecimal Example

Convert:

$$
10101111_2
$$

Group:

$$
1010\quad1111
$$

Now:

$$
1010_2=10=A
$$

$$
1111_2=15=F
$$

Therefore:

$$
\boxed{AF_{16}}
$$

---

# 21. Binary to Hexadecimal With Padding

Convert:

$$
101101_2
$$

Group from right:

$$
10\quad1101
$$

Pad:

$$
0010\quad1101
$$

Now:

$$
0010_2=2
$$

$$
1101_2=D
$$

Therefore:

$$
\boxed{2D_{16}}
$$

---

# 22. Hexadecimal to Binary

Each hexadecimal digit corresponds to exactly **4 binary bits**.

| Hex | Binary |
|---:|---:|
| `0` | `0000` |
| `1` | `0001` |
| `2` | `0010` |
| `3` | `0011` |
| `4` | `0100` |
| `5` | `0101` |
| `6` | `0110` |
| `7` | `0111` |
| `8` | `1000` |
| `9` | `1001` |
| `A` | `1010` |
| `B` | `1011` |
| `C` | `1100` |
| `D` | `1101` |
| `E` | `1110` |
| `F` | `1111` |

---

# 23. Example — Hexadecimal to Binary

Convert:

$$
3F_{16}
$$

Convert each digit:

$$
3=0011
$$

$$
F=1111
$$

Therefore:

$$
\boxed{3F_{16}=00111111_2}
$$

Ignoring leading zeros:

$$
\boxed{111111_2}
$$

---

# 24. Octal to Hexadecimal

There is no direct simple grouping rule between octal and hexadecimal.

The easiest method is:

$$
\boxed{
\text{Octal}\rightarrow\text{Binary}\rightarrow\text{Hexadecimal}
}
$$

or:

$$
\boxed{
\text{Octal}\rightarrow\text{Decimal}\rightarrow\text{Hexadecimal}
}
$$

Binary is usually faster.

---

# 25. Example — Octal to Hexadecimal

Convert:

$$
73_8
$$

First convert octal to binary:

$$
7=111
$$

$$
3=011
$$

Therefore:

$$
73_8=111011_2
$$

Group into four:

$$
0011\quad1011
$$

Therefore:

$$
0011=3
$$

$$
1011=B
$$

Answer:

$$
\boxed{3B_{16}}
$$

---

# 26. Hexadecimal to Octal

Similarly:

$$
\boxed{
\text{Hexadecimal}\rightarrow\text{Binary}\rightarrow\text{Octal}
}
$$

### Example

Convert:

$$
2D_{16}
$$

Hex to binary:

$$
2=0010
$$

$$
D=1101
$$

Therefore:

$$
00101101_2
$$

Group into 3 from right:

$$
00\quad101\quad101
$$

Pad:

$$
000\quad101\quad101
$$

Therefore:

$$
0,\ 5,\ 5
$$

Ignore leading zero:

$$
\boxed{55_8}
$$

---

# 27. Conversion Shortcut Table

| Conversion | Best Method |
|---|---|
| Binary → Decimal | Powers of `2` |
| Decimal → Binary | Divide by `2` |
| Octal → Decimal | Powers of `8` |
| Decimal → Octal | Divide by `8` |
| Hex → Decimal | Powers of `16` |
| Decimal → Hex | Divide by `16` |
| Binary → Octal | Group `3` bits |
| Octal → Binary | Each digit → `3` bits |
| Binary → Hex | Group `4` bits |
| Hex → Binary | Each digit → `4` bits |
| Octal → Hex | Binary bridge |
| Hex → Octal | Binary bridge |

---

# 28. Binary Grouping Rule

> [!important]

Since:

$$
8=2^3
$$

use groups of:

$$
\boxed3\text{ bits}
$$

for octal.

Since:

$$
16=2^4
$$

use groups of:

$$
\boxed4\text{ bits}
$$

for hexadecimal.

---

# 29. General Base Conversion Through Decimal

For any conversion:

$$
A_b\rightarrow C_c
$$

you can always use:

$$
\boxed{
A_b\rightarrow A_{10}\rightarrow A_c
}
$$

This is the universal method.

---

# 30. Example

Convert:

$$
1011_2
$$

to octal.

### Step 1 — Binary to Decimal

$$
1011_2=11_{10}
$$

### Step 2 — Decimal to Octal

$$
11\div8=1\ R3
$$

$$
1\div8=0\ R1
$$

Therefore:

$$
\boxed{13_8}
$$

---

# 31. Faster Binary to Octal

Instead of going through decimal:

$$
1011_2
$$

Pad:

$$
001\quad011
$$

Then:

$$
001=1
$$

$$
011=3
$$

Therefore:

$$
\boxed{13_8}
$$

Much faster.

---

# 32. Faster Binary to Hexadecimal

Convert:

$$
11101110_2
$$

Group:

$$
1110\quad1110
$$

Each group:

$$
1110=E
$$

Therefore:

$$
\boxed{EE_{16}}
$$

---

# 33. Base Conversion With Fractions

For numbers containing a fractional part, the method differs.

Example:

$$
0.101_2
$$

To convert the binary fraction to decimal:

$$
0(2^{-1})+1(2^{-2})+0(2^{-3})+1(2^{-4})
$$

More generally:

$$
\boxed{
(d_{-1}d_{-2}\ldots)_b
=
\sum_{k=1}^{\infty}d_{-k}b^{-k}
}
$$

---

# 34. Example — Binary Fraction

Convert:

$$
0.101_2
$$

to decimal.

$$
1(2^{-1})+0(2^{-2})+1(2^{-3})
$$

$$
=\frac12+\frac18
$$

$$
=\frac58
$$

Therefore:

$$
\boxed{0.101_2=0.625_{10}}
$$

---

# 35. Decimal Fraction to Binary

For the fractional part, repeatedly multiply by `2`.

Record the integer part each time.

Then read those integer parts from top to bottom.

---

# 36. Example — `0.625` to Binary

Start:

$$
0.625\times2=1.25
$$

Record:

$$
1
$$

Remaining fraction:

$$
0.25
$$

Next:

$$
0.25\times2=0.5
$$

Record:

$$
0
$$

Next:

$$
0.5\times2=1.0
$$

Record:

$$
1
$$

Therefore:

$$
\boxed{0.625_{10}=0.101_2}
$$

---

# 37. Important Fraction Conversion Rule

### Integer part

Use:

$$
\boxed{\text{Repeated division}}
$$

### Fractional part

Use:

$$
\boxed{\text{Repeated multiplication}}
$$

This distinction is very important.

---

# 38. Mixed Number Conversion

For:

$$
13.625_{10}
$$

convert integer and fractional parts separately.

### Integer

$$
13_{10}=1101_2
$$

### Fraction

$$
0.625_{10}=0.101_2
$$

Therefore:

$$
\boxed{
13.625_{10}=1101.101_2
}
$$

---

# 39. Important Pattern — Base `b` Fraction

For a fractional decimal value converted to base `b`:

1. Multiply fractional part by `b`.
2. Record the integer part.
3. Continue with the new fractional part.
4. Stop when fraction becomes zero or the desired precision is reached.

Therefore:

$$
\boxed{
\text{Fractional conversion}\rightarrow\text{Repeated multiplication by base}
}
$$

---

# 40. Base Conversion Verification

After converting, always convert the result back if accuracy matters.

Example:

$$
25_{10}=11001_2
$$

Check:

$$
1(16)+1(8)+0(4)+0(2)+1
$$

$$
=25
$$

Therefore the conversion is correct.

---

# 41. Important Pattern — Same Value

Different representations can represent the same value:

$$
\boxed{
10_{10}=1010_2=12_8=A_{16}
}
$$

All represent:

$$
10
$$

---

# 42. Base Arithmetic

Arithmetic can be performed directly in any base.

The carry occurs when the sum reaches the base.

### Decimal

$$
9+1=10_{10}
$$

### Binary

$$
1+1=10_2
$$

### Octal

$$
7+1=10_8
$$

### Hexadecimal

$$
F+1=10_{16}
$$

Therefore:

> [!important]
> **Carry occurs when the value reaches the base.**

---

# 43. General Carry Rule

In base `b`:

$$
\boxed{
b=10_b
}
$$

So:

$$
b-1+1=10_b
$$

Examples:

$$
1+1=10_2
$$

$$
7+1=10_8
$$

$$
9+1=10_{10}
$$

$$
F+1=10_{16}
$$

---

# 44. Base Arithmetic — Example

Add in binary:

$$
101_2+11_2
$$

Align:

$$
101
$$

$$
011
$$

Result:

$$
1000_2
$$

Decimal check:

$$
5+3=8
$$

and:

$$
8=1000_2
$$

---

# 45. Base `b` Place Value

In any base:

$$
\boxed{
\text{Rightmost place}=b^0
}
$$

Then moving left:

$$
b^1,\ b^2,\ b^3,\ldots
$$

Moving right after decimal:

$$
b^{-1},\ b^{-2},\ b^{-3},\ldots
$$

---

# 46. Number of Digits in Base `b`

For a positive integer `N`, the number of digits when represented in base `b` is:

$$
\boxed{
\lfloor\log_bN\rfloor+1
}
$$

### Example

How many binary digits does `25` have?

$$
\lfloor\log_2 25\rfloor+1
$$

Since:

$$
2^4<25<2^5
$$

answer:

$$
\boxed5
$$

---

# 47. `n`-Digit Numbers in Base `b`

The smallest positive `n`-digit number is:

$$
\boxed{
b^{n-1}
}
$$

The largest is:

$$
\boxed{
b^n-1
}
$$

Therefore:

$$
\boxed{
b^{n-1}\le N\le b^n-1
}
$$

---

# 48. Number of `n`-Digit Numbers in Base `b`

The number of positive `n`-digit numbers is:

$$
(b^n-1)-(b^{n-1}-1)
$$

Therefore:

$$
\boxed{
(b-1)b^{n-1}
}
$$

### Decimal

$$
(10-1)10^{n-1}
=
9\times10^{n-1}
$$

### Binary

$$
(2-1)2^{n-1}
=
2^{n-1}
$$

---

# 49. Important Pattern — Maximum `n`-Digit Number

In base `b`:

$$
\boxed{
b^n-1
}
$$

is the maximum `n`-digit number.

Examples:

### Binary

$$
2^4-1=15
$$

$$
1111_2
$$

### Octal

$$
8^3-1=511
$$

$$
777_8
$$

### Decimal

$$
10^3-1=999
$$

### Hexadecimal

$$
16^2-1=255
$$

$$
FF_{16}
$$

---

# 50. Important Pattern — All Maximum Digits

The maximum digit in base `b` is:

$$
\boxed{b-1}
$$

Therefore an `n`-digit number consisting entirely of maximum digits represents:

$$
\boxed{
b^n-1
}
$$

Examples:

$$
1111_2=2^4-1
$$

$$
777_8=8^3-1
$$

$$
999_10=10^3-1
$$

$$
FFF_{16}=16^3-1
$$

---

# 51. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Using the wrong base for place values.
- ❌ Reading decimal-to-base remainders in the wrong direction.
- ❌ Forgetting that valid digits must be less than the base.
- ❌ Grouping binary into 4 bits for octal.
- ❌ Grouping binary into 3 bits for hexadecimal.
- ❌ Forgetting to pad binary groups on the left.
- ❌ Removing meaningful zeros inside a number.
- ❌ Confusing hexadecimal `A` with decimal `10` without considering the base.
- ❌ Using repeated division for the fractional part.
- ❌ Forgetting repeated multiplication for fractional conversion.
- ❌ Confusing number of possible values with maximum value.

---

# 52. Formula Sheet

> [!important] Must Remember

### Base to Decimal

$$
\boxed{
N_{10}=\sum d_i b^i
}
$$

### Decimal to Base

$$
\boxed{
\text{Repeated division by }b
}
$$

### Fractional Decimal to Base

$$
\boxed{
\text{Repeated multiplication by }b
}
$$

### Binary → Octal

$$
\boxed{
3\text{-bit groups}
}
$$

### Binary → Hexadecimal

$$
\boxed{
4\text{-bit groups}
}
$$

### Digits in Base `b`

$$
\boxed{
\lfloor\log_bN\rfloor+1
}
$$

### `n`-Digit Range in Base `b`

$$
\boxed{
b^{n-1}\le N\le b^n-1
}
$$

### Number of `n`-Digit Numbers

$$
\boxed{
(b-1)b^{n-1}
}
$$

### Maximum `n`-Digit Number

$$
\boxed{
b^n-1
}
$$

---

# 53. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Any Base to Decimal

$$
\boxed{
\text{Digit}\times\text{Base}^{\text{position}}
}
$$

### Pattern 2 — Decimal to Any Base

$$
\boxed{
\text{Repeated division by base}
}
$$

### Pattern 3 — Binary to Octal

$$
\boxed{
3\text{ bits}=1\text{ octal digit}
}
$$

### Pattern 4 — Binary to Hexadecimal

$$
\boxed{
4\text{ bits}=1\text{ hexadecimal digit}
}
$$

### Pattern 5 — Octal to Binary

$$
\boxed{
1\text{ octal digit}=3\text{ bits}
}
$$

### Pattern 6 — Hexadecimal to Binary

$$
\boxed{
1\text{ hex digit}=4\text{ bits}
}
$$

### Pattern 7 — Base `b` Maximum

$$
\boxed{
b^n-1
}
$$

### Pattern 8 — Base `b` Digit Count

$$
\boxed{
\lfloor\log_bN\rfloor+1
}
$$

### Pattern 9 — Valid Digit

$$
\boxed{
0\le d<b
}
$$

### Pattern 10 — Fraction Conversion

$$
\boxed{
\text{Multiply fractional part by base}
}
$$

---

# 54. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Very High

Master these first:

1. Binary ↔ Decimal
2. Decimal ↔ Binary
3. Binary ↔ Octal
4. Binary ↔ Hexadecimal
5. Octal ↔ Decimal
6. Hexadecimal ↔ Decimal
7. Octal ↔ Hexadecimal
8. Base validity
9. Base-place values
10. Number of digits in a base
11. Maximum value in a base
12. Base arithmetic
13. Fractional base conversion

---

# 55. Practice Checklist

- [ ] Binary → Decimal
- [ ] Decimal → Binary
- [ ] Octal → Decimal
- [ ] Decimal → Octal
- [ ] Hexadecimal → Decimal
- [ ] Decimal → Hexadecimal
- [ ] Binary → Octal
- [ ] Octal → Binary
- [ ] Binary → Hexadecimal
- [ ] Hexadecimal → Binary
- [ ] Octal → Hexadecimal
- [ ] Hexadecimal → Octal
- [ ] Fractional conversion
- [ ] Base validity
- [ ] Base arithmetic
- [ ] Number of digits in base `b`
- [ ] Maximum `n`-digit value

---

# 56. Related Topics

- [[Base Systems]]
- [[Binary Numbers]]
- [[Decimal Numbers]]
- [[Base-Based Problems]]
- [[Number of Digits]]
- [[Remainders]]
- [[Unit Digit]]

---

# 57. Quick Revision

> [!summary] One-Minute Revision

### Base to Decimal

$$
\boxed{
\sum d_i b^i
}
$$

### Decimal to Base

$$
\boxed{
\text{Divide repeatedly by }b
}
$$

Read:

$$
\boxed{\text{remainders bottom}\rightarrow\text{top}}
$$

### Fraction to Base

$$
\boxed{
\text{Multiply repeatedly by }b
}
$$

Read integer parts:

$$
\boxed{\text{top}\rightarrow\text{bottom}}
$$

### Binary ↔ Octal

$$
\boxed{
3\text{ bits}\leftrightarrow1\text{ octal digit}
}
$$

### Binary ↔ Hex

$$
\boxed{
4\text{ bits}\leftrightarrow1\text{ hex digit}
}
$$

### Base `b` Range

$$
\boxed{
b^{n-1}\le N\le b^n-1
}
$$

### Maximum

$$
\boxed{
b^n-1
}
$$

### Valid Digit

$$
\boxed{
d<b
}
$$

### Golden Memory Trick

> **Base → powers of the base. Decimal → divide by the target base. Binary → group 3 for octal and 4 for hexadecimal.**

### One-Line Recognition

> **Conversion question → first identify the source base and target base, then choose either place-value expansion, repeated division, or binary grouping.**