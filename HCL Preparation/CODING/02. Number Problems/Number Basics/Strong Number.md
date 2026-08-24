---
type: concept
subject: coding
topic: "Strong Number"
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
  - strong-number
  - java
  - factorial
  - digit-problems
wikilinks:
  - "[[Number Basics]]"
  - "[[Armstrong Number]]"
  - "[[Factorial]]"
  - "[[Digit Problems]]"
  - "[[Perfect Number]]"
---

# Strong Number

## 1. Core Concept

> [!summary]
> A **Strong Number** is a number in which the **sum of the factorials of its individual digits** is equal to the original number.
>
> For example:
>
> $$145$$
>
> Its digits are:
>
> $$1,4,5$$
>
> Calculate:
>
> $$1!+4!+5!$$
>
> $$=1+24+120$$
>
> $$=145$$
>
> Therefore:
>
> $$\boxed{145\text{ is a Strong Number}}
> $$

The key idea is:

**Extract each digit → calculate its factorial → add the factorials → compare with the original number.**

---

# 2. Basic Meaning

For a number:

$$
N=d_1d_2d_3\ldots d_k
$$

the number is Strong if:

$$
\boxed{
d_1!+d_2!+d_3!+\cdots+d_k!=N
}
$$

### Example

For:

$$
145
$$

we have:

$$
1!+4!+5!
$$

$$
=1+24+120
$$

$$
=145
$$

Therefore:

$$
\boxed{145\text{ is Strong}}
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
N=\sum_{i=1}^{k}d_i!
}
$$

### Strong Number Condition

$$
\boxed{\text{Sum of digit factorials}=N}
$$

Otherwise:

$$
\boxed{\text{Not a Strong Number}}
$$

---

# 4. Important Properties

## Property 1 — Factorial of Each Digit Is Used

For Strong Numbers, the operation is:

$$
digit!
$$

not:

$$
digit^k
$$

This is the main difference from Armstrong Numbers.

---

## Property 2 — Only Digits Are Processed

For:

$$
145
$$

we process:

$$
1,4,5
$$

not the entire number `145!`.

Correct:

$$
1!+4!+5!
$$

Wrong:

$$
145!
$$

---

## Property 3 — 0! = 1

A very important factorial rule is:

$$
\boxed{0!=1}
$$

Therefore, if a number contains zero, zero contributes `1`.

Example:

$$
10
$$

Calculation:

$$
1!+0!
$$

$$
=1+1
$$

$$
=2
$$

Therefore:

$$
\boxed{10\text{ is Not Strong}}
$$

---

## Property 4 — 1! = 1

Another useful rule:

$$
\boxed{1!=1}
$$

---

## Property 5 — Common Strong Numbers

The commonly known positive Strong Numbers are:

$$
\boxed{1,2,145,40585}
$$

Examples:

$$
145=1!+4!+5!
$$

and:

$$
40585=4!+0!+5!+8!+5!
$$

---

## Property 6 — Strong Number Is Different From Armstrong Number

Armstrong:

$$
\text{digit}^{\text{number of digits}}
$$

Strong:

$$
\text{digit}!
$$

Example:

$$
145
$$

is Strong because:

$$
1!+4!+5!=145
$$

But it is not Armstrong.

---

# 5. Important Factorial Values

For Strong Number problems, memorize factorials from `0!` to `9!`.

| Digit | Factorial |
|---:|---:|
| 0 | $1$ |
| 1 | $1$ |
| 2 | $2$ |
| 3 | $6$ |
| 4 | $24$ |
| 5 | $120$ |
| 6 | $720$ |
| 7 | $5040$ |
| 8 | $40320$ |
| 9 | $362880$ |

> [!important]
> Since a decimal digit can only be from `0` to `9`, you only need factorial values from:
>
> $$0!\text{ to }9!$$

---

# 6. Basic Example — 145

## Example 1

### Question

Check whether `145` is a Strong Number.

### Step 1 — Extract digits

    1
    4
    5

