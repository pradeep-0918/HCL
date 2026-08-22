---
type: concept
subject: aptitude
topic: "Divisibility by 11"
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
  - divisibility-by-11
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 9]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
  - "[[Digit Sum]]"
---

# Divisibility by 11

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `11` if the **difference between the sums of alternate digits** is `0` or a multiple of `11`.

For a number:

$$
d_1d_2d_3d_4\ldots
$$

calculate:

$$
\boxed{
(\text{Sum of digits in odd positions})
-
(\text{Sum of digits in even positions})
}
$$

If the result is:

$$
0,\pm11,\pm22,\pm33,\ldots
$$

then the number is divisible by `11`.

---

# 2. Divisibility Rule

> [!important] Golden Rule
> **Add alternate digits → subtract the two sums → check whether the result is a multiple of `11`.**

The absolute difference can be used:

$$
\boxed{
|\text{Odd-position sum}-\text{Even-position sum}|
}
$$

If this is divisible by `11`, the original number is divisible by `11`.

---

# 3. Example — 121

Check:

$$
121
$$

Separate alternate positions:

$$
(1+1)-2
$$

$$
=2-2
$$

$$
=0
$$

Since `0` is divisible by `11`:

$$
\boxed{121\text{ is divisible by 11}}
$$

---

# 4. Example — 1331

Check:

$$
1331
$$

Odd positions:

$$
1+3=4
$$

Even positions:

$$
3+1=4
$$

Difference:

$$
4-4=0
$$

Therefore:

$$
\boxed{1331\text{ is divisible by 11}}
$$

---

# 5. Example — 1234

Check:

$$
1234
$$

Odd positions:

$$
1+3=4
$$

Even positions:

$$
2+4=6
$$

Difference:

$$
4-6=-2
$$

Absolute difference:

$$
|-2|=2
$$

Since `2` is not divisible by `11`:

$$
\boxed{1234\text{ is not divisible by 11}}
$$

---

# 6. Example — 50644

Check:

$$
50644
$$

Odd positions:

$$
5+6+4=15
$$

Even positions:

$$
0+4=4
$$

Difference:

$$
15-4=11
$$

Since:

$$
11\div11=1
$$

Therefore:

$$
\boxed{50644\text{ is divisible by 11}}
$$

---

# 7. Why the Rule Works

In decimal representation:

$$
10\equiv-1\pmod{11}
$$

Therefore:

$$
10^2\equiv1\pmod{11}
$$

and:

$$
10^3\equiv-1\pmod{11}
$$

The powers of `10` alternate between:

$$
1,-1,1,-1,\ldots
$$

Therefore, modulo `11`, the digits are effectively added and subtracted alternately.

Hence:

$$
\boxed{
N\bmod11
=
\text{Alternating digit sum}\bmod11
}
$$

> [!note] Aptitude Focus
> You do not need to reproduce this proof in the exam.
>
> Remember:
>
> **Alternate addition and subtraction.**

---

# 8. Position Pattern

For:

$$
123456
$$

starting from the left:

| Position | Digit | Group |
|---:|---:|:---:|
| 1 | `1` | `+` |
| 2 | `2` | `−` |
| 3 | `3` | `+` |
| 4 | `4` | `−` |
| 5 | `5` | `+` |
| 6 | `6` | `−` |

Therefore:

$$
(1+3+5)-(2+4+6)
$$

$$
=9-12
$$

$$
=-3
$$

Not divisible by `11`.

---

# 9. Another Way to Remember

You can write the digits with alternating signs:

$$
+\quad-\quad+\quad-\quad+\quad-
$$

For example:

$$
72531
$$

becomes:

$$
7-2+5-3+1
$$

Calculate:

$$
7-2+5-3+1=8
$$

Since `8` is not a multiple of `11`:

$$
\boxed{72531\text{ is not divisible by 11}}
$$

> [!tip] Memory Trick
> **Plus, minus, plus, minus...**

---

# 10. Important Special Case — Difference = 0

If the two alternate sums are equal:

$$
\text{Odd sum}=\text{Even sum}
$$

then:

$$
\text{Difference}=0
$$

Therefore the number is divisible by `11`.

### Example

$$
2728
$$

Odd positions:

$$
2+2=4
$$

Even positions:

$$
7+8=15
$$

Not divisible.

Now:

$$
121
$$

Odd positions:

$$
1+1=2
$$

Even position:

$$
2
$$

Difference:

$$
0
$$

Therefore:

$$
\boxed{121\text{ is divisible by 11}}
$$

---

# 11. Negative Difference

The difference may be negative.

### Example

$$
9185
$$

Odd positions:

$$
9+8=17
$$

Even positions:

$$
1+5=6
$$

Difference:

$$
17-6=11
$$

Divisible.

If the difference were:

$$
-11
$$

that would also mean divisibility.

Therefore:

$$
\boxed{0,\pm11,\pm22,\ldots}
$$

are all valid results.

