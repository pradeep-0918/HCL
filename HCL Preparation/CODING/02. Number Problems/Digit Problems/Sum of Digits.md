---
type: concept
subject: coding
topic: "Sum of Digits"
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
  - sum-of-digits
  - java
  - number-basics
wikilinks:
  - "[[Digit Problems]]"
  - "[[Number Basics]]"
  - "[[Count Digits]]"
  - "[[Reverse Number]]"
  - "[[Palindrome Number]]"
---

# Sum of Digits

## 1. Core Concept

> [!summary]
> **Sum of Digits** means adding all the individual digits of a number.
>
> Example:
>
> $$12345$$
>
> Its digits are:
>
> $$1,2,3,4,5$$
>
> Therefore:
>
> $$1+2+3+4+5=15$$
>
> So:
>
> $$\boxed{\text{Sum of digits of }12345=15}
> $$

The key coding idea is:

**Extract the last digit using `% 10` → add it to the sum → remove the last digit using `/ 10` → repeat.**

---

# 2. Basic Meaning

For a number:

$$
N=d_1d_2d_3\ldots d_k
$$

the sum of digits is:

$$
\boxed{d_1+d_2+d_3+\cdots+d_k}
$$

### Example

For:

$$
583
$$

the sum is:

$$
5+8+3=16
$$

Therefore:

$$
\boxed{16}
$$

---

# 3. Main Formula

If the digits of $N$ are:

$$
d_1,d_2,\ldots,d_k
$$

then:

$$
\boxed{
\text{Digit Sum}=\sum_{i=1}^{k}d_i
}
$$

### Arithmetic Extraction

Last digit:

$$
\boxed{digit=N\%10}
$$

Remove last digit:

$$
\boxed{N=\lfloor N/10\rfloor}
$$

---

# 4. Important Properties

## Property 1 — `% 10` Extracts the Last Digit

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

is the last digit.

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

## Property 3 — The Sum Is Independent of Digit Order

For:

$$
123
$$

and:

$$
321
$$

the digit sums are both:

$$
1+2+3=6
$$

Therefore:

$$
\boxed{\text{Digit order does not affect digit sum}}
$$

---

## Property 4 — Zero Does Not Change the Sum

For any number containing zero:

$$
0
$$

contributes nothing.

Example:

$$
10203
$$

Sum:

$$
1+0+2+0+3=6
$$

Therefore:

$$
\boxed{6}
$$

---

## Property 5 — Single-Digit Numbers

For a single digit:

$$
7
$$

the digit sum is:

$$
7
$$

Therefore:

$$
\boxed{\text{sum}(7)=7}
$$

---

# 5. Basic Example — 123

## Example 1

### Question

Find the sum of digits of `123`.

### Step 1

Extract:

$$
123\%10=3
$$

Sum:

$$
0+3=3
$$

Remove digit:

$$
123/10=12
$$

### Step 2

Extract:

$$
12\%10=2
$$

Sum:

$$
3+2=5
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

Sum:

$$
5+1=6
$$

Remove:

$$
1/10=0
$$

Therefore:

$$
\boxed{\text{Sum}=6}
$$

---

# 6. Basic Example — 987

## Example 2

### Question

Find the sum of digits of `987`.

$$
9+8+7
$$

$$
=24
$$

Therefore:

$$
\boxed{24}
$$

---

# 7. Basic Example — 10001

## Example 3

### Question

Find the sum of digits of `10001`.

$$
1+0+0+0+1
$$

$$
=2
$$

Therefore:

$$
\boxed{2}
$$

---

# 8. Basic Example — 5000

## Example 4

### Question

Find the sum of digits of `5000`.

$$
5+0+0+0
$$

$$
=5
$$

Therefore:

$$
\boxed{5}
$$

---

# 9. Basic Example — Single Digit

## Example 5

### Question

Find the sum of digits of `8`.

There is only one digit:

$$
8
$$

Therefore:

$$
\boxed{8}
$$

