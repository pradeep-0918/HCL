---
type: concept
subject: reasoning
topic: "Mixed Pattern Series"
parent: "03. Series"
company: HCL
difficulty: hard
priority: very-high
status: not-started
tags:
  - reasoning
  - series
  - mixed-pattern-series
  - number-series
  - pattern-recognition
  - logical-reasoning
  - quantitative-reasoning
  - hcl
wikilinks:
  - "[[03. Series]]"
  - "[[Number Series]]"
  - "[[Missing Number Series]]"
  - "[[Wrong Number Series]]"
  - "[[Arithmetic Series]]"
  - "[[Geometric Series]]"
  - "[[Advanced Number Series]]"
---

# Mixed Pattern Series

## 1. Core Concept

> [!summary]
> A **Mixed Pattern Series** is a number sequence where the terms follow a combination of two or more operations or patterns rather than one simple rule.

Typical operations include:

- Addition
- Subtraction
- Multiplication
- Division
- Increasing differences
- Increasing multipliers
- Alternating operations
- Squares
- Cubes
- Prime numbers
- Previous-term relationships
- Previous-two-term relationships
- Position-based formulas

Example:

$$
3,\ 7,\ 15,\ 31,\ 63,\ ?
$$

At first glance, this is not a simple arithmetic series.

Check:

$$
3\times2+1=7
$$

$$
7\times2+1=15
$$

$$
15\times2+1=31
$$

$$
31\times2+1=63
$$

Therefore:

$$
63\times2+1=127
$$

Answer:

$$
\boxed{127}
$$

### Core Intuition

Think:

> **"If simple difference and ratio do not work, look for a repeated combination of operations."**

The main goal is:

$$
\boxed{\text{UNDERSTAND}\rightarrow\text{RECOGNIZE}\rightarrow\text{VERIFY}\rightarrow\text{SOLVE FAST}}
$$

---

# 2. Basic Meaning

A mixed pattern series does not necessarily have one constant difference or one constant ratio.

For example:

$$
4,\ 9,\ 19,\ 39,\ 79
$$

Differences are:

$$
5,\ 10,\ 20,\ 40
$$

The differences themselves double.

Another way to see it:

$$
4\times2+1=9
$$

$$
9\times2+1=19
$$

$$
19\times2+1=39
$$

$$
39\times2+1=79
$$

Therefore, this is a mixed-operation pattern.

---

# 3. Main Formula

There is no single formula for every mixed series.

The most common structures are:

## Multiplication + Constant

$$
\boxed{a_n=a_{n-1}\times k+c}
$$

Example:

$$
\times2+1
$$

---

## Multiplication - Constant

$$
\boxed{a_n=a_{n-1}\times k-c}
$$

Example:

$$
\times3-2
$$

---

## Increasing Addition

$$
\boxed{a_n=a_{n-1}+f(n)}
$$

Example:

$$
+2,+4,+6,+8
$$

---

## Increasing Multiplication

$$
\boxed{a_n=a_{n-1}\times f(n)}
$$

Example:

$$
\times2,\times3,\times4,\times5
$$

---

## Alternating Operations

$$
\boxed{\times2,\ +3,\ \times2,\ +3,\ldots}
$$

---

## Previous-Term Relationship

$$
\boxed{a_n=f(a_{n-1})}
$$

---

## Previous-Two-Term Relationship

$$
\boxed{a_n=f(a_{n-1},a_{n-2})}
$$

---

# 4. Important Properties

1. A mixed series may contain more than one operation.
2. The operation may remain the same while the constant changes.
3. The multiplier may increase or decrease.
4. Addition and multiplication may alternate.
5. Odd and even positions may follow separate patterns.
6. Differences may form another recognizable series.
7. Ratios may form another recognizable series.
8. Squares or cubes may be combined with addition or subtraction.
9. Previous terms may determine later terms.
10. A correct pattern must explain all or nearly all given terms.
11. Prefer the simplest consistent rule.
12. Do not invent complicated formulas when a simpler pattern works.

### Most Important Principle

$$
\boxed{\text{If one-level analysis fails, move to the next level.}}
$$

---

