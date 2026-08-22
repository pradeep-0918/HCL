---
type: concept
subject: aptitude
topic: "Large Number Remainders"
parent: "01. Number System/Remainders"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - remainders
  - modular-arithmetic
  - large-numbers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Remainders]]"
  - "[[Basic Remainder]]"
  - "[[Remainder Theorem]]"
  - "[[Cyclic Remainders]]"
  - "[[Remainder Patterns]]"
---

# Large Number Remainders

## 1. Core Concept

> [!summary] Main Idea
> When a number is extremely large, **do not calculate the entire number**.
>
> Reduce the number step by step using its remainder.

The central rule is:

$$
\boxed{
a\equiv r\pmod m
}
$$

This means `a` and `r` leave the same remainder when divided by `m`.

Therefore, for calculations:

$$
\boxed{
a\rightarrow a\bmod m
}
$$

before performing the operation.

---

# 2. Golden Rule

For modulus `m`:

$$
\boxed{
(a+b)\bmod m
=
[(a\bmod m)+(b\bmod m)]\bmod m
}
$$

$$
\boxed{
(a-b)\bmod m
=
[(a\bmod m)-(b\bmod m)]\bmod m
}
$$

$$
\boxed{
(ab)\bmod m
=
[(a\bmod m)(b\bmod m)]\bmod m
}
$$

$$
\boxed{
a^n\bmod m
=
[(a\bmod m)^n]\bmod m
}
$$

These rules allow huge numbers to be reduced into small numbers.

---

# 3. Why We Reduce First

Suppose we need:

$$
987654321\times123456789\bmod7
$$

Calculating the full product is unnecessary.

Instead:

$$
987654321\bmod7
$$

and:

$$
123456789\bmod7
$$

Then multiply the small remainders.

> [!tip] Exam Principle
>
> **Large number → small remainder → calculation becomes easy.**

---

# 4. Example — Large Multiplication

Find:

$$
123456\times789012\bmod7
$$

First:

$$
123456\bmod7=4
$$

and:

$$
789012\bmod7=3
$$

Therefore:

$$
123456\times789012\bmod7
$$

becomes:

$$
4\times3=12
$$

Then:

$$
12\bmod7=5
$$

Therefore:

$$
\boxed5
$$

---

# 5. Large Powers

The most common large-number pattern is:

$$
a^n\bmod m
$$

For example:

$$
7^{100}\bmod5
$$

Since:

$$
7\bmod5=2
$$

we need:

$$
2^{100}\bmod5
$$

Instead of calculating `2^100`, look for a repeating pattern.

This leads to **cyclic remainders**, which is the next topic in your syllabus.

---

# 6. Example — Easy Large Power

Find:

$$
13^{50}\bmod6
$$

Since:

$$
13\bmod6=1
$$

we get:

$$
13^{50}\bmod6
=
1^{50}\bmod6
$$

Therefore:

$$
\boxed1
$$

> [!important] Shortcut
> If:
>
> $$a\bmod m=1$$
>
> then:
>
> $$\boxed{a^n\bmod m=1}$$
>
> for every positive integer `n`.

---

# 7. Remainder `0` Shortcut

If:

$$
a\bmod m=0
$$

then:

$$
a^n\bmod m=0
$$

for every positive integer `n`.

### Example

Find:

$$
24^{100}\bmod6
$$

Since:

$$
24\bmod6=0
$$

therefore:

$$
\boxed0
$$

---

# 8. Remainder `-1` Shortcut

If:

$$
a\equiv-1\pmod m
$$

then:

$$
a^n\equiv(-1)^n\pmod m
$$

Therefore:

### Even `n`

$$
\boxed1
$$

### Odd `n`

$$
\boxed{-1\equiv m-1\pmod m}
$$

### Example

Find:

$$
9^{101}\bmod10
$$

Since:

$$
9\equiv-1\pmod{10}
$$

and `101` is odd:

$$
\boxed9
$$

---

# 9. Breaking a Large Number Into Parts

A large decimal number can be written using powers of `10`.

For example:

$$
123456
=
123\times1000+456
$$

If calculating modulo `m`, you can reduce each part.

This is particularly useful when:

- the number has many digits
- the divisor is not `10`
- direct division is difficult

---

# 10. Example — Split the Number

Find:

$$
123456\bmod7
$$

Write:

$$
123456=123000+456
$$

Then:

$$
123000=123\times1000
$$

You can reduce each component modulo `7`.

However, for aptitude exams, direct long division or digit-by-digit modular reduction is often faster for a number of this size.

