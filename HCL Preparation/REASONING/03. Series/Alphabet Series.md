---
type: concept
subject: reasoning
topic: "Alphabet Series"
parent: "03. Series"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - series
  - alphabet-series
  - letter-series
  - alphabet-reasoning
  - pattern-recognition
  - logical-reasoning
  - hcl
wikilinks:
  - "[[03. Series]]"
  - "[[Number Series]]"
  - "[[Letter Series]]"
  - "[[Alphanumeric Series]]"
  - "[[Mixed Series]]"
  - "[[Coding Decoding]]"
---

# Alphabet Series

## 1. Core Concept

> [!summary]
> An **Alphabet Series** is a sequence of letters arranged according to a hidden pattern. The pattern may involve forward movement, backward movement, alternate letters, fixed gaps, increasing gaps, repeated blocks, reverse order, or multiple interleaved sequences.

Example:

$$
A,\ C,\ E,\ G,\ I,\ ?
$$

Convert letters into positions:

$$
A=1,\ C=3,\ E=5,\ G=7,\ I=9
$$

The pattern is:

$$
+2
$$

Therefore:

$$
9+2=11
$$

and:

$$
11=K
$$

Answer:

$$
\boxed{K}
$$

### Core Intuition

Think:

> **"Convert letters into positions, find the numerical pattern, then convert back to letters."**

The fundamental mapping is:

$$
\boxed{A=1,\ B=2,\ C=3,\ldots,Z=26}
$$

---

# 2. Basic Meaning

Alphabet Series questions ask you to identify the next, previous, missing, or wrong letter according to a specific pattern.

The pattern may be:

- Forward movement
- Backward movement
- Alternate letters
- Fixed gaps
- Increasing gaps
- Decreasing gaps
- Reverse alphabet
- Odd-position letters
- Even-position letters
- Alternating forward/backward movement
- Multiple independent sequences
- Letter-pair patterns
- Position-based patterns
- Mixed alphabet and number relationships

### Example

$$
B,\ E,\ H,\ K,\ ?
$$

Positions:

$$
2,\ 5,\ 8,\ 11
$$

Pattern:

$$
+3
$$

Next:

$$
11+3=14
$$

Position $14$ is:

$$
N
$$

Therefore:

$$
\boxed{N}
$$

---

# 3. Main Formula

## 3.1 Alphabet Position

For English uppercase letters:

$$
\boxed{A=1,\ B=2,\ C=3,\ldots,Z=26}
$$

---

## 3.2 Reverse Alphabet Position

Sometimes the alphabet is counted from the right.

$$
\boxed{A=26,\ B=25,\ldots,Z=1}
$$

The reverse position of a letter with normal position $p$ is:

$$
\boxed{27-p}
$$

### Example

For $C$:

$$
p=3
$$

Reverse position:

$$
27-3=24
$$

Therefore:

$$
\boxed{C\rightarrow24}
$$

---

## 3.3 Forward Movement

If a letter moves forward by $k$ positions:

$$
\boxed{p_{\text{next}}=p+k}
$$

---

## 3.4 Backward Movement

If a letter moves backward by $k$ positions:

$$
\boxed{p_{\text{next}}=p-k}
$$

---

## 3.5 Cyclic Alphabet

If the sequence goes beyond $Z$, wrap around to $A$.

Using zero-based positions:

$$
\boxed{p_{\text{next}}=(p+k-1)\bmod26+1}
$$

This is useful for patterns such as:

$$
Y,\ A,\ C,\ E,\ldots
$$

---

# 4. Important Properties

1. Every letter has a numerical position.
2. Alphabet series are often easier when converted into numbers.
3. Forward movement means increasing positions.
4. Backward movement means decreasing positions.
5. A fixed gap means the same number of letters is skipped each time.
6. Increasing gaps require checking the differences between positions.
7. Odd and even positions may form separate sequences.
8. The sequence may wrap around after $Z$.
9. The reverse alphabet may be used.
10. Letter pairs may follow independent patterns.
11. The first letter and second letter may follow different rules.
12. Some series use alternating forward and backward movement.
13. Some patterns are based on vowel/consonant classification.
14. Some patterns use alphabet positions such as squares, multiples, or primes.
15. Always verify the pattern across multiple transitions.