# 5. The Mixed-Series Solving Ladder

Use this order in an exam.

$$
\boxed{
1.\ Difference
}
$$

If that fails:

$$
\boxed{
2.\ Ratio
}
$$

If that fails:

$$
\boxed{
3.\ Difference\ of\ Differences
}
$$

If that fails:

$$
\boxed{
4.\ Alternating\ Terms
}
$$

Then:

$$
\boxed{
5.\ Mixed\ Operations
}
$$

Then:

$$
\boxed{
6.\ Squares/Cubes/Powers
}
$$

Then:

$$
\boxed{
7.\ Previous-Term\ Relationship
}
$$

Finally:

$$
\boxed{
8.\ Previous-Two-Term\ Relationship
}
$$

This prevents unnecessary guessing.

---

# 6. Basic Examples

## Example 1 — Multiply and Add

### Question

Find the next number:

$$
2,\ 5,\ 11,\ 23,\ 47,\ ?
$$

### Identify the Pattern

Check:

$$
2\times2+1=5
$$

$$
5\times2+1=11
$$

$$
11\times2+1=23
$$

$$
23\times2+1=47
$$

Therefore:

$$
47\times2+1=95
$$

### Answer

$$
\boxed{95}
$$

---

## Example 2 — Multiply and Subtract

### Question

$$
5,\ 13,\ 37,\ 109,\ ?
$$

Check:

$$
5\times3-2=13
$$

$$
13\times3-2=37
$$

$$
37\times3-2=109
$$

Therefore:

$$
109\times3-2=325
$$

### Answer

$$
\boxed{325}
$$

---

## Example 3 — Divide and Add

### Question

$$
100,\ 52,\ 28,\ 16,\ ?
$$

Check:

$$
100\div2+2=52
$$

$$
52\div2+2=28
$$

$$
28\div2+2=16
$$

Therefore:

$$
16\div2+2=10
$$

### Answer

$$
\boxed{10}
$$

---

# 7. Increasing Addition Pattern

## Example 4

### Question

$$
3,\ 5,\ 9,\ 15,\ 23,\ ?
$$

Differences:

$$
+2,+4,+6,+8
$$

The differences increase by:

$$
+2
$$

Next difference:

$$
+10
$$

Therefore:

$$
23+10=33
$$

### Answer

$$
\boxed{33}
$$

### Recognition

> [!important]
> If the differences themselves form:

$$
2,4,6,8,\ldots
$$

check an increasing-addition pattern.

---

# 8. Increasing Subtraction Pattern

## Example 5

### Question

$$
50,\ 48,\ 44,\ 38,\ 30,\ ?
$$

Differences:

$$
-2,-4,-6,-8
$$

Next:

$$
-10
$$

Therefore:

$$
30-10=20
$$

### Answer

$$
\boxed{20}
$$

---

# 9. Increasing Multiplication Pattern

## Example 6

### Question

$$
2,\ 4,\ 12,\ 48,\ 240,\ ?
$$

Check ratios:

$$
\times2,\times3,\times4,\times5
$$

Next:

$$
\times6
$$

Therefore:

$$
240\times6=1440
$$

### Answer

$$
\boxed{1440}
$$

> [!warning]
> This is not a normal GP because the ratio changes.

The pattern is:

$$
\times2,\times3,\times4,\times5,\times6
$$

---

# 10. Decreasing Multiplication Pattern

## Example 7

### Question

$$
720,\ 360,\ 120,\ 30,\ 6,\ ?
$$

Ratios:

$$
\div2,\div3,\div4,\div5
$$

Next:

$$
\div6
$$

Therefore:

$$
6\div6=1
$$

### Answer

$$
\boxed{1}
$$

---

# 11. Alternating Pattern

## Example 8

### Question

$$
3,\ 6,\ 8,\ 16,\ 18,\ 36,\ ?
$$

Operations:

$$
\times2,\ +2,\ \times2,\ +2,\ \times2
$$

Therefore:

$$
36+2=38
$$

### Answer

$$
\boxed{38}
$$

---

# 12. Alternating Multiplication and Subtraction

## Example 9

### Question

