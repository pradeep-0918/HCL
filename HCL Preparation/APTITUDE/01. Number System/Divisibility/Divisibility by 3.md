---
type: concept
subject: aptitude
topic: "Divisibility by 3"
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
  - divisibility-by-3
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 4]]"
  - "[[Divisibility by 6]]"
  - "[[Divisibility by 9]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
---

# Divisibility by 3

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `3` if the **sum of its digits is divisible by `3`**.

Mathematically:

$$
\boxed{n\equiv0\pmod3}
$$

or:

$$
\boxed{n=3k}
$$

where `k` is an integer.

---

# 2. Divisibility Rule

For any positive integer:

1. Add all its digits.
2. Check whether the digit sum is divisible by `3`.
3. If yes, the original number is divisible by `3`.

### Rule

$$
\boxed{\text{Digit Sum}\equiv0\pmod3}
$$

Therefore:

$$
\boxed{\text{Number divisible by 3}\iff\text{Digit sum divisible by 3}}
$$

---

# 3. Why the Rule Works

Consider a decimal number:

$$
N=100a+10b+c
$$

Since:

$$
100\equiv1\pmod3
$$

and:

$$
10\equiv1\pmod3
$$

we get:

$$
N\equiv a+b+c\pmod3
$$

Therefore:

$$
\boxed{N\bmod3=(\text{Digit Sum})\bmod3}
$$

This is why the digit-sum rule works.

---

# 4. Basic Examples

## Example 1

Check whether `123` is divisible by `3`.

Digit sum:

$$
1+2+3=6
$$

Since:

$$
6\div3=2
$$

Therefore:

$$
\boxed{123\text{ is divisible by 3}}
$$

---

## Example 2

Check whether `124` is divisible by `3`.

Digit sum:

$$
1+2+4=7
$$

`7` is not divisible by `3`.

Therefore:

$$
\boxed{124\text{ is not divisible by 3}}
$$

---

## Example 3

Check `987654`.

Digit sum:

$$
9+8+7+6+5+4=39
$$

Since:

$$
39\div3=13
$$

Therefore:

$$
\boxed{987654\text{ is divisible by 3}}
$$

> [!tip] Exam Shortcut
> For a very large number, you do **not** need to perform division.
>
> Just calculate the digit sum.

---

# 5. Digit-Sum Reduction

If the digit sum is still large, you can add its digits again.

### Example

Consider:

$$
987654321
$$

Digit sum:

$$
9+8+7+6+5+4+3+2+1=45
$$

Reduce again:

$$
4+5=9
$$

Since `9` is divisible by `3`:

$$
\boxed{987654321\text{ is divisible by 3}}
$$

> [!important] Pattern
> Repeatedly adding digits does not change divisibility by `3`.

---

# 6. Possible Digit-Sum Remainders

When checking divisibility by `3`, the digit sum can be classified by its remainder:

$$
0,\ 1,\ 2
$$

### If digit sum remainder is `0`

$$
\boxed{\text{Number divisible by 3}}
$$

### If digit sum remainder is `1`

$$
\boxed{\text{Remainder is 1}}
$$

### If digit sum remainder is `2`

$$
\boxed{\text{Remainder is 2}}
$$

Therefore:

$$
\boxed{N\bmod3=(\text{Digit Sum})\bmod3}
$$

---

# 7. Connection With Divisibility by 9

The rules for `3` and `9` are closely related.

### Divisible by 3

Digit sum must be divisible by:

$$
\boxed{3}
$$

### Divisible by 9

Digit sum must be divisible by:

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

`12`:

$$
1+2=3
$$

So `12` is divisible by `3`.

But `3` is not divisible by `9`.

Therefore:

$$
\boxed{12\text{ is not divisible by 9}}
$$

---

# 8. Connection With Divisibility by 6

Since:

$$
6=2\times3
$$

a number is divisible by `6` if it is divisible by both `2` and `3`.

Therefore:

$$
\boxed{\text{Divisible by 6}\iff\text{Divisible by 2 and 3}}
$$

### Example

Check `438`.

Last digit:

$$
8
$$

So it is divisible by `2`.

Digit sum:

$$
4+3+8=15
$$

`15` is divisible by `3`.

Therefore:

