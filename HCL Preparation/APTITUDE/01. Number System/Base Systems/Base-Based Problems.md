---
type: concept
subject: aptitude
topic: "Base-Based Problems"
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
  - base-based-problems
  - number-base
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Base Systems]]"
  - "[[Binary Numbers]]"
  - "[[Decimal Numbers]]"
  - "[[Number Base Conversion]]"
---

# Base-Based Problems

## 1. Core Concept

> [!summary] Definition
> **Base-based problems** use the representation of numbers in different bases and ask you to determine:
>
> - the decimal value
> - an unknown base
> - an unknown digit
> - whether a number is valid in a base
> - addition or subtraction in another base
> - number of digits
> - relationships between numbers represented in different bases

The most important idea is:

$$
\boxed{
\text{Convert the base representation into place-value algebra}
}
$$

---

# 2. General Base Representation

A number:

$$
(abc)_b
$$

means:

$$
\boxed{
a\times b^2+c\times b+b
}
$$

Careful: the last digit is `c`, so correctly:

$$
\boxed{
(abc)_b=a b^2+b_{\text{digit}}b+c
}
$$

To avoid confusion, use variables:

$$
(xyz)_b
$$

means:

$$
\boxed{
xb^2+yb+z
}
$$

---

# 3. Universal Formula

For:

$$
(d_nd_{n-1}\ldots d_1d_0)_b
$$

the value is:

$$
\boxed{
\sum_{i=0}^{n}d_i b^i
}
$$

This is the master formula for base problems.

---

# 4. Digit Validity

In base `b`, every digit must satisfy:

$$
\boxed{
0\le d<b
}
$$

Therefore:

### Base 2

Valid:

$$
0,1
$$

### Base 5

Valid:

$$
0,1,2,3,4
$$

### Base 8

Valid:

$$
0,1,2,3,4,5,6,7
$$

### Base 10

Valid:

$$
0-9
$$

---

# 5. Invalid Base Detection

Suppose:

$$
(527)_b
$$

is given.

The largest digit is:

$$
7
$$

Therefore the base must satisfy:

$$
b>7
$$

So:

$$
\boxed{
b\ge8
}
$$

This is an extremely common shortcut.

---

# 6. Example — Find Possible Bases

For:

$$
(438)_b
$$

the largest digit is:

$$
8
$$

Therefore:

$$
b>8
$$

Hence:

$$
\boxed{
b\ge9
}
$$

---

# 7. Important Pattern — Minimum Possible Base

For a number whose largest digit is `d`:

$$
\boxed{
\text{Minimum base}=d+1
}
$$

Example:

$$
(572)_b
$$

largest digit:

$$
7
$$

minimum base:

$$
\boxed8
$$

---

# 8. Two-Digit Number in Base `b`

Let:

$$
(ab)_b
$$

Then its decimal value is:

$$
\boxed{
ab+b
}
$$

Using different variable names:

$$
(xy)_b
$$

means:

$$
\boxed{
xb+y
}
$$

---

# 9. Three-Digit Number in Base `b`

For:

$$
(xyz)_b
$$

the decimal value is:

$$
\boxed{
xb^2+yb+z
}
$$

This is one of the most important formulas.

---

# 10. Four-Digit Number

For:

$$
(wxyz)_b
$$

the decimal value is:

$$
\boxed{
wb^3+xb^2+yb+z
}
$$

---

# 11. Example — Base 5

Convert:

$$
(243)_5
$$

to decimal.

$$
2(5^2)+4(5)+3
$$

$$
=2(25)+20+3
$$

$$
=73
$$

Therefore:

$$
\boxed{
(243)_5=73_{10}
}
$$

---

# 12. Example — Base 7

Convert:

$$
(326)_7
$$

to decimal.

$$
3(7^2)+2(7)+6
$$

$$
=147+14+6
$$

$$
\boxed{167}
$$

---

# 13. Unknown Base Problems

A common question gives:

$$
(abc)_b=N
$$

and asks you to find `b`.

Write:

$$
\boxed{
ab^2+bb+c=N
}
$$

Use different symbols for the digit and base to avoid confusion.

For:

$$
(xyz)_b=N
$$

write:

$$
\boxed{
xb^2+yb+z=N
}
$$

Then solve for `b`.

---

# 14. Example — Find the Base

Suppose:

$$
(21)_b=11_{10}
$$

Representation:

$$
2b+1=11
$$

Therefore:

$$
2b=10
$$

$$
\boxed{b=5}
$$

So:

$$
\boxed{(21)_5=11_{10}}
$$

---

# 15. Example — Three-Digit Unknown Base

Suppose:

$$
(123)_b=38_{10}
$$

Then:

$$
1b^2+2b+3=38
$$

Therefore:

$$
b^2+2b-35=0
$$

Factor:

$$
(b+7)(b-5)=0
$$

Since base must be positive:

$$
\boxed{b=5}
$$

Check digit validity:

Largest digit is `3`, and:

$$
5>3
$$

valid.

---

# 16. Important Pattern — Always Check the Base

After solving for `b`, verify:

$$
\boxed{
b>\text{largest digit}
}
$$

A mathematically obtained base may be invalid if this condition fails.

---

# 17. Equality Between Two Bases

A common question may give:

$$
(abc)_b=(xyz)_c
$$

Convert both to decimal expressions.

Left:

$$
ab^2+bb+c
$$

Better using digit variables:

$$
\boxed{
xb^2+yb+z
}
$$

Right:

$$
\boxed{
pc^2+qc+r
}
$$

Then equate:

$$
\boxed{
xb^2+yb+z=pc^2+qc+r
}
$$

---

# 18. Example — Same Value

Consider:

$$
(11)_2
$$

and:

$$
(3)_{{10}}
$$

Binary:

$$
1(2)+1=3
$$

Therefore:

$$
\boxed{
(11)_2=(3)_{10}
}
$$

Different representations, same value.

---

# 19. Base Addition

Arithmetic in any base follows the same principle as decimal.

The key rule is:

> **Whenever a column reaches the base, carry `1` to the next position.**

---

# 20. Binary Addition

In base `2`:

$$
1+1=10_2
$$

Therefore:

$$
\boxed{
1+1=10_2
}
$$

---

# 21. Octal Addition

In base `8`:

$$
7+1=10_8
$$

Therefore:

$$
\boxed{
7+1=10_8
}
$$

---

# 22. General Base Addition

In base `b`:

$$
\boxed{
(b-1)+1=10_b
}
$$

This is the universal carry rule.

---

# 23. Example — Base 5 Addition

Add:

$$
23_5+14_5
$$

Units:

$$
3+4=7
$$

Since:

$$
7=1(5)+2
$$

write `2` and carry `1`.

Next:

$$
2+1+1=4
$$

Therefore:

$$
\boxed{
23_5+14_5=42_5
}
$$

Check:

$$
23_5=13_{10}
$$

$$
14_5=9_{10}
$$

Sum:

$$
22_{10}
$$

and:

$$
42_5=22_{10}
$$

Correct.

---

# 24. Base Subtraction

Subtraction also follows the same principle.

If the top digit is smaller than the bottom digit, borrow `1` from the next position.

But in base `b`, borrowing `1` means receiving:

$$
\boxed b
$$

units.

---

# 25. Example — Base 5 Subtraction

Calculate:

$$
42_5-13_5
$$

Units:

$$
2-3
$$

cannot be done.

Borrow `1` from the `4`.

The `2` becomes:

$$
2+5=7
$$

Then:

$$
7-3=4
$$

The first digit becomes:

$$
3
$$

Therefore:

$$
\boxed{
42_5-13_5=24_5
}
$$

Check:

$$
42_5=22
$$

$$
13_5=8
$$

Difference:

$$
14
$$

and:

$$
24_5=14
$$

Correct.

---

# 26. Base Multiplication

Multiplication works exactly like decimal multiplication.

The only difference is that carrying occurs at the given base.