$$
5,\ 10,\ 8,\ 16,\ 14,\ 28,\ ?
$$

Pattern:

$$
\times2,\ -2,\ \times2,\ -2,\ \times2
$$

Therefore:

$$
28-2=26
$$

### Answer

$$
\boxed{26}
$$

---

# 13. Alternating Addition and Multiplication

## Example 10

### Question

$$
2,\ 5,\ 15,\ 18,\ 54,\ ?
$$

Pattern:

$$
+3,\times3,+3,\times3,+3
$$

Therefore:

$$
54+3=57
$$

### Answer

$$
\boxed{57}
$$

---

# 14. Odd-Even Position Pattern

Sometimes the operations are difficult to see because two separate sequences are interwoven.

## Example 11

### Question

$$
2,\ 10,\ 4,\ 20,\ 6,\ 30,\ ?
$$

Separate positions.

### Odd Positions

$$
2,\ 4,\ 6,\ ?
$$

Pattern:

$$
+2
$$

Therefore:

$$
8
$$

### Even Positions

$$
10,\ 20,\ 30
$$

Pattern:

$$
+10
$$

### Answer

$$
\boxed{8}
$$

---

# 15. Difference-of-Differences Pattern

## Example 12

### Question

$$
4,\ 7,\ 12,\ 19,\ 28,\ ?
$$

First differences:

$$
+3,+5,+7,+9
$$

Next difference:

$$
+11
$$

Therefore:

$$
28+11=39
$$

### Answer

$$
\boxed{39}
$$

---

# 16. Difference Pattern with Squares

## Example 13

### Question

$$
2,\ 3,\ 7,\ 16,\ 32,\ ?
$$

Differences:

$$
+1,+4,+9,+16
$$

These are:

$$
1^2,\ 2^2,\ 3^2,\ 4^2
$$

Next difference:

$$
5^2=25
$$

Therefore:

$$
32+25=57
$$

### Answer

$$
\boxed{57}
$$

---

# 17. Difference Pattern with Cubes

## Example 14

### Question

$$
1,\ 2,\ 10,\ 37,\ 101,\ ?
$$

Differences:

$$
+1,+8,+27,+64
$$

These are:

$$
1^3,\ 2^3,\ 3^3,\ 4^3
$$

Next:

$$
5^3=125
$$

Therefore:

$$
101+125=226
$$

### Answer

$$
\boxed{226}
$$

---

# 18. Multiplication Plus Increasing Addition

## Example 15

### Question

$$
2,\ 5,\ 12,\ 27,\ 58,\ ?
$$

Check:

$$
2\times2+1=5
$$

$$
5\times2+2=12
$$

$$
12\times2+3=27
$$

$$
27\times2+4=58
$$

Next:

$$
58\times2+5
$$

$$
=116+5
$$

$$
=121
$$

### Answer

$$
\boxed{121}
$$

### Pattern

$$
\times2+1
$$

$$
\times2+2
$$

$$
\times2+3
$$

$$
\times2+4
$$

---

# 19. Multiplication Plus Increasing Multiplier

## Example 16

### Question

$$
3,\ 7,\ 17,\ 43,\ 129,\ ?
$$

Try:

$$
3\times2+1=7
$$

$$
7\times2+3=17
$$

$$
17\times2+9=43
$$

This does not produce a simple consistent pattern.

> [!warning]
> Do not force a mixed-operation rule when the constants do not follow a clear sequence.

A professional solver should reject a weak pattern and test other possibilities.

---

# 20. Multiplication by Increasing Numbers + Constant

## Example 17

### Question

$$
1,\ 3,\ 10,\ 41,\ 206,\ ?
$$

Check:

$$
1\times2+1=3
$$

$$
3\times3+1=10
$$

$$
10\times4+1=41
$$

$$
41\times5+1=206
$$

Next:

$$
206\times6+1
$$

$$
=1236+1
$$

$$
=1237
$$

### Answer

$$
\boxed{1237}
$$

### Pattern

$$
\times2+1,\times3+1,\times4+1,\times5+1,\times6+1
$$

---

# 21. Square-Based Mixed Pattern

## Example 18

### Question

