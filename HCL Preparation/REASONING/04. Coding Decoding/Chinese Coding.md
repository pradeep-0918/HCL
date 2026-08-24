---
type: concept
subject: reasoning
topic: "Chinese Coding"
parent: "04. Coding Decoding"
company: HCL
difficulty: hard
priority: very-high
status: not-started
tags:
  - reasoning
  - coding-decoding
  - chinese-coding
  - coded-language
  - logical-reasoning
  - word-coding
  - pattern-recognition
  - hcl
wikilinks:
  - "[[04. Coding Decoding]]"
  - "[[Letter Coding]]"
  - "[[Number Coding]]"
  - "[[Word Coding]]"
  - "[[Substitution Coding]]"
  - "[[Pattern Coding]]"
  - "[[Matrix Coding]]"
  - "[[Mixed Coding Decoding]]"
---

# Chinese Coding

## 1. Core Concept

> [!summary]
> **Chinese Coding** is a coded-language reasoning problem in which words or phrases are represented by artificial words or codes. The original meaning of the artificial codes is unknown, so the solver must decode them by comparing multiple statements.

The central idea is:

$$
\boxed{\text{Compare common words} \leftrightarrow \text{common codes}}
$$

Example:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

The common original word is:

$$
RED
$$

The common code is:

$$
KA
$$

Therefore:

$$
\boxed{RED=KA}
$$

Then:

$$
FLOWER=TI
$$

$$
CAR=MO
$$

This is the fundamental technique behind Chinese Coding.

---

# 2. Basic Meaning

Chinese Coding does **not** usually mean that the question requires knowledge of the Chinese language.

The term refers to a **coded-language reasoning format**.

The question gives artificial codes such as:

$$
KA,\ TI,\ MO,\ ZU
$$

These codes have no inherent meaning.

Your task is to determine which code corresponds to which original word.

For example:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

From comparison:

$$
RED=KA
$$

$$
FLOWER=TI
$$

$$
CAR=MO
$$

Therefore:

$$
\boxed{\text{Chinese Coding = Common Word + Common Code + Elimination}}
$$

---

# 3. Main Formula

There is no mathematical formula for Chinese Coding.

The fundamental relationship is:

$$
\boxed{\text{Common Word} \leftrightarrow \text{Common Code}}
$$

For two statements:

$$
A+B \rightarrow X+Y
$$

$$
A+C \rightarrow X+Z
$$

The common elements reveal:

$$
\boxed{A=X}
$$

Then:

$$
\boxed{B=Y}
$$

and:

$$
\boxed{C=Z}
$$

---

# 4. Core Solving Principle

Use:

$$
\boxed{
\text{Compare}
\rightarrow
\text{Find Common Element}
\rightarrow
\text{Assign Code}
\rightarrow
\text{Eliminate}
\rightarrow
\text{Decode}
}
$$

### Most Important Rule

If the same original word appears in two statements, the code associated with that common word should also appear in both statements, assuming a standard one-to-one coding system.

Example:

$$
A+B\rightarrow X+Y
$$

$$
A+C\rightarrow X+Z
$$

Common original:

$$
A
$$

Common code:

$$
X
$$

Therefore:

$$
\boxed{A=X}
$$

---

# 5. Important Properties

1. The codes are artificial.
2. The code usually has no natural meaning.
3. Multiple statements are normally required.
4. Repeated words are extremely important.
5. Repeated codes are equally important.
6. Common-word comparison is the fastest method.
7. Common-code comparison can solve decoding questions.
8. Elimination is useful when most mappings are known.
9. Word order is usually preserved unless stated otherwise.
10. The same word normally has the same code throughout a question.
11. The same code normally represents the same word in standard questions.
12. Unknown mappings should not be invented.
13. A mapping table reduces mistakes.
14. Longer statements often provide more information.
15. The question may ask for encoding or decoding.
16. Some questions involve repeated words.
17. Some questions involve three or more words.
18. Some questions provide incomplete information.
19. "Cannot be determined" can be the correct answer when information is insufficient.
20. Chinese Coding is primarily a **logical comparison problem**, not a mathematical calculation problem.

---

# 6. Chinese Coding vs Other Coding Types

