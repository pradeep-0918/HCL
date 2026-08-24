---
type: concept
subject: coding
topic: "Even and Odd"
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
  - even-odd
  - java
  - programming-fundamentals
  - problem-solving
wikilinks:
  - "[[Number Basics]]"
  - "[[Positive and Negative]]"
  - "[[Prime Number]]"
  - "[[Divisibility]]"
  - "[[Modular Arithmetic]]"
---

# Even and Odd

## 1. Core Concept

> [!summary]
> An integer is **even** if it is exactly divisible by `2`.
>
> An integer is **odd** if it leaves a remainder of `1` when divided by `2`.
>
> The most important programming test is:
>
> $$n\%2==0$$
>
> → Even
>
> Otherwise:
>
> → Odd

The `%` operator gives the remainder after division.

Example:

$$
10\%2=0
$$

Therefore, `10` is even.

Example:

$$
7\%2=1
$$

Therefore, `7` is odd.

### Core Rule

$$
\boxed{n\%2==0\Rightarrow Even}
$$

$$
\boxed{n\%2\neq0\Rightarrow Odd}
$$

---

# 2. Basic Meaning

## Even Number

A number is even when it can be written as:

$$
n=2k
$$

where $k$ is an integer.

Examples:

$$
0,2,4,6,8,10,12,\ldots
$$

Negative even numbers also exist:

$$
-2,-4,-6,-8,\ldots
$$

## Odd Number

A number is odd when it can be written as:

$$
n=2k+1
$$

where $k$ is an integer.

Examples:

$$
1,3,5,7,9,11,\ldots
$$

Negative odd numbers also exist:

$$
-1,-3,-5,-7,\ldots
$$

> [!important]
> **Zero is even** because:
>
> $$0\%2=0$$
>
> and:
>
> $$0=2\times0$$

---

# 3. Main Formula

| Concept | Formula |
|---|---|
| Even | $n\%2=0$ |
| Odd | $n\%2\neq0$ |
| Even representation | $n=2k$ |
| Odd representation | $n=2k+1$ |

### Java Condition

Even:

    if (n % 2 == 0) {
        // Even
    }

Odd:

    if (n % 2 != 0) {
        // Odd
    }

Complete program:

    import java.util.Scanner;

    class Main {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            if (n % 2 == 0) {
                System.out.println("Even");
            } else {
                System.out.println("Odd");
            }
        }
    }

---

# 4. Important Properties

### Property 1 — Even + Even

The result is always even.

Example:

$$
4+8=12
$$

$$
12\%2=0
$$

Therefore:

$$
\boxed{Even+Even=Even}
$$

---

### Property 2 — Odd + Odd

The result is always even.

Example:

$$
5+7=12
$$

Therefore:

$$
\boxed{Odd+Odd=Even}
$$

---

### Property 3 — Even + Odd

The result is always odd.

Example:

$$
4+7=11
$$

Therefore:

$$
\boxed{Even+Odd=Odd}
$$

---

### Property 4 — Even × Any Integer

The result is always even.

Example:

$$
6\times5=30
$$

Therefore:

$$
\boxed{Even\times Any=Even}
$$

---

### Property 5 — Odd × Odd

The result is odd.

Example:

$$
3\times5=15
$$

Therefore:

$$
\boxed{Odd\times Odd=Odd}
$$

---

### Property 6 — Odd × Even

The result is even.

Example:

$$
3\times4=12
$$

Therefore:

$$
\boxed{Odd\times Even=Even}
$$

---

### Property 7 — Even Powers

If a non-zero number is even, every positive power is even.

Example:

$$
2^3=8
$$

$$
4^2=16
$$

---

### Property 8 — Odd Powers

If a number is odd, every positive integer power is odd.

Example:

$$
3^3=27
$$

$$
5^2=25
$$

---

# 5. Basic Example — Check One Number

## Example 1

### Question

Determine whether `24` is even or odd.

### Step 1 — Apply the remainder test

$$
24\%2=0
$$

### Step 2 — Identify the result

Remainder is `0`.

Therefore, the number is even.

### Answer

$$
\boxed{24\text{ is Even}}
$$

---

# 6. Basic Example — Odd Number

## Example 2

### Question

Determine whether `37` is even or odd.

### Calculation

$$
37\%2=1
$$

The remainder is not zero.

Therefore:

$$
\boxed{37\text{ is Odd}}
$$

---

# 7. Basic Example — Zero

## Example 3

### Question

Is `0` even or odd?

### Calculation

