---
type: concept
subject: reasoning
topic: "Letter Series"
parent: "03. Series"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - series
  - letter-series
  - alphabet-reasoning
  - pattern-recognition
  - logical-reasoning
  - hcl
wikilinks:
  - "[[03. Series]]"
  - "[[Alphabet Series]]"
  - "[[Alphanumeric Series]]"
  - "[[Mixed Series]]"
  - "[[Coding Decoding]]"
---

# Letter Series

## 1. Core Concept

> [!summary]
> A **Letter Series** is a sequence of letters or groups of letters arranged according to a logical rule. The rule may involve forward/backward movement, fixed or changing gaps, alternate positions, reverse order, vowel-consonant patterns, paired letters, or multiple interleaved sequences.

Example:

$$
B,\ E,\ H,\ K,\ ?
$$

Convert letters into positions:

$$
2,\ 5,\ 8,\ 11,\ ?
$$

The pattern is:

$$
+3
$$

Therefore:

$$
11+3=14
$$

Position $14$ is:

$$
\boxed{N}
$$

### Core Intuition

Think:

$$
\boxed{\text{LETTER}\rightarrow\text{POSITION}\rightarrow\text{PATTERN}\rightarrow\text{ANSWER}}
$$

The key difference from a simple alphabet sequence is that **Letter Series can use more complex relationships between letters**, including groups and alternating rules.

---

# 2. Basic Meaning

A letter series question gives a sequence such as:

$$
A,\ C,\ F,\ J,\ O,\ ?
$$

and asks you to determine the next or missing letter.

The hidden rule can be based on:

- Alphabet position
- Forward movement
- Backward movement
- Increasing gaps
- Decreasing gaps
- Alternating gaps
- Odd-even positions
- Reverse alphabet
- Vowels
- Consonants
- Letter pairs
- Mirror positions
- Cyclic movement
- Position-based mathematics
- Multiple simultaneous patterns

### Example

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

Next difference:

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

# 3. Main Formula

## 3.1 Alphabet Position

$$
\boxed{A=1,\ B=2,\ C=3,\ldots,Z=26}
$$

---

## 3.2 Forward Movement

If a letter moves forward by $k$ positions:

$$
\boxed{p_{\text{next}}=p+k}
$$

---

## 3.3 Backward Movement

$$
\boxed{p_{\text{next}}=p-k}
$$

---

## 3.4 Reverse Position

For normal position $p$:

$$
\boxed{p_{\text{reverse}}=27-p}
$$

Example:

$$
H=8
$$

Therefore:

$$
27-8=19
$$

So the reverse-position counterpart of $H$ is:

$$
\boxed{S}
$$

---

## 3.5 Cyclic Alphabet

When the sequence wraps after $Z$:

$$
\boxed{p_{\text{next}}=((p+k-1)\bmod26)+1}
$$

Example:

$$
Y\rightarrow A
$$

with a movement of $2$.

---

# 4. Important Properties

1. Letter series can contain one or multiple patterns.
2. Alphabet positions are usually the easiest representation.
3. Forward movement increases the position.
4. Backward movement decreases the position.
5. The gap between letters may remain constant.
6. The gap may increase or decrease.
7. Odd and even positions may form separate series.
8. The sequence may alternate between two operations.
9. Letters may be paired.
10. The first and second letters of each pair may follow separate rules.
11. Reverse alphabet relationships may be used.
12. Vowel and consonant classification may form the pattern.
13. The sequence may wrap around $Z$.
14. Mathematical sequences can be mapped to letter positions.
15. A pattern must be verified across multiple transitions.

---

# 5. Alphabet Position Reference

| Letter | Position | Letter | Position |
|---|---:|---|---:|
| A | 1 | N | 14 |
| B | 2 | O | 15 |
| C | 3 | P | 16 |
| D | 4 | Q | 17 |
| E | 5 | R | 18 |
| F | 6 | S | 19 |
| G | 7 | T | 20 |
| H | 8 | U | 21 |
| I | 9 | V | 22 |
| J | 10 | W | 23 |
| K | 11 | X | 24 |
| L | 12 | Y | 25 |
| M | 13 | Z | 26 |