| Topic | Main Technique |
|---|---|
| Letter Coding | Transform letters |
| Number Coding | Convert letters/words to numbers |
| Word Coding | Identify word-level relationships |
| Substitution Coding | Direct replacement |
| Pattern Coding | Discover mathematical/structural pattern |
| Chinese Coding | Compare coded phrases |
| Matrix Coding | Locate code using rows/columns |
| Mixed Coding | Combine multiple coding methods |

> [!important]
> Chinese Coding is best remembered as:
>
> $$\boxed{\text{Common Word} \leftrightarrow \text{Common Code}}$$

---

# 7. Standard Chinese Coding Format

A typical question looks like:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

The question may ask:

- What is the code for RED?
- What is the code for BLUE?
- What does TI mean?
- What is the code for BLUE FLOWER?
- What does ZU TI represent?
- Which code represents CAR?

---

# 8. Basic Example — Two Statements

## Example 1

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

Find the code for RED.

### Step 1

Find the common original word:

$$
RED
$$

### Step 2

Find the common code:

$$
KA
$$

Therefore:

$$
\boxed{RED=KA}
$$

---

# 9. Example 2 — Find the Code for Flower

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

From the first statement:

$$
RED=KA
$$

Therefore the remaining code is:

$$
FLOWER=TI
$$

### Answer

$$
\boxed{TI}
$$

---

# 10. Example 3 — Find the Code for Car

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

The common word is RED.

Therefore:

$$
RED=KA
$$

The remaining code in the second statement is:

$$
CAR=MO
$$

### Answer

$$
\boxed{MO}
$$

---

# 11. Example 4 — Three Statements

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

Find the code for BLUE.

Compare statements 2 and 3.

Common word:

$$
CAR
$$

Common code:

$$
MO
$$

Therefore:

$$
CAR=MO
$$

The remaining pair in statement 3 is:

$$
BLUE=ZU
$$

### Answer

$$
\boxed{ZU}
$$

---

# 12. Example 5 — Find the Code for Blue Flower

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

We have:

$$
BLUE=ZU
$$

and:

$$
FLOWER=TI
$$

Therefore:

$$
BLUE\ FLOWER
\rightarrow
ZU\ TI
$$

### Answer

$$
\boxed{ZU\ TI}
$$

---

# 13. Example 6 — Decode a Code

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{red car} \rightarrow \text{ka mo}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

What does:

$$
ZU\ TI
$$

represent?

We know:

$$
ZU=BLUE
$$

$$
TI=FLOWER
$$

Therefore:

$$
\boxed{BLUE\ FLOWER}
$$

---

# 14. Example 7 — Common Code Method

Given:

$$
\text{cat dog} \rightarrow \text{ma po}
$$

$$
\text{dog bird} \rightarrow \text{po ti}
$$

Find the code for DOG.

Common original word:

$$
DOG
$$

Common code:

$$
PO
$$

Therefore:

$$
\boxed{DOG=PO}
$$

---

# 15. Example 8 — Reverse Common-Code Method

Given:

$$
\text{cat dog} \rightarrow \text{ma po}
$$

$$
\text{dog bird} \rightarrow \text{po ti}
$$

What word is represented by:

$$
PO
$$

Since:

$$
DOG=PO
$$

the answer is:

$$
\boxed{DOG}
$$

---

# 16. Example 9 — Three-Word Statement

Given:

$$
\text{red big car} \rightarrow \text{ka po mo}
$$

$$
\text{red small car} \rightarrow \text{ka ti mo}
$$

Find the code for BIG.

Common words:

$$
RED,\ CAR
$$

Common codes:

$$
KA,\ MO
$$

The remaining pair is:

$$
BIG=PO
$$

### Answer

$$
\boxed{PO}
$$

---

# 17. Example 10 — Three-Word Decoding

Given:

$$
\text{red big car} \rightarrow \text{ka po mo}
$$

$$
\text{red small car} \rightarrow \text{ka ti mo}
$$

Find the meaning of:

$$
KA\ TI\ MO
$$

Mappings:

$$
KA=RED
$$

$$
TI=SMALL
$$

$$
MO=CAR
$$

Therefore:

$$
\boxed{RED\ SMALL\ CAR}
$$

