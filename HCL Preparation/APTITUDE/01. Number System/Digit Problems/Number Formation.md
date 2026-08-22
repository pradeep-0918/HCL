---
type: concept
subject: aptitude
topic: "Number Formation"
parent: "01. Number System/Digit Problems"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - digit-problems
  - number-formation
  - permutations
  - combinations
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Digit Problems]]"
  - "[[Digit Sum]]"
  - "[[Reverse of Number]]"
  - "[[Number of Digits]]"
  - "[[Digit-Based Equations]]"
---

# Number Formation

## 1. Core Concept

> [!summary] Definition
> **Number formation** deals with creating numbers using given digits while satisfying conditions such as:
>
> - no repetition
> - repetition allowed
> - even number
> - odd number
> - divisible by a number
> - greater than or less than a given number
> - fixed number of digits
> - specific first or last digit

The main idea is:

$$
\boxed{
\text{Number formation}=\text{position-based counting}
}
$$

---

# 2. Place Value

Every digit has a different value depending on its position.

For a 3-digit number:

$$
\boxed{
100a+10b+c
}
$$

For a 4-digit number:

$$
\boxed{
1000a+100b+10c+d
}
$$

For an `n`-digit number:

$$
\boxed{
a_n10^{n-1}+a_{n-1}10^{n-2}+\cdots+a_1
}
$$

---

# 3. Important Rule — First Digit Cannot Be Zero

A number cannot begin with `0`.

For example:

`0254` is not a 4-digit number.

It represents:

$$
254
$$

Therefore, when forming an `n`-digit number:

> [!important]
> **The first position cannot contain zero.**

This is one of the most common traps.

---

# 4. Example — Forming 3-Digit Numbers

Digits:

$$
1,2,3
$$

How many 3-digit numbers can be formed without repetition?

### Hundreds place

3 choices.

### Tens place

2 choices.

### Units place

1 choice.

Therefore:

$$
3\times2\times1
$$

$$
=3!
$$

Answer:

$$
\boxed6
$$

The numbers are:

$$
123,\ 132,\ 213,\ 231,\ 312,\ 321
$$

---

# 5. Permutation Formula

If `n` distinct objects are arranged using `r` positions:

$$
\boxed{
{}^nP_r=\frac{n!}{(n-r)!}
}
$$

This is the main formula for number formation without repetition.

---

# 6. Full Arrangement

If all `n` digits are used:

$$
\boxed{
n!
}
$$

### Example

5 distinct digits are available and all 5 must be used.

Number of arrangements:

$$
5!=120
$$

Therefore:

$$
\boxed{120}
$$

---

# 7. Example — 4-Digit Numbers

Digits:

$$
1,2,3,4,5
$$

How many 4-digit numbers can be formed without repetition?

Choose and arrange 4 digits from 5:

$$
{}^5P_4
$$

$$
=\frac{5!}{1!}
$$

$$
=120
$$

Answer:

$$
\boxed{120}
$$

---

# 8. Repetition Allowed

If repetition is allowed and there are `n` choices for every position, then for `r` positions:

$$
\boxed{
n^r
}
$$

### Example

Using digits:

$$
1,2,3,4
$$

how many 3-digit numbers can be formed if repetition is allowed?

Each position has `4` choices.

Therefore:

$$
4^3=64
$$

Answer:

$$
\boxed{64}
$$

---

# 9. Repetition Not Allowed

If repetition is not allowed:

$$
\boxed{
{}^nP_r
}
$$

### Example

Using:

$$
1,2,3,4
$$

form 3-digit numbers without repetition.

$$
{}^4P_3
=
4\times3\times2
$$

$$
\boxed{24}
$$

---

# 10. Basic Comparison

| Condition | Formula |
|---|---|
| Repetition allowed | \(n^r\) |
| Repetition not allowed | \({}^nP_r\) |
| All `n` used | \(n!\) |
| Choose only | \({}^nC_r\) |
| Arrange selected objects | \({}^nP_r\) |

---

# 11. Number Formation With Zero

Suppose digits are:

$$
0,1,2,3
$$

How many 3-digit numbers can be formed without repetition?

### First position

