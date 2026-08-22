---
type: concept
subject: aptitude
topic: "Reverse of Number"
parent: "01. Number System/Digit Problems"
company: HCL
difficulty: easy
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - digit-problems
  - reverse-of-number
  - digits
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Digit Problems]]"
  - "[[Number Formation]]"
  - "[[Digit Sum]]"
  - "[[Number of Digits]]"
  - "[[Digit-Based Equations]]"
---

# Reverse of Number

## 1. Core Concept

> [!summary] Definition
> The **reverse of a number** is obtained by writing its digits from right to left.

Example:

$$
12345\rightarrow54321
$$

Therefore:

$$
\boxed{\operatorname{Reverse}(12345)=54321}
$$

---

# 2. Basic Examples

| Number | Reverse |
|---:|---:|
| `123` | `321` |
| `4567` | `7654` |
| `908` | `809` |
| `120` | `21` |
| `1000` | `1` |

> [!important]
> Zeros at the beginning of the reversed result are not written as part of the number.

For example:

$$
120\rightarrow021
$$

but numerically:

$$
\boxed{21}
$$

---

# 3. Mathematical Representation

For a 3-digit number:

$$
N=100a+10b+c
$$

Its reverse is:

$$
\boxed{
R=100c+10b+a
}
$$

For example:

$$
N=123
$$

Then:

$$
a=1,\quad b=2,\quad c=3
$$

So:

$$
R=300+20+1
$$

$$
\boxed{321}
$$

---

# 4. Two-Digit Number

Let:

$$
N=10a+b
$$

Then its reverse is:

$$
\boxed{
R=10b+a
}
$$

### Example

$$
N=47
$$

Then:

$$
a=4,\quad b=7
$$

Therefore:

$$
R=74
$$

---

# 5. Three-Digit Number

Let:

$$
N=100a+10b+c
$$

Then:

$$
\boxed{
R=100c+10b+a
}
$$

### Example

$$
N=582
$$

Reverse:

$$
\boxed285
$$

---

# 6. Four-Digit Number

Let:

$$
N=1000a+100b+10c+d
$$

Then:

$$
\boxed{
R=1000d+100c+10b+a
}
$$

### Example

$$
N=1234
$$

Reverse:

$$
\boxed4321
$$

---

# 7. General Reverse Formula

For:

$$
N=d_1d_2d_3\ldots d_n
$$

the reverse is:

$$
\boxed{
d_nd_{n-1}\ldots d_3d_2d_1
}
$$

This is the simplest conceptual definition.

---

# 8. Reverse Using Arithmetic

The reverse can be constructed digit by digit.

Suppose:

$$
N=1234
$$

Take the last digit:

$$
4
$$

Then:

$$
3
$$

Then:

$$
2
$$

Then:

$$
1
$$

Construct:

$$
4321
$$

This method is useful for both aptitude reasoning and programming.

---

# 9. Programming Formula

To extract the last digit:

$$
\boxed{
d=N\bmod10
}
$$

To remove the last digit:

$$
\boxed{
N=\left\lfloor\frac{N}{10}\right\rfloor
}
$$

Therefore, repeatedly:

1. Extract last digit.
2. Add it to reversed number.
3. Remove last digit.

---

# 10. Reverse Algorithm

For a positive integer `N`:

```text
reverse = 0

while N > 0:
    digit = N % 10
    reverse = reverse * 10 + digit
    N = N / 10
```

The key formula is:

$$
\boxed{
R=10R+d
}
$$

where `d` is the extracted last digit.

---

# 11. Example — Arithmetic Method

Find the reverse of:

$$
472
$$

Start:

$$
R=0
$$

### Step 1

Last digit:

$$
472\bmod10=2
$$

Update:

$$
R=0\times10+2=2
$$

Remaining:

$$
47
$$

### Step 2

Last digit:

$$
47\bmod10=7
$$

Update:

$$
R=2\times10+7=27
$$

Remaining:

$$
4
$$

### Step 3

Last digit:

$$
4
$$

Update:

$$
R=27\times10+4
$$

$$
\boxed{274}
$$

---

# 12. Reverse of a Number Ending in Zero

If a number ends in zero, the zero disappears from the reversed numerical value.

Example:

$$
1200
$$

Reverse digits:

$$
0021
$$

Numerically:

$$
\boxed{21}
$$

> [!warning]
> Do not write `0021` as the final numerical answer unless the question specifically asks for a fixed-width digit string.

---

# 13. Reverse of a Number Ending in Multiple Zeros

Example:

$$
45000
$$

Reverse:

$$
00054
$$

