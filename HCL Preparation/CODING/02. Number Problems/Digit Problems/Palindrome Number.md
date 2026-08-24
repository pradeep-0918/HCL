---
type: concept
subject: coding
topic: "Palindrome Number"
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
  - palindrome-number
  - java
  - number-basics
wikilinks:
  - "[[Digit Problems]]"
  - "[[Number Basics]]"
  - "[[Reverse Number]]"
  - "[[Count Digits]]"
  - "[[Sum of Digits]]"
---

# Palindrome Number

## 1. Core Concept

> [!summary]
> A **Palindrome Number** is a number that remains the same when its digits are reversed.
>
> Example:
>
> $$121\rightarrow121$$
>
> Therefore:
>
> $$\boxed{121\text{ is a Palindrome Number}}
> $$
>
> Non-example:
>
> $$123\rightarrow321$$
>
> Since:
>
> $$123\neq321$$
>
> $$\boxed{123\text{ is Not a Palindrome Number}}
> $$

The key idea is:

**Reverse the number and compare the reversed number with the original number.**

---

# 2. Basic Meaning

A number $N$ is a palindrome if:

$$
\boxed{N=Reverse(N)}
$$

Examples:

| Number | Reverse | Palindrome |
|---:|---:|---|
| 121 | 121 | Yes |
| 1331 | 1331 | Yes |
| 123 | 321 | No |
| 1234 | 4321 | No |
| 1001 | 1001 | Yes |
| 10 | 1 | No |

The most important prerequisite is the **Reverse Number** pattern.

---

# 3. Main Formula

First extract the last digit:

$$
\boxed{digit=N\%10}
$$

Build the reverse:

$$
\boxed{reverse=reverse\times10+digit}
$$

Remove the last digit:

$$
\boxed{N=\lfloor N/10\rfloor}
$$

After processing all digits:

$$
\boxed{\text{Palindrome if }original=reverse}
$$

---

# 4. Important Properties

## Property 1 — Same Forward and Backward

A palindrome reads the same in both directions.

Example:

$$
121
$$

Forward:

$$
1\rightarrow2\rightarrow1
$$

Backward:

$$
1\rightarrow2\rightarrow1
$$

Therefore:

$$
\boxed{121\text{ is Palindrome}}
$$

---

## Property 2 — Single-Digit Numbers

Every single-digit number is a palindrome.

For example:

$$
0,1,2,3,\ldots,9
$$

because reversing one digit gives the same digit.

Therefore:

$$
\boxed{\text{Every single-digit number is Palindromic}}
$$

---

## Property 3 — Trailing Zeros Matter

Consider:

$$
120
$$

Reverse:

$$
21
$$

Since:

$$
120\neq21
$$

it is not a palindrome.

Therefore:

$$
\boxed{120\text{ is Not Palindrome}}
$$

---

## Property 4 — Leading Zeros Are Not Preserved in Integers

Consider:

$$
100
$$

Its digit reversal would conceptually be:

$$
001
$$

But as an integer:

$$
001=1
$$

Therefore:

$$
100\neq1
$$

So:

$$
\boxed{100\text{ is Not Palindrome}}
$$

---

## Property 5 — Symmetry

A palindrome has symmetrical digits.

Example:

$$
12321
$$

Positions:

$$
1=1
$$

$$
2=2
$$

The middle digit:

$$
3
$$

is automatically symmetric.

Therefore:

$$
\boxed{12321\text{ is Palindrome}}
$$

---

# 5. Basic Example — 121

## Example 1

### Question

Check whether `121` is a palindrome.

### Step 1

Original:

$$
121
$$

Extract `1`:

$$
121\%10=1
$$

Reverse:

$$
0\times10+1=1
$$

Remaining:

$$
121/10=12
$$

### Step 2

Extract:

$$
12\%10=2
$$

Reverse:

$$
1\times10+2=12
$$

Remaining:

$$
12/10=1
$$

### Step 3

