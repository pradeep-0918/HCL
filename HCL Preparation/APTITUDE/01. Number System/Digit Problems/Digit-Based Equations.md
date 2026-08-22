---
type: concept
subject: aptitude
topic: "Digit-Based Equations"
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
  - digit-based-equations
  - algebra
  - number-formation
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Digit Problems]]"
  - "[[Number Formation]]"
  - "[[Digit Sum]]"
  - "[[Reverse of Number]]"
  - "[[Number of Digits]]"
  - "[[Divisibility Rules]]"
---

# Digit-Based Equations

## 1. Core Concept

> [!summary] Definition
> **Digit-based equations** convert a number into an algebraic expression using its digits.
>
> This is especially useful when a question gives:
>
> - a two-digit number
> - a three-digit number
> - a number and its reverse
> - digit sum
> - digit difference
> - a condition involving divisibility
> - a relation between digits

The main idea is:

$$
\boxed{
\text{Number}=\text{digit}\times\text{place value}
}
$$

---

# 2. Two-Digit Number

Let the tens digit be `x` and the units digit be `y`.

Then the number is:

$$
\boxed{
10x+y
}
$$

### Example

If the digits are `4` and `7`:

$$
N=10(4)+7
$$

$$
\boxed{47}
$$

> [!important]
> **Two-digit number → `10x + y`**

---

# 3. Reverse of a Two-Digit Number

Original:

$$
N=10x+y
$$

Reverse:

$$
\boxed{
R=10y+x
}
$$

### Example

For `47`:

$$
N=10(4)+7=47
$$

$$
R=10(7)+4=74
$$

---

# 4. Three-Digit Number

Let the digits be:

$$
x,\ y,\ z
$$

Then:

$$
\boxed{
N=100x+10y+z
}
$$

### Example

Digits:

$$
3,5,8
$$

Number:

$$
100(3)+10(5)+8
$$

$$
\boxed{358}
$$

---

# 5. Reverse of a Three-Digit Number

Original:

$$
N=100x+10y+z
$$

Reverse:

$$
\boxed{
R=100z+10y+x
}
$$

### Example

$$
358\rightarrow853
$$

---

# 6. Four-Digit Number

Let the digits be:

$$
a,b,c,d
$$

Then:

$$
\boxed{
N=1000a+100b+10c+d
}
$$

Reverse:

$$
\boxed{
R=1000d+100c+10b+a
}
$$

---

# 7. Place-Value Pattern

For an `n`-digit number:

$$
\boxed{
N=d_1\times10^{n-1}
+d_2\times10^{n-2}
+\cdots+d_n
}
$$

The position determines the multiplier.

| Position | Multiplier |
|---|---:|
| Units | `1` |
| Tens | `10` |
| Hundreds | `100` |
| Thousands | `1000` |
| Ten-thousands | `10000` |

---

# 8. Digit Sum Equation

For a two-digit number:

$$
N=10x+y
$$

digit sum:

$$
\boxed{
x+y
}
$$

Therefore:

$$
\boxed{
S(N)=x+y
}
$$

### Example

If digit sum is `11`:

$$
x+y=11
$$

---

# 9. Digit Difference Equation

For two digits `x` and `y`, if the difference is `d`:

$$
\boxed{
x-y=d
}
$$

or:

$$
\boxed{
|x-y|=d
}
$$

depending on the wording.

### Example

"The tens digit exceeds the units digit by `3`."

Then:

$$
\boxed{
x-y=3
}
$$

---

# 10. Sum and Difference of Digits

Suppose:

$$
x+y=S
$$

and:

$$
x-y=D
$$

Add the equations:

$$
2x=S+D
$$

Therefore:

$$
\boxed{
x=\frac{S+D}{2}
}
$$

Subtract:

$$
2y=S-D
$$

Therefore:

$$
\boxed{
y=\frac{S-D}{2}
}
$$

These are extremely useful formulas.

---

# 11. Example — Find the Digits

The sum of two digits is `11` and their difference is `3`.

We have:

$$
x+y=11
$$

$$
x-y=3
$$

Therefore:

$$
x=\frac{11+3}{2}=7
$$

and:

$$
y=\frac{11-3}{2}=4
$$

Therefore the digits are:

$$
\boxed{7,4}
$$

---

# 12. Number From Digit Sum and Difference

If the larger digit is `x` and smaller digit is `y`:

$$
x=\frac{S+D}{2}
$$

$$
y=\frac{S-D}{2}
$$

Then the two-digit number can be:

$$
\boxed{
10x+y
}
$$

### Example

Sum:

$$
S=13
$$

Difference:

$$
D=5
$$