$$
0\%2=0
$$

Therefore:

$$
\boxed{0\text{ is Even}}
$$

> [!important]
> Do not classify `0` as odd.
>
> **Zero is even.**

---

# 8. Basic Example — Negative Number

## Example 4

### Question

Determine whether `-8` is even or odd.

### Calculation

$$
-8\%2=0
$$

Therefore:

$$
\boxed{-8\text{ is Even}}
$$

### Another Example

For `-7`:

$$
-7\%2=-1
$$

The remainder is non-zero.

Therefore:

$$
\boxed{-7\text{ is Odd}}
$$

> [!important]
> For programming, the safest test is still:
>
> $$n\%2==0$$
>
> for evenness.
>
> Any non-zero remainder indicates oddness for an integer.

---

# 9. Example — Print Even Numbers from 1 to N

## Example 5

### Question

Print all even numbers from `1` to `10`.

### Recognition

We need to check each number.

Use:

$$
i\%2==0
$$

### Code

    for (int i = 1; i <= 10; i++) {

        if (i % 2 == 0) {
            System.out.print(i + " ");
        }
    }

### Answer

    2 4 6 8 10

---

# 10. Example — Print Odd Numbers from 1 to N

## Example 6

### Question

Print all odd numbers from `1` to `10`.

### Code

    for (int i = 1; i <= 10; i++) {

        if (i % 2 != 0) {
            System.out.print(i + " ");
        }
    }

### Answer

    1 3 5 7 9

---

# 11. Shortcut — Start Directly from 2

Instead of checking every number:

    for (int i = 1; i <= n; i++) {

        if (i % 2 == 0) {
            System.out.print(i + " ");
        }
    }

We can directly generate even numbers:

    for (int i = 2; i <= n; i += 2) {
        System.out.print(i + " ");
    }

For `n = 10`:

    2 4 6 8 10

> [!tip]
> If you only need even numbers, start from `2` and increase by `2`.

---

# 12. Shortcut — Generate Odd Numbers Directly

Instead of checking:

    for (int i = 1; i <= n; i++) {

        if (i % 2 != 0) {
            System.out.print(i + " ");
        }
    }

Use:

    for (int i = 1; i <= n; i += 2) {
        System.out.print(i + " ");
    }

For `n = 10`:

    1 3 5 7 9

> [!tip]
> If you only need odd numbers, start from `1` and increase by `2`.

---

# 13. Example — Count Even Numbers

## Example 7

### Question

Count the even numbers from `1` to `10`.

### Code

    int count = 0;

    for (int i = 1; i <= 10; i++) {

        if (i % 2 == 0) {
            count++;
        }
    }

    System.out.println(count);

Even numbers:

    2 4 6 8 10

Count:

$$
5
$$

### Answer

$$
\boxed{5}
$$

---

# 14. Shortcut — Count Even Numbers from 1 to N

For positive integer $n$:

$$
\boxed{\left\lfloor\frac{n}{2}\right\rfloor}
$$

Example:

$$
n=10
$$

$$
\frac{10}{2}=5
$$

Therefore:

$$
\boxed{5}
$$

For:

$$
n=11
$$

$$
\left\lfloor\frac{11}{2}\right\rfloor=5
$$

Therefore:

$$
\boxed{5}
$$

---

# 15. Shortcut — Count Odd Numbers from 1 to N

For positive integer $n$:

$$
\boxed{\left\lceil\frac{n}{2}\right\rceil}
$$

Equivalent integer formula:

$$
\boxed{\frac{n+1}{2}}
$$

when using integer division for positive integers.

Example:

$$
n=10
$$

$$
\frac{10+1}{2}=5
$$

Therefore:

$$
\boxed{5}
$$

For:

$$
n=11
$$

$$
\frac{11+1}{2}=6
$$

Therefore:

$$
\boxed{6}
$$

---

# 16. Example — Sum of Even Numbers

## Example 8

### Question

Find the sum of even numbers from `1` to `10`.

Even numbers:

    2 4 6 8 10

Calculation:

$$
2+4+6+8+10=30
$$

### Answer

$$
\boxed{30}
$$

### Programming Approach

    int sum = 0;

    for (int i = 2; i <= 10; i += 2) {
        sum += i;
    }

    System.out.println(sum);

---

# 17. Example — Sum of Odd Numbers

## Example 9

### Question

Find the sum of odd numbers from `1` to `9`.

Odd numbers:

    1 3 5 7 9

Calculation:

$$
1+3+5+7+9=25
$$

### Answer

