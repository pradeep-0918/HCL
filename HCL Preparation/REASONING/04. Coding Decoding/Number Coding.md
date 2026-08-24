---
type: concept
subject: reasoning
topic: "Letter Coding"
parent: "04. Coding Decoding"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - coding-decoding
  - letter-coding
  - alphabet
  - pattern-recognition
  - logical-reasoning
  - hcl
wikilinks:
  - "[[04. Coding Decoding]]"
  - "[[Number Coding]]"
  - "[[Word Coding]]"
  - "[[Substitution Coding]]"
  - "[[Pattern Coding]]"
  - "[[Mixed Coding Decoding]]"
---

# Letter Coding

## 1. Core Concept

> [!summary]
> **Letter Coding** is a reasoning method in which letters of a word are transformed into other letters according to a specific rule. The task is to identify the coding rule and use it to encode or decode another word.

Example:

$$
CAT \rightarrow DBU
$$

Observe:

$$
C\rightarrow D
$$

$$
A\rightarrow B
$$

$$
T\rightarrow U
$$

Each letter moves:

$$
+1
$$

Therefore:

$$
DOG\rightarrow EPH
$$

### Core Intuition

Do not guess the coded word directly.

Convert each letter into its alphabet position:

$$
A=1,\ B=2,\ldots,Z=26
$$

Then identify the transformation.

The basic process is:

$$
\boxed{
\text{Letter}
\rightarrow
\text{Position}
\rightarrow
\text{Transformation}
\rightarrow
\text{Coded Letter}
}
$$

---

# 2. Basic Meaning

In Letter Coding, a word is changed using a predetermined relationship between its original letters and coded letters.

For example:

$$
APPLE\rightarrow BQQMF
$$

Compare each letter:

| Original | Position | Code | Position | Change |
|---|---:|---|---:|---:|
| A | 1 | B | 2 | $+1$ |
| P | 16 | Q | 17 | $+1$ |
| P | 16 | Q | 17 | $+1$ |
| L | 12 | M | 13 | $+1$ |
| E | 5 | F | 6 | $+1$ |

Therefore:

$$
\boxed{\text{Each letter is shifted by }+1}
$$

---

# 3. Main Formula

## Forward Shift

If a letter has position $p$ and moves $k$ positions forward:

$$
\boxed{p'=p+k}
$$

Example:

$$
C=3
$$

For $+2$:

$$
3+2=5=E
$$

Therefore:

$$
C\rightarrow E
$$

---

## Backward Shift

$$
\boxed{p'=p-k}
$$

Example:

$$
H=8
$$

For $-3$:

$$
8-3=5=E
$$

Therefore:

$$
H\rightarrow E
$$

---

## Cyclic Alphabet

If the shift goes beyond $Z$:

$$
\boxed{p'=((p+k-1)\bmod26)+1}
$$

Example:

$$
Z+1=A
$$

because:

$$
26+1\rightarrow1
$$

---

## Reverse Alphabet

The reverse alphabet relationship is:

$$
\boxed{p'=27-p}
$$

Therefore:

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

# 4. Alphabet Position Table

| Letter | Position | Reverse Pair |
|---|---:|---|
| A | 1 | Z |
| B | 2 | Y |
| C | 3 | X |
| D | 4 | W |
| E | 5 | V |
| F | 6 | U |
| G | 7 | T |
| H | 8 | S |
| I | 9 | R |
| J | 10 | Q |
| K | 11 | P |
| L | 12 | O |
| M | 13 | N |
| N | 14 | M |
| O | 15 | L |
| P | 16 | K |
| Q | 17 | J |
| R | 18 | I |
| S | 19 | H |
| T | 20 | G |
| U | 21 | F |
| V | 22 | E |
| W | 23 | D |
| X | 24 | C |
| Y | 25 | B |
| Z | 26 | A |

> [!tip]
> Memorize at least:
>
> $$A=1,\ E=5,\ J=10,\ O=15,\ T=20,\ Y=25$$
>
> These anchor points make alphabet-position calculations much faster.

---

# 5. Important Properties

1. Letter Coding is based on transformations between letters.
2. Every letter may follow the same shift.
3. Different letters may sometimes follow different shifts.
4. Coding may move letters forward.
5. Coding may move letters backward.
6. Coding may reverse the alphabet.
7. Coding may use alternating shifts.
8. Coding may use increasing or decreasing shifts.
9. The first and last letters may follow separate rules.
10. A word may be coded by reversing its letters.
11. Letter positions may be converted into numerical relationships.
12. Coding can combine multiple transformations.
13. The alphabet may be treated cyclically.
14. The same coding rule should explain all available examples.
15. Never assume a rule from only one letter if more evidence is available.

---

# 6. Pattern Recognition Framework

When you see a Letter Coding question, check the following in order:

$$
\boxed{
+1/-1
\rightarrow
\text{Fixed Shift}
\rightarrow
\text{Reverse Alphabet}
\rightarrow
\text{Reversal}
\rightarrow
\text{Alternating Shift}
\rightarrow
\text{Position-Based Rule}
\rightarrow
\text{Complex Rule}
}
$$

### Fast Questions to Ask

1. Is every letter shifted by the same amount?
2. Is the shift forward or backward?
3. Does the alphabet wrap around?
4. Is the alphabet reversed?
5. Is the word itself reversed?
6. Are odd and even letters treated differently?
7. Does the shift increase?
8. Does the shift decrease?
9. Are first and last letters treated differently?
10. Is there a relationship between letter positions?

---

# 7. Basic Examples

## Example 1 — Shift by +1

### Question

If:

$$
CAT\rightarrow DBU
$$

then encode:

$$
DOG
$$

### Identify the Pattern

$$
C\rightarrow D
$$

$$
A\rightarrow B
$$

$$
T\rightarrow U
$$

Therefore:

$$
+1
$$

### Encode DOG

$$
D\rightarrow E
$$

$$
O\rightarrow P
$$

$$
G\rightarrow H
$$

### Answer

$$
\boxed{EPH}
$$

---

# 8. Example 2 — Shift by +2

### Question

If:

$$
CAT\rightarrow ECV
$$

encode:

$$
DOG
$$

### Pattern

$$
C\rightarrow E
$$

$$
A\rightarrow C
$$

$$
T\rightarrow V
$$

Therefore:

$$
+2
$$

### DOG

$$
D+2=F
$$

$$
O+2=Q
$$

$$
G+2=I
$$

### Answer

$$
\boxed{FQI}
$$

---

# 9. Example 3 — Shift by -1

### Question

If:

$$
DOG\rightarrow CNF
$$

encode:

$$
CAT
$$

### Pattern

$$
D\rightarrow C
$$

$$
O\rightarrow N
$$

$$
G\rightarrow F
$$

Therefore:

$$
-1
$$

### CAT

$$
C\rightarrow B
$$

$$
A\rightarrow Z
$$

$$
T\rightarrow S
$$

### Answer

$$
\boxed{BZS}
$$

> [!important]
> When moving backward from $A$, use cyclic movement:

$$
A-1=Z
$$

---

# 10. Example 4 — Shift by +3

### Question

If:

$$
BAT\rightarrow EDW
$$

find the code for:

$$
DOG
$$

### Pattern

$$
B\rightarrow E
$$

$$
A\rightarrow D
$$

$$
T\rightarrow W
$$

Therefore:

$$
+3
$$

### DOG

$$
D+3=G
$$

$$
O+3=R
$$

$$
G+3=J
$$

### Answer

$$
\boxed{GRJ}
$$

---

# 11. Example 5 — Reverse Alphabet Coding

### Question

If:

$$
CAT\rightarrow XZG
$$

encode:

$$
DOG
$$

### Pattern

Use:

$$
A\leftrightarrow Z
$$

$$
B\leftrightarrow Y
$$

$$
C\leftrightarrow X
$$

Therefore:

$$
C\rightarrow X
$$

$$
A\rightarrow Z
$$

$$
T\rightarrow G
$$

### DOG

$$
D\rightarrow W
$$

$$
O\rightarrow L
$$

$$
G\rightarrow T
$$

### Answer

$$
\boxed{WLT}
$$

---

# 12. Example 6 — Reverse the Word

### Question

If:

$$
CAT\rightarrow TAC
$$

what is the code for:

$$
DOG
$$

The rule is simply:

$$
\boxed{\text{Reverse the order of letters}}
$$

Therefore:

$$
DOG\rightarrow GOD
$$

### Answer

$$
\boxed{GOD}
$$

> [!important]
> Do not confuse:
>
> **Reverse word**:
>
> $$CAT\rightarrow TAC$$
>
> with:
>
> **Reverse alphabet**:
>
> $$CAT\rightarrow XZG$$

---

# 13. Example 7 — Reverse Word + Shift

### Question

If:

$$
CAT\rightarrow UBD
$$

identify the rule.

First reverse:

$$
CAT\rightarrow TAC
$$

Then shift each letter:

$$
T+1=U
$$

$$
A+1=B
$$

$$
C+1=D
$$

Therefore:

$$
\boxed{\text{Reverse the word, then shift each letter by }+1}
$$

---

# 14. Example 8 — Shift by Different Amounts

### Question

Suppose:

$$
ABC\rightarrow BDF
$$

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

Therefore, the shift increases by position.

### Rule

$$
\boxed{\text{1st letter }+1,\ 2nd +2,\ 3rd +3}
$$

For:

$$
DOG
$$

we get:

$$
D+1=E
$$

$$
O+2=Q
$$

$$
G+3=J
$$

### Answer

$$
\boxed{EQJ}
$$

---

# 15. Example 9 — Decreasing Shift

### Question

Suppose:

$$
ABC\rightarrow ZYX
$$

This gives:

$$
A\rightarrow Z=-1
$$

$$
B\rightarrow Y=-3
$$

$$
C\rightarrow X=-5
$$

The shifts are:

$$
-1,-3,-5
$$

The shift decreases by $2$ each time.

> [!warning]
> Do not assume every coding question uses a fixed shift. Calculate the change for each position.

---

# 16. Example 10 — Alternating Shift

### Question

Suppose:

$$
ABCDE\rightarrow BZDCF
$$

Compare:

$$
A\rightarrow B=+1
$$

$$
B\rightarrow Z=-2
$$

$$
C\rightarrow D=+1
$$

$$
D\rightarrow C=-1
$$

This example does not produce a clean alternating rule.

> [!important]
> Always verify a suspected pattern against **every character** before using it.

---

# 17. Example 11 — Odd and Even Letters

Suppose:

$$
ABCDE\rightarrow BDFHJ
$$

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

$$
D\rightarrow H=+4
$$

$$
E\rightarrow J=+5
$$

The shift depends on the position.

### Rule

$$
\boxed{\text{Position }n\rightarrow +n}
$$

For:

$$
DOG
$$

$$
D+1=E
$$

$$
O+2=Q
$$

$$
G+3=J
$$

### Answer

$$
\boxed{EQJ}
$$

---

# 18. Example 12 — Position-Based Shift

### Question

If:

$$
ABCDE\rightarrow BDFJN
$$

identify the rule.

Positions:

| Original | Position | Code | Shift |
|---|---:|---|---:|
| A | 1 | B | $+1$ |
| B | 2 | D | $+2$ |
| C | 3 | F | $+3$ |
| D | 4 | H | $+4$ |
| E | 5 | J | $+5$ |

The pattern is:

$$
\boxed{p'=p+n}
$$

where $n$ is the letter's position in the word.

---

# 19. Example 13 — Alternate +1 and -1

### Question

Suppose:

$$
ABCDE\rightarrow BAZDF
$$

Check:

$$
A\rightarrow B=+1
$$

$$
B\rightarrow A=-1
$$

$$
C\rightarrow D=+1
$$

$$
D\rightarrow C=-1
$$

$$
E\rightarrow F=+1
$$

Therefore:

$$
\boxed{+1,-1,+1,-1,+1}
$$

This is an alternating transformation.

---

# 20. Example 14 — Alternate +2 and -2

Suppose:

$$
ABCDE\rightarrow CYEW G
$$

Ignoring spacing:

$$
ABCDE\rightarrow CYEGW
$$

Check:

$$
A+2=C
$$

$$
B-3=Y
$$

This does not fit the claimed pattern.

> [!warning]
> In real aptitude questions, do not force a rule simply because the first two letters appear to match.

The correct rule must explain the entire word.

---

# 21. Example 15 — First Half Forward, Second Half Backward

Suppose a coding rule transforms a word by:

- First half: shift forward
- Second half: shift backward

For a six-letter word:

$$
ABCDEF
$$

the transformation may be:

$$
A+1,\ B+1,\ C+1,\ D-1,\ E-1,\ F-1
$$

giving:

$$
BCB C D E
$$

The exact output depends on the specified rule.

> [!important]
> Such questions must be solved position by position.

---

# 22. Example 16 — First Letter and Last Letter Swap

### Question

If:

$$
CAT\rightarrow TAC
$$

the transformation is:

$$
\boxed{\text{Reverse the entire word}}
$$

But another possible rule could swap only the first and last letters.

For:

$$
CART
$$

swapping first and last gives:

$$
TARC
$$

while reversing gives:

$$
TRAC
$$

### Recognition

> [!important]
> Check whether **all letters reverse** or only selected positions exchange.

---

# 23. Example 17 — Pairwise Swapping

Suppose:

$$
ABCDEFGH
$$

is transformed by swapping adjacent pairs:

$$
AB\rightarrow BA
$$

$$
CD\rightarrow DC
$$

$$
EF\rightarrow FE
$$

$$
GH\rightarrow HG
$$

Therefore:

$$
ABCDEFGH\rightarrow BADCFEHG
$$

### Rule

$$
\boxed{\text{Swap every adjacent pair}}
$$

---

# 24. Example 18 — Pair Reversal

### Question

Encode:

$$
COMPUTER
$$

using adjacent-pair swapping.

Break into pairs:

$$
CO\ MP\ UT\ ER
$$

Swap each pair:

$$
OC\ PM\ TU\ RE
$$

Therefore:

$$
\boxed{OCPMTURE}
$$

---

# 25. Example 19 — Alphabetic Mirror Coding

### Question

Encode:

$$
DOG
$$

using reverse alphabet coding.

$$
D=4
$$

Reverse:

$$
27-4=23=W
$$

$$
O=15
$$

$$
27-15=12=L
$$

$$
G=7
$$

$$
27-7=20=T
$$

### Answer

$$
\boxed{WLT}
$$

---

# 26. Example 20 — Cyclic Shift

### Question

If each letter moves $+2$, encode:

$$
YAZ
$$

### Solution

$$
Y+2=A
$$

because:

$$
25+2=27\rightarrow1
$$

$$
A+2=C
$$

$$
Z+2=B
$$

Therefore:

$$
\boxed{ACB}
$$

> [!important]
> When a shift crosses $Z$, continue from $A$.

---

# 27. Example 21 — Backward Cyclic Shift

Encode:

$$
ABC
$$

using:

$$
-2
$$

### Solution

$$
A-2=Y
$$

$$
B-2=Z
$$

$$
C-2=A
$$

### Answer

$$
\boxed{YZA}
$$

---

# 28. Example 22 — Increasing Shift

Suppose:

$$
ABC\rightarrow BDF
$$

The shifts are:

$$
+1,+2,+3
$$

Encode:

$$
DOG
$$

### Solution

$$
D+1=E
$$

$$
O+2=Q
$$

$$
G+3=J
$$

### Answer

$$
\boxed{EQJ}
$$

---

# 29. Example 23 — Decreasing Shift

Suppose the rule is:

$$
-1,-2,-3,-4,\ldots
$$

Encode:

$$
ABCDE
$$

### Solution

$$
A-1=Z
$$

$$
B-2=Z
$$

$$
C-3=Z
$$

$$
D-4=Z
$$

$$
E-5=Z
$$

### Answer

$$
\boxed{ZZZZZ}
$$

This demonstrates that position-based shifts may create unexpected repeated letters.

---

# 30. Example 24 — Alphabet Position Difference

Suppose:

$$
CAT\rightarrow 3,1,20
$$

The code directly represents alphabet positions.

For:

$$
DOG
$$

we have:

$$
D=4
$$

$$
O=15
$$

$$
G=7
$$

### Answer

$$
\boxed{4,15,7}
$$

> [!important]
> This is technically a positional representation rather than a letter substitution, but it is a common bridge between Letter Coding and Number Coding.

---

# 31. Example 25 — Reverse Positions

Encode:

$$
DOG
$$

using:

$$
27-p
$$

### Solution

$$
D=4
$$

$$
27-4=23=W
$$

$$
O=15
$$

$$
27-15=12=L
$$

$$
G=7
$$

$$
27-7=20=T
$$

### Answer

$$
\boxed{WLT}
$$

---

# 32. Example 26 — Position Swapping

Suppose:

$$
ABCDE\rightarrow EDCBA
$$

The word is completely reversed.

For:

$$
TRAIN
$$

reverse the letters:

$$
N I A R T
$$

### Answer

$$
\boxed{NIART}
$$

---

# 33. Example 27 — First and Second Half Exchange

Suppose:

$$
ABCDEFGH
$$

is split into:

$$
ABCD|EFGH
$$

Exchange the halves:

$$
EFGH|ABCD
$$

Therefore:

$$
\boxed{EFGHABCD}
$$

This is a structural coding rule.

---

# 34. Example 28 — Odd and Even Positions Exchange

Suppose:

$$
ABCDEFGH
$$

Odd positions:

$$
A,C,E,G
$$

Even positions:

$$
B,D,F,H
$$

If the code is formed as odd positions followed by even positions:

$$
ACEGBDFH
$$

### Answer

$$
\boxed{ACEGBDFH}
$$

> [!important]
> Position-based rearrangement is different from letter substitution.

---

# 35. Example 29 — Alphabet Shift + Reversal

Suppose the rule is:

1. Shift every letter by $+1$
2. Reverse the resulting word

Encode:

$$
CAT
$$

### Step 1 — Shift

$$
CAT\rightarrow DBU
$$

### Step 2 — Reverse

$$
DBU\rightarrow UBD
$$

### Answer

$$
\boxed{UBD}
$$

---

# 36. Example 30 — Reverse + Alphabet Shift

Suppose the rule is:

1. Reverse the word
2. Shift each letter by $+1$

Encode:

$$
CAT
$$

### Step 1

$$
CAT\rightarrow TAC
$$

### Step 2

$$
T+1=U
$$

$$
A+1=B
$$

$$
C+1=D
$$

### Answer

$$
\boxed{UBD}
$$

In this particular example, both operation orders produce the same result because a uniform shift commutes with reversal.

> [!important]
> The order of operations matters for some transformations, so always follow the stated rule exactly.

---

# 37. Example 31 — Alternating Forward and Reverse Alphabet

Suppose:

- Odd-position letters use $+1$
- Even-position letters use reverse alphabet coding

Encode:

$$
ABCD
$$

### A

$$
A+1=B
$$

### B

Reverse of $B$:

$$
Y
$$

### C

$$
C+1=D
$$

### D

Reverse of $D$:

$$
W
$$

### Answer

$$
\boxed{BYDW}
$$

---

# 38. Example 32 — Different Shift for Different Positions

Suppose the rule is:

$$
+1,+2,+3,+4
$$

Encode:

$$
MATH
$$

### M

$$
M+1=N
$$

### A

$$
A+2=C
$$

### T

$$
T+3=W
$$

### H

$$
H+4=L
$$

### Answer

$$
\boxed{NCWL}
$$

---

# 39. Advanced Pattern — Increasing Shift with Wraparound

Encode:

$$
WXYZ
$$

using:

$$
+1,+2,+3,+4
$$

### W

$$
W+1=X
$$

### X

$$
X+2=Z
$$

### Y

$$
Y+3=B
$$

### Z

$$
Z+4=D
$$

### Answer

$$
\boxed{XZBD}
$$

---

# 40. Advanced Pattern — Alternating Direction

Suppose the rule is:

$$
+2,-2,+2,-2
$$

Encode:

$$
MATH
$$

### M

$$
M+2=O
$$

### A

$$
A-2=Y
$$

### T

$$
T+2=V
$$

### H

$$
H-2=F
$$

### Answer

$$
\boxed{OYVF}
$$

---

# 41. Advanced Pattern — Increasing and Decreasing Shifts

Suppose the shifts are:

$$
+1,+2,-1,-2
$$

Encode:

$$
CODE
$$

### C

$$
C+1=D
$$

### O

$$
O+2=Q
$$

### D

$$
D-1=C
$$

### E

$$
E-2=C
$$

### Answer

$$
\boxed{DQCC}
$$

---

# 42. Advanced Pattern — Letter Position Transformation

Suppose the new position is:

$$
p'=2p
$$

for positions that remain within the alphabet.

Encode:

$$
ABC
$$

### A

$$
1\times2=2=B
$$

### B

$$
2\times2=4=D
$$

### C

$$
3\times2=6=F
$$

### Answer

$$
\boxed{BDF}
$$

> [!warning]
> If multiplication produces a value above $26$, determine whether the question intends cyclic treatment or another rule. Do not assume automatically.

---

# 43. Advanced Pattern — Position Complement

Suppose:

$$
p'=27-p
$$

Encode:

$$
MATH
$$

### M

$$
13\rightarrow14=N
$$

### A

$$
1\rightarrow26=Z
$$

### T

$$
20\rightarrow7=G
$$

### H

$$
8\rightarrow19=S
$$

### Answer

$$
\boxed{NZGS}
$$

---

# 44. How to Recognize Letter Coding Patterns

## Pattern 1 — Every Letter Moves the Same Amount

> [!important]
> If:

$$
CAT\rightarrow DBU
$$

check:

$$
+1,+1,+1
$$

Think:

$$
\boxed{\text{Uniform shift}}
$$

---

## Pattern 2 — Every Letter Moves Backward

> [!important]
> If:

$$
DOG\rightarrow CNF
$$

think:

$$
\boxed{-1}
$$

---

## Pattern 3 — Letters Become Their Opposites

> [!important]
> If:

$$
A\rightarrow Z,\ B\rightarrow Y,\ C\rightarrow X
$$

think:

$$
\boxed{27-p}
$$

---

## Pattern 4 — Word Appears Backward

> [!important]
> If:

$$
CAT\rightarrow TAC
$$

think:

$$
\boxed{\text{Reverse order}}
$$

---

## Pattern 5 — Shift Changes by Position

> [!important]
> If:

$$
A\rightarrow B
$$

$$
B\rightarrow D
$$

$$
C\rightarrow F
$$

think:

$$
\boxed{+1,+2,+3}
$$

---

## Pattern 6 — Alternating Shifts

> [!important]
> If shifts look like:

$$
+1,-1,+1,-1
$$

think:

$$
\boxed{\text{Alternating transformation}}
$$

---

## Pattern 7 — Pairwise Exchange

> [!important]
> If:

$$
ABCD\rightarrow BADC
$$

think:

$$
\boxed{\text{Adjacent pair swapping}}
$$

---

## Pattern 8 — Odd-Even Rearrangement

> [!important]
> If:

$$
ABCDEFGH\rightarrow ACEGBDFH
$$

think:

$$
\boxed{\text{Odd positions followed by even positions}}
$$

---

## Pattern 9 — Cyclic Shift

> [!important]
> If:

$$
Z\rightarrow A
$$

the alphabet is being treated cyclically.

---

## Pattern 10 — Multiple Transformations

> [!important]
> If one simple rule fails, test:

$$
\boxed{
\text{Reverse}
+
\text{Shift}
}
$$

or:

$$
\boxed{
\text{Position Change}
+
\text{Letter Substitution}
}
$$

---

# 45. Shortcuts

> [!tip]
> **Shortcut 1 — Memorize anchor positions**

Remember:

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
O=15
$$

$$
T=20
$$

$$
Y=25
$$

This reduces counting time.

---

> [!tip]
> **Shortcut 2 — Calculate the shift from the first two letters**

If:

$$
C\rightarrow F
$$

then:

$$
+3
$$

Immediately test whether the same shift works for the remaining letters.

---

> [!tip]
> **Shortcut 3 — Use position differences**

For:

$$
H\rightarrow K
$$

calculate:

$$
11-8=3
$$

Therefore:

$$
+3
$$

---

> [!tip]
> **Shortcut 4 — Memorize reverse pairs**

Useful pairs:

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

---

> [!tip]
> **Shortcut 5 — Check word reversal**

If the coded word contains the same letters in reverse order, no alphabet calculation is needed.

---

> [!tip]
> **Shortcut 6 — For long words, create a shift row**

Example:

$$
A\ B\ C\ D\ E
$$

Code:

$$
B\ D\ F\ H\ J
$$

Shifts:

$$
+1,+2,+3,+4,+5
$$

The rule becomes immediately visible.

---

> [!tip]
> **Shortcut 7 — Check odd and even positions**

If shifts look irregular:

$$
1^{st},3^{rd},5^{th}
$$

and:

$$
2^{nd},4^{th},6^{th}
$$

may follow separate rules.

---

> [!tip]
> **Shortcut 8 — Use cyclic movement for boundary letters**

Remember:

$$
Z+1=A
$$

$$
A-1=Z
$$

This avoids unnecessary counting.

---

# 46. Common Exam Patterns

> [!important] Must Master

### Basic Letter Transformation

1. Shift by $+1$
2. Shift by $-1$
3. Shift by $+2$
4. Shift by $-2$
5. Fixed positive shift
6. Fixed negative shift

### Alphabet Patterns

7. Reverse alphabet
8. Cyclic alphabet
9. Alphabet position mapping
10. Complementary positions

### Word Patterns

11. Reverse word
12. Swap first and last letters
13. Swap adjacent letters
14. Pairwise reversal
15. First-half/second-half exchange
16. Odd-even rearrangement

### Position-Based Patterns

17. Increasing shift
18. Decreasing shift
19. Alternating shift
20. Position-dependent shift
21. Different shift for odd/even positions

### Advanced Patterns

22. Shift + reverse
23. Reverse + shift
24. Multiple transformations
25. Inner/outer position relationships
26. Cyclic position transformation
27. Mathematical transformation of alphabet positions
28. Complex mixed coding

---

# 47. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Assuming +1 immediately

For:

$$
ABC\rightarrow BDF
$$

the shifts are:

$$
+1,+2,+3
$$

not:

$$
+1
$$

---

### Mistake 2 — Confusing reverse alphabet with reverse word

Reverse alphabet:

$$
CAT\rightarrow XZG
$$

Reverse word:

$$
CAT\rightarrow TAC
$$

They are completely different.

---

### Mistake 3 — Forgetting cyclic movement

$$
Z+1=A
$$

and:

$$
A-1=Z
$$

---

### Mistake 4 — Checking only one letter

A rule is valid only if it explains the complete example.

---

### Mistake 5 — Ignoring position

Sometimes the first letter changes by $+1$, the second by $+2$, and so on.

---

### Mistake 6 — Ignoring word order

A coding rule may rearrange positions rather than change letters.

---

### Mistake 7 — Confusing substitution with rearrangement

Example:

$$
CAT\rightarrow DBU
$$

is substitution.

Example:

$$
CAT\rightarrow TAC
$$

is rearrangement.

---

### Mistake 8 — Forgetting zero-based programming logic

In aptitude, alphabet positions are usually:

$$
A=1,\ldots,Z=26
$$

Do not accidentally use:

$$
A=0
$$

unless the question explicitly defines it.

---

### Mistake 9 — Applying a rule beyond its evidence

If only one example is given, several rules may fit.

Use all provided information and the answer choices where applicable.

---

### Mistake 10 — Overcomplicating

If every letter moves $+2$, use $+2$.

Do not invent an advanced rule without evidence.

---

# 48. Advanced Pattern Recognition Table

| Observed Pattern | Likely Rule |
|---|---|
| $A\rightarrow B,\ B\rightarrow C$ | $+1$ |
| $A\rightarrow C,\ B\rightarrow D$ | $+2$ |
| $D\rightarrow B,\ E\rightarrow C$ | $-2$ |
| $A\rightarrow Z,\ B\rightarrow Y$ | Reverse alphabet |
| $CAT\rightarrow TAC$ | Reverse word |
| $ABCD\rightarrow BADC$ | Adjacent swap |
| $ABCDE\rightarrow BDFHJ$ | Increasing shift |
| Shifts $+1,-1,+1,-1$ | Alternating shift |
| $Z\rightarrow A$ | Cyclic alphabet |
| Odd letters grouped first | Odd-even rearrangement |
| First and last exchange | Position swapping |
| Number represents letter | Alphabet-position coding |

---

# 49. Exam-Speed Solving Strategy

For a typical Letter Coding question:

### 5-Second Scan

Check:

$$
\boxed{+1?}
$$

$$
\boxed{-1?}
$$

$$
\boxed{\text{Fixed shift?}}
$$

$$
\boxed{\text{Reverse alphabet?}}
$$

$$
\boxed{\text{Reverse word?}}
$$

### 10-Second Scan

If none works:

$$
\boxed{\text{Alternating shift}}
$$

$$
\boxed{\text{Position-based shift}}
$$

$$
\boxed{\text{Pair swapping}}
$$

$$
\boxed{\text{Odd-even rearrangement}}
$$

### Advanced

Then test:

$$
\boxed{\text{Multiple transformations}}
$$

---

# 50. Mini Practice Set

## Question 1

If:

$$
CAT\rightarrow DBU
$$

find the code for:

$$
BAT
$$

Pattern:

$$
+1
$$

Answer:

$$
\boxed{CBU}
$$

---

## Question 2

If:

$$
DOG\rightarrow CNF
$$

find the code for:

$$
CAT
$$

Pattern:

$$
-1
$$

Answer:

$$
\boxed{BZS}
$$

---

## Question 3

Using reverse alphabet coding, encode:

$$
BAT
$$

$$
B\rightarrow Y
$$

$$
A\rightarrow Z
$$

$$
T\rightarrow G
$$

Answer:

$$
\boxed{YZG}
$$

---

## Question 4

Reverse:

$$
COMPUTER
$$

Answer:

$$
\boxed{RETUPMOC}
$$

---

## Question 5

Using a $+2$ shift, encode:

$$
XYZ
$$

$$
X+2=Z
$$

$$
Y+2=A
$$

$$
Z+2=B
$$

Answer:

$$
\boxed{ZAB}
$$

---

# 51. Formula Sheet

## Alphabet Position

$$
\boxed{A=1,\ldots,Z=26}
$$

## Forward Shift

$$
\boxed{p'=p+k}
$$

## Backward Shift

$$
\boxed{p'=p-k}
$$

## Cyclic Shift

$$
\boxed{p'=((p+k-1)\bmod26)+1}
$$

## Reverse Alphabet

$$
\boxed{p'=27-p}
$$

## Constant Difference

$$
\boxed{k=p'-p}
$$

## Increasing Shift

$$
\boxed{k_n=n}
$$

## Decreasing Shift

$$
\boxed{k_n=k_1-(n-1)d}
$$

## Reverse Word

$$
\boxed{C_1C_2\ldots C_n\rightarrow C_n\ldots C_2C_1}
$$

## Mirror Pair

$$
\boxed{p_1+p_2=27}
$$

---

# 52. Quick Revision

> [!summary] One-Minute Revision

## Letter Coding

The master approach:

$$
\boxed{
\text{Convert}
\rightarrow
\text{Compare}
\rightarrow
\text{Find Shift}
\rightarrow
\text{Apply}
}
$$

### Always Remember

$$
A=1,\ldots,Z=26
$$

### First Check

$$
+1,\ -1
$$

### Second Check

$$
\text{Fixed shift}
$$

### Third Check

$$
\text{Reverse alphabet}
$$

### Fourth Check

$$
\text{Reverse word}
$$

### Fifth Check

$$
\text{Cyclic movement}
$$

### Sixth Check

$$
\text{Alternating shifts}
$$

### Seventh Check

$$
\text{Position-based shifts}
$$

### Eighth Check

$$
\text{Pair/position rearrangement}
$$

### Ninth Check

$$
\text{Multiple transformations}
$$

### Most Important Patterns

$$
CAT\rightarrow DBU
$$

means:

$$
\boxed{+1}
$$

$$
CAT\rightarrow ECV
$$

means:

$$
\boxed{+2}
$$

$$
CAT\rightarrow XZG
$$

means:

$$
\boxed{\text{Reverse alphabet}}
$$

$$
CAT\rightarrow TAC
$$

means:

$$
\boxed{\text{Reverse word}}
$$

$$
ABCDE\rightarrow BDFHJ
$$

means:

$$
\boxed{+1,+2,+3,+4,+5}
$$

$$
Z+1=A
$$

means:

$$
\boxed{\text{Cyclic alphabet}}
$$

### Golden Memory Trick

**"Convert letters to positions, find the transformation, verify it on every letter, and only then encode the new word."**

# One-Line Recognition

**When a word is converted into another word, compare corresponding letters using alphabet positions and first test fixed shifts, reverse alphabet, word reversal, cyclic movement, and position-based transformations.**