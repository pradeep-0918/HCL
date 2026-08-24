---
type: concept
subject: coding
topic: "Count Digits"
parent: "Digit Problems"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - number-problems
  - digit-problems
  - count-digits
  - java
  - number-basics
wikilinks:
  - "[[Digit Problems]]"
  - "[[Number Basics]]"
  - "[[Sum of Digits]]"
  - "[[Reverse Number]]"
  - "[[Palindrome Number]]"
---

# Count Digits

## 1. Core Concept

> [!summary]
> **Count Digits** means finding how many digits are present in an integer.
>
> The standard arithmetic method repeatedly divides the number by `10` until it becomes `0`.
>
> Example:
>
> $$12345\rightarrow1234\rightarrow123\rightarrow12\rightarrow1\rightarrow0$$
>
> Number of divisions:
>
> $$5$$
>
> Therefore:
>
> $$\boxed{12345\text{ has }5\text{ digits}}
> $$

The key idea is:

**Remove one digit at a time using `/ 10` and count how many times you can do it.**

---

# 2. Basic Meaning

A decimal number contains digits in the range:

$$
0\text{ to }9
$$

For a positive integer:

$$
1234
$$

the digits are:

$$
1,2,3,4
$$

Therefore:

$$
\boxed{4\text{ digits}}
$$

The arithmetic method is:

    count = 0

    while n > 0
        n = n / 10
        count++

---

# 3. Main Formula

For a positive integer $N$:

$$
\boxed{
\text{Number of digits}=\lfloor\log_{10}(N)\rfloor+1
}
$$

Example:

$$
N=1000
$$

Then:

$$
\log_{10}(1000)=3
$$

Therefore:

$$
3+1=4
$$

So:

$$
\boxed{1000\text{ has }4\text{ digits}}
$$

> [!important]
> The logarithm formula is mathematically useful, but the repeated-division method is usually easier to implement safely in beginner coding problems.

---

# 4. Important Properties

## Property 1 — Dividing by 10 Removes One Digit

For integer division:

$$
12345/10=1234
$$

Then:

$$
1234/10=123
$$

Then:

$$
123/10=12
$$

Then:

$$
12/10=1
$$

Then:

$$
1/10=0
$$

Every division removes one digit.

---

## Property 2 — Positive Numbers

For:

$$
N>0
$$

the algorithm is:

    count = 0

    while n > 0:
        count++
        n /= 10

---

## Property 3 — Zero Needs Special Handling

The loop:

    while (n > 0)

does not execute for:

$$
n=0
$$

But mathematically:

$$
0
$$

has:

$$
1
$$

digit.

Therefore:

$$
\boxed{\text{digits}(0)=1}
$$

---

## Property 4 — Negative Numbers

Usually, when counting digits, the negative sign is **not counted as a digit**.

Example:

$$
-12345
$$

has:

$$
5
$$

digits.

Therefore:

$$
\boxed{-12345\text{ has }5\text{ digits}}
$$

Use:

$$
|N|
$$

when necessary.

---

# 5. Basic Example — 123

## Example 1

### Question

Count the number of digits in `123`.

### Step 1

Start:

$$
n=123
$$

### Step 2

Divide by `10`:

$$
123/10=12
$$

Count:

$$
1
$$

### Step 3

$$
12/10=1
$$

Count:

$$
2
$$

### Step 4

$$
1/10=0
$$

Count:

$$
3
$$

Therefore:

$$
\boxed{123\text{ has }3\text{ digits}}
$$

---

# 6. Basic Example — 98765

## Example 2

### Question

Count the digits in `98765`.

Sequence:

$$
98765\rightarrow9876\rightarrow987\rightarrow98\rightarrow9\rightarrow0
$$

There are:

$$
5
$$

divisions.

Therefore:

$$
\boxed{5\text{ digits}}
$$

---

# 7. Basic Example — Single Digit

## Example 3

### Question

How many digits are present in `7`?

Since `7` is a single digit:

$$
\boxed{1}
$$

---

# 8. Basic Example — Zero

## Example 4

### Question

How many digits are present in `0`?

The number `0` itself is one digit.

Therefore:

$$
\boxed{1}
$$

> [!warning]
> Do not return `0` digits for input `0`.

---

# 9. Basic Example — Negative Number

## Example 5

### Question

How many digits are present in `-1234`?

Ignore the negative sign.

Consider:

$$
|-1234|=1234
$$

`1234` has:

$$
4
$$

digits.

Therefore:

$$
\boxed{4}
$$

---

# 10. Standard Java Program

## Example 6

### Question

Write a Java program to count the digits of an integer.