$$
\boxed{25}
$$

### Useful Formula

The sum of the first $n$ odd numbers is:

$$
\boxed{n^2}
$$

For the first `5` odd numbers:

$$
5^2=25
$$

Therefore:

$$
\boxed{25}
$$

---

# 18. Important Formula — Sum of First N Even Numbers

The first $n$ positive even numbers are:

$$
2,4,6,\ldots,2n
$$

Their sum is:

$$
2+4+6+\cdots+2n
$$

Factor out `2`:

$$
2(1+2+3+\cdots+n)
$$

Using:

$$
1+2+\cdots+n=\frac{n(n+1)}{2}
$$

Therefore:

$$
\boxed{n(n+1)}
$$

### Example

Sum of first `5` even numbers:

$$
5(6)=30
$$

### Answer

$$
\boxed{30}
$$

---

# 19. Important Formula — Sum of First N Odd Numbers

The first $n$ positive odd numbers are:

$$
1,3,5,\ldots,2n-1
$$

Their sum is:

$$
\boxed{n^2}
$$

### Example

First `6` odd numbers:

$$
1+3+5+7+9+11
$$

Using the formula:

$$
6^2=36
$$

### Answer

$$
\boxed{36}
$$

---

# 20. Example — Check Parity of Sum

## Example 10

### Question

Without calculating the exact value, determine whether:

$$
28+46
$$

is even or odd.

Both numbers are even.

Therefore:

$$
Even+Even=Even
$$

### Answer

$$
\boxed{Even}
$$

---

# 21. Example — Odd + Odd

## Example 11

### Question

Determine the parity of:

$$
35+47
$$

Both numbers are odd.

Therefore:

$$
Odd+Odd=Even
$$

Actual calculation:

$$
35+47=82
$$

### Answer

$$
\boxed{Even}
$$

---

# 22. Example — Even + Odd

## Example 12

### Question

Determine the parity of:

$$
28+35
$$

One number is even.

The other is odd.

Therefore:

$$
Even+Odd=Odd
$$

Actual result:

$$
28+35=63
$$

### Answer

$$
\boxed{Odd}
$$

---

# 23. Example — Product Parity

## Example 13

### Question

Determine whether:

$$
24\times37
$$

is even or odd.

Since `24` is even:

$$
Even\times Any=Even
$$

Therefore:

$$
\boxed{Even}
$$

No multiplication is required.

> [!tip]
> If at least one factor is even, the entire product is even.

---

# 24. Example — Odd Product

## Example 14

### Question

Determine whether:

$$
15\times21
$$

is even or odd.

Both factors are odd.

Therefore:

$$
Odd\times Odd=Odd
$$

Actual result:

$$
15\times21=315
$$

### Answer

$$
\boxed{Odd}
$$

---

# 25. Example — Power of a Number

## Example 15

### Question

Determine whether:

$$
7^{100}
$$

is even or odd.

Since `7` is odd:

$$
Odd^{positive\ integer}=Odd
$$

Therefore:

$$
\boxed{Odd}
$$

No need to calculate the huge number.

---

# 26. Example — Even Power

## Example 16

### Question

Determine whether:

$$
12^{100}
$$

is even or odd.

Since `12` is even:

$$
Even^{positive\ integer}=Even
$$

Therefore:

$$
\boxed{Even}
$$

---

# 27. Pattern Recognition — Single Number

> [!important]
> **If the question says:**
>
> "Check whether a number is even or odd."
>
> Think immediately:
>
> $$\boxed{n\%2}$$

Decision:

    n % 2 == 0
        ↓
      Even

    otherwise
        ↓
       Odd

---

# 28. Pattern Recognition — Print Even Numbers

> [!important]
> **If the question says:**
>
> "Print all even numbers from 1 to N."
>
> Think:
>
> Start from `2`.
>
> Increase by `2`.

Template:

    for (int i = 2; i <= n; i += 2) {
        System.out.print(i + " ");
    }

---

# 29. Pattern Recognition — Print Odd Numbers

> [!important]
> **If the question says:**
>
> "Print all odd numbers from 1 to N."
>
> Think:
>
> Start from `1`.
>
> Increase by `2`.

Template:

    for (int i = 1; i <= n; i += 2) {
        System.out.print(i + " ");
    }

---

# 30. Pattern Recognition — Count Even Numbers

> [!important]
> **If the question says:**
>
> "Count even numbers from 1 to N."
>
> Think:
>
> $$\boxed{\left\lfloor\frac{n}{2}\right\rfloor}$$

