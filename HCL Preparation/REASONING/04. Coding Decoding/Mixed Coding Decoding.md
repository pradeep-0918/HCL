---
type: concept
subject: reasoning
topic: "Matrix Coding"
parent: "04. Coding Decoding"
company: HCL
difficulty: hard
priority: very-high
status: not-started
tags:
  - reasoning
  - coding-decoding
  - matrix-coding
  - matrix-reasoning
  - coded-language
  - logical-reasoning
  - pattern-recognition
  - hcl
wikilinks:
  - "[[04. Coding Decoding]]"
  - "[[Letter Coding]]"
  - "[[Number Coding]]"
  - "[[Word Coding]]"
  - "[[Substitution Coding]]"
  - "[[Pattern Coding]]"
  - "[[Chinese Coding]]"
  - "[[Mixed Coding Decoding]]"
---

# Matrix Coding

## 1. Core Concept

> [!summary]
> **Matrix Coding** is a coding-decoding method in which letters, numbers, symbols, or words are assigned positions inside a matrix or grid. The required code is obtained by identifying the row and column, or by combining the coordinates of the required item.

The central idea is:

$$
\boxed{\text{Item}\rightarrow\text{Matrix Position}\rightarrow\text{Code}}
$$

A typical matrix may look like:

| Row | Column 1 | Column 2 | Column 3 | Column 4 | Column 5 |
|---|---|---|---|---|---|
| 1 | A | B | C | D | E |
| 2 | F | G | H | I | J |
| 3 | K | L | M | N | O |
| 4 | P | Q | R | S | T |
| 5 | U | V | W | X | Y |

If:

$$
A=(1,1)
$$

then the code for A may be:

$$
\boxed{11}
$$

If:

$$
M=(3,3)
$$

then:

$$
\boxed{33}
$$

The exact coding format depends on the question.

---

# 2. Basic Meaning

A matrix is simply an organized arrangement of elements in:

- Rows
- Columns
- Cells

For example:

$$
\begin{matrix}
A&B&C\\
D&E&F\\
G&H&I
\end{matrix}
$$

Here:

- A is in row 1, column 1.
- B is in row 1, column 2.
- D is in row 2, column 1.
- E is in row 2, column 2.
- I is in row 3, column 3.

Therefore:

$$
A=(1,1)
$$

$$
E=(2,2)
$$

$$
I=(3,3)
$$

The matrix acts like a **coordinate system**.

---

# 3. Main Formula

For a standard row-column matrix:

$$
\boxed{\text{Code}=(\text{Row},\text{Column})}
$$

If an item is at row $r$ and column $c$:

$$
\boxed{Code=(r,c)}
$$

If the question joins the coordinates:

$$
\boxed{Code=10r+c}
$$

or simply:

$$
\boxed{rc}
$$

depending on the stated convention.

### Important

There is **no universal Matrix Coding formula**.

Always follow the coding rule specified by the question.

---

# 4. Important Properties

1. A matrix is organized using rows and columns.
2. Every cell has a unique position.
3. Position can be represented by:
   - Row number
   - Column number
4. The first coordinate usually represents the row.
5. The second coordinate usually represents the column.
6. Some questions reverse the order.
7. Some matrices use letters.
8. Some use numbers.
9. Some use symbols.
10. Some use mixed elements.
11. A single item can have a coordinate code.
12. A word can be represented by multiple coordinate codes.
13. Matrix questions may involve a single matrix or multiple matrices.
14. The question may require encoding or decoding.
15. Coordinate order must be checked carefully.
16. Matrix boundaries may create special cases.
17. Repeated elements can create ambiguity.
18. Some questions use a larger matrix such as $5\times5$.
19. Some questions use two-dimensional coordinate systems.
20. Speed comes from locating cells quickly.

---

# 5. Matrix Terminology

| Term | Meaning |
|---|---|
| Matrix | Rectangular arrangement |
| Row | Horizontal line |
| Column | Vertical line |
| Cell | Individual position |
| Coordinate | Row-column location |
| Dimension | Number of rows × columns |
| $2\times2$ | 2 rows, 2 columns |
| $3\times3$ | 3 rows, 3 columns |
| $5\times5$ | 5 rows, 5 columns |
| Main diagonal | Cells where row = column |
| Position | Exact location of an element |

---

# 6. Basic Matrix

Consider:

|   | C1 | C2 | C3 |
|---|---|---|---|
| R1 | A | B | C |
| R2 | D | E | F |
| R3 | G | H | I |