Numerical value:

$$
\boxed{54}
$$

---

# 14. Important Property — Digit Sum

A number and its reverse contain exactly the same digits.

Therefore:

$$
\boxed{
S(N)=S(R)
}
$$

where:

- `S(N)` = digit sum of `N`
- `R` = reverse of `N`

### Example

$$
12345
$$

Digit sum:

$$
1+2+3+4+5=15
$$

Reverse:

$$
54321
$$

Digit sum:

$$
5+4+3+2+1=15
$$

Therefore:

$$
\boxed{
S(N)=S(R)
}
$$

---

# 15. Important Property — Divisibility by 3

Since the digit sum is unchanged:

$$
\boxed{
N\text{ and }R\text{ have the same divisibility by }3
}
$$

If:

$$
3\mid N
$$

then:

$$
3\mid R
$$

---

# 16. Important Property — Divisibility by 9

Similarly:

$$
\boxed{
9\mid N\iff9\mid R
}
$$

because reversing the digits does not change their sum.

---

# 17. Important Property — Same Remainder Modulo 9

Since:

$$
S(N)=S(R)
$$

and:

$$
N\equiv S(N)\pmod9
$$

we get:

$$
\boxed{
N\equiv R\pmod9
}
$$

Therefore:

$$
\boxed{
N-R\text{ is divisible by }9
}
$$

---

# 18. Example

Take:

$$
N=1234
$$

Reverse:

$$
R=4321
$$

Difference:

$$
4321-1234=3087
$$

Check:

$$
3087\div9=343
$$

Therefore:

$$
\boxed{
4321-1234\text{ is divisible by }9
}
$$

---

# 19. Important Property — Parity

The parity of a number depends on its last digit.

After reversal, the new last digit is the original first digit.

Therefore:

> [!important]
> A number and its reverse do **not necessarily** have the same parity.

### Example

$$
123
$$

is odd.

Reverse:

$$
321
$$

is also odd.

But:

$$
124
$$

is even.

Reverse:

$$
421
$$

is odd.

Therefore:

$$
\boxed{
\text{Parity may change after reversal}
}
$$

---

# 20. When Does Parity Stay the Same?

The original number and reverse have the same parity when their first and last digits have the same parity.

### Example

$$
123
$$

First digit `1` → odd.

Last digit `3` → odd.

So both original and reverse are odd.

---

# 21. Important Property — Number of Digits

Reversing a number generally preserves its number of digits, except for trailing zeros.

Example:

$$
1234\rightarrow4321
$$

Both have 4 digits.

But:

$$
1200\rightarrow21
$$

The original has 4 digits, while the reverse has 2 digits numerically.

Therefore:

$$
\boxed{
\text{Trailing zeros disappear after reversal}
}
$$

---

# 22. Palindrome Number

A number is a **palindrome** if it is equal to its reverse.

$$
\boxed{
N=R
}
$$

### Examples

$$
121
$$

$$
1331
$$

$$
1221
$$

These are palindromes.

---

# 23. Non-Palindrome Example

$$
123
$$

Reverse:

$$
321
$$

Since:

$$
123\ne321
$$

it is not a palindrome.

---

# 24. Palindrome Condition

The simplest condition is:

$$
\boxed{
N=\operatorname{Reverse}(N)
}
$$

For digit-based questions, compare digits from both ends.

---

# 25. Two-Digit Palindrome

A two-digit number:

$$
10a+b
$$

is a palindrome if:

$$
a=b
$$

Therefore possible two-digit palindromes are:

$$
11,22,33,\ldots,99
$$

There are:

$$
\boxed9
$$

two-digit palindromes.

---

# 26. Three-Digit Palindrome

A three-digit palindrome has the form:

$$
\boxed{
aba
}
$$

Its value is:

$$
100a+10b+a
$$

Therefore:

$$
\boxed{
101a+10b
}
$$

### Example

$$
121,\ 232,\ 343,\ 454
$$

are examples.

---

# 27. Four-Digit Palindrome

A four-digit palindrome has the form:

$$
\boxed{
abba
}
$$

Its value is:

$$
1000a+100b+10b+a
$$

Therefore:

$$
\boxed{
1001a+110b
}
$$

Examples:

$$
1221,\ 1331,\ 1441
$$

---

# 28. Number of Palindromes

### `n`-digit palindrome

The first half determines the second half.

Therefore, for an `n`-digit palindrome:

$$
\boxed{
9\times10^{\lceil n/2\rceil-1}
}
$$

### Examples

#### 2-digit

$$
9\times10^{1-1}=9
$$

