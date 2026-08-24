---
type: concept
subject: coding
topic: "Positive and Negative"
parent: "Number Basics"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - number-problems
  - number-basics
  - positive-negative
  - java
  - problem-solving
  - comparison
wikilinks:
  - "[[Number Basics]]"
  - "[[Even and Odd]]"
  - "[[Prime Number]]"
  - "[[Conditional Statements]]"
  - "[[Operators]]"
---

# Positive and Negative

## 1. Core Concept

> [!summary]
> A number is **positive** if it is greater than zero, **negative** if it is less than zero, and **zero** is neither positive nor negative.

The basic conditions are:

$$
n>0\Rightarrow Positive
$$

$$
n<0\Rightarrow Negative
$$

$$
n=0\Rightarrow Zero
$$

In programming, use comparison operators:

    if (n > 0) {
        // Positive
    } else if (n < 0) {
        // Negative
    } else {
        // Zero
    }

The key idea is very simple:

**Compare the number with `0`.**

---

# 2. Basic Meaning

## Positive Number

A number greater than zero is positive.

Examples:

$$
1,2,5,10,100
$$

Therefore:

$$
\boxed{n>0}
$$

---

## Negative Number

A number less than zero is negative.

Examples:

$$
-1,-2,-5,-10,-100
$$

Therefore:

$$
\boxed{n<0}
$$

---

## Zero

Zero is:

$$
n=0
$$

Zero is neither positive nor negative.

> [!important]
> **Zero is a special case.**
>
> Do not classify `0` as positive or negative.

---

# 3. Main Formula

| Category | Condition |
|---|---|
| Positive | $n>0$ |
| Negative | $n<0$ |
| Zero | $n=0$ |
| Non-negative | $n\geq0$ |
| Non-positive | $n\leq0$ |

### Java Conditions

Positive:

    n > 0

Negative:

    n < 0

Zero:

    n == 0

Non-negative:

    n >= 0

Non-positive:

    n <= 0

---

# 4. Important Properties

## Property 1 — Positive Number

If:

$$
n>0
$$

then `n` is positive.

Example:

$$
25>0
$$

Therefore:

$$
\boxed{25\text{ is Positive}}
$$

---

## Property 2 — Negative Number

If:

$$
n<0
$$

then `n` is negative.

Example:

$$
-25<0
$$

Therefore:

$$
\boxed{-25\text{ is Negative}}
$$

---

## Property 3 — Zero

If:

$$
n=0
$$

then the number is zero.

Therefore:

$$
\boxed{0\text{ is Zero}}
$$

---

## Property 4 — Absolute Value

The absolute value removes the sign.

For positive numbers:

$$
|5|=5
$$

For negative numbers:

$$
|-5|=5
$$

For zero:

$$
|0|=0
$$

Therefore:

$$
\boxed{|n|\geq0}
$$

for every real number $n$.

---

# 5. Basic Example — Positive Number

## Example 1

### Question

Determine whether `25` is positive, negative, or zero.

### Step 1 — Compare with zero

$$
25>0
$$

Therefore:

$$
\boxed{Positive}
$$

---

# 6. Basic Example — Negative Number

## Example 2

### Question

Determine whether `-15` is positive, negative, or zero.

### Calculation

$$
-15<0
$$

Therefore:

$$
\boxed{Negative}
$$

---

# 7. Basic Example — Zero

## Example 3

### Question

Determine whether `0` is positive, negative, or zero.

### Calculation

$$
0=0
$$

Therefore:

$$
\boxed{Zero}
$$

> [!important]
> Always handle zero separately when the question asks for positive, negative, or zero.

---

# 8. Basic Java Program

## Example 4

### Question

Write a program to determine whether a number is positive, negative, or zero.

### Code

    import java.util.Scanner;

    class Main {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            if (n > 0) {
                System.out.println("Positive");
            } else if (n < 0) {
                System.out.println("Negative");
            } else {
                System.out.println("Zero");
            }
        }
    }

### Logic

    n > 0
    → Positive

    n < 0
    → Negative

    n == 0
    → Zero

---

# 9. Example — Multiple Numbers

## Example 5

### Question

Classify:

    10 -5 0 25 -18