---

# 10. Basic Example — Zero

## Example 6

### Question

Find the sum of digits of `0`.

The only digit is `0`.

Therefore:

$$
\boxed{0}
$$

> [!important]
> `0` has one digit, but its digit sum is `0`.

---

# 11. Standard Java Program

## Example 7

### Question

Write a Java program to find the sum of digits of a number.

### Code

    import java.util.Scanner;

    class Main {

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            n = Math.abs(n);

            int sum = 0;

            while (n > 0) {

                int digit = n % 10;

                sum += digit;

                n /= 10;
            }

            System.out.println(sum);
        }
    }

### Main Pattern

    digit = n % 10;
    sum += digit;
    n /= 10;

This is the core pattern to remember.

---

# 12. Handling Zero

The basic loop:

    while (n > 0)

does not execute when:

$$
n=0
$$

But the correct digit sum of zero is:

$$
0
$$

Fortunately, the initialized value:

    int sum = 0;

already gives the correct result.

Therefore, no special handling is required for the sum itself.

---

# 13. Handling Negative Numbers

For:

$$
-123
$$

the minus sign is not a digit.

Consider:

$$
|-123|=123
$$

Then:

$$
1+2+3=6
$$

Therefore:

$$
\boxed{\text{Sum of digits of }-123=6}
$$

Use:

    n = Math.abs(n);

when the problem treats negative numbers by ignoring the sign.

> [!warning]
> Always check the problem statement. Some problems may define negative input differently.

---

# 14. Reusable Function

## Example 8

### Code

    static int sumOfDigits(int n) {

        n = Math.abs(n);

        int sum = 0;

        while (n > 0) {

            sum += n % 10;

            n /= 10;
        }

        return sum;
    }

For:

    sumOfDigits(12345)

we get:

$$
1+2+3+4+5=15
$$

Therefore:

$$
\boxed{15}
$$

---

# 15. Pattern Recognition — Sum of Digits

> [!important]
> **If the question asks "Find the sum of digits":**
>
> Immediately think:
>
>     sum = 0
>
>     while n > 0:
>         digit = n % 10
>         sum += digit
>         n /= 10
>
> This is the standard pattern.

---

# 16. Pattern Recognition — Process Every Digit

> [!important]
> If the problem says:
>
> "For every digit..."
>
> think:
>
>     digit = n % 10;
>     n /= 10;
>
> Then replace the processing step depending on the problem.
>
> Examples:
>
> Sum:
>
>     sum += digit;
>
> Reverse:
>
>     reverse = reverse * 10 + digit;
>
> Frequency:
>
>     freq[digit]++;
>
> Armstrong:
>
>     sum += power(digit, digits);
>
> Strong:
>
>     sum += factorial(digit);

---

# 17. Digit Processing Master Pattern

This is one of the most important coding patterns in Number Problems.

    while (n > 0) {

        int digit = n % 10;

        // Process digit

        n /= 10;
    }

### `% 10`

Gets:

$$
\boxed{\text{last digit}}
$$

### `/ 10`

Removes:

$$
\boxed{\text{last digit}}
$$

> [!tip]
> Mastering these two operations makes many beginner number problems much easier.

---

# 18. Example — Step-by-Step Table

## Example 9

### Question

Find the sum of digits of `4567`.

| Step | $n$ | $n\%10$ | Sum | New $n$ |
|---:|---:|---:|---:|---:|
| 1 | 4567 | 7 | 7 | 456 |
| 2 | 456 | 6 | 13 | 45 |
| 3 | 45 | 5 | 18 | 4 |
| 4 | 4 | 4 | 22 | 0 |

Therefore:

$$
\boxed{22}
$$

---

# 19. Example — Digit Sum of 99999

## Example 10

### Question

Find the digit sum of `99999`.

There are five `9`s:

$$
9+9+9+9+9
$$

$$
=45
$$

Therefore:

$$
\boxed{45}
$$