---

# 18. Example 11 — Four Words

Given:

$$
\text{red big car} \rightarrow \text{ka po mo}
$$

$$
\text{blue big car} \rightarrow \text{zu po mo}
$$

$$
\text{blue small bike} \rightarrow \text{zu ti lu}
$$

Find the code for RED SMALL BIKE.

### Step 1

Compare first and second:

Common words:

$$
BIG,\ CAR
$$

Common codes:

$$
PO,\ MO
$$

Therefore:

$$
RED=KA
$$

$$
BLUE=ZU
$$

### Step 2

Compare second and third.

Common word:

$$
BLUE
$$

Common code:

$$
ZU
$$

The remaining mappings give:

$$
SMALL=TI
$$

$$
BIKE=LU
$$

### Step 3

Encode:

$$
RED\ SMALL\ BIKE
$$

$$
KA\ TI\ LU
$$

### Answer

$$
\boxed{KA\ TI\ LU}
$$

---

# 19. Example 12 — Chain of Statements

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{blue flower} \rightarrow \text{zu ti}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

$$
\text{green car} \rightarrow \text{pa mo}
$$

Find the code for GREEN.

Compare:

$$
BLUE\ CAR\rightarrow ZU\ MO
$$

$$
GREEN\ CAR\rightarrow PA\ MO
$$

Common word:

$$
CAR
$$

Common code:

$$
MO
$$

Therefore:

$$
GREEN=PA
$$

### Answer

$$
\boxed{PA}
$$

---

# 20. Example 13 — Full Mapping

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{blue flower} \rightarrow \text{zu ti}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

$$
\text{green car} \rightarrow \text{pa mo}
$$

Build the mapping.

| Original Word | Code |
|---|---|
| Red | KA |
| Blue | ZU |
| Green | PA |
| Flower | TI |
| Car | MO |

Now encode:

$$
GREEN\ FLOWER
$$

Therefore:

$$
\boxed{PA\ TI}
$$

---

# 21. Example 14 — Word Order

Given:

$$
\text{red blue} \rightarrow \text{ka zu}
$$

Then:

$$
\text{blue red}
$$

becomes:

$$
\boxed{zu\ ka}
$$

The mappings are:

$$
RED=KA
$$

$$
BLUE=ZU
$$

The order changes because the input order changes.

---

# 22. Example 15 — Same Word Repeated

Given:

$$
\text{red red blue} \rightarrow \text{ka ka zu}
$$

The repeated original word is:

$$
RED
$$

The repeated code is:

$$
KA
$$

Therefore:

$$
\boxed{RED=KA}
$$

and:

$$
\boxed{BLUE=ZU}
$$

---

# 23. Example 16 — Repeated Code

Given:

$$
\text{red blue} \rightarrow \text{ka zu}
$$

$$
\text{green blue} \rightarrow \text{pa zu}
$$

The repeated code is:

$$
ZU
$$

The repeated original word is:

$$
BLUE
$$

Therefore:

$$
\boxed{BLUE=ZU}
$$

---

# 24. Example 17 — Elimination

Given:

$$
\text{red blue green} \rightarrow \text{ka zu mo}
$$

Suppose we already know:

$$
RED=KA
$$

$$
BLUE=ZU
$$

Then the remaining mapping must be:

$$
GREEN=MO
$$

### Answer

$$
\boxed{MO}
$$

---

# 25. Example 18 — Multiple Unknowns

Given:

$$
\text{red blue green} \rightarrow \text{ka zu mo}
$$

$$
\text{red yellow green} \rightarrow \text{ka pa mo}
$$

Find the code for YELLOW.

Common words:

$$
RED,\ GREEN
$$

Common codes:

$$
KA,\ MO
$$

Remaining pair:

$$
YELLOW=PA
$$

### Answer

$$
\boxed{PA}
$$

---

# 26. Example 19 — Decode a Three-Code Phrase

Given:

$$
\text{red blue green} \rightarrow \text{ka zu mo}
$$

$$
\text{red yellow green} \rightarrow \text{ka pa mo}
$$

Decode:

$$
PA\ ZU\ KA
$$

Mappings:

$$
PA=YELLOW
$$

$$
ZU=BLUE
$$

