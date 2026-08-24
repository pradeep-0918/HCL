---
type: concept
subject: reasoning
topic: "Substitution Coding"
parent: "04. Coding Decoding"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - reasoning
  - coding-decoding
  - substitution-coding
  - coded-language
  - logical-reasoning
  - pattern-recognition
  - hcl
wikilinks:
  - "[[04. Coding Decoding]]"
  - "[[Letter Coding]]"
  - "[[Number Coding]]"
  - "[[Word Coding]]"
  - "[[Pattern Coding]]"
  - "[[Chinese Coding]]"
  - "[[Mixed Coding Decoding]]"
---

# Substitution Coding

## 1. Core Concept

> [!summary]
> **Substitution Coding** is a reasoning method in which one word, letter, number, object, action, or symbol is deliberately represented by another word, letter, number, or symbol.

The key idea is:

$$
\boxed{\text{Original Item} \rightarrow \text{Assigned Code}}
$$

The code does **not necessarily represent the natural meaning** of the item.

For example, suppose:

$$
DOG \rightarrow CAT
$$

This does **not** mean a dog is a cat.

It means the question has assigned:

$$
\boxed{DOG=CAT}
$$

If the question asks for the code of DOG, the answer is:

$$
\boxed{CAT}
$$

### Core Intuition

Substitution Coding is mainly about **mapping**.

Think:

$$
\boxed{\text{What does this item stand for in the question?}}
$$

not:

$$
\boxed{\text{What does this item normally mean?}}
$$

---

# 2. Basic Meaning

In Substitution Coding, a question establishes an artificial relationship.

Example:

$$
PEN \rightarrow BOOK
$$

$$
BOOK \rightarrow TABLE
$$

$$
TABLE \rightarrow CHAIR
$$

These are artificial substitutions.

If asked:

> What is the substituted word for PEN?

Answer:

$$
\boxed{BOOK}
$$

If asked:

> What is the substituted word for BOOK?

Answer:

$$
\boxed{TABLE}
$$

The important point is that the **coded meaning is defined by the question**.

---

# 3. Main Formula

Substitution Coding does not have one universal mathematical formula.

The basic representation is:

$$
\boxed{X\rightarrow f(X)}
$$

where:

- $X$ = original item
- $f(X)$ = substituted code

For direct substitution:

$$
\boxed{X=Y}
$$

For multiple mappings:

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

$$
C\rightarrow D
$$

The solver must carefully distinguish between:

1. **Direct substitution**
2. **Reverse decoding**
3. **Chain substitution**
4. **Symbol substitution**
5. **Letter substitution**
6. **Number substitution**
7. **Word substitution**

---

# 4. Important Properties

1. Substitution creates an artificial mapping.
2. The code may be unrelated to the natural meaning.
3. One item can be replaced by another item.
4. Symbols can represent letters or words.
5. Numbers can represent words.
6. Words can represent numbers.
7. The mapping must be learned from the question.
8. The same substitution should remain consistent unless the question states otherwise.
9. Encoding and decoding are different directions.
10. Some questions use chains of substitutions.
11. Some questions use complete sentences.
12. Some questions substitute only selected words.
13. Some questions use symbols such as $@,\#,\$,\%$.
14. Context is important.
15. The most common trap is confusing the **assigned code** with the **actual meaning**.

---

# 5. Substitution Coding vs Other Coding Types

| Type | Main Idea | Example |
|---|---|---|
| Letter Coding | Transform letters | $CAT\rightarrow DBU$ |
| Number Coding | Convert into numbers | $CAT\rightarrow24$ |
| Word Coding | Word-level relationship | $DOG\rightarrow ANIMAL$ |
| Substitution Coding | Artificial replacement | $DOG\rightarrowCAT$ |
| Pattern Coding | Mathematical/structural pattern | $ABC\rightarrow BDF$ |
| Chinese Coding | Decode unknown word codes | `go na` = red flower |

> [!important]
> **Substitution Coding is about assigned replacement.**
>
> If the question says:
>
> $$DOG\rightarrowCAT$$
>
> treat it as a mapping, even though the words have no natural relationship.

---

# 6. Types of Substitution Coding

## Type 1 — Word Substitution

$$
DOG\rightarrowCAT
$$

A complete word is replaced by another word.

---

## Type 2 — Letter Substitution

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

Each letter has a replacement.

---

## Type 3 — Number Substitution

$$
1\rightarrow5
$$

$$
2\rightarrow7
$$

Numbers are replaced according to a given mapping.

---

## Type 4 — Symbol Substitution

$$
@\rightarrow A
$$

$$
\#\rightarrow B
$$

---

## Type 5 — Sentence Substitution

Example:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

Words are represented using artificial codes.

---

## Type 6 — Chain Substitution

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