### Step 2 — Calculate factorials

$$
1!=1
$$

$$
4!=24
$$

$$
5!=120
$$

### Step 3 — Add

$$
1+24+120=145
$$

### Step 4 — Compare

$$
145=145
$$

### Answer

$$
\boxed{145\text{ is a Strong Number}}
$$

---

# 7. Basic Example — 123

## Example 2

### Question

Check whether `123` is a Strong Number.

Calculate:

$$
1!+2!+3!
$$

$$
=1+2+6
$$

$$
=9
$$

Since:

$$
9\neq123
$$

Therefore:

$$
\boxed{123\text{ is Not a Strong Number}}
$$

---

# 8. Basic Example — 1

## Example 3

### Question

Is `1` a Strong Number?

There is only one digit:

$$
1
$$

Calculate:

$$
1!=1
$$

Therefore:

$$
\boxed{1\text{ is a Strong Number}}
$$

---

# 9. Basic Example — 2

## Example 4

### Question

Is `2` a Strong Number?

$$
2!=2
$$

Therefore:

$$
\boxed{2\text{ is a Strong Number}}
$$

---

# 10. Basic Example — 10

## Example 5

### Question

Is `10` a Strong Number?

Digits:

$$
1,0
$$

Calculate:

$$
1!+0!
$$

Since:

$$
1!=1
$$

and:

$$
0!=1
$$

we get:

$$
1+1=2
$$

Since:

$$
2\neq10
$$

Therefore:

$$
\boxed{10\text{ is Not a Strong Number}}
$$

---

# 11. Basic Java Program

## Example 6

### Question

Write a Java program to check whether a number is a Strong Number.

### Code

    import java.util.Scanner;

    class Main {

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            int original = n;
            int sum = 0;

            while (n > 0) {

                int digit = n % 10;

                int fact = 1;

                for (int i = 1; i <= digit; i++) {
                    fact *= i;
                }

                sum += fact;

                n /= 10;
            }

            if (sum == original) {
                System.out.println("Strong Number");
            } else {
                System.out.println("Not a Strong Number");
            }
        }
    }

### Main Logic

    digit = n % 10
    → Extract digit

    Calculate digit!

    Add digit! to sum

    n /= 10
    → Remove digit

    Compare sum with original

---

# 12. Preserve the Original Number

While extracting digits:

    n /= 10;

the value of `n` changes.

For example:

$$
145
$$

becomes:

$$
14
$$

then:

$$
1
$$

then:

$$
0
$$

Therefore store:

    int original = n;

before processing.

> [!warning]
> Always preserve the original number before modifying it.

---

# 13. Factorial Function

A reusable factorial method:

    static int factorial(int n) {

        int fact = 1;

        for (int i = 1; i <= n; i++) {
            fact *= i;
        }

        return fact;
    }

Then:

    sum += factorial(digit);

This makes the Strong Number logic cleaner.

---

# 14. Improved Java Solution

## Example 7

### Code

    static int factorial(int n) {

        int fact = 1;

        for (int i = 2; i <= n; i++) {
            fact *= i;
        }

        return fact;
    }

    static boolean isStrong(int n) {

        if (n < 0) {
            return false;
        }

        int original = n;
        int sum = 0;

        if (n == 0) {
            return factorial(0) == 0;
        }

        while (n > 0) {

            int digit = n % 10;

            sum += factorial(digit);

            n /= 10;
        }

        return sum == original;
    }

For the standard positive-integer definition, `0` is not a Strong Number because:

$$
0!=1\neq0
$$

So the special case returns false.

---

# 15. Precomputed Factorial Shortcut

Since digits only range from `0` to `9`, we can precompute their factorials.

### Code

    static boolean isStrong(int n) {

        int[] fact = {
            1,
            1,
            2,
            6,
            24,
            120,
            720,
            5040,
            40320,
            362880
        };

        int original = n;
        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += fact[digit];

            n /= 10;
        }

        return sum == original;
    }