---

# 11. Digit-by-Digit Remainder Method

This is extremely useful for very large decimal numbers.

Suppose we want:

$$
N\bmod d
$$

Read digits from left to right.

For each new digit:

$$
\boxed{
r_{\text{new}}
=
(10r_{\text{old}}+\text{digit})\bmod d
}
$$

Start with:

$$
r=0
$$

---

# 12. Example — Digit-by-Digit Method

Find:

$$
12345\bmod7
$$

Start:

$$
r=0
$$

Read `1`:

$$
r=(10(0)+1)\bmod7
$$

$$
r=1
$$

Read `2`:

$$
r=(10(1)+2)\bmod7
$$

$$
=12\bmod7
$$

$$
r=5
$$

Read `3`:

$$
r=(10(5)+3)\bmod7
$$

$$
=53\bmod7
$$

$$
r=4
$$

Read `4`:

$$
r=(10(4)+4)\bmod7
$$

$$
=44\bmod7
$$

$$
r=2
$$

Read `5`:

$$
r=(10(2)+5)\bmod7
$$

$$
=25\bmod7
$$

$$
r=4
$$

Therefore:

$$
\boxed{12345\bmod7=4}
$$

---

# 13. Why the Digit Method Works

Suppose the current number is:

$$
N
$$

and a new digit `d` is appended.

The new number becomes:

$$
10N+d
$$

Therefore, modulo `m`:

$$
10N+d
\equiv
10(N\bmod m)+d
\pmod m
$$

Hence:

$$
\boxed{
r_{\text{new}}
=
(10r_{\text{old}}+d)\bmod m
}
$$

---

# 14. Large Number Divisibility

If:

$$
N\bmod d=0
$$

then:

$$
\boxed{d\mid N}
$$

Therefore, large-number remainder questions can also become divisibility questions.

For example:

> Is a huge number divisible by `3`?

Instead of dividing the entire number, use the divisibility rule for `3`.

This connects:

$$
\boxed{
\text{Divisibility Rules}
\leftrightarrow
\text{Remainders}
}
$$

---

# 15. Modulo `10`

For any integer `N`:

$$
\boxed{
N\bmod10
=
\text{last digit}
}
$$

Example:

$$
987654321\bmod10=1
$$

Therefore:

$$
\boxed1
$$

---

# 16. Modulo `100`

For:

$$
N\bmod100
$$

only the last two digits matter.

$$
\boxed{
N\bmod100
=
\text{last two digits}
}
$$

Example:

$$
987654321\bmod100=21
$$

Therefore:

$$
\boxed{21}
$$

---

# 17. Modulo `1000`

Similarly:

$$
\boxed{
N\bmod1000
=
\text{last three digits}
}
$$

Example:

$$
987654321\bmod1000=321
$$

Therefore:

$$
\boxed{321}
$$

---

# 18. General Power of 10 Rule

For:

$$
10^k
$$

the remainder is determined by the last `k` digits.

$$
\boxed{
N\bmod10^k
=
\text{last }k\text{ digits}
}
$$

Examples:

$$
\bmod10
\rightarrow
1\text{ digit}
$$

$$
\bmod100
\rightarrow
2\text{ digits}
$$

$$
\bmod1000
\rightarrow
3\text{ digits}
$$

$$
\bmod10000
\rightarrow
4\text{ digits}
$$

---

# 19. Large Sum

Suppose:

$$
N=a_1+a_2+\cdots+a_n
$$

Then:

$$
\boxed{
N\bmod m
=
[(a_1\bmod m)+\cdots+(a_n\bmod m)]\bmod m
}
$$

### Example

Find:

$$
123456+789012\bmod9
$$

Since:

$$
123456\bmod9=3
$$

and:

$$
789012\bmod9=3
$$

Therefore:

$$
3+3=6
$$

Hence:

$$
\boxed6
$$

---

# 20. Large Difference

For:

$$
A-B
$$

reduce both numbers:

$$
\boxed{
(A-B)\bmod m
=
[(A\bmod m)-(B\bmod m)]\bmod m
}
$$

If the result is negative, add `m` until it falls into:

$$
0\le r<m
$$

---

# 21. Example — Negative Intermediate Remainder

Find:

$$
23-17\bmod6
$$

We have:

$$
23\bmod6=5
$$

and:

$$
17\bmod6=5
$$

Therefore:

$$
5-5=0
$$

Answer:

$$
\boxed0
$$

---

# 22. Example With Negative Result

Suppose:

$$
17-25\bmod6
$$