Coordinates:

| Letter | Coordinate |
|---|---|
| A | $(1,1)$ |
| B | $(1,2)$ |
| C | $(1,3)$ |
| D | $(2,1)$ |
| E | $(2,2)$ |
| F | $(2,3)$ |
| G | $(3,1)$ |
| H | $(3,2)$ |
| I | $(3,3)$ |

---

# 7. Basic Example — Find Position

## Example 1

### Question

Find the matrix position of E.

Matrix:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

E is:

- Row = 2
- Column = 2

Therefore:

$$
\boxed{E=(2,2)}
$$

---

# 8. Example 2 — Find Position of H

From the same matrix:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

H is in:

$$
Row=3
$$

$$
Column=2
$$

Therefore:

$$
\boxed{H=(3,2)}
$$

---

# 9. Example 3 — Encode a Letter

Suppose the coding rule is:

$$
\boxed{\text{Code}=\text{Row followed by Column}}
$$

Using:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Encode:

$$
G
$$

G is at:

$$
(3,1)
$$

Therefore:

$$
\boxed{31}
$$

---

# 10. Example 4 — Encode a Word

Using the same matrix:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Encode:

$$
BAD
$$

Mappings:

$$
B=(1,2)
$$

$$
A=(1,1)
$$

$$
D=(2,1)
$$

Therefore:

$$
\boxed{12\ 11\ 21}
$$

---

# 11. Example 5 — Decode a Coordinate

Given:

$$
21
$$

and the matrix:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Interpret:

$$
21
$$

as:

$$
Row=2
$$

$$
Column=1
$$

The cell is D.

Therefore:

$$
\boxed{D}
$$

---

# 12. Example 6 — Decode Multiple Coordinates

Decode:

$$
11\ 23\ 32
$$

Using:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Mappings:

$$
11=A
$$

$$
23=F
$$

$$
32=H
$$

Therefore:

$$
\boxed{AFH}
$$

---

# 13. Matrix Coding With a $5\times5$ Alphabet Matrix

A common arrangement is:

|   | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| 1 | A | B | C | D | E |
| 2 | F | G | H | I | J |
| 3 | K | L | M | N | O |
| 4 | P | Q | R | S | T |
| 5 | U | V | W | X | Y |

Z may be handled separately depending on the question.

Coordinates:

$$
A=(1,1)
$$

$$
F=(2,1)
$$

$$
M=(3,3)
$$

$$
T=(4,5)
$$

$$
Y=(5,5)
$$

---

# 14. Example 7 — Encode M

Using the $5\times5$ matrix:

M is at:

$$
Row=3
$$

$$
Column=3
$$

Therefore:

$$
\boxed{33}
$$

---

# 15. Example 8 — Encode T

T is at:

$$
(4,5)
$$

Therefore:

$$
\boxed{45}
$$

---

# 16. Example 9 — Decode 52

Using:

|   | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| 1 | A | B | C | D | E |
| 2 | F | G | H | I | J |
| 3 | K | L | M | N | O |
| 4 | P | Q | R | S | T |
| 5 | U | V | W | X | Y |

$$
52
$$

means:

$$
Row=5
$$

$$
Column=2
$$

The letter is V.

Therefore:

$$
\boxed{V}
$$

---

# 17. Example 10 — Encode HELLO

Using the same matrix:

$$
H=(2,3)
$$

$$
E=(1,5)
$$

$$
L=(3,2)
$$

$$
L=(3,2)
$$

$$
O=(3,5)
$$

Therefore:

$$
\boxed{23\ 15\ 32\ 32\ 35}
$$

---

# 18. Coordinate Recognition

> [!important]
> If the code consists of two digits and a matrix is provided, immediately check:
>
> $$\boxed{\text{First digit = Row, Second digit = Column}}$$
>
> unless the question specifies the reverse.

For example:

$$
34
$$

means:

$$
Row=3,\ Column=4
$$

---

# 19. Reverse Coordinate Coding

Some questions may define:

$$
\boxed{\text{Code}=(Column,Row)}
$$

Then:

$$
34
$$

means:

$$
Column=3
$$

$$
Row=4
$$

Always read the instruction before solving.

---

# 20. Example 11 — Reversed Coordinates

Suppose:

> Code is written as Column followed by Row.

Using:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Find the code for D.

D is:

$$
Row=2
$$

$$
Column=1
$$

Normally:

$$
21
$$

But the question requires:

$$
Column+Row
$$

Therefore:

$$
\boxed{12}
$$

---

# 21. Matrix Coding of Words

If each character is represented by its coordinate:

$$
WORD=W_1W_2\ldots W_n
$$

then:

$$
Code(W)=Code(W_1),Code(W_2),\ldots,Code(W_n)
$$

For example:

$$
CAT
$$

using:

|   | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| 1 | A | B | C | D | E |
| 2 | F | G | H | I | J |
| 3 | K | L | M | N | O |
| 4 | P | Q | R | S | T |
| 5 | U | V | W | X | Y |

We have:

$$
C=(1,3)
$$

$$
A=(1,1)
$$

$$
T=(4,5)
$$

Therefore:

$$
\boxed{13\ 11\ 45}
$$

---

# 22. Matrix Coding With Numbers

Consider:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | 2 | 5 | 8 |
| 2 | 1 | 4 | 7 |
| 3 | 3 | 6 | 9 |

The code of number 6 is:

$$
(3,2)
$$

Therefore:

$$
\boxed{32}
$$

---

# 23. Matrix Coding With Symbols

Consider:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | @ | # | $ |
| 2 | % | & | * |
| 3 | + | - | / |

The position of:

$$
\&
$$

is:

$$
(2,2)
$$

Therefore:

$$
\boxed{22}
$$

---

# 24. Matrix Coding With Words

Consider:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | CAT | DOG | COW |
| 2 | HORSE | LION | TIGER |
| 3 | GOAT | DEER | BEAR |

The code for LION is:

$$
(2,2)
$$

Therefore:

$$
\boxed{22}
$$

---

# 25. Matrix Coding With Multiple Matrices

Some questions use more than one matrix.

For example:

### Matrix A

|   | 1 | 2 |
|---|---|---|
| 1 | A | B |
| 2 | C | D |

### Matrix B

|   | 1 | 2 |
|---|---|---|
| 1 | E | F |
| 2 | G | H |

The code may be represented by:

$$
\boxed{\text{Matrix ID + Row + Column}}
$$

For example:

$$
A\rightarrow A11
$$

$$
H\rightarrow B22
$$

The exact format depends on the question.

---

# 26. Example 12 — Three-Part Coordinate

Suppose:

- Matrix 1 contains A-D.
- Matrix 2 contains E-H.

A is at:

$$
(1,1)
$$

H is at:

$$
(2,2)
$$

If the code includes matrix number:

$$
A\rightarrow111
$$

$$
H\rightarrow222
$$

### Answer

$$
\boxed{111,\ 222}
$$

---

# 27. Matrix Coding Using Row Labels

A matrix may use letters for rows and numbers for columns.

Example:

|   | 1 | 2 | 3 |
|---|---|---|---|
| A | P | Q | R |
| B | S | T | U |
| C | V | W | X |

Then:

$$
T
$$

is:

$$
Row=B
$$

$$
Column=2
$$

Therefore:

$$
\boxed{B2}
$$

---

# 28. Matrix Coding Using Column Labels

Sometimes columns are letters.

|   | A | B | C |
|---|---|---|---|
| 1 | P | Q | R |
| 2 | S | T | U |
| 3 | V | W | X |

The position of W is:

$$
Row=3
$$

$$
Column=B
$$

Therefore:

$$
\boxed{3B}
$$

---

# 29. Matrix Coding With Coordinates

A question may explicitly give:

$$
A=(2,3)
$$

$$
B=(1,2)
$$

and ask for a combined code.

For:

$$
A+B
$$

the code could be:

$$
23\ 12
$$

Therefore:

$$
\boxed{2312}
$$

if the question says to concatenate the coordinates.

---

# 30. Diagonal Recognition

In a square matrix, cells where:

$$
Row=Column
$$

form the main diagonal.

For:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Main diagonal:

$$
A,E,I
$$

because:

$$
A=(1,1)
$$

$$
E=(2,2)
$$

$$
I=(3,3)
$$

Therefore:

$$
\boxed{AEI}
$$

---

# 31. Anti-Diagonal

For a $3\times3$ matrix, the opposite diagonal is:

$$
C,E,G
$$

Coordinates:

$$
C=(1,3)
$$

$$
E=(2,2)
$$

$$
G=(3,1)
$$

Therefore:

$$
\boxed{CEG}
$$

---

# 32. Example 13 — Diagonal Code

Given:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Find the code represented by the main diagonal.

Main diagonal:

$$
A,E,I
$$

### Answer

$$
\boxed{AEI}
$$

---