Then:

$$
x=9
$$

$$
y=4
$$

Number:

$$
10(9)+4
$$

$$
\boxed{94}
$$

---

# 13. Important Pattern — Number and Reverse Sum

For:

$$
N=10x+y
$$

and:

$$
R=10y+x
$$

we get:

$$
N+R
=
10x+y+10y+x
$$

Therefore:

$$
\boxed{
N+R=11(x+y)
}
$$

This is one of the most important formulas in digit-based equations.

---

# 14. Important Pattern — Number and Reverse Difference

Similarly:

$$
N-R
=
10x+y-(10y+x)
$$

Therefore:

$$
\boxed{
N-R=9(x-y)
}
$$

If absolute difference is required:

$$
\boxed{
|N-R|=9|x-y|
}
$$

---

# 15. Example — Reverse Difference

A two-digit number exceeds its reverse by `36`.

Let:

$$
N=10x+y
$$

Then:

$$
N-R=36
$$

Therefore:

$$
9(x-y)=36
$$

So:

$$
x-y=4
$$

Possible digit pairs:

$$
4,0
$$

$$
5,1
$$

$$
6,2
$$

$$
7,3
$$

$$
8,4
$$

$$
9,5
$$

Additional information is needed to determine one unique number.

---

# 16. Example — Reverse Sum

A two-digit number and its reverse have sum `121`.

We know:

$$
N+R=11(x+y)
$$

Therefore:

$$
11(x+y)=121
$$

So:

$$
x+y=11
$$

Possible digit pairs include:

$$
2,9
$$

$$
3,8
$$

$$
4,7
$$

$$
5,6
$$

etc.

---

# 17. Important Pattern — Number Exceeds Reverse

If a two-digit number:

$$
N=10x+y
$$

is greater than its reverse, then:

$$
10x+y>10y+x
$$

Therefore:

$$
9x>9y
$$

Hence:

$$
\boxed{x>y}
$$

So:

> **If the number is greater than its reverse, the tens digit is greater than the units digit.**

---

# 18. Important Pattern — Reverse Exceeds Number

Similarly:

$$
R>N
$$

means:

$$
\boxed{y>x}
$$

The units digit is greater than the tens digit.

---

# 19. Three-Digit Digit Sum

For:

$$
N=100x+10y+z
$$

digit sum:

$$
\boxed{
x+y+z
}
$$

### Example

If the digit sum is `15`:

$$
\boxed{
x+y+z=15
}
$$

---

# 20. Three-Digit Reverse Difference

Original:

$$
N=100x+10y+z
$$

Reverse:

$$
R=100z+10y+x
$$

Therefore:

$$
N-R
=
100x+10y+z-100z-10y-x
$$

Thus:

$$
\boxed{
N-R=99(x-z)
}
$$

Notice that the middle digit `y` disappears.

> [!important]
> **For a 3-digit number, the reverse difference depends only on the first and last digits.**

---

# 21. Example — Three-Digit Reverse Difference

Let:

$$
N=572
$$

Then:

$$
x=5,\quad y=7,\quad z=2
$$

Therefore:

$$
N-R=99(5-2)
$$

$$
=99\times3
$$

$$
\boxed{297}
$$

Actual:

$$
572-275=297
$$

---

# 22. Three-Digit Palindrome

A three-digit number is a palindrome if:

$$
x=z
$$

because:

$$
xyz=z y x
$$

Therefore:

$$
\boxed{
x=z
}
$$

Its form is:

$$
\boxed{
xyx
}
$$

---

# 23. Four-Digit Digit Equation

For:

$$
N=1000a+100b+10c+d
$$

digit sum:

$$
\boxed{
a+b+c+d
}
$$

Reverse:

$$
\boxed{
1000d+100c+10b+a
}
$$

---

# 24. Divisibility by 3

For:

$$
N=10x+y
$$

the number is divisible by `3` if:

$$
\boxed{
x+y\equiv0\pmod3
}
$$

For three digits:

$$
\boxed{
x+y+z\equiv0\pmod3
}
$$

---

# 25. Divisibility by 9

For a two-digit number:

$$
\boxed{
x+y\equiv0\pmod9
}
$$

For a three-digit number:

$$
\boxed{
x+y+z\equiv0\pmod9
}
$$

---

# 26. Divisibility by 11

For:

$$
N=10x+y
$$

the divisibility condition is:

$$
x-y\equiv0\pmod{11}
$$

For a three-digit number:

$$
N=100x+10y+z
$$

the alternating sum is:

$$
\boxed{
x-y+z
}
$$

Therefore:

$$
\boxed{
11\mid N
\iff
x-y+z\equiv0\pmod{11}
}
$$

---

# 27. Divisibility by 4

For a two-digit number:

$$
10x+y
$$

the number is divisible by `4` if:

$$
\boxed{
10x+y\equiv0\pmod4
}
$$

More practically:

> **Check the two-digit number itself.**

For larger numbers, only the last two digits matter.

---

# 28. Divisibility by 5

For:

$$
N=10x+y
$$

divisibility by `5` requires:

$$
\boxed{
y=0\text{ or }5
}
$$

This directly restricts the units digit.

---

# 29. Even Number Condition

A two-digit number:

$$
10x+y
$$

is even when:

$$
\boxed{
y\in\{0,2,4,6,8\}
}
$$

---

# 30. Odd Number Condition

It is odd when:

$$
\boxed{
y\in\{1,3,5,7,9\}
}
$$

---

# 31. Digit Product

Sometimes the question gives the product of digits.

For a two-digit number:

$$
\boxed{
xy=P
}
$$

For a three-digit number:

$$
\boxed{
xyz=P
}
$$

### Example

The product of two digits is `24`.

Possible digit pairs include:

$$
3\times8
$$

and:

$$
4\times6
$$

---

# 32. Sum and Product of Two Digits

Suppose:

$$
x+y=S
$$

and:

$$
xy=P
$$

Then `x` and `y` are roots of:

$$
\boxed{
t^2-St+P=0
}
$$

This is a useful algebraic shortcut.

---

# 33. Example — Sum and Product

Two digits have:

$$
x+y=9
$$

and:

$$
xy=20
$$

Then:

$$
t^2-9t+20=0
$$

Factor:

$$
(t-4)(t-5)=0
$$

Therefore:

$$
\boxed{x,y=4,5}
$$

The possible two-digit numbers are:

$$
45,\ 54
$$

---

# 34. Important Pattern — Sum and Product

If:

$$
x+y=S
$$

and:

$$
xy=P
$$

then:

$$
\boxed{
x,y\text{ are roots of }t^2-St+P=0
}
$$

This is useful when direct trial is difficult.

---

# 35. Digit Difference and Product

Suppose:

$$
x-y=D
$$

and:

$$
xy=P
$$

Then:

$$
x=y+D
$$

Substitute:

$$
y(y+D)=P
$$

Therefore:

$$
\boxed{
y^2+Dy-P=0
}
$$

Then solve for the digits.

---

# 36. Example

Two digits differ by `2` and their product is `24`.

Let:

$$
x-y=2
$$

Therefore:

$$
x=y+2
$$

Product:

$$
y(y+2)=24
$$

So:

$$
y^2+2y-24=0
$$

Factor:

$$
(y+6)(y-4)=0
$$

Digit:

$$
y=4
$$

Therefore:

$$
x=6
$$

Digits:

$$
\boxed{6,4}
$$

---

# 37. Digit Equation From a Number Relation

Suppose a two-digit number is `27` more than its reverse.

Let:

$$
N=10x+y
$$

and:

$$
R=10y+x
$$

Then:

$$
10x+y=10y+x+27
$$

Simplify:

$$
9x-9y=27
$$

Therefore:

$$
\boxed{x-y=3}
$$

This converts a number problem into a simple digit equation.

---

# 38. Number Is a Multiple of Its Digit Sum

Suppose:

$$
N=10x+y
$$

and:

$$
N=k(x+y)
$$

Then:

$$
10x+y=kx+ky
$$

Rearrange:

$$
\boxed{
(10-k)x=(k-1)y
}
$$

This type of equation can be solved using digit constraints:

$$
0\le x,y\le9
$$

with:

$$
x\ne0
$$

---

# 39. Digit Constraints

Whenever `x` and `y` represent digits:

$$
\boxed{
0\le x\le9
}
$$

$$
\boxed{
0\le y\le9
}
$$

If `x` is the first digit of a multi-digit number:

$$
\boxed{
1\le x\le9
}
$$

These constraints are essential.

---

# 40. Three-Digit Digit Constraints

For:

$$
N=100x+10y+z
$$

we have:

$$
\boxed{
1\le x\le9
}
$$

and:

$$
\boxed{
0\le y,z\le9
}
$$

If the problem says digits are distinct:

$$
\boxed{
x\ne y,\quad y\ne z,\quad x\ne z
}
$$

---

# 41. Important Pattern — Distinct Digits

If digits are distinct, add:

$$
\boxed{
x_i\ne x_j
}
$$

for every pair of positions.

### Example

For:

$$
100x+10y+z
$$

distinct digits require:

$$
x\ne y
$$