Then:

$$
17\bmod6=5
$$

$$
25\bmod6=1
$$

Therefore:

$$
5-1=4
$$

Answer:

$$
\boxed4
$$

---

# 23. Large Product — Reduce Early

Find:

$$
123\times456\times789\bmod5
$$

Reduce:

$$
123\bmod5=3
$$

$$
456\bmod5=1
$$

$$
789\bmod5=4
$$

Then:

$$
3\times1\times4=12
$$

Therefore:

$$
12\bmod5=2
$$

Answer:

$$
\boxed2
$$

> [!tip] Golden Habit
>
> **Reduce after every multiplication.**

---

# 24. Large Power — Repeated Squaring

For extremely large exponents, repeated squaring can be used.

Suppose:

$$
a^n\bmod m
$$

Instead of multiplying `a` `n` times:

1. Square the base.
2. Reduce modulo `m`.
3. Continue squaring.
4. Use the binary representation of `n`.

This is called **modular exponentiation**.

---

# 25. Example — Repeated Squaring

Find:

$$
3^{10}\bmod7
$$

Start:

$$
3^2=9\equiv2\pmod7
$$

Then:

$$
3^4\equiv2^2=4\pmod7
$$

Then:

$$
3^8\equiv4^2=16\equiv2\pmod7
$$

Now:

$$
3^{10}=3^8\times3^2
$$

Therefore:

$$
3^{10}\equiv2\times2
$$

$$
=4
$$

Hence:

$$
\boxed4
$$

---

# 26. When to Use Which Method?

| Situation | Best method |
|---|---|
| Small number | Direct division |
| Large multiplication | Reduce each factor |
| Large sum | Reduce each term |
| Large power | Cyclicity / modular exponentiation |
| Huge decimal number | Digit-by-digit |
| Modulo `10` | Last digit |
| Modulo `100` | Last two digits |
| Modulo `1000` | Last three digits |
| Divisibility by `3` | Digit sum |
| Divisibility by `9` | Digit sum |
| Divisibility by `11` | Alternating digit sum |

---

# 27. Important Pattern — Factor With Remainder Zero

If:

$$
a\equiv0\pmod m
$$

then:

$$
\boxed{
a\times b\times c\equiv0\pmod m
}
$$

No further calculation is required.

---

# 28. Important Pattern — Factor With Remainder One

If:

$$
a\equiv1\pmod m
$$

then:

$$
a^n\equiv1\pmod m
$$

Therefore:

$$
\boxed1
$$

for any positive `n`.

---

# 29. Important Pattern — Factor With Remainder `-1`

If:

$$
a\equiv-1\pmod m
$$

then:

$$
a^n\equiv(-1)^n\pmod m
$$

Therefore:

$$
\boxed{
\begin{cases}
1 & n\text{ even}\\
m-1 & n\text{ odd}
\end{cases}
}
$$

---

# 30. Important Pattern — Same Remainder

If:

$$
a\equiv b\pmod m
$$

then:

$$
\boxed{
a-b\equiv0\pmod m
}
$$

Therefore:

$$
\boxed{
m\mid(a-b)
}
$$

This is useful for simplifying large expressions.

---

# 31. Large Number Using Divisibility

Suppose:

$$
N=10^{100}+1
$$

Find the remainder when divided by `9`.

Since:

$$
10\equiv1\pmod9
$$

therefore:

$$
10^{100}\equiv1^{100}
$$

$$
\equiv1\pmod9
$$

So:

$$
10^{100}+1
\equiv1+1
$$

$$
\boxed2
$$

---

# 32. Large Power of 10 Modulo 9

Because:

$$
10\equiv1\pmod9
$$

we immediately get:

$$
\boxed{
10^n\equiv1\pmod9
}
$$

for every positive integer `n`.

This is a very common aptitude shortcut.

---

# 33. Large Power of 10 Modulo 11

Since:

$$
10\equiv-1\pmod{11}
$$

we get:

$$
10^n\equiv(-1)^n\pmod{11}
$$

Therefore:

### Even `n`

$$
\boxed1
$$

### Odd `n`

$$
\boxed{10}
$$

---

# 34. Example

Find:

$$
10^{2026}\bmod11
$$

Since:

$$
10\equiv-1\pmod{11}
$$

and `2026` is even:

$$
10^{2026}\equiv1
$$

Therefore:

$$
\boxed1
$$

---

# 35. Large Number Modulo 3 and 9

For modulo `3`:

$$
\boxed{
N\bmod3
=
(\text{sum of digits})\bmod3
}
$$

