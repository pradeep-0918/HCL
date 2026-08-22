---
type: concept
subject: aptitude
topic: "Divisibility by 5"
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
  - divisibility-by-5
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Divisibility Rules]]"
  - "[[Divisibility by 2]]"
  - "[[Divisibility by 3]]"
  - "[[Divisibility by 6]]"
  - "[[Divisibility by 10]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Remainders]]"
  - "[[Digit Problems]]"
---

# Divisibility by 5

## 1. Core Concept

> [!summary] Definition
> A number is divisible by `5` if its remainder is `0` when divided by `5`.

Mathematically:

$$
\boxed{n\equiv0\pmod5}
$$

or:

$$
\boxed{n=5k}
$$

where `k` is an integer.

---

# 2. Divisibility Rule

A number is divisible by `5` if its **last digit is either `0` or `5`**.

$$
\boxed{\text{Last digit}=0\text{ or }5}
$$

### Therefore

| Last Digit | Divisible by 5? |
|---:|:---:|
| `0` | ✅ |
| `1` | ❌ |
| `2` | ❌ |
| `3` | ❌ |
| `4` | ❌ |
| `5` | ✅ |
| `6` | ❌ |
| `7` | ❌ |
| `8` | ❌ |
| `9` | ❌ |

> [!important] Golden Rule
> **For divisibility by `5`, check ONLY the last digit.**

---

# 3. Why Only the Last Digit Matters

Every decimal number can be written as:

$$
N=10k+d
$$

where `d` is the last digit.

Since:

$$
10k
$$

is always divisible by `5`:

$$
10k=5(2k)
$$

the divisibility depends only on the final digit.

Therefore:

$$
\boxed{\text{Divisibility by 5 depends only on the last digit}}
$$

---

# 4. Basic Examples

## Example 1

Check:

$$
125
$$

Last digit:

$$
5
$$

Therefore:

$$
\boxed{125\text{ is divisible by 5}}
$$

---

## Example 2

Check:

$$
340
$$

Last digit:

$$
0
$$

Therefore:

$$
\boxed{340\text{ is divisible by 5}}
$$

---

## Example 3

Check:

$$
127
$$

Last digit:

$$
7
$$

Therefore:

$$
\boxed{127\text{ is not divisible by 5}}
$$

---

## Example 4

Check:

$$
9876543215
$$

Last digit:

$$
5
$$

Therefore:

$$
\boxed{9876543215\text{ is divisible by 5}}
$$

No complete division is required.

---

# 5. Connection With Multiples of 5

The multiples of `5` follow the pattern:

$$
5,10,15,20,25,30,35,40,\ldots
$$

Their last digits alternate:

$$
5,0,5,0,5,0,\ldots
$$

Therefore:

$$
\boxed{\text{Every multiple of 5 ends in 0 or 5}}
$$

---

# 6. Connection With Divisibility by 10

Since:

$$
10=2\times5
$$

a number divisible by `10` must be divisible by `5`.

Therefore:

$$
\boxed{\text{Divisible by 10}\Rightarrow\text{Divisible by 5}}
$$

But the reverse is not always true.

### Example

`25` is divisible by `5`:

$$
25\div5=5
$$

but:

$$
25\div10=2.5
$$

Therefore:

$$
\boxed{25\text{ is divisible by 5 but not by 10}}
$$

> [!important] Pattern
> **Divisibility by `10` is stricter than divisibility by `5`.**

---

# 7. Connection With Divisibility by 2

A number ending in `0` is divisible by both `2` and `5`.

A number ending in `5` is divisible by `5` but not by `2`.

### Therefore

| Last Digit | Divisible by 2 | Divisible by 5 |
|---:|:---:|:---:|
| `0` | ✅ | ✅ |
| `5` | ❌ | ✅ |

> [!tip] Important Pattern
> **A number divisible by both `2` and `5` must end in `0`.**

---

# 8. Divisibility by 10 Pattern

Because:

$$
10=2\times5
$$

we get:

$$
\boxed{\text{Divisible by 2 and 5}\Rightarrow\text{Divisible by 10}}
$$

### Example

`250`:

- Last digit `0` → divisible by `2`
- Last digit `0` → divisible by `5`

Therefore:

$$
\boxed{250\text{ is divisible by 10}}
$$

---

# 9. Missing Digit Problems

## Pattern 1 — One Missing Digit

Find `x` such that:

$$
73x
$$

is divisible by `5`.

The last digit must be:

$$
0\text{ or }5
$$

Therefore:

$$
\boxed{x\in\{0,5\}}
$$

---

# 10. Pattern — Largest Missing Digit

Find the largest digit `x` such that:

$$
428x
$$

is divisible by `5`.

Possible values:

$$
0,5
$$

Largest:

$$
\boxed{x=5}
$$

---

# 11. Pattern — Smallest Missing Digit

Find the smallest digit `x` such that:

$$
921x
$$

is divisible by `5`.

Possible values:

$$
0,5
$$

Smallest:

$$
\boxed{x=0}
$$

> [!warning] Check Conditions
> If the question says the number is a **positive number** and `x` is the first digit, then `0` may not be allowed.
>
> Always check whether the missing digit is the units digit or a leading digit.

---

# 12. Pattern — Divisibility by 15

Since:

$$
15=3\times5
$$

a number is divisible by `15` if it is divisible by both `3` and `5`.

### Example

Check:

$$
345
$$

For `5`:

Last digit:

$$
5
$$

So it is divisible by `5`.

For `3`:

$$
3+4+5=12
$$

`12` is divisible by `3`.

Therefore:

$$
\boxed{345\text{ is divisible by 15}}
$$

---

# 13. Pattern — Missing Digit for Divisibility by 15

Find `x` such that:

$$
42x
$$

is divisible by `15`.

### Condition 1: Divisible by 5

Therefore:

$$
x\in\{0,5\}
$$

### Condition 2: Divisible by 3

Digit sum:

$$
4+2+x=6+x
$$

For `x=0`:

$$
6+0=6
$$

which is divisible by `3`.

For `x=5`:

$$
6+5=11
$$

which is not divisible by `3`.

Therefore:

$$
\boxed{x=0}
$$

---

# 14. Pattern — Remainder

For a number divisible by `5`:

$$
\boxed{N\bmod5=0}
$$

If it is not divisible by `5`, the remainder can be:

$$
1,2,3,\text{ or }4
$$

### Example

Find the remainder when:

$$
127
$$

is divided by `5`.

Last digit is `7`.

Since:

$$
127=5(25)+2
$$

remainder:

$$
\boxed{2}
$$

---

# 15. Pattern — Remainder of a Large Number

Find:

$$
98765432198765\bmod5
$$

Only the last digit matters:

$$
5
$$

Therefore:

$$
\boxed{0}
$$

> [!tip] Exam Shortcut
> **Huge number + divisor `5` → check only the last digit.**

---

# 16. Pattern — Count Multiples of 5

The number of positive multiples of `5` from `1` to `N` is:

$$
\boxed{\left\lfloor\frac N5\right\rfloor}
$$

### Example

How many numbers from `1` to `100` are divisible by `5`?

$$
\left\lfloor\frac{100}{5}\right\rfloor
$$

$$
\boxed{20}
$$

---

# 17. Pattern — Multiples in a Range

The number of integers divisible by `5` between `A` and `B`, inclusive, is:

$$
\boxed{
\left\lfloor\frac B5\right\rfloor
-
\left\lfloor\frac{A-1}{5}\right\rfloor
}
$$

### Example

How many numbers from `20` to `80` are divisible by `5`?

$$
\left\lfloor\frac{80}{5}\right\rfloor
-
\left\lfloor\frac{19}{5}\right\rfloor
$$

$$
=16-3
$$

$$
\boxed{13}
$$

---

# 18. Pattern — Number Formation

Suppose you need to form a number divisible by `5`.

The **units digit** has only two possibilities:

$$
\boxed{0\text{ or }5}
$$

### Example

How many three-digit numbers are divisible by `5`?

Three-digit numbers:

$$
100\text{ to }999
$$

The first multiple of `5` is:

$$
100
$$

The last multiple of `5` is:

$$
995
$$

Number of terms:

$$
\frac{995-100}{5}+1
$$

$$
=\frac{895}{5}+1
$$

$$
=179+1
$$

$$
\boxed{180}
$$

---

# 19. Pattern — Last Digit Restriction

If a number must be divisible by `5`, its units digit has:

$$
\boxed{2\text{ choices}}
$$

Those choices are:

$$
\boxed{0,5}
$$

This becomes very useful in **number-formation and counting problems**.

---

# 20. Pattern — Divisibility by 25

A number is divisible by `25` if its last two digits are:

$$
\boxed{00,25,50,75}
$$

### Example

Check:

$$
1275
$$

Last two digits:

$$
75
$$

Therefore:

$$
\boxed{1275\text{ is divisible by 25}}
$$

---

# 21. Pattern — Divisibility by 50

A number is divisible by `50` if its last two digits are:

$$
\boxed{00\text{ or }50}
$$

Examples:

$$
150,\quad250,\quad500,\quad750
$$

are divisible by `50`.

---

# 22. Pattern — Divisibility by 100