Extract:

$$
1\%10=1
$$

Reverse:

$$
12\times10+1=121
$$

Remaining:

$$
1/10=0
$$

Compare:

$$
original=121
$$

$$
reverse=121
$$

Therefore:

$$
\boxed{121\text{ is a Palindrome Number}}
$$

---

# 6. Basic Example — 123

## Example 2

### Question

Check whether `123` is a palindrome.

Reverse:

$$
123\rightarrow321
$$

Compare:

$$
123\neq321
$$

Therefore:

$$
\boxed{123\text{ is Not a Palindrome}}
$$

---

# 7. Basic Example — 1331

## Example 3

### Question

Check whether `1331` is a palindrome.

Reverse:

$$
1331\rightarrow1331
$$

Therefore:

$$
\boxed{1331\text{ is a Palindrome}}
$$

---

# 8. Basic Example — 12321

## Example 4

### Question

Check whether `12321` is a palindrome.

Reverse:

$$
12321\rightarrow12321
$$

Therefore:

$$
\boxed{12321\text{ is a Palindrome}}
$$

---

# 9. Basic Example — 1001

## Example 5

### Question

Check whether `1001` is a palindrome.

Reverse:

$$
1001\rightarrow1001
$$

Therefore:

$$
\boxed{1001\text{ is a Palindrome}}
$$

---

# 10. Basic Example — 10

## Example 6

### Question

Check whether `10` is a palindrome.

Reverse:

$$
10\rightarrow1
$$

Compare:

$$
10\neq1
$$

Therefore:

$$
\boxed{10\text{ is Not a Palindrome}}
$$

---

# 11. Standard Java Program

## Example 7

### Question

Write a Java program to check whether a number is a palindrome.

### Code

    import java.util.Scanner;

    class Main {

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            int original = n;
            int reverse = 0;

            while (n != 0) {

                int digit = n % 10;

                reverse = reverse * 10 + digit;

                n /= 10;
            }

            if (original == reverse) {
                System.out.println("Palindrome");
            } else {
                System.out.println("Not Palindrome");
            }
        }
    }

### Main Pattern

    original = n;

    while (n != 0) {

        digit = n % 10;

        reverse = reverse * 10 + digit;

        n /= 10;
    }

    original == reverse

---

# 12. Reusable Function

## Example 8

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

    isPalindrome(12321)

result:

$$
\boxed{true}
$$

For:

    isPalindrome(12345)

result:

$$
\boxed{false}
$$

---

# 13. Pattern Recognition — Palindrome Number

> [!important]
> **If the question says "check whether a number reads the same backward":**
>
> Immediately think:
>
> $$\boxed{\text{Reverse + Compare}}
> $$
>
> The pattern is:
>
>     original = n;
>     reverse = 0;
>
>     while (n != 0) {
>         digit = n % 10;
>         reverse = reverse * 10 + digit;
>         n /= 10;
>     }
>
>     original == reverse

---

# 14. Pattern Recognition — Reverse-Based Problems

> [!important]
> If the question involves:
>
> - Same forward and backward
> - Reads the same from both directions
> - Reverse equals original
> - Symmetric digits
>
> Think:
>
> $$\boxed{\text{Palindrome}}
> $$
>
> Then use:
>
> $$\boxed{Reverse(N)=N}
> $$

---

# 15. Why Store the Original Number?

Suppose:

    int n = 121;

After reversing:

    n = 0;

Therefore, if you want to compare the original number, you must save it first:

    int original = n;

Then:

    original = 121
    reverse = 121
    n = 0

Comparison:

$$
original==reverse
$$

Therefore:

$$
\boxed{\text{Palindrome}}
$$

> [!warning]
> A common mistake is trying to compare `n` with `reverse` after the loop because `n` has already become `0`.

---

# 16. Example — Full Trace

## Example 9

### Question

Check whether `1221` is a palindrome.