---

# 31. Pattern Recognition — Count Odd Numbers

> [!important]
> **If the question says:**
>
> "Count odd numbers from 1 to N."
>
> Think:
>
> $$\boxed{\left\lceil\frac{n}{2}\right\rceil}$$

For positive integer $n$:

$$
\boxed{\frac{n+1}{2}}
$$

using integer division.

---

# 32. Pattern Recognition — Range [L, R]

Suppose the question asks:

> How many even numbers are present between $L$ and $R$?

First count the even numbers from `1` to `R`.

Then subtract the even numbers from `1` to `L-1`.

Formula:

$$
\boxed{
\left\lfloor\frac{R}{2}\right\rfloor
-
\left\lfloor\frac{L-1}{2}\right\rfloor
}
$$

### Example

Find the number of even numbers from `5` to `12`.

Count up to `12`:

$$
\left\lfloor\frac{12}{2}\right\rfloor=6
$$

Count up to `4`:

$$
\left\lfloor\frac{4}{2}\right\rfloor=2
$$

Therefore:

$$
6-2=4
$$

Even numbers:

    6 8 10 12

### Answer

$$
\boxed{4}
$$

---

# 33. Pattern Recognition — Count Odd Numbers in a Range

For the range $[L,R]$:

$$
\boxed{
\left\lceil\frac{R}{2}\right\rceil
-
\left\lceil\frac{L-1}{2}\right\rceil
}
$$

For positive integers, an integer-division-friendly approach is:

$$
\boxed{
\frac{R+1}{2}
-
\frac{L}{2}
}
$$

when both divisions are performed as positive integer divisions.

---

# 34. Example — Even Numbers in a Range

## Example 17

### Question

How many even numbers are between `10` and `20`, inclusive?

Even numbers:

    10 12 14 16 18 20

Count:

$$
6
$$

Using the formula:

$$
\left\lfloor\frac{20}{2}\right\rfloor
-
\left\lfloor\frac{9}{2}\right\rfloor
$$

$$
=10-4
$$

$$
=6
$$

### Answer

$$
\boxed{6}
$$

---

# 35. Example — Odd Numbers in a Range

## Example 18

### Question

How many odd numbers are between `10` and `20`, inclusive?

Odd numbers:

    11 13 15 17 19

Count:

$$
5
$$

### Answer

$$
\boxed{5}
$$

---

# 36. Parity Rules for Arithmetic

Parity means whether a number is even or odd.

| Operation | Result |
|---|---|
| Even + Even | Even |
| Even + Odd | Odd |
| Odd + Even | Odd |
| Odd + Odd | Even |
| Even × Even | Even |
| Even × Odd | Even |
| Odd × Even | Even |
| Odd × Odd | Odd |

### Subtraction

| Operation | Result |
|---|---|
| Even − Even | Even |
| Even − Odd | Odd |
| Odd − Even | Odd |
| Odd − Odd | Even |

### Division

Division is different.

For example:

$$
8/2=4
$$

but:

$$
7/2=3.5
$$

Therefore, do not blindly apply multiplication/addition parity rules to arbitrary division problems.

---

# 37. Important Insight — Last Digit

For positive decimal integers, parity can be determined from the last digit.

Even last digits:

$$
0,2,4,6,8
$$

Odd last digits:

$$
1,3,5,7,9
$$

Examples:

    248 → Even
    731 → Odd
    560 → Even
    999 → Odd

> [!tip]
> In a normal decimal integer, you do not need the entire number to determine parity. **Only the last digit matters.**

---

# 38. Example — Very Large Number

## Example 19

### Question

Determine whether:

$$
987654321987654321987654321
$$

is even or odd.

Look only at the last digit:

$$
1
$$

Since `1` is odd:

$$
\boxed{Odd}
$$

No large-number calculation is required.

---

# 39. Shortcut — Last Digit Test

> [!tip]
> **Shortcut**
>
> For a decimal number:
>
> Last digit in:
>
> $$0,2,4,6,8$$
>
> → Even
>
> Last digit in:
>
> $$1,3,5,7,9$$
>
> → Odd

This is useful in aptitude questions because it avoids unnecessary division.

---

# 40. Example — Parity Without Calculation

## Example 20

### Question

Determine whether:

$$
1234567\times246810
$$

is even or odd.

Look at the factors.

`246810` is even.

Therefore:

$$
Odd\times Even=Even
$$

### Answer

$$
\boxed{Even}
$$

No multiplication is required.

---

# 41. Example — Sum of Many Numbers