### Analysis

    10  → Positive
    -5  → Negative
    0   → Zero
    25  → Positive
    -18 → Negative

### Answer

$$
\boxed{Positive=2,\ Negative=2,\ Zero=1}
$$

---

# 10. Example — Count Positive Numbers

## Example 6

### Question

Count positive numbers in:

    -5 10 -2 7 0 15

### Code

    int[] arr = {-5, 10, -2, 7, 0, 15};

    int count = 0;

    for (int num : arr) {

        if (num > 0) {
            count++;
        }
    }

    System.out.println(count);

Positive numbers:

    10, 7, 15

Count:

$$
3
$$

### Answer

$$
\boxed{3}
$$

---

# 11. Example — Count Negative Numbers

## Example 7

### Question

Count negative numbers in:

    -5 10 -2 7 0 15

### Code

    int[] arr = {-5, 10, -2, 7, 0, 15};

    int count = 0;

    for (int num : arr) {

        if (num < 0) {
            count++;
        }
    }

    System.out.println(count);

Negative numbers:

    -5, -2

Count:

$$
2
$$

### Answer

$$
\boxed{2}
$$

---

# 12. Example — Count Positive, Negative, and Zero

## Example 8

### Question

For:

    -5 10 -2 7 0 15 0

count positive numbers, negative numbers, and zeros.

### Code

    int[] arr = {-5, 10, -2, 7, 0, 15, 0};

    int positive = 0;
    int negative = 0;
    int zero = 0;

    for (int num : arr) {

        if (num > 0) {
            positive++;
        } else if (num < 0) {
            negative++;
        } else {
            zero++;
        }
    }

    System.out.println("Positive = " + positive);
    System.out.println("Negative = " + negative);
    System.out.println("Zero = " + zero);

### Calculation

Positive:

    10, 7, 15

$$
3
$$

Negative:

    -5, -2

$$
2
$$

Zero:

    0, 0

$$
2
$$

### Answer

$$
\boxed{Positive=3,\ Negative=2,\ Zero=2}
$$

---

# 13. Example — Sum of Positive Numbers

## Example 9

### Question

Find the sum of positive numbers in:

    -4 5 -2 8 10 -3

### Code

    int[] arr = {-4, 5, -2, 8, 10, -3};

    int sum = 0;

    for (int num : arr) {

        if (num > 0) {
            sum += num;
        }
    }

    System.out.println(sum);

Calculation:

$$
5+8+10=23
$$

### Answer

$$
\boxed{23}
$$

---

# 14. Example — Sum of Negative Numbers

## Example 10

### Question

Find the sum of negative numbers in:

    -4 5 -2 8 10 -3

### Code

    int[] arr = {-4, 5, -2, 8, 10, -3};

    int sum = 0;

    for (int num : arr) {

        if (num < 0) {
            sum += num;
        }
    }

    System.out.println(sum);

Calculation:

$$
-4+(-2)+(-3)
$$

$$
=-9
$$

### Answer

$$
\boxed{-9}
$$

> [!warning]
> Do not add absolute values unless the question specifically asks for them.
>
> The sum of negative numbers remains negative.

---

# 15. Example — Sum of Absolute Values

## Example 11

### Question

Find the sum of absolute values of:

    -4 5 -2

### Absolute values

$$
|-4|=4
$$

$$
|5|=5
$$

$$
|-2|=2
$$

Therefore:

$$
4+5+2=11
$$

### Answer

$$
\boxed{11}
$$

### Java

    int[] arr = {-4, 5, -2};

    int sum = 0;

    for (int num : arr) {
        sum += Math.abs(num);
    }

    System.out.println(sum);

---

# 16. Absolute Value

Absolute value represents the distance of a number from zero.

Examples:

$$
|5|=5
$$

$$
|-5|=5
$$

$$
|0|=0
$$

### Mathematical Definition

$$
|x|=
\begin{cases}
x & x\geq0\\
-x & x<0
\end{cases}
$$

### Programming

    Math.abs(x)

Example:

    Math.abs(-25)

Result:

    25

> [!tip]
> If the question says **distance from zero**, **magnitude**, or **absolute difference**, think of absolute value.

---

# 17. Example — Absolute Difference

## Example 12

### Question

Find the difference between `8` and `20` without considering direction.