| Step | $n$ | Digit | Reverse |
|---:|---:|---:|---:|
| 1 | 1221 | 1 | 1 |
| 2 | 122 | 2 | 12 |
| 3 | 12 | 2 | 122 |
| 4 | 1 | 1 | 1221 |

Original:

$$
1221
$$

Reverse:

$$
1221
$$

Therefore:

$$
\boxed{\text{Palindrome}}
$$

---

# 17. Example — Full Trace

## Example 10

### Question

Check whether `1234` is a palindrome.

| Step | $n$ | Digit | Reverse |
|---:|---:|---:|---:|
| 1 | 1234 | 4 | 4 |
| 2 | 123 | 3 | 43 |
| 3 | 12 | 2 | 432 |
| 4 | 1 | 1 | 4321 |

Compare:

$$
1234\neq4321
$$

Therefore:

$$
\boxed{\text{Not Palindrome}}
$$

---

# 18. Palindrome vs Reverse Number

These concepts are closely related but not identical.

| Topic | Goal |
|---|---|
| Reverse Number | Find the reversed number |
| Palindrome Number | Check whether original equals reversed number |

Example:

$$
123
$$

Reverse:

$$
321
$$

So:

$$
\boxed{Reverse=321}
$$

But:

$$
123\neq321
$$

Therefore:

$$
\boxed{\text{Not Palindrome}}
$$

---

# 19. Palindrome vs String Palindrome

A number can be checked using arithmetic.

A string can be checked using characters.

### Number

    121

Use:

    digit = n % 10;

### String

    "121"

Use:

    s.charAt(i)

Both represent the same basic concept:

$$
\boxed{\text{Read the same forward and backward}}
$$

---

# 20. String-Based Palindrome

## Example 11

### Code

    static boolean isPalindrome(String s) {

        int left = 0;
        int right = s.length() - 1;

        while (left < right) {

            if (s.charAt(left) != s.charAt(right)) {
                return false;
            }

            left++;
            right--;
        }

        return true;
    }

For:

    "racecar"

result:

$$
\boxed{true}
$$

For:

    "hello"

result:

$$
\boxed{false}
$$

> [!important]
> String palindrome naturally leads to the **Two Pointers** pattern.

---

# 21. Number Palindrome vs Two Pointers

There are two common approaches.

### Approach 1 — Number + Reverse

$$
\boxed{Reverse(N)=N}
$$

Good for integer-based problems.

### Approach 2 — Convert to String + Two Pointers

Compare:

$$
s[left]
$$

with:

$$
s[right]
$$

Then move inward.

Good when the input is a string or when string processing is allowed.

---

# 22. Example — Two Pointer Palindrome

## Example 12

### Question

Check `"1221"` using two pointers.

Initial:

$$
left=0
$$

$$
right=3
$$

Compare:

$$
s[0]=1
$$

and:

$$
s[3]=1
$$

Match.

Move:

$$
left=1,\quad right=2
$$

Compare:

$$
s[1]=2
$$

and:

$$
s[2]=2
$$

Match.

Now:

$$
left\geq right
$$

Therefore:

$$
\boxed{\text{Palindrome}}
$$

---

# 23. Example — Two Pointer Failure

## Example 13

### Question

Check `"1234"`.

Compare:

$$
s[0]=1
$$

and:

$$
s[3]=4
$$

They are different.

Therefore, we can immediately return:

$$
\boxed{\text{Not Palindrome}}
$$

> [!tip]
> In a two-pointer solution, the first mismatch is enough to conclude that the string is not a palindrome.

---

# 24. Shortcut — Half Comparison

A palindrome is symmetric.

For a string, you only need to compare the first half with the second half.

Example:

$$
12321
$$

Compare:

$$
1=1
$$

$$
2=2
$$

The middle digit does not need comparison.

> [!tip]
> This is why the two-pointer solution takes only about half as many comparisons.

---

# 25. Even-Length Palindrome

Example:

$$
1221
$$

There is no single middle digit.