### Useful Anchors

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

> [!tip]
> Memorizing anchor letters is faster than memorizing the entire alphabet-position table.

---

# 6. Basic Examples

## Example 1 — Consecutive Letter Series

### Question

Find the next letter:

$$
D,\ E,\ F,\ G,\ ?
$$

Positions:

$$
4,\ 5,\ 6,\ 7
$$

Pattern:

$$
+1
$$

Therefore:

$$
\boxed{H}
$$

---

## Example 2 — Fixed Forward Gap

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

Next:

$$
10+3=13
$$

Therefore:

$$
\boxed{M}
$$

---

## Example 3 — Fixed Backward Gap

### Question

$$
Z,\ W,\ T,\ Q,\ ?
$$

Positions:

$$
26,\ 23,\ 20,\ 17
$$

Difference:

$$
-3
$$

Next:

$$
17-3=14
$$

Therefore:

$$
\boxed{N}
$$

---

# 7. Increasing Gap Series

## Example 4

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

> [!important]
> When the gaps increase by $1$, immediately test:

$$
+2,+3,+4,+5,\ldots
$$

---

# 8. Decreasing Gap Series

## Example 5

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

# 9. Alternating Gap Series

## Example 6

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

### Pattern

$$
+3,+2,+3,+2,+3,+2
$$

---

# 10. Alternating Direction Series

## Example 7

### Question

$$
B,\ E,\ D,\ G,\ F,\ I,\ ?
$$

Positions:

$$
2,\ 5,\ 4,\ 7,\ 6,\ 9
$$

Operations:

$$
+3,-1,+3,-1,+3
$$

Next:

$$
9-1=8
$$

### Answer

$$
\boxed{H}
$$

---

# 11. Odd-Even Position Series

## Example 8

### Question

$$
A,\ Z,\ C,\ X,\ E,\ V,\ ?
$$

Separate odd and even positions.

### Odd Positions

$$
A,\ C,\ E,\ ?
$$

Pattern:

$$
+2
$$

Next:

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

The next term is in an odd position.

### Answer

$$
\boxed{G}
$$

> [!important]
> This is one of the most important letter-series patterns for placement exams.

---

# 12. Two Interleaved Letter Series

## Example 9

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
H+3=K
$$

Even positions:

$$
D,\ G,\ J
$$

also follow:

$$
+3
$$

### Answer

$$
\boxed{K}
$$

---

# 13. Reverse Alphabet Series

## Example 10

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

# 14. Reverse-Pair Pattern

## Example 11

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

Therefore:

$$
E,V
$$

### Answer

$$
\boxed{EV}
$$

---

# 15. Mirror Alphabet Pattern

## Example 12

### Question

$$
A,\ Z,\ B,\ Y,\ C,\ X,\ ?
$$

Odd positions:

$$
A,B,C,\ ?
$$

Next:

$$
D
$$

Even positions:

$$
Z,Y,X
$$

Next:

$$
W
$$

Therefore:

$$
\boxed{D}
$$

### Full Pattern

$$
A,Z,B,Y,C,X,D,W,\ldots
$$

---

# 16. Letter Pairs

## Example 13

### Question

$$
AB,\ DE,\ GH,\ JK,\ ?
$$

First letters:

$$
A,D,G,J
$$

Movement:

$$
+3
$$

Second letters:

$$
B,E,H,K
$$

Movement:

$$
+3
$$

Therefore:

$$
M,N
$$

### Answer

$$
\boxed{MN}
$$

---

# 17. Pair Pattern with Different Directions

## Example 14

### Question

$$
AZ,\ CX,\ EV,\ GT,\ ?
$$

First letters:

$$
A,C,E,G
$$

Pattern:

$$
+2
$$

Second letters:

$$
Z,X,V,T
$$

Pattern:

$$
-2
$$

Next pair:

$$
I,R
$$

### Answer

$$
\boxed{IR}
$$

---

# 18. Vowel Series

## Example 15

### Question

$$
A,\ E,\ I,\ O,\ ?
$$

The English vowels are:

$$
A,E,I,O,U
$$

Therefore:

$$
\boxed{U}
$$

> [!important]
> If alphabet-position arithmetic does not produce a useful pattern, check whether the letters belong to a category such as vowels or consonants.

---

# 19. Consonant Series

## Example 16

### Question

$$
B,\ C,\ D,\ F,\ G,\ ?
$$

These are consecutive consonants.

After $G$ comes $H$.

### Answer

$$
\boxed{H}
$$

---

# 20. Vowel-Consonant Alternation

## Example 17

Consider:

$$
A,\ B,\ E,\ F,\ I,\ J,\ ?
$$

Group the terms:

$$
A,B
$$

$$
E,F
$$

$$
I,J
$$

The first letter of each pair follows:

$$
A,E,I
$$

and the second letter follows:

$$
B,F,J
$$

Both move by:

$$
+4
$$

Next first letter:

$$
I+4=M
$$

### Answer

$$
\boxed{M}
$$

---

# 21. Position-Based Letter Series

## Example 18

### Question

$$
A,\ D,\ I,\ P,\ ?
$$

Positions:

$$
1,\ 4,\ 9,\ 16
$$

These are squares:

$$
1^2,2^2,3^2,4^2
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

# 22. Prime-Position Letter Series

## Example 19

### Question

$$
B,\ C,\ E,\ G,\ K,\ M,\ ?
$$

Positions:

$$
2,\ 3,\ 5,\ 7,\ 11,\ 13
$$

These are consecutive prime numbers.

Next:

$$
17
$$

Therefore:

$$
\boxed{Q}
$$

---

# 23. Odd-Position Letter Series

## Example 20

### Question

$$
A,\ C,\ E,\ G,\ I,\ ?
$$

Positions:

$$
1,3,5,7,9
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

# 24. Even-Position Letter Series

## Example 21

### Question

$$
B,\ D,\ F,\ H,\ ?
$$

Positions:

$$
2,4,6,8
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

# 25. Wrap-Around Series

## Example 22

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

After $Z$, the sequence returns to $A$.

Therefore:

$$
D+2=F
$$

### Answer

$$
\boxed{F}
$$

---

# 26. Wrap-Around with a Larger Step

## Example 23

### Question

$$
Y,\ C,\ G,\ K,\ ?
$$

Positions:

$$
25,\ 3,\ 7,\ 11
$$

The movement is:

$$
+4
$$

Next:

$$
11+4=15
$$

Position $15$:

$$
\boxed{O}
$$

---

# 27. Reverse Wrap-Around

## Example 24

### Question

$$
C,\ A,\ Y,\ W,\ ?
$$

Positions:

$$
3,\ 1,\ 25,\ 23
$$

Movement:

$$
-2
$$

Therefore:

$$
23-2=21
$$

Position $21$:

$$
\boxed{U}
$$

---

# 28. Increasing Movement with Letter Series

## Example 25

### Question

$$
B,\ D,\ G,\ K,\ P,\ ?
$$

Positions:

$$
2,\ 4,\ 7,\ 11,\ 16
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
16+6=22
$$

### Answer

$$
\boxed{V}
$$

---

# 29. Decreasing Movement with Letter Series

## Example 26

### Question

$$
Z,\ W,\ S,\ N,\ H,\ ?
$$

Positions:

$$
26,\ 23,\ 19,\ 14,\ 8
$$

Differences:

$$
-3,-4,-5,-6
$$

Next:

$$
-7
$$

Therefore:

$$
8-7=1
$$

### Answer

$$
\boxed{A}
$$

---

# 30. Alternating Increasing Movement

## Example 27

### Question

$$
A,\ C,\ G,\ I,\ M,\ O,\ ?
$$