Cannot be `0`.

Therefore:

$$
3
$$

choices:

$$
1,2,3
$$

### Second position

3 remaining choices.

### Third position

2 remaining choices.

Therefore:

$$
3\times3\times2
$$

$$
\boxed{18}
$$

---

# 12. General Formula — Zero Included

Suppose there are:

- `n` total digits
- one of them is `0`
- `r` positions
- repetition not allowed

Then:

### First position

$$
n-1
$$

choices.

### Remaining positions

Choose from the remaining digits.

Therefore:

$$
\boxed{
(n-1)\times{}^{n-1}P_{r-1}
}
$$

---

# 13. Example

Digits:

$$
0,1,2,3,4
$$

How many 4-digit numbers can be formed without repetition?

First digit:

$$
4
$$

choices.

Remaining:

$$
4\times3\times2
$$

Therefore:

$$
4\times4\times3\times2
$$

$$
\boxed{96}
$$

---

# 14. Even Number Formation

A number is even if its last digit is:

$$
\boxed{
0,2,4,6,8
}
$$

Therefore, when forming an even number:

> [!important]
> **Start by fixing the units digit.**

This is one of the most important number-formation patterns.

---

# 15. Example — Even Numbers

Using digits:

$$
1,2,3,4,5
$$

form 3-digit even numbers without repetition.

Possible last digits:

$$
2,4
$$

So:

$$
2
$$

choices for the units position.

For each choice:

- hundreds: `4` choices
- tens: `3` choices

Therefore:

$$
2\times4\times3
$$

$$
\boxed{24}
$$

---

# 16. Odd Number Formation

A number is odd if its last digit is:

$$
\boxed{
1,3,5,7,9
}
$$

Therefore:

> **For odd-number formation, fix the last digit first.**

---

# 17. Example — Odd Numbers

Digits:

$$
1,2,3,4,5
$$

Form 3-digit odd numbers without repetition.

Possible last digits:

$$
1,3,5
$$

Therefore:

$$
3
$$

choices for the last digit.

Remaining positions:

$$
4\times3
$$

Therefore:

$$
3\times4\times3
$$

$$
\boxed{36}
$$

---

# 18. Divisibility by 5

A number is divisible by `5` if its last digit is:

$$
\boxed{0\text{ or }5}
$$

Therefore:

> **Fix the units digit first.**

This is exactly the same strategy as even-number formation.

---

# 19. Divisibility by 10

A number is divisible by `10` if its last digit is:

$$
\boxed0
$$

Therefore:

> **The final position is fixed immediately.**

This often reduces the problem to arranging the remaining digits.

---

# 20. Divisibility by 2

A number is divisible by `2` if its last digit is:

$$
\boxed{0,2,4,6,8}
$$

So for formation problems:

$$
\boxed{
\text{Check the units position first}
}
$$

---

# 21. Divisibility by 4

A number is divisible by `4` if its last two digits form a number divisible by `4`.

Therefore:

> [!important]
> **Fix or analyze the last two positions first.**

### Example

Possible endings:

$$
12,\ 16,\ 20,\ 24,\ 28,\ldots
$$

Then arrange the remaining digits.

---

# 22. Divisibility by 8

A number is divisible by `8` if its last three digits form a number divisible by `8`.

Therefore:

$$
\boxed{
\text{Analyze the last three positions first}
}
$$

This is a powerful number-formation pattern.

---

# 23. Divisibility by 3

A number is divisible by `3` if the sum of its digits is divisible by `3`.

Therefore:

$$
\boxed{
\text{Digit sum}\bmod3=0
}
$$

In formation problems, the key is often choosing a valid set of digits before arranging them.

---

# 24. Divisibility by 9

Similarly:

$$
\boxed{
\text{Digit sum}\bmod9=0
}
$$

So the **selection of digits** matters more than their order.

> [!tip]
> For divisibility by `3` or `9`, first analyze the **set of digits**, then arrange them.

---

# 25. Example — Divisible by 3

Using:

$$
1,2,3
$$

form 3-digit numbers without repetition that are divisible by `3`.

Digit sum:

$$
1+2+3=6
$$

Since:

$$
6\bmod3=0
$$

every arrangement is divisible by `3`.

Number of arrangements:

$$
3!=6
$$

Answer:

$$
\boxed6
$$

---

# 26. Number Formation With Repeated Digits

Suppose digits contain repetitions.

Example:

$$
1,1,2
$$

The arrangements are:

$$
112,\ 121,\ 211
$$

There are only:

$$
\boxed3
$$

distinct numbers.

---

# 27. Repeated-Digit Formula

If there are `n` total objects with repetitions:

$$
n_1,n_2,\ldots,n_k
$$

then the number of distinct arrangements is:

$$
\boxed{
\frac{n!}{n_1!n_2!\cdots n_k!}
}
$$

---

# 28. Example — Repeated Digits

How many distinct arrangements can be formed from:

$$
1,1,2,2,3
$$

There are `5` digits.

Two `1`s and two `2`s are repeated.

Therefore:

$$
\frac{5!}{2!2!}
$$

$$
=\frac{120}{4}
$$

$$
\boxed{30}
$$

---

# 29. Important Pattern — Fixed Position

If one digit must occupy a specific position:

> **Fix that digit first.**

Then arrange the remaining digits.

### Example

How many 4-digit numbers using:

$$
1,2,3,4
$$

have `2` in the thousands place?

Fix `2`.

Remaining:

$$
1,3,4
$$

can be arranged in:

$$
3!=6
$$

ways.

Answer:

$$
\boxed6
$$

---

# 30. Important Pattern — First Digit Fixed

If the first digit is fixed:

$$
\boxed{
\text{Arrange the remaining digits}
}
$$

Example:

4 distinct digits with first digit fixed:

$$
3!
$$

arrangements.

---

# 31. Important Pattern — Last Digit Fixed

If the last digit is fixed:

$$
\boxed{
\text{Arrange the remaining digits}
}
$$

Example:

5 distinct digits, last digit fixed:

$$
4!
$$

arrangements.

---

# 32. First and Last Digits Fixed

If both first and last digits are fixed, only the middle positions remain.

For `n` distinct digits:

$$
\boxed{
(n-2)!
}
$$

if all remaining digits are used.

---

# 33. Example

Digits:

$$
1,2,3,4,5
$$

How many 5-digit numbers have:

- `1` as first digit
- `5` as last digit?

Middle digits:

$$
2,3,4
$$

Number of arrangements:

$$
3!=6
$$

Answer:

$$
\boxed6
$$

---

# 34. Important Pattern — At Least One Condition

Questions may ask:

> How many numbers contain at least one `5`?

Use:

$$
\boxed{
\text{Total}-\text{Numbers without 5}
}
$$

This is the **complement method**.

---

# 35. Example — At Least One Digit

Using digits:

$$
1,2,3,4,5
$$

form 3-digit numbers without repetition containing at least one `5`.

### Total

$$
{}^5P_3=60
$$

### Without `5`

Use:

$$
1,2,3,4
$$

Form 3-digit numbers:

$$
{}^4P_3=24
$$

Therefore:

$$
60-24
$$

$$
\boxed{36}
$$

---

# 36. Important Pattern — Exactly One Condition

For exactly one occurrence of a particular digit:

1. Choose its position.
2. Fill the remaining positions without using that digit.

This is often easier than direct counting.

---

# 37. Example — Exactly One `5`

Using:

$$
1,2,3,4,5
$$

form 3-digit numbers without repetition containing exactly one `5`.

Choose position of `5`:

$$
3
$$

Remaining two positions:

$$
4\times3
$$

Therefore:

$$
3\times4\times3
$$

$$
\boxed{36}
$$

---

# 38. Important Pattern — At Most

"At most one `5`" means:

$$
\boxed{
0\text{ occurrences}+1\text{ occurrence}
}
$$

Break the problem into cases.

---

# 39. Important Pattern — Exactly Two Digits

If exactly two positions must contain a specific property:

1. Choose the positions.
2. Fill them.
3. Fill the remaining positions.

This often uses combinations plus permutations.

---

# 40. Permutation vs Combination

> [!important]

### Combination

Order does **not** matter.

