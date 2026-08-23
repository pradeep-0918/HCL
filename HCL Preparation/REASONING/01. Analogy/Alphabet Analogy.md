---
type: concept
subject: reasoning
topic: "Alphabet Analogy"
parent: "01. Analogy"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - analogy
  - alphabet-analogy
  - alphabet-reasoning
  - hcl
  - quantitative-reasoning
wikilinks:
  - "[[01. Analogy]]"
  - "[[Letter Analogy]]"
  - "[[Alphabet Series]]"
  - "[[Coding Decoding]]"
---

# Alphabet Analogy

## 1. Core Concept

> [!summary]
> **Alphabet Analogy** identifies the relationship between letters or alphabet positions and applies the same relationship to another pair of letters.

The standard form is:

$$
A:B::C:D
$$

In alphabet analogy, the relationship may involve:

- Forward movement
- Backward movement
- Alphabet position
- Equal positional gaps
- Reverse alphabet positions
- Alternating movement
- Letter pairs
- Vowels and consonants
- Position-based arithmetic

### Basic Idea

Convert letters into their alphabet positions:

$$
A=1,\ B=2,\ C=3,\ldots,Z=26
$$

Then solve the relationship numerically whenever possible.

Example:

**A : D :: F : ?**

A → D means:

$$
1\rightarrow4
$$

The shift is:

$$
+3
$$

Therefore:

$$
F+3=I
$$

Answer:

$$
\boxed{I}
$$

---

# 2. Basic Meaning

Alphabet analogy is a reasoning question where one pair of letters has a specific relationship, and the same relationship must be applied to another letter.

### Standard Form

$$
A:B::C:D
$$

means:

> A is related to B in the same way C is related to D.

### Alphabet Positions

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

---

# 3. Main Formula

## Alphabet Position

For a letter:

$$
A=1,\ B=2,\ldots,Z=26
$$

If the alphabet position of a letter is $n$, then:

### Forward Shift

$$
n+k
$$

### Backward Shift

$$
n-k
$$

### Reverse Alphabet Position

$$
27-n
$$

Therefore:

$$
\boxed{\text{Reverse Position}=27-\text{Original Position}}
$$

Example:

For C:

$$
27-3=24
$$

So:

$$
C\leftrightarrow X
$$

---

# 4. Important Properties

1. Always remember:

$$
A=1,\quad Z=26
$$

2. Alphabet positions make letter relationships easier to calculate.
3. Forward movement means increasing position.
4. Backward movement means decreasing position.
5. Reverse alphabet mapping follows:

$$
A\leftrightarrow Z
$$

$$
B\leftrightarrow Y
$$

$$
C\leftrightarrow X
$$

6. Alphabet analogy may contain one-letter or multi-letter patterns.
7. The direction of movement matters.
8. Wrap-around may be used.

Example:

$$
Y+3=B
$$

because:

$$
Y\rightarrow Z\rightarrow A\rightarrow B
$$

9. Not every question uses simple shifting.
10. Always verify the relationship with the complete pair.

---

# 5. Basic Examples

## Example 1 — Forward Shift

### Question

**A : D :: F : ?**

### Pattern Recognition

Alphabet positions:

$$
A=1
$$

$$
D=4
$$

Difference:

$$
4-1=3
$$

So the rule is:

$$
+3
$$

Apply to F:

$$
F=6
$$

$$
6+3=9
$$

Position 9 is I.

### Answer

$$
\boxed{I}
$$

---

## Example 2 — Backward Shift

### Question

**H : E :: M : ?**

### Pattern Recognition

$$
H=8
$$

$$
E=5
$$

Difference:

$$
8-5=3
$$

So the rule is:

$$
-3
$$

Apply to M:

$$
M=13
$$

$$
13-3=10
$$

Position 10 = J.

### Answer

$$
\boxed{J}
$$

---

## Example 3 — Shift by 5

### Question

**C : H :: K : ?**