> [!important] Remember
> **The sign does not matter. Only whether the difference is a multiple of `11` matters.**

---

# 12. Missing Digit Problems

This is a very important aptitude pattern.

## Pattern 1 — One Missing Digit

Find `x` such that:

$$
12x1
$$

is divisible by `11`.

Odd positions:

$$
1+x
$$

Even positions:

$$
2+1=3
$$

Therefore:

$$
(1+x)-3
$$

must be a multiple of `11`.

So:

$$
x-2
$$

must be a multiple of `11`.

Since `x` is a digit:

$$
x=2
$$

Therefore:

$$
\boxed{x=2}
$$

Check:

$$
1221
$$

and:

$$
1+2=3
$$

$$
2+1=3
$$

Difference:

$$
0
$$

Correct.

---

# 13. Pattern — Missing Digit With Multiple Answers

Find possible values of `x` such that:

$$
5x72
$$

is divisible by `11`.

Odd positions:

$$
5+7=12
$$

Even positions:

$$
x+2
$$

Difference:

$$
12-(x+2)
$$

$$
=10-x
$$

This must be a multiple of `11`.

Since `x` is a digit:

$$
10-x=0
$$

Therefore:

$$
\boxed{x=10}
$$

But `10` is not a digit.

So there is:

$$
\boxed{\text{No valid digit }x}
$$

> [!warning] Important
> Always verify that the final value of a missing variable is actually a digit from `0` to `9`.

---

# 14. Pattern — Another Missing Digit

Find `x` such that:

$$
4x35
$$

is divisible by `11`.

Odd positions:

$$
4+3=7
$$

Even positions:

$$
x+5
$$

Difference:

$$
7-(x+5)
$$

$$
=2-x
$$

Possible multiple of `11` within the digit range:

$$
0
$$

Therefore:

$$
2-x=0
$$

$$
\boxed{x=2}
$$

Check:

$$
4235
$$

Odd sum:

$$
4+3=7
$$

Even sum:

$$
2+5=7
$$

Difference:

$$
0
$$

Correct.

---

# 15. Pattern — Multiple Missing Digits

Suppose:

$$
5xy2
$$

is divisible by `11`.

Odd positions:

$$
5+y
$$

Even positions:

$$
x+2
$$

Therefore:

$$
(5+y)-(x+2)
$$

must be a multiple of `11`.

Simplify:

$$
\boxed{3+y-x}
$$

So:

$$
\boxed{3+y-x\equiv0\pmod{11}}
$$

Additional conditions may be required to determine unique values.

> [!tip] Pattern
> For multiple missing digits, assign each unknown digit to its **correct alternating group**.

---

# 16. Remainder Pattern

For any number:

$$
N
$$

the remainder modulo `11` can be found from the alternating digit sum.

Therefore:

$$
\boxed{
N\bmod11
=
(\text{Alternating Digit Sum})\bmod11
}
$$

### Example

Find the remainder when:

$$
12345
$$

is divided by `11`.

Alternating sum:

$$
1-2+3-4+5
$$

$$
=3
$$

Therefore:

$$
\boxed{12345\bmod11=3}
$$

---

# 17. Large Number Pattern

Suppose:

$$
987654321987654
$$

must be checked for divisibility by `11`.

Write:

$$
9-8+7-6+5-4+3-2+1-9+8-7+6-5+4
$$

Group instead:

Odd positions:

$$
9+7+5+3+1+8+6+4
$$

Even positions:

$$
8+6+4+2+9+7+5
$$

Then calculate the difference.

If the difference is a multiple of `11`, the number is divisible by `11`.

> [!tip] Exam Shortcut
> **Huge number + divisor `11` → alternating digit sum.**

---

# 18. Counting Multiples of 11

The number of positive multiples of `11` from `1` to `N` is:

$$
\boxed{\left\lfloor\frac N{11}\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `11`?

$$
\left\lfloor\frac{100}{11}\right\rfloor
$$

$$
=9
$$

Therefore:

$$
\boxed{9}
$$

---

# 19. Multiples in a Range

The number of integers divisible by `11` from `A` to `B`, inclusive, is:

$$
\boxed{
\left\lfloor\frac B{11}\right\rfloor
-
\left\lfloor\frac{A-1}{11}\right\rfloor
}
$$

### Example

How many numbers from `20` to `100` are divisible by `11`?

$$
\left\lfloor\frac{100}{11}\right\rfloor
-
\left\lfloor\frac{19}{11}\right\rfloor
$$

$$
=9-1
$$

$$
\boxed{8}
$$

---

# 20. Divisibility by 22

Since:

$$
22=2\times11
$$

a number is divisible by `22` if it is divisible by both:

$$
2
$$

and:

$$
11
$$

### Example

Check:

$$
132
$$

For `2`:

Last digit:

$$
2
$$

So it is divisible by `2`.

For `11`:

$$
1-3+2=0
$$

So it is divisible by `11`.

Therefore:

$$
\boxed{132\text{ is divisible by 22}}
$$

---

# 21. Divisibility by 33

Since:

$$
33=3\times11
$$

a number is divisible by `33` if it is divisible by both:

$$
3
$$

and:

$$
11
$$

### Example

Check:

$$
363
$$

For `3`:

$$
3+6+3=12
$$

So divisible by `3`.

For `11`:

$$
3-6+3=0
$$

So divisible by `11`.

Therefore:

$$
\boxed{363\text{ is divisible by 33}}
$$

---

# 22. Divisibility by 55

Since:

$$
55=5\times11
$$

a number is divisible by `55` if it is divisible by both:

$$
5
$$

and:

$$
11
$$

### Example

Check:

$$
605
$$

For `5`:

Last digit is `5`.

For `11`:

$$
6-0+5=11
$$

Therefore:

$$
\boxed{605\text{ is divisible by 55}}
$$

---

# 23. Important Formula Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Divisibility by `11` | Difference of alternate digit sums is a multiple of `11` |
| Alternating form | `+ − + − + − ...` |
| Valid difference | `0, ±11, ±22, ±33, ...` |
| Remainder mod `11` | Alternating digit sum mod `11` |
| Divisibility by `22` | Divisible by `2` and `11` |
| Divisibility by `33` | Divisible by `3` and `11` |
| Divisibility by `55` | Divisible by `5` and `11` |
| Multiples from `1` to `N` | `⌊N/11⌋` |
| Multiples from `A` to `B` | `⌊B/11⌋ − ⌊(A−1)/11⌋` |

---

# 24. Important Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{+\ -\ +\ -\ +\ -}
$$

### Pattern 2

$$
\boxed{
|\text{Odd-position sum}-\text{Even-position sum}|
}
$$

### Pattern 3

If the difference is:

$$
0
$$

then divisible by `11`.

### Pattern 4

If the difference is:

$$
11,\ 22,\ 33,\ldots
$$

then divisible by `11`.

### Pattern 5

For missing digits:

$$
\boxed{\text{Place each digit in the correct alternating group}}
$$

---

# 25. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Adding all digits like the rule for `3` or `9`.
- ❌ Checking only the last digit.
- ❌ Forgetting the alternating pattern.
- ❌ Taking the difference between adjacent digits instead of the two sums.
- ❌ Forgetting that `0` is a valid difference.
- ❌ Rejecting a negative difference.
- ❌ Assigning a missing digit to the wrong group.
- ❌ Forgetting to check whether the final missing value is between `0` and `9`.

---

# 26. Exam Strategy

> [!tip] Fast Method

When you see:

> **"Is this number divisible by `11`?"**

### Step 1

Write alternating signs:

$$
+\ -\ +\ -\ +\ -\ldots
$$

### Step 2

Add the `+` digits.

### Step 3

Add the `−` digits.

### Step 4

Find the difference.

### Step 5

Check whether the difference is:

$$
0,\ 11,\ 22,\ldots
$$

### Example

$$
2728
$$

$$
(2+2)-(7+8)
$$

$$
=4-15
$$

$$
=-11
$$

Therefore:

$$
\boxed{2728\text{ is divisible by 11}}
$$

---

# 27. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Alternating-sum rule
2. Odd/even position grouping
3. Difference of sums
4. Negative differences
5. Missing-digit problems
6. Multiple missing digits
7. Remainder questions
8. Divisibility by `22`
9. Divisibility by `33`
10. Divisibility by `55`

---

# 28. Practice Checklist

- [ ] Memorize the alternating-sum rule
- [ ] Practice 2-digit numbers
- [ ] Practice 3-digit numbers
- [ ] Practice 4-digit numbers
- [ ] Practice large numbers
- [ ] Practice negative differences
- [ ] Practice missing-digit questions
- [ ] Practice multiple missing digits
- [ ] Practice remainder questions
- [ ] Practice divisibility by `22`
- [ ] Practice divisibility by `33`
- [ ] Practice divisibility by `55`
- [ ] Revise common traps

---

# 29. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 5]]
- [[Divisibility by 6]]
- [[Divisibility by 9]]
- [[Remainders]]
- [[Digit Sum]]
- [[Digit Problems]]
- [[Factors]]
- [[Multiples]]

---

# 30. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
N\text{ is divisible by 11}
\iff
|\text{Odd Sum}-\text{Even Sum}|
\text{ is a multiple of 11}
}
$$

### Alternating Pattern

$$
\boxed{+\ -\ +\ -\ +\ -}
$$

### Valid Results

$$
\boxed{0,\ 11,\ 22,\ 33,\ldots}
$$

or their negative equivalents.

### Example

$$
121
$$

$$
1-2+1=0
$$

Therefore:

$$
\boxed{121\text{ is divisible by 11}}
$$

### Key Pattern

> **Divisibility by `11` → Alternate + and − → Find the difference → Check multiple of `11`.**