$$
\boxed{438\text{ is divisible by 6}}
$$

---

# 9. Missing Digit Problems

This is one of the most important aptitude patterns.

## Pattern 1 — One Missing Digit

Find `x` such that:

$$
52x
$$

is divisible by `3`.

Digit sum:

$$
5+2+x=7+x
$$

We need:

$$
7+x
$$

to be divisible by `3`.

Possible digits:

$$
\boxed{x=2,5,8}
$$

Check:

$$
7+2=9
$$

$$
7+5=12
$$

$$
7+8=15
$$

All are divisible by `3`.

Therefore:

$$
\boxed{x\in\{2,5,8\}}
$$

---

# 10. Pattern — Largest Missing Digit

Find the largest digit `x` such that:

$$
43x
$$

is divisible by `3`.

Digit sum:

$$
4+3+x=7+x
$$

Possible values:

$$
x=2,5,8
$$

Largest:

$$
\boxed{x=8}
$$

---

# 11. Pattern — Smallest Missing Digit

Find the smallest digit `x` such that:

$$
71x
$$

is divisible by `3`.

Digit sum:

$$
7+1+x=8+x
$$

We need:

$$
8+x
$$

to be divisible by `3`.

Possible digits:

$$
x=1,4,7
$$

Smallest:

$$
\boxed{x=1}
$$

---

# 12. Pattern — Two Missing Digits

Find possible values of `x` and `y` such that:

$$
52xy
$$

is divisible by `3`.

Digit sum:

$$
5+2+x+y
$$

$$
=7+x+y
$$

Therefore:

$$
\boxed{7+x+y\equiv0\pmod3}
$$

or:

$$
\boxed{x+y\equiv2\pmod3}
$$

Possible pairs depend on the conditions given in the question.

> [!tip] Pattern
> With multiple missing digits, focus on the **sum of the unknown digits**.

---

# 13. Pattern — Remainder Using Digit Sum

Find the remainder when:

$$
1234567
$$

is divided by `3`.

Digit sum:

$$
1+2+3+4+5+6+7=28
$$

Now:

$$
28\div3
$$

remainder:

$$
1
$$

Therefore:

$$
\boxed{1234567\bmod3=1}
$$

> [!important] Shortcut
> For division by `3`, you can find the remainder using the digit sum.

---

# 14. Pattern — Very Large Number

Suppose:

$$
N=987654321987654321987654321
$$

You do not need to divide this huge number.

Add its digits.

If the digit sum is divisible by `3`, the entire number is divisible by `3`.

> [!tip] Exam Pattern
> **Large number + divisor 3 → digit sum immediately.**

---

# 15. Pattern — Removing Digits

Suppose a number is divisible by `3`.

Removing a digit changes the digit sum.

Therefore, the new number's divisibility depends on the new digit sum.

### Example

Number:

$$
123
$$

Digit sum:

$$
6
$$

It is divisible by `3`.

Remove digit `2`:

$$
13
$$

Digit sum:

$$
1+3=4
$$

Therefore:

$$
\boxed{13\text{ is not divisible by 3}}
$$

---

# 16. Pattern — Adding a Digit

Suppose a number has digit sum `S`.

If a digit `x` is appended, the new digit sum becomes:

$$
\boxed{S+x}
$$

Therefore, to make the number divisible by `3`:

$$
\boxed{S+x\equiv0\pmod3}
$$

### Example

Current digit sum:

$$
14
$$

What digit can be appended to make it divisible by `3`?

Need:

$$
14+x\equiv0\pmod3
$$

Since:

$$
14\equiv2\pmod3
$$

we need:

$$
x\equiv1\pmod3
$$

Possible digits:

$$
\boxed{1,4,7}
$$

---

# 17. Pattern — Number of Digits With a Condition

Questions may ask:

> How many digits can replace `x` so that a number is divisible by `3`?

Example:

$$
72x
$$

Digit sum:

$$
7+2+x=9+x
$$

We need:

$$
9+x
$$

to be divisible by `3`.

Therefore:

$$
x\equiv0\pmod3
$$

Possible digits:

$$
\boxed{0,3,6,9}
$$

Number of possibilities:

$$
\boxed{4}
$$

---

# 18. Pattern — Divisibility by Both 2 and 3

