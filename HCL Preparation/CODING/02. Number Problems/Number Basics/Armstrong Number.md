---
type: concept
subject: coding
topic: "Armstrong Number"
parent: "Number Basics"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - number-problems
  - number-basics
  - armstrong-number
  - java
  - digit-problems
  - mathematics
wikilinks:
  - "[[Number Basics]]"
  - "[[Digit Problems]]"
  - "[[Perfect Number]]"
  - "[[Strong Number]]"
  - "[[Power of Number]]"
---

# Armstrong Number

## 1. Core Concept

> [!summary]
> An **Armstrong number** is a number in which the sum of each digit raised to the power of the **number of digits** is equal to the original number.
>
> For a number with $d$ digits:
>
> $$n=d_1^d+d_2^d+\cdots+d_k^d$$
>
> Example:
>
> $$153$$
>
> It has `3` digits.
>
> $$1^3+5^3+3^3$$
>
> $$=1+125+27$$
>
> $$=153$$
>
> Therefore:
>
> $$\boxed{153\text{ is an Armstrong Number}}$$

The most important idea is:

**Count digits → extract each digit → raise it to digit count → add → compare with original number.**

---

# 2. Basic Meaning

For a number $n$ containing $d$ digits:

$$
\boxed{
n=\sum(\text{each digit})^d
}
$$

If the calculated sum equals the original number, the number is an Armstrong number.

### Example

Consider:

$$
370
$$

Number of digits:

$$
3
$$

Calculation:

$$
3^3+7^3+0^3
$$

$$
=27+343+0
$$

$$
=370
$$

Therefore:

$$
\boxed{370\text{ is an Armstrong Number}}
$$

---

# 3. Main Formula

If:

$$
n
$$

has:

$$
d
$$

digits, and its digits are:

$$
a_1,a_2,\ldots,a_d
$$

then:

$$
\boxed{
n=a_1^d+a_2^d+\cdots+a_d^d
}
$$

### Condition

$$
\boxed{\text{Armstrong if calculated sum}=n}
$$

Otherwise:

$$
\boxed{\text{Not Armstrong}}
$$

---

# 4. Important Properties

## Property 1 — Digit Count Determines the Power

This is the most important rule.

For a 3-digit number:

$$
\boxed{\text{Power}=3}
$$

For a 4-digit number:

$$
\boxed{\text{Power}=4}
$$

For a 5-digit number:

$$
\boxed{\text{Power}=5}
$$

Do not always use cube.

---

## Property 2 — Every Single-Digit Number Is Armstrong

For a single-digit number:

$$
d=1
$$

Therefore:

$$
n^1=n
$$

So:

$$
\boxed{0,1,2,3,4,5,6,7,8,9}
$$

are all Armstrong numbers under the standard definition.

> [!important]
> Single-digit numbers are Armstrong numbers because their digit count is `1`.

---

## Property 3 — Common 3-Digit Armstrong Numbers

The well-known 3-digit Armstrong numbers are:

$$
\boxed{153,370,371,407}
$$

Examples:

$$
153=1^3+5^3+3^3
$$

$$
370=3^3+7^3+0^3
$$

$$
371=3^3+7^3+1^3
$$

$$
407=4^3+0^3+7^3
$$

---

## Property 4 — Zero Contributes Nothing

For any positive exponent:

$$
0^d=0
$$

Example:

$$
407
$$

contains digit `0`.

Its contribution is:

$$
0^3=0
$$

---

## Property 5 — Armstrong Is Not the Same as Perfect

These are different concepts.

Perfect number:

$$
\text{Sum of proper divisors}=n
$$

Armstrong number:

$$
\text{Sum of powered digits}=n
$$

Example:

$$
153
$$

is Armstrong but not perfect.

---

# 5. Basic Example — 153

## Example 1

### Question

Check whether `153` is an Armstrong number.

### Step 1 — Count digits

`153` has:

$$
d=3
$$

digits.

### Step 2 — Extract digits

    1
    5
    3

### Step 3 — Raise each digit to the third power

$$
1^3=1
$$

$$
5^3=125
$$

$$
3^3=27
$$

### Step 4 — Add

$$
1+125+27=153
$$

### Step 5 — Compare

$$
153=153
$$

### Answer

$$
\boxed{153\text{ is an Armstrong Number}}
$$

---

