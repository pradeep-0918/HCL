---
type: concept
subject: reasoning
topic: "Letter Classification"
parent: "02. Classification"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - classification
  - letter-classification
  - odd-one-out
  - hcl
  - logical-reasoning
wikilinks:
  - "[[02. Classification]]"
  - "[[Alphabet Classification]]"
  - "[[Word Classification]]"
  - "[[Letter Analogy]]"
---

# Letter Classification

## 1. Core Concept

> [!summary]
> **Letter Classification** identifies the letter or letter group that does not follow the same logical rule as the other options.

The key idea is:

$$
\boxed{\text{Find the common relationship shared by most letters}}
$$

Then identify the exception.

Letter classification may be based on:

- Alphabet position
- Position difference
- Vowel/consonant property
- Letter pairs
- Reverse alphabet
- Consecutive positions
- Symmetry
- Shape or stroke structure
- Position-based arithmetic
- Letter groups

### Example

**A, C, E, G, J**

Positions:

$$
1,3,5,7,10
$$

The first four increase by $2$.

But:

$$
7\rightarrow10=+3
$$

Therefore:

$$
\boxed{J}
$$

---

# 2. Basic Meaning

Letter classification is an **odd-one-out problem involving individual letters or groups of letters**.

Example:

**B, D, F, H, K**

Convert to positions:

$$
2,4,6,8,11
$$

The first four have even positions.

Therefore:

$$
\boxed{K}
$$

### Core Principle

If:

$$
A,B,C,D\rightarrow\text{Common Pattern}
$$

but:

$$
E\rightarrow\text{Different Pattern}
$$

then:

$$
\boxed{E=\text{Odd One Out}}
$$

---

# 3. Main Formula

There is no single formula.

The general rule is:

$$
\boxed{\text{Common Letter Property}\rightarrow\text{Exception}}
$$

### Common Patterns

| Pattern | Example |
|---|---|
| Same position parity | B, D, F, H |
| Same vowel/consonant type | A, E, I, O |
| Fixed position gap | A, D, G, J |
| Consecutive letters | A, B, C, D |
| Reverse pairs | A-Z, B-Y |
| Same position modulo | C, F, I, L |
| Same half | A, F, K, M |
| Increasing sequence | B, E, H, K |
| Decreasing sequence | Z, W, T, Q |
| Same structural property | H, I, O |
| Same number of strokes | Selected letters |

---

# 4. Important Properties

1. Standard alphabet positions are:

$$
A=1,\ldots,Z=26
$$

2. Vowels are:

$$
A,E,I,O,U
$$

3. Consonants are all remaining English letters.
4. First half:

$$
A-M
$$

5. Second half:

$$
N-Z
$$

6. Reverse alphabet positions satisfy:

$$
P_1+P_2=27
$$

7. Fixed-gap patterns can be detected using:

$$
d=P_{n+1}-P_n
$$

8. Letter classification may use visual properties in non-verbal reasoning.
9. For groups of letters, compare corresponding positions.
10. Choose the strongest rule that uniquely identifies one exception.

---

# 5. Basic Examples

## Example 1 — Even Positions

### Question

Find the odd letter:

**B, D, F, H, K**

### Pattern

$$
B=2
$$

$$
D=4
$$

$$
F=6
$$

$$
H=8
$$

These are even positions.

But:

$$
K=11
$$

Therefore:

$$
\boxed{K}
$$

---

## Example 2 — Odd Positions

### Question

**A, C, E, G, J**

Positions:

$$
1,3,5,7,10
$$

The first four are odd positions.

Therefore:

$$
\boxed{J}
$$

---

## Example 3 — Vowel Classification

### Question

**A, E, I, O, T**

A, E, I, and O are vowels.

T is a consonant.

### Answer

$$
\boxed{T}
$$

---

## Example 4 — Consecutive Letters

### Question

**P, Q, R, S, U**

The first four are consecutive:

$$
P,Q,R,S
$$

U skips T.

### Answer

$$
\boxed{U}
$$

---

# 6. Medium Examples

## Example 5 — Fixed Gap

### Question

**A, D, G, J, M, Q**

Positions:

$$
1,4,7,10,13,17
$$

The first five have a gap of:

$$
+3
$$

But:

$$
13\rightarrow17=+4
$$