# 33. Row-Based Questions

Given:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Row 2 contains:

$$
D,E,F
$$

Therefore:

$$
\boxed{DEF}
$$

---

# 34. Column-Based Questions

Column 2 contains:

$$
B,E,H
$$

Therefore:

$$
\boxed{BEH}
$$

---

# 35. Example 14 — Same Row

Find the letters in the same row as E.

Matrix:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

E is in row 2.

Therefore:

$$
\boxed{D,E,F}
$$

---

# 36. Example 15 — Same Column

Find the letters in the same column as H.

H is in column 2.

Therefore:

$$
\boxed{B,E,H}
$$

---

# 37. Matrix Distance

Sometimes questions ask for distance between cells.

If:

$$
A=(1,1)
$$

and:

$$
I=(3,3)
$$

the row difference is:

$$
|3-1|=2
$$

The column difference is:

$$
|3-1|=2
$$

### Manhattan distance

$$
2+2=4
$$

### Answer

$$
\boxed{4}
$$

> [!important]
> Use a distance formula only if the question explicitly defines or requires distance.

---

# 38. Matrix Neighbor Problems

In a matrix, neighboring cells may include:

- Up
- Down
- Left
- Right
- Diagonal

For E:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

### Four direct neighbors

$$
B,D,F,H
$$

### Eight surrounding neighbors

$$
A,B,C,D,F,G,H,I
$$

---

# 39. Example 16 — Direct Neighbors

Find the directly adjacent letters to E.

Direct neighbors:

- Up → B
- Left → D
- Right → F
- Down → H

Therefore:

$$
\boxed{B,D,F,H}
$$

---

# 40. Boundary Cells

Boundary cells do not always have four direct neighbors.

For A:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

A has only:

- Right → B
- Down → D

Therefore:

$$
\boxed{B,D}
$$

---

# 41. Corner Recognition

In a $3\times3$ matrix, corners are:

$$
A,C,G,I
$$

Coordinates:

$$
(1,1),(1,3),(3,1),(3,3)
$$

These are often useful in positional questions.

---

# 42. Example 17 — Corner Code

Using:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Find the letters at the corners.

### Answer

$$
\boxed{A,C,G,I}
$$

---

# 43. Center Recognition

In a $3\times3$ matrix, the center is:

$$
(2,2)
$$

For:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

center:

$$
\boxed{E}
$$

---

# 44. Matrix Rotation

Some advanced Matrix Coding questions may rotate a matrix.

For:

$$
\begin{matrix}
A&B\\
C&D
\end{matrix}
$$

A $90^\circ$ clockwise rotation gives:

$$
\begin{matrix}
C&A\\
D&B
\end{matrix}
$$

A $180^\circ$ rotation gives:

$$
\begin{matrix}
D&C\\
B&A
\end{matrix}
$$

A $90^\circ$ anticlockwise rotation gives:

$$
\begin{matrix}
B&D\\
A&C
\end{matrix}
$$

---

# 45. Example 18 — 180° Rotation

Given:

$$
\begin{matrix}
A&B\\
C&D
\end{matrix}
$$

Rotate by $180^\circ$.

The order reverses:

$$
\boxed{
\begin{matrix}
D&C\\
B&A
\end{matrix}
}
$$

---

# 46. Matrix Reflection

Reflection may be:

### Horizontal Reflection

Top and bottom rows exchange.

### Vertical Reflection

Left and right columns exchange.

For:

$$
\begin{matrix}
A&B\\
C&D
\end{matrix}
$$

Vertical reflection:

$$
\begin{matrix}
B&A\\
D&C
\end{matrix}
$$

Horizontal reflection:

$$
\begin{matrix}
C&D\\
A&B
\end{matrix}
$$

---

# 47. Pattern Recognition

## Pattern 1 — Two-Digit Code

> [!important]
> If a matrix is provided and the code consists of two digits, immediately test:

$$
\boxed{Row+Column}
$$

Example:

$$
34
$$

means:

$$
Row=3,\ Column=4
$$

unless the question states another convention.

---

## Pattern 2 — Code Is a Letter + Number

> [!important]
> Think:

$$
\boxed{\text{Row Label + Column Label}}
$$

Example:

$$
B3
$$

means row B, column 3.

---

## Pattern 3 — Same Row

If the question says:

> "Which elements are in the same row?"

think:

$$
\boxed{\text{Horizontal}}
$$

---

## Pattern 4 — Same Column

If the question says:

> "Which elements are in the same column?"