### Calculation

$$
|8-20|
$$

$$
=|-12|
$$

$$
=12
$$

### Answer

$$
\boxed{12}
$$

Java:

    int difference = Math.abs(8 - 20);

---

# 18. Example — Positive Difference

## Example 13

### Question

Find the positive difference between `15` and `9`.

### Calculation

$$
|15-9|=|6|=6
$$

### Answer

$$
\boxed{6}
$$

> [!important]
> When the question says **positive difference**, the absolute difference is usually required.

---

# 19. Example — Maximum and Minimum

## Example 14

### Question

Find the maximum and minimum values in:

    -8 12 -3 25 4

### Analysis

Maximum:

$$
25
$$

Minimum:

$$
-8
$$

### Answer

$$
\boxed{Maximum=25}
$$

$$
\boxed{Minimum=-8}
$$

### Java

    int[] arr = {-8, 12, -3, 25, 4};

    int max = arr[0];
    int min = arr[0];

    for (int num : arr) {

        if (num > max) {
            max = num;
        }

        if (num < min) {
            min = num;
        }
    }

    System.out.println("Maximum = " + max);
    System.out.println("Minimum = " + min);

---

# 20. Example — Largest Positive Number

## Example 15

### Question

Find the largest positive number in:

    -10 4 -2 15 7 -20

### Code

    int[] arr = {-10, 4, -2, 15, 7, -20};

    int maxPositive = Integer.MIN_VALUE;

    for (int num : arr) {

        if (num > 0 && num > maxPositive) {
            maxPositive = num;
        }
    }

    System.out.println(maxPositive);

Positive numbers:

    4, 15, 7

Largest:

$$
15
$$

### Answer

$$
\boxed{15}
$$

---

# 21. Example — Smallest Negative Number

## Example 16

### Question

Find the smallest negative number in:

    -10 4 -2 15 7 -20

Here, "smallest" means numerically smallest.

Compare:

$$
-10,\ -2,\ -20
$$

The smallest is:

$$
-20
$$

### Answer

$$
\boxed{-20}
$$

### Java

    int[] arr = {-10, 4, -2, 15, 7, -20};

    int minNegative = Integer.MAX_VALUE;

    for (int num : arr) {

        if (num < 0 && num < minNegative) {
            minNegative = num;
        }
    }

    System.out.println(minNegative);

---

# 22. Important Trap — Largest Negative Number

There is a difference between:

**Smallest negative number**

and:

**Largest negative number**

Consider:

    -20 -8 -3 -15

Smallest:

$$
-20
$$

Largest:

$$
-3
$$

Why?

Because on the number line:

$$
-20<-15<-8<-3
$$

Therefore:

$$
\boxed{-3\text{ is the largest negative number}}
$$

> [!warning]
> Negative numbers are often a source of mistakes.
>
> Remember:
>
> **The number closer to zero is larger.**

---

# 23. Example — Positive and Negative Product

## Example 17

### Question

Determine whether:

$$
(-5)\times(-8)
$$

is positive or negative.

Two negative numbers multiply to a positive number.

$$
(-)\times(-)=(+)
$$

Actual result:

$$
40
$$

### Answer

$$
\boxed{Positive}
$$

---

# 24. Example — Positive and Negative Product

## Example 18

### Question

Determine whether:

$$
(-5)\times8
$$

is positive or negative.

A negative multiplied by a positive gives a negative result.

$$
(-)\times(+) = (-)
$$

### Answer

$$
\boxed{Negative}
$$

---

# 25. Sign Rules for Multiplication

| First Sign | Second Sign | Result |
|---|---|---|
| `+` | `+` | `+` |
| `+` | `-` | `-` |
| `-` | `+` | `-` |
| `-` | `-` | `+` |

### Memory Rule

Same signs:

$$
\boxed{+\times+=+}
$$

$$
\boxed{-\times-=+}
$$

Different signs:

$$
\boxed{+\times-=-}
$$

$$
\boxed{-\times+=-}
$$

---

# 26. Sign Rules for Division

The same sign rule applies to division.

| First Sign | Second Sign | Result |
|---|---|---|
| `+` | `+` | `+` |
| `+` | `-` | `-` |
| `-` | `+` | `-` |
| `-` | `-` | `+` |

