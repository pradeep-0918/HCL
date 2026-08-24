---
type: concept
subject: coding
topic: "Reverse Number"
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
  - reverse-number
  - java
  - number-basics
wikilinks:
  - "[[Digit Problems]]"
  - "[[Number Basics]]"
  - "[[Count Digits]]"
  - "[[Sum of Digits]]"
  - "[[Palindrome Number]]"
---

# Reverse Number

## 1. Core Concept

> [!summary]
> **Reverse Number** means rearranging the digits of a number in the opposite order.
>
> Example:
>
> $$12345\rightarrow54321$$
>
> The main coding pattern is:
>
> **Extract the last digit using `% 10` → append it to the reversed number → remove the last digit using `/ 10` → repeat.**

The key formula is:

$$
\boxed{reverse=reverse\times10+digit}
$$

where:

$$
digit=n\%10
$$

and:

$$
n=n/10
$$

---

# 2. Basic Meaning

Consider:

$$
1234
$$

The digits are:

$$
1,2,3,4
$$

Reversing them gives:

$$
4,3,2,1
$$

Therefore:

$$
\boxed{1234\rightarrow4321}
$$

The number is processed from **right to left** because `% 10` always gives the last digit.

---

# 3. Main Formula

For every iteration:

### Step 1 — Extract Last Digit

$$
\boxed{digit=n\%10}
$$

### Step 2 — Add Digit to Reverse

$$
\boxed{reverse=reverse\times10+digit}
$$

### Step 3 — Remove Last Digit

$$
\boxed{n=n/10}
$$

Repeat until:

$$
n=0
$$

---

# 4. Important Properties

## Property 1 — `% 10` Gives the Last Digit

For:

$$
1234
$$

we get:

$$
1234\%10=4
$$

Therefore:

$$
\boxed{4}
$$

is extracted first.

---

## Property 2 — `/ 10` Removes the Last Digit

For integer division:

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

---

## Property 3 — Reverse Is Built From Right to Left

For:

$$
123
$$

first digit extracted:

$$
3
$$

then:

$$
2
$$

then:

$$
1
$$

So the reverse becomes:

$$
321
$$

---

## Property 4 — Leading Zeros Disappear

Consider:

$$
1200
$$

Reverse digits:

$$
0021
$$

But as an integer:

$$
0021=21
$$

Therefore:

$$
\boxed{1200\rightarrow21}
$$

> [!important]
> Integer reversal does not preserve leading zeros.

---

## Property 5 — A Single-Digit Number Remains the Same

For:

$$
7
$$

the reverse is:

$$
7
$$

Therefore:

$$
\boxed{reverse(7)=7}
$$

---

# 5. Basic Example — 123

## Example 1

### Question

Reverse `123`.

### Step 1

Initial:

$$
reverse=0
$$

Extract:

$$
123\%10=3
$$

Build:

$$
reverse=0\times10+3=3
$$

Remove:

$$
123/10=12
$$

### Step 2

Extract:

$$
12\%10=2
$$

Build:

$$
reverse=3\times10+2
$$

$$
=32
$$

Remove:

$$
12/10=1
$$

### Step 3

Extract:

$$
1\%10=1
$$

Build:

$$
reverse=32\times10+1
$$

$$
=321
$$

Remove:

$$
1/10=0
$$

Therefore:

$$
\boxed{321}
$$

---

# 6. Basic Example — 4567

## Example 2

### Question

Reverse `4567`.

| Step | $n$ | Digit | Reverse |
|---:|---:|---:|---:|
| 1 | 4567 | 7 | 7 |
| 2 | 456 | 6 | 76 |
| 3 | 45 | 5 | 765 |
| 4 | 4 | 4 | 7654 |

Therefore:

$$
\boxed{4567\rightarrow7654}
$$

---

# 7. Basic Example — 1000

## Example 3

### Question

Reverse `1000`.

Extract digits:

$$
0,0,0,1
$$

Build reverse:

$$
0001
$$

As an integer:

$$
1
$$

Therefore:

$$
\boxed{1000\rightarrow1}
$$

---

# 8. Basic Example — 120

## Example 4

### Question

Reverse `120`.

$$
120\rightarrow12\rightarrow1\rightarrow0
$$

Extracted digits:

$$
0,2,1
$$

Reverse:

$$
021
$$

As an integer:

$$
21
$$

Therefore:

$$
\boxed{120\rightarrow21}
$$

---

# 9. Basic Example — Single Digit

## Example 5

### Question

Reverse `8`.

There is only one digit:

$$
8
$$

Therefore:

$$
\boxed{8}
$$

---

# 10. Standard Java Program

## Example 6

### Question

Write a Java program to reverse an integer.

### Code

    import java.util.Scanner;

    class Main {

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            int reverse = 0;

            while (n != 0) {

                int digit = n % 10;

                reverse = reverse * 10 + digit;

                n /= 10;
            }

            System.out.println(reverse);
        }
    }

### Main Pattern

    digit = n % 10;
    reverse = reverse * 10 + digit;
    n /= 10;

This pattern is extremely important for number-based coding problems.

---

# 11. Reusable Function

## Example 7

### Code

    static int reverseNumber(int n) {

        int reverse = 0;

        while (n != 0) {

            int digit = n % 10;

            reverse = reverse * 10 + digit;

            n /= 10;
        }

        return reverse;
    }

For:

    reverseNumber(12345)

the result is:

$$
\boxed{54321}
$$

---

# 12. Pattern Recognition — Reverse Number

> [!important]
> **If the question says "reverse the digits of a number":**
>
> Immediately think:
>
>     digit = n % 10;
>     reverse = reverse * 10 + digit;
>     n /= 10;
>
> The most important formula is:
>
> $$\boxed{reverse=reverse\times10+digit}
> $$

---

# 13. Why Multiply Reverse by 10?

Suppose:

$$
reverse=32
$$

and the next digit is:

$$
1
$$

We need:

$$
321
$$

Multiplying by `10` shifts the existing digits left:

$$
32\times10=320
$$

Then add the new digit:

$$
320+1=321
$$

Therefore:

$$
\boxed{reverse\times10+digit}
$$

appends the digit to the right.

---

# 14. Visual Understanding

Suppose:

$$
n=1234
$$

### First Digit

$$
4
$$

Reverse:

$$
4
$$

### Second Digit

$$
3
$$

Build:

$$
4\times10+3=43
$$

### Third Digit

$$
2
$$

Build:

$$
43\times10+2=432
$$

### Fourth Digit

$$
1
$$

Build:

$$
432\times10+1=4321
$$

Final:

$$
\boxed{4321}
$$

---

# 15. Digit Processing Master Pattern

The general number-processing structure is:

    while (n > 0) {

        int digit = n % 10;

        // Process digit

        n /= 10;
    }

For reverse:

    reverse = reverse * 10 + digit;

For sum:

    sum += digit;

For frequency:

    freq[digit]++;

For product:

    product *= digit;

> [!tip]
> Once you understand this pattern, many beginner number problems become variations of the same loop.

---

# 16. Reverse Number vs Sum of Digits

| Problem | Main Operation |
|---|---|
| Count Digits | `count++` |
| Sum Digits | `sum += digit` |
| Reverse Number | `reverse = reverse * 10 + digit` |
| Digit Frequency | `freq[digit]++` |
| Product of Digits | `product *= digit` |

The digit extraction is the same:

$$
\boxed{digit=n\%10}
$$

The processing operation changes.

---

# 17. Example — Reverse 9876

## Example 8

### Question

Reverse `9876`.

Step 1:

$$
digit=6
$$

$$
reverse=6
$$

Step 2:

$$
digit=7
$$

$$
reverse=6\times10+7=67
$$

Step 3:

$$
digit=8
$$

$$
reverse=67\times10+8=678
$$

Step 4:

$$
digit=9
$$

$$
reverse=678\times10+9=6789
$$

Therefore:

$$
\boxed{9876\rightarrow6789}
$$

---

# 18. Example — Reverse 54321

## Example 9

### Question

Reverse `54321`.

The digits are processed:

$$
1\rightarrow2\rightarrow3\rightarrow4\rightarrow5
$$

Build:

$$
1
$$

$$
12
$$

$$
123
$$

$$
1234
$$

$$
12345
$$

Therefore:

$$
\boxed{54321\rightarrow12345}
$$

---

# 19. Example — Reverse 1001

## Example 10

### Question

Reverse `1001`.

Digits extracted:

$$
1,0,0,1
$$

Build:

$$
1
$$

$$
10
$$

$$
100
$$

$$
1001
$$

Therefore:

$$
\boxed{1001\rightarrow1001}
$$

This is a palindrome.

---

# 20. Reverse Number and Palindrome

A number is a palindrome if:

$$
\boxed{N=reverse(N)}
$$

Example:

$$
121
$$

Reverse:

$$
121
$$

Therefore:

$$
\boxed{121\text{ is a Palindrome}}
$$

Example:

$$
123
$$

Reverse:

$$
321
$$

Since:

$$
123\neq321
$$

therefore:

$$
\boxed{123\text{ is Not a Palindrome}}
$$

> [!important]
> **Reverse Number is the core operation used to solve Palindrome Number problems.**

---

# 21. Standard Palindrome Pattern

## Example 11

### Question

Check whether `121` is a palindrome.

### Step 1

Store original:

    original = 121

### Step 2

Reverse:

$$
121\rightarrow121
$$

### Step 3

Compare:

$$
original=reverse
$$

Therefore:

$$
121=121
$$

### Answer

$$
\boxed{121\text{ is a Palindrome}}
$$

---

# 22. Preserving the Original Number

A common mistake is modifying `n` while reversing it.

Suppose:

    int n = 12321;

After the loop:

    n = 0;

If you need to compare the original number later, store:

    int original = n;

Then:

    int reverse = 0;

This gives:

    original = 12321
    n = 0
    reverse = 12321

Therefore:

$$
\boxed{original=reverse}
$$

---

# 23. Example — Palindrome Using Reverse

## Example 12

### Code

    static boolean isPalindrome(int n) {

        int original = n;

        int reverse = 0;

        while (n != 0) {

            int digit = n % 10;

            reverse = reverse * 10 + digit;

            n /= 10;
        }

        return original == reverse;
    }

For:

    isPalindrome(1221)

result:

$$
\boxed{true}
$$

---

# 24. Negative Numbers

Consider:

$$
-123
$$

Depending on the problem definition, the minus sign may make the number non-palindromic.

For ordinary integer reversal:

$$
-123\rightarrow-321
$$

For many coding problems, negative values are handled separately.

> [!warning]
> Do not blindly use `Math.abs()` unless the problem allows or expects the sign to be ignored.

---

# 25. Overflow Problem

Suppose an integer is reversed.

The expression:

$$
reverse\times10+digit
$$

can exceed the range of `int`.

Java `int` range:

$$
-2^{31}\text{ to }2^{31}-1
$$

Therefore, for potentially large values, use `long`.

Example:

    long reverse = 0;

    while (n != 0) {

        long digit = n % 10;

        reverse = reverse * 10 + digit;

        n /= 10;
    }

> [!important]
> In coding platforms, always check the constraints before choosing `int` or `long`.

---

# 26. Overflow-Safe Reverse

For an `int`, an overflow-safe solution can check before multiplying.

### Code

    static int reverseNumber(int x) {

        int reverse = 0;

        while (x != 0) {

            int digit = x % 10;

            if (reverse > Integer.MAX_VALUE / 10 ||
                (reverse == Integer.MAX_VALUE / 10 && digit > 7)) {
                return 0;
            }

            if (reverse < Integer.MIN_VALUE / 10 ||
                (reverse == Integer.MIN_VALUE / 10 && digit < -8)) {
                return 0;
            }

            reverse = reverse * 10 + digit;

            x /= 10;
        }

        return reverse;
    }

This is useful for problems where the reversed result must remain inside the 32-bit signed integer range.

---

# 27. Example — Overflow Concept

Suppose:

$$
reverse=214748364
$$

Multiplying by `10` gives:

$$
2147483640
$$

Adding another digit may exceed:

$$
2147483647
$$

Therefore, blindly calculating:

$$
reverse\times10+digit
$$

can overflow an `int`.

> [!warning]
> Overflow is an important edge case in reverse-number problems.

---

# 28. Shortcut — Palindrome Recognition

> [!tip]
> If the question asks:
>
> **"Is the number the same when reversed?"**
>
> Think:
>
> $$\boxed{reverse(N)=N}
> $$
>
> Use the reverse-number algorithm first, then compare.

---

# 29. Shortcut — Last Digit

> [!tip]
> The last digit is always:
>
> $$\boxed{N\%10}
> $$
>
> This is useful when manually checking a reverse operation.

---

# 30. Shortcut — Remove Last Digit