# 6. Basic Example — 370

## Example 2

### Question

Check whether `370` is an Armstrong number.

Number of digits:

$$
3
$$

Calculation:

$$
3^3+7^3+0^3
$$

$$
=27+343+0
$$

$$
=370
$$

Therefore:

$$
\boxed{370\text{ is an Armstrong Number}}
$$

---

# 7. Basic Example — 371

## Example 3

### Question

Check whether `371` is an Armstrong number.

Number of digits:

$$
3
$$

Calculation:

$$
3^3+7^3+1^3
$$

$$
=27+343+1
$$

$$
=371
$$

Therefore:

$$
\boxed{371\text{ is an Armstrong Number}}
$$

---

# 8. Basic Example — 407

## Example 4

### Question

Check whether `407` is an Armstrong number.

Calculation:

$$
4^3+0^3+7^3
$$

$$
=64+0+343
$$

$$
=407
$$

Therefore:

$$
\boxed{407\text{ is an Armstrong Number}}
$$

---

# 9. Basic Example — Not Armstrong

## Example 5

### Question

Check whether `123` is an Armstrong number.

Number of digits:

$$
3
$$

Calculate:

$$
1^3+2^3+3^3
$$

$$
=1+8+27
$$

$$
=36
$$

But:

$$
36\neq123
$$

Therefore:

$$
\boxed{123\text{ is Not an Armstrong Number}}
$$

---

# 10. Basic Java Program

## Example 6

### Question

Write a Java program to check whether a number is an Armstrong number.

### Code

    import java.util.Scanner;

    class Main {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            int original = n;
            int digits = String.valueOf(n).length();
            int sum = 0;

            while (n > 0) {

                int digit = n % 10;

                sum += Math.pow(digit, digits);

                n /= 10;
            }

            if (sum == original) {
                System.out.println("Armstrong Number");
            } else {
                System.out.println("Not an Armstrong Number");
            }
        }
    }

### Main Pattern

    digit = n % 10
    → Extract last digit

    n /= 10
    → Remove last digit

    Math.pow(digit, digits)
    → Raise digit to required power

    sum += ...
    → Add contribution

---

# 11. Important Issue — Original Number

While processing digits, the number is repeatedly divided:

    n /= 10;

Therefore, after the loop:

$$
n=0
$$

So we must preserve the original value.

Use:

    int original = n;

Then compare:

    sum == original

> [!warning]
> Never compare the final modified `n` with `sum`.
>
> Store the original number before digit extraction.

---

# 12. Handling Zero

The basic loop:

    while (n > 0)

does not execute for:

$$
n=0
$$

But `0` is an Armstrong number.

A robust implementation should handle it explicitly.

### Code

    static boolean isArmstrong(int n) {

        if (n < 0) {
            return false;
        }

        int original = n;
        int digits = String.valueOf(n).length();
        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += (int) Math.pow(digit, digits);

            n /= 10;
        }

        return sum == original;
    }

For:

$$
n=0
$$

the sum remains:

$$
0
$$

and:

$$
sum=original=0
$$

Therefore:

$$
\boxed{0\text{ is Armstrong}}
$$

---

# 13. Counting Digits Without String

In coding interviews, you may be expected to solve the problem using arithmetic only.

### Code

    static int countDigits(int n) {

        if (n == 0) {
            return 1;
        }

        int count = 0;

        while (n > 0) {
            count++;
            n /= 10;
        }

        return count;
    }

### Example

For:

$$
153
$$

Iterations:

    153 → 15
     15 → 1
      1 → 0

Count:

$$
3
$$

Therefore:

$$
\boxed{3\text{ digits}}
$$

---

# 14. Complete Arithmetic-Based Solution

## Example 7

### Code

    static boolean isArmstrong(int n) {

        if (n < 0) {
            return false;
        }

        int original = n;

        int digits = 0;
        int temp = n;

        if (temp == 0) {
            digits = 1;
        } else {

            while (temp > 0) {
                digits++;
                temp /= 10;
            }
        }

        int sum = 0;
        temp = n;

        while (temp > 0) {

            int digit = temp % 10;

            sum += (int) Math.pow(digit, digits);

            temp /= 10;
        }

        return sum == original;
    }

### Flow

    Original number
          ↓
    Count digits
          ↓
    Extract digits
          ↓
    Raise each digit to digit count
          ↓
    Add
          ↓
    Compare with original
          ↓
    Armstrong / Not Armstrong