---

# 5. Alphabet Position Table

| Letter | Position | Reverse Position |
|---|---:|---:|
| A | 1 | 26 |
| B | 2 | 25 |
| C | 3 | 24 |
| D | 4 | 23 |
| E | 5 | 22 |
| F | 6 | 21 |
| G | 7 | 20 |
| H | 8 | 19 |
| I | 9 | 18 |
| J | 10 | 17 |
| K | 11 | 16 |
| L | 12 | 15 |
| M | 13 | 14 |
| N | 14 | 13 |
| O | 15 | 12 |
| P | 16 | 11 |
| Q | 17 | 10 |
| R | 18 | 9 |
| S | 19 | 8 |
| T | 20 | 7 |
| U | 21 | 6 |
| V | 22 | 5 |
| W | 23 | 4 |
| X | 24 | 3 |
| Y | 25 | 2 |
| Z | 26 | 1 |

> [!tip]
> Memorize at least the anchor positions:
>
> $$A=1,\ E=5,\ J=10,\ M=13,\ N=14,\ T=20,\ Z=26$$
>
> These make mental calculation much faster.

---

# 6. Basic Examples

## Example 1 — Consecutive Letters

### Question

Find the next letter:

$$
A,\ B,\ C,\ D,\ ?
$$

Positions:

$$
1,\ 2,\ 3,\ 4
$$

Pattern:

$$
+1
$$

Therefore:

$$
\boxed{E}
$$

---

## Example 2 — Every Second Letter

### Question

$$
A,\ C,\ E,\ G,\ ?
$$

Positions:

$$
1,\ 3,\ 5,\ 7
$$

Pattern:

$$
+2
$$

Next position:

$$
7+2=9
$$

Position $9$ is:

$$
\boxed{I}
$$

---

## Example 3 — Every Third Letter

### Question

$$
B,\ E,\ H,\ K,\ ?
$$

Positions:

$$
2,\ 5,\ 8,\ 11
$$

Pattern:

$$
+3
$$

Next:

$$
11+3=14
$$

Therefore:

$$
\boxed{N}
$$

---

# 7. Backward Alphabet Series

## Example 4

### Question

$$
Z,\ Y,\ X,\ W,\ ?
$$

Positions:

$$
26,\ 25,\ 24,\ 23
$$

Pattern:

$$
-1
$$

Therefore:

$$
\boxed{V}
$$

---

## Example 5

### Question

$$
Z,\ X,\ V,\ T,\ ?
$$

Positions:

$$
26,\ 24,\ 22,\ 20
$$

Pattern:

$$
-2
$$

Next:

$$
20-2=18
$$

Position $18$ is:

$$
\boxed{R}
$$

---

# 8. Fixed-Gap Alphabet Series

The number of skipped letters is important.

## Example 6

### Question

$$
A,\ D,\ G,\ J,\ ?
$$

Positions:

$$
1,\ 4,\ 7,\ 10
$$

Difference:

$$
+3
$$

Therefore:

$$
10+3=13
$$

### Answer

$$
\boxed{M}
$$

### Gap Interpretation

Between:

$$
A\rightarrow D
$$

letters skipped:

$$
B,C
$$

So there are **2 skipped letters**.

> [!important]
> Be careful:
>
> **Movement by 3 positions = 2 letters skipped.**

---

# 9. Increasing Gap Pattern

## Example 7

### Question

$$
A,\ B,\ D,\ G,\ K,\ ?
$$

Positions:

$$
1,\ 2,\ 4,\ 7,\ 11
$$

Differences:

$$
+1,+2,+3,+4
$$

Next difference:

$$
+5
$$

Therefore:

$$
11+5=16
$$

Position $16$ is:

$$
\boxed{P}
$$