#### 3-digit

$$
9\times10^{2-1}=90
$$

#### 4-digit

$$
9\times10^{2-1}=90
$$

#### 5-digit

$$
9\times10^{3-1}=900
$$

---

# 29. Reverse Difference — Two-Digit Number

Let:

$$
N=10a+b
$$

Reverse:

$$
R=10b+a
$$

Then:

$$
N-R
=
10a+b-(10b+a)
$$

Therefore:

$$
\boxed{
N-R=9(a-b)
}
$$

Hence:

$$
\boxed{
9\mid(N-R)
}
$$

---

# 30. Reverse Difference — Three-Digit Number

Let:

$$
N=100a+10b+c
$$

Reverse:

$$
R=100c+10b+a
$$

Then:

$$
N-R
=
100a+10b+c-(100c+10b+a)
$$

Therefore:

$$
\boxed{
N-R=99(a-c)
}
$$

Since:

$$
99=9\times11
$$

we get:

$$
\boxed{
99\mid(N-R)
}
$$

---

# 31. Important Pattern — Three-Digit Reverse

For:

$$
N=100a+10b+c
$$

and:

$$
R=100c+10b+a
$$

we have:

$$
\boxed{
N-R=99(a-c)
}
$$

This is a very important aptitude shortcut.

---

# 32. Example

Let:

$$
N=572
$$

Reverse:

$$
R=275
$$

Difference:

$$
572-275=297
$$

Using the formula:

$$
99(5-2)
$$

$$
=99\times3
$$

$$
=297
$$

Correct.

---

# 33. Reverse Difference — Four-Digit Number

Let:

$$
N=1000a+100b+10c+d
$$

Reverse:

$$
R=1000d+100c+10b+a
$$

Then:

$$
N-R
=
999(a-d)+90(b-c)
$$

Therefore:

$$
\boxed{
N-R=999(a-d)+90(b-c)
}
$$

This can be useful in advanced digit-equation problems.

---

# 34. Special Pattern — Difference Is Divisible by 9

For any positive integer `N`:

$$
\boxed{
N-\operatorname{Reverse}(N)
}
$$

is divisible by `9`.

Why?

Because:

$$
N\equiv S(N)\pmod9
$$

and:

$$
R\equiv S(R)\pmod9
$$

Since:

$$
S(N)=S(R)
$$

therefore:

$$
\boxed{
N\equiv R\pmod9
}
$$

---

# 35. Special Pattern — Three-Digit Difference Is Divisible by 99

For a 3-digit number:

$$
\boxed{
N-R
}
$$

is always divisible by `99`.

### Example

$$
821-128=693
$$

and:

$$
693=99\times7
$$

---

# 36. Reverse and Modulo 11

For certain digit structures, reversal also interacts nicely with modulo `11`.

For a number:

$$
12345
$$

the alternating sum is:

$$
1-2+3-4+5=3
$$

After reversal:

$$
54321
$$

alternating sum:

$$
5-4+3-2+1=3
$$

The sign can depend on the number of digits, but divisibility by `11` is preserved under reversal.

Therefore:

$$
\boxed{
11\mid N\iff11\mid\operatorname{Reverse}(N)
}
$$

---

# 37. Important Property — Divisibility by 11

A number and its reverse have the same divisibility status by `11`.

### Example

$$
121
$$

is divisible by `11`.

Reverse:

$$
121
$$

also divisible by `11`.

Another example:

$$
1331
$$

Reverse:

$$
1331
$$

also divisible by `11`.

---

# 38. Reverse of a Multiple of 10

If:

$$
N=10k
$$

then the reverse loses the trailing zero.

Example:

$$
450\rightarrow54
$$

Therefore:

> [!warning]
> Reversal is not multiplication or division by a fixed number.

---

# 39. Reverse of a Two-Digit Number — Useful Formula

For:

$$
N=10a+b
$$

reverse:

$$
R=10b+a
$$

Sum:

$$
N+R
$$

$$
=(10a+b)+(10b+a)
$$

$$
\boxed{
N+R=11(a+b)
}
$$

Therefore:

$$
\boxed{
11\mid(N+R)
}
$$

---

# 40. Example — Two-Digit Reverse Sum

Take:

$$
N=47
$$

Reverse:

$$
74
$$

Sum:

$$
47+74=121
$$

And:

$$
121=11\times11
$$

Therefore:

$$
\boxed{
N+R\text{ is always divisible by }11
}
$$

for a two-digit number.

---

# 41. Three-Digit Reverse Sum

Let:

$$
N=100a+10b+c
$$

and:

