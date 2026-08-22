---
type: concept
subject: aptitude
topic: "Last Two Digits"
parent: "01. Number System/Unit Digit"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - unit-digit
  - last-two-digits
  - modular-arithmetic
  - powers
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Unit Digit]]"
  - "[[Last Digit]]"
  - "[[Cyclicity]]"
  - "[[Powers and Unit Digits]]"
  - "[[Remainders]]"
---

# Last Two Digits

## 1. Core Concept

> [!summary] Definition
> The **last two digits** of a number are its tens and units digits.
>
> Mathematically, the last two digits are obtained by finding the remainder when the number is divided by `100`.

Therefore:

$$
\boxed{
\text{Last two digits}=N\bmod100
}
$$

### Examples

$$
12345\bmod100=45
$$

$$
987654\bmod100=54
$$

$$
1200\bmod100=0
$$

So:

> **Last two digits → think modulo `100`.**

---

# 2. Fundamental Formula

$$
\boxed{
\text{Last two digits of }N=N\bmod100
}
$$

Since:

$$
100=10^2
$$

we can also write:

$$
\boxed{
N\bmod10^2
}
$$

---

# 3. Only the Last Two Digits Matter

Suppose:

$$
N=987654321
$$

The last two digits are:

$$
\boxed{21}
$$

Therefore:

$$
987654321\bmod100=21
$$

All digits before `21` can be ignored.

---

# 4. Last Two Digits of a Sum

For:

$$
A+B
$$

take the last two digits of each number.

$$
\boxed{
(A+B)\bmod100
=
[(A\bmod100)+(B\bmod100)]\bmod100
}
$$

### Example

Find the last two digits of:

$$
1234+5678
$$

Last two digits:

$$
34+78=112
$$

Therefore:

$$
112\bmod100=12
$$

Answer:

$$
\boxed{12}
$$

---

# 5. Last Two Digits of a Product

For:

$$
A\times B
$$

only the last two digits of each factor are needed.

$$
\boxed{
AB\bmod100
=
[(A\bmod100)(B\bmod100)]\bmod100
}
$$

### Example

Find the last two digits of:

$$
1234\times5678
$$

Take:

$$
34\times78=2652
$$

Then:

$$
2652\bmod100=52
$$

Therefore:

$$
\boxed{52}
$$

---

# 6. Last Two Digits of Multiple Factors

For:

$$
A\times B\times C
$$

reduce each factor modulo `100`.

### Example

Find the last two digits of:

$$
123\times456\times789
$$

Take:

$$
23\times56\times89
$$

First:

$$
23\times56=1288
$$

Keep last two digits:

$$
88
$$

Then:

$$
88\times89=7832
$$

Keep last two digits:

$$
\boxed{32}
$$

---

# 7. Reduce After Every Operation

> [!important] Golden Rule

When calculating modulo `100`, you can reduce the intermediate result after every multiplication.

Example:

$$
23\times56\times89
$$

Instead of calculating the complete product:

$$
23\times56=1288
$$

keep:

$$
88
$$

Then:

$$
88\times89=7832
$$

keep:

$$
\boxed{32}
$$

This keeps calculations small.

---

# 8. Last Two Digits of a Power

For:

$$
a^n
$$

we need:

$$
\boxed{
a^n\bmod100
}
$$

Unlike last-digit questions, the cycle behavior modulo `100` is more complicated.

> [!warning] Important
> Do **not** blindly use the unit-digit cycle table for last-two-digit questions.
>
> Last digit uses modulo `10`.
>
> Last two digits use modulo `100`.

---

# 9. First Reduction

For:

$$
a^n\bmod100
$$

first reduce:

$$
a\bmod100
$$

Then calculate the power.

### Example

Find the last two digits of:

$$
123^2
$$

Only:

$$
23^2
$$

matters.

$$
23^2=529
$$

Therefore:

$$
\boxed29
$$

---

# 10. Example — Simple Power

Find the last two digits of:

$$
37^3
$$

Calculate:

$$
37^2=1369
$$

Keep last two digits:

$$
69
$$

Then:

$$
69\times37=2553
$$

Keep last two digits:

$$
\boxed53
$$

Therefore:

$$
37^3\bmod100=53
$$