$$
KA=RED
$$

Therefore:

$$
\boxed{YELLOW\ BLUE\ RED}
$$

---

# 27. Example 20 — Four Statements

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{blue flower} \rightarrow \text{zu ti}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

$$
\text{green bike} \rightarrow \text{pa lu}
$$

Can we determine the code for GREEN?

The fourth statement contains:

$$
GREEN\ BIKE\rightarrow PA\ LU
$$

But there is no repeated word linking GREEN or BIKE to another statement.

Therefore, we can identify the pair only if position matching is guaranteed by the problem.

Without such confirmation:

$$
\boxed{\text{The individual mapping cannot be independently confirmed}}
$$

> [!important]
> Do not assume pair positions automatically determine word-code mappings unless the question format guarantees that correspondence.

---

# 28. Common-Word Method

This is the most important technique.

Suppose:

$$
A+B\rightarrow X+Y
$$

$$
A+C\rightarrow X+Z
$$

Then:

$$
A=X
$$

and:

$$
B=Y
$$

$$
C=Z
$$

### Memory Rule

> [!important]
> **Same word → Same code**

and:

> [!important]
> **Same code → Same word**

in standard one-to-one Chinese Coding questions.

---

# 29. Common-Code Method

Suppose:

$$
A+B\rightarrow X+Y
$$

$$
C+B\rightarrow Z+Y
$$

The common original word is:

$$
B
$$

The common code is:

$$
Y
$$

Therefore:

$$
\boxed{B=Y}
$$

---

# 30. Elimination Method

Suppose:

$$
A+B+C\rightarrow X+Y+Z
$$

and you already know:

$$
A=X
$$

$$
B=Y
$$

Then:

$$
\boxed{C=Z}
$$

This is especially useful for long statements.

---

# 31. Mapping Table Method

Always create a table when the problem has more than two statements.

Example:

| Word | Code |
|---|---|
| Red | KA |
| Blue | ZU |
| Green | PA |
| Flower | TI |
| Car | MO |
| Bike | LU |

Then questions become direct lookups.

For:

$$
BLUE\ BIKE
$$

use:

$$
BLUE=ZU
$$

$$
BIKE=LU
$$

Therefore:

$$
\boxed{ZU\ LU}
$$

---

# 32. Pattern Recognition

## Pattern 1 — Two Statements Differ by One Word

> [!important]
> If:

$$
A+B\rightarrow X+Y
$$

$$
A+C\rightarrow X+Z
$$

the shared word/code pair is immediately visible.

Think:

$$
\boxed{A=X}
$$

---

## Pattern 2 — Two Statements Share Two Words

> [!important]
> If:

$$
A+B+C\rightarrow X+Y+Z
$$

$$
A+B+D\rightarrow X+Y+W
$$

then the common mappings are:

$$
A=X
$$

$$
B=Y
$$

The remaining pair gives:

$$
C=Z
$$

$$
D=W
$$

---

## Pattern 3 — Only One Word Changes

This is the easiest case.

Example:

$$
RED\ BLUE\rightarrow KA\ ZU
$$

$$
RED\ GREEN\rightarrow KA\ MO
$$

The changed word:

$$
BLUE\rightarrow GREEN
$$

corresponds to:

$$
ZU\rightarrow MO
$$

---

## Pattern 4 — Only One Code Changes

Same principle in reverse.

If:

$$
A+B\rightarrow X+Y
$$

$$
C+B\rightarrow Z+Y
$$

then:

$$
B=Y
$$

---

## Pattern 5 — Three-Word Statements

Use common elements first.

$$
A+B+C\rightarrow X+Y+Z
$$

Compare with:

$$
A+D+C\rightarrow X+W+Z
$$

Common mappings:

$$
A=X
$$

$$
C=Z
$$

Remaining:

$$
B=Y
$$

$$
D=W
$$

---

# 33. Shortcuts

> [!tip]
> **Shortcut 1 — Compare the shortest statements first**

Two-word statements are usually easier to analyze than four- or five-word statements.

---

> [!tip]
> **Shortcut 2 — Look for maximum overlap**

If two statements share two or three words, compare them first.

More overlap means faster identification.

---

> [!tip]
> **Shortcut 3 — Circle repeated words**