## Example 21

### Question

Determine whether the following sum is even or odd:

$$
17+28+35+46+51
$$

Classify each:

    17 → Odd
    28 → Even
    35 → Odd
    46 → Even
    51 → Odd

There are three odd numbers.

Important rule:

- Even number of odd terms → even sum
- Odd number of odd terms → odd sum

There are:

$$
3
$$

odd terms.

Therefore:

$$
\boxed{Odd}
$$

---

# 42. Shortcut — Sum Parity

> [!tip]
> To determine whether a sum is even or odd, **count the number of odd terms**.
>
> If the number of odd terms is:
>
> Even → sum is even.
>
> Odd → sum is odd.

Example:

$$
3+5+8+10
$$

Odd terms:

$$
3,5
$$

There are `2` odd terms.

Therefore:

$$
\boxed{Even}
$$

---

# 43. Example — Product Parity

## Example 22

### Question

Determine whether:

$$
3\times5\times7\times8\times11
$$

is even or odd.

There is one even factor:

$$
8
$$

Therefore, the entire product is even.

### Answer

$$
\boxed{Even}
$$

> [!tip]
> For a product of integers:
>
> **If at least one factor is even, the product is even.**
>
> The product is odd only when **every factor is odd**.

---

# 44. Common Programming Implementation

### Using `if else`

    if (n % 2 == 0) {
        System.out.println("Even");
    } else {
        System.out.println("Odd");
    }

### Using Ternary Operator

    String result = (n % 2 == 0) ? "Even" : "Odd";

    System.out.println(result);

> [!important]
> The `if else` version is usually easier for beginners and easier to read during coding tests.

---

# 45. Example — Array Even/Odd Classification

## Example 23

### Question

For:

    10 15 22 31 44

print whether each number is even or odd.

### Code

    int[] arr = {10, 15, 22, 31, 44};

    for (int num : arr) {

        if (num % 2 == 0) {
            System.out.println(num + " → Even");
        } else {
            System.out.println(num + " → Odd");
        }
    }

### Answer

    10 → Even
    15 → Odd
    22 → Even
    31 → Odd
    44 → Even

---

# 46. Example — Count Even and Odd in an Array

## Example 24

### Question

Count even and odd numbers in:

    10 15 22 31 44 57

### Code

    int[] arr = {10, 15, 22, 31, 44, 57};

    int even = 0;
    int odd = 0;

    for (int num : arr) {

        if (num % 2 == 0) {
            even++;
        } else {
            odd++;
        }
    }

    System.out.println("Even = " + even);
    System.out.println("Odd = " + odd);

### Classification

Even:

    10, 22, 44

Count:

$$
3
$$

Odd:

    15, 31, 57

Count:

$$
3
$$

### Answer

$$
\boxed{Even=3,\ Odd=3}
$$

---

# 47. Example — Sum Even and Odd Separately

## Example 25

### Question

For:

    1 2 3 4 5 6

find the sum of even numbers and odd numbers separately.

### Code

    int[] arr = {1, 2, 3, 4, 5, 6};

    int evenSum = 0;
    int oddSum = 0;

    for (int num : arr) {

        if (num % 2 == 0) {
            evenSum += num;
        } else {
            oddSum += num;
        }
    }

    System.out.println("Even Sum = " + evenSum);
    System.out.println("Odd Sum = " + oddSum);

### Calculation

Even:

$$
2+4+6=12
$$

Odd:

$$
1+3+5=9
$$

### Answer

$$
\boxed{Even\ Sum=12}
$$

$$
\boxed{Odd\ Sum=9}
$$

---

# 48. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Using `/` Instead of `%`

Wrong:

    if (n / 2 == 0)

This does not check whether a number is even.

Correct:

    if (n % 2 == 0)

Why?

`%` gives the remainder.

`/` gives the quotient.

---

### Mistake 2 — Forgetting Zero

Wrong assumption:

    0 → Odd

Correct:

$$
0\%2=0
$$

Therefore:

$$
\boxed{0\text{ is Even}}
$$

---

### Mistake 3 — Checking Only Positive Numbers

Negative numbers can also be even or odd.

Examples:

$$
-8\rightarrow Even
$$

$$
-7\rightarrow Odd
$$

---

### Mistake 4 — Multiplying Huge Numbers Unnecessarily

Question:

$$
999999999\times2468
$$

Instead of calculating the product, notice:

$$
2468\rightarrow Even
$$

Therefore:

$$
Odd\times Even=Even
$$

Answer:

$$
\boxed{Even}
$$

---

### Mistake 5 — Confusing Odd Number with Non-Divisibility

A number is odd when:

$$
n\%2\neq0
$$

For integer inputs, that is the correct parity test.

---

### Mistake 6 — Using Floating-Point Logic

For integer parity, use:

    n % 2

Do not convert the number to floating point unnecessarily.

---

### Mistake 7 — Incorrect Range Counting

For the range $[L,R]$, do not simply calculate:

$$
\frac{R-L}{2}
$$

without considering whether the endpoints are even or odd.

Use the counting formulas instead.

---

# 49. Recognition Checklist

> [!important] Must Recognize Quickly

### Question says:

**"Check whether a number is even or odd."**

Think:

$$
\boxed{n\%2}
$$

---

### Question says:

**"Print even numbers."**

Think:

    start = 2
    step = 2

---

### Question says:

**"Print odd numbers."**

Think:

    start = 1
    step = 2

---

### Question says:

**"Count even numbers from 1 to N."**

Think:

$$
\boxed{\left\lfloor\frac{n}{2}\right\rfloor}
$$

---

### Question says:

**"Count odd numbers from 1 to N."**

Think:

$$
\boxed{\left\lceil\frac{n}{2}\right\rceil}
$$

---

### Question says:

**"Determine parity of a large number."**

Think:

**Look at the last digit.**

---

### Question says:

**"Determine parity of a sum."**

Think:

**Count the odd terms.**

---

### Question says:

**"Determine parity of a product."**

Think:

**Check whether at least one factor is even.**

---

# 50. Formula Sheet

## Basic Test

$$
\boxed{n\%2=0\Rightarrow Even}
$$

$$
\boxed{n\%2\neq0\Rightarrow Odd}
$$

## Mathematical Representation

$$
\boxed{Even=2k}
$$

$$
\boxed{Odd=2k+1}
$$

## Count Even Numbers from 1 to N

$$
\boxed{\left\lfloor\frac{n}{2}\right\rfloor}
$$

## Count Odd Numbers from 1 to N

$$
\boxed{\left\lceil\frac{n}{2}\right\rceil}
$$

For positive integer $n$:

$$
\boxed{\frac{n+1}{2}}
$$

using integer division.

## Count Even Numbers in [L, R]

$$
\boxed{
\left\lfloor\frac{R}{2}\right\rfloor
-
\left\lfloor\frac{L-1}{2}\right\rfloor
}
$$

## Sum of First N Even Numbers

$$
\boxed{n(n+1)}
$$

## Sum of First N Odd Numbers

$$
\boxed{n^2}
$$

## Number of Even Digits

Check each digit with:

$$
digit\%2=0
$$

## Number of Odd Digits

Check each digit with:

$$
digit\%2\neq0
$$

## Last Digit Rule

Even:

$$
\boxed{0,2,4,6,8}
$$

Odd:

$$
\boxed{1,3,5,7,9}
$$

---

# 51. Quick Revision

> [!summary] One-Minute Revision

    Even number
    → Exactly divisible by 2.
    → n % 2 == 0.

    Odd number
    → Not divisible by 2.
    → n % 2 != 0.

    Mathematical form
    → Even = 2k.
    → Odd = 2k + 1.

    Zero
    → Even.

    Positive or negative
    → Both can be even or odd.

    Last digit
    → 0, 2, 4, 6, 8 → Even.
    → 1, 3, 5, 7, 9 → Odd.

    Even + Even
    → Even.

    Odd + Odd
    → Even.

    Even + Odd
    → Odd.

    Even × Any
    → Even.

    Odd × Odd
    → Odd.

    At least one even factor
    → Product is even.

    All factors odd
    → Product is odd.

    Count evens from 1 to N
    → floor(N / 2).

    Count odds from 1 to N
    → ceil(N / 2).

    First N even numbers
    → Sum = N(N + 1).

    First N odd numbers
    → Sum = N².

    Print evens
    → Start at 2, increment by 2.

    Print odds
    → Start at 1, increment by 2.

    Parity of a sum
    → Count odd terms.

    Parity of a product
    → Check whether any factor is even.

    Large decimal number
    → Check only the last digit.

    Programming operator
    → % gives the remainder.

    Main recognition
    → "Even or odd?" → Think % 2.

---

## Golden Memory Trick

**If `n % 2 == 0`, it is Even; otherwise, it is Odd.**

## One-Line Recognition

**Whenever a coding problem asks about parity, immediately think of the remainder when dividing by `2`.**