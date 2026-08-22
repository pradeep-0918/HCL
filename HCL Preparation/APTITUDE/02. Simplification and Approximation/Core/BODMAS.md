---
type: concept
subject: aptitude
topic: "BODMAS"
parent: "02. Simplification and Approximation"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - simplification
  - approximation
  - bodmas
  - quantitative-aptitude
wikilinks:
  - "[[02. Simplification and Approximation]]"
  - "[[Fractions]]"
  - "[[Decimals]]"
  - "[[Recurring Decimals]]"
  - "[[Surds]]"
  - "[[Indices and Exponents]]"
  - "[[Approximation]]"
  - "[[Simplification Tricks]]"
---

# BODMAS

## 1. Core Concept

> [!summary] Definition
> **BODMAS** is the standard order used to solve mathematical expressions containing multiple operations.
>
> BODMAS stands for:
>
> - **B** → Brackets
> - **O** → Orders
> - **D** → Division
> - **M** → Multiplication
> - **A** → Addition
> - **S** → Subtraction

The purpose of BODMAS is to ensure that everyone evaluates an expression in the same order.

---

# 2. BODMAS Order

The standard order is:

$$
\boxed{
\text{Brackets}
\rightarrow
\text{Orders}
\rightarrow
\text{Division}
\rightarrow
\text{Multiplication}
\rightarrow
\text{Addition}
\rightarrow
\text{Subtraction}
}
$$

Remember:

> **B → O → D → M → A → S**

---

# 3. What Are Orders?

**Orders** means powers, roots, and other exponent operations.

Examples:

$$
2^3
$$

$$
\sqrt{25}
$$

$$
5^{-2}
$$

Therefore:

$$
\boxed{
\text{Orders}=\text{powers, roots, exponents}
}
$$

---

# 4. Brackets

Brackets have the highest priority.

Common brackets:

$$
( )
$$

$$
[ ]
$$

$$
\{ \}
$$

When brackets are nested, solve the innermost bracket first.

---

# 5. Nested Brackets

Example:

$$
2+[3-(4-1)]
$$

First:

$$
(4-1)=3
$$

Then:

$$
[3-3]=0
$$

Finally:

$$
2+0=2
$$

Therefore:

$$
\boxed2
$$

---

# 6. Types of Brackets

Commonly used:

### Parentheses

$$
( )
$$

### Square brackets

$$
[ ]
$$

### Curly brackets

$$
\{ \}
$$

A common convention is:

$$
\boxed{
\{[()] \}
}
$$

Solve from the innermost bracket outward.

---

# 7. Division and Multiplication

A very important rule:

> [!important]
> **Division and multiplication have the same priority.**

Therefore, do **not** always perform division before multiplication.

Instead:

$$
\boxed{
\text{Solve from left to right}
}
$$

---

# 8. Example — Division and Multiplication

Consider:

$$
24\div6\times2
$$

Do from left to right:

$$
24\div6=4
$$

Then:

$$
4\times2=8
$$

Therefore:

$$
\boxed8
$$

Not:

$$
24\div(6\times2)
$$

---

# 9. Addition and Subtraction

Addition and subtraction also have the same priority.

Therefore:

$$
\boxed{
\text{Solve from left to right}
}
$$

---

# 10. Example — Addition and Subtraction

Consider:

$$
20-8+3
$$

Left to right:

$$
20-8=12
$$

$$
12+3=15
$$

Therefore:

$$
\boxed{15}
$$

---

# 11. Complete BODMAS Example

Solve:

$$
10+6\times2-8\div4
$$

### Step 1 — Multiplication

$$
6\times2=12
$$

### Step 2 — Division

$$
8\div4=2
$$

Expression becomes:

$$
10+12-2
$$

### Step 3 — Addition

$$
10+12=22
$$

### Step 4 — Subtraction

$$
22-2=20
$$

Therefore:

$$
\boxed{20}
$$

---

# 12. BODMAS With Brackets

Solve:

$$
5+[8-3]\times2
$$

First brackets:

$$
8-3=5
$$

Expression:

$$
5+5\times2
$$

Multiplication:

$$
5\times2=10
$$

Addition:

$$
5+10=15
$$

Therefore:

$$
\boxed{15}
$$

---

# 13. BODMAS With Powers

Solve:

$$
3+2^3\times2
$$

Order:

1. Power
2. Multiplication
3. Addition

Therefore:

$$
2^3=8
$$

$$
8\times2=16
$$