A number is divisible by `100` if its last two digits are:

$$
\boxed{00}
$$

Therefore:

$$
\boxed{\text{Divisible by 100}\Rightarrow\text{Divisible by 5}}
$$

---

# 23. Important Formula Sheet

> [!important] Must Remember

| Concept | Rule |
|---|---|
| Divisibility by `5` | Last digit `0` or `5` |
| Remainder `0` | Last digit `0` or `5` |
| Divisibility by `10` | Last digit `0` |
| Divisibility by `15` | Divisible by `3` and `5` |
| Divisibility by `25` | Last 2 digits `00,25,50,75` |
| Divisibility by `50` | Last 2 digits `00` or `50` |
| Divisibility by `100` | Last 2 digits `00` |
| Multiples from `1` to `N` | `⌊N/5⌋` |
| Multiples from `A` to `B` | `⌊B/5⌋ − ⌊(A−1)/5⌋` |

---

# 24. Important Patterns

> [!important] Remember These

### Pattern 1

$$
\boxed{\text{Last digit }0\text{ or }5\Rightarrow\text{Divisible by 5}}
$$

### Pattern 2

$$
\boxed{\text{Divisible by 2 and 5}\Rightarrow\text{Divisible by 10}}
$$

### Pattern 3

$$
\boxed{\text{Divisible by 3 and 5}\Rightarrow\text{Divisible by 15}}
$$

### Pattern 4

$$
\boxed{\text{Last 2 digits }00,25,50,75\Rightarrow\text{Divisible by 25}}
$$

---

# 25. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Checking the whole number unnecessarily.
- ❌ Thinking a number ending in `0` or `5` is automatically divisible by `10`.
- ❌ Forgetting that numbers ending in `5` are not divisible by `2`.
- ❌ Confusing divisibility by `5` with divisibility by `25`.
- ❌ Checking the last two digits for divisibility by `5` when only the last digit is needed.
- ❌ Forgetting additional conditions in divisibility-by-15 problems.
- ❌ Assuming every number ending in `0` is divisible by `25`.
- ❌ Forgetting that `50` is divisible by `5` and `25`, but not by `100`.

---

# 26. Exam Strategy

> [!tip] 2-Second Method

When the divisor is `5`:

### Step 1

Look at the last digit.

### Step 2

Check:

$$
0\quad\text{or}\quad5
$$

### Step 3

Answer immediately.

### Example

$$
783492615
$$

Last digit:

$$
5
$$

Therefore:

$$
\boxed{\text{Divisible by 5}}
$$

---

# 27. HCL Preparation Priority

**Priority:** 🔥 Very High

### Master These First

1. Basic divisibility rule
2. Last-digit shortcut
3. Missing-digit problems
4. Divisibility by `10`
5. Divisibility by `15`
6. Divisibility by `25`
7. Divisibility by `50`
8. Counting multiples
9. Number-formation problems
10. Remainder questions

---

# 28. Practice Checklist

- [ ] Memorize `0 or 5`
- [ ] Practice direct divisibility questions
- [ ] Practice large-number questions
- [ ] Practice missing-digit questions
- [ ] Practice largest/smallest digit questions
- [ ] Practice remainder questions
- [ ] Practice counting multiples
- [ ] Practice number-formation questions
- [ ] Practice divisibility by `15`
- [ ] Practice divisibility by `25`
- [ ] Revise common traps

---

# 29. Related Topics

- [[Divisibility Rules]]
- [[Divisibility by 2]]
- [[Divisibility by 3]]
- [[Divisibility by 6]]
- [[Factors]]
- [[Multiples]]
- [[Remainders]]
- [[Digit Problems]]
- [[Number Formation]]
- [[Divisibility by 10]]

---

# 30. Quick Revision

> [!summary] One-Minute Revision

### Main Rule

$$
\boxed{
N\text{ is divisible by 5}
\iff
\text{Last digit is }0\text{ or }5
}
$$

### Multiples of 5

$$
5,10,15,20,25,30,\ldots
$$

### Divisibility by 10

$$
\boxed{\text{Last digit }0}
$$

### Divisibility by 25

$$
\boxed{00,25,50,75}
$$

### Divisibility by 50

$$
\boxed{00,50}
$$

### Counting Multiples

From `1` to `N`:

$$
\boxed{\left\lfloor\frac N5\right\rfloor}
$$

From `A` to `B`:

$$
\boxed{
\left\lfloor\frac B5\right\rfloor
-
\left\lfloor\frac{A-1}{5}\right\rfloor
}
$$

### Key Pattern

> **Divisibility by `5` → Check only the last digit.**

> **Last digit `0` or `5` → Divisible by `5`.**