---

# 11. Important Pattern — Powers Ending in `0`

If a number ends in `0`, then:

$$
a^2
$$

ends in at least two zeros.

Therefore for:

$$
n\ge2
$$

if `a` is divisible by `10`:

$$
\boxed{
a^n\bmod100=0
}
$$

### Example

$$
120^{10}
$$

ends in:

$$
\boxed{00}
$$

---

# 12. Important Pattern — Powers Ending in `5`

For a number ending in `5`:

$$
5^1=5
$$

$$
5^2=25
$$

$$
5^3=125
$$

$$
5^4=625
$$

For every positive power `n≥2`:

$$
\boxed{
5^n\text{ ends in }25
}
$$

### Example

$$
125^{100}
$$

Last two digits:

$$
\boxed{25}
$$

---

# 13. Important Pattern — Powers Ending in `25`

If a number ends in `25`, then its powers also end in:

$$
\boxed{25}
$$

for positive powers.

### Example

$$
25^{1000}
$$

Last two digits:

$$
\boxed{25}
$$

---

# 14. Important Pattern — Powers Ending in `75`

Similarly:

$$
75^1=75
$$

$$
75^2=5625
$$

$$
75^3=421875
$$

Therefore for positive powers:

$$
\boxed{
75^n\bmod100=75
}
$$

---

# 15. Important Pattern — Powers Ending in `76`

A famous last-two-digit pattern is:

$$
76^1=76
$$

$$
76^2=5776
$$

$$
76^3=438976
$$

Therefore:

$$
\boxed{
76^n\bmod100=76
}
$$

for every positive integer `n`.

This is a useful aptitude shortcut.

---

# 16. Important Pattern — Powers Ending in `01`

If:

$$
a\equiv1\pmod{100}
$$

then:

$$
a^n\equiv1^n
$$

Therefore:

$$
\boxed{
a^n\bmod100=1
}
$$

### Example

$$
301^{100}
$$

Last two digits:

$$
\boxed01
$$

---

# 17. Important Pattern — Powers Ending in `99`

Since:

$$
99\equiv-1\pmod{100}
$$

we get:

$$
99^n\equiv(-1)^n\pmod{100}
$$

Therefore:

### Odd `n`

$$
\boxed{99}
$$

### Even `n`

$$
\boxed{01}
$$

---

# 18. Example — `99^2026`

Since:

$$
99\equiv-1\pmod{100}
$$

and `2026` is even:

$$
99^{2026}\equiv1
$$

Therefore the last two digits are:

$$
\boxed{01}
$$

> [!tip] Remember
> For last-two-digit questions, write `1` as `01`.

---

# 19. Pattern — Numbers Ending in `50`

If a number ends in `50`, its square ends in:

$$
00
$$

because:

$$
50^2=2500
$$

Therefore:

$$
\boxed{
a\equiv50\pmod{100}
\Rightarrow
a^n\equiv0\pmod{100}
}
$$

for `n≥2`.

---

# 20. Pattern — Divisible by `4` and `25`

Since:

$$
100=4\times25
$$

to determine divisibility by `100`, both factors matter:

$$
\boxed{
100\mid N
\iff
4\mid N\text{ and }25\mid N
}
$$

This is especially useful for determining whether the last two digits are `00`.

---

# 21. Last Two Digits `00`

To prove:

$$
N\bmod100=0
$$

show that:

$$
100\mid N
$$

Since:

$$
100=2^2\times5^2
$$

the number must contain at least:

- two factors of `2`
- two factors of `5`

---

# 22. Example — Factorial

Find the last two digits of:

$$
20!
$$

Since:

$$
20!
$$

contains many factors of `2` and `5`, it contains at least:

$$
2^2\times5^2=100
$$

Therefore:

$$
20!\bmod100=0
$$

Answer:

$$
\boxed{00}
$$

---

# 23. Factorial Shortcut

For:

$$
n\ge10
$$

the last two digits of:

$$
n!
$$

are:

$$
\boxed{00}
$$

because `10!` already contains enough factors of `2` and `5` to produce `100`.

---

# 24. Last Two Digits of Powers — Factorization Method

For:

$$
a^n\bmod100
$$

factor:

$$
100=4\times25
$$