On rough paper, mark every repeated original word.

Then locate the corresponding repeated code.

---

> [!tip]
> **Shortcut 4 — Build the dictionary immediately**

Write:

$$
RED=KA
$$

$$
BLUE=ZU
$$

instead of repeatedly rereading the statements.

---

> [!tip]
> **Shortcut 5 — Use elimination**

Once most mappings are known, remaining pairs can often be determined without further comparison.

---

> [!tip]
> **Shortcut 6 — Decode only what is asked**

If the question asks for BLUE, do not decode every word unless necessary.

---

> [!tip]
> **Shortcut 7 — Preserve order**

If:

$$
RED\ BLUE\rightarrow KA\ ZU
$$

then:

$$
BLUE\ RED\rightarrow ZU\ KA
$$

---

> [!tip]
> **Shortcut 8 — Check repeated words before using position**

Repeated-word evidence is generally stronger than guessing by position.

---

> [!tip]
> **Shortcut 9 — Use reverse lookup for decoding**

Create both:

$$
RED\rightarrow KA
$$

and:

$$
KA\rightarrow RED
$$

This makes encoding and decoding equally fast.

---

> [!tip]
> **Shortcut 10 — Stop once the required mapping is known**

Do not waste time finding unrelated mappings.

---

# 34. Common Exam Patterns

> [!important] Must Master

### Basic

1. Two-word coded sentences
2. Three-word coded sentences
3. Four-word coded sentences
4. Direct code identification
5. Direct word identification

### Comparison

6. Common-word method
7. Common-code method
8. One-word difference
9. Two-word overlap
10. Multiple-word overlap

### Elimination

11. Missing word-code pair
12. Remaining code
13. Remaining word
14. Partial mapping
15. Full mapping table

### Encoding

16. Encode a word
17. Encode a phrase
18. Encode a rearranged phrase

### Decoding

19. Decode a code
20. Decode multiple codes
21. Decode a sentence
22. Reverse code order

### Advanced

23. Repeated words
24. Repeated codes
25. Multiple unknowns
26. Incomplete information
27. Cannot-be-determined cases
28. Long coded sentences
29. Mixed repeated patterns
30. Multi-step decoding

---

# 35. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking the artificial code has meaning

If:

$$
RED=KA
$$

do not ask what "KA" means.

It is simply the assigned code.

---

### Mistake 2 — Assuming position without evidence

If:

$$
A+B\rightarrow X+Y
$$

do not automatically assume:

$$
A=X,\ B=Y
$$

unless the format guarantees positional correspondence.

Use repeated comparisons whenever possible.

---

### Mistake 3 — Ignoring repeated words

Repeated words are the strongest clues.

---

### Mistake 4 — Ignoring repeated codes

The same method works in reverse.

---

### Mistake 5 — Mixing encoding and decoding

If:

$$
DOG=KA
$$

then:

Encoding:

$$
DOG\rightarrow KA
$$

Decoding:

$$
KA\rightarrow DOG
$$

---

### Mistake 6 — Changing the mapping midway

If:

$$
RED=KA
$$

then RED should remain KA throughout the question.

---

### Mistake 7 — Repeatedly applying a mapping

If:

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

the direct code of A is B, not C.

---

### Mistake 8 — Ignoring word order

Mappings remain fixed, but the order of codes follows the order of the input phrase.

---

### Mistake 9 — Inventing missing information

If a mapping cannot be established:

$$
\boxed{\text{Cannot be determined}}
$$

may be correct.

---

### Mistake 10 — Solving everything

Only derive mappings required for the question.

---

# 36. Advanced Example — Maximum Overlap

Given:

$$
\text{red blue green} \rightarrow \text{ka zu mo}
$$

$$
\text{red blue yellow} \rightarrow \text{ka zu pa}
$$

Compare.

Common words:

$$
RED,\ BLUE
$$

Common codes:

$$
KA,\ ZU
$$

Therefore:

$$
RED=KA
$$

$$
BLUE=ZU
$$

Remaining:

$$
GREEN=MO
$$

$$
YELLOW=PA
$$

### Answer

$$
\boxed{GREEN=MO,\ YELLOW=PA}
$$

---