### Answer

$$
\boxed{Q}
$$

---

## Example 6 — Multiples of 4

### Question

**D, H, L, P, T, V**

Positions:

$$
4,8,12,16,20,22
$$

The first five are multiples of $4$.

But:

$$
22
$$

is not a multiple of $4$.

### Answer

$$
\boxed{V}
$$

---

## Example 7 — Reverse Alphabet

### Question

Which pair is different?

**A-Z, B-Y, C-X, D-W, E-U**

For reverse pairs:

$$
P_1+P_2=27
$$

Check E-U:

$$
5+21=26
$$

Therefore it does not satisfy the rule.

### Answer

$$
\boxed{E-U}
$$

---

# 7. Advanced Examples

## Example 8 — Increasing Gap

### Question

Find the odd letter:

**A, B, D, G, K, P, W**

### Pattern Recognition

Positions:

$$
1,2,4,7,11,16,23
$$

Differences:

$$
+1,+2,+3,+4,+5,+7
$$

The expected final difference is:

$$
+6
$$

From P:

$$
16+6=22
$$

Position $22$ is V.

But the given letter is W:

$$
W=23
$$

Therefore:

$$
\boxed{W}
$$

---

## Example 9 — Alternating Pattern

### Question

Find the odd letter:

**A, D, C, F, E, H, J**

### Pattern Recognition

Look at pairs:

$$
A,D
$$

$$
C,F
$$

$$
E,H
$$

Each pair has:

$$
+3
$$

But:

$$
J
$$

does not form the expected pair with the preceding pattern.

Therefore:

$$
\boxed{J}
$$

---

## Example 10 — Letter Groups

### Question

Find the odd group:

**ABC, DEF, GHI, JKL, MNO, PRT**

### Pattern Recognition

The first five groups contain consecutive letters:

$$
ABC
$$

$$
DEF
$$

$$
GHI
$$

$$
JKL
$$

$$
MNO
$$

But:

$$
PRT
$$

is not consecutive.

### Answer

$$
\boxed{PRT}
$$

---

# 8. Structural Letter Classification

Some questions classify letters based on their visual structure rather than alphabet position.

## Example 11 — Closed Areas

Letters such as:

- A
- D
- O
- P
- Q
- R

may contain enclosed regions depending on the font/style.

> [!important]
> Structural classification depends on how the letters are represented. Use this pattern only when the question clearly uses visual letter shapes.

### Recognition

If the question emphasizes the **shape of letters**, check:

- enclosed areas
- straight/curved lines
- vertical symmetry
- horizontal symmetry
- number of strokes

---

# 9. Shortcuts

> [!tip]
> **Shortcut 1 — Convert to positions**

If the pattern is unclear:

$$
A=1,\ldots,Z=26
$$

Then calculate differences.

---

> [!tip]
> **Shortcut 2 — Check parity first**

Look for:

$$
Odd,\ Even
$$

Example:

$$
C=3,\ E=5,\ G=7
$$

All are odd positions.

---

> [!tip]
> **Shortcut 3 — Check gaps**

For:

$$
B,E,H,K
$$

positions:

$$
2,5,8,11
$$

Each difference is:

$$
+3
$$

---

> [!tip]
> **Shortcut 4 — Check reverse pairs**

Use:

$$
\boxed{P_1+P_2=27}
$$

Example:

$$
D=4
$$

Reverse position:

$$
27-4=23
$$

Therefore:

$$
D\leftrightarrow W
$$

---

> [!tip]
> **Shortcut 5 — Check vowels quickly**

If options contain several letters, first check whether most are:

$$
A,E,I,O,U
$$

---

> [!tip]
> **Shortcut 6 — For groups, compare internally**

For:

$$
ACE,\ BDF,\ CEG
$$

look at the internal gaps:

$$
+2,+2
$$

This can reveal the pattern immediately.

---

# 10. Recognition Tricks

## Pattern 1 — Even Position

> [!important]
> If most letters have positions divisible by $2$, check **Even Position**.

Example:

$$
B,D,F,H
$$

---

## Pattern 2 — Odd Position

> [!important]
> If most letters have odd positions, identify the even-position exception.

---

## Pattern 3 — Fixed Gap

> [!important]
> If the letters are regularly spaced, calculate the positional difference.