> [!tip]
> This is very efficient because factorials for digits `0` through `9` never need to be recalculated.

---

# 16. Example — 40585

## Example 8

### Question

Check whether `40585` is a Strong Number.

Digits:

$$
4,0,5,8,5
$$

Calculate:

$$
4!+0!+5!+8!+5!
$$

Substitute:

$$
24+1+120+40320+120
$$

Calculate:

$$
24+1=25
$$

$$
25+120=145
$$

$$
145+40320=40465
$$

$$
40465+120=40585
$$

Therefore:

$$
\boxed{40585\text{ is a Strong Number}}
$$

---

# 17. Example — 145 vs 40585

| Number | Factorial Sum | Result |
|---:|---:|---|
| 145 | $1!+4!+5!=145$ | Strong |
| 40585 | $4!+0!+5!+8!+5!=40585$ | Strong |
| 123 | $1!+2!+3!=9$ | Not Strong |
| 10 | $1!+0!=2$ | Not Strong |

---

# 18. Pattern Recognition — Strong Number

> [!important]
> **If the question says "Strong Number":**
>
> Immediately think:
>
> $$\boxed{\text{Factorial of each digit}}
> $$
>
> Then:
>
> $$\boxed{\text{Sum factorials and compare with N}}
> $$

---

# 19. Pattern Recognition — Digit Factorial

> [!important]
> If the question says:
>
> "Sum of factorials of digits"
>
> think:
>
> $$\boxed{Strong Number}
> $$

Example:

$$
145
$$

becomes:

$$
1!+4!+5!
$$

---

# 20. Pattern Recognition — Digit Extraction

> [!important]
> If the problem requires processing each digit:
>
> Use:
>
>     digit = n % 10;
>     n /= 10;

This same pattern is useful for:

- Strong Number
- Armstrong Number
- Palindrome Number
- Reverse Number
- Sum of Digits
- Digit Frequency

---

# 21. Pattern Recognition — Factorial Lookup

> [!important]
> Because every digit is between `0` and `9`, use a factorial lookup table when many numbers must be checked.

Example:

    fact[0] = 1
    fact[1] = 1
    fact[2] = 2
    fact[3] = 6
    fact[4] = 24
    fact[5] = 120
    fact[6] = 720
    fact[7] = 5040
    fact[8] = 40320
    fact[9] = 362880

---

# 22. Example — Check 145 Quickly

## Example 9

### Question

Is `145` Strong?

Memorized factorials:

$$
1!=1
$$

$$
4!=24
$$

$$
5!=120
$$

Therefore:

$$
1+24+120=145
$$

### Answer

$$
\boxed{Yes}
$$

---

# 23. Example — Check 146

## Example 10

### Question

Is `146` Strong?

Calculate:

$$
1!+4!+6!
$$

$$
=1+24+720
$$

$$
=745
$$

Since:

$$
745\neq146
$$

Therefore:

$$
\boxed{146\text{ is Not Strong}}
$$

---

# 24. Strong Number in a Range

## Example 11

### Question

Find Strong Numbers from `1` to `1000`.

Known Strong Numbers in this range:

$$
\boxed{1,2,145}
$$

Therefore:

$$
\boxed{1,2,145}
$$

---

# 25. Java Program — Strong Numbers in a Range

### Code

    static int factorial(int n) {

        int fact = 1;

        for (int i = 2; i <= n; i++) {
            fact *= i;
        }

        return fact;
    }

    static boolean isStrong(int n) {

        if (n <= 0) {
            return false;
        }

        int original = n;
        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += factorial(digit);

            n /= 10;
        }

        return sum == original;
    }

    for (int n = 1; n <= 1000; n++) {

        if (isStrong(n)) {
            System.out.print(n + " ");
        }
    }

### Output

    1 2 145

---

# 26. Count Strong Numbers

## Example 12

### Question

How many Strong Numbers are between `1` and `1000`?

Strong numbers:

$$
1,2,145
$$

Count:

$$
3
$$

### Answer

$$
\boxed{3}
$$

---

# 27. Sum Strong Numbers

## Example 13

### Question

Find the sum of Strong Numbers from `1` to `1000`.

Strong numbers:

$$
1,2,145
$$

Therefore:

$$
1+2+145=148
$$

### Answer

$$
\boxed{148}
$$

---

# 28. Find Strong Numbers in an Array

## Example 14

### Question

Find Strong Numbers in:

    145 123 40585 10 2 100

Strong numbers:

    145
    40585
    2

Therefore:

$$
\boxed{145,40585,2}
$$

---

# 29. Example — Sum Strong Numbers in an Array

## Example 15

### Question

Find the sum of Strong Numbers in:

    145 123 2 100 40585

Strong numbers:

$$
145,2,40585
$$

Sum:

$$
145+2+40585
$$

$$
=40732
$$

### Answer

$$
\boxed{40732}
$$

---

# 30. Strong Number vs Armstrong Number

This is an important placement comparison.

| Concept | Operation on Each Digit |
|---|---|
| Armstrong | Raise digit to number of digits |
| Strong | Calculate digit factorial |
| Palindrome | Reverse digit order |
| Perfect | Sum proper divisors |

### Example

For `145`:

Strong:

$$
1!+4!+5!=145
$$

Armstrong:

$$
1^3+4^3+5^3
$$

$$
=1+64+125
$$

$$
=190
$$

Therefore:

$$
\boxed{145\text{ is Strong but Not Armstrong}}
$$

> [!important]
> Remember:
>
> **Armstrong → Power**
>
> **Strong → Factorial**

---

# 31. Strong Number vs Perfect Number

| Feature | Strong Number | Perfect Number |
|---|---|---|
| Works with | Digits | Divisors |
| Operation | Factorial | Addition |
| Main elements | Individual digits | Proper divisors |
| Example | 145 | 6 |
| Formula | $\sum digit!$ | $\sum proper\ divisors=N$ |

Example:

$$
145
$$

uses:

$$
1!,4!,5!
$$

while:

$$
6
$$

uses:

$$
1+2+3
$$

---

# 32. Example — Identify the Pattern

## Example 16

### Question

A number is said to satisfy:

$$
1!+4!+5!=145
$$

What type of number is it?

The expression uses factorials of digits.

Therefore:

$$
\boxed{\text{Strong Number}}
$$

---

# 33. Example — Identify the Pattern

## Example 17

### Question

A number satisfies:

$$
1^3+5^3+3^3=153
$$

What type of number is it?

The digits are raised to the number of digits.

Therefore:

$$
\boxed{\text{Armstrong Number}}
$$

---

# 34. Common Exam Pattern — Check Strong Number

Standard algorithm:

    original = n
    sum = 0

    while n > 0

        digit = n % 10

        sum += factorial(digit)

        n /= 10

    if sum == original
        Strong
    else
        Not Strong

---

# 35. Common Exam Pattern — Range

For:

$$
L\text{ to }R
$$

use:

    for (int n = L; n <= R; n++) {

        if (isStrong(n)) {
            System.out.println(n);
        }
    }

---

# 36. Common Exam Pattern — Count

Use:

    int count = 0;

    for (int n = L; n <= R; n++) {

        if (isStrong(n)) {
            count++;
        }
    }

---

# 37. Common Exam Pattern — Sum

Use:

    int sum = 0;

    for (int n = L; n <= R; n++) {

        if (isStrong(n)) {
            sum += n;
        }
    }

---

# 38. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Check Strong Number

Calculate:

$$
\sum digit!
$$

and compare with `N`.

### Pattern 2 — Extract Digits

Use:

    digit = n % 10;
    n /= 10;

### Pattern 3 — Factorial of Digit

Use:

    fact = 1;

    for (int i = 2; i <= digit; i++) {
        fact *= i;
    }

### Pattern 4 — Strong Numbers in Range

Check every number independently.