$$
\boxed{
{}^nC_r=\frac{n!}{r!(n-r)!}
}
$$

### Permutation

Order **does** matter.

$$
\boxed{
{}^nP_r=\frac{n!}{(n-r)!}
}
$$

Number formation usually involves **permutations** because:

$$
123\ne321
$$

---

# 41. Important Pattern — "How Many Numbers?"

If the question asks:

> How many numbers can be formed?

Usually:

$$
\boxed{\text{Order matters}}
$$

Therefore permutation-style counting is often required.

---

# 42. Important Pattern — "How Many Sets?"

If the question asks:

> How many groups/sets can be selected?

Usually:

$$
\boxed{\text{Order does not matter}}
$$

Therefore combinations are often used.

---

# 43. Example — 3-Digit Number From 6 Digits

Digits:

$$
1,2,3,4,5,6
$$

No repetition.

Number of 3-digit numbers:

$$
{}^6P_3
$$

$$
=6\times5\times4
$$

$$
\boxed{120}
$$

---

# 44. Repetition Allowed — Zero Not Included

Digits:

$$
1,2,3,4,5
$$

Form 4-digit numbers with repetition allowed.

Every position has `5` choices:

$$
5^4
$$

$$
\boxed625
$$

---

# 45. Repetition Allowed — Zero Included

Digits:

$$
0,1,2,3,4
$$

Form 4-digit numbers with repetition allowed.

### First digit

Cannot be `0`.

Therefore:

$$
4
$$

choices.

### Remaining positions

Each has:

$$
5
$$

choices.

Therefore:

$$
4\times5^3
$$

$$
\boxed500
$$

---

# 46. Even Number With Repetition

Digits:

$$
0,1,2,3,4
$$

Form 3-digit even numbers with repetition allowed.

### Units digit

Possible:

$$
0,2,4
$$

So:

$$
3
$$

choices.

### Hundreds digit

Cannot be `0`:

$$
4
$$

choices.

### Tens digit

Any digit:

$$
5
$$

choices.

Therefore:

$$
4\times5\times3
$$

$$
\boxed60
$$

---

# 47. Odd Number With Repetition

Digits:

$$
0,1,2,3,4
$$

Form 3-digit odd numbers.

Units digit:

$$
1,3
$$

Therefore:

$$
2
$$

choices.

Hundreds:

$$
4
$$

choices.

Tens:

$$
5
$$

choices.

Therefore:

$$
4\times5\times2
$$

$$
\boxed40
$$

---

# 48. Important Pattern — Divisibility Condition Determines Positions

Different divisibility rules focus on different positions.

| Condition | Important positions |
|---|---|
| Even | Last digit |
| Divisible by `5` | Last digit |
| Divisible by `10` | Last digit |
| Divisible by `4` | Last 2 digits |
| Divisible by `8` | Last 3 digits |
| Divisible by `3` | Digit sum |
| Divisible by `9` | Digit sum |
| Divisible by `11` | Alternating digit sum |

> [!important] Recognition
> **Find which digits control the divisibility rule, then count those positions first.**

---

# 49. Number Formation Using Digits `0–9`

If no restrictions are given:

### 1-digit numbers

There are:

$$
10
$$

possible digits.

### `n`-digit numbers

First digit:

$$
9
$$

choices:

$$
1-9
$$

Remaining digits:

$$
10
$$

choices each if repetition is allowed.

Therefore:

$$
\boxed{
9\times10^{n-1}
}
$$

---

# 50. Example — 5-Digit Numbers

How many 5-digit numbers exist?

First digit:

$$
9
$$

Remaining:

$$
10^4
$$

Therefore:

$$
9\times10^4
$$

$$
\boxed{90000}
$$

---

# 51. Number Formation Without Repetition Using `0–9`

For an `n`-digit number without repetition:

### First digit

$$
9
$$

choices.

### Remaining positions

$$
9,\ 8,\ 7,\ldots
$$

Therefore:

$$
\boxed{
9\times{}^9P_{n-1}
}
$$

---

# 52. Example — 4-Digit Numbers Without Repetition

Using digits `0–9`:

First digit:

$$
9
$$

choices.