> [!tip]
> Integer division by `10` removes the last digit:
>
> $$\boxed{N/10}
> $$
>
> Example:
>
> $$4567/10=456$$

---

# 31. Shortcut — Build a Number

> [!tip]
> Whenever you need to construct a number digit by digit:
>
> $$\boxed{result=result\times10+digit}
> $$
>
> This pattern appears in:
>
> - Reverse Number
> - Constructing numbers from digits
> - String-to-number conversion
> - Some parsing problems

---

# 32. Common Exam Pattern — Reverse Number

> [!important] Must Master

### Pattern 1 — Basic Reverse

    digit = n % 10;
    reverse = reverse * 10 + digit;
    n /= 10;

### Pattern 2 — Reverse and Compare

Used for:

$$
\boxed{\text{Palindrome}}
$$

### Pattern 3 — Reverse With Temporary Variable

Use:

    int temp = n;

when the original number is needed later.

### Pattern 4 — Reverse Negative Numbers

Understand how the problem expects the sign to be handled.

### Pattern 5 — Reverse With Overflow Check

Use boundary checks when the result must fit inside `int`.

### Pattern 6 — Reverse a Large Number

Use `long` or `String` depending on constraints.

### Pattern 7 — Reverse Number in an Array

Apply the same reverse function to each element.

---

# 33. Example — Reverse Every Number in an Array

## Example 13

### Question

Reverse every number in:

    [12, 345, 100, 789]

Calculations:

$$
12\rightarrow21
$$

$$
345\rightarrow543
$$

$$
100\rightarrow1
$$

$$
789\rightarrow987
$$

Therefore:

$$
\boxed{[21,543,1,987]}
$$

---

# 34. Example — Find Palindromes in an Array

## Example 14

### Question

Find palindrome numbers in:

    [121, 123, 454, 678, 1001]

Check:

$$
121\rightarrow121
$$

Palindrome.

$$
123\rightarrow321
$$

Not palindrome.

$$
454\rightarrow454
$$

Palindrome.

$$
678\rightarrow876
$$

Not palindrome.

$$
1001\rightarrow1001
$$

Palindrome.

Therefore:

$$
\boxed{121,454,1001}
$$

---

# 35. Example — Count Palindromes in an Array

## Example 15

From:

    [121, 123, 454, 678, 1001]

Palindrome numbers are:

$$
121,454,1001
$$

Count:

$$
\boxed{3}
$$

---

# 36. Example — Reverse and Add

## Example 16

### Question

Reverse `123` and add it to the original number.

Original:

$$
123
$$

Reverse:

$$
321
$$

Sum:

$$
123+321=444
$$

Therefore:

$$
\boxed{444}
$$

---

# 37. Example — Reverse Until Palindrome

## Example 17

### Question

Start with `12`, reverse it, and add it to the original.

First:

$$
12+21=33
$$

`33` is a palindrome.

Therefore:

$$
\boxed{33}
$$

This type of problem combines:

- Reverse Number
- Addition
- Palindrome checking

---

# 38. Example — Reverse 1200

## Example 18

### Question

Reverse `1200`.

Extract:

$$
0
$$

Then:

$$
0
$$

Then:

$$
2
$$

Then:

$$
1
$$

Build:

$$
0\rightarrow0\rightarrow2\rightarrow21
$$

Therefore:

$$
\boxed{21}
$$

> [!important]
> The leading zeros generated during reversal are not represented in an integer.

---

# 39. Reverse Number Using String

## Example 19

Java provides a simpler string-based approach.

### Code

    String s = "12345";

    String reversed = new StringBuilder(s)
            .reverse()
            .toString();

    System.out.println(reversed);

Result:

    54321

> [!tip]
> This is convenient when the input is already a string or may contain a very large number.
>
> For number-logic questions, prefer the arithmetic method.

---

# 40. Large Number Reversal

If the number is too large for `long`, use a string.

Example:

    String s = "123456789012345678901234567890";

Reverse:

    String reversed = new StringBuilder(s)
            .reverse()
            .toString();

Result:

    098765432109876543210987654321

Notice that because this is a string, the leading zero is preserved.

Therefore:

> [!important]
> Arithmetic integer reversal and string reversal can produce different representations when zeros are involved.

---

# 41. Arithmetic Reverse vs String Reverse