### Pattern 5 — Count Strong Numbers

Increment count when `isStrong(n)` is true.

### Pattern 6 — Sum Strong Numbers

Add `n` when `isStrong(n)` is true.

### Pattern 7 — Array Search

Check each array element.

### Pattern 8 — Factorial Lookup

Use precomputed factorials for `0` through `9`.

---

# 39. Shortcuts

> [!tip]
> **Shortcut 1 — Memorize Factorials**
>
> The most useful values:
>
> $$1!=1$$
>
> $$2!=2$$
>
> $$3!=6$$
>
> $$4!=24$$
>
> $$5!=120$$
>
> $$6!=720$$
>
> $$7!=5040$$
>
> $$8!=40320$$
>
> $$9!=362880$$

> [!tip]
> **Shortcut 2 — Remember Common Strong Numbers**
>
> $$\boxed{1,2,145,40585}
> $$

> [!tip]
> **Shortcut 3 — Use Lookup Table**
>
> Since digits are only `0` through `9`, precompute factorials once.

> [!tip]
> **Shortcut 4 — Digit Extraction**
>
> `% 10` → get last digit.
>
> `/ 10` → remove last digit.

> [!tip]
> **Shortcut 5 — Pattern Recognition**
>
> If you see factorial signs attached to digits:
>
> $$\boxed{\text{Strong Number}}
> $$

---

# 40. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Calculating N!

Wrong:

$$
145!
$$

Correct:

$$
1!+4!+5!
$$

---

### Mistake 2 — Using Powers Instead of Factorials

Wrong:

$$
1^3+4^3+5^3
$$

Correct:

$$
1!+4!+5!
$$

---

### Mistake 3 — Forgetting 0!

Remember:

$$
\boxed{0!=1}
$$

---

### Mistake 4 — Losing the Original Number

Wrong approach:

    while (n > 0) {
        ...
        n /= 10;
    }

then:

    if (sum == n)

At this point:

$$
n=0
$$

Correct:

    int original = n;

and compare:

    sum == original

---

### Mistake 5 — Recalculating Factorials Unnecessarily

Since digits are only `0` through `9`, use a lookup table when appropriate.

---

### Mistake 6 — Confusing Strong and Armstrong

Strong:

$$
digit!
$$

Armstrong:

$$
digit^{number\ of\ digits}
$$

---

### Mistake 7 — Treating 0 as Strong

For standard positive Strong Number definitions:

$$
0!=1
$$

but:

$$
1\neq0
$$

Therefore:

$$
\boxed{0\text{ is Not Strong}}
$$

---

# 41. Advanced Example — 40585

## Example 18

### Question

Verify `40585` using factorial values.

Digits:

$$
4,0,5,8,5
$$

Factorials:

$$
4!=24
$$

$$
0!=1
$$

$$
5!=120
$$

$$
8!=40320
$$

$$
5!=120
$$

Sum:

$$
24+1+120+40320+120
$$

$$
=40585
$$

Therefore:

$$
\boxed{40585\text{ is a Strong Number}}
$$

---

# 42. Advanced Example — Non-Strong Five-Digit Number

## Example 19

### Question

Check whether `12345` is Strong.

Calculate:

$$
1!+2!+3!+4!+5!
$$

$$
=1+2+6+24+120
$$

$$
=153
$$

Since:

$$
153\neq12345
$$

Therefore:

$$
\boxed{12345\text{ is Not a Strong Number}}
$$

---

# 43. Advanced Example — Efficient Range Processing

## Example 20

### Question

Find all Strong Numbers between `1` and `100000`.

### Efficient Strategy

Since only digit factorials are required:

1. Precompute factorials `0!` to `9!`.
2. Process each number.
3. Extract each digit.
4. Use the lookup table.
5. Compare the sum with the original.

This avoids repeatedly calculating factorials.

### Complexity

If each number has at most $d$ digits:

$$
O(R\cdot d)
$$

for a range from `1` to `R`.

With fixed-size decimal integers:

$$
d=O(\log R)
$$

so:

$$
\boxed{O(R\log R)}
$$

in terms of the numeric range.

---

# 44. Integer Overflow Consideration

Factorials grow quickly.

For digits:

$$
9!=362880
$$

which fits comfortably inside an `int`.

However, the sum for a very large number can exceed `int`.

> [!warning]
> If the input constraints allow very large values, prefer:
>
>     long sum
>
> instead of:
>
>     int sum

For normal 32-bit integer input, `long` is a safe choice for the accumulated sum.

---

# 45. Recognition Checklist

> [!important] Must Recognize Quickly

**"Sum of factorials of digits."**

Think:

$$
\boxed{Strong Number}
$$

---

**"Check whether N is Strong."**

Think:

$$
\boxed{\text{Extract digits}\rightarrow\text{factorial}\rightarrow\text{sum}\rightarrow\text{compare}}
$$

---

**"Process every digit."**

Think:

    digit = n % 10;
    n /= 10;

---

**"0 appears as a digit."**

Think:

$$
\boxed{0!=1}
$$

---

**"Armstrong or Strong?"**

Think:

$$
Armstrong\rightarrow digit^{d}
$$

$$
Strong\rightarrow digit!
$$

---

**"Many numbers must be checked."**

Think:

$$
\boxed{\text{Precompute }0!\text{ through }9!}
$$

---

# 46. Formula Sheet

## Strong Number Condition

$$
\boxed{
N=\sum_{i=1}^{k}d_i!
}
$$

## Factorial Definition

$$
\boxed{
n!=n\times(n-1)\times\cdots\times2\times1
}
$$

## Important Special Cases

$$
\boxed{0!=1}
$$

$$
\boxed{1!=1}
$$

## Digit Extraction

$$
\boxed{digit=N\%10}
$$

## Remove Last Digit

$$
\boxed{N=\lfloor N/10\rfloor}
$$

## Important Factorials

$$
\boxed{0!=1}
$$

$$
\boxed{1!=1}
$$

$$
\boxed{2!=2}
$$

$$
\boxed{3!=6}
$$

$$
\boxed{4!=24}
$$

$$
\boxed{5!=120}
$$

$$
\boxed{6!=720}
$$

$$
\boxed{7!=5040}
$$

$$
\boxed{8!=40320}
$$

$$
\boxed{9!=362880}
$$

## Common Strong Numbers

$$
\boxed{1,2,145,40585}
$$

## Complexity

With factorial calculation per digit:

$$
\boxed{O(d\times9)=O(d)}
$$

With factorial lookup:

$$
\boxed{O(d)}
$$

where $d$ is the number of digits.

Space:

$$
\boxed{O(1)}
$$

---

# 47. Quick Revision

> [!summary] One-Minute Revision

    Strong Number
    → Sum of factorials of individual digits
      equals the original number.

    Formula
    → d₁! + d₂! + ... + dₖ! = N.

    Main operation
    → Factorial of each digit.

    0!
    → 1.

    1!
    → 1.

    Digit extraction
    → digit = n % 10.

    Remove digit
    → n /= 10.

    Preserve original
    → int original = n.

    Common Strong Numbers
    → 1, 2, 145, 40585.

    145
    → 1! + 4! + 5! = 145.

    40585
    → 4! + 0! + 5! + 8! + 5! = 40585.

    Strong vs Armstrong
    → Strong uses factorial.
    → Armstrong uses powers.

    Strong vs Perfect
    → Strong uses digit factorials.
    → Perfect uses proper divisors.

    Range problem
    → Check every number.

    Array problem
    → Check every element.

    Optimization
    → Precompute factorials from 0! to 9!.

    Complexity
    → O(number of digits).

    Space
    → O(1).

---

## Golden Memory Trick

**Strong Number means every digit contributes its factorial, and all those factorials add back to the original number.**

## One-Line Recognition

**When you see "sum of factorials of digits equals the number," immediately think Strong Number.**