---
type: concept
subject: aptitude
topic: "Divisibility by 9"
parent: "01. Number System/Divisibility"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - divisibility
  - divisibility-by-9
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 6]]"
  - "[[Divisibility by 18]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
  - "[[Digit Sum]]"
---

# Divisibility by 9

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `9` if the **sum of its digits is divisible by `9`**.

Mathematically:

$$
\boxed{n\equiv0\pmod9}
$$

or:

$$
\boxed{n=9k}
$$

where `k` is an integer.

---

# 2. Divisibility Rule

To check whether a number is divisible by `9`:

1. Add all the digits.
2. Check whether the digit sum is divisible by `9`.
3. If yes, the original number is divisible by `9`.

Therefore:

$$
\boxed{
N\text{ divisible by 9}
\iff
\text{Digit Sum divisible by 9}
}
$$

---

# 3. Why the Rule Works

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
N\equiv a+b+c\pmod9
$$

Hence:

$$
\boxed{
N\bmod9
=
(\text{Digit Sum})\bmod9
}
$$

This is why the digit-sum rule works.

> [!note] Aptitude Focus
> You do not need to reproduce the proof in the exam.
>
> Remember:
>
> **Add the digits → check divisibility by 9.**

---

# 4. Basic Examples

## Example 1

Check:

$$
729
$$

Digit sum:

$$
7+2+9=18
$$

Since:

$$
18\div9=2
$$

therefore:

$$
\boxed{729\text{ is divisible by 9}}
$$

---

## Example 2

Check:

$$
725
$$

Digit sum:

$$
7+2+5=14
$$

`14` is not divisible by `9`.

Therefore:

$$
\boxed{725\text{ is not divisible by 9}}
$$

---

## Example 3

Check:

$$
987654
$$

Digit sum:

$$
9+8+7+6+5+4=39
$$

Since:

$$
39\div9
$$

is not an integer:

$$
\boxed{987654\text{ is not divisible by 9}}
$$

---

# 5. Digit-Sum Reduction

If the digit sum is large, reduce it again.

### Example

Check:

$$
987654321
$$

First digit sum:

$$
9+8+7+6+5+4+3+2+1=45
$$

Reduce:

$$
4+5=9
$$

Since:

$$
9\div9=1
$$

therefore:

$$
\boxed{987654321\text{ is divisible by 9}}
$$

> [!important] Pattern
> Repeatedly adding digits preserves the remainder modulo `9`.

---

# 6. Divisibility by 3 vs Divisibility by 9

These two rules look almost identical, so this is an important distinction.

### Divisible by 3

Digit sum must be a multiple of:

$$
\boxed{3}
$$

### Divisible by 9

Digit sum must be a multiple of:

$$
\boxed{9}
$$

Therefore:

$$
\boxed{\text{Divisible by 9}\Rightarrow\text{Divisible by 3}}
$$

But:

$$
\boxed{\text{Divisible by 3}\not\Rightarrow\text{Divisible by 9}}
$$

### Example

Consider:

$$
12
$$

Digit sum:

$$
1+2=3
$$

So:

$$
12\text{ is divisible by 3}
$$

but:

$$
12\text{ is not divisible by 9}
$$

---

# 7. Important Relationship

Since:

$$
9=3\times3
$$

every multiple of `9` is also a multiple of `3`.

Examples:

$$
9,18,27,36,45,54,63,72,81,90
$$

All are divisible by `3`.

Therefore:

$$
\boxed{9\mid n\Rightarrow3\mid n}
$$

---

# 8. Remainder Pattern

The digit-sum rule can also determine the remainder when dividing by `9`.

For any integer `N`:

$$
\boxed{
N\bmod9
=
(\text{Digit Sum})\bmod9
}
$$

### Example

Find the remainder when:

$$
1234567
$$

is divided by `9`.

Digit sum:

$$
1+2+3+4+5+6+7=28
$$

Now:

$$
28\div9
$$

remainder:

$$
1
$$

Therefore:

$$
\boxed{1234567\bmod9=1}
$$

---

# 9. Large Number Remainder

Find:

$$
987654321987654321\bmod9
$$

Digit sum:

$$
9+8+7+6+5+4+3+2+1
$$

for each repeated block:

$$
45+45=90
$$

Then:

$$
90\bmod9=0
$$

Therefore:

$$
\boxed{987654321987654321\bmod9=0}
$$

So the number is divisible by `9`.

> [!tip] Exam Shortcut
> **Huge number + divisor `9` → calculate digit sum.**

---

# 10. Missing Digit Problems

This is one of the most important aptitude patterns.

## Pattern 1 — One Missing Digit