### Pattern Recognition

$$
C=3
$$

$$
H=8
$$

Therefore:

$$
+5
$$

For K:

$$
K=11
$$

$$
11+5=16
$$

Position 16 = P.

### Answer

$$
\boxed{P}
$$

---

## Example 4 — Reverse Alphabet

### Question

**A : Z :: C : ?**

### Pattern Recognition

A and Z are opposite positions.

$$
A\leftrightarrow Z
$$

C is:

$$
C=3
$$

Reverse position:

$$
27-3=24
$$

Position 24 = X.

### Answer

$$
\boxed{X}
$$

---

# 6. Medium Examples

## Example 5 — Reverse Mapping

### Question

**D : W :: G : ?**

### Pattern Recognition

D is the 4th letter.

Reverse position:

$$
27-4=23
$$

Position 23 = W.

Therefore the rule is:

$$
n\rightarrow27-n
$$

For G:

$$
G=7
$$

$$
27-7=20
$$

Position 20 = T.

### Answer

$$
\boxed{T}
$$

---

## Example 6 — Equal Positional Difference

### Question

**M : Q :: R : ?**

### Pattern Recognition

$$
M=13
$$

$$
Q=17
$$

Difference:

$$
17-13=4
$$

Apply +4 to R:

$$
R=18
$$

$$
18+4=22
$$

Position 22 = V.

### Answer

$$
\boxed{V}
$$

---

## Example 7 — Backward Movement

### Question

**T : O :: K : ?**

### Pattern Recognition

$$
T=20
$$

$$
O=15
$$

Difference:

$$
20-15=5
$$

Rule:

$$
-5
$$

For K:

$$
11-5=6
$$

Position 6 = F.

### Answer

$$
\boxed{F}
$$

---

# 7. Advanced Examples

## Example 8 — Wrap-Around

### Question

**X : B :: W : ?**

### Pattern Recognition

X → B:

$$
X\rightarrow Y\rightarrow Z\rightarrow A\rightarrow B
$$

This is:

$$
+4
$$

Apply +4 to W:

$$
W\rightarrow X\rightarrow Y\rightarrow Z\rightarrow A
$$

### Answer

$$
\boxed{A}
$$

---

## Example 9 — Reverse + Shift

### Question

**B : X :: D : ?**

### Pattern Recognition

B has position:

$$
2
$$

Its reverse position is:

$$
27-2=25
$$

Position 25 = Y, not X.

So test a different relationship.

B → X means:

$$
2\rightarrow24
$$

Difference:

$$
+22
$$

Equivalent to:

$$
-4
$$

Therefore:

$$
B-4=X
$$

using cyclic movement.

Apply -4 to D:

$$
D\rightarrow C\rightarrow B\rightarrow A\rightarrow Z
$$

### Answer

$$
\boxed{Z}
$$

---

## Example 10 — Pair Relationship

### Question

**AB : CD :: EF : ?**

### Pattern Recognition

Each letter moves forward by 2:

$$
A\rightarrow C
$$

$$
B\rightarrow D
$$

Apply the same rule:

$$
E\rightarrow G
$$

$$
F\rightarrow H
$$

### Answer

$$
\boxed{GH}
$$

---

## Example 11 — Pair with Reverse Order

### Question

**AB : YZ :: CD : ?**

### Pattern Recognition

A → Y:

$$
1\rightarrow25
$$

B → Z:

$$
2\rightarrow26
$$

The relationship is:

$$
+24
$$

Apply to C and D:

$$
C\rightarrow A
$$

$$
D\rightarrow B
$$

### Answer

$$
\boxed{AB}
$$

---

# 8. Letter-Pair Analogy

Some questions use multiple letters.

## Example 12

### Question

**ACE : BDF :: MOQ : ?**

### Pattern Recognition

Compare corresponding positions:

$$
A\rightarrow B
$$

$$
C\rightarrow D
$$

