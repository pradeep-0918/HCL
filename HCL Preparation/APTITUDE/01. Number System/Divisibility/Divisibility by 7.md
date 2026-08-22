---
type: concept
subject: aptitude
topic: "Divisibility by 7"
parent: "01. Number System/Divisibility"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - divisibility
  - divisibility-by-7
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 4]]"
  - "[[Divisibility by 5]]"
  - "[[Divisibility by 6]]"
  - "[[Divisibility by 8]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
---

# Divisibility by 7

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `7` if division by `7` leaves remainder `0`.

Mathematically:

$$
\boxed{n\equiv0\pmod7}
$$

or:

$$
\boxed{n=7k}
$$

where `k` is an integer.

Unlike `2`, `3`, `4`, and `5`, there is no simple rule based only on one final digit.

The most useful aptitude shortcut is:

$$
\boxed{\text{Double the last digit and subtract it from the remaining number}}
$$

---

# 2. Divisibility Rule

For a number:

$$
N=10a+b
$$

where `b` is the last digit:

1. Separate the last digit.
2. Double the last digit.
3. Subtract it from the remaining number.
4. Repeat if necessary.
5. If the final result is divisible by `7`, the original number is divisible by `7`.

### Shortcut

$$
\boxed{a-2b}
$$

If:

$$
a-2b
$$

is divisible by `7`, then:

$$
10a+b
$$

is divisible by `7`.

---

# 3. Why the Rule Works

We know:

$$
10\equiv3\pmod7
$$

Also:

$$
3^{-1}\equiv5\pmod7
$$

because:

$$
3\times5=15\equiv1\pmod7
$$

For:

$$
N=10a+b
$$

we have:

$$
N\equiv3a+b\pmod7
$$

Multiplying by `5`:

$$
5N\equiv15a+5b\pmod7
$$

Since:

$$
15\equiv1\pmod7
$$

we get:

$$
5N\equiv a+5b\pmod7
$$

and since:

$$
5\equiv-2\pmod7
$$

we get:

$$
5N\equiv a-2b\pmod7
$$

Therefore:

$$
\boxed{N\text{ divisible by 7}\iff a-2b\text{ divisible by 7}}
$$

> [!note] Aptitude Level
> You do **not** need to reproduce this proof in an exam. Remember the shortcut:
>
> **Double the last digit → subtract from remaining number.**

---

# 4. Basic Example

Check whether:

$$
203
$$

is divisible by `7`.

Separate last digit:

$$
3
$$

Double:

$$
3\times2=6
$$

Remaining number:

$$
20
$$

Subtract:

$$
20-6=14
$$

Since:

$$
14=7\times2
$$

therefore:

$$
\boxed{203\text{ is divisible by 7}}
$$

---

# 5. Example — 371

Check:

$$
371
$$

Last digit:

$$
1
$$

Double:

$$
2
$$

Remaining:

$$
37
$$

Subtract:

$$
37-2=35
$$

Since:

$$
35=7\times5
$$

therefore:

$$
\boxed{371\text{ is divisible by 7}}
$$

---

# 6. Example — 672

Check:

$$
672
$$

Last digit:

$$
2
$$

Double:

$$
4
$$

Remaining:

$$
67
$$

Subtract:

$$
67-4=63
$$

Since:

$$
63=7\times9
$$

therefore:

$$
\boxed{672\text{ is divisible by 7}}
$$

---

# 7. Example — 325

Check:

$$
325
$$

Last digit:

$$
5
$$

Double:

$$
10
$$

Remaining:

$$
32
$$

Subtract:

$$
32-10=22
$$

`22` is not divisible by `7`.

Therefore:

$$
\boxed{325\text{ is not divisible by 7}}
$$

---

# 8. Repeating the Rule

Sometimes one application does not produce an obvious answer.

### Example

Check:

$$
1372
$$

Last digit:

$$
2
$$

Double:

$$
4
$$

Remaining:

$$
137
$$

Subtract:

$$
137-4=133
$$

Again:

Last digit:

$$
3
$$

Double:

$$
6
$$

Remaining:

$$
13
$$

Subtract:

$$
13-6=7
$$

Since:

$$
7
$$

is divisible by `7`:

$$
\boxed{1372\text{ is divisible by 7}}
$$

---

# 9. Example With Multiple Repetitions

Check:

$$
123456
$$

### First step

Last digit:

$$
6
$$

Double:

$$
12
$$

Remaining:

$$
12345
$$

Subtract:

$$
12345-12=12333
$$

### Second step

Last digit:

$$
3
$$

Double:

$$
6
$$

Remaining:

$$
1233
$$

