---
type: concept
subject: reasoning
topic: "Letter Analogy"
parent: "01. Analogy"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - analogy
  - letter-analogy
  - hcl
  - logical-reasoning
wikilinks:
  - "[[01. Analogy]]"
  - "[[Word Analogy]]"
  - "[[Alphabet Analogy]]"
  - "[[Coding Decoding]]"
---

# Letter Analogy

## 1. Core Concept

> [!summary]
> **Letter Analogy** finds the relationship between letters or groups of letters and applies the same relationship to another group.

Basic form:

$$
A:B::C:D
$$

The important question is:

> **What transformation changes A into B?**

Then apply the same transformation to C.

Letter analogy is closely related to alphabet analogy, but it can involve more complex transformations such as:

- Position shifting
- Reversal
- Pair swapping
- Alternate-letter movement
- Increasing/decreasing shifts
- Letter combinations
- Position-based arithmetic
- Vowel/consonant relationships

---

# 2. Basic Meaning

A letter analogy gives a relationship between two letters or letter groups.

Example:

**AB : BC :: DE : ?**

Compare the first pair:

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

Each letter moves one position forward.

Apply the same rule:

$$
D\rightarrow E
$$

$$
E\rightarrow F
$$

Therefore:

$$
\boxed{EF}
$$

---

# 3. Main Formula

For alphabet position:

$$
A=1,\ B=2,\ldots,Z=26
$$

If a letter moves $k$ positions:

### Forward

$$
P'=P+k
$$

### Backward

$$
P'=P-k
$$

### Reverse

$$
P'=27-P
$$

For a multi-letter group, apply the transformation to each corresponding position unless the pattern indicates otherwise.

General rule:

$$
\boxed{f(L_1,L_2,\ldots,L_n)=R_1,R_2,\ldots,R_n}
$$

Then apply the same $f$ to the second group.

---

# 4. Important Properties

1. Letter order is important.
2. The same transformation must apply to both pairs.
3. Convert letters into positions when the relationship is unclear.
4. Compare corresponding letters first.
5. Check whether the shift is constant.
6. If the shift is not constant, check whether it follows a sequence.
7. Check reversal and swapping.
8. Check alternate positions.
9. Watch for cyclic movement after Z.
10. Use the simplest rule that completely explains the given pair.

### Common Alphabet Positions

| Letter | Position |
|---|---:|
| A | 1 |
| E | 5 |
| I | 9 |
| M | 13 |
| O | 15 |
| Q | 17 |
| U | 21 |
| Y | 25 |
| Z | 26 |

---

# 5. Basic Examples

## Example 1 — One-Step Forward

### Question

**A : B :: F : ?**

### Pattern

$$
A\rightarrow B
$$

Shift:

$$
+1
$$

Apply to F:

$$
F\rightarrow G
$$

### Answer

$$
\boxed{G}
$$

---

## Example 2 — Backward Shift

### Question

**H : F :: M : ?**

### Pattern

$$
H\rightarrow F
$$

Alphabet positions:

$$
8\rightarrow6
$$

Therefore:

$$
-2
$$

Apply to M:

$$
13-2=11
$$

Position 11 = K.

### Answer

$$
\boxed{K}
$$

---

## Example 3 — Fixed Forward Shift

### Question

**C : H :: J : ?**

### Pattern

$$
C=3,\quad H=8
$$

Difference:

$$
8-3=5
$$

Apply +5 to J:

$$
J=10
$$

$$
10+5=15
$$

Position 15 = O.

### Answer

$$
\boxed{O}
$$

---

## Example 4 — Reverse Alphabet

### Question

**D : W :: G : ?**

### Pattern

D is position 4.

Reverse position:

$$
27-4=23
$$

Position 23 = W.

For G:

$$
27-7=20
$$

Position 20 = T.

### Answer

$$
\boxed{T}
$$

---

# 6. Letter Group Examples

## Example 5 — Each Letter +1

### Question

**ABC : BCD :: PQR : ?**

### Pattern

Compare:

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

$$
C\rightarrow D
$$

Each letter moves:

$$
+1
$$

Apply to PQR:

$$
P\rightarrow Q
$$

$$
Q\rightarrow R
$$

$$
R\rightarrow S
$$

### Answer

$$
\boxed{QRS}
$$

---

## Example 6 — Each Letter +2

### Question

**ABC : CDE :: MNO : ?**

### Pattern

$$
A\rightarrow C=+2
$$

$$
B\rightarrow D=+2
$$

$$
C\rightarrow E=+2
$$

Apply to MNO:

$$
M\rightarrow O
$$

$$
N\rightarrow P
$$

$$
O\rightarrow Q
$$

### Answer

$$
\boxed{OPQ}
$$