Second:

$$
9
$$

Third:

$$
8
$$

Fourth:

$$
7
$$

Therefore:

$$
9\times9\times8\times7
$$

$$
\boxed4536
$$

---

# 53. Number Formation — Greater Than a Given Number

When forming numbers greater than a particular number:

> [!tip]
> Compare digits **from left to right**.

For example, to compare:

$$
5234
$$

and:

$$
5129
$$

compare the thousands digit first.

Since:

$$
5=5
$$

compare hundreds:

$$
2>1
$$

Therefore:

$$
5234>5129
$$

---

# 54. Important Pattern — Lexicographical Counting

For numbers with the same number of digits:

> **The first differing digit determines which number is larger.**

Therefore, for questions asking:

- greater than
- smaller than
- between two numbers

start from the **leftmost digit**.

---

# 55. Number Formation — Smallest Number

To form the smallest possible number:

1. Choose the smallest valid non-zero digit for the first position.
2. Arrange remaining digits in ascending order.

### Example

Digits:

$$
0,2,3,5
$$

Smallest 4-digit number:

First digit cannot be `0`.

Choose:

$$
2
$$

Then arrange:

$$
0,3,5
$$

Therefore:

$$
\boxed{2035}
$$

---

# 56. Number Formation — Largest Number

To form the largest number:

> Arrange digits in descending order.

### Example

Digits:

$$
1,4,7,9
$$

Largest number:

$$
\boxed{9741}
$$

---

# 57. Number Formation — Repeated Digits

For digits:

$$
1,1,2,3
$$

number of distinct arrangements:

$$
\frac{4!}{2!}
$$

$$
\boxed{12}
$$

If the repeated digit is zero, additional care is required because the first digit cannot be zero.

---

# 58. Repeated Zero Trap

Digits:

$$
0,0,1,2
$$

Total arrangements:

$$
\frac{4!}{2!}=12
$$

But arrangements beginning with `0` are invalid.

Fix one `0` at the beginning.

Remaining:

$$
0,1,2
$$

Number of arrangements:

$$
3!=6
$$

Therefore valid numbers:

$$
12-6
$$

$$
\boxed6
$$

---

# 59. Formula Summary

> [!important] Core Formulas

### Permutation

$$
\boxed{
{}^nP_r=\frac{n!}{(n-r)!}
}
$$

### Combination

$$
\boxed{
{}^nC_r=\frac{n!}{r!(n-r)!}
}
$$

### Repetition Allowed

$$
\boxed{
n^r
}
$$

### All Distinct Digits

$$
\boxed{
n!
}
$$

### Repeated Objects

$$
\boxed{
\frac{n!}{n_1!n_2!\cdots n_k!}
}
$$

### `n`-Digit Numbers Using `0–9`, Repetition Allowed

$$
\boxed{
9\times10^{n-1}
}
$$

### `n`-Digit Numbers Using `0–9`, No Repetition

$$
\boxed{
9\times{}^9P_{n-1}
}
$$

---

# 60. High-Yield Patterns

> [!important] Must Master

### Pattern 1 — First Digit

$$
\boxed{
\text{Never zero}
}
$$

### Pattern 2 — Even Number

$$
\boxed{
\text{Fix the last digit}
}
$$

### Pattern 3 — Odd Number

$$
\boxed{
\text{Fix the last digit}
}
$$

### Pattern 4 — Divisible by `5`

$$
\boxed{
\text{Last digit}=0\text{ or }5
}
$$

### Pattern 5 — Divisible by `4`

$$
\boxed{
\text{Check last two digits}
}
$$

### Pattern 6 — Divisible by `8`

$$
\boxed{
\text{Check last three digits}
}
$$

### Pattern 7 — Divisible by `3` or `9`

$$
\boxed{
\text{Check digit sum}
}
$$

### Pattern 8 — Repetition Allowed

$$
\boxed{
n^r
}
$$

### Pattern 9 — No Repetition

$$
\boxed{
{}^nP_r
}
$$

### Pattern 10 — At Least One

$$
\boxed{
\text{Total}-\text{None}
}
$$

---