| Situation | Recommended Method |
|---|---|
| Normal integer | Arithmetic |
| Learn digit manipulation | Arithmetic |
| Palindrome integer | Arithmetic |
| Very large number | String |
| Need to preserve leading zeros | String |
| Input already a string | String |
| Overflow-sensitive integer problem | Arithmetic with checks |

---

# 42. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting `reverse * 10`

Wrong:

    reverse += digit;

Correct:

    reverse = reverse * 10 + digit;

Why?

Because multiplication by `10` shifts existing digits left.

---

### Mistake 2 — Using `/ 10` to Extract the Digit

Wrong:

    digit = n / 10;

Correct:

    digit = n % 10;

---

### Mistake 3 — Forgetting `/ 10`

If you do not remove the last digit:

    n /= 10;

the loop may never terminate.

---

### Mistake 4 — Destroying the Original Number

For palindrome checking, store:

    int original = n;

before modifying `n`.

---

### Mistake 5 — Ignoring Overflow

The expression:

    reverse * 10 + digit

may exceed the range of `int`.

Check constraints.

---

### Mistake 6 — Expecting Leading Zeros

For:

$$
1200
$$

the mathematical digit reversal is:

$$
0021
$$

but integer output is:

$$
21
$$

---

### Mistake 7 — Incorrect Negative Handling

Do not automatically assume:

$$
-123\rightarrow321
$$

The actual result depends on whether the sign is preserved.

In standard integer arithmetic:

$$
-123\rightarrow-321
$$

---

# 43. Time and Space Complexity

Let:

$$
d=\text{number of digits}
$$

Each digit is processed exactly once.

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

Extra space:

$$
\boxed{O(1)}
$$

for arithmetic reversal.

---

# 44. Reverse Number Pattern in One Line

The entire algorithm can be remembered as:

$$
\boxed{
digit=n\%10,\quad
reverse=reverse\times10+digit,\quad
n=n/10
}
$$

This is one of the most important formulas in beginner number programming.

---

# 45. Recognition Checklist

> [!important] Must Recognize Quickly

**"Reverse the number."**

Think:

$$
\boxed{digit=n\%10}
$$

then:

$$
\boxed{reverse=reverse\times10+digit}
$$

then:

$$
\boxed{n=n/10}
$$

---

**"Same after reversing."**

Think:

$$
\boxed{\text{Palindrome}}
$$

---

**"Extract the last digit."**

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

**"Build a number from digits."**

Think:

$$
\boxed{result=result\times10+digit}
$$

---

**"Very large number."**

Think:

$$
\boxed{\text{String}}
$$

---

**"Result may exceed int."**

Think:

$$
\boxed{\text{Overflow check or long}}
$$

---

**"Leading zeros matter."**

Think:

$$
\boxed{\text{String representation}}
$$

---

# 46. Formula Sheet

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

## Build Reverse

$$
\boxed{
reverse=reverse\times10+digit
}
$$

## Palindrome Condition

$$
\boxed{
N=reverse(N)
}
$$

## Digit Processing Complexity

$$
\boxed{
O(d)=O(\log N)
}
$$

## Extra Space

$$
\boxed{
O(1)
}
$$

## K-Digit Range

$$
\boxed{
10^{k-1}\leq N\leq10^k-1
}
$$

---

# 47. Quick Revision

> [!summary] One-Minute Revision

    Reverse Number
    → Rearrange digits in reverse order.

    Main pattern
    → digit = n % 10
    → reverse = reverse * 10 + digit
    → n /= 10

    % 10
    → Extract last digit.

    / 10
    → Remove last digit.

    Why reverse * 10?
    → Shift existing digits left before adding
      the new digit.

    Example
    → 123 → 321.

    1200
    → 21 as an integer because leading zeros disappear.

    Palindrome
    → original == reverse.

    Preserve original
    → int original = n.

    Overflow
    → reverse * 10 + digit may exceed int.

    Very large number
    → Use String.

    Preserve leading zeros
    → Use String.

    Core related problems
    → Count Digits.
    → Sum of Digits.
    → Palindrome.
    → Digit Frequency.
    → Number Formation.

    Complexity
    → O(log N).

    Space
    → O(1).

---

## Golden Memory Trick

**Take the last digit with `%10`, append it using `reverse × 10 + digit`, remove it with `/10`, and repeat.**

## One-Line Recognition

**When a problem asks to reverse digits, immediately think `%10 → reverse×10+digit → /10`.**