Pairs:

$$
1=1
$$

$$
2=2
$$

Therefore:

$$
\boxed{\text{Palindrome}}
$$

---

# 26. Odd-Length Palindrome

Example:

$$
12321
$$

Pairs:

$$
1=1
$$

$$
2=2
$$

The middle:

$$
3
$$

does not need to match anything.

Therefore:

$$
\boxed{\text{Palindrome}}
$$

---

# 27. Pattern Recognition — Odd and Even Length

> [!important]
> A palindrome can have:
>
> **Odd number of digits**
>
> Example:
>
> $$12321
> $$
>
> or
>
> **Even number of digits**
>
> Example:
>
> $$1221
> $$
>
> The important property is symmetry, not length parity.

---

# 28. Negative Numbers

Consider:

$$
-121
$$

The handling depends on the problem definition.

If the sign is considered part of the number representation:

$$
-121\rightarrow-121
$$

could be treated as a palindrome under a representation-based definition.

However, many programming problems define negative integers as **not palindrome** because the negative sign appears only on the left.

For standard interview-style integer palindrome problems:

$$
\boxed{\text{Negative numbers are generally treated as Not Palindrome}}
$$

> [!warning]
> Always follow the exact problem statement.

---

# 29. Example — Negative Number

## Example 14

### Question

Check whether `-121` is a palindrome under the standard integer interpretation.

The sign is not symmetric.

Therefore:

$$
\boxed{-121\text{ is Not Palindrome}}
$$

A common implementation can immediately return `false` when:

    n < 0

if the problem uses the standard definition.

---

# 30. Trailing Zero Rule

A positive number ending in zero cannot be a palindrome unless the number is exactly zero.

Example:

$$
10\rightarrow1
$$

Not palindrome.

Example:

$$
120\rightarrow21
$$

Not palindrome.

Example:

$$
1000\rightarrow1
$$

Not palindrome.

Therefore:

> [!important]
> For positive integers:
>
> **If the last digit is `0`, the number is not a palindrome.**
>
> Exception:
>
> $$0
> $$
>
> itself is a palindrome.

---

# 31. Example — Trailing Zero

## Example 15

### Question

Is `1010` a palindrome?

Reverse:

$$
1010\rightarrow101
$$

Since:

$$
1010\neq101
$$

Therefore:

$$
\boxed{\text{Not Palindrome}}
$$

---

# 32. Example — Zero

## Example 16

### Question

Is `0` a palindrome?

The reverse of `0` is:

$$
0
$$

Therefore:

$$
0=0
$$

and:

$$
\boxed{0\text{ is a Palindrome}}
$$

---

# 33. Advanced Example — Count Palindrome Numbers in a Range

## Example 17

### Question

Count palindrome numbers from `1` to `20`.

Palindromes:

$$
1,2,3,4,5,6,7,8,9,11
$$

Count:

$$
10
$$

Therefore:

$$
\boxed{10}
$$

---

# 34. Advanced Example — Palindromes in an Array

## Example 18

### Question

Find palindrome numbers in:

    [121, 123, 44, 98, 1331, 120]

Check:

$$
121\rightarrow121
$$

$$
123\rightarrow321
$$

$$
44\rightarrow44
$$

$$
98\rightarrow89
$$

$$
1331\rightarrow1331
$$

$$
120\rightarrow21
$$

Therefore:

$$
\boxed{121,44,1331}
$$

---

# 35. Advanced Example — Count Palindromes in an Array

## Example 19

For:

    [121, 123, 44, 98, 1331, 120]

Palindrome numbers:

$$
121,44,1331
$$

Count:

$$
\boxed{3}
$$

---

# 36. Advanced Example — Largest Palindrome in an Array

## Example 20

### Question

Find the largest palindrome in:

    [121, 44, 999, 123, 1331]

Palindrome numbers:

$$
121,44,999,1331
$$

Largest:

$$
\boxed{1331}
$$

