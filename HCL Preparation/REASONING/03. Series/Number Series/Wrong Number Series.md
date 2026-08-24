---
type: concept
subject: reasoning
topic: "Wrong Number Series"
parent: "03. Series"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - series
  - wrong-number-series
  - number-series
  - logical-reasoning
  - quantitative-reasoning
  - hcl
wikilinks:
  - "[[03. Series]]"
  - "[[Number Series]]"
  - "[[Missing Number Series]]"
  - "[[Arithmetic Series]]"
  - "[[Geometric Series]]"
  - "[[Mixed Pattern Series]]"
---

# Wrong Number Series

## 1. Core Concept

> [!summary]
> **Wrong Number Series** is a sequence in which one term violates the mathematical pattern followed by the remaining terms. The task is to identify the incorrect term.

Example:

$$
3,\ 6,\ 9,\ 12,\ 16,\ 18
$$

The expected pattern is:

$$
+3
$$

So after $12$:

$$
12+3=15
$$

But the series contains $16$.

Therefore:

$$
\boxed{16}
$$

is the wrong number.

### Core Strategy

$$
\boxed{
Observe
\rightarrow
Find\ Pattern
\rightarrow
Predict
\rightarrow
Compare
\rightarrow
Identify\ Wrong\ Term
}
$$

---

# 2. Basic Meaning

In a normal number series, every term follows a rule.

In a Wrong Number Series, one term is deliberately incorrect.

Suppose:

$$
a_1,a_2,a_3,a_4,a_5
$$

follow a rule:

$$
a_n=f(a_{n-1})
$$

but one term does not satisfy it.

That term is the answer.

### Example

$$
5,\ 10,\ 15,\ 20,\ 26,\ 30
$$

Expected:

$$
+5
$$

Therefore:

$$
20+5=25
$$

But the series contains $26$.

Hence:

$$
\boxed{26}
$$

---

# 3. Main Formula

There is no single formula for all Wrong Number Series.

The most common rules are:

## Arithmetic Pattern

$$
\boxed{a_n=a_{n-1}+d}
$$

## Geometric Pattern

$$
\boxed{a_n=a_{n-1}\times r}
$$

## Increasing Difference

$$
\boxed{\Delta a_n=a_{n+1}-a_n}
$$

## Second Difference

$$
\boxed{\Delta^2a_n=\Delta a_{n+1}-\Delta a_n}
$$

## Fibonacci-Type

$$
\boxed{a_n=a_{n-1}+a_{n-2}}
$$

## Mixed Operation

$$
\boxed{a_n=a_{n-1}\times k+c}
$$

The wrong term is the value that breaks the valid rule.

---

# 4. Important Properties

1. Do not immediately assume the largest number is wrong.
2. Find the mathematical rule first.
3. Check consecutive differences.
4. Check ratios when numbers grow rapidly.
5. Check second differences if the first differences are changing.
6. Check alternating positions.
7. Check squares and cubes.
8. Check prime numbers and multiples.
9. Check mixed operations.
10. Verify the suspected wrong term using both neighboring terms whenever possible.
11. The wrong term may make the **next term** appear wrong, even though the next term itself is correct according to the intended sequence.
12. In some questions, the correct approach is to replace the wrong term and reconstruct the rest of the series.

### Golden Principle

$$
\boxed{\text{Find the rule first; identify the violation second.}}
$$

---

# 5. Basic Examples

## Example 1 — Constant Difference

### Question

Find the wrong number:

$$
4,\ 8,\ 12,\ 16,\ 21,\ 24
$$

### Step 1 — Calculate Differences

$$
+4,+4,+4,+5,+3
$$

The intended pattern is:

$$
+4
$$

Expected sequence:

$$
4,\ 8,\ 12,\ 16,\ 20,\ 24
$$

The given term is $21$.

### Answer

$$
\boxed{21}
$$

---

## Example 2 — Constant Addition

### Question

$$
7,\ 12,\ 17,\ 22,\ 27,\ 33
$$

Expected:

$$
+5
$$

Therefore:

$$
27+5=32
$$

But the given number is $33$.

### Answer

$$
\boxed{33}
$$

---

## Example 3 — Constant Subtraction

### Question

$$
50,\ 45,\ 40,\ 35,\ 29,\ 25
$$

Expected pattern:

$$
-5
$$

After $35$:

$$
35-5=30
$$

But the series contains $29$.

### Answer

$$
\boxed{29}
$$

---

