---
type: concept
subject: aptitude
topic: "Digit Sum"
parent: "01. Number System/Digit Problems"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - digit-problems
  - digit-sum
  - divisibility
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Digit Problems]]"
  - "[[Number Formation]]"
  - "[[Divisibility Rules]]"
  - "[[Remainders]]"
---

# Digit Sum

## 1. Core Concept

> [!summary] Definition
> **Digit sum** means adding all the digits of a number.

For:

$$
N=58327
$$

the digit sum is:

$$
5+8+3+2+7=25
$$

Therefore:

$$
\boxed{25}
$$

---

# 2. Basic Formula

If:

$$
N=d_1d_2d_3\ldots d_n
$$

then:

$$
\boxed{
S(N)=d_1+d_2+d_3+\cdots+d_n
}
$$

where `S(N)` represents the digit sum.

---

# 3. Example

Find the digit sum of:

$$
728491
$$

Calculate:

$$
7+2+8+4+9+1
$$

$$
=31
$$

Therefore:

$$
\boxed{31}
$$

---

# 4. Repeated Digit Sum

Sometimes we repeatedly add the digits until only one digit remains.

Example:

$$
9875
$$

First:

$$
9+8+7+5=29
$$

Again:

$$
2+9=11
$$

Again:

$$
1+1=2
$$

Therefore:

$$
\boxed2
$$

This final single digit is called the **digital root**.

---

# 5. Digital Root

For a positive integer `N`:

$$
\boxed{
\text{Digital Root}(N)
=
1+((N-1)\bmod9)
}
$$

An equivalent rule is:

$$
\boxed{
N\bmod9
}
$$

except that a remainder of `0` corresponds to digital root `9` for positive `N`.

### Example

For:

$$
987654
$$

digit sum:

$$
9+8+7+6+5+4=39
$$

Then:

$$
3+9=12
$$

Then:

$$
1+2=3
$$

Therefore:

$$
\boxed3
$$

---

# 6. Digit Sum and Divisibility by 3

A number is divisible by `3` if its digit sum is divisible by `3`.

$$
\boxed{
N\text{ divisible by }3
\iff
S(N)\text{ divisible by }3
}
$$

### Example

Check whether:

$$
57231
$$

is divisible by `3`.

Digit sum:

$$
5+7+2+3+1=18
$$

Since:

$$
18\bmod3=0
$$

therefore:

$$
\boxed{57231\text{ is divisible by }3}
$$

---

# 7. Digit Sum and Divisibility by 9

Similarly:

$$
\boxed{
N\text{ divisible by }9
\iff
S(N)\text{ divisible by }9
}
$$

### Example

Check:

$$
72918
$$

Digit sum:

$$
7+2+9+1+8=27
$$

Since:

$$
27\bmod9=0
$$

therefore:

$$
\boxed{72918\text{ is divisible by }9}
$$

---

# 8. Remainder Using Digit Sum

For modulus `3`:

$$
\boxed{
N\bmod3=S(N)\bmod3
}
$$

For modulus `9`:

$$
\boxed{
N\bmod9=S(N)\bmod9
}
$$

This is extremely useful for very large numbers.

---

# 9. Example — Huge Number Modulo 9

Find:

$$
987654321987654321\bmod9
$$

Do not divide the huge number.

Find digit sum:

$$
9+8+7+6+5+4+3+2+1+9+8+7+6+5+4+3+2+1
$$

Then reduce the sum modulo `9`.

This is much faster than performing long division.

> [!tip] Exam Pattern
> **Huge number + modulus `3` or `9` → digit sum immediately.**

---

# 10. Adding a Number's Digits

Suppose:

$$
N=100a+10b+c
$$

Then digit sum is:

$$
\boxed{
a+b+c
}
$$

### Example

For:

$$
472
$$

we have:

$$
4+7+2=13
$$

---

# 11. Digit Sum of a Two-Digit Number

For:

$$
10a+b
$$

digit sum:

$$
\boxed{
a+b
}
$$

### Example

$$
84
$$

Digit sum:

$$
8+4=12
$$

---

# 12. Digit Sum of a Three-Digit Number

For:

$$
100a+10b+c
$$

digit sum:

$$
\boxed{
a+b+c
}
$$

This representation is useful in digit-equation problems.

---

# 13. Digit Sum of a Four-Digit Number

For:

$$
1000a+100b+10c+d
$$

digit sum:

$$
\boxed{
a+b+c+d
}
$$

---

# 14. Important Pattern — Adding Zeros