---

# 37. Advanced Example — Sum of Palindrome Numbers

## Example 21

### Question

Find the sum of palindrome numbers in:

    [121, 123, 44, 99]

Palindromes:

$$
121,44,99
$$

Sum:

$$
121+44+99
$$

$$
=264
$$

Therefore:

$$
\boxed{264}
$$

---

# 38. Palindrome Construction Pattern

Sometimes a problem asks you to create a palindrome.

For example:

    123

Its reverse:

    321

A simple palindrome can be formed as:

$$
123321
$$

or:

$$
12321
$$

depending on whether the middle digit is duplicated.

> [!important]
> When constructing palindromes, first identify whether the problem wants:
>
> - Even-length palindrome
> - Odd-length palindrome
> - Minimum palindrome
> - Lexicographically smallest palindrome
> - Palindrome by modifying digits

These are different problems.

---

# 39. Palindrome and Reverse-and-Add

A common coding pattern is:

1. Take number.
2. Reverse number.
3. Add original and reverse.
4. Check whether result is palindrome.
5. Repeat if required.

Example:

$$
12+21=33
$$

Since:

$$
33=reverse(33)
$$

we get:

$$
\boxed{33\text{ is Palindrome}}
$$

---

# 40. Common Exam Pattern — Palindrome Number

> [!important] Must Master

### Pattern 1 — Reverse and Compare

$$
\boxed{original=reverse}
$$

### Pattern 2 — Store Original

    int original = n;

### Pattern 3 — Digit Extraction

    digit = n % 10;

### Pattern 4 — Reverse Construction

    reverse = reverse * 10 + digit;

### Pattern 5 — Remove Digit

    n /= 10;

### Pattern 6 — Zero

`0` is a palindrome.

### Pattern 7 — Trailing Zero

Positive numbers ending in `0` are not palindromes.

### Pattern 8 — Negative Numbers

Usually return `false` under standard integer-palindrome definitions.

### Pattern 9 — String Palindrome

Use two pointers:

    left = 0;
    right = length - 1;

### Pattern 10 — Array Problems

Apply `isPalindrome()` to each element.

---

# 41. Shortcuts

> [!tip]
> **Shortcut 1 — Core Condition**
>
> Memorize:
>
> $$\boxed{N=Reverse(N)}
> $$

> [!tip]
> **Shortcut 2 — Trailing Zero**
>
> If a positive integer ends with `0`, immediately think:
>
> $$\boxed{\text{Not Palindrome}}
> $$
>
> because its reverse loses the leading zero.

> [!tip]
> **Shortcut 3 — Single Digit**
>
> Every single-digit number is a palindrome.

> [!tip]
> **Shortcut 4 — Symmetry**
>
> For mental checking, compare the first and last digits, then move inward.
>
> Example:
>
> $$12321
> $$
>
> Compare:
>
> $$1=1$$
>
> $$2=2$$

> [!tip]
> **Shortcut 5 — String Input**
>
> If the input is a string, use two pointers instead of constructing a reversed string.

---

# 42. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Not Saving Original

Wrong:

    while (n != 0) {
        ...
    }

    if (n == reverse)

After the loop:

$$
n=0
$$

Correct:

    int original = n;

---

### Mistake 2 — Building Reverse Incorrectly

Wrong:

    reverse += digit;

Correct:

    reverse = reverse * 10 + digit;

---

### Mistake 3 — Using `/10` to Extract Digits

Wrong:

    digit = n / 10;

Correct:

    digit = n % 10;

---

### Mistake 4 — Forgetting to Remove the Digit

Without:

    n /= 10;

the loop can become infinite.

---

### Mistake 5 — Treating `120` as Palindrome

Reverse:

$$
120\rightarrow21
$$

Therefore:

$$
\boxed{\text{Not Palindrome}}
$$

---

### Mistake 6 — Ignoring Overflow

For large integers:

$$
reverse\times10+digit
$$

can overflow.