---

## Example 7 — Each Letter −1

### Question

**DEF : CDE :: HIJ : ?**

### Pattern

Each letter moves backward by 1:

$$
D\rightarrow C
$$

$$
E\rightarrow D
$$

$$
F\rightarrow E
$$

Apply to HIJ:

$$
H\rightarrow G
$$

$$
I\rightarrow H
$$

$$
J\rightarrow I
$$

### Answer

$$
\boxed{GHI}
$$

---

# 7. Medium Examples

## Example 8 — Reverse Order

### Question

**ABC : CBA :: DEF : ?**

### Pattern Recognition

The letters are reversed:

$$
ABC\rightarrow CBA
$$

Apply the same transformation:

$$
DEF\rightarrow FED
$$

### Answer

$$
\boxed{FED}
$$

---

## Example 9 — Swap Adjacent Letters

### Question

**ABCD : BADC :: EFGH : ?**

### Pattern Recognition

The first pair swaps adjacent letters:

$$
AB\rightarrow BA
$$

$$
CD\rightarrow DC
$$

Apply to EFGH:

$$
EF\rightarrow FE
$$

$$
GH\rightarrow HG
$$

### Answer

$$
\boxed{FEHG}
$$

---

## Example 10 — Alternate Shift

### Question

**ABCD : BDFH :: EFGH : ?**

### Pattern Recognition

Compare positions:

$$
A\rightarrow B=+1
$$

$$
B\rightarrow D=+2
$$

$$
C\rightarrow F=+3
$$

$$
D\rightarrow H=+4
$$

The shifts are:

$$
+1,+2,+3,+4
$$

Apply to EFGH:

$$
E+1=F
$$

$$
F+2=H
$$

$$
G+3=J
$$

$$
H+4=L
$$

### Answer

$$
\boxed{FHJL}
$$

---

# 8. Advanced Examples

## Example 11 — Alternate Positions

### Question

**ABCD : BADC :: EFGH : ?**

### Pattern Recognition

The transformation is:

$$
A\leftrightarrow B
$$

$$
C\leftrightarrow D
$$

So adjacent letters are exchanged.

Apply:

$$
E\leftrightarrow F
$$

$$
G\leftrightarrow H
$$

Therefore:

$$
\boxed{FEHG}
$$

---

## Example 12 — Increasing Shift

### Question

**ACE : BDF :: GIK : ?**

### Pattern Recognition

First pair:

$$
A\rightarrow B=+1
$$

$$
C\rightarrow D=+1
$$

$$
E\rightarrow F=+1
$$

So every letter moves +1.

Apply:

$$
G\rightarrow H
$$

$$
I\rightarrow J
$$

$$
K\rightarrow L
$$

### Answer

$$
\boxed{HJL}
$$

---

## Example 13 — Cyclic Transformation

### Question

**XYZ : YZA :: PQR : ?**

### Pattern Recognition

Each letter moves one step forward.

$$
X\rightarrow Y
$$

$$
Y\rightarrow Z
$$

$$
Z\rightarrow A
$$

Apply to PQR:

$$
P\rightarrow Q
$$

$$
Q\rightarrow R
$$

$$
R\rightarrow S
$$

### Answer

$$
\boxed{QRS}
$$

---

# 9. Position-Based Letter Analogy

Some questions require calculating the numerical relationship between letter positions.

## Example 14

### Question

**B : E :: H : ?**

### Pattern Recognition

Positions:

$$
B=2
$$

$$
E=5
$$

Difference:

$$
5-2=3
$$

Apply +3:

$$
H=8
$$

$$
8+3=11
$$

Position 11 = K.

### Answer

$$
\boxed{K}
$$

---

## Example 15 — Multiplication of Position

### Question

**B : D :: C : ?**

### Pattern Recognition

Positions:

$$
B=2
$$

$$
D=4
$$

Relationship:

$$
2\times2=4
$$

Apply to C:

$$
3\times2=6
$$

Position 6 = F.

### Answer

$$
\boxed{F}
$$

> [!warning]
> Position multiplication is less common than simple shifting. Use it only when the given pair clearly supports it and simpler rules do not.

---

# 10. Shortcuts

> [!tip]
> **Shortcut 1 — Compare positions first**

For:

**G : K**

calculate:

$$
11-7=4
$$

So the relationship is +4.

This is faster than manually counting.

---

> [!tip]
> **Shortcut 2 — Compare corresponding letters**

For:

**ABC : DEF**

check:

$$
A\rightarrow D=+3
$$

$$
B\rightarrow E=+3
$$

$$
C\rightarrow F=+3
$$

One common shift solves the entire pair.

---

> [!tip]
> **Shortcut 3 — Check reversal early**

If:

**ABC → CBA**

the answer is simply the reverse of the new group.

Do not calculate alphabet positions unnecessarily.

---

> [!tip]
> **Shortcut 4 — Check adjacent swapping**

For patterns such as:

$$
ABCD\rightarrow BADC
$$

think:

> Swap every adjacent pair.

---

> [!tip]
> **Shortcut 5 — Check cyclic movement near Z**

If the transformation reaches beyond Z, wrap to A.

Example:

$$
Z+2=B
$$

---

# 11. Recognition Tricks

## Pattern 1 — Fixed Forward Shift

> [!important]
> If every corresponding letter moves the same number of positions forward, think **Fixed Shift**.

Example:

$$
ABC\rightarrow DEF
$$

All letters move:

$$
+3
$$

---

## Pattern 2 — Fixed Backward Shift

> [!important]
> If every letter moves backward by the same amount, think **Backward Shift**.

Example:

$$
FGH\rightarrow CDE
$$

All letters move:

$$
-3
$$

---

## Pattern 3 — Reversal

> [!important]
> If the letters appear in reverse order, think **Reversal**.

Example:

$$
ABCD\rightarrow DCBA
$$

---

## Pattern 4 — Adjacent Swap

> [!important]
> If:

$$
ABCD\rightarrow BADC
$$

think:

> Swap neighboring letters.

---

## Pattern 5 — Increasing Shift

> [!important]
> If corresponding letters move by:

$$
+1,+2,+3,\ldots
$$

think **Increasing Shift**.

---

## Pattern 6 — Cyclic Shift

> [!important]
> If the transformation crosses Z, think **Cyclic Alphabet**.

Example:

$$
XYZ\rightarrow YZA
$$

---

## Pattern 7 — Position Arithmetic

> [!important]
> If ordinary shifting does not work, convert letters into numbers.

Example:

$$
C=3,\quad F=6
$$

Then investigate:

$$
3\rightarrow6
$$

---

# 12. Common Exam Patterns

> [!important] Must Master

1. Single-letter transformation
2. Fixed forward shift
3. Fixed backward shift
4. Reverse alphabet
5. Cyclic alphabet
6. Letter-group shift
7. Letter-group reversal
8. Adjacent letter swapping
9. Increasing shifts
10. Decreasing shifts
11. Alternate-position transformation
12. Alphabet position arithmetic
13. Vowel-based transformation
14. Consonant-based transformation
15. Mixed letter transformation

---

# 13. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Treating Letter Analogy as Word Analogy

Do not search for meanings.

For:

**ABC : DEF**

the relationship is positional, not semantic.

---

### Mistake 2 — Forgetting corresponding positions

For:

**ABC : DEF**

compare:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

not random letters.

---

### Mistake 3 — Ignoring order

**ABC → CBA**

is reversal.

It is not a simple alphabet shift.

---

### Mistake 4 — Forgetting cyclic movement

For:

$$
Y+3
$$

the answer is:

$$
B
$$

because:

$$
Y\rightarrow Z\rightarrow A\rightarrow B
$$

---

### Mistake 5 — Assuming every problem uses +1

Letter analogy can involve:

- +1
- +2
- −1
- reversal
- swapping
- increasing shifts
- position arithmetic

Always verify.

---

### Mistake 6 — Using a complicated rule too early

Start with:

1. Fixed shift
2. Reverse
3. Swap
4. Cyclic movement
5. Position arithmetic

Only then test more complicated patterns.

---

# 14. Formula Sheet

## Alphabet Position

$$
\boxed{A=1,\ldots,Z=26}
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

## Cyclic Forward Shift

$$
\boxed{P'=(P+k-1)\bmod26+1}
$$

## Cyclic Backward Shift

$$
\boxed{P'=(P-k-1)\bmod26+1}
$$

## General Analogy

$$
\boxed{f(A)=B\Rightarrow f(C)=D}
$$

## Increasing Shift

$$
\boxed{+1,+2,+3,\ldots}
$$

---

# 15. Quick Revision

> [!summary] One-Minute Revision

### Letter Analogy

$$
A:B::C:D
$$

Find the transformation from A to B and apply it to C.

### Check First

1. Fixed forward shift
2. Fixed backward shift
3. Reverse order
4. Adjacent swapping
5. Cyclic movement
6. Increasing/decreasing shift
7. Alphabet position arithmetic
8. Vowel/consonant pattern

### Essential Rule

$$
\boxed{\text{Same transformation, same position, same direction}}
$$

### Golden Memory Trick

**"Compare position-by-position before looking for a complicated pattern."**

# One-Line Recognition

**When letters or letter groups are given in analogy form, compare corresponding positions first and identify the simplest transformation connecting the two groups.**