---

# 15. Example — Four-Digit Armstrong Number

## Example 8

### Question

Check whether `1634` is an Armstrong number.

Number of digits:

$$
4
$$

Therefore use fourth powers.

$$
1^4+6^4+3^4+4^4
$$

Calculate:

$$
1^4=1
$$

$$
6^4=1296
$$

$$
3^4=81
$$

$$
4^4=256
$$

Add:

$$
1+1296+81+256
$$

$$
=1634
$$

Therefore:

$$
\boxed{1634\text{ is an Armstrong Number}}
$$

---

# 16. Example — Another Four-Digit Armstrong Number

## Example 9

### Question

Check whether `8208` is an Armstrong number.

Number of digits:

$$
4
$$

Calculate:

$$
8^4+2^4+0^4+8^4
$$

$$
=4096+16+0+4096
$$

$$
=8208
$$

Therefore:

$$
\boxed{8208\text{ is an Armstrong Number}}
$$

---

# 17. Example — Not Armstrong

## Example 10

### Question

Check whether `1234` is an Armstrong number.

Number of digits:

$$
4
$$

Calculate:

$$
1^4+2^4+3^4+4^4
$$

$$
=1+16+81+256
$$

$$
=354
$$

Since:

$$
354\neq1234
$$

Therefore:

$$
\boxed{1234\text{ is Not an Armstrong Number}}
$$

---

# 18. Pattern Recognition — Digit Count

> [!important]
> **If the question says Armstrong number, first determine the number of digits.**
>
> Then:
>
> 1 digit → power 1
>
> 2 digits → power 2
>
> 3 digits → power 3
>
> 4 digits → power 4
>
> and so on.

This is the most important recognition rule.

---

# 19. Pattern Recognition — Digit Extraction

> [!important]
> **If the problem asks you to process every digit individually:**
>
> Think:
>
>     digit = n % 10;
>     n /= 10;
>
> `% 10` extracts the last digit.

Example:

$$
153\%10=3
$$

Then:

$$
153/10=15
$$

Next:

$$
15\%10=5
$$

Then:

$$
15/10=1
$$

---

# 20. Pattern Recognition — Armstrong Formula

> [!important]
> **If the question says:**
>
> "Sum of digits raised to the number of digits equals the original number."
>
> Immediately think:
>
> $$\boxed{\text{Armstrong Number}}
> $$

Example:

$$
153
$$

has 3 digits:

$$
1^3+5^3+3^3=153
$$

---

# 21. Pattern Recognition — Range of Armstrong Numbers

> [!important]
> **If the question says:**
>
> "Print all Armstrong numbers between L and R."
>
> Think:
>
>     for each number
>     → count digits
>     → calculate powered digit sum
>     → compare with original

Template:

    for (int n = L; n <= R; n++) {

        if (isArmstrong(n)) {
            System.out.print(n + " ");
        }
    }

---

# 22. Example — Armstrong Numbers from 1 to 500

## Example 11

### Question

Print all Armstrong numbers from `1` to `500`.

Single-digit Armstrong numbers:

$$
0,1,2,3,4,5,6,7,8,9
$$

Three-digit Armstrong numbers in this range:

$$
153,370,371,407
$$

Therefore, for the range `1` to `500`:

$$
\boxed{1,2,3,4,5,6,7,8,9,153,370,371,407}
$$

---

# 23. Example — Count Armstrong Numbers in a Range

## Example 12

### Question

How many Armstrong numbers are between `1` and `500`?

Armstrong numbers:

$$
1,2,3,4,5,6,7,8,9
$$

There are:

$$
9
$$

single-digit Armstrong numbers.

Additional Armstrong numbers:

$$
153,370,371,407
$$

Count:

$$
4
$$

Total:

$$
9+4=13
$$

### Answer

$$
\boxed{13}
$$

---

# 24. Common Armstrong Numbers to Remember

For quick recognition:

### Single Digit

$$
\boxed{0,1,2,3,4,5,6,7,8,9}
$$

### Three Digit

$$
\boxed{153,370,371,407}
$$

### Four Digit

$$
\boxed{1634,8208,9474}
$$

Other well-known examples include:

$$
54748,92727,93084
$$

for five-digit Armstrong numbers.