$$
2,\ 5,\ 10,\ 17,\ 26,\ ?
$$

Recognize:

$$
1^2+1=2
$$

$$
2^2+1=5
$$

$$
3^2+1=10
$$

$$
4^2+1=17
$$

$$
5^2+1=26
$$

Therefore:

$$
6^2+1=37
$$

### Answer

$$
\boxed{37}
$$

---

# 22. Cube-Based Mixed Pattern

## Example 19

### Question

$$
2,\ 9,\ 28,\ 65,\ ?
$$

Pattern:

$$
1^3+1=2
$$

$$
2^3+1=9
$$

$$
3^3+1=28
$$

$$
4^3+1=65
$$

Therefore:

$$
5^3+1=126
$$

### Answer

$$
\boxed{126}
$$

---

# 23. Previous-Term Pattern

## Example 20

### Question

$$
2,\ 5,\ 11,\ 23,\ 47,\ ?
$$

Each term:

$$
a_n=2a_{n-1}+1
$$

Therefore:

$$
a_6=2(47)+1
$$

$$
=95
$$

### Answer

$$
\boxed{95}
$$

---

# 24. Previous-Two-Term Pattern

## Example 21

### Question

$$
1,\ 2,\ 3,\ 5,\ 8,\ 13,\ ?
$$

Each term is:

$$
a_n=a_{n-1}+a_{n-2}
$$

Therefore:

$$
13+8=21
$$

### Answer

$$
\boxed{21}
$$

---

# 25. Previous-Two-Term Mixed Pattern

## Example 22

### Question

$$
1,\ 2,\ 4,\ 7,\ 12,\ 20,\ ?
$$

Check differences:

$$
+1,+2,+3,+5,+8
$$

These differences themselves resemble a Fibonacci pattern:

$$
1,\ 2,\ 3,\ 5,\ 8
$$

Therefore the next difference is:

$$
13
$$

Hence:

$$
20+13=33
$$

### Answer

$$
\boxed{33}
$$

---

# 26. Recursive Pattern with Multiplication

## Example 23

### Question

$$
1,\ 3,\ 10,\ 33,\ 108,\ ?
$$

Check:

$$
1\times3=3
$$

$$
3\times3+1=10
$$

$$
10\times3+3=33
$$

$$
33\times3+9=108
$$

This is not immediately simple.

> [!warning]
> A pattern should not be accepted merely because several terms can be manipulated to fit it. Look for a repeated, natural rule.

---

# 27. Advanced Exam-Style Pattern

## Example 24

### Question

$$
4,\ 9,\ 19,\ 39,\ 79,\ ?
$$

### Method 1 — Operation

$$
4\times2+1=9
$$

$$
9\times2+1=19
$$

$$
19\times2+1=39
$$

$$
39\times2+1=79
$$

Therefore:

$$
79\times2+1=159
$$

### Method 2 — Differences

Differences:

$$
+5,+10,+20,+40
$$

Next:

$$
+80
$$

Therefore:

$$
79+80=159
$$

Both methods agree.

### Answer

$$
\boxed{159}
$$

> [!important]
> When two independent methods confirm the same answer, confidence in the pattern is high.

---

# 28. Advanced Exam-Style Pattern — Increasing Operations

## Example 25

### Question

$$
2,\ 5,\ 17,\ 71,\ 359,\ ?
$$

Check:

$$
2\times2+1=5
$$

$$
5\times3+2=17
$$

$$
17\times4+3=71
$$

$$
71\times5+4=359
$$

Next:

$$
359\times6+5
$$

$$
=2154+5
$$

$$
=2159
$$

### Answer

$$
\boxed{2159}
$$

### Pattern

$$
\times2+1
$$

$$
\times3+2
$$

$$
\times4+3
$$

$$
\times5+4
$$

$$
\times6+5
$$

---

# 29. Advanced Exam-Style Pattern — Alternating Multipliers

## Example 26

### Question

$$
2,\ 6,\ 12,\ 36,\ 72,\ ?
$$

Pattern:

$$
\times3,\times2,\times3,\times2,\times3
$$

Therefore:

$$
72\times3=216
$$

### Answer