$$
y\ne z
$$

$$
x\ne z
$$

---

# 42. Important Pattern — Repeated Digits

If two digits are equal:

$$
x=y
$$

then the number has a repeated digit.

### Example

Three-digit palindrome:

$$
xyx
$$

has:

$$
\boxed{x=z}
$$

---

# 43. Digit-Based Equation With Reverse

A common structure is:

$$
N+R=A
$$

or:

$$
N-R=A
$$

For two digits, immediately substitute:

$$
N=10x+y
$$

$$
R=10y+x
$$

Then simplify.

This should become automatic.

---

# 44. Example

A two-digit number and its reverse have a difference of `45`.

Set:

$$
N-R=45
$$

Then:

$$
9(x-y)=45
$$

Therefore:

$$
x-y=5
$$

Possible pairs:

$$
5,0
$$

$$
6,1
$$

$$
7,2
$$

$$
8,3
$$

$$
9,4
$$

So the possible numbers are:

$$
\boxed{50,61,72,83,94}
$$

if the original number is greater than its reverse.

---

# 45. Important Pattern — Difference Must Be Divisible by 9

For any two-digit number and its reverse:

$$
N-R=9(x-y)
$$

Therefore:

$$
\boxed{
N-R\text{ must be divisible by }9
}
$$

So if a question gives a difference like:

$$
28
$$

there is immediately:

$$
\boxed{\text{No solution}}
$$

because:

$$
28
$$

is not divisible by `9`.

---

# 46. Important Pattern — Sum Must Be Divisible by 11

For a two-digit number:

$$
N+R=11(x+y)
$$

Therefore:

$$
\boxed{
N+R\text{ must be divisible by }11
}
$$

If the given sum is not divisible by `11`, no solution exists.

---

# 47. Number Formation From Digit Equations

Suppose:

$$
x+y=10
$$

and:

$$
x-y=4
$$

Then:

$$
x=7
$$

and:

$$
y=3
$$

The number can be:

$$
\boxed{73}
$$

If the problem does not specify which digit is larger, the reverse:

$$
37
$$

may also be possible.

---

# 48. Important Pattern — Check Uniqueness

After solving digit equations, always ask:

> **Does the information identify one number or multiple numbers?**

For example:

$$
x+y=9
$$

alone gives many possibilities:

$$
0+9,\ 1+8,\ 2+7,\ldots
$$

Therefore:

$$
\boxed{
\text{One equation may not be enough}
}
$$

---

# 49. Common Aptitude Conditions

Digit-based equations commonly involve:

### Sum

$$
x+y=S
$$

### Difference

$$
x-y=D
$$

### Product

$$
xy=P
$$

### Number

$$
10x+y
$$

### Reverse

$$
10y+x
$$

### Palindrome

$$
x=z
$$

### Even

$$
y\in\{0,2,4,6,8\}
$$

### Divisible by 3

$$
x+y\equiv0\pmod3
$$

### Divisible by 9

$$
x+y\equiv0\pmod9
$$

---

# 50. Master Method

> [!tip] Universal Approach

When you see a digit equation:

### Step 1 — Assign Variables

For a two-digit number:

$$
N=10x+y
$$

For a three-digit number:

$$
N=100x+10y+z
$$

### Step 2 — Translate Every Statement

Convert words into equations.

### Step 3 — Solve

Use algebra.

### Step 4 — Apply Digit Constraints

$$
0\le x,y,z\le9
$$

and first digit:

$$
\ne0
$$

### Step 5 — Check the Answer

Substitute back into the original condition.

---

# 51. Word-to-Equation Translation

| Statement | Equation |
|---|---|
| Sum of digits is `S` | `x + y = S` |
| Difference is `D` | `x - y = D` |
| Product is `P` | `xy = P` |
| Tens digit is 3 more | `x = y + 3` |
| Units digit is twice tens | `y = 2x` |
| Number | `10x + y` |
| Reverse | `10y + x` |
| Number is even | `y` is even |
| Number is odd | `y` is odd |
| Divisible by 3 | `x + y` divisible by 3 |
| Divisible by 9 | `x + y` divisible by 9 |

---

# 52. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Writing a two-digit number as `x + y`.
- ❌ Forgetting place values.
- ❌ Allowing the first digit to be zero.
- ❌ Confusing digit sum with the number itself.
- ❌ Forgetting the reverse formula.
- ❌ Ignoring digit constraints.
- ❌ Assuming one equation always gives one answer.
- ❌ Forgetting distinct-digit conditions.
- ❌ Using `x-y` when the question says absolute difference.
- ❌ Not checking the solution in the original equation.