think:

$$
\boxed{\text{Vertical}}
$$

---

## Pattern 5 — Main Diagonal

If the question says:

> "Principal diagonal"

think:

$$
\boxed{Row=Column}
$$

---

## Pattern 6 — Opposite Diagonal

For an $n\times n$ matrix:

$$
\boxed{r+c=n+1}
$$

---

## Pattern 7 — Center

For an odd-sized square matrix:

$$
\boxed{
\left(
\frac{n+1}{2},
\frac{n+1}{2}
\right)
}
$$

---

## Pattern 8 — Corner

For an $n\times n$ matrix, corners are:

$$
\boxed{
(1,1),(1,n),(n,1),(n,n)
}
$$

---

## Pattern 9 — Neighbor

If the question asks for adjacent elements, first determine whether it means:

- Four-directional
- Eight-directional

---

## Pattern 10 — Multiple Matrices

> [!important]
> If more than one matrix exists, identify the matrix first, then locate the row and column.

---

# 48. Shortcuts

> [!tip]
> **Shortcut 1 — Memorize the 3×3 coordinate layout**

$$
\begin{matrix}
11&12&13\\
21&22&23\\
31&32&33
\end{matrix}
$$

This allows instant coordinate recognition.

---

> [!tip]
> **Shortcut 2 — Memorize the 5×5 pattern**

$$
\begin{matrix}
11&12&13&14&15\\
21&22&23&24&25\\
31&32&33&34&35\\
41&42&43&44&45\\
51&52&53&54&55
\end{matrix}
$$

Then simply locate the letter.

---

> [!tip]
> **Shortcut 3 — Read row first**

Unless explicitly stated otherwise:

$$
\boxed{\text{Row}\rightarrow\text{Column}}
$$

---

> [!tip]
> **Shortcut 4 — For words, make a coordinate dictionary**

Example:

$$
C=13
$$

$$
A=11
$$

$$
T=45
$$

Then:

$$
CAT=13\ 11\ 45
$$

---

> [!tip]
> **Shortcut 5 — Use the matrix rather than recalculating**

Once the matrix is given, do not repeatedly count from A.

Locate the cell directly.

---

> [!tip]
> **Shortcut 6 — Diagonal shortcut**

Main diagonal:

$$
r=c
$$

Opposite diagonal:

$$
r+c=n+1
$$

---

> [!tip]
> **Shortcut 7 — Corner shortcut**

Remember:

$$
(1,1),(1,n),(n,1),(n,n)
$$

---

> [!tip]
> **Shortcut 8 — Center shortcut**

For a $5\times5$ matrix:

$$
\left(\frac{5+1}{2},\frac{5+1}{2}\right)
=
(3,3)
$$

So the center is always position 33.

---

> [!tip]
> **Shortcut 9 — Reverse decoding**

If:

$$
32=M
$$

then immediately:

$$
M=32
$$

You are simply reversing the lookup.

---

> [!tip]
> **Shortcut 10 — Check the coding convention first**

Before solving, identify:

$$
\boxed{
\text{Row-Column?}
}
$$

or:

$$
\boxed{
\text{Column-Row?}
}
$$

or:

$$
\boxed{
\text{Matrix-Row-Column?}
}
$$

---

# 49. Common Exam Patterns

> [!important] Must Master

### Basic Matrix

1. Identify row
2. Identify column
3. Find cell
4. Find coordinate
5. Encode a single element
6. Decode a coordinate

### Word Coding

7. Encode a word
8. Decode a word
9. Encode a sentence
10. Decode a sentence

### Coordinate Coding

11. Row-column code
12. Column-row code
13. Letter-number coordinate
14. Number-letter coordinate
15. Three-part coordinates

### Positional Reasoning

16. Same row
17. Same column
18. Main diagonal
19. Opposite diagonal
20. Center
21. Corner
22. Boundary
23. Adjacent cells
24. Neighboring cells

### Advanced Matrix

25. Multiple matrices
26. Matrix selection
27. Matrix rotation
28. Matrix reflection
29. Coordinate transformation
30. Mixed matrix coding

---

# 50. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Reversing row and column

If:

$$
M=(3,2)
$$

do not write:

$$
23
$$

unless the coding rule says column first.

---

### Mistake 2 — Ignoring the given matrix

Do not assume the alphabet is always arranged:

$$
A,B,C,\ldots
$$

The question may use a custom arrangement.

---

### Mistake 3 — Assuming A is always 11

A is 11 only if A is actually located at row 1, column 1.