If a question asks for divisibility by `6`, combine:

### Divisibility by 2

Last digit must be:

$$
0,2,4,6,8
$$

### Divisibility by 3

Digit sum must be divisible by:

$$
3
$$

### Example

Find possible `x` such that:

$$
45x
$$

is divisible by `6`.

For `2`:

$$
x\in\{0,2,4,6,8\}
$$

For `3`:

$$
4+5+x=9+x
$$

So `x` must be divisible by `3`.

Intersection:

$$
\{0,2,4,6,8\}\cap\{0,3,6,9\}
$$

Therefore:

$$
\boxed{x\in\{0,6\}}
$$

---

# 19. Important Formula Sheet

> [!important] Must Remember

| Concept | Formula / Rule |
|---|---|
| Divisible by 3 | Digit sum divisible by `3` |
| Remainder mod 3 | Same as digit-sum remainder mod `3` |
| Digit sum | Sum of all decimal digits |
| Missing digit | Make digit sum a multiple of `3` |
| Multiple missing digits | Make total digit sum a multiple of `3` |
| Divisible by 6 | Divisible by both `2` and `3` |
| Divisible by 9 | Digit sum divisible by `9` |

---

# 20. Common Multiples of 3

Some useful multiples:

$$
3,6,9,12,15,18,21,24,27,30
$$

Continuing:

$$
33,36,39,42,45,48,51,54,57,60
$$

You do not need to memorize many of them because the digit-sum rule is faster.

---

# 21. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Checking only the last digit.
- ❌ Confusing the rule for `3` with the rule for `4`.
- ❌ Assuming divisibility by `3` means divisibility by `9`.
- ❌ Forgetting to include all digits in the digit sum.
- ❌ Performing complete division on huge numbers.
- ❌ Forgetting that `0` contributes nothing to the digit sum.
- ❌ Choosing only one possible missing digit when several exist.
- ❌ Forgetting additional conditions in missing-digit questions.

---

# 22. Exam Strategy

> [!tip] 3-Second Method

When the divisor is `3`:

### Step 1

Add the digits.

### Step 2

Check whether the sum is divisible by `3`.

### Step 3

If the sum is large, reduce it again.

Example:

$$
987654
$$

Digit sum:

$$
9+8+7+6+5+4=39
$$

Reduce:

$$
3+9=12
$$

Reduce:

$$
1+2=3
$$

Therefore:

$$
\boxed{\text{Divisible by 3}}
$$

---

# 23. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Basic divisibility rule
2. Digit-sum method
3. Repeated digit reduction
4. Remainder using digit sum
5. Missing-digit questions
6. Largest/smallest possible digit
7. Multiple missing digits
8. Divisibility by `6`
9. Divisibility by `9`
10. Large-number divisibility

---

# 24. Practice Checklist

- [ ] Memorize the divisibility rule
- [ ] Practice digit sums
- [ ] Practice large numbers
- [ ] Practice repeated digit reduction
- [ ] Practice remainder questions
- [ ] Practice missing-digit questions
- [ ] Practice largest/smallest digit questions
- [ ] Practice multiple missing digits
- [ ] Practice divisibility by `6`
- [ ] Practice divisibility by `9`
- [ ] Revise common traps

---

# 25. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 4]]
- [[Divisibility by 5]]
- [[Divisibility by 6]]
- [[Divisibility by 9]]
- [[Remainders]]
- [[Digit Sum]]
- [[Digit Problems]]
- [[Factors]]
- [[Multiples]]

---

# 26. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
N\text{ is divisible by 3}
\iff
\text{Sum of digits is divisible by 3}
}
$$

### Remainder

$$
\boxed{
N\bmod3
=
(\text{Digit Sum})\bmod3
}
$$

### Missing Digit

If:

$$
\text{Digit Sum}=S
$$

then choose `x` such that:

$$
\boxed{S+x\equiv0\pmod3}
$$

### Divisibility by 6

$$
\boxed{6=2\times3}
$$

So:

$$
\boxed{\text{Divisible by 6}\iff\text{Divisible by 2 and 3}}
$$

### Key Pattern

> **For divisibility by `3`, forget the actual number and look at its digit sum.**

> **Huge number? → Add the digits.**