---

# 10. Decreasing Gap Pattern

## Example 8

### Question

$$
Z,\ Y,\ W,\ T,\ P,\ ?
$$

Positions:

$$
26,\ 25,\ 23,\ 20,\ 16
$$

Differences:

$$
-1,-2,-3,-4
$$

Next:

$$
-5
$$

Therefore:

$$
16-5=11
$$

Position $11$ is:

$$
\boxed{K}
$$

---

# 11. Alternate Alphabet Series

## Example 9

### Question

$$
A,\ B,\ C,\ D,\ E,\ F,\ ?
$$

This is simple consecutive movement.

But consider:

$$
A,\ C,\ B,\ D,\ C,\ E,\ ?
$$

Separate odd and even positions.

### Odd Positions

$$
A,\ B,\ C,\ ?
$$

Therefore:

$$
D
$$

### Even Positions

$$
C,\ D,\ E
$$

Therefore:

$$
F
$$

Hence the next term:

$$
\boxed{D}
$$

---

# 12. Alternating Forward and Backward Movement

## Example 10

### Question

$$
A,\ D,\ C,\ F,\ E,\ H,\ ?
$$

Positions:

$$
1,\ 4,\ 3,\ 6,\ 5,\ 8
$$

Operations:

$$
+3,-1,+3,-1,+3
$$

Therefore:

$$
8-1=7
$$

Position $7$:

$$
\boxed{G}
$$

---

# 13. Alternating Increasing Movement

## Example 11

### Question

$$
A,\ C,\ F,\ J,\ O,\ ?
$$

Positions:

$$
1,\ 3,\ 6,\ 10,\ 15
$$

Differences:

$$
+2,+3,+4,+5
$$

Next:

$$
+6
$$

Therefore:

$$
15+6=21
$$

Position $21$ is:

$$
\boxed{U}
$$

---

# 14. Reverse Alphabet with Increasing Gaps

## Example 12

### Question

$$
Z,\ X,\ U,\ Q,\ L,\ ?
$$

Positions:

$$
26,\ 24,\ 21,\ 17,\ 12
$$

Differences:

$$
-2,-3,-4,-5
$$

Next:

$$
-6
$$

Therefore:

$$
12-6=6
$$

Position $6$:

$$
\boxed{F}
$$

---

# 15. Odd-Position and Even-Position Patterns

This is one of the most important advanced patterns.

## Example 13

### Question

$$
A,\ Z,\ C,\ X,\ E,\ V,\ ?
$$

Separate the positions.

### Odd Positions

$$
A,\ C,\ E,\ ?
$$

Pattern:

$$
+2
$$

Therefore:

$$
G
$$

### Even Positions

$$
Z,\ X,\ V
$$

Pattern:

$$
-2
$$

Therefore:

$$
T
$$

The next term is at an odd position.

### Answer

$$
\boxed{G}
$$

---

# 16. Two Interleaved Series

## Example 14

### Question

$$
B,\ D,\ E,\ G,\ H,\ J,\ ?
$$

Odd positions:

$$
B,\ E,\ H,\ ?
$$

Pattern:

$$
+3
$$

Therefore:

$$
K
$$

Even positions:

$$
D,\ G,\ J
$$

Pattern:

$$
+3
$$

The next term belongs to the odd sequence.

### Answer

$$
\boxed{K}
$$

---

# 17. Position-Based Alphabet Series

Alphabet positions may follow a numerical sequence.

## Example 15

### Question

$$
A,\ D,\ I,\ P,\ ?
$$

Positions:

$$
1,\ 4,\ 9,\ 16
$$

These are:

$$
1^2,\ 2^2,\ 3^2,\ 4^2
$$

Next:

$$
5^2=25
$$

Position $25$:

$$
\boxed{Y}
$$

---

# 18. Cube-Based Alphabet Series

## Example 16

### Question

$$
A,\ H,\ Q,\ ?
$$

Positions:

$$
1,\ 8,\ 17
$$

This is not:

$$
1^3,\ 2^3,\ 3^3
$$

because:

$$
3^3=27
$$

So do not force the cube pattern.

> [!warning]
> Always convert the letters to positions and verify the numerical sequence before deciding the rule.

---

# 19. Prime-Position Alphabet Series

## Example 17

### Question

$$
B,\ C,\ E,\ G,\ K,\ M,\ ?
$$

Positions:

$$
2,\ 3,\ 5,\ 7,\ 11,\ 13
$$

These are prime numbers.

Next prime:

$$
17
$$

Position $17$ is:

$$
\boxed{Q}
$$

---

# 20. Odd-Position Alphabet Series

## Example 18

### Question

$$
A,\ C,\ E,\ G,\ I,\ ?
$$

These are letters at odd positions:

$$
1,\ 3,\ 5,\ 7,\ 9
$$

Next:

$$
11
$$

Therefore:

$$
\boxed{K}
$$

---

# 21. Even-Position Alphabet Series

## Example 19

### Question

$$
B,\ D,\ F,\ H,\ ?
$$

Positions:

$$
2,\ 4,\ 6,\ 8
$$

Next:

$$
10
$$

Therefore:

$$
\boxed{J}
$$

---

# 22. Vowel-Based Series

Some questions may use letter categories instead of pure positions.

The main English vowels are:

$$
A,E,I,O,U
$$

## Example 20

### Question

$$
A,\ E,\ I,\ O,\ ?
$$

The pattern is the sequence of vowels.

Therefore:

$$
\boxed{U}
$$

> [!important]
> Vowel/consonant patterns should be considered when numerical alphabet positions do not produce a useful rule.

---

# 23. Consonant Series

## Example 21

Consider:

$$
B,\ C,\ D,\ F,\ G,\ ?
$$

These are consecutive consonants, skipping vowels.

After:

$$
B,C,D,F,G
$$

the next consonant is:

$$
H
$$

### Answer

$$
\boxed{H}
$$

---

# 24. Mirror Alphabet Pattern

The alphabet may move simultaneously from both ends.

## Example 22

### Question

$$
A,\ Z,\ B,\ Y,\ C,\ X,\ ?
$$

Odd positions:

$$
A,\ B,\ C,\ ?
$$

Next:

$$
D
$$

Even positions:

$$
Z,\ Y,\ X
$$

Next:

$$
W
$$

Therefore the next term:

$$
\boxed{D}
$$

### Pattern

$$
A,Z,B,Y,C,X,D,W,\ldots
$$

---

# 25. Pair-Based Alphabet Series

## Example 23

### Question

$$
AB,\ DE,\ GH,\ JK,\ ?
$$

Each pair moves by $3$ positions.

Pairs:

$$
AB
$$

$$
DE
$$

$$
GH
$$

$$
JK
$$

Next:

$$
MN
$$

### Answer

$$
\boxed{MN}
$$

---

# 26. Reverse Pair Series

## Example 24

### Question

$$
ZY,\ XW,\ VU,\ TS,\ ?
$$

Pairs move backward.

Positions:

$$
26,25
$$

then:

$$
24,23
$$

then:

$$
22,21
$$

then:

$$
20,19
$$

Next:

$$
18,17
$$

Therefore:

$$
\boxed{RQ}
$$

---

# 27. Letter Gap Recognition

Consider:

$$
A,\ F,\ K,\ P,\ U
$$

Positions:

$$
1,\ 6,\ 11,\ 16,\ 21
$$

Difference:

$$
+5
$$

Each transition skips:

$$
4
$$

letters.

### Important Distinction

Movement:

$$
+5
$$

Skipped letters:

$$
4
$$

> [!warning]
> Do not confuse "move by 5 positions" with "skip 5 letters."

---

# 28. Wrap-Around Series

Alphabet series can continue after $Z$.

## Example 25

### Question

$$
X,\ Z,\ B,\ D,\ ?
$$

Positions:

$$
24,\ 26,\ 2,\ 4
$$