Find `x` such that:

$$
52x
$$

is divisible by `9`.

Digit sum:

$$
5+2+x=7+x
$$

We need:

$$
7+x
$$

to be a multiple of `9`.

Therefore:

$$
7+x=9
$$

So:

$$
\boxed{x=2}
$$

---

# 11. Pattern — Largest Missing Digit

Find the largest digit `x` such that:

$$
43x
$$

is divisible by `9`.

Digit sum:

$$
4+3+x=7+x
$$

Possible values must satisfy:

$$
7+x=9
$$

or:

$$
7+x=18
$$

The second gives:

$$
x=11
$$

which is not a digit.

Therefore:

$$
\boxed{x=2}
$$

---

# 12. Pattern — Smallest Missing Digit

Find the smallest digit `x` such that:

$$
71x
$$

is divisible by `9`.

Digit sum:

$$
7+1+x=8+x
$$

Need:

$$
8+x=9
$$

Therefore:

$$
\boxed{x=1}
$$

---

# 13. Pattern — Multiple Missing Digits

Suppose:

$$
52xy
$$

is divisible by `9`.

Digit sum:

$$
5+2+x+y
$$

$$
=7+x+y
$$

Therefore:

$$
\boxed{x+y\equiv2\pmod9}
$$

Since `x` and `y` are digits, possible values depend on the additional conditions in the question.

> [!important] Key Pattern
> With multiple missing digits, focus on the **total digit sum**.

---

# 14. Pattern — Missing Digit for Divisibility by 18

Since:

$$
18=2\times9
$$

a number must satisfy:

1. Divisibility by `2`
2. Divisibility by `9`

### Example

Find `x` such that:

$$
45x
$$

is divisible by `18`.

### Condition 1: Divisible by 2

`x` must be even:

$$
x\in\{0,2,4,6,8\}
$$

### Condition 2: Divisible by 9

Digit sum:

$$
4+5+x=9+x
$$

Therefore:

$$
x\in\{0,9\}
$$

Intersection:

$$
\{0,2,4,6,8\}
\cap
\{0,9\}
$$

Therefore:

$$
\boxed{x=0}
$$

---

# 15. Pattern — Adding a Digit

Suppose the current digit sum is:

$$
S
$$

and you append a digit `x`.

New digit sum:

$$
S+x
$$

To make the number divisible by `9`:

$$
\boxed{S+x\equiv0\pmod9}
$$

### Example

Current digit sum:

$$
23
$$

What digit can be appended to make the number divisible by `9`?

Since:

$$
23\equiv5\pmod9
$$

we need:

$$
x\equiv4\pmod9
$$

The digit is:

$$
\boxed{4}
$$

because:

$$
23+4=27
$$

and:

$$
27\div9=3
$$

---

# 16. Pattern — Removing a Digit

Removing a digit changes the digit sum.

### Example

Consider:

$$
729
$$

Digit sum:

$$
7+2+9=18
$$

So it is divisible by `9`.

Remove digit `2`:

$$
79
$$

New digit sum:

$$
7+9=16
$$

Since `16` is not divisible by `9`:

$$
\boxed{79\text{ is not divisible by 9}}
$$

---

# 17. Pattern — Counting Multiples of 9

The number of positive multiples of `9` from `1` to `N` is:

$$
\boxed{\left\lfloor\frac N9\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `9`?

$$
\left\lfloor\frac{100}{9}\right\rfloor
$$

$$
=11
$$

Therefore:

$$
\boxed{11}
$$

---

# 18. Pattern — Multiples in a Range

The number of integers divisible by `9` from `A` to `B`, inclusive, is:

$$
\boxed{
\left\lfloor\frac B9\right\rfloor
-
\left\lfloor\frac{A-1}{9}\right\rfloor
}
$$

### Example

How many numbers from `20` to `100` are divisible by `9`?

$$
\left\lfloor\frac{100}{9}\right\rfloor
-
\left\lfloor\frac{19}{9}\right\rfloor
$$

$$
=11-2
$$

$$
\boxed{9}
$$

---

# 19. Pattern — Divisibility by 27

Since:

$$
27=3^3
$$

there is **no standard simple digit-sum rule equivalent to the rule for `9`**.

For divisibility by `27`, use modular arithmetic or direct division when appropriate.

> [!warning] Important
> Do not blindly extend the divisibility-by-`9` rule to every multiple or power of `3`.

---

# 20. Pattern — Divisibility by 18

Since:

$$
18=2\times9
$$

a number is divisible by `18` if:

- Last digit is even.
- Digit sum is divisible by `9`.

Therefore:

$$
\boxed{
18\mid n
\iff
2\mid n\text{ and }9\mid n
}
$$

---

# 21. Pattern — Divisibility by 45

Since:

$$
45=5\times9
$$

a number is divisible by `45` if:

- Last digit is `0` or `5`.
- Digit sum is divisible by `9`.

Therefore:

$$
\boxed{
45\mid n
\iff
5\mid n\text{ and }9\mid n
}
$$

### Example

Check:

$$
360
$$

Last digit:

$$
0
$$

So divisible by `5`.

Digit sum:

$$
3+6+0=9
$$

So divisible by `9`.

Therefore:

$$
\boxed{360\text{ is divisible by 45}}
$$

---

# 22. Important Formula Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Divisibility by `9` | Digit sum divisible by `9` |
| Remainder mod `9` | Same as digit-sum remainder mod `9` |
| Divisibility by `3` | Digit sum divisible by `3` |
| Divisibility by `18` | Divisible by `2` and `9` |
| Divisibility by `45` | Divisible by `5` and `9` |
| Multiples from `1` to `N` | `⌊N/9⌋` |
| Multiples from `A` to `B` | `⌊B/9⌋ − ⌊(A−1)/9⌋` |

---

# 23. Important Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
N\div9\text{ exactly}
\iff
\text{Digit Sum}\div9\text{ exactly}
}
$$