For modulo `9`:

$$
\boxed{
N\bmod9
=
(\text{sum of digits})\bmod9
}
$$

### Example

Find:

$$
987654321\bmod9
$$

Digit sum:

$$
9+8+7+6+5+4+3+2+1
$$

$$
=45
$$

Then:

$$
45\bmod9=0
$$

Therefore:

$$
\boxed0
$$

---

# 36. Large Number Modulo 11

Use the alternating sum of digits.

For:

$$
987654321
$$

calculate:

$$
(1+3+5+7+9)-(2+4+6+8)
$$

$$
=25-20
$$

$$
=5
$$

Therefore:

$$
987654321\bmod11=5
$$

---

# 37. Important Caution About Divisibility Rules

Divisibility rules are shortcuts for particular divisors.

Do not assume the digit-sum rule works for every modulus.

For example:

$$
\boxed{
\text{Digit sum rule is directly useful for }3\text{ and }9
}
$$

The last-digit rule is useful for:

$$
2,\ 5,\ 10
$$

The last-two-digit rule is useful for:

$$
4,\ 25,\ 100
$$

The last-three-digit rule is useful for:

$$
8,\ 125,\ 1000
$$

---

# 38. Large Number + Factorization

If a large expression can be factored, factorization may make the remainder much easier.

Example:

$$
999999
$$

can be written as:

$$
10^6-1
$$

Therefore, modulo `9`:

$$
10^6-1
\equiv1-1
$$

$$
\boxed0
$$

---

# 39. Important Pattern — Rewrite Around a Multiple

If a number is close to a convenient multiple:

$$
N=kd\pm r
$$

then the remainder is immediately determined.

### Example

Find:

$$
9997\bmod10
$$

Write:

$$
9997=10000-3
$$

Therefore:

$$
9997\bmod10
=
-3\bmod10
$$

$$
\boxed7
$$

---

# 40. Important Pattern — Use a Convenient Base

For powers involving `10`, look for:

$$
10\equiv1\pmod9
$$

$$
10\equiv-1\pmod{11}
$$

For other moduli, look for a small equivalent remainder.

### Example

Modulo `7`:

$$
10\equiv3
$$

Therefore:

$$
10^n\bmod7
=
3^n\bmod7
$$

This reduces the base.

---

# 41. Modular Exponentiation Formula

For:

$$
a^n\bmod m
$$

you can repeatedly reduce:

$$
a^2\bmod m
$$

$$
a^4\bmod m
$$

$$
a^8\bmod m
$$

and so on.

This gives:

$$
\boxed{
O(\log n)
}
$$

time computationally.

For aptitude questions, however, **cyclicity is often faster** when the pattern is short.

---

# 42. Exam Decision Tree

> [!tip] Fast Method Selection

### Is the number small?

Use:

$$
\boxed{\text{Direct division}}
$$

### Is it a large product?

Use:

$$
\boxed{\text{Reduce each factor}}
$$

### Is it a large sum?

Use:

$$
\boxed{\text{Reduce each term}}
$$

### Is it a huge power?

Use:

$$
\boxed{\text{Cyclicity / modular exponentiation}}
$$

### Is the divisor `10^k`?

Use:

$$
\boxed{\text{Last }k\text{ digits}}
$$

### Is the divisor `3` or `9`?

Use:

$$
\boxed{\text{Digit sum}}
$$

### Is the divisor `11`?

Use:

$$
\boxed{\text{Alternating digit sum}}
$$

---

# 43. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Calculating the entire huge number.
- ❌ Forgetting to reduce intermediate results.
- ❌ Forgetting to reduce the final result.
- ❌ Using the wrong divisibility rule.
- ❌ Confusing `-1` modulo `m` with `-1` as the final remainder.
- ❌ Forgetting that the standard remainder must satisfy:
>
> $$0\le r<m$$
>
> ❌ Using a cycle before establishing that a cycle exists.
- ❌ Multiplying huge numbers directly.
- ❌ Forgetting the difference between modulo `10`, `100`, and `1000`.

---

# 44. Formula Sheet

> [!important] Must Remember

### Addition

$$
\boxed{
(a+b)\bmod m
=
[(a\bmod m)+(b\bmod m)]\bmod m
}
$$

### Subtraction

$$
\boxed{
(a-b)\bmod m
=
[(a\bmod m)-(b\bmod m)]\bmod m
}
$$

### Multiplication

$$
\boxed{
(ab)\bmod m
=
[(a\bmod m)(b\bmod m)]\bmod m
}
$$

