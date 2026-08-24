---
type: concept
subject: reasoning
topic: "Pattern Coding"
parent: "04. Coding Decoding"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - coding-decoding
  - pattern-coding
  - pattern-recognition
  - logical-reasoning
  - alphabet-pattern
  - number-pattern
  - hcl
wikilinks:
  - "[[04. Coding Decoding]]"
  - "[[Letter Coding]]"
  - "[[Number Coding]]"
  - "[[Word Coding]]"
  - "[[Substitution Coding]]"
  - "[[Chinese Coding]]"
  - "[[Matrix Coding]]"
  - "[[Mixed Coding Decoding]]"
---

# Pattern Coding

## 1. Core Concept

> [!summary]
> **Pattern Coding** is a coding-decoding method in which letters, numbers, words, or symbols are transformed according to a specific repeating, positional, arithmetic, or structural pattern.

The main objective is to discover:

$$
\boxed{\text{Original} \rightarrow \text{Pattern} \rightarrow \text{Code}}
$$

Unlike direct substitution, Pattern Coding usually requires you to **discover the transformation**.

For example:

$$
A\rightarrow C
$$

$$
B\rightarrow E
$$

$$
C\rightarrow G
$$

The shifts are:

$$
+2,\ +3,\ +4
$$

So the pattern itself is increasing.

The next transformation would be:

$$
+5
$$

Therefore:

$$
D\rightarrow I
$$

---

# 2. Basic Meaning

Pattern Coding uses a systematic rule to transform input into output.

The pattern may involve:

- Constant addition
- Constant subtraction
- Increasing shifts
- Decreasing shifts
- Alternating shifts
- Multiplication
- Division
- Position-based operations
- Odd/even positions
- Reverse order
- Alphabet reversal
- Circular alphabet movement
- Number sequences
- Prime numbers
- Squares
- Cubes
- Fibonacci-like patterns
- Combination of two or more rules

The most important skill is:

$$
\boxed{\text{Recognize the transformation quickly}}
$$

---

# 3. Main Formula

There is no single formula for Pattern Coding.

Common forms are:

### Constant Shift