### Pattern 2

$$
\boxed{
N\bmod9
=
(\text{Digit Sum})\bmod9
}
$$

### Pattern 3

$$
\boxed{
9\mid N\Rightarrow3\mid N
}
$$

### Pattern 4

For missing digits:

$$
\boxed{
\text{Total digit sum must be a multiple of 9}
}
$$

### Pattern 5

For huge numbers:

$$
\boxed{
\text{Ignore the number's size; use digit sum}
}
$$

---

# 24. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Confusing divisibility by `3` with divisibility by `9`.
- ❌ Thinking a digit sum divisible by `3` is automatically divisible by `9`.
- ❌ Forgetting to include every digit.
- ❌ Performing long division for a huge number.
- ❌ Forgetting that `0` contributes nothing to the digit sum.
- ❌ Assuming divisibility by `9` means divisibility by `18`.
- ❌ Forgetting the extra divisibility-by-`2` condition for `18`.
- ❌ Blindly applying the digit-sum rule to `27`.

---

# 25. Exam Strategy

> [!tip] Fast 3-Second Method

When the divisor is `9`:

### Step 1

Add all digits.

### Step 2

Reduce the sum if necessary.

### Step 3

Check whether the final value is:

$$
9,\ 18,\ 27,\ 36,\ldots
$$

or equivalently whether its remainder modulo `9` is `0`.

### Example

$$
738492
$$

Digit sum:

$$
7+3+8+4+9+2=33
$$

Reduce:

$$
3+3=6
$$

Since `6` is not `9` or `0` modulo `9`:

$$
\boxed{\text{Not divisible by 9}}
$$

---

# 26. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Digit-sum rule
2. Repeated digit reduction
3. Difference between `3` and `9`
4. Remainder using digit sum
5. Missing-digit problems
6. Multiple missing digits
7. Divisibility by `18`
8. Divisibility by `45`
9. Counting multiples
10. Large-number questions

---

# 27. Practice Checklist

- [ ] Memorize the digit-sum rule
- [ ] Practice basic divisibility questions
- [ ] Practice large numbers
- [ ] Practice repeated digit reduction
- [ ] Practice remainder questions
- [ ] Practice missing-digit questions
- [ ] Practice largest/smallest digit questions
- [ ] Practice multiple missing digits
- [ ] Practice divisibility by `18`
- [ ] Practice divisibility by `45`
- [ ] Practice counting multiples
- [ ] Revise common traps

---

# 28. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 6]]
- [[Divisibility by 11]]
- [[Remainders]]
- [[Digit Sum]]
- [[Digit Problems]]
- [[Factors]]
- [[Multiples]]

---

# 29. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
N\text{ is divisible by 9}
\iff
\text{Digit Sum is divisible by 9}
}
$$

### Remainder

$$
\boxed{
N\bmod9
=
(\text{Digit Sum})\bmod9
}
$$

### Example

$$
729
$$

$$
7+2+9=18
$$

$$
18\div9=2
$$

Therefore:

$$
\boxed{729\text{ is divisible by 9}}
$$

### Important Relationship

$$
\boxed{9\mid N\Rightarrow3\mid N}
$$

but:

$$
\boxed{3\mid N\not\Rightarrow9\mid N}
$$

### Key Pattern

> **Divisibility by `9` → Add all digits → Check whether the sum is a multiple of `9`.**