Examples:

$$
20/5=4
$$

$$
20/(-5)=-4
$$

$$
(-20)/5=-4
$$

$$
(-20)/(-5)=4
$$

> [!important]
> **Same signs → positive.**
>
> **Different signs → negative.**

---

# 27. Multiple Negative Factors

## Example 19

### Question

Determine the sign of:

$$
(-2)(-3)(-4)
$$

Count negative factors:

$$
3
$$

There are an odd number of negative factors.

Therefore, the result is negative.

### Answer

$$
\boxed{Negative}
$$

---

# 28. Multiple Negative Factors

## Example 20

### Question

Determine the sign of:

$$
(-2)(-3)(-4)(-5)
$$

Number of negative factors:

$$
4
$$

Four is even.

Therefore:

$$
\boxed{Positive}
$$

> [!tip]
> For multiplication:
>
> **Even number of negative factors → Positive**
>
> **Odd number of negative factors → Negative**

---

# 29. Pattern Recognition — Check Sign

> [!important]
> **If the question says "positive, negative, or zero":**
>
> Compare with zero.
>
> $$n>0\rightarrow Positive$$
>
> $$n<0\rightarrow Negative$$
>
> $$n=0\rightarrow Zero$$

---

# 30. Pattern Recognition — Absolute Difference

> [!important]
> **If the question says:**
>
> "Difference without considering sign"
>
> "Positive difference"
>
> "Distance between two numbers"
>
> Think:
>
> $$\boxed{|a-b|}$$

---

# 31. Pattern Recognition — Product Sign

> [!important]
> **If the question asks only whether a product is positive or negative:**
>
> Do not calculate the complete product.
>
> Count the number of negative factors.
>
> Even count:
>
> $$\boxed{Positive}$$
>
> Odd count:
>
> $$\boxed{Negative}$$

---

# 32. Pattern Recognition — Array Classification

> [!important]
> **If the question says:**
>
> "Count positive and negative elements in an array."
>
> Use:
>
>     if (num > 0)
>         positive++;
>     else if (num < 0)
>         negative++;
>     else
>         zero++;

---

# 33. Pattern Recognition — Largest Negative

> [!important]
> **If the question asks for the largest negative number:**
>
> Think:
>
> **The negative number closest to zero.**
>
> Example:
>
> $$-20,-8,-3,-15$$
>
> Largest:
>
> $$\boxed{-3}$$

---

# 34. Pattern Recognition — Smallest Negative

> [!important]
> **If the question asks for the smallest negative number:**
>
> Think:
>
> **The negative number farthest from zero.**
>
> Example:
>
> $$-20,-8,-3,-15$$
>
> Smallest:
>
> $$\boxed{-20}$$

---

# 35. Shortcuts

> [!tip]
> **Shortcut 1 — Sign Check**
>
> Compare directly with zero.
>
> No arithmetic is required.

> [!tip]
> **Shortcut 2 — Large Number**
>
> For positive/negative classification, only the sign matters.
>
> The size of the number does not matter.

> [!tip]
> **Shortcut 3 — Absolute Difference**
>
> If direction does not matter:
>
> $$\boxed{|a-b|}$$

> [!tip]
> **Shortcut 4 — Product Sign**
>
> Count negative factors.
>
> Even number of negatives:
>
> $$\boxed{Positive}$$
>
> Odd number of negatives:
>
> $$\boxed{Negative}$$

> [!tip]
> **Shortcut 5 — Largest Negative**
>
> Choose the negative number closest to zero.

> [!tip]
> **Shortcut 6 — Smallest Negative**
>
> Choose the negative number farthest from zero.

> [!tip]
> **Shortcut 7 — Non-Negative**
>
> If the question says non-negative:
>
> $$\boxed{n\geq0}$$
>
> Zero is included.

> [!tip]
> **Shortcut 8 — Non-Positive**
>
> If the question says non-positive:
>
> $$\boxed{n\leq0}$$
>
> Zero is included.

---

# 36. Non-Negative and Non-Positive

These terms are important in coding questions.

## Non-Negative

Means:

$$
n\geq0
$$

Includes:

    0, 1, 2, 3, ...

Does not include:

    -1, -2, ...

---

## Non-Positive