$$
\boxed{p'=p+k}
$$

### Increasing Shift

$$
\boxed{p'=p+(k+i)}
$$

### Decreasing Shift

$$
\boxed{p'=p+(k-i)}
$$

### Multiplicative Coding

$$
\boxed{x'=kx}
$$

### Position-Based Coding

$$
\boxed{x'=x+f(i)}
$$

where $i$ is the position of the character.

### Alternating Pattern

$$
\boxed{+a,-b,+a,-b,\ldots}
$$

### Reverse Alphabet

$$
\boxed{p'=27-p}
$$

### Reverse Order

$$
\boxed{C_1C_2\ldots C_n\rightarrow C_n\ldots C_2C_1}
$$

---

# 4. Important Properties

1. Pattern Coding depends on a discoverable rule.
2. The rule may apply to letters, numbers, words, or symbols.
3. The pattern may be constant or changing.
4. Position often determines the transformation.
5. The same operation may repeat periodically.
6. Multiple operations may alternate.
7. Alphabet coding usually uses $A=1,\ldots,Z=26$.
8. Alphabet operations may wrap around after Z.
9. Number coding may use arithmetic sequences.
10. Structural patterns may rearrange positions.
11. The simplest rule should always be tested first.
12. The rule must explain all given examples.
13. Pattern Coding often combines concepts from Letter and Number Coding.
14. Pattern recognition is more important than calculation speed.
15. Complex-looking patterns are often combinations of simple patterns.

---

# 5. Pattern Coding vs Other Coding Types

| Type | Main Idea | Example |
|---|---|---|
| Letter Coding | Transform individual letters | $A\rightarrow D$ |
| Number Coding | Convert into numerical values | $CAT\rightarrow24$ |
| Word Coding | Transform complete words | $DOG\rightarrowANIMAL$ |
| Substitution Coding | Artificial replacement | $DOG\rightarrowCAT$ |
| Pattern Coding | Apply systematic transformation | $A\rightarrow C,\ B\rightarrow E$ |
| Chinese Coding | Decode artificial word codes | `red flower = ka ti` |
| Matrix Coding | Use row/column or grid mapping | Grid-based code |

---

# 6. Major Types of Pattern Coding

| Pattern Type | Example |
|---|---|
| Constant Shift | $+3,+3,+3$ |
| Constant Difference | $-2,-2,-2$ |
| Increasing Shift | $+1,+2,+3$ |
| Decreasing Shift | $+5,+4,+3$ |
| Alternating Shift | $+2,-1,+2,-1$ |
| Multiplication | $\times2$ |
| Division | $\div2$ |
| Position-Based | $+1,+2,+3$ |
| Reverse Alphabet | $A\rightarrow Z$ |
| Reverse Position | $ABC\rightarrow CBA$ |
| Odd-Even Pattern | Odd positions treated differently |
| Pair Pattern | Letters processed in pairs |
| Prime Pattern | $+2,+3,+5,+7$ |
| Square Pattern | $+1,+4,+9$ |
| Cube Pattern | $+1,+8,+27$ |
| Fibonacci Pattern | $1,1,2,3,5,\ldots$ |
| Mixed Arithmetic | Multiple operations |
| Structural Pattern | Rearrangement of positions |

---

# 7. Alphabet Position Table

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

---

# 8. Basic Pattern — Constant Shift

## Example 1

### Question

If:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

find the code for:

$$
D
$$

### Pattern

$$
A+3=D
$$

$$
B+3=E
$$

$$
C+3=F
$$

Therefore:

$$
D+3=G
$$

### Answer

$$
\boxed{G}
$$

---

# 9. Example 2 — Constant $+2$ Shift

Encode:

$$
CAT
$$

using a $+2$ shift.

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
\boxed{ECV}
$$

---

# 10. Example 3 — Constant $-2$ Shift

Encode:

$$
DOG
$$

using $-2$.

$$
D\rightarrow B
$$

$$
O\rightarrow M
$$

$$
G\rightarrow E
$$

Therefore:

$$
\boxed{BME}
$$

---

# 11. Circular Alphabet Pattern

If the shift goes beyond Z, continue from A.

For example:

$$
Y+3
$$

Move:

$$
Y\rightarrow Z\rightarrow A\rightarrow B
$$

Therefore:

$$
\boxed{B}
$$

---

# 12. Example 4 — Circular Shift

Encode:

$$
XYZ
$$

using $+3$.

$$
X\rightarrow A
$$

$$
Y\rightarrow B
$$

$$
Z\rightarrow C
$$

### Answer

$$
\boxed{ABC}
$$

---

# 13. Increasing Shift Pattern

## Example 5

Suppose:

$$
A\rightarrow B
$$

$$
B\rightarrow D
$$

$$
C\rightarrow F
$$

Find the code for $D$.

### Step 1 — Find shifts

$$
A\rightarrow B=+1
$$

$$
B\rightarrow D=+2
$$

$$
C\rightarrow F=+3
$$

The shift increases by $1$.

Next shift:

$$
+4
$$

Therefore:

$$
D+4=H
$$

### Answer

$$
\boxed{H}
$$

---

# 14. Example 6 — Increasing Shift in a Word

Encode:

$$
CAT
$$

using shifts:

$$
+1,+2,+3
$$

### C

$$
C+1=D
$$

### A

$$
A+2=C
$$

### T

$$
T+3=W
$$

### Answer

$$
\boxed{DCW}
$$

---

# 15. Decreasing Shift Pattern

## Example 7

Suppose the shifts are:

$$
+5,+4,+3,+2,+1
$$

Encode:

$$
ABCDE
$$

### A

$$
A+5=F
$$

### B

$$
B+4=F
$$

### C

$$
C+3=F
$$

### D

$$
D+2=F
$$

### E

$$
E+1=F
$$

### Answer

$$
\boxed{FFFFF}
$$

> [!important]
> Different original letters can produce the same code when the position-based shifts are designed that way.

---

# 16. Alternating Pattern

## Example 8

Suppose:

$$
+2,-1,+2,-1,\ldots
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
A-1=Z
$$

### T

$$
T+2=V
$$

### H

$$
H-1=G
$$

### Answer

$$
\boxed{OZVG}
$$

---

# 17. Example 9 — Alternating $+1,-1$

Encode:

$$
ABCDE
$$

using:

$$
+1,-1,+1,-1,+1
$$

### Solution

$$
A+1=B
$$

$$
B-1=A
$$

$$
C+1=D
$$

$$
D-1=C
$$

$$
E+1=F
$$

### Answer

$$
\boxed{BADCF}
$$

---

# 18. Position-Based Pattern

## Example 10

Each letter is shifted by its position:

$$
+1,+2,+3,+4,\ldots
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

# 19. Reverse Position Pattern

Suppose the word has 4 letters and shifts are:

$$
+4,+3,+2,+1
$$

Encode:

$$
MATH
$$

### M

$$
M+4=Q
$$

### A

$$
A+3=D
$$

### T

$$
T+2=V
$$

### H

$$
H+1=I
$$

### Answer

$$
\boxed{QDVI}
$$

---

# 20. Reverse Alphabet Pattern

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
CAT
$$

becomes:

$$
C\rightarrow X
$$

$$
A\rightarrow Z
$$

$$
T\rightarrow G
$$

### Answer

$$
\boxed{XZG}
$$

---

# 21. Example 11 — Reverse Alphabet Recognition

Suppose:

$$
A\rightarrow Z
$$

$$
B\rightarrow Y
$$

$$
C\rightarrow X
$$

Find the code for:

$$
DOG
$$

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

# 22. Multiplication Pattern

Pattern Coding can also operate on numbers.

## Example 12

Suppose:

$$
2\rightarrow4
$$

$$
3\rightarrow6
$$

$$
4\rightarrow8
$$

The rule is:

$$
\times2
$$

Therefore:

$$
5\rightarrow10
$$

### Answer

$$
\boxed{10}
$$

---

# 23. Division Pattern

## Example 13

Suppose:

$$
20\rightarrow10
$$

$$
16\rightarrow8
$$

$$
12\rightarrow6
$$

The rule is:

$$
\div2
$$

Therefore:

$$
18\rightarrow9
$$

### Answer

$$
\boxed{9}
$$

---

# 24. Mixed Arithmetic Pattern

## Example 14

Suppose:

$$
2\rightarrow5
$$

$$
3\rightarrow8
$$

$$
4\rightarrow11
$$

Check:

$$
2(3)-1=5
$$

$$
3(3)-1=8
$$

$$
4(3)-1=11
$$

Therefore:

$$
\boxed{f(n)=3n-1}
$$

For:

$$
5
$$

$$
3(5)-1=14
$$

### Answer

$$
\boxed{14}
$$

---

# 25. Increasing Difference Pattern

## Example 15

Suppose:

$$
1\rightarrow2
$$

$$
2\rightarrow4
$$

$$
3\rightarrow7
$$

$$
4\rightarrow11
$$

Differences:

$$
+1,+2,+3,+4
$$

Therefore next:

$$
11+5=16
$$

### Answer

$$
\boxed{16}
$$

---

# 26. Square Pattern

## Example 16

Suppose:

$$
1\rightarrow1
$$

$$
2\rightarrow4
$$

$$
3\rightarrow9
$$

$$
4\rightarrow16
$$

The pattern is:

$$
n^2
$$

Therefore:

$$
5\rightarrow25
$$

### Answer

$$
\boxed{25}
$$

---

# 27. Cube Pattern

## Example 17

Suppose:

$$
1\rightarrow1
$$

$$
2\rightarrow8
$$

$$
3\rightarrow27
$$

$$
4\rightarrow64
$$

The pattern is:

$$
n^3
$$

Therefore:

$$
5\rightarrow125
$$

### Answer

$$
\boxed{125}
$$

---

# 28. Prime Number Pattern

## Example 18

Suppose the shifts are:

$$
+2,+3,+5,+7,\ldots
$$

These are consecutive prime numbers.

Encode:

$$
ABCDE
$$

### A

$$
A+2=C
$$

### B

$$
B+3=E
$$

### C

$$
C+5=H
$$

### D

$$
D+7=K
$$

For the fifth letter, the next prime is:

$$
11
$$

Therefore:

$$
E+11=P
$$

### Answer

$$
\boxed{CEHKP}
$$

---

# 29. Fibonacci Pattern

The Fibonacci sequence is:

$$
1,1,2,3,5,8,\ldots
$$

Suppose these values are used as shifts.

For:

$$
ABCDE
$$

use:

$$
+1,+1,+2,+3,+5
$$

Then:

$$
A+1=B
$$

$$
B+1=C
$$

$$
C+2=E
$$

$$
D+3=G
$$

$$
E+5=J
$$

### Answer

$$
\boxed{BCEGJ}
$$

---

# 30. Pair-Based Pattern

## Example 19

Suppose letters are processed in pairs:

$$
AB\rightarrow BA
$$

$$
CD\rightarrow DC
$$

$$
EF\rightarrow FE
$$

Encode:

$$
ABCDEFGH
$$

Split:

$$
AB|CD|EF|GH
$$

Reverse each pair:

$$
BA|DC|FE|HG
$$

### Answer

$$
\boxed{BADCF EHG}
$$

Without spaces:

$$
\boxed{BAD CFEHG}
$$

Correctly written:

$$
\boxed{BADCFEHG}
$$

---

# 31. Odd-Even Rearrangement

## Example 20

For:

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

If the code is odd positions followed by even positions:

$$
ACEG+BDFH
$$

### Answer

$$
\boxed{ACEGBDFH}
$$

---

# 32. Even-Odd Rearrangement

If the code is even positions followed by odd positions:

$$
BDFH+ACEG
$$

### Answer

$$
\boxed{BDFHACEG}
$$

---

# 33. First-Last Alternation

For:

$$
ABCDE
$$

Take:

1. First
2. Last
3. Second
4. Second-last
5. Middle

Therefore:

$$
A,E,B,D,C
$$

### Answer

$$
\boxed{AEBDC}
$$

---

# 34. Example 21 — First-Last Pattern

Encode:

$$
COMPUTER
$$

using:

$$
\text{first, last, second, second-last,\ldots}
$$

Positions:

$$
C,O,M,P,U,T,E,R
$$

Order:

$$
C,R,O,E,M,T,P,U
$$

### Answer

$$
\boxed{CROEMTPU}
$$

---

# 35. Half-Swap Pattern

For:

$$
ABCDEFGH
$$

split:

$$
ABCD|EFGH
$$

Swap halves:

$$
EFGH|ABCD
$$

### Answer

$$
\boxed{EFGHABCD}
$$

---

# 36. Reverse Each Half

For:

$$
ABCDEFGH
$$

split:

$$
ABCD|EFGH
$$

Reverse:

$$
DCBA|HGFE
$$

### Answer

$$
\boxed{DCBAHGFE}
$$

---

# 37. Alternate From Both Ends

For:

$$
ABCDEFG
$$

take:

$$
A,G,B,F,C,E,D
$$

### Answer

$$
\boxed{AGBFCED}
$$

This is different from simply reversing the word.

---

# 38. Position Difference Pattern

Sometimes the code depends on the difference between adjacent letters.

For:

$$
ACE
$$

alphabet positions:

$$
1,3,5
$$

Differences:

$$
3-1=2
$$

$$
5-3=2
$$

Therefore:

$$
\boxed{2,2}
$$

---

# 39. Example 22 — Adjacent Difference

For:

$$
DOG
$$

positions:

$$
4,15,7
$$

Differences:

$$
|15-4|=11
$$

$$
|7-15|=8
$$

### Answer

$$
\boxed{11,8}
$$

---

# 40. Sum of Adjacent Differences

For:

$$
DOG
$$

$$
|15-4|+|7-15|
$$

$$
=11+8
$$

$$
=19
$$

### Answer

$$
\boxed{19}
$$

---

# 41. Pattern Coding With First and Last

For:

$$
MANGO
$$

first:

$$
M=13
$$

last:

$$
O=15
$$

Difference:

$$
|15-13|=2
$$

### Answer

$$
\boxed{2}
$$

This can be used as a compact code.

---

# 42. Pattern Coding With Sum and Difference

For:

$$
CAT
$$

positions:

$$
3,1,20
$$

Sum:

$$
24
$$

Maximum:

$$
20
$$

Minimum:

$$
1
$$

Difference:

$$
20-1=19
$$

A question may combine these values.

Example:

$$
24+19=43
$$

### Answer

$$
\boxed{43}
$$

---

# 43. Mixed Pattern Example

Suppose:

$$
A\rightarrow B
$$

$$
B\rightarrow D
$$

$$
C\rightarrow G
$$

$$
D\rightarrow K
$$

Find the pattern.

### Step 1 — Calculate shifts

$$
+1,+2,+4,+7
$$

The differences between shifts are:

$$
+1,+2,+3
$$

So the next shift is:

$$
+11
$$

for the next input.

This type of question requires **second-level pattern analysis**.

> [!important]
> When direct differences do not form a pattern, inspect the differences of the differences.

---

# 44. Second-Level Pattern Recognition

Suppose:

$$
2,\ 5,\ 10,\ 17,\ 26
$$

First differences:

$$
+3,+5,+7,+9
$$

Second differences:

$$
+2,+2,+2
$$

Therefore the next difference is:

$$
+11
$$

So:

$$
26+11=37
$$

### Answer

$$
\boxed{37}
$$

---

# 45. Third-Level Pattern

Sometimes even second differences do not remain constant.

Example:

$$
1,\ 2,\ 6,\ 24,\ 120
$$

Observe:

$$
1\times2=2
$$

$$
2\times3=6
$$

$$
6\times4=24
$$

$$
24\times5=120
$$

The rule is:

$$
\times2,\times3,\times4,\times5
$$

Next:

$$
120\times6=720
$$

### Answer

$$
\boxed{720}
$$

---

# 46. Recognition of Pattern Complexity

Use this hierarchy:

$$
\boxed{\text{Constant}}
$$

↓

$$
\boxed{\text{Increasing/Decreasing}}
$$

↓

$$
\boxed{\text{Alternating}}
$$

↓

$$
\boxed{\text{Position-Based}}
$$

↓

$$
\boxed{\text{Second Difference}}
$$

↓

$$
\boxed{\text{Arithmetic + Structural}}
$$

Do not jump directly to complicated patterns.

---

# 47. Pattern Recognition Tricks

## Pattern 1 — Same Shift Everywhere

> [!important]
> If every letter moves by the same amount:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

think:

$$
\boxed{+3}
$$

---

## Pattern 2 — Shift Increases by 1

If:

$$
+1,+2,+3,+4
$$

think:

$$
\boxed{\text{Position-based increasing shift}}
$$

---

## Pattern 3 — Shift Decreases by 1

If:

$$
+5,+4,+3,+2
$$

think:

$$
\boxed{\text{Decreasing shift}}
$$

---

## Pattern 4 — Two Operations Repeat

If:

$$
+2,-1,+2,-1
$$

think:

$$
\boxed{\text{Alternating pattern}}
$$

---

## Pattern 5 — Letters Stay the Same

If the same letters appear in a different order:

$$
ABCDE\rightarrow EABCD
$$

think:

$$
\boxed{\text{Structural rearrangement}}
$$

---

## Pattern 6 — A Becomes Z

> [!important]
> Think:

$$
\boxed{\text{Reverse alphabet}}
$$

---

## Pattern 7 — Numbers Grow Rapidly

If:

$$
1,4,9,16,25
$$

think:

$$
\boxed{n^2}
$$

---

## Pattern 8 — Numbers Grow Very Rapidly

If:

$$
1,8,27,64
$$

think:

$$
\boxed{n^3}
$$

---

## Pattern 9 — Differences Grow

If:

$$
+2,+4,+6,+8
$$

think:

$$
\boxed{\text{Increasing even differences}}
$$

---

## Pattern 10 — Multiplication Changes

If:

$$
\times2,\times3,\times4
$$

think:

$$
\boxed{\text{Increasing multiplier}}
$$

---

# 48. Shortcuts

> [!tip]
> **Shortcut 1 — Write positions instead of counting letters**

For:

$$
M
$$

immediately use:

$$
M=13
$$

For:

$$
T
$$

use:

$$
T=20
$$

This makes alphabet patterns faster.

---

> [!tip]
> **Shortcut 2 — Detect constant shift with one comparison**

If:

$$
C\rightarrow F
$$

then:

$$
+3
$$

Immediately test the next pair.

---

> [!tip]
> **Shortcut 3 — For changing shifts, write the differences**

If:

$$
A\rightarrow B
$$

$$
B\rightarrow D
$$

$$
C\rightarrow F
$$

write:

$$
+1,+2,+3
$$

The pattern becomes obvious.

---

> [!tip]
> **Shortcut 4 — Separate odd and even positions**

For:

$$
ABCDEFGH
$$

write:

$$
ACEG
$$

and:

$$
BDFH
$$

Many difficult-looking patterns become simple.

---

> [!tip]
> **Shortcut 5 — Check wrapping immediately**

If:

$$
X+5
$$

do not stop at Z.

Continue:

$$
X\rightarrow Y\rightarrow Z\rightarrow A\rightarrow B\rightarrow C
$$

Therefore:

$$
\boxed{C}
$$

---

> [!tip]
> **Shortcut 6 — Look for complementary letters**

If:

$$
A\rightarrow Z
$$

$$
B\rightarrow Y
$$

think:

$$
\boxed{27-p}
$$

---

> [!tip]
> **Shortcut 7 — For number patterns, calculate differences first**

Example:

$$
3,7,13,21,31
$$

Differences:

$$
4,6,8,10
$$

The pattern becomes obvious.

---

> [!tip]
> **Shortcut 8 — If differences fail, check ratios**

Example:

$$
2,4,8,16
$$

Differences are:

$$
2,4,8
$$

but ratios are:

$$
2,2,2
$$

Therefore think:

$$
\boxed{\times2}
$$

---

> [!tip]
> **Shortcut 9 — If both differences and ratios fail, inspect positions**

Look for:

$$
+1,+2,+3
$$

or:

$$
+1,-1,+1,-1
$$

---

> [!tip]
> **Shortcut 10 — Verify before committing**

A pattern is valid only if it explains all provided examples.

---

# 49. Common Exam Patterns

> [!important] Must Master

### Alphabet Patterns

1. Constant forward shift
2. Constant backward shift
3. Circular shift
4. Increasing shift
5. Decreasing shift
6. Alternating shift
7. Reverse alphabet
8. Position-based shift
9. Prime-number shifts
10. Fibonacci shifts

### Number Patterns

11. Constant difference
12. Increasing difference
13. Decreasing difference
14. Constant ratio
15. Increasing multiplier
16. Decreasing multiplier
17. Squares
18. Cubes
19. Prime numbers
20. Fibonacci
21. Factorial-like pattern
22. Mixed arithmetic pattern

### Structural Patterns

23. Reverse word
24. First-last exchange
25. Pair swapping
26. Odd-even arrangement
27. Half swapping
28. Reverse each half
29. First-last alternating
30. Position rotation

### Advanced

31. Difference of differences
32. Difference-ratio combination
33. Arithmetic + alphabet shift
34. Position + alphabet shift
35. Multiple alternating operations
36. Mixed structural and arithmetic coding

---

# 50. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Assuming constant shift

Do not assume:

$$
+2
$$

just because the first pair shows a $+2$ shift.

Check all pairs.

---

### Mistake 2 — Ignoring circular movement

After:

$$
Z
$$

comes:

$$
A
$$

in cyclic alphabet coding.

---

### Mistake 3 — Confusing reverse word and reverse alphabet

Reverse word:

$$
CAT\rightarrow TAC
$$

Reverse alphabet:

$$
CAT\rightarrow XZG
$$

These are completely different.

---

### Mistake 4 — Ignoring position

If shifts are:

$$
+1,+2,+3
$$

each position has a different rule.

---

### Mistake 5 — Missing alternating patterns

A pattern may be:

$$
+2,-1,+2,-1
$$

rather than:

$$
+2,+2,+2,+2
$$

---

### Mistake 6 — Checking differences only

For number patterns, also check:

- Ratios
- Squares
- Cubes
- Multipliers
- Alternation

---

### Mistake 7 — Overfitting

Do not create a complicated rule just because it matches two examples.

The intended aptitude rule is usually simple.

---

### Mistake 8 — Arithmetic errors

Pattern recognition is useless if the final calculation is wrong.

---

### Mistake 9 — Ignoring second differences

If:

$$
+3,+5,+7,+9
$$

appears, recognize the difference itself is changing regularly.

---

### Mistake 10 — Forgetting the question direction

Encoding:

$$
A\rightarrow B
$$

does not mean decoding:

$$
A\rightarrow B
$$

When decoding, reverse the mapping.

---

# 51. Advanced Example — Mixed Alphabet Pattern

## Example 23

Suppose:

$$
A\rightarrow C
$$

$$
B\rightarrow E
$$

$$
C\rightarrow G
$$

$$
D\rightarrow I
$$

Find the code for E.

### Step 1 — Calculate shifts

$$
+2,+3,+4,+5
$$

### Step 2 — Continue

Next shift:

$$
+6
$$

Therefore:

$$
E+6=K
$$

### Answer

$$
\boxed{K}
$$

---

# 52. Advanced Example — Alternating Pattern

## Example 24

Suppose:

$$
A\rightarrow C
$$

$$
B\rightarrow A
$$

$$
C\rightarrow E
$$

$$
D\rightarrow B
$$

Identify the rule.

Shifts:

$$
+2,-1,+2,-2
$$

The simple alternating interpretation does not fit perfectly.

Therefore, do not assume a pattern without enough information.

> [!important]
> **Insufficient evidence is better than inventing a rule.**

---

# 53. Advanced Example — Pair-Based Transformation

Suppose:

$$
AB\rightarrow CD
$$

$$
EF\rightarrow GH
$$

The transformation is:

$$
+2
$$

for each letter.

Encode:

$$
IJ
$$

$$
I+2=K
$$

$$
J+2=L
$$

### Answer

$$
\boxed{KL}
$$

---

# 54. Advanced Example — Pair Reversal + Shift

Suppose:

1. Swap each pair.
2. Shift each letter by $+1$.

Encode:

$$
ABCD
$$

### Step 1 — Pair swap

$$
AB|CD
$$

becomes:

$$
BA|DC
$$

### Step 2 — Shift

$$
B\rightarrow C
$$

$$
A\rightarrow B
$$

$$
D\rightarrow E
$$

$$
C\rightarrow D
$$

### Answer

$$
\boxed{CBED}
$$

---

# 55. Advanced Example — Odd-Even + Shift

Suppose:

1. Rearrange odd positions first.
2. Then shift every letter by $+1$.

Encode:

$$
ABCDE
$$

### Step 1

Odd positions:

$$
A,C,E
$$

Even positions:

$$
B,D
$$

Therefore:

$$
ACEBD
$$

### Step 2

Shift:

$$
A\rightarrow B
$$

$$
C\rightarrow D
$$

$$
E\rightarrow F
$$

$$
B\rightarrow C
$$

$$
D\rightarrow E
$$

### Answer

$$
\boxed{BDFCE}
$$

---

# 56. Advanced Example — Numerical Pattern

## Example 25

Suppose:

$$
2\rightarrow5
$$

$$
4\rightarrow11
$$

$$
6\rightarrow17
$$

Find the code for 8.

Observe:

$$
2(3)-1=5
$$

$$
4(3)-1=11
$$

$$
6(3)-1=17
$$

Therefore:

$$
f(n)=3n-1
$$

For $8$:

$$
3(8)-1=23
$$

### Answer

$$
\boxed{23}
$$

---

# 57. Advanced Example — Square Plus Position

Suppose:

$$
1\rightarrow2
$$

$$
2\rightarrow6
$$

$$
3\rightarrow12
$$

$$
4\rightarrow20
$$

Observe:

$$
1(1+1)=2
$$

$$
2(2+1)=6
$$

$$
3(3+1)=12
$$

$$
4(4+1)=20
$$

Therefore:

$$
f(n)=n(n+1)
$$

For:

$$
5
$$

$$
5(6)=30
$$

### Answer

$$
\boxed{30}
$$

---

# 58. Advanced Example — Factorial-Like Pattern

Suppose:

$$
1\rightarrow1
$$

$$
2\rightarrow2
$$

$$
3\rightarrow6
$$

$$
4\rightarrow24
$$

$$
5\rightarrow120
$$

The pattern is:

$$
n!
$$

Therefore:

$$
6\rightarrow720
$$

### Answer

$$
\boxed{720}
$$

---

# 59. Advanced Example — Alternating Multiplication

Suppose:

$$
2\rightarrow4
$$

$$
4\rightarrow12
$$

$$
6\rightarrow12
$$

$$
8\rightarrow24
$$

This may indicate alternating operations:

$$
\times2,\times3,\times2,\times3
$$

Always inspect whether the operation itself alternates.

---

# 60. Advanced Example — Multiple Pattern Verification

Suppose:

$$
A\rightarrow C
$$

$$
B\rightarrow E
$$

$$
C\rightarrow G
$$

The shifts are:

$$
+2,+3,+4
$$

The pattern is increasing by one.

But another possible interpretation could exist with only three data points.

> [!important]
> In aptitude questions, use the pattern that is:
>
> 1. Simple
> 2. Consistent
> 3. Supported by all examples
> 4. Appropriate to the answer choices

---

# 61. Exam-Speed Recognition Framework

## Level 1 — Immediate Checks

Check:

$$
\boxed{\text{Same shift?}}
$$

$$
\boxed{\text{Reverse?}}
$$

$$
\boxed{\text{Same letters, different order?}}
$$

---

## Level 2 — Position Checks

Check:

$$
\boxed{+1,+2,+3}
$$

$$
\boxed{+3,+2,+1}
$$

$$
\boxed{+2,-1,+2,-1}
$$

---

## Level 3 — Mathematical Checks

For numbers:

$$
\boxed{\text{Difference}}
$$

$$
\boxed{\text{Ratio}}
$$

$$
\boxed{\text{Square}}
$$

$$
\boxed{\text{Cube}}
$$

$$
\boxed{\text{Prime}}
$$

$$
\boxed{\text{Fibonacci}}
$$

---

## Level 4 — Structural Checks

Check:

$$
\boxed{\text{Odd/Even}}
$$

$$
\boxed{\text{Pairs}}
$$

$$
\boxed{\text{Halves}}
$$

$$
\boxed{\text{First/Last}}
$$

---

## Level 5 — Mixed Rules

Only after simple rules fail:

$$
\boxed{\text{Arithmetic + Structural}}
$$

$$
\boxed{\text{Position + Shift}}
$$

$$
\boxed{\text{Multiple Operations}}
$$

---

# 62. Pattern Recognition Master Table

| Observation | Think |
|---|---|
| Same shift | Constant shift |
| Shift grows by 1 | Increasing shift |
| Shift decreases by 1 | Decreasing shift |
| Two shifts repeat | Alternating |
| A becomes Z | Reverse alphabet |
| Letters reorder | Structural pattern |
| Odd letters grouped | Odd-even pattern |
| Pairs reversed | Pair pattern |
| Two halves exchange | Half-swap |
| Number differences constant | Arithmetic progression |
| Ratios constant | Geometric progression |
| Differences increase regularly | Second difference |
| $1,4,9,16$ | Squares |
| $1,8,27,64$ | Cubes |
| $1,2,6,24$ | Factorial |
| $1,1,2,3,5$ | Fibonacci |
| $2,3,5,7$ | Prime pattern |

---

# 63. Formula Sheet

## Alphabet Position

$$
\boxed{A=1,\ldots,Z=26}
$$

## Constant Shift

$$
\boxed{p'=p+k}
$$

## Backward Shift

$$
\boxed{p'=p-k}
$$

## Reverse Alphabet

$$
\boxed{p'=27-p}
$$

## Increasing Position Shift

$$
\boxed{p'=p+i}
$$

## Decreasing Position Shift

$$
\boxed{p'=p+(n-i+1)}
$$

## Arithmetic Progression

$$
\boxed{a_n=a_1+(n-1)d}
$$

## Geometric Progression

$$
\boxed{a_n=a_1r^{n-1}}
$$

## Sum of First $n$ Natural Numbers

$$
\boxed{\frac{n(n+1)}{2}}
$$

## Square Pattern

$$
\boxed{a_n=n^2}
$$

## Cube Pattern

$$
\boxed{a_n=n^3}
$$

## Factorial Pattern

$$
\boxed{a_n=n!}
$$

## Fibonacci

$$
\boxed{F_n=F_{n-1}+F_{n-2}}
$$

## Reverse Word

$$
\boxed{C_1C_2\ldots C_n\rightarrow C_n\ldots C_2C_1}
$$

## Odd-Even Rearrangement

$$
\boxed{
C_1C_3C_5\ldots C_2C_4C_6\ldots
}
$$

---

# 64. Quick Revision

> [!summary] One-Minute Revision

## Pattern Coding

The core process is:

$$
\boxed{
\text{Observe}
\rightarrow
\text{Calculate}
\rightarrow
\text{Identify Pattern}
\rightarrow
\text{Verify}
\rightarrow
\text{Apply}
}
$$

### For Letters

Check:

$$
\boxed{\text{Constant shift}}
$$

$$
\boxed{\text{Increasing shift}}
$$

$$
\boxed{\text{Decreasing shift}}
$$

$$
\boxed{\text{Alternating shift}}
$$

$$
\boxed{\text{Reverse alphabet}}
$$

$$
\boxed{\text{Position-based shift}}
$$

### For Numbers

Check:

$$
\boxed{\text{Difference}}
$$

$$
\boxed{\text{Ratio}}
$$

$$
\boxed{\text{Square}}
$$

$$
\boxed{\text{Cube}}
$$

$$
\boxed{\text{Prime}}
$$

$$
\boxed{\text{Fibonacci}}
$$

$$
\boxed{\text{Factorial}}
$$

### For Word Structure

Check:

$$
\boxed{\text{Reverse}}
$$

$$
\boxed{\text{Pair swap}}
$$

$$
\boxed{\text{Odd-even}}
$$

$$
\boxed{\text{Half swap}}
$$

$$
\boxed{\text{First-last}}
$$

### Golden Memory Trick

**"Pattern Coding is not about guessing the code; it is about finding the smallest consistent rule that explains every transformation."**

# One-Line Recognition

**When the coding rule is not directly given, compare the input and output systematically—first check constant shifts, then changing shifts, arithmetic patterns, position patterns, and finally structural rearrangements.**