> [!tip]
> Memorization is useful for small aptitude questions, but in coding problems you should implement the general algorithm.

---

# 25. Example — 9474

## Example 13

### Question

Check whether `9474` is Armstrong.

It has:

$$
4
$$

digits.

Calculate:

$$
9^4+4^4+7^4+4^4
$$

$$
=6561+256+2401+256
$$

$$
=9474
$$

Therefore:

$$
\boxed{9474\text{ is an Armstrong Number}}
$$

---

# 26. Example — Single-Digit Number

## Example 14

### Question

Is `7` an Armstrong number?

Number of digits:

$$
1
$$

Therefore:

$$
7^1=7
$$

So:

$$
\boxed{7\text{ is an Armstrong Number}}
$$

---

# 27. Example — Zero

## Example 15

### Question

Is `0` an Armstrong number?

Number of digits:

$$
1
$$

Therefore:

$$
0^1=0
$$

Hence:

$$
\boxed{0\text{ is an Armstrong Number}}
$$

---

# 28. Armstrong vs Palindrome

These are completely different concepts.

| Concept | Condition |
|---|---|
| Armstrong | Powered digit sum = original |
| Palindrome | Number reads the same backward |

Example:

`153`:

- Armstrong → Yes
- Palindrome → No

Example:

`121`:

- Armstrong → No
- Palindrome → Yes

> [!warning]
> Do not confuse digit reversal with Armstrong calculation.

---

# 29. Armstrong vs Perfect Number

| Concept | What is calculated? |
|---|---|
| Armstrong | Powers of digits |
| Perfect | Sum of proper divisors |

Example:

$$
153
$$

Armstrong:

$$
1^3+5^3+3^3=153
$$

But its proper divisors do not sum to `153`.

Therefore:

$$
\boxed{153\text{ is Armstrong, not Perfect}}
$$

---

# 30. Example — Armstrong Number Using a Function

## Example 16

### Code

    static boolean isArmstrong(int n) {

        int original = n;

        int digits = String.valueOf(n).length();

        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += (int) Math.pow(digit, digits);

            n /= 10;
        }

        return sum == original;
    }

Usage:

    if (isArmstrong(153)) {
        System.out.println("Armstrong");
    }

### Output

    Armstrong

---

# 31. Example — Find Armstrong Numbers in an Array

## Example 17

### Question

Find Armstrong numbers in:

    153 120 370 123 407 500

Armstrong numbers:

    153
    370
    407

### Answer

$$
\boxed{153,370,407}
$$

---

# 32. Example — Sum Armstrong Numbers in an Array

## Example 18

### Question

Find the sum of Armstrong numbers in:

    153 100 370 200 407

Armstrong numbers:

$$
153,370,407
$$

Sum:

$$
153+370+407
$$

$$
=930
$$

### Answer

$$
\boxed{930}
$$

---

# 33. Example — Largest Armstrong Number in an Array

## Example 19

### Question

Find the largest Armstrong number in:

    153 370 100 407 200

Armstrong numbers:

    153
    370
    407

Largest:

$$
407
$$

### Answer

$$
\boxed{407}
$$

---

# 34. Example — Armstrong Number With Zero Digit

## Example 20

### Question

Verify `407`.

Number of digits:

$$
3
$$

Calculation:

$$
4^3+0^3+7^3
$$

$$
=64+0+343
$$

$$
=407
$$

Therefore:

$$
\boxed{407\text{ is Armstrong}}
$$

> [!important]
> A zero digit contributes:
>
> $$0^d=0$$
>
> but it still counts as one of the digits when determining `d`.

---

# 35. Common Exam Pattern — Count Digits First

This pattern appears in many number problems.

For:

$$
9474
$$

the digit count is:

$$
4
$$

Therefore use:

$$
digit^4
$$

For:

$$
153
$$

the digit count is:

$$
3
$$

Therefore use:

$$
digit^3
$$

> [!tip]
> **Never choose the power before counting the digits.**

---

# 36. Common Exam Pattern — Extract Every Digit

The standard arithmetic pattern is:

    while (n > 0) {

        int digit = n % 10;

        // process digit

        n /= 10;
    }

This pattern is useful for:

- Armstrong Number
- Palindrome Number
- Reverse Number
- Sum of Digits
- Digit Frequency
- Digit Product
- Count Digits
- Number Formation