$$
R=100c+10b+a
$$

Then:

$$
N+R
=
101(a+c)+20b
$$

Therefore:

$$
\boxed{
N+R=101(a+c)+20b
}
$$

There is no universal divisibility by `11` for all three-digit numbers.

---

# 42. Reverse and Digit Sum

Because reversal does not change the digits:

$$
\boxed{
S(N)=S(R)
}
$$

This means:

- same digit sum
- same digital root
- same remainder modulo `3`
- same remainder modulo `9`

Therefore:

$$
\boxed{
N\equiv R\pmod9
}
$$

---

# 43. Reverse and Digital Root

Since:

$$
N\equiv R\pmod9
$$

their digital roots are equal for positive numbers.

Therefore:

$$
\boxed{
DR(N)=DR(R)
}
$$

### Example

$$
123456
$$

Digit sum:

$$
21
$$

Digital root:

$$
3
$$

Reverse:

$$
654321
$$

Digit sum:

$$
21
$$

Digital root:

$$
3
$$

---

# 44. Finding a Number From Its Reverse

Suppose:

$$
N=10a+b
$$

and:

$$
R=10b+a
$$

If the sum and difference are known:

$$
N+R=11(a+b)
$$

$$
N-R=9(a-b)
$$

These two equations can be used to find the digits.

---

# 45. Example — Sum and Difference

A two-digit number and its reverse have sum:

$$
121
$$

Then:

$$
N+R=11(a+b)
$$

Therefore:

$$
a+b=11
$$

Possible digit pairs:

$$
2+9,\ 3+8,\ 4+7,\ 5+6
$$

Additional information is needed to identify the exact number.

---

# 46. Reverse Equation

A common aptitude question may say:

> A two-digit number is `x` more than its reverse.

Let:

$$
N=10a+b
$$

Reverse:

$$
R=10b+a
$$

Then:

$$
N-R=9(a-b)
$$

Therefore:

$$
\boxed{
a-b=\frac{x}{9}
}
$$

This immediately tells you that `x` must be divisible by `9`.

---

# 47. Example — Difference `27`

A two-digit number exceeds its reverse by `27`.

Then:

$$
N-R=27
$$

Using:

$$
9(a-b)=27
$$

we get:

$$
a-b=3
$$

Possible digit pairs:

$$
3,0
$$

$$
4,1
$$

$$
5,2
$$

$$
6,3
$$

$$
7,4
$$

$$
8,5
$$

$$
9,6
$$

So possible numbers include:

$$
30,41,52,63,74,85,96
$$

---

# 48. Important Pattern — Two-Digit Reverse Difference

Always remember:

$$
\boxed{
N-R=9(a-b)
}
$$

Therefore:

$$
\boxed{
\text{Difference is always divisible by }9
}
$$

---

# 49. Important Pattern — Two-Digit Reverse Sum

Always remember:

$$
\boxed{
N+R=11(a+b)
}
$$

Therefore:

$$
\boxed{
\text{Sum is always divisible by }11
}
$$

---

# 50. Number + Reverse

For a two-digit number:

$$
N=10a+b
$$

Reverse:

$$
R=10b+a
$$

Therefore:

$$
\boxed{
N+R=11(a+b)
}
$$

and:

$$
\boxed{
N-R=9(a-b)
}
$$

These two formulas are extremely high-yield.

---

# 51. Palindrome and Reverse

If:

$$
N=R
$$

then:

$$
N-R=0
$$

Therefore the number is a palindrome.

For a two-digit number:

$$
10a+b=10b+a
$$

Therefore:

$$
9a=9b
$$

Hence:

$$
\boxed{a=b}
$$

---

# 52. Important Pattern — Reverse Twice

Reversing a number twice gives the original number, ignoring leading zeros created during the first reversal.

Example:

$$
1234\rightarrow4321\rightarrow1234
$$

Therefore:

$$
\boxed{
R(R(N))=N
}
$$

for numbers without trailing zeros.

---

# 53. Reverse of a Palindrome

If:

$$
N
$$

is a palindrome:

$$
\boxed{
R(N)=N
}
$$

Examples:

$$
121\rightarrow121
$$

$$
1331\rightarrow1331
$$

---

# 54. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Treating `120` reversed as `021` numerically instead of `21`.
- ❌ Forgetting that trailing zeros disappear.
- ❌ Assuming reversal preserves parity.
- ❌ Confusing reverse with complement.
- ❌ Forgetting the digit-sum property.
- ❌ Using the two-digit formulas for three-digit numbers.
- ❌ Assuming `N + reverse(N)` is always divisible by `11` for every number.
- ❌ Forgetting the first digit cannot be zero when forming a number.
- ❌ Confusing palindrome with any repeated-digit number.