$$
3+16=19
$$

Answer:

$$
\boxed{19}
$$

---

# 14. BODMAS With Multiple Operations

Solve:

$$
20-[3+2^2]\times2
$$

First order:

$$
2^2=4
$$

Bracket:

$$
3+4=7
$$

Multiplication:

$$
7\times2=14
$$

Subtraction:

$$
20-14=6
$$

Therefore:

$$
\boxed6
$$

---

# 15. Important Rule — Same Priority

These operations have equal priority:

### Division and Multiplication

$$
\boxed{D=M}
$$

Solve left to right.

### Addition and Subtraction

$$
\boxed{A=S}
$$

Solve left to right.

This is one of the biggest BODMAS traps.

---

# 16. Wrong Approach

Consider:

$$
30\div5\times3
$$

A common mistake is:

$$
5\times3=15
$$

then:

$$
30\div15=2
$$

This is incorrect.

Correct:

$$
30\div5=6
$$

then:

$$
6\times3=18
$$

Therefore:

$$
\boxed{18}
$$

---

# 17. Important Pattern — Left to Right

Whenever operations have equal precedence:

$$
\boxed{
\text{Evaluate from left to right}
}
$$

Examples:

$$
a\div b\times c
$$

and:

$$
a-b+c
$$

must be evaluated left to right.

---

# 18. Fractions in BODMAS

A fraction bar acts like a grouping structure.

Example:

$$
\frac{6+4}{2}
$$

First calculate numerator:

$$
6+4=10
$$

Then:

$$
10\div2=5
$$

Therefore:

$$
\boxed5
$$

---

# 19. Important Fraction Pattern

For:

$$
\frac{a+b}{c}
$$

the numerator:

$$
a+b
$$

must be evaluated before division.

Therefore:

$$
\boxed{
\frac{a+b}{c}
=
(a+b)\div c
}
$$

---

# 20. Negative Numbers

BODMAS still applies when negative numbers are present.

Example:

$$
10-(-3)\times2
$$

Multiplication first:

$$
(-3)\times2=-6
$$

Then:

$$
10-(-6)
$$

$$
=16
$$

Therefore:

$$
\boxed{16}
$$

---

# 21. Sign Rules

Important multiplication/division rules:

$$
(+)\times(+)=+
$$

$$
(+)\times(-)=-
$$

$$
(-)\times(+) =-
$$

$$
(-)\times(-)=+
$$

The same sign rule applies to division.

Therefore:

> [!important]
> **Same signs → positive**
>
> **Different signs → negative**

---

# 22. Powers With Negative Signs

Be careful with:

$$
-2^2
$$

and:

$$
(-2)^2
$$

They are different.

### First

$$
-2^2=-(2^2)=-4
$$

### Second

$$
(-2)^2=4
$$

Therefore:

$$
\boxed{
-2^2\ne(-2)^2
}
$$

This is a very common aptitude trap.

---

# 23. Negative Powers

Example:

$$
2^{-2}
$$

Using:

$$
a^{-n}=\frac1{a^n}
$$

we get:

$$
2^{-2}=\frac1{2^2}
$$

$$
\boxed{\frac14}
$$

---

# 24. Zero Power

For:

$$
a\ne0
$$

we have:

$$
\boxed{
a^0=1
}
$$

Examples:

$$
5^0=1
$$

$$
100^0=1
$$

$$
(-7)^0=1
$$

---

# 25. BODMAS and Root

Roots are treated as orders.

Example:

$$
\sqrt{16}+3\times2
$$

First:

$$
\sqrt{16}=4
$$

Then:

$$
3\times2=6
$$

Finally:

$$
4+6=10
$$

Therefore:

$$
\boxed{10}
$$

---

# 26. BODMAS With Square Root

Solve:

$$
\sqrt{25}+2^3-4
$$

Orders:

$$
\sqrt{25}=5
$$

$$
2^3=8
$$

Then:

$$
5+8-4=9
$$

Therefore:

$$
\boxed9
$$

---

# 27. BODMAS With Nested Operations

Solve:

$$
[20-\{6+(2\times3)\}]\div2
$$

First:

$$
2\times3=6
$$

Then:

$$
6+6=12
$$

Then:

$$
20-12=8
$$

Finally:

$$
8\div2=4
$$

Therefore:

$$
\boxed4
$$

---

# 28. Simplification Strategy

For a complicated expression:

### Step 1

Solve innermost brackets.

### Step 2

Solve powers and roots.

### Step 3