# 6. Medium Examples

## Example 4 — Multiplication Pattern

### Question

$$
2,\ 4,\ 8,\ 16,\ 34,\ 64
$$

Expected:

$$
\times2
$$

Therefore:

$$
16\times2=32
$$

But:

$$
34
$$

is given.

Verify:

$$
32\times2=64
$$

### Answer

$$
\boxed{34}
$$

---

## Example 5 — Division Pattern

### Question

$$
128,\ 64,\ 32,\ 16,\ 9,\ 4
$$

Expected:

$$
\div2
$$

After $16$:

$$
16\div2=8
$$

But the series contains $9$.

Also:

$$
8\div2=4
$$

### Answer

$$
\boxed{9}
$$

---

## Example 6 — Increasing Difference

### Question

$$
2,\ 5,\ 9,\ 14,\ 20,\ 27,\ 35
$$

Differences:

$$
+3,+4,+5,+6,+7,+8
$$

Every difference follows the pattern.

Therefore, there is:

$$
\boxed{\text{No wrong number}}
$$

> [!important]
> Not every sequence necessarily contains a wrong number. If the question guarantees one wrong number, recheck your calculations or the exact sequence.

---

## Example 7 — Wrong Term in an Increasing-Difference Series

### Question

$$
2,\ 5,\ 9,\ 14,\ 20,\ 28,\ 35
$$

Expected differences:

$$
+3,+4,+5,+6,+7,+8
$$

Expected sequence:

$$
2,\ 5,\ 9,\ 14,\ 20,\ 27,\ 35
$$

But the given term is:

$$
28
$$

### Answer

$$
\boxed{28}
$$

---

# 7. Second Difference Pattern

## Example 8

### Question

$$
3,\ 7,\ 13,\ 21,\ 32,\ 43
$$

Calculate first differences:

$$
+4,+6,+8,+11,+11
$$

Expected differences should be:

$$
+4,+6,+8,+10,+12
$$

Expected sequence:

$$
3,\ 7,\ 13,\ 21,\ 31,\ 43
$$

Therefore:

$$
\boxed{32}
$$

is wrong.

### Verification

$$
21+10=31
$$

$$
31+12=43
$$

---

# 8. Square Number Pattern

## Example 9

### Question

$$
1,\ 4,\ 9,\ 16,\ 24,\ 36
$$

Expected:

$$
1^2,\ 2^2,\ 3^2,\ 4^2,\ 5^2,\ 6^2
$$

Therefore:

$$
5^2=25
$$

But the series contains $24$.

### Answer

$$
\boxed{24}
$$

---

# 9. Cube Number Pattern

## Example 10

### Question

$$
1,\ 8,\ 27,\ 64,\ 100,\ 216
$$

Expected:

$$
1^3,\ 2^3,\ 3^3,\ 4^3,\ 5^3,\ 6^3
$$

Expected fifth term:

$$
5^3=125
$$

But:

$$
100
$$

is given.

### Answer

$$
\boxed{100}
$$

---

# 10. Prime Number Pattern

## Example 11

### Question

$$
2,\ 3,\ 5,\ 7,\ 11,\ 15,\ 17
$$

These should be consecutive prime numbers:

$$
2,\ 3,\ 5,\ 7,\ 11,\ 13,\ 17
$$

But:

$$
15
$$

is not prime.

### Answer

$$
\boxed{15}
$$

---

# 11. Multiples Pattern

## Example 12

### Question

$$
6,\ 12,\ 18,\ 24,\ 31,\ 36
$$

Expected multiples of $6$:

$$
6,\ 12,\ 18,\ 24,\ 30,\ 36
$$

The incorrect term is:

$$
\boxed{31}
$$

---

# 12. Alternate Pattern

Sometimes the entire series follows two separate patterns.

## Example 13

### Question

$$
2,\ 5,\ 4,\ 10,\ 6,\ 15,\ 9,\ 20
$$

Separate odd and even positions.

### Odd Positions

$$
2,\ 4,\ 6,\ 9
$$

Expected:

$$
2,\ 4,\ 6,\ 8
$$

Therefore:

$$
\boxed{9}
$$

is wrong.

### Even Positions

$$
5,\ 10,\ 15,\ 20
$$

Pattern:

$$
+5
$$

This confirms the answer.

---

# 13. Alternating Operation Pattern

## Example 14

### Question

$$
3,\ 6,\ 8,\ 16,\ 18,\ 35,\ 37
$$

Expected operations:

$$
\times2,\ +2,\ \times2,\ +2,\ \times2,\ +2
$$

Check:

$$
3\times2=6
$$

$$
6+2=8
$$

$$
8\times2=16
$$

$$
16+2=18
$$

Expected:

$$
18\times2=36
$$

But the given value is:

$$
35
$$

Then:

$$
35+2=37
$$

### Answer

$$
\boxed{35}
$$

---

# 14. Fibonacci-Type Pattern

## Example 15

### Question

$$
1,\ 1,\ 2,\ 3,\ 5,\ 9,\ 13
$$

Expected:

$$
1+1=2
$$

$$
1+2=3
$$

$$
2+3=5
$$

$$
3+5=8
$$

$$
5+8=13
$$

But the series contains:

$$
9
$$

instead of $8$.

### Answer

$$
\boxed{9}
$$

---

# 15. Increasing Multiplication Pattern

## Example 16

### Question

$$
2,\ 4,\ 12,\ 48,\ 245,\ 1440
$$

Expected:

$$
2\times2=4
$$

$$
4\times3=12
$$

$$
12\times4=48
$$

$$
48\times5=240
$$

$$
240\times6=1440
$$

But the series contains:

$$
245
$$

### Answer

$$
\boxed{245}
$$

---

# 16. Mixed Operation Pattern

## Example 17

### Question

$$
4,\ 9,\ 19,\ 39,\ 80,\ 159
$$

Expected:

$$
\times2+1
$$

Check:

$$
4\times2+1=9
$$

$$
9\times2+1=19
$$

$$
19\times2+1=39
$$

Expected:

$$
39\times2+1=79
$$

But given:

$$
80
$$

Then:

$$
80\times2-1=159
$$

The consistent intended pattern is broken at $80$.

### Answer

$$
\boxed{80}
$$

---

# 17. Square + Constant Pattern

## Example 18

### Question

$$
2,\ 5,\ 10,\ 17,\ 27,\ 37
$$

Expected:

$$
n^2+1
$$

Terms:

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

$$
6^2+1=37
$$

But the given fifth term is $27$.

### Answer

$$
\boxed{27}
$$

---

# 18. Cube + Constant Pattern

## Example 19

### Question

$$
2,\ 9,\ 28,\ 65,\ 126,\ 216
$$

Expected:

$$
n^3+1
$$

Check:

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

$$
5^3+1=126
$$

But:

$$
6^3+1=217
$$

Given:

$$
216
$$

### Answer

$$
\boxed{216}
$$

---

# 19. Digit-Based Pattern

## Example 20 — Digit Sum

### Question

$$
12,\ 21,\ 30,\ 39,\ 47,\ 57
$$

Check digit sums:

$$
1+2=3
$$

$$
2+1=3
$$

$$
3+0=3
$$

$$
3+9=12
$$

This does not form a strong digit-sum pattern.

> [!warning]
> Do not force digit operations merely because they are possible.

Instead, check the ordinary differences:

$$
+9,+9,+9,+8,+10
$$

The expected pattern is:

$$
+9
$$

Expected:

$$
12,21,30,39,48,57
$$

Therefore:

$$
\boxed{47}
$$

---

# 20. Difference Table Method

For difficult Wrong Number Series, create a difference table.

### Example

$$
3,\ 8,\ 15,\ 24,\ 35,\ 48
$$

First differences:

$$
5,\ 7,\ 9,\ 11,\ 13
$$

Second differences:

$$
2,\ 2,\ 2,\ 2
$$

This is a valid series.

If the sequence were:

$$
3,\ 8,\ 15,\ 25,\ 35,\ 48
$$

First differences:

$$
5,\ 7,\ 10,\ 10,\ 13
$$

The intended pattern is:

$$
+5,+7,+9,+11,+13
$$

Expected sequence:

$$
3,\ 8,\ 15,\ 24,\ 35,\ 48
$$

Therefore:

$$
\boxed{25}
$$

---

# 21. How to Solve Any Wrong Number Series

## Step 1 — Calculate Differences

Write:

$$
d_1=a_2-a_1
$$

$$
d_2=a_3-a_2
$$

Continue for the complete sequence.

If the differences follow a clear rule, identify the violation.

---

## Step 2 — Check Ratios

If differences do not work, check:

$$
\frac{a_2}{a_1},\quad
\frac{a_3}{a_2},\quad
\frac{a_4}{a_3}
$$

Look for:

$$
\times2,\times3,\div2,\div3
$$

---

## Step 3 — Check Second Differences

If the first differences change regularly:

$$
\Delta^2 a_n
$$

may be constant.

---

## Step 4 — Check Powers

Look for:

$$
n^2
$$

or:

$$
n^3
$$

or:

$$
2^n,\ 3^n
$$

---

## Step 5 — Check Alternating Terms

Separate:

$$
a_1,a_3,a_5,\ldots
$$

from:

$$
a_2,a_4,a_6,\ldots
$$

---

## Step 6 — Check Mixed Operations

Test:

$$
\times k+c
$$

or:

$$
\times k-c
$$

---

## Step 7 — Check Number Properties

Look for:

- Prime numbers
- Multiples
- Factors
- Odd/even numbers
- Perfect squares
- Perfect cubes

---

## Step 8 — Verify the Suspected Term

Once you identify a candidate, replace it with the expected value.

Then check whether the complete sequence becomes consistent.

---

# 22. Pattern Recognition Tricks

## Pattern 1 — Constant Difference

> [!important]
> If differences are mostly equal, the outlier is usually the term creating the abnormal difference.

Example:

$$
5,10,15,21,25
$$

Expected:

$$
+5
$$

Therefore:

$$
\boxed{21}
$$

---

## Pattern 2 — Constant Ratio

> [!important]
> For rapidly growing or shrinking values, check ratios.

Example:

$$
2,6,18,55,162
$$

Expected:

$$
\times3
$$

The expected fourth term is:

$$
18\times3=54
$$

Therefore:

$$
\boxed{55}
$$

---

## Pattern 3 — Increasing Difference

> [!important]
> If differences are:

$$
+3,+4,+5,+7,+7
$$

look for the expected sequence:

$$
+3,+4,+5,+6,+7
$$

This may reveal the wrong term.

---

## Pattern 4 — Second Difference

> [!important]
> If the first differences are not constant but their differences are constant, use second differences.

---

## Pattern 5 — Alternating Series

> [!important]
> If the complete sequence looks irregular, split odd and even positions.

---

## Pattern 6 — Power Series

> [!important]
> If values resemble:

$$
1,4,9,16,25
$$

check squares.

If they resemble:

$$
1,8,27,64,125
$$

check cubes.

---

## Pattern 7 — Fibonacci

> [!important]
> Check:

$$
a_n=a_{n-1}+a_{n-2}
$$

when each term seems related to the previous two.

---

## Pattern 8 — Increasing Multiplier

> [!important]
> For rapidly increasing values, test:

$$
\times2,\times3,\times4,\times5
$$

---

## Pattern 9 — Mixed Operation

> [!important]
> Test repeated operations such as:

$$
\times2+1
$$

$$
\times3-2
$$

---

## Pattern 10 — Position-Based Pattern

> [!important]
> Sometimes the terms follow a formula based on their position:

$$
a_n=n^2+1
$$

or:

$$
a_n=n^3-2
$$

Compare each term against its position.

---

# 23. Shortcuts

> [!tip]
> **Shortcut 1 — Start with differences**

For most placement-level series, differences reveal the pattern quickly.

---

> [!tip]
> **Shortcut 2 — Check the suspicious jump**

If the series is:

$$
10,\ 15,\ 20,\ 25,\ 32,\ 35
$$

the jump:

$$
25\rightarrow32
$$

is immediately suspicious.

---

> [!tip]
> **Shortcut 3 — Verify from both directions**

If you suspect $32$ is wrong:

Expected:

$$
25+5=30
$$

and:

$$
30+5=35
$$

Both sides confirm:

$$
\boxed{32}
$$

is wrong.

---

> [!tip]
> **Shortcut 4 — Use position numbers**

For a power-based series, write:

$$
1,2,3,4,5,\ldots
$$

under the terms.

Then compare each term with:

$$
n^2,\ n^3,\ 2^n
$$

---

> [!tip]
> **Shortcut 5 — Split before overthinking**

If the sequence alternates, separate odd and even positions before testing complicated formulas.

---

> [!tip]
> **Shortcut 6 — Reconstruct the expected series**

Instead of asking:

> "Which number looks wrong?"

ask:

> "What should the sequence be?"

Then compare the given series against the reconstructed sequence.

---

# 24. Common Exam Patterns

> [!important] Must Master

### Basic Patterns

1. Constant addition
2. Constant subtraction
3. Constant multiplication
4. Constant division

### Difference Patterns