Zeros do not affect digit sum.

### Example

$$
5000203
$$

Digit sum:

$$
5+0+0+0+2+0+3
$$

$$
=10
$$

Therefore:

$$
\boxed{10}
$$

---

# 15. Important Pattern — Appending Zeros

Appending zero to a number does not change its digit sum.

Example:

$$
123
$$

Digit sum:

$$
6
$$

Now:

$$
1230
$$

Digit sum:

$$
1+2+3+0=6
$$

Therefore:

$$
\boxed{
S(10N)=S(N)
}
$$

---

# 16. Digit Sum After Multiplication by 10

Because:

$$
10N
$$

simply adds a zero at the end:

$$
\boxed{
S(10N)=S(N)
}
$$

More generally:

$$
\boxed{
S(10^kN)=S(N)
}
$$

for positive integer `k`.

---

# 17. Digit Sum and Multiples of 9

If:

$$
N=9k
$$

then:

$$
S(N)
$$

is also divisible by `9`.

Therefore:

$$
\boxed{
9\mid N\Rightarrow9\mid S(N)
}
$$

The converse is also true:

$$
\boxed{
9\mid S(N)\Rightarrow9\mid N
}
$$

---

# 18. Digit Sum and Multiples of 3

Similarly:

$$
\boxed{
3\mid N
\iff
3\mid S(N)
}
$$

This is one of the most frequently used aptitude shortcuts.

---

# 19. Repeated Digit Sum and Modulo 9

Repeated digit addition does not change the number's remainder modulo `9`.

For example:

$$
9876
$$

Digit sum:

$$
9+8+7+6=30
$$

Again:

$$
3+0=3
$$

Therefore:

$$
9876\bmod9=3
$$

and its digital root is:

$$
\boxed3
$$

---

# 20. Casting Out Nines

> [!summary] Classic Technique
> **Casting out nines** means repeatedly reducing a number by its digit sum to determine its remainder modulo `9`.

Example:

$$
456789
$$

Digit sum:

$$
4+5+6+7+8+9=39
$$

Then:

$$
3+9=12
$$

Then:

$$
1+2=3
$$

Therefore:

$$
456789\bmod9=3
$$

---

# 21. Digit Sum of a Number Plus Another Number

Digit sum itself is not generally additive without carrying.

For example:

$$
58+47=105
$$

Digit sum of result:

$$
1+0+5=6
$$

But:

$$
S(58)+S(47)
=
13+11
=
24
$$

So:

$$
S(a+b)\ne S(a)+S(b)
$$

in general.

> [!warning] Important
> Digit sum is preserved **modulo `9`**, but not necessarily as an exact value.

---

# 22. Correct Modular Relationship

Although exact digit sums do not always add directly:

$$
\boxed{
S(a+b)\equiv S(a)+S(b)\pmod9
}
$$

Similarly:

$$
\boxed{
S(ab)\equiv S(a)S(b)\pmod9
}
$$

This is because every power of `10` satisfies:

$$
10\equiv1\pmod9
$$

---

# 23. Why Digit Sum Works

Consider:

$$
N=100a+10b+c
$$

Modulo `9`:

$$
100\equiv1\pmod9
$$

and:

$$
10\equiv1\pmod9
$$

Therefore:

$$
N
\equiv
a+b+c
\pmod9
$$

So:

$$
\boxed{
N\equiv S(N)\pmod9
}
$$

This is the mathematical foundation of the digit-sum rule.

---

# 24. Digit Sum Modulo 3

Since:

$$
10\equiv1\pmod3
$$

we similarly get:

$$
\boxed{
N\equiv S(N)\pmod3
}
$$

Therefore digit sum works for both:

$$
\boxed{3\text{ and }9}
$$

---

# 25. Example — Divisibility by 3

Check:

$$
847392
$$

Digit sum:

$$
8+4+7+3+9+2=33
$$

Since:

$$
33
$$

is divisible by `3`:

$$
\boxed{\text{Yes}}
$$

---

# 26. Example — Divisibility by 9

Check:

$$
847392
$$

Digit sum:

$$
33
$$

Since:

$$
33\bmod9\ne0
$$

the number is:

$$
\boxed{\text{not divisible by }9}
$$

But it is divisible by `3`.

---

# 27. Difference Between Divisibility by 3 and 9

If digit sum is:

### Multiple of 9

Then the number is divisible by:

$$
\boxed9
$$

and therefore also by:

$$
\boxed3
$$

### Multiple of 3 but not 9

Then the number is divisible by:

$$
\boxed3
$$

but not by `9`.

### Example

Digit sum:

$$
21
$$

Since:

$$
21\bmod3=0
$$

but:

$$
21\bmod9\ne0
$$

the number is divisible by `3`, not `9`.

---

# 28. Finding Missing Digit Using Digit Sum

This is a very important aptitude pattern.

Suppose a number must be divisible by `9` and contains an unknown digit `x`.

Use:

$$
\boxed{
\text{Digit sum}\equiv0\pmod9
}
$$

### Example

Find `x` so that:

$$
45x3
$$

is divisible by `9`.

Digit sum:

$$
4+5+x+3
$$

$$
=12+x
$$

Need:

$$
12+x\equiv0\pmod9
$$

Therefore:

$$
x=6
$$

Answer:

$$
\boxed6
$$

---

# 29. Missing Digit — Divisible by 3

Suppose:

$$
72x4
$$

is divisible by `3`.

Digit sum:

$$
7+2+x+4
$$

$$
=13+x
$$

Need:

$$
13+x\equiv0\pmod3
$$

Therefore:

$$
x\equiv2\pmod3
$$

Possible digits:

$$
\boxed{2,5,8}
$$

---

# 30. Missing Multiple Digits

If more than one digit is unknown, create an equation using the digit sum.

Example:

$$
4x7y
$$

is divisible by `9`.

Then:

$$
4+x+7+y
$$

$$
=11+x+y
$$

Need:

$$
11+x+y\equiv0\pmod9
$$

Therefore:

$$
\boxed{
x+y\equiv7\pmod9
}
$$

---

# 31. Digit Sum of Consecutive Numbers

Consider:

$$
99,\ 100,\ 101
$$

Digit sums:

$$
18,\ 1,\ 2
$$

The digit sum can change sharply when carrying occurs.

Therefore:

> [!warning]
> Do not assume digit sums increase smoothly with the number.

---

# 32. Carrying and Digit Sum

When adding numbers, carrying changes the digit sum.

If one carry of `10` occurs, the digit sum decreases by `9`.

Therefore:

$$
\boxed{
\text{Each carry changes digit sum by a multiple of }9
}
$$

This explains why digit sum modulo `9` remains unchanged.

---

# 33. Example — Carry

Consider:

$$
58+47=105
$$

Individual digit sums:

$$
S(58)=13
$$

$$
S(47)=11
$$

Total:

$$
24
$$

Result digit sum:

$$
S(105)=6
$$

Difference:

$$
24-6=18
$$

which is a multiple of `9`.

Therefore:

$$
\boxed{
S(58)+S(47)\equiv S(105)\pmod9
}
$$

---

# 34. Digit Sum and Number Formation

When digits are rearranged, the digit sum remains unchanged.

Example:

$$
1234
$$

Digit sum:

$$
10
$$

Rearrange:

$$
4321
$$

Digit sum:

$$
10
$$

Therefore:

$$
\boxed{
\text{Permutation of digits does not change digit sum}
}
$$

---

# 35. Important Pattern — Rearrangement

Any arrangement of the same digits has the same digit sum.

Therefore, if one arrangement is divisible by `3` or `9`, every arrangement of exactly the same digits is also divisible by that divisor.

### Example

Digits:

$$
1,2,6
$$

Digit sum:

$$
9
$$

Therefore every 3-digit arrangement:

$$
126,\ 162,\ 216,\ldots
$$

is divisible by `9`.

---

# 36. Digit Sum and Divisibility by 11

Do not confuse the rules.

For `3` and `9`:

$$
\boxed{\text{ordinary digit sum}}
$$

For `11`:

$$
\boxed{\text{alternating digit sum}}
$$

Example:

$$
12345
$$

For `11`:

$$
(5-4+3-2+1)=3
$$

So:

$$
12345\bmod11=3
$$

---

# 37. Digit Sum of Powers

For powers, digit sum can help with divisibility by `3` or `9`.

Example:

$$
7^{100}
$$

Since:

$$
7\equiv1\pmod3
$$

we know:

$$
7^{100}\equiv1\pmod3
$$

Therefore its digit sum must leave remainder `1` modulo `3`.

You do not need to calculate the huge power.

---

# 38. Digit Sum of Factorials

For:

$$
n!
$$

when `n≥3`, the factorial contains a factor `3`.

Therefore:

$$
3\mid n!
$$

So its digit sum is divisible by `3`.

For:

$$
n\ge6
$$

the factorial contains factors sufficient for divisibility by `9`.

Therefore:

$$
\boxed{
9\mid n!,\quad n\ge6
}
$$

and its digit sum is divisible by `9`.

---

# 39. Example — `10!`

Since:

$$
10!
$$

is divisible by `9`:

$$
\boxed{
\text{digit sum of }10!\text{ is divisible by }9
}
$$

There is no need to calculate `10!`.

---

# 40. Digit Sum of Multiples of 9

Every positive multiple of `9` has a digit sum that is a multiple of `9`.

Examples:

$$
18\rightarrow9
$$

$$
27\rightarrow9
$$

$$
45\rightarrow9
$$

$$
99\rightarrow18
$$

$$
108\rightarrow9
$$

---

# 41. Digital Root Pattern

For positive integers, the digital root can only be:

$$
\boxed{
1,2,3,4,5,6,7,8,9
}
$$

It can never be `0`.

However:

$$
N\bmod9=0
$$

corresponds to:

$$
\boxed{\text{digital root }9}
$$

---

# 42. Digital Root Table

| `N mod 9` | Digital root |
|---:|---:|
| `0` | `9` |
| `1` | `1` |
| `2` | `2` |
| `3` | `3` |
| `4` | `4` |
| `5` | `5` |
| `6` | `6` |
| `7` | `7` |
| `8` | `8` |

---

# 43. Digital Root Shortcut

For positive `N`:

$$
\boxed{
DR(N)=1+((N-1)\bmod9)
}
$$

### Example

Find the digital root of:

$$
123456789
$$

Since:

$$
123456789\bmod9=0
$$

the digital root is:

$$
\boxed9
$$

---

# 44. Digital Root of a Product

For positive integers:

$$
DR(ab)=DR(DR(a)\times DR(b))
$$

### Example

Find the digital root of:

$$
123\times456
$$

First:

$$
DR(123)=6
$$

because:

$$
1+2+3=6
$$

For `456`:

$$
4+5+6=15
$$

then:

$$
1+5=6
$$

Therefore:

$$
6\times6=36
$$

Digital root:

$$
3+6=9
$$

Answer:

$$
\boxed9
$$

---

# 45. Digital Root of a Sum

Similarly:

$$
\boxed{
DR(a+b)=DR(DR(a)+DR(b))
}
$$

### Example

$$
DR(789+456)
$$

First:

$$
DR(789)=6
$$

$$
DR(456)=6
$$

Then:

$$
6+6=12
$$

Digital root:

$$
1+2=3
$$

Answer:

$$
\boxed3
$$

---

# 46. Digit Sum in Missing-Digit Problems

> [!important] Common Question Types

You may be asked to find:

- one missing digit
- multiple missing digits
- smallest possible digit
- largest possible digit
- number of possible digits

The usual method is:

$$
\boxed{
\text{Create a digit-sum congruence}
}
$$

---

# 47. Example — Smallest Missing Digit

Find the smallest digit `x` such that:

$$
56x2
$$

is divisible by `9`.

Digit sum:

$$
5+6+x+2=13+x
$$

Need a multiple of `9`.

Possible:

$$
13+x=18
$$

Therefore:

$$
x=5
$$

Answer:

$$
\boxed5
$$

---

# 48. Example — Largest Missing Digit

Find the largest digit `x` such that:

$$
82x5
$$

is divisible by `3`.

Digit sum:

$$
8+2+x+5=15+x
$$

Since `15` is already divisible by `3`:

$$
x\equiv0\pmod3
$$

Possible digits:

$$
0,3,6,9
$$

Largest:

$$
\boxed9
$$

---

# 49. Digit Sum and Difference

If two numbers have the same digit sum modulo `9`, then their difference is divisible by `9`.

If:

$$
S(a)\equiv S(b)\pmod9
$$

then:

$$
\boxed{
9\mid(a-b)
}
$$

This is useful in comparison and divisibility questions.

---

# 50. Example

Consider:

$$
123456
$$

and:

$$
654321
$$

Both have digit sum:

$$
21
$$

Therefore:

$$
123456\equiv654321\pmod9
$$

Hence:

$$
\boxed{
9\mid(654321-123456)
}
$$

---

# 51. Important Pattern — Same Digits

If two numbers contain exactly the same digits, then:

$$
\boxed{
\text{same digit sum}
}
$$

Therefore they have the same remainder modulo `9` and modulo `3`.

This is useful in rearrangement problems.

---