$$
E\rightarrow F
$$

Every letter moves:

$$
+1
$$

Apply to MOQ:

$$
M\rightarrow N
$$

$$
O\rightarrow P
$$

$$
Q\rightarrow R
$$

### Answer

$$
\boxed{NPR}
$$

---

## Example 13 — Alternating Shift

### Question

**ABC : BDF :: DEF : ?**

### Pattern Recognition

Compare:

$$
A\rightarrow B=+1
$$

$$
B\rightarrow D=+2
$$

$$
C\rightarrow F=+3
$$

The shifts are:

$$
+1,\ +2,\ +3
$$

Apply to DEF:

$$
D+1=E
$$

$$
E+2=G
$$

$$
F+3=I
$$

### Answer

$$
\boxed{EGI}
$$

---

# 9. Shortcuts

> [!tip]
> **Shortcut 1 — Memorize anchor positions**

You should know these instantly:

$$
A=1,\ E=5,\ I=9,\ M=13,\ Q=17,\ U=21,\ Y=25
$$

Then count from the nearest anchor.

---

> [!tip]
> **Shortcut 2 — Memorize reverse pairs**

Remember:

$$
A-Z
$$

$$
B-Y
$$

$$
C-X
$$

$$
D-W
$$

$$
E-V
$$

$$
F-U
$$

$$
G-T
$$

$$
H-S
$$

$$
I-R
$$

$$
J-Q
$$

$$
K-P
$$

$$
L-O
$$

$$
M-N
$$

This makes reverse alphabet questions extremely fast.

---

> [!tip]
> **Shortcut 3 — Use position differences**

Instead of visually counting:

**F : K**

calculate:

$$
11-6=5
$$

So the relationship is:

$$
+5
$$

---

> [!tip]
> **Shortcut 4 — Use cyclic movement**

For letters near the end:

$$
Y+3=B
$$

Instead of continuing beyond Z, wrap around to A.

---

> [!tip]
> **Shortcut 5 — For letter groups, compare position-by-position**

For:

**ACE : BDF**

compare:

$$
A\rightarrow B
$$

$$
C\rightarrow D
$$

$$
E\rightarrow F
$$

The pattern becomes obvious.

---

# 10. Recognition Tricks

## Pattern 1 — Forward Shift

> [!important]
> If the second letter comes a fixed number of positions after the first, think **Forward Shift**.

Example:

**D : H**

$$
8-4=4
$$

Rule:

$$
+4
$$

---

## Pattern 2 — Backward Shift

> [!important]
> If the second letter comes a fixed number of positions before the first, think **Backward Shift**.

Example:

**M : I**

$$
13-9=4
$$

Rule:

$$
-4
$$

---

## Pattern 3 — Reverse Alphabet

> [!important]
> If A maps to Z, B maps to Y, or C maps to X, think **Reverse Alphabet**.

Formula:

$$
\boxed{27-n}
$$

---

## Pattern 4 — Wrap-Around

> [!important]
> If movement crosses Z, use cyclic alphabet movement.

Example:

$$
Y+4=C
$$

because:

$$
Y\rightarrow Z\rightarrow A\rightarrow B\rightarrow C
$$

---

## Pattern 5 — Corresponding Letter Shift

> [!important]
> For multiple letters, compare each corresponding position separately.

Example:

**ABC : CDE**

Each letter moves:

$$
+2
$$

---

## Pattern 6 — Increasing Shift

> [!important]
> If the differences are different but systematic, check whether they increase.

Example:

$$
A\rightarrow B=+1
$$

$$
B\rightarrow D=+2
$$

$$
C\rightarrow F=+3
$$

Think:

$$
+1,+2,+3
$$

---

## Pattern 7 — Vowel/Consonant Relationship

> [!important]
> If normal positional arithmetic does not work, check whether the letters are classified as vowels or consonants.

Vowels:

$$
A,E,I,O,U
$$

Some questions may use:

- next vowel
- previous vowel
- vowel position
- consonant position

Do not assume this pattern unless the given pair supports it.

---

# 11. Common Exam Patterns

> [!important] Must Master

### Pattern 1

Forward alphabet shift.

### Pattern 2

Backward alphabet shift.

### Pattern 3

Reverse alphabet.

### Pattern 4

Cyclic/wrap-around alphabet.

### Pattern 5

Fixed positional difference.

### Pattern 6

Two-letter analogy.

### Pattern 7

Three-letter analogy.

### Pattern 8

Corresponding letter transformation.

### Pattern 9

Increasing or decreasing shifts.

### Pattern 10

Vowel-based relationship.

### Pattern 11

Consonant-based relationship.

### Pattern 12

Alphabet position arithmetic.

### Pattern 13

Reverse position arithmetic.

### Pattern 14

Mixed letter transformation.

---

# 12. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Counting letters incorrectly

For:

**G → L**

the shift is:

$$
12-7=5
$$

Do not count G itself as the first movement.

---

### Mistake 2 — Forgetting A = 1

Alphabet positions start at:

$$
A=1
$$

not $A=0$ in standard aptitude reasoning.

---

### Mistake 3 — Forgetting wrap-around

For:

$$
Z+1
$$

the answer is:

$$
A
$$

not "27".

---

### Mistake 4 — Confusing reverse alphabet with backward shift

Reverse alphabet:

$$
A\leftrightarrow Z
$$

Backward shift:

$$
A\rightarrow Z
$$

can look similar at one position but are not generally the same rule.

For example:

$$
C\rightarrow X
$$

is reverse mapping, while:

$$
C-1=B
$$

is backward shifting.

---

### Mistake 5 — Applying one shift to an entire group without checking

For:

**ABC : BDF**

the shifts are:

$$
+1,+2,+3
$$

not a single constant shift.

---

### Mistake 6 — Ignoring corresponding positions

For multi-letter analogies, compare:

$$
1^{st}\rightarrow1^{st}
$$

$$
2^{nd}\rightarrow2^{nd}
$$

$$
3^{rd}\rightarrow3^{rd}
$$

before searching for complicated patterns.

---

# 13. Formula Sheet

## Alphabet Positions

$$
A=1,\ B=2,\ldots,Z=26
$$

## Forward Shift

$$
\boxed{P'=P+k}
$$

## Backward Shift

$$
\boxed{P'=P-k}
$$

## Reverse Alphabet

$$
\boxed{P'=27-P}
$$

## Positional Difference

$$
\boxed{k=P_2-P_1}
$$

## Cyclic Forward Movement

If the position exceeds 26:

$$
\boxed{P'=(P+k-1)\bmod26+1}
$$

## Cyclic Backward Movement

$$
\boxed{P'=(P-k-1)\bmod26+1}
$$

## Analogy Rule

$$
\boxed{f(A)=B\Rightarrow f(C)=D}
$$

---

# 14. Quick Revision

> [!summary] One-Minute Revision

### Alphabet Analogy

$$
A:B::C:D
$$

Find the transformation from the first letter/group to the second.

### Essential Positions

$$
A=1,\quad M=13,\quad Z=26
$$

### Reverse Rule

$$
\boxed{27-n}
$$

### Check in This Order

1. Forward shift
2. Backward shift
3. Positional difference
4. Reverse alphabet
5. Wrap-around
6. Multi-letter correspondence
7. Increasing/decreasing shifts
8. Vowel/consonant pattern

### Must Remember

$$
A\leftrightarrow Z
$$

$$
B\leftrightarrow Y
$$

$$
C\leftrightarrow X
$$

$$
M\leftrightarrow N
$$

### Golden Memory Trick

**"Convert letters to positions, find the shift, then apply the same shift."**

# One-Line Recognition

**When you see letters in an analogy, convert them to alphabet positions and first check for a fixed forward, backward, or reverse relationship.**