$$
C\rightarrow D
$$

This requires careful direction tracking.

---

# 7. Basic Examples

## Example 1 — Direct Word Substitution

### Question

If:

$$
PEN\rightarrowBOOK
$$

what is the substituted code for PEN?

### Solution

The question directly states:

$$
PEN\rightarrowBOOK
$$

Therefore:

$$
\boxed{BOOK}
$$

---

# 8. Example 2 — Multiple Word Substitution

Suppose:

$$
PEN\rightarrowBOOK
$$

$$
BOOK\rightarrowTABLE
$$

$$
TABLE\rightarrowCHAIR
$$

Find the code for:

$$
BOOK
$$

The mapping says:

$$
BOOK\rightarrowTABLE
$$

### Answer

$$
\boxed{TABLE}
$$

> [!warning]
> Do not substitute BOOK twice unless the question explicitly asks for repeated application.

---

# 9. Example 3 — Decode a Given Code

Suppose:

$$
PEN\rightarrowBOOK
$$

What original word is represented by:

$$
BOOK
$$

Reverse the mapping:

$$
BOOK\leftarrow PEN
$$

Therefore:

$$
\boxed{PEN}
$$

---

# 10. Example 4 — Letter Substitution

Suppose:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

Encode:

$$
ABC
$$

Apply each mapping:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

Therefore:

$$
\boxed{DEF}
$$

---

# 11. Example 5 — Decode Letter Substitution

Suppose:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

Decode:

$$
FED
$$

Reverse the mapping:

$$
F\rightarrow C
$$

$$
E\rightarrow B
$$

$$
D\rightarrow A
$$

Therefore:

$$
\boxed{CBA}
$$

---

# 12. Example 6 — Symbol Substitution

Suppose:

$$
@\rightarrow A
$$

$$
\#\rightarrow B
$$

$$
\$\rightarrow C
$$

Encode:

$$
ABC
$$

Therefore:

$$
A\rightarrow@
$$

$$
B\rightarrow\#
$$

$$
C\rightarrow\$
$$

### Answer