Positions:

$$
1,\ 3,\ 7,\ 9,\ 13,\ 15
$$

Differences:

$$
+2,+4,+2,+4,+2
$$

Next:

$$
+4
$$

Therefore:

$$
15+4=19
$$

### Answer

$$
\boxed{S}
$$

---

# 31. Letter Series Based on Multiples

## Example 28

### Question

$$
C,\ F,\ I,\ L,\ O,\ ?
$$

Positions:

$$
3,\ 6,\ 9,\ 12,\ 15
$$

These are multiples of $3$.

Next:

$$
18
$$

Therefore:

$$
\boxed{R}
$$

---

# 32. Letter Series Based on Odd Numbers

## Example 29

### Question

$$
A,\ C,\ G,\ M,\ U,\ ?
$$

Positions:

$$
1,\ 3,\ 7,\ 13,\ 21
$$

Differences:

$$
+2,+4,+6,+8
$$

Next:

$$
+10
$$

This gives:

$$
21+10=31
$$

Without cyclic wrapping, there is no valid alphabet position.

> [!warning]
> Always check whether the numerical pattern remains within $1$ to $26$. If it exceeds $26$, do not assume wrapping unless the sequence supports it.

---

# 33. Advanced Letter Pattern — Alternating Large Steps

## Example 30

### Question

$$
A,\ F,\ D,\ I,\ G,\ L,\ ?
$$

Positions:

$$
1,\ 6,\ 4,\ 9,\ 7,\ 12
$$

Pattern:

$$
+5,-2,+5,-2,+5
$$

Next:

$$
12-2=10
$$

### Answer

$$
\boxed{J}
$$

---

# 34. Advanced Letter Pattern — Two Independent Rules

## Example 31

### Question

$$
B,\ Y,\ E,\ V,\ H,\ S,\ ?
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
Y,\ V,\ S
$$

Pattern:

$$
-3
$$

The next term belongs to the odd sequence.

### Answer

$$
\boxed{K}
$$

---

# 35. Advanced Letter Pattern — Pair Movement

## Example 32

### Question

$$
AC,\ DF,\ GI,\ JL,\ ?
$$

First letters:

$$
A,D,G,J
$$

Second letters:

$$
C,F,I,L
$$

Both move by:

$$
+3
$$

Therefore:

$$
M,O
$$

### Answer

$$
\boxed{MO}
$$

---

# 36. Advanced Letter Pattern — Mirror Pairs

## Example 33

### Question

$$
AZ,\ BY,\ CX,\ DW,\ ?
$$

The pair positions always sum to:

$$
27
$$

because:

$$
A(1)+Z(26)=27
$$

$$
B(2)+Y(25)=27
$$

$$
C(3)+X(24)=27
$$

$$
D(4)+W(23)=27
$$

Therefore:

$$
E(5)+V(22)=27
$$

### Answer

$$
\boxed{EV}
$$

> [!important]
> When two letters appear as mirror pairs, check whether their alphabet positions sum to $27$.

---

# 37. Advanced Letter Pattern — Difference Sequence

## Example 34

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

---

# 38. Advanced Letter Pattern — Prime Positions

## Example 35

### Question

$$
B,\ C,\ E,\ G,\ K,\ M,\ Q,\ ?
$$

Positions:

$$
2,3,5,7,11,13,17
$$

These are prime numbers.

Next:

$$
19
$$

Therefore:

$$
\boxed{S}
$$

---

# 39. How to Solve Letter Series

## Step 1 — Identify the Type

Ask:

> Are these single letters, pairs, or groups?

---

## Step 2 — Convert to Positions

Example:

$$
D,\ H,\ L,\ P
$$

becomes:

$$
4,\ 8,\ 12,\ 16
$$

---

## Step 3 — Check Direct Difference

$$
+4,+4,+4
$$

If constant, stop.

---

## Step 4 — Check Changing Difference

Look for:

$$
+2,+3,+4,+5
$$

or:

$$
-2,-3,-4,-5
$$