The movement is:

$$
+2
$$

After $Z$, return to $A$.

Therefore:

$$
D+2=F
$$

### Answer

$$
\boxed{F}
$$

### Sequence

$$
X,\ Z,\ B,\ D,\ F
$$

---

# 29. Wrap-Around with Larger Steps

## Example 26

### Question

$$
Y,\ C,\ G,\ K,\ ?
$$

Positions:

$$
25,\ 3,\ 7,\ 11
$$

Each step is:

$$
+4
$$

because:

$$
25+4=29
$$

Wrap:

$$
29-26=3
$$

Therefore:

$$
11+4=15
$$

Position $15$:

$$
\boxed{O}
$$

---

# 30. Reverse Wrap-Around

## Example 27

### Question

$$
C,\ A,\ Y,\ W,\ ?
$$

Positions:

$$
3,\ 1,\ 25,\ 23
$$

Each step:

$$
-2
$$

After $A$, wrap to $Z$:

$$
1-2=-1
$$

Convert cyclically to:

$$
25
$$

Therefore:

$$
23-2=21
$$

### Answer

$$
\boxed{U}
$$

---

# 31. Alphabet Series with Increasing Gaps

## Example 28

### Question

$$
A,\ C,\ F,\ J,\ O,\ ?
$$

Positions:

$$
1,\ 3,\ 6,\ 10,\ 15
$$

Differences:

$$
+2,+3,+4,+5
$$

Next:

$$
+6
$$

Therefore:

$$
15+6=21
$$

### Answer

$$
\boxed{U}
$$

---

# 32. Alphabet Series with Decreasing Gaps

## Example 29

### Question

$$
Z,\ X,\ U,\ Q,\ L,\ ?
$$

Positions:

$$
26,\ 24,\ 21,\ 17,\ 12
$$

Differences:

$$
-2,-3,-4,-5
$$

Next:

$$
-6
$$

Therefore:

$$
12-6=6
$$

### Answer

$$
\boxed{F}
$$

---

# 33. Alternating Gap Pattern

## Example 30

### Question

$$
A,\ D,\ F,\ I,\ K,\ N,\ ?
$$

Positions:

$$
1,\ 4,\ 6,\ 9,\ 11,\ 14
$$

Differences:

$$
+3,+2,+3,+2,+3
$$

Next:

$$
+2
$$

Therefore:

$$
14+2=16
$$

### Answer

$$
\boxed{P}
$$

---

# 34. Alternating Large and Small Movement

## Example 31

### Question

$$
B,\ G,\ E,\ J,\ H,\ M,\ ?
$$

Positions:

$$
2,\ 7,\ 5,\ 10,\ 8,\ 13
$$

Pattern:

$$
+5,-2,+5,-2,+5
$$

Next:

$$
-2
$$

Therefore:

$$
13-2=11
$$

### Answer

$$
\boxed{K}
$$

---

# 35. Alphabetical Order with Reverse Movement

## Example 32

### Question

$$
A,\ D,\ C,\ F,\ E,\ H,\ ?
$$

Pattern:

$$
+3,-1,+3,-1,+3
$$

Therefore:

$$
H-1=G
$$

### Answer

$$
\boxed{G}
$$

---

# 36. Letter Pair Position Pattern

## Example 33

### Question

$$
AC,\ DF,\ GI,\ JL,\ ?
$$

First letters:

$$
A,D,G,J
$$

Positions:

$$
1,4,7,10
$$

Pattern:

$$
+3
$$

Second letters:

$$
C,F,I,L
$$

Positions:

$$
3,6,9,12
$$

Pattern:

$$
+3
$$

Next pair:

First letter:

$$
J+3=M
$$

Second letter:

$$
L+3=O
$$

### Answer

$$
\boxed{MO}
$$

---

# 37. Letter Pair with Different Patterns

## Example 34

### Question

$$
AZ,\ BY,\ CX,\ DW,\ ?
$$

First letters:

$$
A,B,C,D
$$

Pattern:

$$
+1
$$

Second letters:

$$
Z,Y,X,W
$$

Pattern:

$$
-1
$$

Next:

$$
E,V
$$

### Answer

$$
\boxed{EV}
$$

---

# 38. Alphabetical Position Arithmetic

Some advanced series use arithmetic directly on letter positions.

## Example 35

### Question

$$
B,\ E,\ J,\ Q,\ ?
$$

Positions:

$$
2,\ 5,\ 10,\ 17
$$

Differences:

$$
+3,+5,+7
$$

Next:

$$
+9
$$

Therefore:

$$
17+9=26
$$

### Answer

$$
\boxed{Z}
$$

### Pattern

The differences are consecutive odd numbers:

$$
3,5,7,9
$$

---

# 39. Square-Based Letter Positions

## Example 36

### Question

$$
A,\ D,\ I,\ P,\ Y,\ ?
$$

Positions:

$$
1,\ 4,\ 9,\ 16,\ 25
$$

These are:

$$
1^2,\ 2^2,\ 3^2,\ 4^2,\ 5^2
$$

The next square is:

$$
6^2=36
$$

But the alphabet has only $26$ positions.

Therefore, a simple non-cyclic square-position continuation is impossible.

> [!warning]
> This is a good reminder that not every numerical pattern can be directly mapped into $A-Z$ without considering the range $1$ to $26$.

---

# 40. Advanced Pattern — Prime Alphabet Positions

## Example 37

### Question

$$
B,\ C,\ E,\ G,\ K,\ M,\ Q,\ ?
$$

Positions:

$$
2,\ 3,\ 5,\ 7,\ 11,\ 13,\ 17
$$

These are consecutive prime positions.

Next prime:

$$
19
$$

Position $19$:

$$
\boxed{S}
$$

---

# 41. Advanced Pattern — Composite Positions

Composite numbers beginning from $4$ are:

$$
4,\ 6,\ 8,\ 9,\ 10,\ 12,\ 14,\ldots
$$

Therefore:

$$
D,\ F,\ H,\ I,\ J,\ L,\ N,\ldots
$$

can form a number-property-based alphabet series.

> [!important]
> When ordinary gaps fail, check whether the alphabet positions themselves represent a known number sequence.

---

# 42. Advanced Pattern — Alphabet Position Differences

## Example 38

### Question

$$
C,\ F,\ K,\ R,\ ?
$$

Positions:

$$
3,\ 6,\ 11,\ 18
$$

Differences:

$$
+3,+5,+7
$$

Next:

$$
+9
$$

Therefore:

$$
18+9=27
$$

Since alphabet positions stop at $26$, a normal non-cyclic answer does not exist.

If cyclic movement is explicitly intended:

$$
27\rightarrow1
$$

giving:

$$
\boxed{A}
$$

> [!warning]
> Do not assume cyclic wrapping unless the question's pattern or options clearly support it.

---

# 43. How to Solve Alphabet Series

## Step 1 — Convert Letters to Positions

Example:

$$
C,\ H,\ M,\ R
$$

becomes:

$$
3,\ 8,\ 13,\ 18
$$

---

## Step 2 — Calculate Differences

$$
+5,+5,+5
$$

Therefore:

$$
\boxed{W}
$$

---

## Step 3 — If Not Constant, Check Difference Pattern

Example:

$$
A,\ C,\ F,\ J,\ O
$$

positions:

$$
1,3,6,10,15
$$

differences:

$$
2,3,4,5
$$

---

## Step 4 — Check Alternate Terms

Separate:

$$
1,3,5,\ldots
$$

and:

$$
2,4,6,\ldots
$$

---

## Step 5 — Check Forward and Backward Movement

Examples:

$$
+3,-2,+3,-2
$$

---

## Step 6 — Check Reverse Alphabet

Use:

$$
A=26,\ B=25,\ldots,Z=1
$$

---

## Step 7 — Check Number Properties

Test:

- Odd positions
- Even positions
- Prime positions
- Square positions
- Multiples