### Power

$$
\boxed{
a^n\bmod m
=
[(a\bmod m)^n]\bmod m
}
$$

### Digit-by-Digit

$$
\boxed{
r_{\text{new}}
=
(10r_{\text{old}}+d)\bmod m
}
$$

### Power of 10

$$
\boxed{
N\bmod10^k
=
\text{last }k\text{ digits}
}
$$

---

# 45. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — Reduce First

$$
\boxed{
a\rightarrow a\bmod m
}
$$

### Pattern 2 — Product

$$
\boxed{
ab\bmod m
=
[(a\bmod m)(b\bmod m)]\bmod m
}
$$

### Pattern 3 — Sum

$$
\boxed{
(a+b)\bmod m
=
[(a\bmod m)+(b\bmod m)]\bmod m
}
$$

### Pattern 4 — Zero

$$
\boxed{
a\equiv0\pmod m
\Rightarrow
a^n\equiv0\pmod m
}
$$

### Pattern 5 — One

$$
\boxed{
a\equiv1\pmod m
\Rightarrow
a^n\equiv1\pmod m
}
$$

### Pattern 6 — Negative One

$$
\boxed{
a\equiv-1\pmod m
}
$$

Then:

$$
\boxed{
a^n=
\begin{cases}
1 & n\text{ even}\\
m-1 & n\text{ odd}
\end{cases}
}
$$

### Pattern 7 — Digit Sum

For `3` and `9`:

$$
\boxed{\text{Use digit sum}}
$$

### Pattern 8 — Last Digits

$$
\boxed{
\bmod10^k
\rightarrow
\text{last }k\text{ digits}
}
$$

### Pattern 9 — Digit-by-Digit

$$
\boxed{
r_{\text{new}}
=
(10r+d)\bmod m
}
$$

---

# 46. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

This topic is the foundation for difficult remainder questions involving:

- huge powers
- huge products
- huge decimal numbers
- modular arithmetic
- divisibility
- cyclicity
- unit digits

### Master These First

1. Reduce before calculation
2. Modular addition
3. Modular subtraction
4. Modular multiplication
5. Large powers
6. Remainder `0`
7. Remainder `1`
8. Remainder `-1`
9. Digit-by-digit method
10. Powers of `10`
11. Digit-sum shortcuts
12. Modular exponentiation

---

# 47. Practice Checklist

- [ ] Large multiplication remainders
- [ ] Large addition remainders
- [ ] Large subtraction remainders
- [ ] Large power remainders
- [ ] Numbers with remainder `0`
- [ ] Numbers with remainder `1`
- [ ] Numbers with remainder `-1`
- [ ] Digit-by-digit remainder
- [ ] Modulo `10`
- [ ] Modulo `100`
- [ ] Modulo `1000`
- [ ] Modulo `3`
- [ ] Modulo `9`
- [ ] Modulo `11`
- [ ] Modular exponentiation

---

# 48. Related Topics

- [[Remainders]]
- [[Basic Remainder]]
- [[Remainder Theorem]]
- [[Cyclic Remainders]]
- [[Remainder Patterns]]
- [[Divisibility Rules]]
- [[Unit Digit]]
- [[Last Digit]]
- [[Last Two Digits]]
- [[Prime and Composite Numbers]]

---

# 49. Quick Revision

> [!summary] One-Minute Revision

### Golden Rule

$$
\boxed{
\text{Reduce first, calculate second}
}
$$

### Addition

$$
\boxed{
(a+b)\bmod m
=
[(a\bmod m)+(b\bmod m)]\bmod m
}
$$

### Multiplication

$$
\boxed{
ab\bmod m
=
[(a\bmod m)(b\bmod m)]\bmod m
}
$$

### Powers

$$
\boxed{
a^n\bmod m
=
[(a\bmod m)^n]\bmod m
}
$$

### Special Remainders

$$
a\equiv0
\Rightarrow
a^n\equiv0
$$

$$
a\equiv1
\Rightarrow
a^n\equiv1
$$

$$
a\equiv-1
\Rightarrow
a^n\equiv(-1)^n
$$

### Last Digits

$$
\boxed{
\bmod10^k
\rightarrow
\text{last }k\text{ digits}
}
$$

### Digit-by-Digit

$$
\boxed{
r_{\text{new}}=(10r+d)\bmod m
}
$$

### Golden Memory Trick

> **Never fight a huge number. Replace it with its small remainder.**

### One-Line Recognition

> **Huge number → reduce modulo the divisor → solve the small problem.**