For example, in base `5`:

$$
3\times4=12_{10}
$$

Convert `12` to base `5`:

$$
12=22_5
$$

Therefore:

$$
\boxed{
3\times4=22_5
}
$$

---

# 27. Base Division

Long division can also be performed in any base.

However, for aptitude questions, conversion to decimal is often faster unless the question specifically tests arithmetic in the given base.

---

# 28. Base `b` and Powers

In base `b`:

$$
10_b=b_{10}
$$

Therefore:

$$
\boxed{
10_b=b
}
$$

Similarly:

$$
100_b=b^2
$$

and:

$$
1000_b=b^3
$$

---

# 29. Important Pattern

Remember:

$$
\boxed{
10_b=b
}
$$

$$
\boxed{
100_b=b^2
}
$$

$$
\boxed{
1000_b=b^3
}
$$

This makes many base questions much easier.

---

# 30. Example

What is:

$$
100_7
$$

in decimal?

Since:

$$
100_b=b^2
$$

we immediately get:

$$
\boxed{49}
$$

---

# 31. All-Ones Pattern

A number consisting of `n` ones in base `b` is:

$$
\boxed{
111\ldots111_b
=
\frac{b^n-1}{b-1}
}
$$

This is a very useful formula.

---

# 32. Example — Base 5

Calculate:

$$
111_5
$$

Using the formula:

$$
\frac{5^3-1}{5-1}
$$

$$
=\frac{125-1}{4}
$$

$$
=\frac{124}{4}
$$

$$
\boxed{31}
$$

Check:

$$
1(25)+1(5)+1=31
$$

---

# 33. Two-Digit Repeated Number

For:

$$
11_b
$$

we have:

$$
b+1
$$

Therefore:

$$
\boxed{
11_b=b+1
}
$$

Example:

$$
11_8=9_{10}
$$

---

# 34. Three-Digit Repeated Number

For:

$$
111_b
$$

we have:

$$
b^2+b+1
$$

Therefore:

$$
\boxed{
111_b=b^2+b+1
}
$$

---

# 35. Maximum `n`-Digit Number

The largest digit in base `b` is:

$$
b-1
$$

Therefore the largest `n`-digit number is:

$$
\boxed{
(b-1)(b-1)\ldots(b-1)
}
$$

and its value is:

$$
\boxed{
b^n-1
}
$$

---

# 36. Example — Base 6

Largest 3-digit number:

$$
555_6
$$

Using the shortcut:

$$
6^3-1
$$

$$
=216-1
$$

$$
\boxed{215}
$$

---

# 37. Smallest `n`-Digit Number

The smallest positive `n`-digit number in base `b` is:

$$
\boxed{
b^{n-1}
}
$$

Example:

Smallest 4-digit base `5` number:

$$
5^3
$$

$$
\boxed{125}
$$

Its representation is:

$$
1000_5
$$

---

# 38. Number of `n`-Digit Numbers

In base `b`:

$$
\boxed{
(b-1)b^{n-1}
}
$$

### Example

Number of 3-digit binary numbers:

$$
(2-1)2^2
$$

$$
\boxed4
$$

They are:

$$
100,\ 101,\ 110,\ 111
$$

---

# 39. Base and Number of Digits

For positive `N`, number of digits in base `b`:

$$
\boxed{
\lfloor\log_bN\rfloor+1
}
$$

### Example

How many base-5 digits are needed for decimal `100`?

We know:

$$
5^2=25
$$

$$
5^3=125
$$

Therefore:

$$
25\le100<125
$$

So:

$$
\boxed3
$$

base-5 digits are required.

---

# 40. Minimum Base Problem

Suppose a number contains the digit:

$$
9
$$

Then the base must be:

$$
\boxed{
\ge10
}
$$

because the base must be greater than every digit.

---

# 41. Example

Can:

$$
(729)_b
$$

be a binary number?

No.

Binary allows only:

$$
0,1
$$

but the number contains:

$$
7,\ 2,\ 9
$$

Therefore:

$$
\boxed{\text{Invalid in binary}}
$$

---

# 42. Finding an Unknown Digit

Suppose:

$$
(3x)_5=18_{10}
$$

Then:

$$
3(5)+x=18
$$

Therefore:

$$
x=3
$$

So:

$$
\boxed{x=3}
$$

Check:

$$
3<5
$$

valid.

---

# 43. Example — Unknown Digit

Suppose:

$$
(4x2)_6=170_{10}
$$

Then:

$$
4(6^2)+x(6)+2=170
$$

$$
144+6x+2=170
$$

$$
6x=24
$$

$$
\boxed{x=4}
$$

---

# 44. Unknown Base and Unknown Digit

Sometimes both the base and a digit are unknown.

Example:

$$
(2x)_b=17
$$

Then:

$$
2b+x=17
$$

with:

$$
0\le x<b
$$

and:

$$
b>2
$$

Multiple solutions may exist unless another condition is provided.

> [!important]
> Always count the possible solutions instead of assuming there is only one.

---

# 45. Base Equation Strategy

When you see an unknown base:

### Step 1

Write place-value expansion.

### Step 2

Set it equal to the given decimal value.

### Step 3

Solve the equation.

### Step 4

Check:

$$
b>\text{largest digit}
$$

### Step 5

Check that the base is an integer.

---

# 46. Example — Strategy

Given:

$$
(132)_b=62
$$

Expand:

$$
b^2+3b+2=62
$$

Therefore:

$$
b^2+3b-60=0
$$

Factor:

$$
(b+10)(b-6)=0
$$

Thus:

$$
b=6
$$

Check:

Largest digit:

$$
3
$$

and:

$$
6>3
$$

Therefore:

$$
\boxed{b=6}
$$

---

# 47. Base Comparison

Suppose:

$$
(100)_b
$$

and:

$$
(100)_c
$$

Since:

$$
100_b=b^2
$$

and:

$$
100_c=c^2
$$

if:

$$
b>c
$$

then:

$$
\boxed{
100_b>100_c
}
$$

---

# 48. Base Representation of Zero

The value zero is represented as:

$$
\boxed{0_b}
$$

for every valid base.

For example:

$$
0_2=0_{10}=0_8=0_{16}
$$

---

# 49. Base Representation of One

Similarly:

$$
\boxed{
1_b=1_{10}
}
$$

for every base.

---

# 50. Base Representation of the Base

The base itself is represented as:

$$
\boxed{
10_b
}
$$

Examples:

$$
10_2=2
$$

$$
10_5=5
$$

$$
10_8=8
$$

$$
10_{16}=16
$$

This is one of the most important patterns.

---

# 51. Base Representation of `b-1`

The number immediately before:

$$
10_b
$$

is:

$$
\boxed{
(b-1)_b
}
$$

For multiple digits:

$$
99_{10}=10^2-1
$$

$$
77_8=8^2-1
$$

$$
FF_{16}=16^2-1
$$

---

# 52. Remainder in a Base

The last digit of a number in base `b` gives the remainder when divided by `b`.

Therefore:

$$
\boxed{
N\bmod b=\text{last digit}
}
$$

### Example

For:

$$
1234_5
$$

the last digit is:

$$
4
$$

Therefore:

$$
\boxed{
N\bmod5=4
}
$$

---

# 53. Remainder Modulo a Power of Base

The last `k` digits determine the remainder modulo:

$$
\boxed{
b^k
}
$$

### Example

For a base-5 number, the last two digits determine the remainder modulo:

$$
5^2=25
$$

This is analogous to:

- decimal → last 2 digits → modulo `100`
- binary → last 3 bits → modulo `8`

---

# 54. Important Pattern — Last Digit

In base `b`:

$$
\boxed{
\text{Last digit}=N\bmod b
}
$$

This is extremely useful in remainder questions.

---

# 55. Base and Divisibility

A number ending in zero in base `b` is divisible by `b`.

Example:

$$
120_5
$$

ends in zero.

Therefore:

$$
5\mid120_5
$$