---

# 53. Formula Sheet

> [!important] Must Remember

### Two-Digit Number

$$
\boxed{
N=10x+y
}
$$

### Reverse

$$
\boxed{
R=10y+x
}
$$

### Three-Digit Number

$$
\boxed{
N=100x+10y+z
}
$$

### Digit Sum

$$
\boxed{
S=x+y
}
$$

for two digits.

### Sum and Difference

$$
\boxed{
x=\frac{S+D}{2}
}
$$

$$
\boxed{
y=\frac{S-D}{2}
}
$$

### Reverse Sum

$$
\boxed{
N+R=11(x+y)
}
$$

### Reverse Difference

$$
\boxed{
N-R=9(x-y)
}
$$

### Three-Digit Reverse Difference

$$
\boxed{
N-R=99(x-z)
}
$$

### Sum and Product

$$
\boxed{
t^2-St+P=0
}
$$

where:

$$
S=x+y
$$

and:

$$
P=xy
$$

---

# 54. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
2\text{-digit number}=10x+y
}
$$

### Pattern 2

$$
\boxed{
3\text{-digit number}=100x+10y+z
}
$$

### Pattern 3

$$
\boxed{
\text{Reverse of }10x+y=10y+x
}
$$

### Pattern 4

$$
\boxed{
N+R=11(x+y)
}
$$

### Pattern 5

$$
\boxed{
N-R=9(x-y)
}
$$

### Pattern 6

$$
\boxed{
3\text{-digit }N-R=99(x-z)
}
$$

### Pattern 7

$$
\boxed{
x+y=S,\ x-y=D
}
$$

then:

$$
\boxed{
x=\frac{S+D}{2},\quad
y=\frac{S-D}{2}
}
$$

### Pattern 8

$$
\boxed{
x+y=S,\ xy=P
}
$$

then:

$$
\boxed{
t^2-St+P=0
}
$$

### Pattern 9

Always apply:

$$
\boxed{
0\le\text{digit}\le9
}
$$

### Pattern 10

First digit:

$$
\boxed{
1\le\text{first digit}\le9
}
$$

---

# 55. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Extremely High

This topic combines several Number System concepts and is frequently useful in aptitude problem solving.

### Master These First

1. Place-value representation
2. Two-digit equations
3. Three-digit equations
4. Reverse-number equations
5. Digit sum
6. Digit difference
7. Digit product
8. Sum and difference formulas
9. Divisibility conditions
10. Palindrome conditions
11. Distinct-digit constraints
12. Missing-digit equations
13. Number and reverse relationships

---

# 56. Practice Checklist

- [ ] Two-digit representation
- [ ] Three-digit representation
- [ ] Reverse equations
- [ ] Digit sum equations
- [ ] Digit difference equations
- [ ] Digit product equations
- [ ] Sum and difference of digits
- [ ] Sum and reverse
- [ ] Difference and reverse
- [ ] Palindrome equations
- [ ] Divisibility equations
- [ ] Missing digit
- [ ] Distinct digits
- [ ] Multiple solutions
- [ ] No-solution cases

---

# 57. Related Topics

- [[Digit Problems]]
- [[Number Formation]]
- [[Digit Sum]]
- [[Reverse of Number]]
- [[Number of Digits]]
- [[Divisibility Rules]]
- [[Divisibility by 3]]
- [[Divisibility by 9]]
- [[Remainders]]
- [[Factors]]

---

# 58. Quick Revision

> [!summary] One-Minute Revision

### Two Digits

$$
\boxed{
N=10x+y
}
$$

### Reverse

$$
\boxed{
R=10y+x
}
$$

### Three Digits

$$
\boxed{
N=100x+10y+z
}
$$

### Digit Sum

$$
\boxed{
x+y
}
$$

### Sum + Difference

$$
\boxed{
x=\frac{S+D}{2}
}
$$

$$
\boxed{
y=\frac{S-D}{2}
}
$$

### Number + Reverse

$$
\boxed{
N+R=11(x+y)
}
$$

### Number − Reverse

$$
\boxed{
N-R=9(x-y)
}
$$

### Three-Digit Reverse Difference

$$
\boxed{
N-R=99(x-z)
}
$$

### Digit Constraints

$$
\boxed{
0\le x,y,z\le9
}
$$

First digit:

$$
\boxed{
1\le x\le9
}
$$

### Golden Memory Trick

> **Whenever a question says "two-digit number", immediately write `10x + y`. Whenever it says "reverse", write `10y + x`.**

### One-Line Recognition

> **Digit problem + unknown digits → convert the number into place-value algebra first, then translate every condition into an equation.**