---

## Step 8 — Check Wrap-Around

Only when appropriate:

$$
Z\rightarrow A
$$

---

## Step 9 — Verify

Convert the predicted numerical position back to a letter.

---

# 44. Pattern Recognition Tricks

## Pattern 1 — Consecutive Letters

> [!important]
> If:

$$
A,B,C,D
$$

think:

$$
+1
$$

---

## Pattern 2 — Every Alternate Letter

> [!important]
> If:

$$
A,C,E,G
$$

think:

$$
+2
$$

---

## Pattern 3 — Fixed Gap

> [!important]
> If:

$$
B,F,J,N
$$

positions:

$$
2,6,10,14
$$

think:

$$
+4
$$

---

## Pattern 4 — Increasing Gap

> [!important]
> If:

$$
A,C,F,J
$$

positions:

$$
1,3,6,10
$$

think:

$$
+2,+3,+4
$$

---

## Pattern 5 — Decreasing Gap

> [!important]
> If:

$$
Z,X,U,Q
$$

think:

$$
-2,-3,-4
$$

---

## Pattern 6 — Alternating Direction

> [!important]
> If:

$$
A,D,C,F,E,H
$$

think:

$$
+3,-1,+3,-1,+3
$$

---

## Pattern 7 — Two Interleaved Sequences

> [!important]
> If:

$$
A,Z,C,X,E,V
$$

split odd and even positions.

---

## Pattern 8 — Reverse Alphabet

> [!important]
> If:

$$
Z,Y,X,W
$$

think:

$$
-1
$$

---

## Pattern 9 — Prime Positions

> [!important]
> If letters correspond to:

$$
2,3,5,7,11,13
$$

think:

$$
\boxed{\text{Prime numbers}}
$$

---

## Pattern 10 — Position Squares

> [!important]
> If positions are:

$$
1,4,9,16,25
$$

think:

$$
\boxed{n^2}
$$

---

# 45. Shortcuts

> [!tip]
> **Shortcut 1 — Memorize alphabet anchors**

Memorize:

$$
A=1
$$

$$
E=5
$$

$$
J=10
$$

$$
M=13
$$

$$
N=14
$$

$$
T=20
$$

$$
Z=26
$$

This reduces lookup time.

---

> [!tip]
> **Shortcut 2 — Use distance rather than counting letters**

For:

$$
C\rightarrow H
$$

calculate:

$$
8-3=5
$$

So the movement is:

$$
+5
$$

---

> [!tip]
> **Shortcut 3 — Reverse position formula**

For a letter at position $p$:

$$
\boxed{\text{Reverse position}=27-p}
$$

Example:

$$
G=7
$$

Therefore:

$$
27-7=20
$$

So $G$ has reverse position:

$$
\boxed{20}
$$

---

> [!tip]
> **Shortcut 4 — Middle alphabet anchor**

Since:

$$
M=13,\quad N=14
$$

letters near the middle can be calculated quickly in either direction.

---

> [!tip]
> **Shortcut 5 — Split odd/even positions immediately**

If a sequence looks like:

$$
A,Z,C,X,E,V
$$

do not try to find one global rule.

Split it.

---

> [!tip]
> **Shortcut 6 — Check skipped letters carefully**

If movement is:

$$
+4
$$

then the number of skipped letters is:

$$
3
$$

because:

$$
A\rightarrow E
$$

passes over:

$$
B,C,D
$$

---

> [!tip]
> **Shortcut 7 — Watch for wrap-around**

If the sequence approaches $Z$ and continues:

$$
X,\ Z,\ B,\ D
$$

think cyclic movement.

---

# 46. Common Exam Patterns

> [!important] Must Master

### Basic Patterns

1. Consecutive letters
2. Reverse consecutive letters
3. Alternate letters
4. Fixed-gap letters
5. Increasing gaps
6. Decreasing gaps

### Direction Patterns

7. Forward movement
8. Backward movement
9. Alternating forward/backward
10. Cyclic alphabet

