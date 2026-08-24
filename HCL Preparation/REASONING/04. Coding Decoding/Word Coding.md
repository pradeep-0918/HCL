---
type: concept
subject: reasoning
topic: "Word Coding"
parent: "04. Coding Decoding"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - coding-decoding
  - word-coding
  - word-pattern
  - logical-reasoning
  - pattern-recognition
  - hcl
wikilinks:
  - "[[04. Coding Decoding]]"
  - "[[Letter Coding]]"
  - "[[Number Coding]]"
  - "[[Substitution Coding]]"
  - "[[Pattern Coding]]"
  - "[[Mixed Coding Decoding]]"
---

# Word Coding

## 1. Core Concept

> [!summary]
> **Word Coding** is a reasoning technique in which complete words are represented by other words, symbols, letters, numbers, or codes according to a hidden relationship.

The most important idea is:

$$
\boxed{\text{Compare the given words and their codes to discover the rule}}
$$

Unlike simple Letter Coding, where individual letters are usually transformed, Word Coding often works at the **word level**.

Example:

If:

$$
CAT \rightarrow DBU
$$

the rule may be letter shifting.

But if:

$$
APPLE \rightarrow FRUIT
$$

the rule may be based on **meaning/category** rather than alphabetic transformation.

Therefore, Word Coding can involve:

- Letter transformation
- Word reversal
- Synonyms
- Categories
- Relationships
- Numerical representation
- Position-based coding
- Substitution
- Rearrangement
- Semantic relationships

---

# 2. Basic Meaning

In a Word Coding problem, the question gives one or more examples of words and their corresponding codes.

Example:

$$
DOG \rightarrow 4
$$

$$
CAT \rightarrow 3
$$

If the code represents the number of letters, then:

$$
DOG=3
$$

not $4$.

Therefore, the given examples must be examined carefully.

Another example:

$$
DOG \rightarrow ANIMAL
$$

Here the relationship is semantic:

$$
DOG\in\text{ANIMAL}
$$

The correct approach depends entirely on the coding rule.

---

# 3. Main Formula

There is no single formula for Word Coding.

Common relationships include:

### Length-Based Coding

$$
\boxed{C=\text{Number of letters}}
$$

### Alphabet-Sum Coding

$$
\boxed{C=\sum \text{alphabet positions}}
$$

### First-Letter Coding

$$
\boxed{C=p_1}
$$

### Last-Letter Coding

$$
\boxed{C=p_n}
$$

### Word Reversal

$$
\boxed{C=C_nC_{n-1}\ldots C_1}
$$

### Letter Shift