> [!important]
> Master this pattern because it appears across many number-based coding questions.

---

# 37. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Check Armstrong

    count digits
    →
    extract digits
    →
    power each digit
    →
    sum
    →
    compare

---

### Pattern 2 — Print Armstrong Numbers

Loop through the range and call `isArmstrong()`.

---

### Pattern 3 — Count Armstrong Numbers

Use:

    if (isArmstrong(n)) {
        count++;
    }

---

### Pattern 4 — Sum Armstrong Numbers

Use:

    if (isArmstrong(n)) {
        sum += n;
    }

---

### Pattern 5 — Armstrong Number in Array

Check each element independently.

---

### Pattern 6 — Arithmetic Digit Extraction

Use:

    digit = n % 10;
    n /= 10;

---

### Pattern 7 — Digit Count

Use repeated division by `10`.

---

### Pattern 8 — Preserve Original Number

Use:

    int original = n;

before modifying `n`.

---

# 38. Shortcuts

> [!tip]
> **Shortcut 1 — Remember Common Values**
>
> Three-digit Armstrong numbers:
>
> $$\boxed{153,370,371,407}
> $$

> [!tip]
> **Shortcut 2 — Single-Digit Numbers**
>
> Every single-digit number is Armstrong:
>
> $$\boxed{0\text{ through }9}
> $$

> [!tip]
> **Shortcut 3 — Count Digits First**
>
> The exponent is exactly the number of digits.
>
> 3-digit → cube.
>
> 4-digit → fourth power.
>
> 5-digit → fifth power.

> [!tip]
> **Shortcut 4 — Zero Digit**
>
> A zero contributes:
>
> $$0^d=0$$
>
> but it still counts toward the digit count.

> [!tip]
> **Shortcut 5 — Preserve Original**
>
> Before extracting digits:
>
>     original = n;
>
> because `n` will become zero.

> [!tip]
> **Shortcut 6 — Use Arithmetic Digit Extraction**
>
> `% 10` → last digit.
>
> `/ 10` → remove last digit.

---

# 39. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Always Using Cube

Wrong for:

$$
1634
$$

because it has four digits.

Correct:

$$
1^4+6^4+3^4+4^4
$$

---

### Mistake 2 — Forgetting to Count Digits

The exponent depends on the total number of digits.

Always calculate:

$$
d=\text{number of digits}
$$

first.

---

### Mistake 3 — Losing the Original Number

After:

    n /= 10;

the original value is lost.

Correct:

    int original = n;

---

### Mistake 4 — Forgetting Zero

For:

$$
407
$$

you must include:

$$
0^3
$$

Even though its contribution is zero.

---

### Mistake 5 — Confusing Armstrong With Palindrome

Armstrong uses:

$$
\text{digit}^{\text{digit count}}
$$

Palindrome uses:

$$
\text{reverse of number}
$$

---

### Mistake 6 — Using String Logic When Arithmetic Is Expected

String conversion is often acceptable in general programming, but some coding tests expect arithmetic digit processing.

Know both approaches.

---

### Mistake 7 — Incorrect Handling of 0

A loop using:

    while (n > 0)

does not process `0`.

Handle zero separately if the problem includes it.

---

### Mistake 8 — Using `Math.pow()` Carelessly

`Math.pow()` returns a `double`.

For integer calculations:

    sum += (int) Math.pow(digit, digits);

For values where overflow is possible, use an appropriate integer type and consider implementing integer power.

---

# 40. Integer Power Alternative

For small digit powers, `Math.pow()` is convenient.

But you can also implement integer power manually.

### Code

    static long power(int base, int exponent) {

        long result = 1;

        for (int i = 0; i < exponent; i++) {
            result *= base;
        }

        return result;
    }

Then:

    sum += power(digit, digits);

This avoids floating-point arithmetic.

> [!tip]
> For placement coding, knowing both `Math.pow()` and an integer-power loop is useful.

---

# 41. Time and Space Complexity

Let:

$$
d=\text{number of digits}
$$

To count digits:

$$
O(d)
$$

To process every digit:

$$
O(d)
$$

Therefore:

$$
\boxed{O(d)}
$$

Since:

$$
d=\log_{10}(n)+1
$$

the complexity can also be expressed as:

$$
\boxed{O(\log n)}
$$

Space:

$$
\boxed{O(1)}
$$