---

## Step 5 — Check Alternation

Look for:

$$
+3,-1,+3,-1
$$

---

## Step 6 — Split Odd and Even Terms

For:

$$
A,Z,C,X,E,V
$$

check:

$$
A,C,E
$$

and:

$$
Z,X,V
$$

---

## Step 7 — Check Reverse Relationships

Look for:

$$
A\leftrightarrow Z
$$

$$
B\leftrightarrow Y
$$

$$
C\leftrightarrow X
$$

---

## Step 8 — Check Categories

Test:

- Vowels
- Consonants
- Odd-position letters
- Even-position letters
- Prime-position letters

---

## Step 9 — Check Mathematical Position Patterns

Try:

$$
n^2
$$

$$
n^3
$$

$$
2n
$$

$$
3n
$$

or another obvious sequence.

---

## Step 10 — Check Cyclic Movement

Only when appropriate:

$$
Z\rightarrow A
$$

---

## Step 11 — Verify

The rule should explain all given terms.

---

# 40. Pattern Recognition

## Pattern 1 — Consecutive Letters

> [!important]
> If the letters are:

$$
D,E,F,G
$$

think:

$$
+1
$$

---

## Pattern 2 — Fixed Gap

> [!important]
> If:

$$
B,E,H,K
$$

think:

$$
+3
$$

---

## Pattern 3 — Increasing Gap

> [!important]
> If:

$$
A,C,F,J
$$

think:

$$
+2,+3,+4
$$

---

## Pattern 4 — Decreasing Gap

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

## Pattern 5 — Alternating Gap

> [!important]
> If:

$$
A,D,F,I,K
$$

think:

$$
+3,+2,+3,+2
$$

---

## Pattern 6 — Alternate Directions

> [!important]
> If:

$$
B,E,D,G,F,I
$$

think:

$$
+3,-1,+3,-1,+3
$$

---

## Pattern 7 — Odd-Even Series

> [!important]
> If the sequence looks irregular, separate:

$$
1^{st},3^{rd},5^{th}
$$

and:

$$
2^{nd},4^{th},6^{th}
$$

---

## Pattern 8 — Mirror Pair

> [!important]
> If:

$$
AZ,\ BY,\ CX
$$

think:

$$
p_1+p_2=27
$$

---

## Pattern 9 — Prime Positions

> [!important]
> If positions are:

$$
2,3,5,7,11,13
$$

think:

$$
\boxed{\text{Prime numbers}}
$$

---

## Pattern 10 — Square Positions

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

# 41. Shortcuts

> [!tip]
> **Shortcut 1 — Convert immediately**

Do not mentally count:

$$
G\rightarrow M
$$

Use:

$$
13-7=6
$$

Therefore the movement is:

$$
+6
$$

---

> [!tip]
> **Shortcut 2 — Memorize anchor letters**

Use:

$$
A=1,\ E=5,\ J=10,\ M=13,\ N=14,\ T=20,\ Z=26
$$

---

> [!tip]
> **Shortcut 3 — Difference means movement**

If:

$$
C\rightarrow H
$$

then:

$$
8-3=5
$$

So movement is $+5$.

---

> [!tip]
> **Shortcut 4 — Check alternate positions early**

If the sequence has unusual jumps, split it.

This is especially useful for patterns like:

$$
A,Z,C,X,E,V
$$

---

> [!tip]
> **Shortcut 5 — Check both ends**

For mirror patterns:

$$
A-Z
$$

$$
B-Y
$$

$$
C-X
$$

Remember:

$$
\boxed{p_1+p_2=27}
$$

---

> [!tip]
> **Shortcut 6 — Remember skipped letters**

Movement:

$$
+4
$$

means:

$$
3\text{ letters skipped}
$$

not $4$.

---

> [!tip]
> **Shortcut 7 — Use category recognition**

If the sequence is:

$$
A,E,I,O
$$

do not calculate positions.

Recognize:

$$
\boxed{\text{Vowels}}
$$