Perform multiplication and division from left to right.

### Step 4

Perform addition and subtraction from left to right.

Therefore:

$$
\boxed{
B\rightarrow O\rightarrow(D,M)\rightarrow(A,S)
}
$$

---

# 29. Shortcut — Mark the Operations

For a long expression, mentally mark:

$$
\boxed{
[Brackets]\rightarrow[Orders]\rightarrow[\times,\div]\rightarrow[+,-]
}
$$

This reduces calculation mistakes.

---

# 30. Example — Long Expression

Solve:

$$
50-4\times[3+2^2]+18\div3
$$

### Orders

$$
2^2=4
$$

Expression:

$$
50-4\times[3+4]+18\div3
$$

### Brackets

$$
3+4=7
$$

Expression:

$$
50-4\times7+18\div3
$$

### Multiplication and Division

$$
4\times7=28
$$

$$
18\div3=6
$$

Expression:

$$
50-28+6
$$

### Left to right

$$
50-28=22
$$

$$
22+6=28
$$

Therefore:

$$
\boxed{28}
$$

---

# 31. BODMAS vs PEMDAS

You may encounter **PEMDAS** in some resources.

### BODMAS

- Brackets
- Orders
- Division
- Multiplication
- Addition
- Subtraction

### PEMDAS

- Parentheses
- Exponents
- Multiplication
- Division
- Addition
- Subtraction

The important point is:

> [!important]
> **Multiplication and division have the same precedence.**
>
> **Addition and subtraction have the same precedence.**

So both systems lead to the same correct evaluation when applied properly.

---

# 32. Common Aptitude Question Pattern

Expressions often look like:

$$
\frac{a+b}{c}\times d-e
$$

Use:

1. Numerator
2. Division
3. Multiplication
4. Subtraction

Never randomly calculate from the visual order.

---

# 33. Common Trap — Fraction Bar

Consider:

$$
\frac{10+6}{2+2}
$$

Calculate the entire numerator and denominator:

$$
\frac{16}{4}
$$

Therefore:

$$
\boxed4
$$

Do not interpret it as:

$$
10+\frac62+2
$$

---

# 34. Common Trap — Bracket Multiplication

Consider:

$$
3(4+2)
$$

First:

$$
4+2=6
$$

Then:

$$
3\times6=18
$$

Therefore:

$$
\boxed{18}
$$

A number immediately before a bracket means multiplication.

---

# 35. Common Trap — Missing Multiplication Sign

Expressions such as:

$$
2(3+4)
$$

mean:

$$
2\times(3+4)
$$

Similarly:

$$
(2+3)(4+5)
$$

means:

$$
(2+3)\times(4+5)
$$

---

# 36. Common Trap — Nested Negative

Consider:

$$
5-[3-(2-7)]
$$

Start from inside:

$$
2-7=-5
$$

Then:

$$
3-(-5)=8
$$

Finally:

$$
5-8=-3
$$

Therefore:

$$
\boxed{-3}
$$

---

# 37. Common Trap — Division by a Fraction

Consider:

$$
6\div\frac32
$$

Division by a fraction means multiplication by its reciprocal:

$$
6\times\frac23
$$

Therefore:

$$
\boxed4
$$

This becomes important when solving fraction-based simplification questions.

---

# 38. Complex Fraction

Consider:

$$
\frac{\frac12+\frac13}{\frac56}
$$

Numerator:

$$
\frac12+\frac13
=
\frac36+\frac26
=
\frac56
$$

Therefore:

$$
\frac{\frac56}{\frac56}=1
$$

Answer:

$$
\boxed1
$$

---

# 39. Simplification With Zero

Important identities:

$$
a+0=a
$$

$$
a-0=a
$$

$$
a\times0=0
$$

$$
a\div1=a
$$

Therefore:

$$
\boxed{
0\text{ and }1\text{ are major simplification clues}
}
$$

---

# 40. Important Undefined Cases

Be careful:

$$
\boxed{
\frac{a}{0}\text{ is undefined}
}
$$

But:

$$
\boxed{
\frac0a=0,\quad a\ne0
}
$$

And:

$$
\boxed{
0^0
}
$$

should not be casually treated as `1` in general mathematical contexts.

---

# 41. Order of Operations — Master Table

| Priority | Operation |
|---:|---|
| 1 | Brackets |
| 2 | Powers / Roots |
| 3 | Division / Multiplication |
| 4 | Addition / Subtraction |

For equal priority:

$$
\boxed{\text{Left to right}}
$$

---

# 42. Speed Strategy for Aptitude

> [!tip] Fast Simplification Method

When solving an aptitude expression:

### 1. Scan for brackets

Solve them first.

### 2. Scan for powers and roots

Calculate them.

### 3. Look for multiplication/division

Calculate left to right.

### 4. Finish addition/subtraction

Calculate left to right.

### 5. Look for cancellation

Before doing large calculations, simplify obvious factors.

---

# 43. Cancellation Shortcut

Consider:

$$
\frac{25\times48}{5}
$$

Instead of:

$$
25\times48=1200
$$

then:

$$
1200\div5=240
$$

cancel first:

$$
25\div5=5
$$

Then:

$$
5\times48=240
$$

Therefore:

$$
\boxed{240}
$$

---

# 44. Common Factor Cancellation

For:

$$
\frac{a\times b}{a}
$$

where:

$$
a\ne0
$$

we get:

$$
\boxed b
$$

Example:

$$
\frac{17\times25}{17}=25
$$

This is a useful speed technique.

---

# 45. Multiplication by `5`

A quick shortcut:

$$
\times5=\times10\div2
$$

Example:

$$
48\times5
$$

$$
=480\div2
$$

$$
\boxed{240}
$$

---

# 46. Multiplication by `25`

Use:

$$
\boxed{
\times25=\times100\div4
}
$$

Example:

$$
36\times25
$$

$$
=3600\div4
$$

$$
\boxed{900}
$$

---

# 47. Multiplication by `125`

Use:

$$
\boxed{
\times125=\times1000\div8
}
$$

Example:

$$
24\times125
$$

$$
=24000\div8
$$

$$
\boxed{3000}
$$

---

# 48. Division by `5`

Use:

$$
\boxed{
\div5=\times2\div10
}
$$

Example:

$$
75\div5
$$

$$
=150\div10
$$

$$
\boxed{15}
$$

---

# 49. Division by `25`

Use:

$$
\boxed{
\div25=\times4\div100
}
$$

Example:

$$
300\div25
$$

$$
=1200\div100
$$

$$
\boxed{12}
$$

---

# 50. Division by `125`

Use:

$$
\boxed{
\div125=\times8\div1000
}
$$

Example:

$$
500\div125
$$

$$
=4000\div1000
$$

$$
\boxed4
$$

---

# 51. Important Squares

Memorize common squares:

$$
1^2=1
$$

$$
2^2=4
$$

$$
3^2=9
$$

$$
4^2=16
$$

$$
5^2=25
$$

$$
6^2=36
$$

$$
7^2=49
$$

$$
8^2=64
$$

$$
9^2=81
$$

$$
10^2=100
$$

Useful for fast simplification.

---

# 52. Important Cubes

Memorize:

$$
1^3=1
$$

$$
2^3=8
$$

$$
3^3=27
$$

$$
4^3=64
$$

$$
5^3=125
$$

$$
6^3=216
$$

$$
7^3=343
$$

$$
8^3=512
$$

$$
9^3=729
$$

$$
10^3=1000
$$

---

# 53. Approximation Connection

BODMAS is also important when approximation is involved.

Example:

$$
\frac{49.8\times20.2}{10.1}
$$

Approximate:

$$
49.8\approx50
$$

$$
20.2\approx20
$$

$$
10.1\approx10
$$

Then:

$$
\frac{50\times20}{10}
$$

$$
\boxed{100}
$$

The detailed approximation techniques will be covered in:

[[Approximation]]

---

# 54. HCL Question Recognition

If a question contains:

- `+`
- `-`
- `×`
- `÷`
- brackets
- powers
- roots
- fractions

then immediately think:

$$
\boxed{\text{BODMAS}}
$$

---

# 55. Common Traps

> [!warning] Must Avoid

### Trap 1

Doing multiplication before division automatically.

Wrong idea:

$$
a\div b\times c
\rightarrow
a\div(bc)
$$

Correct:

$$
\boxed{
a\div b\times c
}
$$

from left to right.

---

### Trap 2

Doing addition before subtraction automatically.

Correct:

$$
\boxed{
a-b+c
}
$$

from left to right.

---

### Trap 3

Ignoring brackets.

Wrong:

$$
2+3\times4=20
$$

Correct:

$$
2+12=14
$$

Therefore:

$$
\boxed{14}
$$

---

### Trap 4

Confusing:

$$
-3^2
$$

with:

$$
(-3)^2
$$

They are:

$$
-9
$$

and:

$$
9
$$

respectively.

---

# 56. Formula Sheet

> [!important] Must Remember

### BODMAS

$$
\boxed{
B\rightarrow O\rightarrow(D,M)\rightarrow(A,S)
}
$$

### Equal Priority

$$
\boxed{
D\leftrightarrow M:\text{ left to right}
}
$$

$$
\boxed{
A\leftrightarrow S:\text{ left to right}
}
$$

### Negative Power

$$
\boxed{
a^{-n}=\frac1{a^n}
}
$$

### Zero Power

$$
\boxed{
a^0=1,\quad a\ne0
}
$$

### Multiplication by 5

$$
\boxed{
\times5=\times10\div2
}
$$

### Multiplication by 25

$$
\boxed{
\times25=\times100\div4
}
$$

### Multiplication by 125

$$
\boxed{
\times125=\times1000\div8
}
$$

### Division by 5

$$
\boxed{
\div5=\times2\div10
}
$$

### Division by 25

$$
\boxed{
\div25=\times4\div100
}
$$

### Division by 125

$$
\boxed{
\div125=\times8\div1000
}
$$

---

# 57. High-Yield Patterns

> [!important] Must Master

### Pattern 1

$$
\boxed{
\text{Brackets first}
}
$$

### Pattern 2

$$
\boxed{
\text{Powers and roots next}
}
$$

### Pattern 3

$$
\boxed{
\text{Multiplication and division left to right}
}
$$

### Pattern 4

$$
\boxed{
\text{Addition and subtraction left to right}
}
$$

### Pattern 5

$$
\boxed{
\times5=\times10\div2
}
$$

### Pattern 6

$$
\boxed{
\times25=\times100\div4
}
$$

### Pattern 7

$$
\boxed{
\times125=\times1000\div8
}
$$

### Pattern 8

$$
\boxed{
\div5=\times2\div10
}
$$

### Pattern 9

$$
\boxed{
\div25=\times4\div100
}
$$

### Pattern 10

$$
\boxed{
\text{Cancel before multiplying when possible}
}
$$

---

# 58. HCL Preparation Priority

**Priority:** 🔥🔥🔥 Very High

Master these first:

1. BODMAS order
2. Bracket simplification
3. Powers and roots
4. Left-to-right multiplication/division
5. Left-to-right addition/subtraction
6. Fractions inside expressions
7. Negative numbers
8. Sign rules
9. Cancellation
10. Multiplication shortcuts
11. Division shortcuts
12. Mixed simplification expressions

---

# 59. Practice Checklist

- [ ] BODMAS order
- [ ] Nested brackets
- [ ] Powers
- [ ] Roots
- [ ] Multiplication
- [ ] Division
- [ ] Addition
- [ ] Subtraction
- [ ] Left-to-right rule
- [ ] Negative numbers
- [ ] Fractions
- [ ] Cancellation
- [ ] Multiplication by 5
- [ ] Multiplication by 25
- [ ] Multiplication by 125
- [ ] Division by 5
- [ ] Division by 25
- [ ] Division by 125
- [ ] Mixed BODMAS problems
- [ ] Approximation-based simplification

---

# 60. Related Topics

- [[02. Simplification and Approximation]]
- [[Fractions]]
- [[Decimals]]
- [[Recurring Decimals]]
- [[Surds]]
- [[Indices and Exponents]]
- [[Approximation]]
- [[Simplification Tricks]]

---

# 61. Quick Revision

> [!summary] One-Minute Revision

### BODMAS

$$
\boxed{
B\rightarrow O\rightarrow D/M\rightarrow A/S
}
$$

### Equal Priority

$$
\boxed{
D,M\rightarrow\text{left to right}
}
$$

$$
\boxed{
A,S\rightarrow\text{left to right}
}
$$

### Negative Power

$$
\boxed{
a^{-n}=\frac1{a^n}
}
$$

### Zero Power

$$
\boxed{
a^0=1
}
$$

### Fast Multiplication

$$
\boxed{
\times5=\times10\div2
}
$$

$$
\boxed{
\times25=\times100\div4
}
$$

$$
\boxed{
\times125=\times1000\div8
}
$$

### Golden Memory Trick

> **Brackets → Orders → ×/÷ left-to-right → +/− left-to-right.**

### One-Line Recognition

> **Whenever an aptitude question contains multiple mathematical operations, don't calculate immediately — first identify the BODMAS order.**