in terms of its numerical value.

---

# 56. Example

Consider:

$$
240_7
$$

Since it ends in `0`:

$$
\boxed{
7\mid240_7
}
$$

This works because the number is:

$$
2(49)+4(7)
$$

which is clearly divisible by `7`.

---

# 57. Base-Specific Evenness

Do not confuse decimal evenness with the last digit in another base.

In base `2`, last bit `0` means even because the base itself is `2`.

For a general base, the last digit gives the remainder modulo the base, not necessarily modulo `2`.

---

# 58. Base Conversion Shortcut

If:

$$
b=2^k
$$

then binary conversion is especially easy.

### Base `8`

$$
8=2^3
$$

→ group `3` bits.

### Base `16`

$$
16=2^4
$$

→ group `4` bits.

This is a major aptitude shortcut.

---

# 59. Important Pattern — Base Powers

If:

$$
b=a^k
$$

then one digit in base `b` corresponds naturally to `k` digits in base `a` when the smaller base is represented in positional groups.

For binary:

$$
8=2^3
$$

and:

$$
16=2^4
$$

Therefore:

$$
\boxed{
1\text{ octal digit}=3\text{ binary bits}
}
$$

$$
\boxed{
1\text{ hex digit}=4\text{ binary bits}
}
$$

---

# 60. Base Arithmetic Shortcut

When arithmetic in a strange base looks difficult:

> [!tip]
> **Convert both numbers to decimal, perform the operation, then convert the result back.**

Example:

$$
23_5+14_5
$$

Convert:

$$
23_5=13
$$

$$
14_5=9
$$

Add:

$$
13+9=22
$$

Convert back:

$$
22=42_5
$$

Therefore:

$$
\boxed{42_5}
$$

---

# 61. Common Question Types

Base-based aptitude questions commonly ask:

1. Convert base `b` to decimal.
2. Convert decimal to base `b`.
3. Find the unknown base.
4. Find an unknown digit.
5. Check whether a number is valid in a base.
6. Add numbers in a given base.
7. Subtract numbers in a given base.
8. Find the maximum `n`-digit number.
9. Find the minimum `n`-digit number.
10. Count `n`-digit numbers.
11. Find the number of digits in another base.
12. Find remainders using the last digits.
13. Compare numbers represented in different bases.
14. Convert between binary, octal, decimal and hexadecimal.

---

# 62. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Forgetting that digits must be less than the base.
- ❌ Treating `(123)_5` as decimal `123`.
- ❌ Using decimal place values instead of powers of the given base.
- ❌ Forgetting the base subscript.
- ❌ Solving for a base without checking digit validity.
- ❌ Assuming the unknown base can be non-integer.
- ❌ Confusing `10_b` with decimal `10`.
- ❌ Forgetting that `10_b=b`.
- ❌ Reading decimal-to-base remainders in the wrong direction.
- ❌ Forgetting to convert the final answer back to the required base.
- ❌ Confusing the maximum `n`-digit value with the number of `n`-digit values.
- ❌ Using binary grouping for arbitrary bases.

---

# 63. Formula Sheet

> [!important] Must Remember

### General Base Representation

$$
\boxed{
(d_nd_{n-1}\ldots d_0)_b
=
\sum d_i b^i
}
$$

### Valid Digit

$$
\boxed{
0\le d<b
}
$$

### Minimum Base

$$
\boxed{
\text{minimum base}=\text{largest digit}+1
}
$$

### Two-Digit Number

$$
\boxed{
(xy)_b=xb+y
}
$$

### Three-Digit Number

$$
\boxed{
(xyz)_b=xb^2+yb+z
}
$$

### Four-Digit Number

$$
\boxed{
(wxyz)_b=wb^3+xb^2+yb+z
}
$$

### Base Itself

$$
\boxed{
10_b=b
}
$$

### `n`-Digit Range

$$
\boxed{
b^{n-1}\le N\le b^n-1
}
$$

### Maximum `n`-Digit Number

$$
\boxed{
b^n-1
}
$$