# 37. Advanced Example — Two New Words

Given:

$$
\text{red blue green} \rightarrow \text{ka zu mo}
$$

$$
\text{red blue yellow} \rightarrow \text{ka zu pa}
$$

$$
\text{yellow black green} \rightarrow \text{pa ti mo}
$$

Find the code for BLACK.

From the first two:

$$
YELLOW=PA
$$

$$
GREEN=MO
$$

Third statement:

$$
YELLOW\ BLACK\ GREEN
$$

corresponds to:

$$
PA\ TI\ MO
$$

Therefore:

$$
\boxed{BLACK=TI}
$$

---

# 38. Advanced Example — Full Mapping

Given:

$$
\text{red blue green} \rightarrow \text{ka zu mo}
$$

$$
\text{red blue yellow} \rightarrow \text{ka zu pa}
$$

$$
\text{yellow black green} \rightarrow \text{pa ti mo}
$$

Build the table.

| Word | Code |
|---|---|
| Red | KA |
| Blue | ZU |
| Green | MO |
| Yellow | PA |
| Black | TI |

Now:

$$
BLACK\ BLUE\ RED
$$

becomes:

$$
TI\ ZU\ KA
$$

### Answer

$$
\boxed{TI\ ZU\ KA}
$$

---

# 39. Advanced Example — Decode Reordered Phrase

Using:

| Word | Code |
|---|---|
| Red | KA |
| Blue | ZU |
| Green | MO |
| Yellow | PA |
| Black | TI |

Decode:

$$
MO\ TI\ PA\ KA
$$

Therefore:

$$
MO=GREEN
$$

$$
TI=BLACK
$$

$$
PA=YELLOW
$$

$$
KA=RED
$$

### Answer

$$
\boxed{GREEN\ BLACK\ YELLOW\ RED}
$$

---

# 40. Advanced Example — Repeated Words and Codes

Given:

$$
\text{red blue red} \rightarrow \text{ka zu ka}
$$

$$
\text{blue green blue} \rightarrow \text{zu mo zu}
$$

Immediately:

$$
RED=KA
$$

$$
BLUE=ZU
$$

$$
GREEN=MO
$$

### Answer

$$
\boxed{RED=KA,\ BLUE=ZU,\ GREEN=MO}
$$

---

# 41. Advanced Example — Longer Phrase

Given:

$$
\text{red big blue car} \rightarrow \text{ka po zu mo}
$$

$$
\text{green big blue bike} \rightarrow \text{ti po zu lu}
$$

Common words:

$$
BIG,\ BLUE
$$

Common codes:

$$
PO,\ ZU
$$

Therefore:

$$
BIG=PO
$$

$$
BLUE=ZU
$$

Remaining:

$$
RED=KA
$$

$$
CAR=MO
$$

$$
GREEN=TI
$$

$$
BIKE=LU
$$

### Answer

$$
\boxed{GREEN\ CAR\rightarrow TI\ MO}
$$

---

# 42. Advanced Example — Cannot Be Determined

Given:

$$
\text{red blue} \rightarrow \text{ka zu}
$$

Question:

> What is the code for GREEN?

No statement contains GREEN.

Therefore:

$$
\boxed{\text{Cannot be determined}}
$$

---

# 43. Advanced Example — Insufficient Link

Given:

$$
\text{red blue} \rightarrow \text{ka zu}
$$

$$
\text{green yellow} \rightarrow \text{mo pa}
$$

Can we determine whether:

$$
GREEN=MO
$$

from these statements alone?

Not necessarily, unless the question guarantees positional correspondence.

The safer conclusion is:

$$
\boxed{\text{The individual mapping is not independently established}}
$$

This is why overlapping statements are important.

---

# 44. Advanced Example — Positional Correspondence

If the question explicitly states that each word corresponds to the code in the same position:

$$
RED\ BLUE\ GREEN
$$

$$
KA\ ZU\ MO
$$

then:

$$
RED=KA
$$

$$
BLUE=ZU
$$

$$
GREEN=MO
$$

### Answer

$$
\boxed{GREEN=MO}
$$

> [!important]
> Always follow the exact instructions of the question. Some formats guarantee position-based correspondence.

---