# 61. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Allowing `0` as the first digit.
- ❌ Using combinations when order matters.
- ❌ Using permutations when order does not matter.
- ❌ Forgetting whether repetition is allowed.
- ❌ Forgetting to fix the last digit for even/odd questions.
- ❌ Checking all digits for divisibility by `4` or `8`.
- ❌ Forgetting repeated digits.
- ❌ Counting duplicate arrangements separately.
- ❌ Using `n^r` when repetition is not allowed.
- ❌ Using `nPr` when repetition is allowed.
- ❌ Forgetting leading-zero restrictions.

---

# 62. Exam Decision Tree

> [!tip] Fast Recognition

### "Form `n`-digit numbers"

Ask:

**Is repetition allowed?**

- Yes → use powers.
- No → use permutation.

### "Even/Odd"

Look at:

$$
\boxed{\text{last digit}}
$$

### "Divisible by `5` or `10`"

Look at:

$$
\boxed{\text{last digit}}
$$

### "Divisible by `4`"

Look at:

$$
\boxed{\text{last two digits}}
$$

### "Divisible by `8`"

Look at:

$$
\boxed{\text{last three digits}}
$$

### "Divisible by `3` or `9`"

Look at:

$$
\boxed{\text{digit sum}}
$$

### "At least one"

Think:

$$
\boxed{\text{complement}}
$$

---

# 63. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

Number formation is a foundation for many aptitude questions involving:

- permutations
- digit problems
- divisibility
- probability
- counting
- arrangements

### Master These First

1. First digit cannot be zero
2. Repetition allowed
3. Repetition not allowed
4. Permutation
5. Even numbers
6. Odd numbers
7. Divisibility by `5`
8. Divisibility by `4`
9. Divisibility by `8`
10. Digit-sum conditions
11. Repeated digits
12. At least one / exactly one
13. Complement method
14. Smallest/largest number formation

---

# 64. Practice Checklist

- [ ] Basic number formation
- [ ] 2-digit numbers
- [ ] 3-digit numbers
- [ ] 4-digit numbers
- [ ] Repetition allowed
- [ ] Repetition not allowed
- [ ] Zero included
- [ ] Even numbers
- [ ] Odd numbers
- [ ] Divisible by `5`
- [ ] Divisible by `10`
- [ ] Divisible by `4`
- [ ] Divisible by `8`
- [ ] Divisible by `3`
- [ ] Divisible by `9`
- [ ] Repeated digits
- [ ] At least one digit
- [ ] Exactly one digit
- [ ] Smallest number
- [ ] Largest number
- [ ] Greater/smaller than a given number

---

# 65. Related Topics

- [[Digit Problems]]
- [[Digit Sum]]
- [[Reverse of Number]]
- [[Number of Digits]]
- [[Digit-Based Equations]]
- [[Divisibility Rules]]
- [[Factors]]
- [[Permutation and Combination]]
- [[Unit Digit]]

---

# 66. Quick Revision

> [!summary] One-Minute Revision

### Main Idea

$$
\boxed{
\text{Number formation}=\text{count valid choices for each position}
}
$$

### First Digit

$$
\boxed{
\text{Cannot be }0
}
$$

### Repetition Allowed

$$
\boxed{
n^r
}
$$

### Repetition Not Allowed

$$
\boxed{
{}^nP_r
}
$$

### Even Number

$$
\boxed{
\text{Last digit}\in\{0,2,4,6,8\}
}
$$

### Odd Number

$$
\boxed{
\text{Last digit}\in\{1,3,5,7,9\}
}
$$

### Divisible by `5`

$$
\boxed{
\text{Last digit}=0\text{ or }5
}
$$

### Divisible by `4`

$$
\boxed{
\text{Last two digits divisible by }4
}
$$

### Divisible by `8`

$$
\boxed{
\text{Last three digits divisible by }8
}
$$

### Divisible by `3` / `9`

$$
\boxed{
\text{Digit sum}
}
$$

### Golden Memory Trick

> **Number formation → position by position. Fix the restricted position first, especially the first or last digit.**

### One-Line Recognition

> **Counting numbers → ask "repetition?", "zero?", and "which position controls the condition?" before calculating.**