> [!tip]
> For a number containing repeated digits, multiplication can reduce mental calculation.
>
> Five `9`s:
>
> $$5\times9=45$$

---

# 20. Example — Digit Sum of 123456789

## Example 11

### Question

Find the digit sum of `123456789`.

$$
1+2+3+4+5+6+7+8+9
$$

Pair values:

$$
1+9=10
$$

$$
2+8=10
$$

$$
3+7=10
$$

$$
4+6=10
$$

plus:

$$
5
$$

Therefore:

$$
10+10+10+10+5=45
$$

### Answer

$$
\boxed{45}
$$

---

# 21. Shortcut — Repeated Digits

> [!tip]
> If the same digit occurs many times, multiply instead of repeatedly adding.
>
> Example:
>
> `777777`
>
> contains six `7`s.
>
> Therefore:
>
> $$6\times7=42$$
>
> So:
>
> $$\boxed{42}
> $$

---

# 22. Shortcut — Pairing Digits

> [!tip]
> For mental calculation, pair digits that add to `10`.
>
> Example:
>
> $$1+9=10$$
>
> $$2+8=10$$
>
> $$3+7=10$$
>
> $$4+6=10$$
>
> Therefore:
>
> $$123456789
> $$
>
> has digit sum:
>
> $$40+5=45$$

This is useful for quick aptitude calculations.

---

# 23. Shortcut — Digital Root

A powerful mathematical property is the **digital root**.

Repeatedly add the digits until only one digit remains.

Example:

$$
9875
$$

First:

$$
9+8+7+5=29
$$

Then:

$$
2+9=11
$$

Then:

$$
1+1=2
$$

Therefore:

$$
\boxed{\text{Digital Root}=2}
$$

> [!important]
> **Digit Sum and Digital Root are different.**
>
> Digit Sum:
>
> $$9875\rightarrow29$$
>
> Digital Root:
>
> $$9875\rightarrow29\rightarrow11\rightarrow2$$

---

# 24. Digital Root Formula

For a positive integer $N$:

$$
\boxed{
dr(N)=1+((N-1)\bmod9)
}
$$

For:

$$
N>0
$$

the digital root is between:

$$
1\text{ and }9
$$

For:

$$
N=0
$$

the digital root is:

$$
0
$$

---

# 25. Example — Digital Root of 9999

## Example 12

### Question

Find the digital root of `9999`.

First digit sum:

$$
9+9+9+9=36
$$

Again:

$$
3+6=9
$$

Therefore:

$$
\boxed{9}
$$

Using modulo:

$$
9999\bmod9=0
$$

When the remainder is `0`, the digital root is:

$$
\boxed{9}
$$

---

# 26. Example — Digital Root of 12345

## Example 13

### Question

Find the digital root of `12345`.

Digit sum:

$$
1+2+3+4+5=15
$$

Again:

$$
1+5=6
$$

Therefore:

$$
\boxed{6}
$$

---

# 27. Pattern Recognition — Digital Root

> [!important]
> If the question says:
>
> **"Keep adding digits until a single digit remains."**
>
> Think:
>
> $$\boxed{\text{Digital Root}}
> $$
>
> For positive $N$:
>
> $$\boxed{1+((N-1)\bmod9)}
> $$

---

# 28. Digit Sum and Divisibility by 9

An important number property:

A number is divisible by `9` if and only if its digit sum is divisible by `9`.

Example:

$$
729
$$

Digit sum:

$$
7+2+9=18
$$

Since:

$$
18
$$

is divisible by `9`:

$$
\boxed{729\text{ is divisible by }9}
$$

---

# 29. Example — Divisibility Check

## Example 14

### Question

Is `5832` divisible by `9`?

Digit sum:

$$
5+8+3+2=18
$$

Since:

$$
18\div9=2
$$

the number is divisible by `9`.

Therefore:

$$
\boxed{\text{Yes}}
$$

---

# 30. Divisibility by 3