### Structural Patterns

11. Odd-even position series
12. Two interleaved series
13. Pair-based series
14. Reverse pair series
15. Mirror alphabet series

### Mathematical Position Patterns

16. Odd alphabet positions
17. Even alphabet positions
18. Prime positions
19. Composite positions
20. Square positions
21. Multiple-based positions

### Category-Based Patterns

22. Vowels
23. Consonants
24. Vowel-consonant alternation

### Advanced

25. Increasing movement
26. Alternating movement
27. Mixed position differences
28. Letter pair transformations
29. Position arithmetic
30. Cyclic position patterns

---

# 47. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Counting letters manually

For:

$$
C\rightarrow M
$$

do not count one by one.

Use positions:

$$
13-3=10
$$

---

### Mistake 2 — Confusing movement with skipped letters

Moving by $5$ means skipping $4$ letters.

---

### Mistake 3 — Forgetting reverse direction

For:

$$
Z,X,V,T
$$

the pattern is:

$$
-2
$$

not $+2$.

---

### Mistake 4 — Ignoring odd/even positions

A sequence can contain two simple patterns interleaved together.

---

### Mistake 5 — Assuming cyclic movement

Do not automatically move:

$$
Z\rightarrow A
$$

unless the sequence clearly supports it.

---

### Mistake 6 — Forgetting that $M$ and $N$ are positions 13 and 14

This is a useful central anchor.

---

### Mistake 7 — Treating letter series as pure memorization

Most alphabet series become easier after converting letters into numbers.

---

### Mistake 8 — Accepting a pattern after one transition

For example:

$$
A,D,G
$$

suggests $+3$, but you should verify later terms.

---

# 48. Formula Sheet

## Alphabet Position

$$
\boxed{A=1,\ldots,Z=26}
$$

## Reverse Position

$$
\boxed{27-p}
$$

## Forward Movement

$$
\boxed{p_{\text{next}}=p+k}
$$

## Backward Movement

$$
\boxed{p_{\text{next}}=p-k}
$$

## Position Difference

$$
\boxed{d=p_2-p_1}
$$

## Cyclic Forward Position

$$
\boxed{p_{\text{next}}=(p+k-1)\bmod26+1}
$$

## Cyclic Backward Position

Using a 1-based position:

$$
\boxed{p_{\text{next}}=((p-k-1)\bmod26)+1}
$$

## Reverse Alphabet Mapping

$$
\boxed{A\leftrightarrow Z}
$$

$$
\boxed{B\leftrightarrow Y}
$$

$$
\boxed{C\leftrightarrow X}
$$

In general:

$$
\boxed{p_{\text{reverse}}=27-p}
$$

---

# 49. Quick Revision

> [!summary] One-Minute Revision

## Alphabet Series

The fastest method is:

$$
\boxed{\text{Letter}\rightarrow\text{Position}\rightarrow\text{Pattern}\rightarrow\text{Letter}}
$$

### Alphabet Positions

$$
A=1,\ B=2,\ldots,Z=26
$$

### Reverse Positions

$$
A=26,\ B=25,\ldots,Z=1
$$

### First Things to Check

1. $+1$ / $-1$
2. $+2$ / $-2$
3. Fixed gap
4. Increasing gap
5. Decreasing gap
6. Alternating movement
7. Odd-even positions
8. Reverse alphabet
9. Prime positions
10. Square positions
11. Vowels/consonants
12. Pair patterns
13. Cyclic movement

### Critical Distinction

Movement by $k$ positions means:

$$
\boxed{k-1\text{ letters skipped}}
$$

### Reverse Formula

$$
\boxed{27-p}
$$

### Cyclic Pattern

Use wrap-around only when supported:

$$
Z\rightarrow A
$$

### Golden Memory Trick

**"Convert letters into positions before trying to solve the pattern."**

# One-Line Recognition

**When an alphabet sequence looks unfamiliar, convert each letter to its position from 1 to 26, identify the numerical pattern, and convert the resulting position back into a letter.**