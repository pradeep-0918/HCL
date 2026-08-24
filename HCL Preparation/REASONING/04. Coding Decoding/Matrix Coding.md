---
type: concept
subject: reasoning
topic: "Matrix Coding"
parent: "04. Coding Decoding"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - coding-decoding
  - matrix-coding
  - matrix
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
> **Matrix Coding** is a coding-decoding method in which letters, numbers, symbols, or words are represented using positions inside a matrix or grid. The code is usually determined by identifying the correct row, column, cell, or coordinate.

The central idea is:

$$
\boxed{\text{Item}\rightarrow\text{Matrix Position}\rightarrow\text{Code}}
$$

A matrix may look like:

|  | Column 1 | Column 2 | Column 3 | Column 4 |
|---|---|---|---|---|
| Row 1 | A | B | C | D |
| Row 2 | E | F | G | H |
| Row 3 | I | J | K | L |
| Row 4 | M | N | O | P |

Here:

$$
A=(1,1)
$$

$$
F=(2,2)
$$

$$
K=(3,3)
$$

$$
P=(4,4)
$$

Depending on the question, the code may be:

- Row number
- Column number
- Row-column pair
- A combination of coordinates
- A number assigned to each cell
- A symbol corresponding to a cell
- Multiple coordinates for one character

The key skill is:

$$
\boxed{\text{Locate first, encode second}}
$$

---

# 2. Basic Meaning

A matrix is an arrangement of elements in:

- Rows
- Columns
- Cells

For example:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

The position of:

$$
A=(1,1)
$$

The position of:

$$
E=(2,2)
$$

The position of:

$$
I=(3,3)
$$

If the coding rule is:

$$
\boxed{\text{Code}=\text{Row, Column}}
$$

then:

$$
A\rightarrow11
$$

$$
E\rightarrow22
$$

$$
I\rightarrow33
$$

---

# 3. Main Formula

For a matrix element at row $r$ and column $c$:

$$
\boxed{\text{Code}=(r,c)}
$$

If row and column are written together:

$$
\boxed{\text{Code}=rc}
$$

Example:

If:

$$
B=(1,2)
$$

then:

$$
\boxed{B\rightarrow12}
$$

If:

$$
H=(3,2)
$$

then:

$$
\boxed{H\rightarrow32}
$$

---

# 4. Important Properties

1. A matrix contains rows and columns.
2. Each cell has a unique position.
3. The same element should normally have the same coordinate.
4. Row is usually written before column.
5. Some questions reverse the order and use column-row.
6. Always read the coding rule before solving.
7. A matrix may contain letters, numbers, words, or symbols.
8. Some matrices use two-digit codes.
9. Some use three-digit or multi-part coordinates.
10. Some questions use separate row and column labels.
11. Some questions use symbols as row/column identifiers.
12. Some questions require finding the code of a word.
13. Some questions require decoding a coordinate.
14. Some questions use multiple matrices.
15. Some questions use repeated letters or symbols.
16. A matrix may be rectangular rather than square.
17. Some problems require combining coordinates.
18. Some problems use a second matrix for additional coding.
19. The most common mistake is swapping row and column.
20. The safest method is to physically locate the item before writing its code.

---

# 5. Matrix Terminology

| Term | Meaning |
|---|---|
| Row | Horizontal arrangement |
| Column | Vertical arrangement |
| Cell | Individual position |
| Coordinate | Row-column location |
| Row Index | Position of row |
| Column Index | Position of column |
| Matrix | Complete grid |
| Coordinate Code | Code based on position |

Example:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

For $F$:

- Row = $2$
- Column = $3$
- Coordinate = $(2,3)$

Therefore:

$$
\boxed{F\rightarrow23}
$$

---

# 6. Matrix Coding vs Other Coding Types

| Type | Main Idea |
|---|---|
| Letter Coding | Transform letters |
| Number Coding | Convert items into numbers |
| Word Coding | Replace words |
| Substitution Coding | Artificial replacement |
| Pattern Coding | Apply a transformation pattern |
| Chinese Coding | Decode unknown-language mappings |
| Matrix Coding | Use row/column/cell positions |

> [!important]
> In Matrix Coding, **position is usually more important than the meaning of the item**.

---

# 7. Basic Matrix

Consider:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

The coordinates are:

| Letter | Coordinate |
|---|---|
| A | 11 |
| B | 12 |
| C | 13 |
| D | 21 |
| E | 22 |
| F | 23 |
| G | 31 |
| H | 32 |
| I | 33 |

---

# 8. Example 1 — Direct Coordinate Coding

### Question

Using:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Find the code for $E$.

### Step 1

Locate E.

It is in:

$$
\text{Row}=2
$$

$$
\text{Column}=2
$$

Therefore:

$$
E=(2,2)
$$

### Answer

$$
\boxed{22}
$$

---

# 9. Example 2 — Code for H

Using the same matrix:

$H$ is located at:

$$
\text{Row}=3
$$

$$
\text{Column}=2
$$

Therefore:

$$
\boxed{H\rightarrow32}
$$

---

# 10. Example 3 — Code for C

$C$ is located at:

$$
(1,3)
$$

Therefore:

$$
\boxed{13}
$$

---

# 11. Example 4 — Decode a Coordinate

Using:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Decode:

$$
31
$$

Interpret:

$$
3=\text{Row}
$$

$$
1=\text{Column}
$$

Cell:

$$
(3,1)
$$

contains:

$$
G
$$

### Answer

$$
\boxed{G}
$$

---

# 12. Example 5 — Decode 23

Coordinate:

$$
(2,3)
$$

Look at row $2$, column $3$:

$$
F
$$

### Answer

$$
\boxed{F}
$$

---

# 13. Example 6 — Encode a Word

Using:

|  | 1 | 2 | 3 |
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
B=12
$$

$$
A=11
$$

$$
D=21
$$

Therefore:

$$
\boxed{12\ 11\ 21}
$$

---

# 14. Example 7 — Decode Multiple Codes

Using the same matrix:

Decode:

$$
13\ 22\ 31
$$

Mappings:

$$
13=C
$$

$$
22=E
$$

$$
31=G
$$

### Answer

$$
\boxed{CEG}
$$

---

# 15. Example 8 — Larger Matrix

Consider:

|  | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | A | B | C | D |
| 2 | E | F | G | H |
| 3 | I | J | K | L |
| 4 | M | N | O | P |

Find the code for:

$$
K
$$

K is at:

$$
(3,3)
$$

Therefore:

$$
\boxed{33}
$$

---

# 16. Example 9 — Encode WORD

Using:

|  | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | A | B | C | D |
| 2 | E | F | G | H |
| 3 | I | J | K | L |
| 4 | M | N | O | P |

The letters are:

- W → not present
- O → 43
- R → not present
- D → 14

Therefore, if a letter is absent:

$$
\boxed{\text{It cannot be encoded using this matrix}}
$$

> [!warning]
> Never assume a missing letter has a code unless the question provides another matrix or rule.

---

# 17. Example 10 — Row-Column Labels

Consider:

|  | A | B | C |
|---|---|---|---|
| P | 1 | 2 | 3 |
| Q | 4 | 5 | 6 |
| R | 7 | 8 | 9 |

Here:

- Rows are $P,Q,R$
- Columns are $A,B,C$

The cell containing $5$ is:

$$
(Q,B)
$$

Therefore:

$$
\boxed{5\rightarrow QB}
$$

if the code is row-column.

---

# 18. Example 11 — Letter Labels

Consider:

|  | X | Y | Z |
|---|---|---|---|
| A | P | Q | R |
| B | S | T | U |
| C | V | W | X |

Find the coordinate of $T$.

$T$ is in:

$$
\text{Row}=B
$$

$$
\text{Column}=Y
$$

Therefore:

$$
\boxed{BY}
$$

---

# 19. Example 12 — Column-Row Coding

Suppose the question explicitly states:

> Code is written as column followed by row.

Using:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

For $H$:

$$
\text{Row}=3
$$

$$
\text{Column}=2
$$

Normally:

$$
32
$$

But the question requires column-row:

$$
23
$$

### Answer

$$
\boxed{23}
$$

> [!warning]
> Never assume the order of coordinates. Read the instructions.

---

# 20. Example 13 — Matrix With Numbers

Consider:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | 11 | 12 | 13 |
| 2 | 21 | 22 | 23 |
| 3 | 31 | 32 | 33 |

The cell code is directly equal to its coordinate.

For row $2$, column $3$:

$$
\boxed{23}
$$

---

# 21. Example 14 — Matrix With Symbols

Consider:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | @ | # | \$ |
| 2 | % | & | * |
| 3 | + | - | / |

Find the code for `&`.

It is at:

$$
(2,2)
$$

Therefore:

$$
\boxed{22}
$$

---

# 22. Example 15 — Decode Symbol Code

Using the same matrix, decode:

$$
31
$$

At row $3$, column $1$:

$$
+
$$

### Answer

$$
\boxed{+}
$$

---

# 23. Example 16 — Matrix Word Coding

Consider:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | CAT | DOG | COW |
| 2 | ANT | FOX | BAT |
| 3 | HEN | PIG | RAT |

Find the code for:

$$
FOX
$$

FOX is at:

$$
(2,2)
$$

Therefore:

$$
\boxed{22}
$$

---

# 24. Example 17 — Decode Word From Coordinate

Using the same matrix:

Decode:

$$
31
$$

Row $3$, column $1$ contains:

$$
HEN
$$

### Answer

$$
\boxed{HEN}
$$

---

# 25. Example 18 — Multiple Word Encoding

Using:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | CAT | DOG | COW |
| 2 | ANT | FOX | BAT |
| 3 | HEN | PIG | RAT |

Encode:

$$
DOG\ BAT\ PIG
$$

Mappings:

$$
DOG=12
$$

$$
BAT=23
$$

$$
PIG=32
$$

### Answer

$$
\boxed{12\ 23\ 32}
$$

---

# 26. Example 19 — Row-Based Coding

Suppose the question says:

> The first digit represents the row.

Using:

|  | 1 | 2 | 3 |
|---|---|---|---|
| 1 | A | B | C |
| 2 | D | E | F |
| 3 | G | H | I |

Then:

$$
F=23
$$

because:

$$
F\in\text{Row 2, Column 3}
$$

---

# 27. Example 20 — Column-Based Coding

Suppose:

> The first digit represents the column.

For $F$:

$$
\text{Column}=3
$$

$$
\text{Row}=2
$$

Therefore:

$$
\boxed{32}
$$

---

# 28. Matrix Coding With Coordinates

A common exam format is:

```text
A = 11
B = 12
C = 13
D = 21
E = 22
F = 23
...