# 45. Advanced Example — Mixed Query

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{blue flower} \rightarrow \text{zu ti}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

$$
\text{green car} \rightarrow \text{pa mo}
$$

### Question

What does:

$$
PA\ TI
$$

represent?

We know:

$$
PA=GREEN
$$

$$
TI=FLOWER
$$

Therefore:

$$
\boxed{GREEN\ FLOWER}
$$

---

# 46. Advanced Example — Encoding and Decoding Together

Given:

$$
\text{red flower} \rightarrow \text{ka ti}
$$

$$
\text{blue car} \rightarrow \text{zu mo}
$$

Find:

1. Code for RED
2. Code for CAR
3. Meaning of ZU
4. Code for BLUE FLOWER

### Solution

From first:

$$
RED=KA
$$

$$
FLOWER=TI
$$

From second:

$$
BLUE=ZU
$$

$$
CAR=MO
$$

Therefore:

1. RED:

$$
\boxed{KA}
$$

2. CAR:

$$
\boxed{MO}
$$

3. ZU:

$$
\boxed{BLUE}
$$

4. BLUE FLOWER:

$$
\boxed{ZU\ TI}
$$

---

# 47. Master Solving Algorithm

## Step 1 — Read all statements

Do not solve immediately.

---

## Step 2 — Find repeated words

Mark words that appear in multiple statements.

---

## Step 3 — Find repeated codes

Mark codes that appear repeatedly.

---

## Step 4 — Match common elements

$$
\boxed{\text{Common Word}\leftrightarrow\text{Common Code}}
$$

---

## Step 5 — Record the mapping

Example:

$$
RED=KA
$$

---

## Step 6 — Use elimination

Remove known pairs from longer statements.

---

## Step 7 — Build a table

| Word | Code |
|---|---|
| Red | KA |
| Blue | ZU |
| Green | MO |

---

## Step 8 — Answer only the required part

Do not waste time solving irrelevant mappings.

---

# 48. Exam-Speed Strategy

## 5 Seconds

Look for:

$$
\boxed{\text{Repeated words}}
$$

and:

$$
\boxed{\text{Repeated codes}}
$$

---

## 10 Seconds

Find the easiest overlap.

Example:

$$
A+B\rightarrow X+Y
$$

$$
A+C\rightarrow X+Z
$$

Immediately:

$$
A=X
$$

---

## 20 Seconds

Build a mapping table.

---

## 30 Seconds

Use elimination for remaining mappings.

---

## Final Check

Ask:

1. Is the mapping consistent?
2. Did I preserve word order?
3. Am I encoding or decoding?
4. Did I invent any unsupported mapping?
5. Did I answer exactly what was asked?

---

# 49. Master Recognition Table

| Question Feature | Think |
|---|---|
| Same word in two statements | Same code |
| Same code in two statements | Same word |
| Two statements share one word | Common-word method |
| Two statements share two words | Maximum-overlap method |
| Three words, one changed | Identify remaining pair |
| Known mappings + one unknown | Elimination |
| Code given, word required | Reverse mapping |
| Word given, code required | Forward mapping |
| Words reordered | Preserve mapping, change order |
| Word never appears | Cannot determine |
| Code never appears | Cannot decode |
| Explicit positional rule | Use positions |
| Repeated word appears twice | Same code should repeat |

---

# 50. Common Traps in Placement Exams

> [!warning]
> **Trap 1 — Similar-looking codes**

Do not confuse:

$$
KA
$$

with:

$$
AK
$$

Order matters.

---

> [!warning]
> **Trap 2 — Same letters, different order**

These are different codes:

$$
KA\ TI
$$

and:

$$
TI\ KA
$$

---

> [!warning]
> **Trap 3 — Common word but wrong common code**

Always compare the entire statement carefully.

---

> [!warning]
> **Trap 4 — Assuming direct position matching**

Only use positional matching when supported by the question format.

---

> [!warning]
> **Trap 5 — Applying mappings repeatedly**

Do not convert:

$$
A\rightarrow B
$$

and then automatically:

$$
B\rightarrow C
$$

unless repeated substitution is explicitly required.

---

> [!warning]
> **Trap 6 — Solving the meaning of artificial words**

Codes such as:

$$
KA,\ MO,\ ZU
$$

are arbitrary.

---

> [!warning]
> **Trap 7 — Forgetting direction**

Encoding:

$$
WORD\rightarrow CODE
$$

Decoding:

$$
CODE\rightarrow WORD
$$

---

# 51. Mini Practice Set

## Question 1

Given:

$$
\text{red flower}\rightarrow\text{ka ti}
$$

$$
\text{red car}\rightarrow\text{ka mo}
$$

Find the code for RED.

### Answer

$$
\boxed{KA}
$$

---

## Question 2

Find the code for CAR.

### Answer

$$
\boxed{MO}
$$

---

## Question 3

Given:

$$
\text{red car}\rightarrow\text{ka mo}
$$

$$
\text{blue car}\rightarrow\text{zu mo}
$$

Find the code for BLUE.

### Answer

$$
\boxed{ZU}
$$

---

## Question 4

Given:

$$
\text{red blue}\rightarrow\text{ka zu}
$$

Find the code for BLUE RED.

### Answer

$$
\boxed{ZU\ KA}
$$

---

## Question 5

Given:

$$
\text{red blue green}\rightarrow\text{ka zu mo}
$$

$$
\text{red blue yellow}\rightarrow\text{ka zu pa}
$$

Find the code for YELLOW.

### Answer

$$
\boxed{PA}
$$

---

## Question 6

Using the same information, decode:

$$
PA\ MO
$$

### Answer

$$
\boxed{YELLOW\ GREEN}
$$

---

## Question 7

Given:

$$
\text{cat dog}\rightarrow\text{ma po}
$$

$$
\text{dog bird}\rightarrow\text{po ti}
$$

Find the code for DOG.

### Answer

$$
\boxed{PO}
$$

---

## Question 8

Decode:

$$
TI\ MA
$$

### Answer

$$
\boxed{BIRD\ CAT}
$$

---

# 52. Formula Sheet

## Fundamental Mapping

$$
\boxed{\text{Word}\leftrightarrow\text{Code}}
$$

## Common Word

$$
\boxed{\text{Common Word}=\text{Common Code}}
$$

## Common Code

$$
\boxed{\text{Common Code}=\text{Common Word}}
$$

## Forward Encoding

$$
\boxed{\text{Word}\rightarrow\text{Code}}
$$

## Reverse Decoding

$$
\boxed{\text{Code}\rightarrow\text{Word}}
$$

## Elimination

$$
\boxed{
\text{Known Pairs}
\rightarrow
\text{Remaining Pair}
}
$$

## Sentence Encoding

$$
\boxed{
A+B+C
\rightarrow
X+Y+Z
}
$$

## Sentence Decoding

$$
\boxed{
X+Y+Z
\rightarrow
A+B+C
}
$$

---

# 53. Quick Revision

> [!summary] One-Minute Revision

## Chinese Coding

Think:

$$
\boxed{\text{Coded Language}}
$$

The codes are artificial.

The most important method is:

$$
\boxed{
\text{Compare Statements}
\rightarrow
\text{Find Common Word}
\rightarrow
\text{Find Common Code}
}
$$

### Example

$$
RED\ FLOWER\rightarrow KA\ TI
$$

$$
RED\ CAR\rightarrow KA\ MO
$$

Therefore:

$$
RED=KA
$$

$$
FLOWER=TI
$$

$$
CAR=MO
$$

### For More Statements

Use:

$$
\boxed{\text{Maximum Overlap}}
$$

then:

$$
\boxed{\text{Elimination}}
$$

### Encoding

$$
BLUE\ FLOWER
$$

if:

$$
BLUE=ZU
$$

$$
FLOWER=TI
$$

then:

$$
\boxed{ZU\ TI}
$$

### Decoding

If:

$$
ZU=BLUE
$$

$$
TI=FLOWER
$$

then:

$$
ZU\ TI
\rightarrow
\boxed{BLUE\ FLOWER}
$$

### Golden Memory Trick

**"In Chinese Coding, repeated words reveal repeated codes; repeated codes reveal repeated words."**

# One-Line Recognition

**When several phrases are written in an unfamiliar coded language, compare overlapping phrases first and map common words to common codes before using elimination.**