You can find:

$$
a^n\bmod4
$$

and:

$$
a^n\bmod25
$$

and then combine the results.

This is useful for difficult last-two-digit problems.

---

# 25. Why Modulo `4` and `25`?

Because:

$$
\boxed{
100=4\times25
}
$$

and:

$$
gcd(4,25)=1
$$

Therefore the pair of remainders modulo `4` and `25` uniquely determines the remainder modulo `100`.

This is an application of the **Chinese Remainder Theorem**.

> [!note] Aptitude Level
> You do not need the full Chinese Remainder Theorem for every question. But recognizing:
>
> $$100=4\times25$$
>
> is extremely useful.

---

# 26. Example — `3^n mod 100`

Suppose we need:

$$
3^{100}\bmod100
$$

We can look for a cycle.

Calculate:

$$
3^1=3
$$

$$
3^2=9
$$

$$
3^3=27
$$

$$
3^4=81
$$

$$
3^5=243\rightarrow43
$$

$$
3^6\rightarrow29
$$

$$
3^7\rightarrow87
$$

$$
3^8\rightarrow61
$$

$$
3^9\rightarrow83
$$

$$
3^{10}\rightarrow49
$$

Continuing eventually produces a repeating cycle.

For such problems, **modular exponentiation or CRT decomposition** is generally more efficient than writing a long cycle by hand.

---

# 27. Last Two Digits — Repeated Squaring

For large powers:

$$
a^n\bmod100
$$

use repeated squaring.

### Example

Find:

$$
7^{20}\bmod100
$$

Calculate:

$$
7^2=49
$$

Then:

$$
7^4=49^2=2401
$$

Keep last two digits:

$$
01
$$

Therefore:

$$
7^4\equiv1\pmod{100}
$$

Then:

$$
7^{20}=(7^4)^5
$$

Therefore:

$$
7^{20}\equiv1^5
$$

Hence:

$$
\boxed{01}
$$

---

# 28. Important Pattern — If a Power Becomes `01`

If:

$$
a^k\equiv1\pmod{100}
$$

then:

$$
a^{kq}\equiv1\pmod{100}
$$

for any positive integer `q`.

This allows very large exponents to be reduced.

---

# 29. Example — `21^n`

Observe:

$$
21^2=441
$$

Therefore:

$$
21^2\equiv41\pmod{100}
$$

Then:

$$
21^4\equiv41^2
$$

$$
=1681
$$

Therefore:

$$
21^4\equiv81\pmod{100}
$$

Continue squaring as needed for the required exponent.

> [!tip] Pattern
> For large powers modulo `100`, repeatedly square and keep only the last two digits.

---

# 30. Last Two Digits of a Sum

Example:

Find the last two digits of:

$$
2^{100}+3^{100}
$$

This is more difficult than the corresponding last-digit question.

The correct method is:

1. Find each term modulo `100`.
2. Add.
3. Take modulo `100`.

Do **not** use only the unit-digit cycles.

---

# 31. Last Two Digits of a Product

Similarly:

$$
2^{100}\times3^{100}\bmod100
$$

must be calculated using modulo `100`.

You cannot simply calculate the last digit.

---

# 32. Leading Zero Rule

If the remainder is less than `10`, write it using two digits.

For example:

$$
7\bmod100=7
$$

But the **last two digits** are:

$$
\boxed{07}
$$

Similarly:

$$
1\rightarrow01
$$

$$
0\rightarrow00
$$

> [!important] Exam Tip
> Last **two digits** means always display exactly two digits.

---

# 33. Examples of Formatting

| Number | Last two digits |
|---:|---:|
| `7` | `07` |
| `1` | `01` |
| `0` | `00` |
| `45` | `45` |
| `123` | `23` |
| `1007` | `07` |

---

# 34. Important Difference

### Last Digit

$$
\boxed{
N\bmod10
}
$$

### Last Two Digits

$$
\boxed{
N\bmod100
}
$$

### Last Three Digits

$$
\boxed{
N\bmod1000
}
$$

Therefore:

$$
\boxed{
\text{Last }k\text{ digits}=N\bmod10^k
}
$$

---

# 35. Last Two Digits of Powers — Recognition

When you see:

$$
a^n
$$

and the question asks for the **last two digits**, immediately think:

$$
\boxed{\bmod100}
$$

Then ask:

1. Does the base end in `0`?
2. Does it end in `5`?
3. Is it close to `100`, such as `99`?
4. Does repeated squaring become easy?
5. Can modulo `4` and `25` simplify it?
6. Is there a useful repeating power pattern?

---

# 36. Common Special Bases

> [!important] Memorize These

### `01`

$$
01^n\rightarrow01
$$

### `25`

$$
25^n\rightarrow25
$$

for positive `n`.

### `50`

$$
50^n\rightarrow00
$$

for `n≥2`.

### `75`

$$
75^n\rightarrow75
$$

for positive `n`.

### `76`

$$
76^n\rightarrow76
$$

for positive `n`.

### `99`

$$
99^n\rightarrow
\begin{cases}
99,&n\text{ odd}\\
01,&n\text{ even}
\end{cases}
$$

---

# 37. Why `25` Is Stable

Consider:

$$
25^2=625
$$

Last two digits:

$$
25
$$

Therefore:

$$
25^2\equiv25\pmod{100}
$$

Multiplying by another `25` keeps:

$$
25
$$

So:

$$
\boxed{
25^n\equiv25\pmod{100}
}
$$

for positive `n`.

---

# 38. Why `76` Is Stable

Since:

$$
76^2=5776
$$

we have:

$$
76^2\equiv76\pmod{100}
$$

Therefore:

$$
76^n\equiv76\pmod{100}
$$

for positive `n`.

This is called an **idempotent pattern**.

---

# 39. Idempotent Pattern

If:

$$
a^2\equiv a\pmod m
$$

then:

$$
a^n\equiv a\pmod m
$$

for every positive integer `n`.

For modulo `100`, useful examples include:

$$
\boxed{25,\ 76}
$$

because:

$$
25^2\equiv25\pmod{100}
$$

and:

$$
76^2\equiv76\pmod{100}
$$

---

# 40. Pattern — `99 = -1`

This is one of the easiest last-two-digit patterns:

$$
99\equiv-1\pmod{100}
$$

Therefore:

$$
99^n\equiv(-1)^n\pmod{100}
$$

Hence:

$$
\boxed{
99^n=
\begin{cases}
99,&n\text{ odd}\\
01,&n\text{ even}
\end{cases}
}
$$

---

# 41. Pattern — `01 = 1`

Since:

$$
01\equiv1\pmod{100}
$$

therefore:

$$
\boxed{
01^n\equiv01\pmod{100}
}
$$

---

# 42. Pattern — Multiples of 10

If:

$$
a=10k
$$

then:

$$
a^2=100k^2
$$

Therefore:

$$
\boxed{
a^n\equiv00\pmod{100}
}
$$

for every:

$$
n\ge2
$$

---

# 43. Example — `130^50`

Since:

$$
130=10\times13
$$

we have:

$$
130^2
$$

containing:

$$
10^2=100
$$

Therefore:

$$
\boxed{130^{50}\text{ ends in }00}
$$

---

# 44. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Using modulo `10` when the question asks for two digits.
- ❌ Using the unit-digit cycle directly for modulo `100`.
- ❌ Forgetting leading zeros.
- ❌ Calculating huge powers directly.
- ❌ Forgetting that `100=4×25`.
- ❌ Assuming every base has a short cycle like modulo `10`.
- ❌ Forgetting special patterns such as `25`, `76`, and `99`.
- ❌ Confusing `7` with `07` when the question asks for two digits.
- ❌ Combining powers with different bases incorrectly.

---

# 45. Exam Strategy

> [!tip] Fast Method

For:

$$
a^n
$$

asking for the last two digits:

### Step 1

Reduce:

$$
a\bmod100
$$

### Step 2

Check for special patterns:

$$
00,\ 01,\ 25,\ 50,\ 75,\ 76,\ 99
$$

### Step 3

If no shortcut exists, use:

- repeated squaring
- modular arithmetic
- modulo `4` and `25`
- cycle/pattern recognition

### Step 4

Keep only:

$$
\boxed{2\text{ digits}}
$$

after every major operation.

---

# 46. Formula Sheet