Means:

$$
n\leq0
$$

Includes:

    0, -1, -2, -3, ...

Does not include:

    1, 2, 3, ...

> [!important]
> "Non-negative" includes zero.
>
> "Non-positive" also includes zero.

---

# 37. Example — Count Non-Negative Numbers

## Example 21

### Question

Count non-negative numbers in:

    -3 0 5 -1 8 0

Non-negative means:

$$
n\geq0
$$

Values:

    0, 5, 8, 0

Count:

$$
4
$$

### Answer

$$
\boxed{4}
$$

---

# 38. Example — Count Non-Positive Numbers

## Example 22

### Question

Count non-positive numbers in:

    -3 0 5 -1 8 0

Non-positive means:

$$
n\leq0
$$

Values:

    -3, 0, -1, 0

Count:

$$
4
$$

### Answer

$$
\boxed{4}
$$

---

# 39. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Treating Zero as Positive

Wrong:

$$
0>0
$$

This is false.

Correct:

$$
0=0
$$

Therefore:

$$
\boxed{Zero}
$$

---

### Mistake 2 — Treating Zero as Negative

Wrong:

$$
0<0
$$

This is false.

Correct:

$$
0=0
$$

Therefore:

$$
\boxed{Zero}
$$

---

### Mistake 3 — Confusing Largest and Smallest Negative

For:

    -2 -10 -5

Largest:

$$
-2
$$

Smallest:

$$
-10
$$

> [!warning]
> On the number line, values increase as you move toward the right.
>
> Therefore:
>
> $$-10<-5<-2$$

---

### Mistake 4 — Forgetting Zero in Non-Negative

Non-negative means:

$$
n\geq0
$$

not:

$$
n>0
$$

So zero must be included.

---

### Mistake 5 — Forgetting Zero in Non-Positive

Non-positive means:

$$
n\leq0
$$

not:

$$
n<0
$$

So zero must be included.

---

### Mistake 6 — Calculating a Huge Product to Determine Its Sign

For:

$$
(-999999)(123456)
$$

You only need the signs:

$$
(-)\times(+)=(-)
$$

Therefore:

$$
\boxed{Negative}
$$

No multiplication is required.

---

### Mistake 7 — Confusing Absolute Value with Sign

For:

$$
|-8|
$$

the answer is:

$$
8
$$

not:

$$
-8
$$

Absolute value removes the negative sign.

---

# 40. Number Line Intuition

Think of the number line:

    Negative ←——— Zero ———→ Positive

Example:

    -5  -4  -3  -2  -1   0   1   2   3   4   5

Numbers to the left of zero:

$$
\boxed{Negative}
$$

Number exactly at zero:

$$
\boxed{Zero}
$$

Numbers to the right of zero:

$$
\boxed{Positive}
$$

> [!tip]
> A simple visual memory:
>
> **Left of 0 → Negative**
>
> **At 0 → Zero**
>
> **Right of 0 → Positive**

---

# 41. Advanced Example — Sum Sign

## Example 23

### Question

Determine whether:

$$
-50+30+10
$$

is positive, negative, or zero.

Calculate:

$$
-50+30=-20
$$

Then:

$$
-20+10=-10
$$

Therefore:

$$
\boxed{Negative}
$$

---

# 42. Advanced Example — Sign Without Full Calculation

## Example 24

### Question

Determine the sign of:

$$
(-5)(-7)(3)(-2)
$$

Count negative factors:

    -5 → Negative
    -7 → Negative
    3  → Positive
    -2 → Negative

Total negative factors:

$$
3
$$

Three is odd.

Therefore:

$$
\boxed{Negative}
$$

No multiplication is required.

---

# 43. Advanced Example — Absolute Difference in Array

## Example 25

### Question

Find the minimum absolute difference between adjacent elements:

    10 6 15 8

Calculate adjacent differences:

$$
|10-6|=4
$$

$$
|6-15|=9
$$

$$
|15-8|=7
$$

Minimum:

$$
4
$$

### Answer

$$
\boxed{4}
$$

### Recognition

If the question says:

    minimum difference
    absolute difference
    distance between values

Think:

$$
\boxed{|a-b|}
$$

---

# 44. Advanced Example — Separate Positive and Negative