Example:

$$
A,D,G,J
$$

has:

$$
+3,+3,+3
$$

---

## Pattern 4 — Consecutive Letters

> [!important]
> If the letters appear one after another, think **Consecutive Sequence**.

Example:

$$
M,N,O,P
$$

---

## Pattern 5 — Reverse Alphabet

> [!important]
> For pairs, check:

$$
P_1+P_2=27
$$

---

## Pattern 6 — Multiples of a Number

> [!important]
> If positions are:

$$
3,6,9,12
$$

think:

$$
\text{Multiples of 3}
$$

---

## Pattern 7 — Alternating Pattern

> [!important]
> If the sequence looks irregular, split it into odd and even positions.

Example:

$$
A,C,E,G
$$

and:

$$
B,D,F,H
$$

may reveal two interleaved sequences.

---

## Pattern 8 — Structural Pattern

> [!important]
> If alphabet arithmetic fails and the letters are visually presented, check shape, symmetry, curves, and enclosed regions.

---

# 11. Common Exam Patterns

> [!important] Must Master

1. Even alphabet positions
2. Odd alphabet positions
3. Vowels
4. Consonants
5. Consecutive letters
6. Fixed position gaps
7. Reverse alphabet pairs
8. Multiples of alphabet positions
9. First-half letters
10. Second-half letters
11. Increasing position patterns
12. Decreasing position patterns
13. Alternating patterns
14. Letter-group classification
15. Reverse-order groups
16. Position-based arithmetic
17. Structural letter patterns
18. Symmetry-based classification
19. Stroke-based classification
20. Mixed classification

---

# 12. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Checking only vowels

Vowel/consonant is useful, but it may not be the intended rule.

Always verify whether another stronger pattern exists.

---

### Mistake 2 — Forgetting alphabet positions

For difficult questions, convert:

$$
A\rightarrow1,\ldots,Z\rightarrow26
$$

---

### Mistake 3 — Ignoring gaps

Do not just see:

$$
A,D,G,J
$$

as increasing letters.

Recognize:

$$
+3,+3,+3
$$

---

### Mistake 4 — Missing alternating patterns

For a sequence such as:

$$
A,D,C,F,E,H,G
$$

split odd and even positions before assuming the pattern is random.

---

### Mistake 5 — Confusing reverse alphabet with backward sequence

Reverse alphabet means:

$$
A\leftrightarrow Z
$$

Backward movement means:

$$
D\rightarrow C\rightarrow B
$$

These are different concepts.

---

### Mistake 6 — Using visual properties without evidence

Do not classify letters by appearance unless the question clearly depends on their shapes.

---

# 13. Formula Sheet

## Alphabet Position

$$
\boxed{A=1,\ldots,Z=26}
$$

## Position Difference

$$
\boxed{d=P_2-P_1}
$$

## Reverse Position

$$
\boxed{27-P}
$$

## Reverse Pair

$$
\boxed{P_1+P_2=27}
$$

## Even Position

$$
\boxed{P=2k}
$$

## Odd Position

$$
\boxed{P=2k-1}
$$

## Fixed Gap

$$
\boxed{P_{n+1}-P_n=k}
$$

## General Classification

$$
\boxed{\text{Common Property}\rightarrow\text{Exception}}
$$

---

# 14. Quick Revision

> [!summary] One-Minute Revision

### Letter Classification

Find the letter or letter group that breaks the common pattern.

### Check in This Order

1. Vowel/consonant
2. Odd/even position
3. Consecutive letters
4. Fixed gaps
5. Multiples
6. Reverse pairs
7. Increasing/decreasing sequence
8. Alternating sequence
9. Letter-group structure
10. Visual/structural properties

### Essential Facts

$$
A=1,\quad M=13,\quad Z=26
$$

$$
A,E,I,O,U=\text{Vowels}
$$

$$
A-M=\text{First half}
$$

$$
N-Z=\text{Second half}
$$

$$
P_1+P_2=27
$$

for reverse alphabet pairs.

### Golden Memory Trick

**"Turn letters into numbers, check the gap, then check the category."**

# One-Line Recognition

**When letters are given as an odd-one-out question, first test position, gap, vowel/consonant, and sequence patterns before considering complex visual properties.**