# 52. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Assuming digit sum itself is preserved under addition.
- ❌ Using the digit-sum rule for divisibility by arbitrary numbers.
- ❌ Confusing digit sum with digital root.
- ❌ Forgetting that digital root `0` corresponds to `9` for positive integers.
- ❌ Using ordinary digit sum for divisibility by `11`.
- ❌ Calculating a huge number when only its digit sum modulo `3` or `9` is needed.
- ❌ Forgetting that rearranging digits does not change their sum.
- ❌ Assuming digit sum always increases with the number.

---

# 53. Formula Sheet

> [!important] Must Remember

### Digit Sum

$$
\boxed{
S(N)=\sum\text{digits of }N
}
$$

### Modulo `3`

$$
\boxed{
N\bmod3=S(N)\bmod3
}
$$

### Modulo `9`

$$
\boxed{
N\bmod9=S(N)\bmod9
}
$$

### Divisibility by `3`

$$
\boxed{
3\mid N\iff3\mid S(N)
}
$$

### Divisibility by `9`

$$
\boxed{
9\mid N\iff9\mid S(N)
}
$$

### Digital Root

$$
\boxed{
DR(N)=1+((N-1)\bmod9)
}
$$

### Modular Digit-Sum Property

$$
\boxed{
N\equiv S(N)\pmod9
}
$$

---

# 54. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
\text{Digit sum}=\text{add all digits}
}
$$

### Pattern 2

$$
\boxed{
3\mid N\iff3\mid S(N)
}
$$

### Pattern 3

$$
\boxed{
9\mid N\iff9\mid S(N)
}
$$

### Pattern 4

$$
\boxed{
N\bmod9=S(N)\bmod9
}
$$

### Pattern 5

$$
\boxed{
N\bmod3=S(N)\bmod3
}
$$

### Pattern 6

Missing digit + divisibility by `3` or `9`:

$$
\boxed{
\text{Use digit-sum equation}
}
$$

### Pattern 7

Same digits rearranged:

$$
\boxed{
\text{same digit sum}
}
$$

### Pattern 8

Large number + modulo `3` or `9`:

$$
\boxed{
\text{Use digit sum instead of division}
}
$$

### Pattern 9

Digital root:

$$
\boxed{
1+((N-1)\bmod9)
}
$$

---

# 55. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Digit sum is a small topic but appears inside many other aptitude problems.

### Master These First

1. Basic digit sum
2. Digital root
3. Divisibility by `3`
4. Divisibility by `9`
5. Remainder modulo `3`
6. Remainder modulo `9`
7. Missing digit
8. Multiple missing digits
9. Rearranged digits
10. Carry and digit sum
11. Digit sum of powers
12. Digital-root shortcuts

---

# 56. Practice Checklist

- [ ] Basic digit sum
- [ ] Repeated digit sum
- [ ] Digital root
- [ ] Divisibility by `3`
- [ ] Divisibility by `9`
- [ ] Remainder modulo `3`
- [ ] Remainder modulo `9`
- [ ] Missing digit
- [ ] Smallest missing digit
- [ ] Largest missing digit
- [ ] Multiple missing digits
- [ ] Rearranged digits
- [ ] Large number digit sum
- [ ] Digit sum of powers
- [ ] Carrying patterns
- [ ] Digital-root calculations

---

# 57. Related Topics

- [[Digit Problems]]
- [[Number Formation]]
- [[Reverse of Number]]
- [[Number of Digits]]
- [[Digit-Based Equations]]
- [[Divisibility Rules]]
- [[Divisibility by 3]]
- [[Divisibility by 9]]
- [[Remainders]]
- [[Unit Digit]]

---

# 58. Quick Revision

> [!summary] One-Minute Revision

### Digit Sum

$$
\boxed{
S(N)=\text{sum of all digits}
}
$$

### Divisibility by `3`

$$
\boxed{
S(N)\bmod3=0
}
$$

### Divisibility by `9`

$$
\boxed{
S(N)\bmod9=0
}
$$

### Remainder

$$
\boxed{
N\bmod3=S(N)\bmod3
}
$$

$$
\boxed{
N\bmod9=S(N)\bmod9
}
$$

### Digital Root

$$
\boxed{
DR(N)=1+((N-1)\bmod9)
}
$$

### Missing Digit

$$
\boxed{
\text{Digit sum}+\text{unknown digit}
\rightarrow
\text{divisibility condition}
}
$$

### Golden Memory Trick

> **For `3` and `9`, ignore the size of the number and look at its digit sum.**

### One-Line Recognition

> **Huge number or missing digit + divisibility by `3`/`9` → digit sum is usually the fastest path.**