> [!important] Must Remember

### Last Two Digits

$$
\boxed{
N\bmod100
}
$$

### General Last `k` Digits

$$
\boxed{
N\bmod10^k
}
$$

### Sum

$$
\boxed{
(A+B)\bmod100
=
[(A\bmod100)+(B\bmod100)]\bmod100
}
$$

### Product

$$
\boxed{
AB\bmod100
=
[(A\bmod100)(B\bmod100)]\bmod100
}
$$

### Power

$$
\boxed{
a^n\bmod100
=
[(a\bmod100)^n]\bmod100
}
$$

### Modulo `100` Factorization

$$
\boxed{
100=4\times25
}
$$

---

# 47. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
\text{Last two digits}=N\bmod100
}
$$

### Pattern 2

$$
\boxed{
a^n\bmod100
}
$$

→ Reduce the base modulo `100`.

### Pattern 3

$$
\boxed{
25^n\rightarrow25
}
$$

### Pattern 4

$$
\boxed{
76^n\rightarrow76
}
$$

### Pattern 5

$$
\boxed{
75^n\rightarrow75
}
$$

### Pattern 6

$$
\boxed{
99^n=
\begin{cases}
99,&n\text{ odd}\\
01,&n\text{ even}
\end{cases}
}
$$

### Pattern 7

If `a` ends in `0`:

$$
\boxed{
a^n\rightarrow00,\quad n\ge2
}
$$

### Pattern 8

If:

$$
a^2\equiv1\pmod{100}
$$

then powers can often be reduced using the parity of `n`.

### Pattern 9

$$
\boxed{
100=4\times25
}
$$

Use modulo `4` and `25` when direct calculation is difficult.

---

# 48. HCL Preparation Priority

**Priority:** 🔥🔥 Very High

Last-two-digit questions are slightly more advanced than ordinary unit-digit questions.

### Master These First

1. Modulo `100`
2. Last-two-digit addition
3. Last-two-digit multiplication
4. Last-two-digit powers
5. Special bases `25`, `75`, `76`
6. `99 = -1 mod 100`
7. Powers of numbers ending in `0`
8. Factorial ending in `00`
9. Repeated squaring
10. `100 = 4 × 25`
11. Leading-zero formatting
12. General last-`k`-digits pattern

---

# 49. Practice Checklist

- [ ] Last two digits of a number
- [ ] Last two digits of sums
- [ ] Last two digits of products
- [ ] Last two digits of squares
- [ ] Last two digits of cubes
- [ ] Powers ending in `0`
- [ ] Powers ending in `5`
- [ ] Powers ending in `25`
- [ ] Powers ending in `75`
- [ ] Powers ending in `76`
- [ ] Powers ending in `99`
- [ ] Factorial last two digits
- [ ] Repeated squaring
- [ ] Modulo `4` and `25`
- [ ] Large exponent problems

---

# 50. Related Topics

- [[Unit Digit]]
- [[Last Digit]]
- [[Last Two Digits]]
- [[Cyclic Remainders]]
- [[Remainders]]
- [[Large Number Remainders]]
- [[Powers and Unit Digits]]
- [[Factorization]]
- [[Factors]]

---

# 51. Quick Revision

> [!summary] One-Minute Revision

### Main Formula

$$
\boxed{
\text{Last two digits}=N\bmod100
}
$$

### General Formula

$$
\boxed{
\text{Last }k\text{ digits}=N\bmod10^k
}
$$

### Special Patterns

$$
\boxed{
25^n\rightarrow25
}
$$

$$
\boxed{
75^n\rightarrow75
}
$$

$$
\boxed{
76^n\rightarrow76
}
$$

$$
\boxed{
99^n\rightarrow
\begin{cases}
99,&n\text{ odd}\\
01,&n\text{ even}
\end{cases}
}
$$

$$
\boxed{
a^n\rightarrow00
}
$$

when `a` is divisible by `10` and `n≥2`.

### Important Factorization

$$
\boxed{
100=4\times25
}
$$

### Golden Memory Trick

> **Last digit → modulo `10`. Last two digits → modulo `100`.**

### One-Line Recognition

> **Question asks for the last two digits → immediately think `mod 100`, then look for a special pattern before calculating.**