for the iterative approach.

---

# 42. Advanced Example — General Armstrong Function

## Example 21

### Code

    static boolean isArmstrong(int n) {

        if (n < 0) {
            return false;
        }

        int original = n;

        int digits = 0;
        int temp = n;

        if (temp == 0) {
            digits = 1;
        } else {

            while (temp > 0) {
                digits++;
                temp /= 10;
            }
        }

        long sum = 0;
        temp = n;

        while (temp > 0) {

            int digit = temp % 10;

            long power = 1;

            for (int i = 0; i < digits; i++) {
                power *= digit;
            }

            sum += power;

            temp /= 10;
        }

        return sum == original;
    }

This version:

- Handles digit count.
- Preserves the original.
- Extracts digits arithmetically.
- Uses integer power.
- Avoids floating-point calculations.

---

# 43. Advanced Example — Armstrong Numbers Up to N

## Example 22

### Question

Print all Armstrong numbers from `1` to `10000`.

### Approach

    for each number n
        ↓
    count digits
        ↓
    calculate powered digit sum
        ↓
    compare with original
        ↓
    print if equal

### Known results in this range

$$
\boxed{
1,2,3,4,5,6,7,8,9,
153,370,371,407,
1634,8208,9474
}
$$

---

# 44. Recognition Checklist

> [!important] Must Recognize Quickly

**"Check Armstrong number."**

Think:

$$
\boxed{\text{digit count}\rightarrow\text{digit power sum}\rightarrow\text{compare}}
$$

---

**"Sum of digits raised to number of digits."**

Think:

$$
\boxed{Armstrong}
$$

---

**"Process every digit."**

Think:

    digit = n % 10;
    n /= 10;

---

**"Three-digit Armstrong."**

Think:

$$
\boxed{digit^3}
$$

---

**"Four-digit Armstrong."**

Think:

$$
\boxed{digit^4}
$$

---

**"Print Armstrong numbers in range."**

Think:

    for each number
    → isArmstrong()

---

**"Armstrong number in array."**

Think:

    for each element
    → check independently

---

# 45. Formula Sheet

## Armstrong Condition

For a $d$-digit number:

$$
\boxed{
n=\sum_{i=1}^{d}a_i^d
}
$$

## Three-Digit Number

$$
\boxed{
n=a^3+b^3+c^3
}
$$

## Four-Digit Number

$$
\boxed{
n=a^4+b^4+c^4+d^4
}
$$

## Digit Extraction

$$
\boxed{digit=n\%10}
$$

## Remove Last Digit

$$
\boxed{n=\lfloor n/10\rfloor}
$$

## Zero Contribution

$$
\boxed{0^d=0}
$$

## Single-Digit Armstrong

$$
\boxed{n^1=n}
$$

## Common Three-Digit Armstrong Numbers

$$
\boxed{153,370,371,407}
$$

## Common Four-Digit Armstrong Numbers

$$
\boxed{1634,8208,9474}
$$

## Complexity

$$
\boxed{O(\log n)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 46. Quick Revision

> [!summary] One-Minute Revision

    Armstrong Number
    → Sum of each digit raised to the number of digits
      equals the original number.

    Formula
    → a₁^d + a₂^d + ... + aₖ^d = N.

    First step
    → Count digits.

    Three digits
    → Cube every digit.

    Four digits
    → Fourth power every digit.

    Digit extraction
    → digit = n % 10.

    Remove digit
    → n /= 10.

    Preserve original
    → int original = n.

    0
    → Armstrong.

    1 through 9
    → All are Armstrong.

    Common 3-digit Armstrong numbers
    → 153, 370, 371, 407.

    Common 4-digit Armstrong numbers
    → 1634, 8208, 9474.

    Check Armstrong
    → Calculate powered digit sum.
    → Compare with original.

    Armstrong ≠ Palindrome.

    Armstrong ≠ Perfect Number.

    Range problem
    → Check every number.

    Array problem
    → Check every element.

    Main coding pattern
    → % 10 extracts a digit.
    → / 10 removes a digit.

    Complexity
    → O(log N).

    Space
    → O(1).

---

## Golden Memory Trick

**Count the digits, raise every digit to that count, add them, and see whether you get the original number back.**

## One-Line Recognition

**When you see "sum of powers of digits equals the number," immediately think Armstrong Number.**