Use `long` or overflow checks when necessary.

---

### Mistake 7 — Confusing String and Integer Zeros

String:

    "001"

has length `3`.

Integer:

$$
001=1
$$

has one digit.

Always identify the input representation.

---

# 43. Time and Space Complexity

Let:

$$
d=\text{number of digits}
$$

Every digit is processed once.

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

Extra space for arithmetic reversal:

$$
\boxed{O(1)}
$$

---

# 44. Two-Pointer Complexity for Strings

For a string of length $n$:

Time:

$$
\boxed{O(n)}
$$

Space:

$$
\boxed{O(1)}
$$

because only two indices are required.

---

# 45. Arithmetic vs String Palindrome

| Method | Time | Space | Best Use |
|---|---:|---:|---|
| Reverse Integer | $O(\log N)$ | $O(1)$ | Integer problems |
| String + Reverse | $O(n)$ | $O(n)$ | Simple string solution |
| String + Two Pointers | $O(n)$ | $O(1)$ | Efficient string solution |

> [!tip]
> For integer palindrome questions, the reverse-and-compare approach is the most important pattern to master.

---

# 46. Recognition Checklist

> [!important] Must Recognize Quickly

**"Reads the same forward and backward."**

Think:

$$
\boxed{\text{Palindrome}}
$$

---

**"Reverse is equal to original."**

Think:

$$
\boxed{N=Reverse(N)}
$$

---

**"Check an integer palindrome."**

Think:

$$
\boxed{\text{Reverse + Compare}}
$$

---

**"Check a string palindrome."**

Think:

$$
\boxed{\text{Two Pointers}}
$$

---

**"Positive number ends in 0."**

Think:

$$
\boxed{\text{Not Palindrome}}
$$

---

**"Single digit."**

Think:

$$
\boxed{\text{Always Palindrome}}
$$

---

**"Need original after reversing."**

Think:

$$
\boxed{original=n}
$$

before modifying `n`.

---

**"Large integer."**

Think:

$$
\boxed{\text{long or overflow-safe logic}}
$$

---

# 47. Formula Sheet

## Last Digit

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

## Reverse Number

$$
\boxed{
reverse=reverse\times10+digit
}
$$

## Palindrome Condition

$$
\boxed{
N=Reverse(N)
}
$$

## Non-Palindrome Condition

$$
\boxed{
N\neq Reverse(N)
}
$$

## Positive Number With Trailing Zero

$$
\boxed{
N\%10=0\Rightarrow\text{Not Palindrome}
}
$$

for $N>0$.

## Complexity

$$
\boxed{O(\log N)}
$$

## Extra Space

$$
\boxed{O(1)}
$$

---

# 48. Quick Revision

> [!summary] One-Minute Revision

    Palindrome Number
    → A number that remains the same after reversal.

    Core condition
    → original == reverse.

    Main algorithm
    → Store original.
    → Extract digit using n % 10.
    → Build reverse using reverse * 10 + digit.
    → Remove digit using n /= 10.
    → Compare original and reverse.

    Example
    → 121 → 121 → Palindrome.

    Non-example
    → 123 → 321 → Not Palindrome.

    Single digit
    → Always Palindrome.

    Zero
    → Palindrome.

    Positive trailing zero
    → Not Palindrome.

    Negative numbers
    → Usually Not Palindrome under standard
      integer definitions.

    String palindrome
    → Use two pointers.

    Important related topic
    → Reverse Number.

    Digit extraction
    → % 10.

    Digit removal
    → / 10.

    Reverse construction
    → reverse * 10 + digit.

    Preserve original
    → int original = n.

    Overflow
    → Check constraints.

    Complexity
    → O(log N).

    Space
    → O(1).

---

## Golden Memory Trick

**A palindrome is simply a number whose reverse is exactly equal to the original.**

## One-Line Recognition

**When you see "same forward and backward" or "reverse equals original," immediately think Reverse + Compare.**