$$
\boxed{216}
$$

---

# 30. Advanced Exam-Style Pattern — Alternating Differences

## Example 27

### Question

$$
10,\ 13,\ 11,\ 14,\ 12,\ 15,\ ?
$$

Separate odd positions:

$$
10,\ 11,\ 12,\ ?
$$

Therefore:

$$
13
$$

Even positions:

$$
13,\ 14,\ 15
$$

Therefore the missing odd-position term is:

$$
\boxed{13}
$$

---

# 31. Advanced Exam-Style Pattern — Difference of Differences

## Example 28

### Question

$$
5,\ 9,\ 15,\ 23,\ 33,\ ?
$$

Differences:

$$
+4,+6,+8,+10
$$

Next:

$$
+12
$$

Therefore:

$$
33+12=45
$$

### Answer

$$
\boxed{45}
$$

---

# 32. Advanced Exam-Style Pattern — Difference as Powers

## Example 29

### Question

$$
3,\ 4,\ 8,\ 17,\ 33,\ ?
$$

Differences:

$$
+1,+4,+9,+16
$$

These are:

$$
1^2,\ 2^2,\ 3^2,\ 4^2
$$

Next:

$$
5^2=25
$$

Therefore:

$$
33+25=58
$$

### Answer

$$
\boxed{58}
$$

---

# 33. How to Solve Mixed Pattern Series

## Step 1 — Check First Differences

For:

$$
a_1,a_2,a_3,\ldots
$$

calculate:

$$
a_2-a_1
$$

$$
a_3-a_2
$$

$$
a_4-a_3
$$

Look for:

- Constant difference
- Increasing difference
- Decreasing difference
- Squares
- Cubes
- Alternating differences

---

## Step 2 — Check Ratios

Calculate:

$$
\frac{a_2}{a_1},
\frac{a_3}{a_2},
\frac{a_4}{a_3}
$$

Look for:

- Constant ratio
- Increasing ratio
- Decreasing ratio
- Alternating ratio

---

## Step 3 — Check Alternate Terms

Separate:

$$
a_1,a_3,a_5,\ldots
$$

and:

$$
a_2,a_4,a_6,\ldots
$$

This is one of the most important techniques.

---

## Step 4 — Check Mixed Operations

Try:

$$
\times k+c
$$

or:

$$
\times k-c
$$

Examples:

$$
\times2+1
$$

$$
\times3-2
$$

---

## Step 5 — Check Increasing Operations

Look for:

$$
\times2,\times3,\times4,\times5
$$

or:

$$
+2,+4,+6,+8
$$

---

## Step 6 — Check Powers

Test:

$$
n^2
$$

$$
n^3
$$

$$
2^n
$$

$$
3^n
$$

Also test:

$$
n^2+c
$$

or:

$$
n^3+c
$$

---

## Step 7 — Check Previous Terms

Try:

$$
a_n=2a_{n-1}+1
$$

or:

$$
a_n=a_{n-1}+a_{n-2}
$$

---

## Step 8 — Verify

A valid pattern must explain the complete sequence.

Use:

$$
\boxed{\text{Pattern}+\text{Verification}=\text{Confidence}}
$$

---

# 34. Pattern Recognition Tricks

## Pattern 1 — Difference Looks Structured

> [!important]
> If differences are:

$$
+2,+4,+6,+8
$$

think:

$$
\boxed{\text{Increasing even numbers}}
$$

---

## Pattern 2 — Differences Double

> [!important]
> If differences are:

$$
+5,+10,+20,+40
$$

think:

$$
\boxed{\text{Difference doubles}}
$$

This often corresponds to:

$$
\times2+c
$$

---

## Pattern 3 — Ratios Increase

> [!important]
> If ratios are:

$$
2,3,4,5
$$

think:

$$
\boxed{\text{Increasing multiplier}}
$$

---

## Pattern 4 — Operations Alternate

> [!important]
> If you see:

$$
\times2,+3,\times2,+3
$$

do not calculate one global difference.

Recognize the repeating operation cycle.

---

## Pattern 5 — Odd and Even Terms Behave Differently

> [!important]
> If the series looks irregular:

$$
2,\ 10,\ 4,\ 20,\ 6,\ 30
$$

split it immediately.

---

## Pattern 6 — Difference Is a Square

> [!important]
> If differences are:

$$
1,4,9,16
$$

think:

$$
\boxed{n^2}
$$

---

## Pattern 7 — Difference Is a Cube

> [!important]
> If differences are:

$$
1,8,27,64
$$

think:

$$
\boxed{n^3}
$$

---

## Pattern 8 — Number Doubles and Adds

> [!important]
> If:

$$
3,\ 7,\ 15,\ 31
$$

test:

$$
\times2+1
$$

---

## Pattern 9 — Number Triples and Subtracts

> [!important]
> If:

$$
4,\ 10,\ 28,\ 82
$$

test:

$$
\times3-2
$$

because:

$$
4\times3-2=10
$$

$$
10\times3-2=28
$$

$$
28\times3-2=82
$$

---

## Pattern 10 — Previous Two Terms

> [!important]
> If no simple operation works and terms look interconnected, test:

$$
a_n=a_{n-1}+a_{n-2}
$$

or a similar relationship.

---

# 35. Shortcuts

> [!tip]
> **Shortcut 1 — Difference first**

Do not immediately try complicated formulas.

Calculate:

$$
a_2-a_1,\ a_3-a_2,\ a_4-a_3
$$

first.

---

> [!tip]
> **Shortcut 2 — If differences double, test $\times2+c$**

Example:

$$
5,\ 11,\ 23,\ 47
$$

Differences:

$$
6,\ 12,\ 24
$$

Since differences double, test:

$$
\times2+1
$$

---

> [!tip]
> **Shortcut 3 — If ratios increase by 1, test increasing multiplication**

Example:

$$
2,\ 6,\ 24,\ 120
$$

Ratios:

$$
3,\ 4,\ 5
$$

The next operation is:

$$
\times6
$$

---

> [!tip]
> **Shortcut 4 — Split alternating terms early**

For:

$$
3,\ 10,\ 6,\ 20,\ 9,\ 30
$$

odd positions:

$$
3,\ 6,\ 9
$$

even positions:

$$
10,\ 20,\ 30
$$

---

> [!tip]
> **Shortcut 5 — Compare two methods**

If a sequence can be explained through both:

- Operations
- Differences

and both produce the same answer, the pattern is strongly supported.

---

> [!tip]
> **Shortcut 6 — Look at the growth speed**

### Slow growth

Check:

$$
+,\ -
$$

### Moderate growth

Check:

$$
\text{Increasing differences}
$$

### Fast growth

Check:

$$
\times,\ \text{powers}
$$

### Very irregular growth

Check:

$$
\text{Alternating or recursive patterns}
$$

---

# 36. Common Exam Patterns

> [!important] Must Master

### Difference-Based

1. Constant difference
2. Increasing difference
3. Decreasing difference
4. Differences doubling
5. Differences tripling
6. Differences following squares
7. Differences following cubes
8. Differences following Fibonacci

### Ratio-Based

9. Constant ratio
10. Increasing ratio
11. Decreasing ratio
12. Alternating ratio
13. Negative ratio
14. Fractional ratio

### Mixed Operations

15. $\times k+c$
16. $\times k-c$
17. $\div k+c$
18. $\div k-c$
19. $\times k+n$
20. $\times n+c$

### Alternating

21. $+a,-b$
22. $\times a,\div b$
23. $\times a,+b$
24. $+a,\times b$
25. Two alternating sequences

### Power-Based

26. Squares
27. Cubes
28. Powers of 2
29. Powers of 3
30. Square + constant
31. Cube + constant
32. Power-based differences

### Recursive

33. Previous-term relation
34. Previous-two-term relation
35. Fibonacci-type
36. Difference-based recursion

### Advanced

37. Position-based formulas
38. Multiple-level differences
39. Multiple-level ratios
40. Combined patterns
41. Digit-based transformations
42. Complex alternating patterns

---

# 37. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Assuming every series is AP

A sequence can have changing differences.

Example:

$$
2,\ 5,\ 9,\ 14
$$

Differences:

$$
3,4,5
$$

This is not an AP.

---

### Mistake 2 — Assuming every multiplication pattern is GP

Example:

$$
2,\ 4,\ 12,\ 48
$$

Ratios:

$$
2,3,4
$$

Not a GP.

---

### Mistake 3 — Ignoring alternating patterns

If one rule fails, immediately test:

$$
Odd\ positions
$$

and:

$$
Even\ positions
$$

---

### Mistake 4 — Forcing complicated formulas

A pattern such as:

$$
\times2+1
$$

is preferable to a complicated formula if it consistently explains every term.

---

### Mistake 5 — Checking only the last two terms

A rule that works for the final two terms may fail earlier.

Always verify the entire sequence.

---

### Mistake 6 — Ignoring difference patterns

Sometimes the actual pattern is easier to see in the differences.

Example:

$$
2,\ 3,\ 7,\ 16,\ 32
$$

Differences:

$$
1,\ 4,\ 9,\ 16
$$

The original sequence looks complicated, but the differences are simply:

$$
1^2,\ 2^2,\ 3^2,\ 4^2
$$

---

### Mistake 7 — Confusing increasing multiplication with GP

A GP requires:

$$
r=\text{constant}
$$

If:

$$
r=2,3,4,5
$$

it is not GP.

---

### Mistake 8 — Accepting a pattern without verification

Always ask:

> "Does this rule explain every term?"

If not, reject it.

---

# 38. Formula Sheet

## Mixed Multiplication

$$
\boxed{a_n=ka_{n-1}+c}
$$

## Multiplication and Subtraction

$$
\boxed{a_n=ka_{n-1}-c}
$$

## Arithmetic Difference

$$
\boxed{d_n=a_n-a_{n-1}}
$$

## Second Difference

$$
\boxed{\Delta^2a_n=\Delta a_{n+1}-\Delta a_n}
$$

## Geometric Ratio

$$
\boxed{r_n=\frac{a_n}{a_{n-1}}}
$$

## Arithmetic nth Term

$$
\boxed{a_n=a+(n-1)d}
$$

## Geometric nth Term

$$
\boxed{a_n=ar^{n-1}}
$$

## Square Pattern

$$
\boxed{a_n=n^2+c}
$$

## Cube Pattern

$$
\boxed{a_n=n^3+c}
$$

## Fibonacci-Type

$$
\boxed{a_n=a_{n-1}+a_{n-2}}
$$

## Alternating Pattern

$$
\boxed{\text{Analyze odd and even positions separately}}
$$

---

# 39. Quick Revision

> [!summary] One-Minute Revision

## Mixed Pattern Series

A mixed series uses more than one mathematical relationship.

### Fast Solving Order

$$
\boxed{
Difference
\rightarrow
Ratio
\rightarrow
Second\ Difference
\rightarrow
Alternate
\rightarrow
Mixed\ Operation
\rightarrow
Power
\rightarrow
Recursive
}
$$

### Most Important Patterns

#### Multiply and Add

$$
\times2+1
$$

#### Multiply and Subtract

$$
\times3-2
$$

#### Increasing Addition

$$
+2,+4,+6,+8
$$

#### Increasing Multiplication

$$
\times2,\times3,\times4,\times5
$$

#### Alternating

$$
\times2,+3,\times2,+3
$$

#### Square Differences

$$
1,4,9,16,\ldots
$$

#### Cube Differences

$$
1,8,27,64,\ldots
$$

#### Previous Two Terms

$$
a_n=a_{n-1}+a_{n-2}
$$

### Golden Rules

$$
\boxed{\text{Simple pattern first}}
$$

$$
\boxed{\text{Check differences}}
$$

$$
\boxed{\text{Check ratios}}
$$

$$
\boxed{\text{Split alternate terms}}
$$

$$
\boxed{\text{Verify before answering}}
$$

### Golden Memory Trick

**"If one operation fails, move one level deeper: differences → ratios → alternate → mixed → recursive."**

# One-Line Recognition

**When a number series does not follow one simple difference or ratio, look for alternating operations, changing differences or ratios, power-based differences, mixed operations, and recursive relationships.**