$$
\boxed{p'=p+k}
$$

### Reverse Alphabet

$$
\boxed{p'=27-p}
$$

### Position-Based Coding

$$
\boxed{C=f(p_1,p_2,\ldots,p_n)}
$$

---

# 4. Types of Word Coding

| Type | Basic Idea |
|---|---|
| Direct Word Coding | Word is replaced by another word |
| Letter Transformation | Each letter changes |
| Word Reversal | Letter order is reversed |
| Synonym Coding | Word is represented by synonym |
| Category Coding | Word belongs to a category |
| Relationship Coding | Words are connected logically |
| Number Coding | Word becomes a numerical code |
| Position Coding | Code depends on letter positions |
| Substitution Coding | One word/symbol replaces another |
| Rearrangement Coding | Letters are rearranged |
| Pattern Coding | A mathematical/structural pattern is used |
| Mixed Word Coding | Multiple rules are combined |

---

# 5. Important Properties

1. Word Coding may operate on the entire word.
2. The code may preserve the same letters in a different order.
3. The code may change every letter.
4. The code may represent the word's meaning.
5. The code may represent its category.
6. The code may be a number.
7. The code may be another word.
8. The code may depend on word length.
9. The code may depend on first or last letters.
10. The code may use alphabet positions.
11. Different examples may reveal different components of the rule.
12. Some questions use substitution between complete words.
13. Some questions use multiple transformations simultaneously.
14. Context is extremely important in Word Coding.
15. Never assume that every Word Coding problem is alphabetic.

---

# 6. Word Coding vs Letter Coding

| Feature | Letter Coding | Word Coding |
|---|---|---|
| Main Unit | Individual letter | Complete word |
| Common Rule | Shift/reverse | Meaning, substitution, transformation |
| Example | $CAT\rightarrow DBU$ | $DOG\rightarrow ANIMAL$ |
| Focus | Alphabet positions | Word-level relationship |
| Typical Skill | Pattern calculation | Relationship recognition |

> [!important]
> **Letter Coding asks "How did each letter change?"**
>
> **Word Coding asks "How is the whole word represented?"**

---

# 7. How to Solve Word Coding

Use this order:

$$
\boxed{
\text{Meaning}
\rightarrow
\text{Length}
\rightarrow
\text{Letter Pattern}
\rightarrow
\text{Position}
\rightarrow
\text{Rearrangement}
\rightarrow
\text{Numerical Rule}
}
$$

### Step 1

Check whether the code has a meaningful relationship with the word.

### Step 2

Check word length.

### Step 3

Compare letters.

### Step 4

Check first and last letters.

### Step 5

Check reversal/rearrangement.

### Step 6

Convert letters to alphabet positions.

### Step 7

Check arithmetic relationships.

### Step 8

Verify the rule using every example.

---

# 8. Basic Examples

## Example 1 — Word Reversal

### Question

If:

$$
CAT\rightarrow TAC
$$

find the code for:

$$
DOG
$$

### Pattern

The letters are reversed.

$$
CAT\rightarrow TAC
$$

Therefore:

$$
DOG\rightarrow GOD
$$

### Answer

$$
\boxed{GOD}
$$

---

# 9. Example 2 — Same-Length Substitution

Suppose:

$$
BOOK\rightarrow KOO B
$$

The letters may have been rearranged according to a specific position rule.

The important point is to compare:

$$
B,O,O,K
$$

with the coded arrangement.

> [!warning]
> Do not assume reversal unless the exact order confirms it.

---

# 10. Example 3 — Category Coding

### Question

If:

$$
DOG\rightarrow ANIMAL
$$

what category represents:

$$
ROSE
$$

The relationship is:

$$
DOG\in ANIMAL
$$

and:

$$
ROSE\in PLANT
$$

### Answer

$$
\boxed{PLANT}
$$

> [!important]
> This type of question depends on semantic classification, not alphabet arithmetic.

---

# 11. Example 4 — Synonym-Based Coding

Suppose:

$$
HAPPY\rightarrow JOYFUL
$$

The relationship is:

$$
\boxed{\text{Synonym}}
$$

If:

$$
SAD\rightarrow ?
$$

a suitable synonym may be:

$$
\boxed{UNHAPPY}
$$

The exact answer depends on the options and context.

---

# 12. Example 5 — Opposite-Based Coding

Suppose:

$$
HOT\rightarrow COLD
$$

The relationship is:

$$
\boxed{\text{Opposite}}
$$

If:

$$
DAY\rightarrow ?
$$

then:

$$
\boxed{NIGHT}
$$

---

# 13. Example 6 — Alphabet Shift at Word Level

### Question

If:

$$
CAT\rightarrow DBU
$$

find the code for:

$$
DOG
$$

Each letter shifts:

$$
+1
$$

Therefore:

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

Although this looks like Word Coding, the actual mechanism is Letter Coding.

> [!important]
> Always identify the **underlying mechanism**, not just the question title.

---

# 14. Example 7 — Reverse Alphabet Word Coding

If:

$$
CAT\rightarrow XZG
$$

the relationship is:

$$
A\leftrightarrow Z
$$

$$
B\leftrightarrow Y
$$

$$
C\leftrightarrow X
$$

For:

$$
DOG
$$

we get:

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

# 15. Example 8 — Length Coding

Suppose:

$$
CAT\rightarrow3
$$

$$
APPLE\rightarrow5
$$

The code represents word length.

For:

$$
COMPUTER
$$

there are:

$$
8
$$

letters.

### Answer

$$
\boxed{8}
$$

---

# 16. Example 9 — First Letter Coding

Suppose the code is the alphabet position of the first letter.

For:

$$
MANGO
$$

first letter:

$$
M=13
$$

### Answer

$$
\boxed{13}
$$

---

# 17. Example 10 — Last Letter Coding

For:

$$
MANGO
$$

last letter:

$$
O=15
$$

### Answer

$$
\boxed{15}
$$

---

# 18. Example 11 — First + Last Coding

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

Therefore:

$$
13+15=28
$$

### Answer

$$
\boxed{28}
$$

---

# 19. Example 12 — Alphabet Sum

### Question

Find the code for:

$$
DOG
$$

using alphabet-sum coding.

$$
D=4
$$

$$
O=15
$$

$$
G=7
$$

Therefore:

$$
4+15+7=26
$$

### Answer

$$
\boxed{26}
$$

---

# 20. Example 13 — Product Coding

For:

$$
BAD
$$

$$
B=2,\ A=1,\ D=4
$$

Therefore:

$$
2\times1\times4=8
$$

### Answer

$$
\boxed{8}
$$

---

# 21. Example 14 — Reverse Alphabet Sum

For:

$$
DOG
$$

reverse values:

$$
D=23
$$

$$
O=12
$$

$$
G=20
$$

Therefore:

$$
23+12+20=55
$$

### Answer

$$
\boxed{55}
$$

---

# 22. Example 15 — Odd Position Coding

For:

$$
ABCDE
$$

odd-position letters are:

$$
A,C,E
$$

Therefore:

$$
1+3+5=9
$$

### Answer

$$
\boxed{9}
$$

---

# 23. Example 16 — Even Position Coding

For:

$$
ABCDE
$$

even-position letters:

$$
B,D
$$

Therefore:

$$
2+4=6
$$

### Answer

$$
\boxed{6}
$$

---

# 24. Example 17 — Vowel Coding

For:

$$
EDUCATION
$$

vowels:

$$
E,U,A,I,O
$$

Values:

$$
5+21+1+9+15=51
$$

### Answer

$$
\boxed{51}
$$

---

# 25. Example 18 — Consonant Coding

For:

$$
CAT
$$

consonants:

$$
C,T
$$

Therefore:

$$
3+20=23
$$

### Answer

$$
\boxed{23}
$$

---

# 26. Example 19 — Word Rearrangement

Suppose:

$$
TRAIN\rightarrow NITRA
$$

Compare the positions.

Original:

$$
T\ R\ A\ I\ N
$$

Code:

$$
N\ I\ T\ R\ A
$$

This is a rearrangement rather than a simple alphabet shift.

> [!important]
> Write position numbers above the letters:

$$
1\ 2\ 3\ 4\ 5
$$

Then identify where each original position moved.

---

# 27. Example 20 — First and Last Exchange

Suppose:

$$
COLD\rightarrow DOLC
$$

Original:

$$
C\ O\ L\ D
$$

Code:

$$
D\ O\ L\ C
$$

Only the first and last letters are exchanged.

Therefore:

$$
\boxed{1\leftrightarrow n}
$$

For:

$$
MATH
$$

we get:

$$
HAT M
$$

or:

$$
HATM
$$

### Answer

$$
\boxed{HATM}
$$

---

# 28. Example 21 — Adjacent Pair Swapping

Suppose:

$$
COMPUTER
$$

is divided into pairs:

$$
CO|MP|UT|ER
$$

Swap each pair:

$$
OC|PM|TU|RE
$$

Therefore:

$$
\boxed{OCPMTURE}
$$

---

# 29. Example 22 — Odd-Even Rearrangement

For:

$$
COMPUTER
$$

positions:

| Position | Letter |
|---:|---|
| 1 | C |
| 2 | O |
| 3 | M |
| 4 | P |
| 5 | U |
| 6 | T |
| 7 | E |
| 8 | R |

Odd positions:

$$
C,M,U,E
$$

Even positions:

$$
O,P,T,R
$$

Combine:

$$
CMUEOPTR
$$

### Answer

$$
\boxed{CMUEOPTR}
$$

---

# 30. Example 23 — First Half and Second Half Exchange

For:

$$
COMPUTER
$$

split:

$$
COMP|UTER
$$

Exchange:

$$
UTER|COMP
$$

### Answer

$$
\boxed{UTERCOMP}
$$

---

# 31. Example 24 — Reverse Each Half

For:

$$
COMPUTER
$$

split:

$$
COMP|UTER
$$

Reverse each half:

$$
PMOC|RETU
$$

### Answer

$$
\boxed{PMOCRETU}
$$

---

# 32. Example 25 — Reverse Word + Shift

Suppose the rule is:

1. Reverse the word.
2. Shift each letter by $+1$.

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
T\rightarrow U
$$

$$
A\rightarrow B
$$

$$
C\rightarrow D
$$

Therefore:

$$
\boxed{UBD}
$$

---

# 33. Example 26 — Shift + Reverse

Suppose:

1. Shift every letter by $+1$.
2. Reverse the result.

Encode:

$$
DOG
$$

### Step 1

$$
DOG\rightarrow EPH
$$

### Step 2

$$
EPH\rightarrow HPE
$$

### Answer

$$
\boxed{HPE}
$$

---

# 34. Example 27 — Position-Based Shift

Suppose the rule is:

$$
+1,+2,+3,\ldots
$$

Encode:

$$
DOG
$$

### D

$$
D+1=E
$$

### O

$$
O+2=Q
$$

### G

$$
G+3=J
$$

### Answer

$$
\boxed{EQJ}
$$

---

# 35. Example 28 — Alternating Shift

Suppose the rule is:

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

# 36. Example 29 — Word Relationship

### Question

If:

$$
PUPPY\rightarrow DOG
$$

and:

$$
KITTEN\rightarrow ?
$$

The relationship is:

$$
\boxed{\text{Specific animal}\rightarrow\text{General category}}
$$

Therefore:

$$
KITTEN\rightarrow CAT
$$

### Answer

$$
\boxed{CAT}
$$

---

# 37. Example 30 — Object to Category

If:

$$
MANGO\rightarrow FRUIT
$$

then:

$$
CARROT\rightarrow ?
$$

Carrot belongs to:

$$
\boxed{VEGETABLE}
$$

> [!important]
> Semantic Word Coding is solved by understanding relationships, not calculating letter positions.

---

# 38. Example 31 — Profession Relationship

If:

$$
DOCTOR\rightarrow HOSPITAL
$$

then:

$$
TEACHER\rightarrow ?
$$

Possible relationship:

$$
\text{Profession}\rightarrow\text{Workplace}
$$

Therefore:

$$
\boxed{SCHOOL}
$$

---

# 39. Example 32 — Tool and Profession

If:

$$
DOCTOR\rightarrow STETHOSCOPE
$$

then:

$$
CARPENTER\rightarrow ?
$$

Relationship:

$$
\text{Profession}\rightarrow\text{Common tool}
$$

Possible answer:

$$
\boxed{HAMMER}
$$

The exact answer depends on the available choices.

---

# 40. Example 33 — Animal and Sound

If:

$$
DOG\rightarrow BARK
$$

then:

$$
CAT\rightarrow ?
$$

Relationship:

$$
\text{Animal}\rightarrow\text{Sound}
$$

Therefore:

$$
\boxed{MEOW}
$$

---

# 41. Example 34 — Animal and Young One

If:

$$
DOG\rightarrow PUPPY
$$

then:

$$
CAT\rightarrow ?
$$

Relationship:

$$
\text{Animal}\rightarrow\text{Young one}
$$

Therefore:

$$
\boxed{KITTEN}
$$

---

# 42. Example 35 — Country and Capital

If:

$$
INDIA\rightarrow DELHI
$$

then:

$$
FRANCE\rightarrow ?
$$

Relationship:

$$
\text{Country}\rightarrow\text{Capital}
$$

Therefore:

$$
\boxed{PARIS}
$$

---

# 43. Example 36 — State and Capital

If:

$$
TAMIL\ NADU\rightarrow CHENNAI
$$

then:

$$
MAHARASHTRA\rightarrow ?
$$

Relationship:

$$
\text{State}\rightarrow\text{Capital}
$$

Therefore:

$$
\boxed{MUMBAI}
$$

---

# 44. Example 37 — Cause and Effect

If:

$$
RAIN\rightarrow FLOOD
$$

then:

$$
FIRE\rightarrow ?
$$

A possible relationship is:

$$
\text{Cause}\rightarrow\text{Possible effect}
$$

Therefore:

$$
\boxed{SMOKE}
$$

> [!warning]
> Semantic questions can have multiple reasonable relationships. Use the exact relationship established by the question and answer choices.

---

# 45. Example 38 — Object and Material

If:

$$
CHAIR\rightarrow WOOD
$$

then:

$$
BOTTLE\rightarrow ?
$$

Possible relationship:

$$
\text{Object}\rightarrow\text{Common material}
$$

Possible answer:

$$
\boxed{PLASTIC}
$$

depending on context.

---

# 46. Example 39 — Object and Function

If:

$$
KNIFE\rightarrow CUT
$$

then:

$$
PEN\rightarrow ?
$$

Relationship:

$$
\text{Object}\rightarrow\text{Function}
$$

Therefore:

$$
\boxed{WRITE}
$$

---

# 47. Example 40 — Place and Function

If:

$$
SCHOOL\rightarrow EDUCATION
$$

then:

$$
HOSPITAL\rightarrow ?
$$

Relationship:

$$
\text{Place}\rightarrow\text{Primary function}
$$

Therefore:

$$
\boxed{TREATMENT}
$$

---

# 48. Advanced Word Coding Patterns

## Pattern 1 — Category

$$
DOG\rightarrow ANIMAL
$$

Think:

$$
\boxed{\text{Specific}\rightarrow\text{General}}
$$

---

## Pattern 2 — Synonym

$$
HAPPY\rightarrow JOYFUL
$$

Think:

$$
\boxed{\text{Same meaning}}
$$

---

## Pattern 3 — Antonym

$$
HOT\rightarrow COLD
$$

Think:

$$
\boxed{\text{Opposite meaning}}
$$

---

## Pattern 4 — Profession → Workplace

$$
DOCTOR\rightarrow HOSPITAL
$$

Think:

$$
\boxed{\text{Workplace}}
$$

---

## Pattern 5 — Profession → Tool

$$
CARPENTER\rightarrow HAMMER
$$

Think:

$$
\boxed{\text{Tool used}}
$$

---

## Pattern 6 — Animal → Sound

$$
DOG\rightarrow BARK
$$

Think:

$$
\boxed{\text{Sound}}
$$

---

## Pattern 7 — Animal → Young One

$$
CAT\rightarrow KITTEN
$$

Think:

$$
\boxed{\text{Young one}}
$$

---

## Pattern 8 — Country → Capital

$$
INDIA\rightarrow DELHI
$$

Think:

$$
\boxed{\text{Capital}}
$$

---

## Pattern 9 — Object → Function

$$
PEN\rightarrow WRITE
$$

Think:

$$
\boxed{\text{Function}}
$$

---

## Pattern 10 — Object → Material

$$
CHAIR\rightarrow WOOD
$$

Think:

$$
\boxed{\text{Material}}
$$

---

# 49. Structural Word Coding Patterns

> [!important] Must Master

### Pattern 1 — Reverse

$$
ABCDE\rightarrow EDCBA
$$

### Pattern 2 — First/Last Exchange

$$
ABCDE\rightarrow EBCDA
$$

### Pattern 3 — Adjacent Pair Swap

$$
ABCDEFGH\rightarrow BADCFEHG
$$

### Pattern 4 — Odd-Even Arrangement

$$
ABCDEFGH\rightarrow ACEGBDFH
$$

### Pattern 5 — Half Exchange

$$
ABCDEFGH\rightarrow EFGHABCD
$$

### Pattern 6 — Reverse Each Half

$$
ABCDEFGH\rightarrow DCBAHGFE
$$

### Pattern 7 — Shift

$$
A\rightarrow B
$$

### Pattern 8 — Reverse Alphabet

$$
A\rightarrow Z
$$

### Pattern 9 — Position-Based Shift

$$
+1,+2,+3,\ldots
$$

### Pattern 10 — Multiple Transformations

$$
\boxed{\text{Shift}+\text{Reverse}}
$$

---

# 50. Pattern Recognition Tricks

## If the code contains the same letters

> [!important]
> If the letters are unchanged but reordered, think:

$$
\boxed{\text{Rearrangement}}
$$

---

## If every letter changes by the same amount

> [!important]
> Think:

$$
\boxed{\text{Fixed alphabet shift}}
$$

---

## If A becomes Z

> [!important]
> Think:

$$
\boxed{\text{Reverse alphabet}}
$$

---

## If the code has the same number of letters

> [!important]
> Check:

- Letter substitution
- Rearrangement
- Shift
- Reverse

---

## If the code is a number

> [!important]
> Check:

- Length
- Alphabet sum
- Product
- First/last
- Difference
- Reverse sum

---

## If the code is another meaningful word

> [!important]
> Check:

- Category
- Synonym
- Antonym
- Function
- Workplace
- Tool
- Sound
- Capital
- Young one
- Material

---

## If the code looks unrelated

> [!important]
> Check whether the relationship is semantic rather than alphabetic.

---

# 51. Shortcuts

> [!tip]
> **Shortcut 1 — First classify the code**

Ask:

$$
\boxed{\text{Is the code a word, number, or rearrangement?}}
$$

This immediately narrows the possible rules.

---

> [!tip]
> **Shortcut 2 — If letters are preserved, check order**

For:

$$
ABCDE\rightarrow EABCD
$$

the letters are unchanged.

Only the positions changed.

---

> [!tip]
> **Shortcut 3 — If letters are changed uniformly, calculate one shift**

If:

$$
C\rightarrow F
$$

then:

$$
+3
$$

Test the same shift on the remaining letters.

---

> [!tip]
> **Shortcut 4 — If the code is a small number, test length and boundary letters first**

For a small code:

$$
\text{Length}
$$

$$
\text{First-last difference}
$$

may solve the problem quickly.

---

> [!tip]
> **Shortcut 5 — For semantic coding, identify the relationship type**

Instead of asking:

> "What word comes next?"

ask:

> "What relationship connects the two words?"

---

> [!tip]
> **Shortcut 6 — Use a relationship table**

| Word | Code | Relationship |
|---|---|---|
| DOG | ANIMAL | Category |
| DOCTOR | HOSPITAL | Workplace |
| PEN | WRITE | Function |
| DOG | BARK | Sound |

Once the relationship is known, the answer becomes easier.

---

> [!tip]
> **Shortcut 7 — Check first/last positions**

For structural coding, write:

$$
1,2,3,\ldots,n
$$

above the letters and track where each position moves.

---

> [!tip]
> **Shortcut 8 — Verify using all examples**

The fastest wrong method is one that fits only one example.

---

# 52. Common Exam Patterns

> [!important] Must Master

### Alphabetic

1. Fixed shift
2. Reverse alphabet
3. Cyclic shift
4. Position-based shift
5. Alternating shift

### Rearrangement

6. Reverse word
7. First-last exchange
8. Adjacent pair exchange
9. Odd-even arrangement
10. Half exchange
11. Reverse each half

### Numerical

12. Word length
13. Alphabet sum
14. Product
15. Difference
16. First-letter value
17. Last-letter value
18. Reverse alphabet sum
19. Weighted sum
20. Digit reduction

### Semantic

21. Category
22. Synonym
23. Antonym
24. Profession-workplace
25. Profession-tool
26. Animal-sound
27. Animal-young one
28. Country-capital
29. State-capital
30. Object-function
31. Object-material
32. Cause-effect
33. Place-function
34. Part-whole

### Advanced

35. Multiple transformations
36. Numerical + alphabetic coding
37. Rearrangement + shift
38. Semantic + substitution
39. Multi-condition coding
40. Complex word relationships

---

# 53. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Assuming all Word Coding is alphabetic

Some questions are semantic.

Example:

$$
DOG\rightarrow ANIMAL
$$

does not require alphabet arithmetic.

---

### Mistake 2 — Confusing synonym and category

$$
DOG\rightarrow ANIMAL
$$

is category.

$$
HAPPY\rightarrow JOYFUL
$$

is synonym.

---

### Mistake 3 — Confusing category and function

$$
DOG\rightarrow ANIMAL
$$

is category.

$$
PEN\rightarrow WRITE
$$

is function.

---

### Mistake 4 — Assuming reversal

If letters are rearranged, determine the exact position movement.

---

### Mistake 5 — Ignoring word length

Length may be the entire coding rule.

---

### Mistake 6 — Looking only at the first example

A pattern must work across all examples.

---

### Mistake 7 — Using an unnecessarily complicated rule

Always test simple transformations first.

---

### Mistake 8 — Confusing reverse alphabet and reverse word

Reverse alphabet:

$$
CAT\rightarrow XZG
$$

Reverse word:

$$
CAT\rightarrow TAC
$$

---

### Mistake 9 — Ignoring answer choices

In reasoning exams, answer choices can help eliminate impossible interpretations when multiple rules initially seem possible.

---

### Mistake 10 — Overthinking semantic relationships

Use the most direct relationship supported by the question.

---

# 54. Advanced Example — Complete Analysis

## Example 41

### Question

Suppose:

$$
CAT\rightarrow DBU
$$

$$
DOG\rightarrow EPH
$$

Find the code for:

$$
BAT
$$

### Step 1 — Compare CAT

$$
C\rightarrow D
$$

$$
A\rightarrow B
$$

$$
T\rightarrow U
$$

Rule:

$$
+1
$$

### Step 2 — Verify with DOG

$$
D\rightarrow E
$$

$$
O\rightarrow P
$$

$$
G\rightarrow H
$$

Again:

$$
+1
$$

### Step 3 — Encode BAT

$$
B\rightarrow C
$$

$$
A\rightarrow B
$$

$$
T\rightarrow U
$$

### Answer

$$
\boxed{CBU}
$$

---

# 55. Advanced Example — Multiple Rules

## Example 42

Suppose:

$$
CAT\rightarrow UBD
$$

### Step 1

Reverse:

$$
CAT\rightarrow TAC
$$

### Step 2

Shift:

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
\boxed{\text{Reverse +1 shift}}
$$

For:

$$
DOG
$$

reverse:

$$
GOD
$$

shift:

$$
G+1=H
$$

$$
O+1=P
$$

$$
D+1=E
$$

### Answer

$$
\boxed{HPE}
$$

---

# 56. Advanced Example — Mixed Numerical and Structural Rule

## Example 43

Suppose:

$$
CAT\rightarrow 24
$$

$$
DOG\rightarrow 26
$$

Find the code for:

$$
BAT
$$

### Check Alphabet Sum

CAT:

$$
3+1+20=24
$$

DOG:

$$
4+15+7=26
$$

Therefore the rule is confirmed.

BAT:

$$
2+1+20=23
$$

### Answer

$$
\boxed{23}
$$

---

# 57. Advanced Example — Multiple Semantic Relationships

Suppose:

$$
DOG\rightarrow BARK
$$

$$
CAT\rightarrow MEOW
$$

$$
COW\rightarrow ?
$$

The relationship is:

$$
\boxed{\text{Animal}\rightarrow\text{Sound}}
$$

Therefore:

$$
\boxed{MOO}
$$

---

# 58. Advanced Example — Category Relationship

Suppose:

$$
MANGO\rightarrow FRUIT
$$

$$
CARROT\rightarrow VEGETABLE
$$

$$
ROSE\rightarrow ?
$$

The relationship is:

$$
\boxed{\text{Object}\rightarrow\text{Category}}
$$

Rose belongs to:

$$
\boxed{FLOWER}
$$

---

# 59. Advanced Example — Workplace Relationship

Suppose:

$$
DOCTOR\rightarrow HOSPITAL
$$

$$
TEACHER\rightarrow SCHOOL
$$

$$
JUDGE\rightarrow ?
$$

Relationship:

$$
\boxed{\text{Profession}\rightarrow\text{Workplace}}
$$

Possible answer:

$$
\boxed{COURT}
$$

---

# 60. Advanced Example — Tool Relationship

Suppose:

$$
DOCTOR\rightarrow STETHOSCOPE
$$

$$
CARPENTER\rightarrow HAMMER
$$

$$
PHOTOGRAPHER\rightarrow ?
$$

Relationship:

$$
\boxed{\text{Profession}\rightarrow\text{Common tool}}
$$

Possible answer:

$$
\boxed{CAMERA}
$$

---

# 61. Formula Sheet

## Alphabet Position

$$
\boxed{A=1,\ldots,Z=26}
$$

## Word Length

$$
\boxed{C=n}
$$

## Alphabet Sum

$$
\boxed{C=\sum_{i=1}^{n}p_i}
$$

## Product

$$
\boxed{C=\prod_{i=1}^{n}p_i}
$$

## First Letter

$$
\boxed{C=p_1}
$$

## Last Letter

$$
\boxed{C=p_n}
$$

## First + Last

$$
\boxed{C=p_1+p_n}
$$

## First-Last Difference

$$
\boxed{C=|p_1-p_n|}
$$

## Reverse Alphabet

$$
\boxed{p'=27-p}
$$

## Reverse Sum

$$
\boxed{C=27n-\sum p_i}
$$

## Weighted Coding

$$
\boxed{C=\sum_{i=1}^{n}i\,p_i}
$$

## Reverse Word

$$
\boxed{C_1C_2\ldots C_n\rightarrow C_n\ldots C_2C_1}
$$

---

# 62. Quick Revision

> [!summary] One-Minute Revision

## Word Coding

The fastest approach:

$$
\boxed{
\text{Classify Code}
\rightarrow
\text{Identify Relationship}
\rightarrow
\text{Apply Rule}
\rightarrow
\text{Verify}
}
$$

### If Code Is a Word

Check:

$$
\boxed{\text{Category}}
$$

$$
\boxed{\text{Synonym}}
$$

$$
\boxed{\text{Antonym}}
$$

$$
\boxed{\text{Function}}
$$

$$
\boxed{\text{Workplace}}
$$

$$
\boxed{\text{Tool}}
$$

$$
\boxed{\text{Sound}}
$$

$$
\boxed{\text{Capital}}
$$

### If Code Is Letters

Check:

$$
\boxed{\text{Shift}}
$$

$$
\boxed{\text{Reverse}}
$$

$$
\boxed{\text{Rearrangement}}
$$

$$
\boxed{\text{Reverse Alphabet}}
$$

### If Code Is a Number

Check:

$$
\boxed{\text{Length}}
$$

$$
\boxed{\text{Alphabet Sum}}
$$

$$
\boxed{\text{Product}}
$$

$$
\boxed{\text{Difference}}
$$

$$
\boxed{\text{First/Last}}
$$

$$
\boxed{\text{Selected Positions}}
$$

### Most Important Distinctions

$$
DOG\rightarrow ANIMAL
$$

means:

$$
\boxed{\text{Category}}
$$

$$
HAPPY\rightarrow JOYFUL
$$

means:

$$
\boxed{\text{Synonym}}
$$

$$
HOT\rightarrow COLD
$$

means:

$$
\boxed{\text{Antonym}}
$$

$$
DOG\rightarrow BARK
$$

means:

$$
\boxed{\text{Sound}}
$$

$$
PEN\rightarrow WRITE
$$

means:

$$
\boxed{\text{Function}}
$$

$$
CAT\rightarrow TAC
$$

means:

$$
\boxed{\text{Reverse}}
$$

$$
CAT\rightarrow DBU
$$

means:

$$
\boxed{+1\text{ shift}}
$$

### Golden Memory Trick

**"First identify what kind of code you are looking at—meaning, number, substitution, or rearrangement—then find the simplest rule that explains every example."**

# One-Line Recognition

**When a complete word is converted into another word, number, or code, first determine the relationship type before doing calculations.**