5. Increasing difference
6. Decreasing difference
7. Second difference
8. Third difference

### Power Patterns

9. Squares
10. Cubes
11. Powers of 2
12. Powers of 3
13. Square + constant
14. Cube + constant

### Number Properties

15. Prime numbers
16. Composite numbers
17. Multiples
18. Factors
19. Odd/even
20. Divisibility

### Alternating Patterns

21. Odd-position series
22. Even-position series
23. Alternating addition/subtraction
24. Alternating multiplication/division
25. Alternating mixed operations

### Recursive Patterns

26. Fibonacci
27. Previous-term relationship
28. Previous-two-term relationship

### Mixed Patterns

29. Multiplication + addition
30. Multiplication + subtraction
31. Division + addition
32. Division + subtraction
33. Increasing multiplier
34. Increasing addition
35. Increasing subtraction

### Advanced Patterns

36. Digit-based patterns
37. Position-based formulas
38. Multi-level differences
39. Combined transformations
40. Recursive mathematical patterns

---

# 25. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Choosing the visually largest number

The wrong term is determined by the pattern, not its size.

---

### Mistake 2 — Checking only one difference

Calculate all relevant differences.

One unusual jump may be caused by the preceding wrong term.

---

### Mistake 3 — Blaming the next number

Suppose:

$$
5,\ 10,\ 15,\ 21,\ 25
$$

The abnormal difference is:

$$
15\rightarrow21
$$

and:

$$
21\rightarrow25
$$

But the actual wrong term is $21$.

Always identify the term causing the violation.

---

### Mistake 4 — Ignoring alternating patterns

A sequence may contain two valid interleaved series.

---

### Mistake 5 — Forcing a complicated rule

Prefer:

$$
+5
$$

over an artificial multi-step formula when the simple pattern explains the sequence.

---

### Mistake 6 — Ignoring squares and cubes

Some sequences are easiest to recognize through powers.

---

### Mistake 7 — Not correcting the wrong term

After identifying the wrong term, calculate its expected value.

This is a strong verification method.

---

### Mistake 8 — Failing to verify

A suspected answer is not enough.

Replace it and check the entire sequence.

---

# 26. Formula Sheet

## First Difference

$$
\boxed{\Delta a_n=a_{n+1}-a_n}
$$

## Second Difference

$$
\boxed{\Delta^2a_n=\Delta a_{n+1}-\Delta a_n}
$$

## Arithmetic Pattern

$$
\boxed{a_n=a_{n-1}+d}
$$

## Geometric Pattern

$$
\boxed{a_n=a_{n-1}r}
$$

## Square Pattern

$$
\boxed{a_n=n^2}
$$

## Cube Pattern

$$
\boxed{a_n=n^3}
$$

## Fibonacci Pattern

$$
\boxed{a_n=a_{n-1}+a_{n-2}}
$$

## Mixed Operation

$$
\boxed{a_n=a_{n-1}\times k+c}
$$

## Increasing Multiplier

$$
\boxed{a_n=a_{n-1}\times n}
$$

## Wrong Term Principle

$$
\boxed{\text{Given Term}\neq\text{Expected Term}}
$$

---

# 27. Quick Revision

> [!summary] One-Minute Revision

## Wrong Number Series

Find the one term that violates the hidden series rule.

### Fast Solving Order

$$
\boxed{
Difference
\rightarrow
Ratio
\rightarrow
Second\ Difference
\rightarrow
Powers
\rightarrow
Alternating
\rightarrow
Mixed
\rightarrow
Recursive
}
$$

### Ask These Questions

1. Are the differences constant?
2. Are the ratios constant?
3. Are the differences increasing or decreasing?
4. Is the second difference constant?
5. Are the terms squares?
6. Are the terms cubes?
7. Are the terms prime or multiples?
8. Is there an alternating pattern?
9. Is there a mixed operation?
10. Does each term depend on previous terms?
11. Can I replace one term and make the whole series consistent?

### Golden Rules

$$
\boxed{\text{Find the rule before finding the wrong term}}
$$

$$
\boxed{\text{Reconstruct the expected value}}
$$

$$
\boxed{\text{Verify the entire sequence}}
$$

$$
\boxed{\text{Do not force a pattern}}
$$

### Golden Memory Trick

**"Find what the number should be, then compare it with what is given."**

# One-Line Recognition

**When a series contains one incorrect term, first identify the underlying pattern, calculate the expected term, and select the given number that violates that pattern.**