### Minimum `n`-Digit Number

$$
\boxed{
b^{n-1}
}
$$

### Number of `n`-Digit Numbers

$$
\boxed{
(b-1)b^{n-1}
}
$$

### Number of Digits in Base `b`

$$
\boxed{
\lfloor\log_bN\rfloor+1
}
$$

### All-Ones Number

$$
\boxed{
111\ldots111_b
=
\frac{b^n-1}{b-1}
}
$$

### Last Digit

$$
\boxed{
N\bmod b=\text{last digit}
}
$$

---

# 64. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
\text{Base }b\rightarrow\text{place values are powers of }b
}
$$

### Pattern 2

$$
\boxed{
\text{Valid digit}<b
}
$$

### Pattern 3

$$
\boxed{
\text{Minimum base}=\text{largest digit}+1
}
$$

### Pattern 4

$$
\boxed{
10_b=b
}
$$

### Pattern 5

$$
\boxed{
100_b=b^2
}
$$

### Pattern 6

$$
\boxed{
1000_b=b^3
}
$$

### Pattern 7

$$
\boxed{
\text{Maximum }n\text{-digit value}=b^n-1
}
$$

### Pattern 8

$$
\boxed{
\text{Number of }n\text{-digit values}=(b-1)b^{n-1}
}
$$

### Pattern 9

$$
\boxed{
\text{Last digit}=N\bmod b
}
$$

### Pattern 10

$$
\boxed{
\text{Last }k\text{ digits}\rightarrow N\bmod b^k
}
$$

---

# 65. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Very High

Focus on these patterns first:

1. Place-value representation
2. Unknown base
3. Unknown digit
4. Minimum possible base
5. Base validity
6. Base conversion
7. Base arithmetic
8. `10_b`, `100_b`, `1000_b`
9. Maximum and minimum values
10. Number of digits
11. Remainder using last digits
12. Binary-octal relationship
13. Binary-hexadecimal relationship

---

# 66. Practice Checklist

- [ ] Convert base `b` → decimal
- [ ] Convert decimal → base `b`
- [ ] Find unknown base
- [ ] Find unknown digit
- [ ] Check valid base
- [ ] Find minimum base
- [ ] Base addition
- [ ] Base subtraction
- [ ] Base multiplication
- [ ] Base division
- [ ] Maximum `n`-digit number
- [ ] Minimum `n`-digit number
- [ ] Count `n`-digit numbers
- [ ] Number of digits in base `b`
- [ ] Base remainder
- [ ] Base divisibility
- [ ] Compare different bases
- [ ] Binary ↔ Octal
- [ ] Binary ↔ Hexadecimal

---

# 67. Related Topics

- [[Base Systems]]
- [[Binary Numbers]]
- [[Decimal Numbers]]
- [[Number Base Conversion]]
- [[Remainders]]
- [[Unit Digit]]
- [[Divisibility Rules]]
- [[Number of Digits]]

---

# 68. Quick Revision

> [!summary] One-Minute Revision

### Base Representation

$$
\boxed{
(xyz)_b=xb^2+yb+z
}
$$

### Valid Digit

$$
\boxed{
d<b
}
$$

### Minimum Base

$$
\boxed{
\text{largest digit}+1
}
$$

### Base Itself

$$
\boxed{
10_b=b
}
$$

### Maximum `n`-Digit Value

$$
\boxed{
b^n-1
}
$$

### Minimum `n`-Digit Value

$$
\boxed{
b^{n-1}
}
$$

### Number of `n`-Digit Values

$$
\boxed{
(b-1)b^{n-1}
}
$$

### Digits in Base `b`

$$
\boxed{
\lfloor\log_bN\rfloor+1
}
$$

### Last Digit

$$
\boxed{
N\bmod b
}
$$

### Golden Memory Trick

> **Unknown base → expand using powers of the base → solve → check that every digit is smaller than the base.**

### One-Line Recognition

> **If you see `(number)₍b₎`, never treat it as decimal first; immediately expand it using powers of `b`.**