### Code

    import java.util.Scanner;

    class Main {

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            n = Math.abs(n);

            int count = 0;

            if (n == 0) {
                count = 1;
            } else {

                while (n > 0) {
                    count++;
                    n /= 10;
                }
            }

            System.out.println(count);
        }
    }

### Main Pattern

    n /= 10;
    count++;

This removes one digit and records that one digit was removed.

---

# 11. Simple Function

## Example 7

### Code

    static int countDigits(int n) {

        n = Math.abs(n);

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

For:

    countDigits(12345)

result:

$$
\boxed{5}
$$

---

# 12. Pattern Recognition — Count Digits

> [!important]
> **If the question asks "How many digits are in N?"**
>
> Think immediately:
>
>     count = 0
>     while n > 0:
>         count++
>         n /= 10

This is the standard digit-processing pattern.

---

# 13. Pattern Recognition — Digit-by-Digit Problem

> [!important]
> If a problem requires processing every digit, think:
>
>     while (n > 0) {
>         int digit = n % 10;
>         n /= 10;
>     }
>
> `% 10` → extracts a digit.
>
> `/ 10` → removes a digit.

This pattern is used in:

- Count Digits
- Sum of Digits
- Reverse Number
- Palindrome Number
- Armstrong Number
- Strong Number
- Digit Frequency
- Digit Product

---

# 14. Example — Extracting Digits

## Example 8

### Question

What digits are extracted from `1234` using `% 10`?

Start:

$$
1234\%10=4
$$

Then:

$$
1234/10=123
$$

Next:

$$
123\%10=3
$$

Then:

$$
123/10=12
$$

Next:

$$
12\%10=2
$$

Then:

$$
12/10=1
$$

Finally:

$$
1\%10=1
$$

Therefore digits are extracted in reverse order:

$$
\boxed{4,3,2,1}
$$

---

# 15. Count Digits vs Extract Digits

| Operation | Expression | Purpose |
|---|---|---|
| Extract last digit | `n % 10` | Get digit |
| Remove last digit | `n / 10` | Delete digit |
| Count digits | Repeated `/ 10` | Count digits |
| Sum digits | `% 10` + `/ 10` | Add digits |
| Reverse | `% 10` + place value | Build reverse |
| Palindrome | Reverse + compare | Check symmetry |

> [!tip]
> Memorize this pair:
>
> $$\boxed{\%10=\text{get digit}}
> $$
>
> $$\boxed{/10=\text{remove digit}}
> $$

---

# 16. Example — Count Digits Using String

## Example 9

Java also allows:

    int count = String.valueOf(Math.abs(n)).length();

For:

    n = 12345

we get:

$$
\boxed{5}
$$

### Comparison

| Method | Advantage |
|---|---|
| Arithmetic | Excellent for coding logic |
| String | Very simple |
| Logarithm | Mathematical shortcut |

> [!important]
> For placement coding, learn the arithmetic method first because it directly teaches digit manipulation.

---

# 17. Logarithm Method

For:

$$
N>0
$$

use:

$$
\boxed{\lfloor\log_{10}(N)\rfloor+1}
$$

### Example

For:

$$
N=54321
$$

$$
\log_{10}(54321)\approx4.735
$$

Therefore:

$$
\lfloor4.735\rfloor+1
$$

$$
=4+1
$$

$$
=5
$$

Answer:

$$
\boxed{5}
$$

---

# 18. Important Limitation of Logarithm Method

The logarithm formula does not directly work for:

$$
N=0
$$

because:

$$
\log_{10}(0)
$$

is undefined.

It also needs separate handling for negative numbers.

Therefore:

> [!warning]
> If using the logarithm method:
>
> - Handle `0` separately.
> - Use absolute value for negative numbers.
> - Be aware of floating-point precision.

For beginner coding questions, repeated division is generally safer.

---

# 19. Example — 100000

## Example 10

### Question

Count digits in `100000`.

Using repeated division:

$$
100000
\rightarrow10000
\rightarrow1000
\rightarrow100
\rightarrow10
\rightarrow1
\rightarrow0
$$

Number of digits:

$$
6
$$

Therefore:

$$
\boxed{6}
$$

---

# 20. Example — 1000000

## Example 11

### Question

Count digits in `1000000`.

There are six zeros after `1`.

Therefore:

$$
\boxed{7\text{ digits}}
$$

Using the formula:

$$
\log_{10}(1000000)=6
$$

So:

$$
6+1=7
$$

---

# 21. Example — 999

## Example 12

### Question

Count digits in `999`.

$$
999\rightarrow99\rightarrow9\rightarrow0
$$

Therefore:

$$
\boxed{3}
$$

---

# 22. Example — 1001

## Example 13

### Question

Count digits in `1001`.

Digits:

$$
1,0,0,1
$$

Therefore:

$$
\boxed{4}
$$

> [!important]
> Zeros in the middle of a number are still digits.

---

# 23. Advanced Example — Count Digits Without Modifying Original

Sometimes you need the original number later.

### Code

    static int countDigits(int n) {

        int temp = Math.abs(n);

        if (temp == 0) {
            return 1;
        }

        int count = 0;

        while (temp > 0) {

            count++;

            temp /= 10;
        }

        return count;
    }

The original `n` remains unchanged.

> [!tip]
> Use a temporary variable when the original number is needed later.

---

# 24. Example — Count Digits and Preserve Number

## Example 14

### Question

Count the digits of `153` and then calculate the sum of its digits.

First count:

$$
153\rightarrow15\rightarrow1\rightarrow0
$$

So:

$$
count=3
$$

Now process the original number:

$$
1+5+3=9
$$

Therefore:

$$
\boxed{\text{Digits}=3,\quad\text{Digit Sum}=9}
$$

### Code Pattern

    int temp = n;

    int count = 0;

    while (temp > 0) {
        count++;
        temp /= 10;
    }

    // n is still available here

---

# 25. Advanced Example — Number of Digits in an Array

## Example 15

### Question

For the array:

    [12, 345, 7, 10000]

find the number of digits of each element.

Results:

| Number | Digits |
|---:|---:|
| 12 | 2 |
| 345 | 3 |
| 7 | 1 |
| 10000 | 5 |

Therefore:

$$
\boxed{2,3,1,5}
$$

---

# 26. Advanced Example — Largest Number of Digits

## Example 16

### Question

Find the maximum digit count in:

    [12, 3456, 78, 12345, 9]

Digit counts:

    12    → 2
    3456  → 4
    78    → 2
    12345 → 5
    9     → 1

Maximum:

$$
\boxed{5}
$$

---

# 27. Advanced Example — Count Numbers Having K Digits

## Example 17

### Question

How many numbers in:

    [12, 345, 7, 100, 56, 999]

have exactly `2` digits?

Check:

    12  → 2 digits
    345 → 3 digits
    7   → 1 digit
    100 → 3 digits
    56  → 2 digits
    999 → 3 digits

Therefore:

$$
\boxed{2}
$$

numbers have exactly two digits.

---

# 28. Range Pattern — Count K-Digit Numbers

There is also a mathematical shortcut.

For positive integers, the number of exactly $k$-digit numbers is:

$$
\boxed{9\times10^{k-1}}
$$

### Example

How many 3-digit numbers exist?

$$
9\times10^2
$$

$$
=900
$$

Therefore:

$$
\boxed{900}
$$

---

# 29. Range Pattern — Exactly 4 Digits

Number of four-digit positive integers:

$$
9\times10^3
$$

$$
=9000
$$

Therefore:

$$
\boxed{9000}
$$

They range from:

$$
1000\text{ to }9999
$$

---

# 30. Pattern Recognition — Exactly K Digits

> [!important]
> If the question asks:
>
> **"How many positive numbers have exactly K digits?"**
>
> Think:
>
> $$\boxed{9\times10^{k-1}}
> $$

Example:

For `5` digits:

$$
9\times10^4
$$

$$
=90000
$$

---

# 31. Pattern Recognition — Between Powers of 10

> [!important]
> A positive integer has exactly $k$ digits if:
>
> $$\boxed{10^{k-1}\leq N\leq10^k-1}
> $$

Examples:

### 2 Digits

$$
10\leq N\leq99
$$

### 3 Digits

$$
100\leq N\leq999
$$

### 4 Digits

$$
1000\leq N\leq9999
$$

---

# 32. Example — Is 999 a Three-Digit Number?

## Example 18

Check:

$$
10^{3-1}\leq999\leq10^3-1
$$

$$
100\leq999\leq999
$$

True.

Therefore:

$$
\boxed{999\text{ has 3 digits}}
$$

---

# 33. Example — Is 1000 a Four-Digit Number?

Check:

$$
10^3\leq1000\leq10^4-1
$$

$$
1000\leq1000\leq9999
$$

True.

Therefore:

$$
\boxed{1000\text{ has 4 digits}}
$$

---

# 34. Common Exam Pattern — Count Digits

> [!important] Must Master

### Pattern 1 — Basic Count

    while (n > 0) {
        count++;
        n /= 10;
    }

### Pattern 2 — Handle Zero

    if (n == 0) {
        return 1;
    }

### Pattern 3 — Handle Negative

    n = Math.abs(n);

### Pattern 4 — Preserve Original

Use:

    int temp = n;

### Pattern 5 — Logarithm

For positive `n`:

$$
\lfloor\log_{10}(n)\rfloor+1
$$

### Pattern 6 — Exactly K Digits

$$
9\times10^{k-1}
$$

### Pattern 7 — K-Digit Range

$$
10^{k-1}\leq N\leq10^k-1
$$

### Pattern 8 — Digit Processing

    digit = n % 10;
    n /= 10;

---

# 35. Shortcuts

> [!tip]
> **Shortcut 1 — Powers of 10**
>
> Memorize:
>
> $$10=2\text{ digits}$$
>
> $$100=3\text{ digits}$$
>
> $$1000=4\text{ digits}$$
>
> $$10000=5\text{ digits}$$
>
> $$100000=6\text{ digits}$$

> [!tip]
> **Shortcut 2 — Exactly K Digits**
>
> Number of positive $k$-digit numbers:
>
> $$\boxed{9\times10^{k-1}}
> $$

> [!tip]
> **Shortcut 3 — Range Boundaries**
>
> Exactly $k$ digits:
>
> $$\boxed{10^{k-1}\text{ to }10^k-1}
> $$

> [!tip]
> **Shortcut 4 — Digit Extraction**
>
> Remember:
>
> $$\boxed{\%10=\text{extract}}
> $$
>
> $$\boxed{/10=\text{remove}}
> $$

> [!tip]
> **Shortcut 5 — Small Values**
>
> For common powers of ten, identify the digit count immediately instead of performing repeated division.

---

# 36. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Returning 0 for Input 0

Wrong:

    while (n > 0) {
        count++;
        n /= 10;
    }

For `n = 0`, this gives:

$$
count=0
$$

Correct:

$$
\boxed{0\text{ has 1 digit}}
$$

---

### Mistake 2 — Counting the Minus Sign

For:

$$
-123
$$

the minus sign is not a digit.

Correct:

$$
\boxed{3}
$$

---

### Mistake 3 — Forgetting Integer Division

In Java:

    n /= 10;

uses integer division when `n` is an integer.

Example:

$$
123/10=12
$$

not:

$$
12.3
$$

---

### Mistake 4 — Using `% 10` to Count Digits

`% 10` extracts a digit.

It does not remove a digit.

Correct counting operation:

    n /= 10;

---

### Mistake 5 — Modifying the Original Number

If you need `n` later, do not directly destroy it.

Use:

    int temp = n;

---

### Mistake 6 — Using Logarithm Without Handling Zero

The expression:

$$
\log_{10}(0)
$$

is undefined.

Handle zero separately.

---

### Mistake 7 — Floating-Point Boundary Issues

For integer digit counting, repeated division avoids potential floating-point precision issues associated with logarithms.

---

# 37. Time and Space Complexity

Let:

$$
d=\text{number of digits}
$$

The repeated-division algorithm performs one iteration per digit.

Therefore:

$$
\boxed{O(d)}
$$

Since:

$$
d=O(\log N)
$$

we can write:

$$
\boxed{O(\log N)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 38. Arithmetic vs String vs Logarithm

| Method | Time | Space | Notes |
|---|---:|---:|---|
| Repeated Division | $O(d)$ | $O(1)$ | Best for learning digit logic |
| String Length | $O(d)$ | $O(d)$ | Very simple |
| Logarithm | $O(1)$ | $O(1)$ | Handle zero and precision carefully |

> [!tip]
> For placement coding, prioritize:
>
> **Repeated Division → String → Logarithm**

The arithmetic method teaches the reusable digit-processing pattern.

---

# 39. Advanced Example — Very Large Number as String

If the number is too large for `int` or `long`, arithmetic division may not be possible directly.

Example:

    987654321098765432109876543210

If the input is stored as a `String`, the digit count is simply:

    int count = s.length();

Therefore:

$$
\boxed{\text{digit count}=\text{string length}}
$$

> [!important]
> This approach is necessary when the number is larger than the available integer data type.

---

# 40. Example — Huge Number

## Example 19

### Question

Count digits in:

    123456789012345678901234567890

Since it is stored as a string:

    String s = "123456789012345678901234567890";

    int count = s.length();

The number contains:

$$
30
$$

digits.

Therefore:

$$
\boxed{30}
$$

---

# 41. Example — Leading Zeros

Consider the string:

    "001234"

Its length is:

$$
6
$$

But as an integer:

$$
1234
$$

has:

$$
4
$$

digits.

> [!important]
> Leading zeros are not part of the normal integer representation.
>
> If the input is a **string**, leading zeros count toward the string length.
>
> If the input is an **integer**, leading zeros are lost.

---

# 42. Example — Number of Digits After Removing Leading Zeros

## Example 20

### Question

How many digits does `"000123"` represent as an integer?

Remove leading zeros:

    000123 → 123

Therefore:

$$
\boxed{3}
$$

But the raw string length is:

$$
6
$$

So always identify whether the question refers to:

- String length
- Integer digit count

---

# 43. Example — Count Digits and Sum Digits

## Example 21

### Question

For `9876`, find both the number of digits and the sum of digits.

Digit count:

$$
9876\rightarrow987\rightarrow98\rightarrow9\rightarrow0
$$

Therefore:

$$
count=4
$$

Digit sum:

$$
9+8+7+6=30
$$

### Answer

$$
\boxed{\text{Digits}=4,\quad\text{Sum}=30}
$$

---

# 44. Example — Count Even and Odd Digits

## Example 22

### Question

For `123456`, count the even and odd digits.

Digits:

$$
1,2,3,4,5,6
$$

Odd digits:

$$
1,3,5
$$

Count:

$$
3
$$

Even digits:

$$
2,4,6
$$

Count:

$$
3
$$

### Answer

$$
\boxed{\text{Even}=3,\quad\text{Odd}=3}
$$

This uses the same digit extraction pattern.

---

# 45. Example — Count a Particular Digit

## Example 23

### Question

How many times does digit `2` occur in `1223242`?

Extract digits:

    1
    2
    2
    3
    2
    4
    2

Digit `2` occurs:

$$
4
$$

times.

### Answer

$$
\boxed{4}
$$

The main pattern is still:

    digit = n % 10;
    n /= 10;

---

# 46. Recognition Checklist

> [!important] Must Recognize Quickly

**"How many digits?"**

Think:

$$
\boxed{\text{Repeated division by }10}
$$

---

**"Extract each digit."**

Think:

$$
\boxed{n\%10}
$$

---

**"Remove the last digit."**

Think:

$$
\boxed{n/10}
$$

---

**"Exactly K digits."**

Think:

$$
\boxed{10^{k-1}\leq N\leq10^k-1}
$$

---

**"How many K-digit positive numbers?"**

Think:

$$
\boxed{9\times10^{k-1}}
$$

---

**"Huge number beyond long."**

Think:

$$
\boxed{\text{String length}}
$$

---

**"Zero input."**

Think:

$$
\boxed{0\text{ has 1 digit}}
$$

---

**"Negative input."**

Think:

$$
\boxed{\text{Ignore the sign}}
$$

---

# 47. Formula Sheet

## Number of Digits

For $N>0$:

$$
\boxed{
\lfloor\log_{10}(N)\rfloor+1
}
$$

## Exactly K Digits

$$
\boxed{
10^{k-1}\leq N\leq10^k-1
}
$$

## Count of Positive K-Digit Numbers

$$
\boxed{
9\times10^{k-1}
}
$$

## Extract Last Digit

$$
\boxed{
digit=N\%10
}
$$

## Remove Last Digit

$$
\boxed{
N=\lfloor N/10\rfloor
}
$$

## Zero

$$
\boxed{
\text{digits}(0)=1
}
$$

## Negative Number

$$
\boxed{
\text{digits}(N)=\text{digits}(|N|)
}
$$

for $N\neq0$.

## Complexity

$$
\boxed{O(\log N)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 48. Quick Revision

> [!summary] One-Minute Revision

    Count Digits
    → Find how many digits are in a number.

    Main coding pattern
    → count = 0
    → while n > 0
    → count++
    → n /= 10

    % 10
    → Extract last digit.

    / 10
    → Remove last digit.

    0
    → Has 1 digit.

    Negative number
    → Ignore the minus sign.

    Positive N
    → digits = floor(log₁₀(N)) + 1.

    Exactly K digits
    → 10^(K-1) to 10^K - 1.

    Number of positive K-digit numbers
    → 9 × 10^(K-1).

    Huge number
    → Store as String and use length.

    Preserve original
    → Use a temporary variable.

    Common digit-processing problems
    → Sum digits.
    → Reverse number.
    → Palindrome.
    → Armstrong.
    → Strong.
    → Digit frequency.

    Complexity
    → O(log N).

    Space
    → O(1).

---

## Golden Memory Trick

**To count digits, keep dividing by 10 and count how many times the number survives before becoming 0.**

## One-Line Recognition

**When a problem asks "how many digits," immediately think repeated `/10`; when it asks to process each digit, think `%10` + `/10`.**