$$
\boxed{@\#\$}
$$

---

# 13. Example 7 — Number Substitution

Suppose:

$$
1\rightarrow5
$$

$$
2\rightarrow8
$$

$$
3\rightarrow9
$$

Encode:

$$
123
$$

Therefore:

$$
1\rightarrow5
$$

$$
2\rightarrow8
$$

$$
3\rightarrow9
$$

### Answer

$$
\boxed{589}
$$

---

# 14. Example 8 — Word-to-Number Substitution

Suppose:

$$
APPLE\rightarrow7
$$

$$
MANGO\rightarrow9
$$

$$
GRAPE\rightarrow4
$$

What is the code for MANGO?

Direct mapping:

$$
MANGO\rightarrow9
$$

### Answer

$$
\boxed{9}
$$

> [!important]
> Do not search for an alphabet formula unless the question requires one. Direct substitution may be all that is needed.

---

# 15. Example 9 — Number-to-Word Substitution

Suppose:

$$
5\rightarrowAPPLE
$$

$$
8\rightarrowMANGO
$$

$$
3\rightarrowGRAPE
$$

What word is represented by $8$?

From the mapping:

$$
8\rightarrow MANGO
$$

### Answer

$$
\boxed{MANGO}
$$

---

# 16. Example 10 — Sentence Substitution

Suppose:

$$
"red\ ball"\rightarrow "ka\ ti"
$$

$$
"red\ car"\rightarrow "ka\ mo"
$$

Identify the code for RED.

The common word is:

$$
RED
$$

The common code is:

$$
KA
$$

Therefore:

$$
\boxed{RED\rightarrow KA}
$$

This is a very important technique.

---

# 17. Example 11 — Common Word Method

Given:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

$$
"red\ car"\rightarrow "ka\ mo"
$$

The common original word is:

$$
RED
$$

The common coded word is:

$$
KA
$$

Therefore:

$$
\boxed{RED=KA}
$$

The remaining words can then be decoded:

$$
FLOWER=TI
$$

$$
CAR=MO
$$

---

# 18. Example 12 — Three-Sentence Substitution

Suppose:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

$$
"red\ car"\rightarrow "ka\ mo"
$$

$$
"blue\ car"\rightarrow "zu\ mo"
$$

Find the code for BLUE.

Compare the second and third statements.

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
BLUE\rightarrow ZU
$$

### Answer

$$
\boxed{ZU}
$$

---

# 19. Example 13 — Decode a Sentence

Given:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

$$
"red\ car"\rightarrow "ka\ mo"
$$

$$
"blue\ car"\rightarrow "zu\ mo"
$$

Decode:

$$
"zu\ ti"
$$

From the mappings:

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

# 20. Example 14 — Find a Single Unknown Word

Given:

$$
"white\ rose"\rightarrow "pa\ ki"
$$

$$
"white\ lotus"\rightarrow "pa\ so"
$$

The common original word is:

$$
WHITE
$$

The common code is:

$$
PA
$$

Therefore:

$$
\boxed{WHITE=PA}
$$

---

# 21. Example 15 — Two Unknowns

Given:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

$$
"blue\ flower"\rightarrow "zu\ ti"
$$

The common word:

$$
FLOWER
$$

Common code:

$$
TI
$$

Therefore:

$$
FLOWER=TI
$$

Then:

$$
RED=KA
$$

$$
BLUE=ZU
$$

---

# 22. Example 16 — Three Common Words

Given:

$$
"red\ big\ car"\rightarrow "ka\ po\ mo"
$$

$$
"red\ small\ car"\rightarrow "ka\ ti\ mo"
$$

Compare the two statements.

Common words:

$$
RED,\ CAR
$$

Common codes:

$$
KA,\ MO
$$

Therefore:

$$
RED=KA
$$

$$
CAR=MO
$$

The remaining pair:

$$
BIG=PO
$$

$$
SMALL=TI
$$

---

# 23. Example 17 — Position Is Important

Suppose:

$$
"red\ blue"\rightarrow "ka\ ti"
$$

and:

$$
"blue\ red"\rightarrow "ti\ ka"
$$

The code follows the same order as the original words.

Therefore:

$$
RED=KA
$$

$$
BLUE=TI
$$

The sentence order is preserved.

---

# 24. Example 18 — Order Does Not Change the Mapping

Given:

$$
"red\ blue"\rightarrow "ka\ ti"
$$

If asked for:

$$
"blue\ red"
$$

the corresponding code is:

$$
\boxed{ti\ ka}
$$

because:

$$
BLUE=TI
$$

and:

$$
RED=KA
$$

---

# 25. Example 19 — Repeated Word

Given:

$$
"red\ red\ blue"\rightarrow "ka\ ka\ ti"
$$

The repeated word RED maps consistently:

$$
RED=KA
$$

and:

$$
BLUE=TI
$$

### Answer

$$
\boxed{RED=KA,\ BLUE=TI}
$$

> [!important]
> Repetition can help confirm the mapping.

---

# 26. Example 20 — Sentence With a Repeated Code

Given:

$$
"cat\ dog"\rightarrow "ma\ po"
$$

$$
"dog\ bird"\rightarrow "po\ ti"
$$

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
DOG=PO
$$

Then:

$$
CAT=MA
$$

$$
BIRD=TI
$$

---

# 27. Example 21 — Decode Using Elimination

Given:

$$
"red\ blue\ green"\rightarrow "ka\ ti\ mo"
$$

$$
"blue\ green"\rightarrow "ti\ mo"
$$

The second statement already identifies:

$$
BLUE=TI
$$

$$
GREEN=MO
$$

Therefore the remaining code in the first statement is:

$$
RED=KA
$$

### Answer

$$
\boxed{RED=KA}
$$

---

# 28. Example 22 — Common Word Comparison

Given:

$$
"apple\ mango"\rightarrow "pa\ ki"
$$

$$
"mango\ grape"\rightarrow "ki\ zo"
$$

Common word:

$$
MANGO
$$

Common code:

$$
KI
$$

Therefore:

$$
MANGO=KI
$$

Then:

$$
APPLE=PA
$$

$$
GRAPE=ZO
$$

---

# 29. Example 23 — Three Statements

Given:

$$
"apple\ mango"\rightarrow "pa\ ki"
$$

$$
"mango\ grape"\rightarrow "ki\ zo"
$$

$$
"grape\ orange"\rightarrow "zo\ lu"
$$

Therefore:

$$
MANGO=KI
$$

$$
GRAPE=ZO
$$

$$
APPLE=PA
$$

$$
ORANGE=LU
$$

### Question

What is:

$$
APPLE\ ORANGE
$$

### Answer

$$
\boxed{PA\ LU}
$$

---

# 30. Example 24 — Unknown Sentence

Given:

$$
"apple\ mango"\rightarrow "pa\ ki"
$$

$$
"mango\ grape"\rightarrow "ki\ zo"
$$

Find the code for:

$$
APPLE\ GRAPE
$$

From the mapping:

$$
APPLE=PA
$$

$$
GRAPE=ZO
$$

Therefore:

$$
\boxed{PA\ ZO}
$$

---

# 31. Example 25 — Reverse Decoding

Given:

$$
"apple\ mango"\rightarrow "pa\ ki"
$$

Find the original sentence represented by:

$$
"ki\ pa"
$$

Mappings:

$$
KI=MANGO
$$

$$
PA=APPLE
$$

Therefore:

$$
\boxed{MANGO\ APPLE}
$$

---

# 32. Example 26 — Chain Substitution

Suppose:

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

$$
C\rightarrow D
$$

If the question asks for the **direct code of B**:

$$
\boxed{C}
$$

If it asks to apply the substitution repeatedly twice:

$$
B\rightarrow C\rightarrow D
$$

then:

$$
\boxed{D}
$$

> [!warning]
> Do not repeatedly apply a substitution unless the question explicitly asks for repeated application.

---

# 33. Example 27 — Chain Decoding

Suppose:

$$
DOG\rightarrow CAT
$$

$$
CAT\rightarrow BIRD
$$

What is the direct code for DOG?

$$
DOG\rightarrow CAT
$$

### Answer

$$
\boxed{CAT}
$$

If the question says:

> Apply the substitution twice.

Then:

$$
DOG\rightarrow CAT\rightarrow BIRD
$$

### Answer

$$
\boxed{BIRD}
$$

---

# 34. Example 28 — Symbol-Based Substitution

Suppose:

$$
A=@
$$

$$
B=\#
$$

$$
C=\$
$$

$$
D=\%
$$

Encode:

$$
ABCD
$$

Therefore:

$$
@\#\$\%
$$

### Answer

$$
\boxed{@\#\$\%}
$$

---

# 35. Example 29 — Decode Symbols

Given:

$$
A=@
$$

$$
B=\#
$$

$$
C=\$
$$

$$
D=\%
$$

Decode:

$$
\$\#@
$$

Therefore:

$$
\$=C
$$

$$
\#=B
$$

$$
@=A
$$

### Answer

$$
\boxed{CBA}
$$

---

# 36. Example 30 — Number Symbol Substitution

Suppose:

$$
1=@
$$

$$
2=\#
$$

$$
3=\$
$$

Encode:

$$
123
$$

### Answer

$$
\boxed{@\#\$}
$$

---

# 37. Example 31 — Mixed Symbol Substitution

Suppose:

$$
A=1
$$

$$
B=@
$$

$$
C=\#
$$

$$
D=4
$$

Encode:

$$
ABCD
$$

Therefore:

$$
1@ \#4
$$

### Answer

$$
\boxed{1@\#4}
$$

---

# 38. Example 32 — Substitution in a Sentence

Suppose:

$$
CAT=RED
$$

$$
DOG=BLUE
$$

$$
BIRD=GREEN
$$

Encode:

> CAT and DOG

Mappings:

$$
CAT\rightarrow RED
$$

$$
DOG\rightarrow BLUE
$$

### Answer

$$
\boxed{RED\ BLUE}
$$

---

# 39. Example 33 — Decoding a Sentence

Suppose:

$$
CAT=RED
$$

$$
DOG=BLUE
$$

$$
BIRD=GREEN
$$

Decode:

> BLUE and GREEN

Therefore:

$$
BLUE\rightarrow DOG
$$

$$
GREEN\rightarrow BIRD
$$

### Answer

$$
\boxed{DOG\ BIRD}
$$

---

# 40. Example 34 — Substitution With Unused Words

Suppose:

$$
CAT=RED
$$

$$
DOG=BLUE
$$

Question:

> What is the code for HORSE?

No mapping is provided.

Therefore:

$$
\boxed{\text{Cannot be determined}}
$$

> [!important]
> Never invent a mapping that the question does not provide.

---

# 41. Example 35 — One-to-One Mapping

Suppose:

$$
A\rightarrow X
$$

$$
B\rightarrow Y
$$

$$
C\rightarrow Z
$$

Then:

$$
ABC\rightarrow XYZ
$$

The mapping is one-to-one:

$$
\boxed{A\leftrightarrow X}
$$

$$
\boxed{B\leftrightarrow Y}
$$

$$
\boxed{C\leftrightarrow Z}
$$

---

# 42. Example 36 — Mapping Table Method

Suppose:

$$
"red\ car"\rightarrow "ka\ mo"
$$

$$
"blue\ car"\rightarrow "ti\ mo"
$$

$$
"red\ bike"\rightarrow "ka\ po"
$$

Build a table:

| Original | Code |
|---|---|
| Red | KA |
| Blue | TI |
| Car | MO |
| Bike | PO |

Now:

$$
BLUE\ BIKE
$$

becomes:

$$
\boxed{TI\ PO}
$$

---

# 43. Example 37 — Complex Sentence Coding

Given:

$$
"red\ big\ car"\rightarrow "ka\ po\ mo"
$$

$$
"blue\ big\ car"\rightarrow "ti\ po\ mo"
$$

$$
"blue\ small\ bike"\rightarrow "ti\ zo\ lu"
$$

Find the code for:

$$
RED\ SMALL\ BIKE
$$

From the statements:

$$
RED=KA
$$

$$
BLUE=TI
$$

$$
BIG=PO
$$

$$
CAR=MO
$$

$$
SMALL=ZO
$$

$$
BIKE=LU
$$

Therefore:

$$
RED\ SMALL\ BIKE
$$

becomes:

$$
\boxed{KA\ ZO\ LU}
$$

---

# 44. Example 38 — Determine Unknown Mapping

Given:

$$
"red\ car"\rightarrow "ka\ mo"
$$

$$
"blue\ car"\rightarrow "ti\ mo"
$$

$$
"blue\ bike"\rightarrow "ti\ po"
$$

Find the code for BIKE.

The common word in the second and third statements is:

$$
BLUE
$$

Common code:

$$
TI
$$

Therefore:

$$
BIKE=PO
$$

### Answer

$$
\boxed{PO}
$$

---

# 45. Example 39 — Find Two Unknowns

Given:

$$
"red\ car"\rightarrow "ka\ mo"
$$

$$
"blue\ car"\rightarrow "ti\ mo"
$$

$$
"blue\ bike"\rightarrow "ti\ po"
$$

Find the code for:

$$
RED\ BIKE
$$

From the mappings:

$$
RED=KA
$$

$$
BIKE=PO
$$

Therefore:

$$
\boxed{KA\ PO}
$$

---

# 46. Example 40 — Decoding With Position

Given:

$$
"red\ blue\ green"\rightarrow "ka\ ti\ mo"
$$

Find the original words represented by:

$$
"mo\ ka\ ti"
$$

Mapping:

$$
MO=GREEN
$$

$$
KA=RED
$$

$$
TI=BLUE
$$

Therefore:

$$
\boxed{GREEN\ RED\ BLUE}
$$

---

# 47. Recognition Patterns

## Pattern 1 — Direct Replacement

> [!important]
> If the question explicitly says:

$$
A\text{ is called }B
$$

think:

$$
\boxed{A\rightarrow B}
$$

---

## Pattern 2 — Code Word Is Unrelated

> [!important]
> If:

$$
DOG\rightarrowTABLE
$$

do not search for a semantic relationship.

Think:

$$
\boxed{\text{Artificial substitution}}
$$

---

## Pattern 3 — Same Word Appears in Multiple Statements

> [!important]
> Find the common word.

Then find the common code.

This is the most important technique in sentence-based substitution.

---

## Pattern 4 — Same Code Appears in Multiple Statements

> [!important]
> Find the common code.

Then identify which original word it represents.

---

## Pattern 5 — Two Words Become Two Codes

> [!important]
> Match the common item.

Example:

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

---

## Pattern 6 — Three Words Become Three Codes

> [!important]
> Use elimination.

If two mappings are already known, the remaining word-code pair can be identified.

---

## Pattern 7 — Code Order Matches Word Order

> [!important]
> Preserve position unless the question explicitly indicates rearrangement.

---

## Pattern 8 — Asked to Decode

> [!important]
> Reverse the mapping.

If:

$$
DOG=KA
$$

then:

$$
KA=DOG
$$

---

## Pattern 9 — Asked to Apply Twice

> [!important]
> Follow the chain:

$$
A\rightarrow B\rightarrow C
$$

Only do this when repeated substitution is requested.

---

## Pattern 10 — Unknown Mapping

> [!important]
> If insufficient information is given, the correct conclusion may be:

$$
\boxed{\text{Cannot be determined}}
$$

---

# 48. Sentence Coding Master Method

Consider:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

$$
"red\ car"\rightarrow "ka\ mo"
$$

$$
"blue\ car"\rightarrow "zu\ mo"
$$

### Step 1 — Compare 1 and 2

Common word:

$$
RED
$$

Common code:

$$
KA
$$

Therefore:

$$
RED=KA
$$

### Step 2 — Compare 2 and 3

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

### Step 3 — Remaining Mapping

From statement 1:

$$
FLOWER=TI
$$

From statement 3:

$$
BLUE=ZU
$$

### Final Mapping

| Word | Code |
|---|---|
| Red | KA |
| Flower | TI |
| Car | MO |
| Blue | ZU |

---

# 49. Shortcuts

> [!tip]
> **Shortcut 1 — Circle repeated words**

When solving sentence coding, immediately mark words that occur in multiple statements.

Repeated words usually reveal their code.

---

> [!tip]
> **Shortcut 2 — Compare only two statements at first**

You usually do not need to analyze all statements simultaneously.

Find one common word and one common code.

---

> [!tip]
> **Shortcut 3 — Build a mapping table**

Write:

| Original | Code |
|---|---|
| Red | KA |
| Blue | ZU |
| Car | MO |

This prevents confusion.

---

> [!tip]
> **Shortcut 4 — Preserve order**

If:

$$
RED\ BLUE\rightarrow KA\ TI
$$

then:

$$
BLUE\ RED\rightarrow TI\ KA
$$

unless the question states another arrangement.

---

> [!tip]
> **Shortcut 5 — Use elimination**

If three out of four word-code pairs are known, the fourth can often be identified immediately.

---

> [!tip]
> **Shortcut 6 — Separate direct code from repeated code**

If:

$$
A\rightarrow B
$$

and:

$$
B\rightarrow C
$$

the direct code of A is still:

$$
B
$$

unless repeated substitution is requested.

---

> [!tip]
> **Shortcut 7 — Look for one-to-one mapping**

If each original word appears with exactly one code, construct a direct dictionary.

---

> [!tip]
> **Shortcut 8 — For symbol coding, write a key**

Example:

$$
@=A
$$

$$
\#=B
$$

$$
\$=C
$$

Then decode systematically.

---

> [!tip]
> **Shortcut 9 — Do not use real-world meaning**

If:

$$
APPLE=TABLE
$$

accept the artificial mapping.

---

> [!tip]
> **Shortcut 10 — Stop when the mapping is sufficient**

Do not derive unnecessary relationships once the asked code is known.

---

# 50. Common Exam Patterns

> [!important] Must Master

### Direct Substitution

1. Word → Word
2. Word → Number
3. Word → Symbol
4. Number → Word
5. Symbol → Word

### Letter Substitution

6. Direct letter replacement
7. Reverse decoding
8. Multiple letter mappings
9. Symbol-letter mappings
10. Number-letter mappings

### Sentence Substitution

11. Two-word statements
12. Three-word statements
13. Common-word method
14. Common-code method
15. Elimination method
16. Multiple sentence decoding
17. Sentence encoding
18. Sentence decoding

### Structural

19. Order preservation
20. Position mapping
21. Repeated word mapping
22. Repeated code mapping

### Chain-Based

23. Direct substitution
24. Repeated substitution
25. Forward chain
26. Reverse chain

### Advanced

27. Mixed word-symbol coding
28. Mixed word-number coding
29. Multiple unknown mappings
30. Incomplete-information problems
31. Cannot-be-determined cases

---

# 51. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Treating substitution as meaning

If:

$$
DOG\rightarrowCAT
$$

do not assume the words are related.

It is simply:

$$
DOG=CAT
$$

under the given code.

---

### Mistake 2 — Repeated substitution without instruction

Given:

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

the direct code for A is:

$$
B
$$

not C.

---

### Mistake 3 — Reversing the mapping incorrectly

If:

$$
DOG\rightarrowKA
$$

then:

$$
KA\rightarrowDOG
$$

not:

$$
DOG\rightarrowKA
$$

when decoding.

---

### Mistake 4 — Ignoring order

If:

$$
RED\ BLUE\rightarrow KA\ TI
$$

then:

$$
BLUE\ RED\rightarrow TI\ KA
$$

---

### Mistake 5 — Matching words by position without verification

The first word does not always correspond to the first code if the question involves rearrangement.

Use repeated-word evidence whenever possible.

---

### Mistake 6 — Ignoring common words

Common words are often the fastest route to the mapping.

---

### Mistake 7 — Ignoring common codes

The same technique works in reverse.

---

### Mistake 8 — Assuming every word has a unique code

Some questions may allow multiple meanings or incomplete information.

---

### Mistake 9 — Inventing missing information

If no mapping exists for a word:

$$
\boxed{\text{Cannot be determined}}
$$

may be the correct answer.

---

### Mistake 10 — Overcomplicating

If the question directly gives:

$$
PEN=BOOK
$$

do not search for alphabet formulas.

---

# 52. Advanced Pattern — One-to-One Mapping

Suppose:

$$
A\rightarrow X
$$

$$
B\rightarrow Y
$$

$$
C\rightarrow Z
$$

This is a one-to-one mapping.

Therefore:

$$
ABC\rightarrow XYZ
$$

And:

$$
ZYX\rightarrow CBA
$$

The reverse mapping is:

$$
X\rightarrow A
$$

$$
Y\rightarrow B
$$

$$
Z\rightarrow C
$$

---

# 53. Advanced Pattern — Many-Step Chain

Suppose:

$$
A\rightarrow B
$$

$$
B\rightarrow C
$$

$$
C\rightarrow D
$$

$$
D\rightarrow E
$$

Repeated application gives:

$$
A\rightarrow B\rightarrow C\rightarrow D\rightarrow E
$$

Therefore:

- 1 application → $B$
- 2 applications → $C$
- 3 applications → $D$
- 4 applications → $E$

### Important

$$
\boxed{\text{Direct substitution}\neq\text{Repeated substitution}}
$$

---

# 54. Advanced Pattern — Sentence Mapping With Elimination

Given:

$$
"red\ blue\ green"\rightarrow "ka\ ti\ mo"
$$

$$
"red\ yellow"\rightarrow "ka\ zo"
$$

$$
"yellow\ green"\rightarrow "zo\ mo"
$$

From first and second:

$$
RED=KA
$$

From second and third:

$$
YELLOW=ZO
$$

From first and third:

$$
GREEN=MO
$$

The remaining code is:

$$
BLUE=TI
$$

### Final Mapping

| Word | Code |
|---|---|
| Red | KA |
| Blue | TI |
| Green | MO |
| Yellow | ZO |

---

# 55. Advanced Pattern — Decode a Mixed Sentence

Using:

| Word | Code |
|---|---|
| Red | KA |
| Blue | TI |
| Green | MO |
| Yellow | ZO |

Decode:

$$
ZO\ KA\ MO
$$

Therefore:

$$
ZO=YELLOW
$$

$$
KA=RED
$$

$$
MO=GREEN
$$

### Answer

$$
\boxed{YELLOW\ RED\ GREEN}
$$

---

# 56. Advanced Pattern — Partial Information

Suppose:

$$
"red\ blue"\rightarrow "ka\ ti"
$$

and:

$$
"green\ blue"\rightarrow "mo\ ti"
$$

We can determine:

$$
BLUE=TI
$$

But if asked for the code of RED:

$$
RED=KA
$$

If asked for the code of YELLOW, there is no information.

Therefore:

$$
\boxed{\text{Cannot be determined}}
$$

---

# 57. Advanced Pattern — Repeated Code

Suppose:

$$
"red\ blue"\rightarrow "ka\ ti"
$$

$$
"green\ blue"\rightarrow "mo\ ti"
$$

The common code is:

$$
TI
$$

Therefore the common word is:

$$
BLUE
$$

Hence:

$$
\boxed{BLUE=TI}
$$

This is the reverse form of the common-word method.

---

# 58. Advanced Pattern — Multiple Occurrences

Suppose:

$$
"red\ blue\ red"\rightarrow "ka\ ti\ ka"
$$

The repeated word:

$$
RED
$$

has the repeated code:

$$
KA
$$

Therefore:

$$
\boxed{RED=KA}
$$

This is a strong confirmation of the mapping.

---

# 59. Advanced Pattern — Order and Mapping

Suppose:

$$
"red\ blue\ green"\rightarrow "ka\ ti\ mo"
$$

Then:

$$
RED=KA
$$

$$
BLUE=TI
$$

$$
GREEN=MO
$$

If asked:

$$
GREEN\ RED\ BLUE
$$

the answer is:

$$
\boxed{MO\ KA\ TI}
$$

The mapping stays fixed while the order changes.

---

# 60. Advanced Pattern — Unknown Code in a Sentence

Given:

$$
"red\ blue\ green"\rightarrow "ka\ ti\ mo"
$$

$$
"red\ yellow\ green"\rightarrow "ka\ zo\ mo"
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

Therefore the remaining pair is:

$$
YELLOW=ZO
$$

### Answer

$$
\boxed{ZO}
$$

---

# 61. Recognition Decision Tree

When you see a Coding-Decoding question, use:

$$
\boxed{\text{Is the code a complete word?}}
$$

If YES:

$$
\downarrow
$$

Check:

$$
\boxed{\text{Direct substitution}}
$$

$$
\boxed{\text{Semantic relationship}}
$$

If NO:

$$
\downarrow
$$

Check:

$$
\boxed{\text{Letter transformation}}
$$

$$
\boxed{\text{Number coding}}
$$

$$
\boxed{\text{Symbol coding}}
$$

For multiple coded sentences:

$$
\boxed{\text{Use common-word/common-code method}}
$$

---

# 62. Exam-Speed Strategy

## 5-Second Scan

Ask:

1. Is it direct substitution?
2. Is it a word-to-word mapping?
3. Is it a symbol?
4. Is it a number?
5. Are there multiple coded sentences?

---

## 10-Second Method

If multiple sentences exist:

$$
\boxed{\text{Find repeated words}}
$$

Then:

$$
\boxed{\text{Find repeated codes}}
$$

Then:

$$
\boxed{\text{Build mapping}}
$$

---

## 20-Second Method

For complex questions:

1. Write every original word.
2. Write every code.
3. Match common words.
4. Match common codes.
5. Fill known mappings.
6. Use elimination.
7. Answer only what is required.

---

# 63. Mapping Table Template

Use this during practice:

| Original | Code | Confirmed? |
|---|---|---|
| Red | KA | Yes |
| Blue | TI | Yes |
| Green | MO | Yes |
| Yellow | ZO | Yes |
| Flower | ? | No |
| Car | ? | No |

This prevents repeated re-analysis.

---

# 64. Mini Practice Set

## Question 1

If:

$$
DOG\rightarrowCAT
$$

what is the code for DOG?

### Answer

$$
\boxed{CAT}
$$

---

## Question 2

If:

$$
CAT\rightarrowRED
$$

what is the original word represented by RED?

### Answer

$$
\boxed{CAT}
$$

---

## Question 3

Given:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

$$
"red\ car"\rightarrow "ka\ mo"
$$

What is the code for RED?

### Answer

$$
\boxed{KA}
$$

---

## Question 4

Given:

$$
"red\ flower"\rightarrow "ka\ ti"
$$

$$
"blue\ flower"\rightarrow "zu\ ti"
$$

What is the code for BLUE?

### Answer

$$
\boxed{ZU}
$$

---

## Question 5

Given:

$$
"red\ car"\rightarrow "ka\ mo"
$$

$$
"blue\ car"\rightarrow "ti\ mo"
$$

What is the code for CAR?

### Answer

$$
\boxed{MO}
$$

---

## Question 6

Given:

$$
"red\ blue"\rightarrow "ka\ ti"
$$

What is the code for:

$$
BLUE\ RED
$$

### Answer

$$
\boxed{TI\ KA}
$$

---

## Question 7

Given:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

Encode:

$$
ABC
$$

### Answer

$$
\boxed{DEF}
$$

---

## Question 8

Given:

$$
A\rightarrow D
$$

$$
B\rightarrow E
$$

$$
C\rightarrow F
$$

Decode:

$$
FED
$$

### Answer

$$
\boxed{CBA}
$$

---

## Question 9

Given:

$$
"apple\ mango"\rightarrow "pa\ ki"
$$

$$
"mango\ grape"\rightarrow "ki\ zo"
$$

What is the code for GRAPE?

### Answer

$$
\boxed{ZO}
$$

---

## Question 10

Given:

$$
"apple\ mango"\rightarrow "pa\ ki"
$$

$$
"mango\ grape"\rightarrow "ki\ zo"
$$

Decode:

$$
ZO\ PA
$$

### Answer

$$
\boxed{GRAPE\ APPLE}
$$

---

# 65. Formula Sheet

## Direct Substitution

$$
\boxed{X\rightarrow f(X)}
$$

## Reverse Decoding

$$
\boxed{f(X)\rightarrow X}
$$

## Letter Mapping

$$
\boxed{A\rightarrow B}
$$

## Symbol Mapping

$$
\boxed{@\rightarrow A}
$$

## Number Mapping

$$
\boxed{1\rightarrow5}
$$

## Repeated Substitution

$$
\boxed{A\rightarrow B\rightarrow C}
$$

## Direct Code

$$
\boxed{f(A)=B}
$$

## Sentence Mapping

$$
\boxed{
\text{Common Word}
\leftrightarrow
\text{Common Code}
}
$$

## Elimination

$$
\boxed{
\text{Known pairs}
\rightarrow
\text{Remaining pair}
}
$$

---

# 66. Quick Revision

> [!summary] One-Minute Revision

## Substitution Coding

Think:

$$
\boxed{\text{Mapping}}
$$

The most important question is:

> **What does this item stand for?**

### Direct Substitution

$$
DOG\rightarrowCAT
$$

means:

$$
\boxed{DOG=CAT}
$$

under the given coding system.

### Decoding

Reverse the mapping:

$$
CAT\rightarrowDOG
$$

### Sentence Coding

If:

$$
RED\ FLOWER\rightarrow KA\ TI
$$

and:

$$
RED\ CAR\rightarrow KA\ MO
$$

then:

$$
RED=KA
$$

and:

$$
FLOWER=TI
$$

$$
CAR=MO
$$

### Most Important Method

For multiple statements:

$$
\boxed{
\text{Find Common Word}
\rightarrow
\text{Find Common Code}
\rightarrow
\text{Create Mapping}
\rightarrow
\text{Use Elimination}
}
$$

### Always Check

$$
\boxed{\text{Direct substitution}}
$$

$$
\boxed{\text{Reverse decoding}}
$$

$$
\boxed{\text{Common-word method}}
$$

$$
\boxed{\text{Common-code method}}
$$

$$
\boxed{\text{Elimination}}
$$

$$
\boxed{\text{Order}}
$$

$$
\boxed{\text{Repeated substitution}}
$$

$$
\boxed{\text{Incomplete information}}
$$

### Golden Memory Trick

**"Substitution Coding is a mapping problem: find what each original item stands for, record the mapping, and use it consistently."**

# One-Line Recognition

**When a question assigns one word, letter, number, or symbol to another, treat it as a mapping and use repeated words, repeated codes, and elimination to decode quickly.**