## Example 26

### Question

Move positive and negative values into separate arrays.

Input:

    -2 5 -7 8 3 -1

### Code

    int[] arr = {-2, 5, -7, 8, 3, -1};

    for (int num : arr) {

        if (num > 0) {
            System.out.print("Positive: " + num + " ");
        } else if (num < 0) {
            System.out.print("Negative: " + num + " ");
        }
    }

### Classification

Positive:

    5, 8, 3

Negative:

    -2, -7, -1

---

# 45. Advanced Example — Largest Positive and Largest Negative

## Example 27

### Question

Find the largest positive and largest negative values in:

    -20 5 -8 12 -3 7

Positive values:

    5, 12, 7

Largest positive:

$$
12
$$

Negative values:

    -20, -8, -3

Largest negative:

$$
-3
$$

### Answer

$$
\boxed{Largest\ Positive=12}
$$

$$
\boxed{Largest\ Negative=-3}
$$

---

# 46. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Check Sign

    if (n > 0) {
        // Positive
    } else if (n < 0) {
        // Negative
    } else {
        // Zero
    }

### Pattern 2 — Count Positive

    if (num > 0) {
        positive++;
    }

### Pattern 3 — Count Negative

    if (num < 0) {
        negative++;
    }

### Pattern 4 — Count Zero

    if (num == 0) {
        zero++;
    }

### Pattern 5 — Absolute Difference

    int diff = Math.abs(a - b);

### Pattern 6 — Sign of Product

    Even number of negative factors
    → Positive

    Odd number of negative factors
    → Negative

### Pattern 7 — Largest Negative

Choose the negative value closest to zero.

### Pattern 8 — Smallest Negative

Choose the negative value farthest from zero.

### Pattern 9 — Non-Negative

$$
n\geq0
$$

### Pattern 10 — Non-Positive

$$
n\leq0
$$

---

# 47. Formula Sheet

## Sign Classification

$$
\boxed{n>0\Rightarrow Positive}
$$

$$
\boxed{n<0\Rightarrow Negative}
$$

$$
\boxed{n=0\Rightarrow Zero}
$$

## Non-Negative

$$
\boxed{n\geq0}
$$

## Non-Positive

$$
\boxed{n\leq0}
$$

## Absolute Value

$$
\boxed{|x|\geq0}
$$

## Absolute Difference

$$
\boxed{|a-b|}
$$

## Product Sign

Even number of negative factors:

$$
\boxed{Positive}
$$

Odd number of negative factors:

$$
\boxed{Negative}
$$

## Sign Multiplication

$$
(+)(+)=+
$$

$$
(+)(-) = -
$$

$$
(-)(+) = -
$$

$$
(-)(-) = +
$$

## Number Line

$$
Negative<0<Positive
$$

---

# 48. Quick Revision

> [!summary] One-Minute Revision

    Positive
    → n > 0.

    Negative
    → n < 0.

    Zero
    → n == 0.

    Zero
    → Neither positive nor negative.

    Non-negative
    → n >= 0.
    → Includes zero.

    Non-positive
    → n <= 0.
    → Includes zero.

    Number line
    → Left of zero = Negative.
    → Zero = Zero.
    → Right of zero = Positive.

    Absolute value
    → Removes the sign.
    → |-5| = 5.

    Absolute difference
    → |a - b|.

    Largest negative
    → Closest to zero.

    Smallest negative
    → Farthest from zero.

    Positive × Positive
    → Positive.

    Positive × Negative
    → Negative.

    Negative × Positive
    → Negative.

    Negative × Negative
    → Positive.

    Product with even negative factors
    → Positive.

    Product with odd negative factors
    → Negative.

    Check a number's sign
    → Compare it with zero.

    Count positive array elements
    → num > 0.

    Count negative array elements
    → num < 0.

    Count zeros
    → num == 0.

    Positive difference
    → Math.abs(a - b).

    Huge product sign
    → Do not calculate.
    → Count negative factors.

---

## Golden Memory Trick

**Positive is greater than zero, negative is less than zero, and zero is the boundary between them.**

## One-Line Recognition

**Whenever a problem asks for positive, negative, zero, sign, magnitude, or absolute difference, compare with zero or use `Math.abs()` as appropriate.**