A number is divisible by `3` if its digit sum is divisible by `3`.

Example:

$$
12345
$$

Digit sum:

$$
15
$$

Since:

$$
15\div3=5
$$

we get:

$$
\boxed{12345\text{ is divisible by }3}
$$

> [!tip]
> Digit sum is an important shortcut for divisibility by `3` and `9`.

---

# 31. Example — Not Divisible by 9

## Example 15

### Question

Is `1234` divisible by `9`?

Digit sum:

$$
1+2+3+4=10
$$

Since `10` is not divisible by `9`:

$$
\boxed{1234\text{ is Not divisible by }9}
$$

---

# 32. Sum of Digits in an Array

## Example 16

### Question

Find the digit sum of every element in:

    [12, 345, 6789]

Calculations:

$$
12\rightarrow1+2=3
$$

$$
345\rightarrow3+4+5=12
$$

$$
6789\rightarrow6+7+8+9=30
$$

Therefore:

$$
\boxed{3,12,30}
$$

---

# 33. Find Number With Maximum Digit Sum

## Example 17

### Question

Find the number with the maximum digit sum:

    [123, 999, 456, 78]

Digit sums:

$$
123\rightarrow6
$$

$$
999\rightarrow27
$$

$$
456\rightarrow15
$$

$$
78\rightarrow15
$$

Maximum:

$$
27
$$

Corresponding number:

$$
999
$$

### Answer

$$
\boxed{999}
$$

---

# 34. Count Numbers With Digit Sum K

## Example 18

### Question

Count numbers in:

    [12, 21, 30, 45, 123]

whose digit sum is `3`.

Calculate:

$$
12\rightarrow1+2=3
$$

$$
21\rightarrow2+1=3
$$

$$
30\rightarrow3+0=3
$$

$$
45\rightarrow9
$$

$$
123\rightarrow6
$$

Therefore, three numbers satisfy the condition.

### Answer

$$
\boxed{3}
$$

---

# 35. Sum of Digits Until One Digit

## Example 19

### Question

Reduce `987654` to a single digit.

First:

$$
9+8+7+6+5+4
$$

$$
=39
$$

Again:

$$
3+9=12
$$

Again:

$$
1+2=3
$$

Therefore:

$$
\boxed{3}
$$

This is the digital root.

---

# 36. Java Program — Digital Root

## Example 20

### Code

    static int digitalRoot(int n) {

        n = Math.abs(n);

        while (n >= 10) {

            int sum = 0;

            while (n > 0) {
                sum += n % 10;
                n /= 10;
            }

            n = sum;
        }

        return n;
    }

For:

    digitalRoot(987654)

the result is:

$$
\boxed{3}
$$

---

# 37. Optimized Digital Root

For a positive integer:

$$
\boxed{
dr(N)=1+((N-1)\%9)
}
$$

### Java

    static int digitalRoot(int n) {

        n = Math.abs(n);

        if (n == 0) {
            return 0;
        }

        return 1 + (n - 1) % 9;
    }

This gives:

    digitalRoot(987654)

Result:

$$
\boxed{3}
$$

> [!tip]
> Use the iterative method when the interviewer wants logic.
>
> Use the modulo formula when a mathematical shortcut is allowed.

---

# 38. Common Exam Pattern — Sum of Digits

> [!important] Must Master

### Pattern 1 — Basic Digit Sum

    sum = 0

    while n > 0:
        sum += n % 10
        n /= 10

---

### Pattern 2 — Digit Extraction

    digit = n % 10;

---

### Pattern 3 — Remove Digit

    n /= 10;

---

### Pattern 4 — Sum Until Single Digit

Repeatedly calculate digit sum.

---

### Pattern 5 — Digital Root

Use:

$$
1+((N-1)\bmod9)
$$

for positive $N$.

---

### Pattern 6 — Divisibility by 3

Check:

$$
\text{digit sum}\%3=0
$$

---

### Pattern 7 — Divisibility by 9