---

# 55. Formula Sheet

> [!important] Must Remember

### Two-Digit Number

$$
\boxed{
N=10a+b
}
$$

### Reverse

$$
\boxed{
R=10b+a
}
$$

### Three-Digit Number

$$
\boxed{
N=100a+10b+c
}
$$

### Reverse

$$
\boxed{
R=100c+10b+a
}
$$

### Two-Digit Reverse Sum

$$
\boxed{
N+R=11(a+b)
}
$$

### Two-Digit Reverse Difference

$$
\boxed{
N-R=9(a-b)
}
$$

### Three-Digit Reverse Difference

$$
\boxed{
N-R=99(a-c)
}
$$

### Digit Sum

$$
\boxed{
S(N)=S(R)
}
$$

### Modulo `9`

$$
\boxed{
N\equiv R\pmod9
}
$$

### Palindrome

$$
\boxed{
N=R
}
$$

---

# 56. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
\text{Reverse → write digits from right to left}
}
$$

### Pattern 2

$$
\boxed{
S(N)=S(R)
}
$$

### Pattern 3

$$
\boxed{
N\equiv R\pmod9
}
$$

### Pattern 4 — Two Digits

$$
\boxed{
N+R=11(a+b)
}
$$

### Pattern 5 — Two Digits

$$
\boxed{
N-R=9(a-b)
}
$$

### Pattern 6 — Three Digits

$$
\boxed{
N-R=99(a-c)
}
$$

### Pattern 7

$$
\boxed{
N=R\Rightarrow\text{palindrome}
}
$$

### Pattern 8

$$
\boxed{
3\mid N\iff3\mid R
}
$$

### Pattern 9

$$
\boxed{
9\mid N\iff9\mid R
}
$$

### Pattern 10

$$
\boxed{
11\mid N\iff11\mid R
}
$$

---

# 57. HCL Preparation Priority

**Priority:** 🔥🔥 High

Master these patterns because reverse-number questions are often combined with:

- digit equations
- divisibility
- palindromes
- number formation
- digit sums
- two-digit algebra

### Master These First

1. Basic reversal
2. Reverse with zero
3. Two-digit formula
4. Three-digit formula
5. Reverse sum
6. Reverse difference
7. Digit-sum property
8. Divisibility by `3` and `9`
9. Palindromes
10. Missing-digit reverse problems

---

# 58. Practice Checklist

- [ ] Basic reverse
- [ ] Reverse with trailing zeros
- [ ] Two-digit reverse
- [ ] Three-digit reverse
- [ ] Four-digit reverse
- [ ] Reverse using algebra
- [ ] Reverse sum
- [ ] Reverse difference
- [ ] Digit-sum property
- [ ] Divisibility after reversal
- [ ] Palindrome numbers
- [ ] Number from reverse
- [ ] Missing digits
- [ ] Reverse and divisibility
- [ ] Reverse-based equations

---

# 59. Related Topics

- [[Digit Problems]]
- [[Number Formation]]
- [[Digit Sum]]
- [[Number of Digits]]
- [[Digit-Based Equations]]
- [[Divisibility Rules]]
- [[Divisibility by 3]]
- [[Divisibility by 9]]
- [[Remainders]]
- [[Palindromic Numbers]]

---

# 60. Quick Revision

> [!summary] One-Minute Revision

### Basic

$$
\boxed{
1234\rightarrow4321
}
$$

### Two-Digit

$$
N=10a+b
$$

$$
\boxed{
R=10b+a
}
$$

### Three-Digit

$$
N=100a+10b+c
$$

$$
\boxed{
R=100c+10b+a
}
$$

### Two-Digit Sum

$$
\boxed{
N+R=11(a+b)
}
$$

### Two-Digit Difference

$$
\boxed{
N-R=9(a-b)
}
$$

### Three-Digit Difference

$$
\boxed{
N-R=99(a-c)
}
$$

### Digit Sum

$$
\boxed{
S(N)=S(R)
}
$$

### Divisibility

$$
\boxed{
3\mid N\iff3\mid R
}
$$

$$
\boxed{
9\mid N\iff9\mid R
}
$$

### Palindrome

$$
\boxed{
N=R
}
$$

### Golden Memory Trick

> **Reverse problems → write the number algebraically using place values, then compare it with its reverse.**

### One-Line Recognition

> **Two-digit number + reverse → immediately think `N = 10a+b`, `R = 10b+a`, then use sum/difference formulas.**