Subtract:

$$
1233-6=1227
$$

### Third step

Last digit:

$$
7
$$

Double:

$$
14
$$

Remaining:

$$
122
$$

Subtract:

$$
122-14=108
$$

### Fourth step

Last digit:

$$
8
$$

Double:

$$
16
$$

Remaining:

$$
10
$$

Subtract:

$$
10-16=-6
$$

`-6` is not divisible by `7`.

Therefore:

$$
\boxed{123456\text{ is not divisible by 7}}
$$

---

# 10. Negative Results Are Allowed

The process can produce a negative number.

For example:

$$
12-2(8)=12-16=-4
$$

If the result is a multiple of `7`, the original number is divisible by `7`.

Examples of multiples of `7` include:

$$
\ldots,-21,-14,-7,0,7,14,21,\ldots
$$

Therefore:

$$
\boxed{-14\text{ is divisible by 7}}
$$

> [!important] Remember
> **Negative multiples of `7` are still multiples of `7`.**

---

# 11. Fast Recognition

Some multiples of `7` are useful to know:

$$
7,14,21,28,35,42,49
$$

$$
56,63,70,77,84,91,98
$$

And:

$$
105,112,119,126,133,140
$$

Knowing these helps you recognize the final result quickly.

---

# 12. Pattern — Missing Digit

Find `x` such that:

$$
35x
$$

is divisible by `7`.

Using the rule:

Remaining number:

$$
35
$$

Last digit:

$$
x
$$

Therefore:

$$
35-2x
$$

must be divisible by `7`.

So:

$$
35-2x\equiv0\pmod7
$$

Since:

$$
35\equiv0\pmod7
$$

we get:

$$
2x\equiv0\pmod7
$$

Therefore:

$$
x\equiv0\pmod7
$$

Possible digit values:

$$
\boxed{x=0\text{ or }7}
$$

---

# 13. Pattern — Missing Digit With a Larger Number

Find `x` such that:

$$
52x
$$

is divisible by `7`.

Apply the rule:

$$
52-2x
$$

must be divisible by `7`.

Therefore:

$$
52-2x\equiv0\pmod7
$$

Since:

$$
52\equiv3\pmod7
$$

we get:

$$
3-2x\equiv0\pmod7
$$

Thus:

$$
2x\equiv3\pmod7
$$

The inverse of `2` modulo `7` is `4`:

$$
2\times4=8\equiv1\pmod7
$$

Therefore:

$$
x\equiv3\times4\pmod7
$$

$$
x\equiv12\pmod7
$$

$$
x\equiv5\pmod7
$$

Hence:

$$
\boxed{x=5}
$$

Check:

$$
525\div7=75
$$

Correct.

---

# 14. Pattern — Remainder

The divisibility shortcut can also help find remainders.

### Example

Find the remainder when:

$$
203
$$

is divided by `7`.

We know:

$$
203=7\times29
$$

Therefore:

$$
\boxed{203\bmod7=0}
$$

For larger numbers, repeatedly applying the divisibility transformation can reduce the number significantly.

> [!note]
> For general remainder calculations, modular arithmetic is often faster than repeatedly applying the divisibility shortcut.

---

# 15. Pattern — Count Multiples of 7

The number of positive multiples of `7` from `1` to `N` is:

$$
\boxed{\left\lfloor\frac N7\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `7`?

$$
\left\lfloor\frac{100}{7}\right\rfloor
$$

$$
=14
$$

Therefore:

$$
\boxed{14}
$$

---

# 16. Pattern — Multiples in a Range

The number of integers divisible by `7` from `A` to `B`, inclusive, is:

$$
\boxed{
\left\lfloor\frac B7\right\rfloor
-
\left\lfloor\frac{A-1}{7}\right\rfloor
}
$$

### Example

How many numbers from `20` to `100` are divisible by `7`?

$$
\left\lfloor\frac{100}{7}\right\rfloor
-
\left\lfloor\frac{19}{7}\right\rfloor
$$

$$
=14-2
$$

$$
\boxed{12}
$$

---

# 17. Pattern — Divisibility by 14

Since:

$$
14=2\times7
$$

a number is divisible by `14` if it is divisible by both:

$$
2
$$

and:

$$
7
$$

### Example

Check:

$$
672
$$

For `2`:

Last digit is `2`.

So divisible by `2`.

For `7`:

$$
67-2(2)=63
$$

Since:

$$
63=7\times9
$$

it is divisible by `7`.

Therefore:

$$
\boxed{672\text{ is divisible by 14}}
$$

---

# 18. Pattern — Divisibility by 21

Since:

$$
21=3\times7
$$

a number is divisible by `21` if it is divisible by both `3` and `7`.

### Example

Check:

$$
147
$$

For `3`:

$$
1+4+7=12
$$

So divisible by `3`.

For `7`:

$$
14-2(7)=0
$$

So divisible by `7`.

Therefore:

$$
\boxed{147\text{ is divisible by 21}}
$$

---

# 19. Pattern — Divisibility by 35

Since:

$$
35=5\times7
$$

a number is divisible by `35` if it is divisible by both `5` and `7`.

### Example

Check:

$$
245
$$

For `5`:

Last digit = `5`.

For `7`:

$$
24-2(5)=14
$$

Since `14` is divisible by `7`:

$$
\boxed{245\text{ is divisible by 35}}
$$

---

# 20. Important Formula Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Divisibility by `7` | Double last digit and subtract from remaining number |
| Transformation | `a − 2b` for `N = 10a + b` |
| Divisibility by `14` | Divisible by `2` and `7` |
| Divisibility by `21` | Divisible by `3` and `7` |
| Divisibility by `35` | Divisible by `5` and `7` |
| Multiples from `1` to `N` | `⌊N/7⌋` |
| Multiples from `A` to `B` | `⌊B/7⌋ − ⌊(A−1)/7⌋` |

---

# 21. Important Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{\text{Separate last digit}}
$$

### Pattern 2

$$
\boxed{\text{Double last digit}}
$$

### Pattern 3

$$
\boxed{\text{Subtract from remaining number}}
$$

### Pattern 4

$$
\boxed{\text{Repeat if necessary}}
$$

### Pattern 5

If the final result is:

$$
0,\pm7,\pm14,\pm21,\ldots
$$

then the original number is divisible by `7`.

---

# 22. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Adding the last digit instead of subtracting.
- ❌ Doubling the remaining number instead of the last digit.
- ❌ Forgetting to remove the last digit before subtracting.
- ❌ Stopping too early when the result is not obviously divisible by `7`.
- ❌ Thinking a negative result automatically means the number is not divisible.
- ❌ Forgetting that negative multiples of `7` are valid.
- ❌ Using the rule incorrectly for a missing-digit problem.
- ❌ Confusing the `7` rule with the digit-sum rule for `3` and `9`.

---

# 23. Exam Strategy

> [!tip] Fast Method

When asked whether a number is divisible by `7`:

### Step 1

Take the last digit.

### Step 2

Multiply it by `2`.

### Step 3

Subtract from the remaining number.

### Step 4

Repeat until the result is small.

### Example

$$
672
$$

$$
67-2(2)=63
$$

Since:

$$
63=7\times9
$$

answer:

$$
\boxed{\text{Divisible by 7}}
$$

---

# 24. HCL Preparation Priority

**Priority:** 🔥 Very High

The rule is slightly harder than divisibility by `2`, `3`, `4`, `5`, and `6`, so practice is important.

### Master These First

1. Basic `7` divisibility rule
2. `a − 2b` transformation
3. Repeated application
4. Negative results
5. Missing-digit questions
6. Remainder patterns
7. Counting multiples
8. Divisibility by `14`
9. Divisibility by `21`
10. Divisibility by `35`

---

# 25. Practice Checklist

- [ ] Memorize the `7` rule
- [ ] Practice 2-digit examples
- [ ] Practice 3-digit examples
- [ ] Practice large numbers
- [ ] Practice repeated transformations
- [ ] Practice negative results
- [ ] Practice missing-digit questions
- [ ] Practice remainder questions
- [ ] Practice counting multiples
- [ ] Practice divisibility by `14`
- [ ] Practice divisibility by `21`
- [ ] Practice divisibility by `35`
- [ ] Revise common traps

---

# 26. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 5]]
- [[Divisibility by 6]]
- [[Divisibility by 8]]
- [[Divisibility by 9]]
- [[Remainders]]
- [[Factors]]
- [[Multiples]]
- [[Digit Problems]]

---

# 27. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

For:

$$
N=10a+b
$$

calculate:

$$
\boxed{a-2b}
$$

If the result is divisible by `7`, then `N` is divisible by `7`.

### Memory Trick

> **Double the last → subtract → repeat.**

### Example

$$
203
$$

$$
20-2(3)=14
$$

$$
14\div7=2
$$

Therefore:

$$
\boxed{203\text{ is divisible by 7}}
$$

### Important Multiples

$$
7,14,21,28,35,42,49,56,63,70
$$

### Key Pattern

$$
\boxed{\text{Last digit}\times2\rightarrow\text{Subtract}\rightarrow\text{Repeat}}
$$