---

# 42. Common Exam Patterns

> [!important] Must Master

### Basic

1. Consecutive letters
2. Reverse letters
3. Fixed-gap letters
4. Alternate letters
5. Odd-position letters
6. Even-position letters

### Gap-Based

7. Increasing gaps
8. Decreasing gaps
9. Alternating gaps
10. Alternating direction
11. Mixed gap patterns

### Structural

12. Odd-even interleaving
13. Two independent sequences
14. Pair series
15. Reverse pair series
16. Mirror pair series

### Mathematical

17. Odd positions
18. Even positions
19. Multiples
20. Prime positions
21. Composite positions
22. Square positions
23. Position-based sequences

### Category-Based

24. Vowels
25. Consonants
26. Vowel-consonant alternation

### Advanced

27. Cyclic alphabet
28. Reverse cyclic alphabet
29. Position arithmetic
30. Multiple simultaneous patterns
31. Complex pair transformations
32. Mixed letter-position patterns

---

# 43. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Counting manually

Do not count:

$$
A,B,C,D,E,F
$$

every time.

Use positions.

---

### Mistake 2 — Confusing gap with skipped letters

For:

$$
A\rightarrow F
$$

movement is:

$$
+5
$$

but skipped letters are:

$$
B,C,D,E
$$

So:

$$
4\text{ letters skipped}
$$

---

### Mistake 3 — Forgetting reverse direction

For:

$$
Z,W,T,Q
$$

the pattern is:

$$
-3
$$

---

### Mistake 4 — Missing alternating patterns

Always test odd/even positions when a direct pattern fails.

---

### Mistake 5 — Assuming cyclic movement

Do not automatically convert:

$$
Z+1=A
$$

unless the sequence clearly requires cyclic movement.

---

### Mistake 6 — Ignoring pairs

For:

$$
AZ,\ BY,\ CX
$$

treat each pair structurally.

---

### Mistake 7 — Ignoring letter categories

A sequence may use:

$$
A,E,I,O,U
$$

rather than numerical positions.

---

### Mistake 8 — Accepting a rule too early

Verify the pattern across the entire sequence.

---

# 44. Formula Sheet

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

## Cyclic Forward Movement

$$
\boxed{((p+k-1)\bmod26)+1}
$$

## Cyclic Backward Movement

$$
\boxed{((p-k-1)\bmod26)+1}
$$

## Mirror Pair

$$
\boxed{p_1+p_2=27}
$$

## Position Difference

$$
\boxed{d=p_2-p_1}
$$

---

# 45. Quick Revision

> [!summary] One-Minute Revision

## Letter Series

The fastest solving method is:

$$
\boxed{
Letter
\rightarrow
Position
\rightarrow
Difference
\rightarrow
Pattern
\rightarrow
Answer
}
$$

### First Check

$$
+1,-1
$$

### Second Check

$$
\text{Fixed gap}
$$

### Third Check

$$
\text{Increasing/decreasing gap}
$$

### Fourth Check

$$
\text{Alternating pattern}
$$

### Fifth Check

$$
\text{Odd/even positions}
$$

### Sixth Check

$$
\text{Reverse alphabet}
$$

### Seventh Check

$$
\text{Pairs/mirror pairs}
$$

### Eighth Check

$$
\text{Prime/square/multiple positions}
$$

### Ninth Check

$$
\text{Vowel/consonant pattern}
$$

### Tenth Check

$$
\text{Cyclic movement}
$$

### Critical Formulas

$$
A=1,\ldots,Z=26
$$

$$
\boxed{\text{Reverse position}=27-p}
$$

$$
\boxed{\text{Mirror pair sum}=27}
$$

### Golden Memory Trick

**"Letter series becomes easy when every letter is converted into a number and every jump is treated as a movement."**

# One-Line Recognition

**When a sequence of letters looks irregular, convert the letters to positions and check fixed gaps, changing gaps, alternate positions, reverse pairs, categories, and cyclic movement.**