---

### Mistake 4 — Ignoring labels

Rows or columns may use letters rather than numbers.

---

### Mistake 5 — Confusing diagonal types

Main diagonal:

$$
r=c
$$

Opposite diagonal:

$$
r+c=n+1
$$

---

### Mistake 6 — Treating diagonal as row or column

Diagonal cells follow a positional relationship, not a common row or column.

---

### Mistake 7 — Ignoring boundary limitations

Corner cells have fewer neighbors than center cells.

---

### Mistake 8 — Assuming four neighbors when diagonals count

Check whether the question means:

$$
\boxed{4\text{-directional}}
$$

or:

$$
\boxed{8\text{-directional}}
$$

---

### Mistake 9 — Forgetting repeated letters

If:

$$
CAT
$$

contains a repeated letter in another word, its matrix coordinate remains the same.

---

### Mistake 10 — Rebuilding the matrix unnecessarily

Once you have located the element, record its coordinate and move on.

---

# 51. Advanced Example — Custom Matrix

Consider:

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | M | A | T | H |
| 2 | P | R | O | B |
| 3 | L | E | M | S |
| 4 | C | O | D | I |

Find the code for:

$$
MATH
$$

Mappings:

$$
M=(1,1)
$$

$$
A=(1,2)
$$

$$
T=(1,3)
$$

$$
H=(1,4)
$$

Therefore:

$$
\boxed{11\ 12\ 13\ 14}
$$

---

# 52. Advanced Example — Custom Matrix Decode

Using the same matrix, decode:

$$
21\ 22\ 24
$$

Mappings:

$$
21=P
$$

$$
22=R
$$

$$
24=B
$$

Therefore:

$$
\boxed{PRB}
$$

---

# 53. Advanced Example — Find Same Row

Using:

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | M | A | T | H |
| 2 | P | R | O | B |
| 3 | L | E | M | S |
| 4 | C | O | D | I |

Find the letters in the same row as O.

O occurs in row 2, column 3.

Therefore row 2 contains:

$$
P,R,O,B
$$

### Answer

$$
\boxed{P,R,O,B}
$$

---

# 54. Advanced Example — Same Column

Using the same matrix, find the letters in the same column as O at position $(2,3)$.

Column 3:

$$
T,O,M,D
$$

### Answer

$$
\boxed{T,O,M,D}
$$

---

# 55. Advanced Example — Main Diagonal

Using the same $4\times4$ matrix:

Main diagonal:

$$
(1,1),(2,2),(3,3),(4,4)
$$

Letters:

$$
M,R,M,I
$$

Therefore:

$$
\boxed{MRMI}
$$

---

# 56. Advanced Example — Opposite Diagonal

For a $4\times4$ matrix:

$$
r+c=5
$$

Positions:

$$
(1,4),(2,3),(3,2),(4,1)
$$

Letters:

$$
H,O,E,C
$$

Therefore:

$$
\boxed{HOEC}
$$

---

# 57. Advanced Example — Corner Elements

For the same matrix:

Corners:

$$
(1,1),(1,4),(4,1),(4,4)
$$

Letters:

$$
M,H,C,I
$$

### Answer

$$
\boxed{MHCI}
$$

---

# 58. Advanced Example — Coordinate Distance

Suppose:

$$
A=(1,2)
$$

and:

$$
B=(4,5)
$$

Manhattan distance:

$$
|4-1|+|5-2|
$$

$$
=3+3
$$

$$
=6
$$

### Answer

$$
\boxed{6}
$$

---

# 59. Advanced Example — Matrix Rotation

Given:

$$
\begin{matrix}
A&B&C\\
D&E&F\\
G&H&I
\end{matrix}
$$

Rotate $90^\circ$ clockwise.

The result is:

$$
\begin{matrix}
G&D&A\\
H&E&B\\
I&F&C
\end{matrix}
$$

Therefore:

$$
\boxed{
\begin{matrix}
G&D&A\\
H&E&B\\
I&F&C
\end{matrix}
}
$$

---

# 60. Advanced Example — Matrix Reflection

Given:

$$
\begin{matrix}
A&B&C\\
D&E&F\\
G&H&I
\end{matrix}
$$

Reflect vertically.

The left and right columns exchange:

$$
\boxed{
\begin{matrix}
C&B&A\\
F&E&D\\
I&H&G
\end{matrix}
}
$$

---

# 61. Advanced Example — Matrix-Based Word

Consider:

|   | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| 1 | A | B | C | D | E |
| 2 | F | G | H | I | J |
| 3 | K | L | M | N | O |
| 4 | P | Q | R | S | T |
| 5 | U | V | W | X | Y |

Encode:

$$
LOGIC
$$

Mappings:

$$
L=(3,2)
$$

$$
O=(3,5)
$$

$$
G=(2,2)
$$

$$
I=(2,4)
$$

$$
C=(1,3)
$$

Therefore:

$$
\boxed{32\ 35\ 22\ 24\ 13}
$$

---

# 62. Advanced Example — Decode a Word

Using the same matrix, decode:

$$
23\ 15\ 32\ 35
$$

Mappings:

$$
23=H
$$

$$
15=E
$$

$$
32=L
$$

$$
35=O
$$

Therefore:

$$
\boxed{HELO}
$$

---

# 63. Advanced Pattern — Multiple Possible Coordinates

If a matrix contains a repeated element:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | A | F |
| 3 | G | H | I |

A occurs twice:

$$
A=(1,1)
$$

and:

$$
A=(2,2)
$$

Therefore the code for A is ambiguous unless the question gives an additional rule.

> [!warning]
> Never assume a unique coordinate when the matrix contains repeated elements.

---

# 64. Advanced Pattern — Matrix + Symbol

Suppose:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | @ | A | 1 |
| 2 | # | B | 2 |
| 3 | $ | C | 3 |

The code of C is:

$$
(3,2)
$$

Therefore:

$$
\boxed{32}
$$

The type of element does not matter; only its position matters.

---

# 65. Advanced Pattern — Matrix Search

If asked:

> Which element is at row 3 and column 4?

Do not scan the entire matrix.

Immediately locate:

$$
(3,4)
$$

This is the fundamental matrix lookup operation.

---

# 66. Advanced Pattern — Coordinate to Element

If asked:

> Which element is represented by 42?

Interpret:

$$
4,2
$$

Then locate row 4, column 2.

This is:

$$
\boxed{\text{Coordinate}\rightarrow\text{Element}}
$$

---

# 67. Advanced Pattern — Element to Coordinate

If asked:

> What is the code for Q?

Locate Q:

$$
Q=(4,2)
$$

Therefore:

$$
\boxed{42}
$$

This is:

$$
\boxed{\text{Element}\rightarrow\text{Coordinate}}
$$

---

# 68. Matrix Coding Decision Tree

When you see a matrix question:

### Step 1

Ask:

$$
\boxed{\text{What is inside the matrix?}}
$$

Letters?

Numbers?

Symbols?

Words?

---

### Step 2

Ask:

$$
\boxed{\text{How is the code defined?}}
$$

Row-column?

Column-row?

Matrix-row-column?

---

### Step 3

Locate the required element.

---

### Step 4

Record its coordinate.

---

### Step 5

Convert the coordinate into the required code format.

---

### Step 6

For decoding, reverse the process.

---

# 69. Exam-Speed Strategy

## 5-Second Scan

Identify:

1. Matrix dimensions
2. Row labels
3. Column labels
4. Coding direction

---

## 10-Second Lookup

Find:

$$
\boxed{\text{Required cell}}
$$

---

## 15-Second Encoding

Write:

$$
\boxed{\text{Row + Column}}
$$

or the specified format.

---

## 20-Second Decoding

Split the code:

$$
34\rightarrow Row\ 3,\ Column\ 4
$$

Then locate the cell.

---

# 70. Matrix Recognition Master Table

| Question Says | Think |
|---|---|
| Position | Row + Column |
| Code of element | Element → coordinate |
| Meaning of code | Coordinate → element |
| Same row | Horizontal |
| Same column | Vertical |
| Principal diagonal | $r=c$ |
| Opposite diagonal | $r+c=n+1$ |
| Center | Middle cell |
| Corner | Four extreme cells |
| Adjacent | Neighboring cells |
| 90° clockwise | Rotate right |
| 90° anticlockwise | Rotate left |
| 180° | Reverse both directions |
| Reflection | Mirror |
| Multiple matrices | Identify matrix first |
| Repeated element | Check ambiguity |

---

# 71. Common Traps

> [!warning]
> **Trap 1 — Row vs Column**

Always determine which coordinate comes first.

---

> [!warning]
> **Trap 2 — Custom Matrix**

Never assume alphabetic order unless the matrix actually uses it.

---

> [!warning]
> **Trap 3 — Repeated Element**

A repeated letter may have more than one coordinate.

---