Check:

$$
\text{digit sum}\%9=0
$$

---

### Pattern 8 — Array Digit Sum

Apply the digit-sum function to every element.

---

# 39. Shortcuts

> [!tip]
> **Shortcut 1 — `% 10` and `/ 10`**
>
> Memorize:
>
> $$\boxed{\%10=\text{extract last digit}}
> $$
>
> $$\boxed{/10=\text{remove last digit}}
> $$

> [!tip]
> **Shortcut 2 — Repeated Digits**
>
> `88888`:
>
> $$5\times8=40$$

> [!tip]
> **Shortcut 3 — Divisibility by 9**
>
> Add the digits instead of performing long division.
>
> If the digit sum is divisible by `9`, the original number is divisible by `9`.

> [!tip]
> **Shortcut 4 — Divisibility by 3**
>
> Check whether the digit sum is divisible by `3`.

> [!tip]
> **Shortcut 5 — Digital Root**
>
> For positive $N$:
>
> $$\boxed{1+((N-1)\bmod9)}
> $$

> [!tip]
> **Shortcut 6 — Pair Digits**
>
> Pair values that add to `10` for fast mental calculation.

---

# 40. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting to Add the Extracted Digit

Wrong:

    digit = n % 10;
    n /= 10;

Correct:

    digit = n % 10;
    sum += digit;
    n /= 10;

---

### Mistake 2 — Using `/ 10` Instead of `% 10` to Get a Digit

Wrong:

    digit = n / 10;

Correct:

    digit = n % 10;

---

### Mistake 3 — Using `% 10` to Remove a Digit

`% 10` gives the last digit.

It does not remove the digit.

Correct removal:

    n /= 10;

---

### Mistake 4 — Forgetting Negative Numbers

If negative values are allowed and the sign should be ignored:

    n = Math.abs(n);

---

### Mistake 5 — Confusing Digit Sum With Digital Root

For:

$$
9875
$$

Digit sum:

$$
29
$$

Digital root:

$$
2
$$

Therefore:

$$
\boxed{\text{They are not the same}}
$$

---

### Mistake 6 — Assuming Zero Has No Digit

`0` has one digit.

Its digit sum is:

$$
0
$$

---

### Mistake 7 — Destroying the Original Number

If the original number is required later, use:

    int temp = n;

and process `temp`.

---

# 41. Time and Space Complexity

Let:

$$
d=\text{number of digits}
$$

Every digit is processed exactly once.

Therefore:

$$
\boxed{O(d)}
$$

Since:

$$
d=O(\log N)
$$

we can also write:

$$
\boxed{O(\log N)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 42. Arithmetic vs String Method

| Method | Time | Space | Best Use |
|---|---:|---:|---|
| Arithmetic `%10` and `/10` | $O(d)$ | $O(1)$ | Coding logic |
| String traversal | $O(d)$ | $O(d)$ | Very large numbers |
| Digital root formula | $O(1)$ | $O(1)$ | Repeated reduction to one digit |

> [!important]
> The arithmetic method is the most important pattern to master because it is reused in many number problems.

---

# 43. Very Large Number as String

If a number cannot fit inside `long`, store it as a `String`.

Example:

    String s = "987654321098765432109876543210";

To find its digit sum:

    int sum = 0;

    for (char ch : s.toCharArray()) {
        sum += ch - '0';
    }

### Explanation

If:

    ch = '7'

then:

    ch - '0'

gives:

$$
7
$$

Therefore:

$$
\boxed{\text{Character digit}=\text{ch}-'0'}
$$

---

# 44. Example — Large String Number

## Example 21

### Question

Find the digit sum of:

    "123456789012345"

Calculate:

$$
1+2+3+4+5+6+7+8+9+0+1+2+3+4+5
$$

First nine digits:

$$
45
$$

Remaining:

$$
0+1+2+3+4+5=15
$$

Total:

$$
45+15=60
$$

### Answer

$$
\boxed{60}
$$

---

# 45. Advanced Pattern — Sum of Digits of Every Number in a Range

## Example 22

### Question

Find the total sum of digits of all numbers from `1` to `10`.

Write the numbers:

$$
1,2,3,4,5,6,7,8,9,10
$$

Digit sums:

$$
1+2+3+4+5+6+7+8+9+1
$$

$$
=46
$$

Therefore:

$$
\boxed{46}
$$

For larger ranges, more advanced digit-DP or mathematical techniques may be required.

---

# 46. Advanced Pattern — Digital Root and Modulo 9

The reason digital root works is:

$$
10\equiv1\pmod9
$$

Therefore:

$$
10^k\equiv1\pmod9
$$

A number and its digit sum have the same remainder modulo `9`.

Example:

$$
5832
$$

Modulo `9`:

$$
5832\equiv5+8+3+2
$$

$$
\equiv18
$$

$$
\equiv0\pmod9
$$

Therefore the number is divisible by `9`.

---

# 47. Recognition Checklist

> [!important] Must Recognize Quickly

**"Find sum of digits."**

Think:

$$
\boxed{\%10\rightarrow+\rightarrow/10}
$$

---

**"Extract last digit."**

Think:

$$
\boxed{N\%10}
$$

---

**"Remove last digit."**

Think:

$$
\boxed{N/10}
$$

---

**"Keep adding digits until one digit remains."**

Think:

$$
\boxed{\text{Digital Root}}
$$

---

**"Check divisibility by 3."**

Think:

$$
\boxed{\text{Digit sum divisible by 3}}
$$

---

**"Check divisibility by 9."**

Think:

$$
\boxed{\text{Digit sum divisible by 9}}
$$

---

**"Very large number."**

Think:

$$
\boxed{\text{String traversal}}
$$

---

**"Process every digit."**

Think:

    while (n > 0) {
        int digit = n % 10;
        n /= 10;
    }

---

# 48. Formula Sheet

## Digit Sum

$$
\boxed{
S=d_1+d_2+\cdots+d_k
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

## Digital Root

For $N>0$:

$$
\boxed{
dr(N)=1+((N-1)\bmod9)
}
$$

For zero:

$$
\boxed{
dr(0)=0
}
$$

## Divisibility by 3

$$
\boxed{
\text{digit sum}\equiv0\pmod3
}
$$

## Divisibility by 9

$$
\boxed{
\text{digit sum}\equiv0\pmod9
}
$$

## Complexity

$$
\boxed{O(\log N)}
$$

Space:

$$
\boxed{O(1)}
$$

---

# 49. Quick Revision

> [!summary] One-Minute Revision

    Sum of Digits
    → Add all individual digits.

    Main pattern
    → digit = n % 10
    → sum += digit
    → n /= 10

    % 10
    → Extract last digit.

    / 10
    → Remove last digit.

    Example
    → 12345 → 1+2+3+4+5 = 15.

    Zero
    → Digit sum is 0.

    Negative number
    → Usually ignore the sign using abs.

    Digit Sum ≠ Digital Root.

    Digital Root
    → Repeatedly sum digits until one digit remains.

    Positive digital root
    → 1 + ((N - 1) % 9).

    Divisibility by 3
    → Digit sum divisible by 3.

    Divisibility by 9
    → Digit sum divisible by 9.

    Huge number
    → Use String.

    Character to digit
    → ch - '0'.

    Preserve original
    → Use a temporary variable.

    Common related problems
    → Count Digits.
    → Reverse Number.
    → Palindrome.
    → Armstrong.
    → Strong.
    → Digit Frequency.

    Complexity
    → O(log N).

    Space
    → O(1).

---

## Golden Memory Trick

**For every digit, take it with `%10`, add it to the sum, remove it with `/10`, and repeat until the number becomes 0.**

## One-Line Recognition

**When a problem asks for the sum of individual digits, immediately think `%10 → add → /10 → repeat`.**