> [!warning]
> **Trap 4 — Matrix Labels**

The row may be labeled A, B, C instead of 1, 2, 3.

---

> [!warning]
> **Trap 5 — Diagonal Confusion**

Main diagonal:

$$
r=c
$$

Opposite diagonal:

$$
r+c=n+1
$$

---

> [!warning]
> **Trap 6 — Rotation Direction**

Clockwise and anticlockwise rotations are different.

---

> [!warning]
> **Trap 7 — Four vs Eight Neighbors**

Always check the definition of adjacency.

---

> [!warning]
> **Trap 8 — Forgetting Leading Zeros**

If a coordinate system allows single-digit positions to be written as two-digit codes, preserve the intended format.

---

# 72. Mini Practice Set

## Question 1

Given:

|   | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Find the code for E.

### Answer

$$
\boxed{22}
$$

---

## Question 2

Find the code for H.

### Answer

$$
\boxed{32}
$$

---

## Question 3

Decode:

$$
13
$$

### Answer

$$
\boxed{C}
$$

---

## Question 4

Encode:

$$
BAD
$$

### Answer

$$
B=12
$$

$$
A=11
$$

$$
D=21
$$

$$
\boxed{12\ 11\ 21}
$$

---

## Question 5

Which elements are in column 2?

### Answer

$$
\boxed{B,E,H}
$$

---

## Question 6

Which elements are in the main diagonal?

### Answer

$$
\boxed{A,E,I}
$$

---

## Question 7

Which elements are at the corners?

### Answer

$$
\boxed{A,C,G,I}
$$

---

## Question 8

What is the center element?

### Answer

$$
\boxed{E}
$$

---

## Question 9

What are the direct neighbors of E?

### Answer

$$
\boxed{B,D,F,H}
$$

---

## Question 10

For a $5\times5$ matrix, what is the center coordinate?

### Answer

$$
\left(\frac{5+1}{2},\frac{5+1}{2}\right)
$$

$$
\boxed{(3,3)}
$$

---

# 73. Formula Sheet

## Matrix Position

$$
\boxed{Position=(Row,Column)}
$$

## Standard Code

$$
\boxed{Code=Row\ followed\ by\ Column}
$$

## Main Diagonal

$$
\boxed{r=c}
$$

## Opposite Diagonal

$$
\boxed{r+c=n+1}
$$

## Center of Odd $n\times n$ Matrix

$$
\boxed{
\left(
\frac{n+1}{2},
\frac{n+1}{2}
\right)
}
$$

## Corners

$$
\boxed{
(1,1),(1,n),(n,1),(n,n)
}
$$

## Manhattan Distance

$$
\boxed{
|r_1-r_2|+|c_1-c_2|
}
$$

## Matrix Word Encoding

$$
\boxed{
W_1W_2\ldots W_n
\rightarrow
C_1C_2\ldots C_n
}
$$

where each $C_i$ is the coordinate of $W_i$.

## Coordinate Decoding

$$
\boxed{
(r,c)\rightarrow\text{Element at row }r,\text{ column }c
}
$$

---

# 74. Quick Revision

> [!summary] One-Minute Revision

## Matrix Coding

Think:

$$
\boxed{\text{POSITION}}
$$

A matrix gives every element a location.

The basic coordinate is:

$$
\boxed{(Row,Column)}
$$

### Encoding

Element:

$$
M
$$

Position:

$$
(3,3)
$$

Code:

$$
\boxed{33}
$$

### Decoding

Code:

$$
42
$$

means:

$$
Row=4
$$

$$
Column=2
$$

Locate that cell.

### Must Know

$$
\boxed{\text{Row-Column}}
$$

$$
\boxed{\text{Column-Row}}
$$

$$
\boxed{\text{Same Row}}
$$

$$
\boxed{\text{Same Column}}
$$

$$
\boxed{\text{Main Diagonal}}
$$

$$
\boxed{\text{Opposite Diagonal}}
$$

$$
\boxed{\text{Center}}
$$

$$
\boxed{\text{Corners}}
$$

$$
\boxed{\text{Neighbors}}
$$

$$
\boxed{\text{Rotation}}
$$

$$
\boxed{\text{Reflection}}
$$

### Golden Memory Trick

**"Matrix Coding is a coordinate game: locate the element, read its row and column, and convert that position into the required code."**

# One-Line Recognition

**When a coding question provides a grid or matrix and asks for a code or element, immediately think row-column coordinates and verify the exact coordinate convention before solving.**