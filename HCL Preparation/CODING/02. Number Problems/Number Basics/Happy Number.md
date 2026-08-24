---
type: concept
subject: coding
topic: "Happy Number"
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
  - happy-number
  - java
  - digit-problems
  - cycle-detection
wikilinks:
  - "[[Number Basics]]"
  - "[[Digit Problems]]"
  - "[[Strong Number]]"
  - "[[Armstrong Number]]"
  - "[[Recursion Basics]]"
---

# Happy Number

## 1. Core Concept

> [!summary]
> A **Happy Number** is a positive integer that eventually becomes `1` when repeatedly replaced by the **sum of the squares of its digits**.
>
> If the process reaches:
>
> $$1$$
>
> the number is **Happy**.
>
> If the process enters a cycle that never reaches `1`, the number is **Not Happy**.
>
> Example:
>
> $$19$$
>
> $$1^2+9^2=1+81=82$$
>
> $$8^2+2^2=64+4=68$$
>
> $$6^2+8^2=36+64=100$$
>
> $$1^2+0^2+0^2=1$$
>
> Therefore:
>
> $$\boxed{19\text{ is a Happy Number}}
> $$

The key idea is:

**Square every digit → add → repeat → check whether you reach 1 or enter a cycle.**

---

# 2. Basic Meaning

For a number $N$:

1. Extract every digit.
2. Square each digit.
3. Add the squares.
4. Replace $N$ with the resulting sum.
5. Repeat the process.

If the result becomes:

$$
1
$$

then:

$$
\boxed{\text{Happy Number}}
$$

If the process repeats previous values without reaching `1`:

$$
\boxed{\text{Not a Happy Number}}
$$

---

# 3. Main Formula

If the digits of $N$ are:

$$
d_1,d_2,\ldots,d_k
$$

then the next value is:

$$
\boxed{
f(N)=d_1^2+d_2^2+\cdots+d_k^2
}
$$

Repeat:

$$
N\rightarrow f(N)\rightarrow f(f(N))\rightarrow\cdots
$$

### Happy Condition

$$
\boxed{\text{Eventually reaches }1}
$$

### Unhappy Condition

$$
\boxed{\text{Enters a cycle without reaching }1}
$$

---

# 4. Important Properties

## Property 1 — The Process Is Repeated

Unlike Armstrong or Strong Number problems, you do not perform the digit operation only once.

For example:

$$
19
$$

First:

$$
19\rightarrow82
$$

Then:

$$
82\rightarrow68
$$

Then:

$$
68\rightarrow100
$$

Then:

$$
100\rightarrow1
$$

Therefore:

$$
\boxed{19\text{ is Happy}}
$$

---

## Property 2 — Reaching 1 Means Happy

Once the process reaches:

$$
1
$$

the number is happy.

Also:

$$
1^2=1
$$

so `1` remains at `1`.

---

## Property 3 — Unhappy Numbers Enter Cycles

Some numbers never reach `1`.

A famous cycle is:

$$
4\rightarrow16\rightarrow37\rightarrow58\rightarrow89\rightarrow145\rightarrow42\rightarrow20\rightarrow4
$$

The value `4` appears again.

Therefore, the process will repeat forever.

So:

$$
\boxed{\text{Numbers entering this cycle are Not Happy}}
$$

---

## Property 4 — 1 Is Happy

For:

$$
1
$$

we get:

$$
1^2=1
$$

Therefore:

$$
\boxed{1\text{ is Happy}}
$$

---

## Property 5 — 19 Is a Common Example

The sequence is:

$$
19\rightarrow82\rightarrow68\rightarrow100\rightarrow1
$$

Therefore:

$$
\boxed{19\text{ is Happy}}
$$

---

# 5. Basic Example — 19

## Example 1

### Question

Check whether `19` is a Happy Number.

### Step 1

Digits:

$$
1,9
$$

Square and add:

$$
1^2+9^2
$$

$$
=1+81
$$

$$
=82
$$

### Step 2

For `82`:

$$
8^2+2^2
$$

$$
=64+4
$$

$$
=68
$$

### Step 3

For `68`:

$$
6^2+8^2
$$

$$
=36+64
$$

$$
=100
$$

### Step 4

For `100`:

$$
1^2+0^2+0^2
$$

$$
=1
$$

Therefore:

$$
\boxed{19\text{ is a Happy Number}}
$$

---

# 6. Basic Example — 1

## Example 2

### Question

Is `1` a Happy Number?

$$
1^2=1
$$

Therefore:

$$
\boxed{1\text{ is Happy}}
$$

---

# 7. Basic Example — 7

## Example 3

### Question

Check whether `7` is Happy.

Start:

$$
7^2=49
$$

Then:

$$
4^2+9^2
$$

$$
=16+81
$$

$$
=97
$$

Then:

$$
9^2+7^2
$$

$$
=81+49
$$

$$
=130
$$

Then:

$$
1^2+3^2+0^2
$$

$$
=1+9
$$

$$
=10
$$

Then:

$$
1^2+0^2=1
$$

Therefore:

$$
\boxed{7\text{ is Happy}}
$$

---

# 8. Basic Example — 2

## Example 4

### Question

Check whether `2` is Happy.

Sequence:

$$
2\rightarrow4
$$

$$
4\rightarrow16
$$

$$
16\rightarrow37
$$

$$
37\rightarrow58
$$

$$
58\rightarrow89
$$

$$
89\rightarrow145
$$

$$
145\rightarrow42
$$

$$
42\rightarrow20
$$

$$
20\rightarrow4
$$

We returned to:

$$
4
$$

without reaching `1`.

Therefore:

$$
\boxed{2\text{ is Not Happy}}
$$

---

# 9. Basic Example — 20

## Example 5

### Question

Is `20` Happy?

Calculate:

$$
2^2+0^2
$$

$$
=4
$$

Then:

$$
4\rightarrow16\rightarrow37\rightarrow58\rightarrow89\rightarrow145\rightarrow42\rightarrow20
$$

The value `20` appears again.

Therefore:

$$
\boxed{20\text{ is Not Happy}}
$$

---

# 10. Standard Java Program

## Example 6

### Question

Write a Java program to check whether a number is Happy.

### Code

    import java.util.HashSet;
    import java.util.Scanner;

    class Main {

        static int sumOfSquares(int n) {

            int sum = 0;

            while (n > 0) {

                int digit = n % 10;

                sum += digit * digit;

                n /= 10;
            }

            return sum;
        }

        static boolean isHappy(int n) {

            HashSet<Integer> seen = new HashSet<>();

            while (n != 1) {

                if (seen.contains(n)) {
                    return false;
                }

                seen.add(n);

                n = sumOfSquares(n);
            }

            return true;
        }

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            if (isHappy(n)) {
                System.out.println("Happy Number");
            } else {
                System.out.println("Not a Happy Number");
            }
        }
    }

### Main Logic

    n
    ↓
    Sum of squares of digits
    ↓
    New number
    ↓
    Repeat
    ↓
    Reaches 1 → Happy
    ↓
    Repeats previous value → Not Happy

---

# 11. Digit-Square Function

The most important helper function is:

    static int sumOfSquares(int n) {

        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += digit * digit;

            n /= 10;
        }

        return sum;
    }

For:

$$
123
$$

we calculate:

$$
1^2+2^2+3^2
$$

$$
=1+4+9
$$

$$
=14
$$

Therefore:

$$
\boxed{sumOfSquares(123)=14}
$$

---

# 12. Pattern Recognition — Happy Number

> [!important]
> **If the question says "Happy Number":**
>
> Immediately think:
>
> $$\boxed{\text{Repeated sum of squares of digits}}
> $$
>
> Continue until:
>
> $$1$$
>
> or a previously seen value appears.

---

# 13. Pattern Recognition — Repeated Transformation

> [!important]
> If a problem says:
>
> "Repeatedly perform an operation until..."
>
> think:
>
> **Iteration + cycle detection.**

For Happy Number:

    current number
    ↓
    transform
    ↓
    transform
    ↓
    transform
    ↓
    1 or repeated value

This is the key algorithmic pattern.

---

# 14. Pattern Recognition — Cycle

> [!important]
> If the process can continue indefinitely, ask:
>
> **Can a value repeat?**
>
> If yes, use:
>
> - `HashSet`
> - Floyd's Cycle Detection
>
> to detect the cycle.

Happy Number is a classic **cycle detection** problem.

---

# 15. Example — Cycle Detection

## Example 7

### Question

Why is `2` not Happy?

Sequence:

$$
2\rightarrow4
$$

$$
4\rightarrow16
$$

$$
16\rightarrow37
$$

$$
37\rightarrow58
$$

$$
58\rightarrow89
$$

$$
89\rightarrow145
$$

$$
145\rightarrow42
$$

$$
42\rightarrow20
$$

$$
20\rightarrow4
$$

Now `4` has appeared before.

Therefore:

$$
\boxed{\text{Cycle detected}}
$$

and:

$$
\boxed{2\text{ is Not Happy}}
$$

---

# 16. Happy Number Cycle

For unhappy numbers, the common cycle is:

$$
\boxed{
4\rightarrow16\rightarrow37\rightarrow58\rightarrow89\rightarrow145\rightarrow42\rightarrow20\rightarrow4
}
$$

> [!tip]
> For simple coding problems, you can remember this cycle.
>
> However, a general `HashSet` solution is safer and demonstrates proper cycle detection.

---

# 17. Shortcut — Known Unhappy Cycle

> [!tip]
> If the problem only deals with standard positive integers, you can stop when the sequence reaches `4`.
>
> Because:
>
> $$4\rightarrow16\rightarrow37\rightarrow58\rightarrow89\rightarrow145\rightarrow42\rightarrow20\rightarrow4
> $$
>
> Therefore:
>
> `1` → Happy
>
> `4` → Not Happy

Example:

    static boolean isHappy(int n) {

        while (n != 1 && n != 4) {
            n = sumOfSquares(n);
        }

        return n == 1;
    }

This is shorter than using a `HashSet`.

---

# 18. Example — Optimized Java Solution

## Example 8

### Code

    static int sumOfSquares(int n) {

        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += digit * digit;

            n /= 10;
        }

        return sum;
    }

    static boolean isHappy(int n) {

        while (n != 1 && n != 4) {
            n = sumOfSquares(n);
        }

        return n == 1;
    }

### Why It Works

All unhappy positive integers eventually enter the known cycle containing `4`.

Therefore:

$$
n=4
$$

is enough to conclude:

$$
\boxed{\text{Not Happy}}
$$

---

# 19. HashSet vs Fast and Slow Pointers

There are two important cycle-detection approaches.

| Method | Idea | Space |
|---|---|---:|
| HashSet | Store visited values | $O(k)$ |
| Floyd Cycle Detection | Slow and fast pointers | $O(1)$ |

For placement coding:

> [!tip]
> Learn the `HashSet` approach first because it is simple and easy to debug.
>
> Then learn Floyd's algorithm for optimized cycle detection.

---

# 20. Floyd Cycle Detection

The transformation:

$$
f(n)=\text{sum of squares of digits}
$$

creates a sequence.

We can use:

- `slow` moves one step.
- `fast` moves two steps.

### Code

    static int nextNumber(int n) {

        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += digit * digit;

            n /= 10;
        }

        return sum;
    }

    static boolean isHappy(int n) {

        int slow = n;
        int fast = nextNumber(n);

        while (fast != 1 && slow != fast) {

            slow = nextNumber(slow);

            fast = nextNumber(nextNumber(fast));
        }

        return fast == 1;
    }

### Idea

If the sequence contains a cycle:

$$
slow
$$

and:

$$
fast
$$

will eventually meet.

If the sequence reaches `1`, the number is Happy.

---

# 21. Example — Floyd Method

For:

$$
19
$$

the sequence is:

$$
19\rightarrow82\rightarrow68\rightarrow100\rightarrow1
$$

Since `1` is reached:

$$
\boxed{19\text{ is Happy}}
$$

For an unhappy number, slow and fast eventually meet inside the cycle.

Therefore:

$$
\boxed{\text{Cycle detected}}
$$

---

# 22. Example — 19 Sequence Table

| Step | Number | Sum of Digit Squares |
|---:|---:|---:|
| 1 | 19 | $1^2+9^2=82$ |
| 2 | 82 | $8^2+2^2=68$ |
| 3 | 68 | $6^2+8^2=100$ |
| 4 | 100 | $1^2+0^2+0^2=1$ |

Final:

$$
\boxed{1}
$$

Therefore:

$$
\boxed{19\text{ is Happy}}
$$

---

# 23. Example — 2 Sequence Table

| Step | Number | Next |
|---:|---:|---:|
| 1 | 2 | 4 |
| 2 | 4 | 16 |
| 3 | 16 | 37 |
| 4 | 37 | 58 |
| 5 | 58 | 89 |
| 6 | 89 | 145 |
| 7 | 145 | 42 |
| 8 | 42 | 20 |
| 9 | 20 | 4 |

Now:

$$
4
$$

appears again.

Therefore:

$$
\boxed{2\text{ is Not Happy}}
$$

---

# 24. Example — Find Happy Numbers in a Range

## Example 9

### Question

Find Happy Numbers from `1` to `20`.

Happy numbers in this range include:

$$
1,7,10,13,19
$$

Therefore:

$$
\boxed{1,7,10,13,19}
$$

---

# 25. Example — Check 10

## Example 10

### Question

Is `10` Happy?

$$
1^2+0^2=1
$$

Therefore:

$$
\boxed{10\text{ is Happy}}
$$

---

# 26. Example — Check 13

## Example 11

### Question

Is `13` Happy?

First:

$$
1^2+3^2=10
$$

Then:

$$
1^2+0^2=1
$$

Therefore:

$$
\boxed{13\text{ is Happy}}
$$

---

# 27. Example — Check 100

## Example 12

### Question

Is `100` Happy?

$$
1^2+0^2+0^2=1
$$

Therefore:

$$
\boxed{100\text{ is Happy}}
$$

---

# 28. Example — Check 4

## Example 13

### Question

Is `4` Happy?

Sequence:

$$
4\rightarrow16\rightarrow37\rightarrow58\rightarrow89\rightarrow145\rightarrow42\rightarrow20\rightarrow4
$$

The sequence returns to `4`.

Therefore:

$$
\boxed{4\text{ is Not Happy}}
$$

---

# 29. Example — Count Happy Numbers

## Example 14

### Question

Count Happy Numbers from `1` to `20`.

Happy numbers:

$$
1,7,10,13,19
$$

Count:

$$
5
$$

### Answer

$$
\boxed{5}
$$

---

# 30. Java Program — Happy Numbers in a Range

### Code

    static int sumOfSquares(int n) {

        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += digit * digit;

            n /= 10;
        }

        return sum;
    }

    static boolean isHappy(int n) {

        while (n != 1 && n != 4) {
            n = sumOfSquares(n);
        }

        return n == 1;
    }

    for (int n = 1; n <= 100; n++) {

        if (isHappy(n)) {
            System.out.print(n + " ");
        }
    }

This prints the Happy Numbers in the range.

---

# 31. Find Happy Numbers in an Array

## Example 15

### Question

Find Happy Numbers in:

    19 2 7 20 10 13

Happy numbers:

    19
    7
    10
    13

Therefore:

$$
\boxed{19,7,10,13}
$$

---

# 32. Sum Happy Numbers in an Array

## Example 16

### Question

Find the sum of Happy Numbers in:

    19 2 7 20 10 13

Happy numbers:

$$
19,7,10,13
$$

Sum:

$$
19+7+10+13=49
$$

### Answer

$$
\boxed{49}
$$

---

# 33. Largest Happy Number in an Array

## Example 17

### Question

Find the largest Happy Number in:

    19 2 7 20 10 13

Happy numbers:

$$
19,7,10,13
$$

Largest:

$$
\boxed{19}
$$

---

# 34. Happy Number vs Armstrong Number

This is an important comparison.

| Concept | Operation |
|---|---|
| Happy | Repeated sum of squared digits |
| Armstrong | Sum of digit powers using digit count |
| Strong | Sum of digit factorials |
| Perfect | Sum of proper divisors |

### Happy

$$
19\rightarrow82\rightarrow68\rightarrow100\rightarrow1
$$

### Armstrong

$$
153=1^3+5^3+3^3
$$

### Strong

$$
145=1!+4!+5!
$$

### Perfect

$$
6=1+2+3
$$

> [!important]
> These four number types are based on completely different transformations.

---

# 35. Pattern Recognition — Cycle Detection

> [!important]
> If a problem says:
>
> "Repeat an operation until a value repeats or a target is reached."
>
> Think:
>
> $$\boxed{\text{Cycle Detection}}
> $$
>
> Common tools:
>
> - HashSet
> - Floyd's Slow/Fast Pointers

Happy Number is one of the simplest examples of this pattern.

---

# 36. Pattern Recognition — Digit Transformation

> [!important]
> If every step requires processing all digits:
>
> Use:
>
>     while (n > 0) {
>         int digit = n % 10;
>         n /= 10;
>     }
>
> Then apply the required operation to `digit`.

For Happy Number:

$$
digit^2
$$

---

# 37. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Check Happy Number

Repeatedly calculate:

$$
\sum digit^2
$$

until `1` or a cycle.

---

### Pattern 2 — Detect Cycle Using HashSet

Store previously seen values.

If a value repeats:

$$
\boxed{\text{Not Happy}}
$$

---

### Pattern 3 — Use Known Cycle

For standard positive integers:

$$
4
$$

can be used as the unhappy-cycle indicator.

---

### Pattern 4 — Floyd Cycle Detection

Use:

$$
slow=f(slow)
$$

and:

$$
fast=f(f(fast))
$$

to detect a cycle with constant extra space.

---

### Pattern 5 — Happy Numbers in Range

Call `isHappy()` for each number.

---

### Pattern 6 — Count Happy Numbers

Increment a counter whenever `isHappy(n)` is true.

---

### Pattern 7 — Sum Happy Numbers

Add the number when `isHappy(n)` is true.

---

### Pattern 8 — Happy Number in Array

Check each element independently.

---

# 38. Shortcuts

> [!tip]
> **Shortcut 1 — Remember the Target**
>
> The only successful target is:
>
> $$\boxed{1}
> $$

> [!tip]
> **Shortcut 2 — Remember the Unhappy Cycle**
>
> $$\boxed{
> 4\rightarrow16\rightarrow37\rightarrow58\rightarrow89\rightarrow145\rightarrow42\rightarrow20\rightarrow4
> }
> $$

> [!tip]
> **Shortcut 3 — One-Step Transformation**
>
> For every step:
>
> $$\boxed{\text{sum of squares of digits}}
> $$

> [!tip]
> **Shortcut 4 — Digit Extraction**
>
> `% 10` → last digit.
>
> `/ 10` → remove last digit.

> [!tip]
> **Shortcut 5 — Cycle Problems**
>
> If the process can repeat forever:
>
> think:
>
> $$\boxed{HashSet\text{ or Floyd Cycle Detection}}
> $$

---

# 39. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Checking Only Once

Wrong:

$$
19\rightarrow82
$$

and stopping.

You must continue:

$$
19\rightarrow82\rightarrow68\rightarrow100\rightarrow1
$$

---

### Mistake 2 — Forgetting Cycle Detection

If the number does not reach `1`, the process may continue forever.

You need to detect repetition.

---

### Mistake 3 — Using Digit Cubes

Wrong:

$$
digit^3
$$

Correct:

$$
digit^2
$$

Happy Number always uses **squares**.

---

### Mistake 4 — Confusing Happy With Armstrong

Happy:

$$
\text{Repeated sum of digit squares}
$$

Armstrong:

$$
\text{One-time sum of digit powers}
$$

---

### Mistake 5 — Forgetting to Update N

After calculating the sum:

    n = sum;

must happen.

Otherwise, you keep processing the same number.

---

### Mistake 6 — Losing the Original Number When Needed

If the problem requires displaying or comparing the original number later, store:

    int original = n;

---

### Mistake 7 — Infinite Loop

A solution like:

    while (n != 1) {
        n = sumOfSquares(n);
    }

can run forever for unhappy numbers.

Use:

- `HashSet`
- known cycle `4`
- Floyd's cycle detection

---

### Mistake 8 — Mishandling Zero

For:

$$
0
$$

the digit-square sum is:

$$
0
$$

So a loop should be designed carefully if zero is allowed.

---

# 40. Time Complexity

Let:

$$
d=\text{number of digits}
$$

One transformation takes:

$$
O(d)
$$

For a fixed-width integer, `d` is small.

If the sequence requires `k` transformations:

$$
\boxed{O(kd)}
$$

With a `HashSet`, extra space is:

$$
\boxed{O(k)}
$$

With Floyd cycle detection:

$$
\boxed{O(1)}
$$

extra space.

---

# 41. HashSet vs Floyd vs Known Cycle

| Method | Time | Extra Space | Simplicity |
|---|---:|---:|---|
| HashSet | $O(kd)$ | $O(k)$ | Easy |
| Known `4` cycle | $O(kd)$ | $O(1)$ | Very Easy |
| Floyd | $O(kd)$ | $O(1)$ | Medium |

> [!tip]
> For placement coding:
>
> **Start with HashSet → learn the `4` shortcut → then master Floyd.**

---

# 42. Advanced Example — General HashSet Solution

## Example 18

### Code

    static int nextNumber(int n) {

        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += digit * digit;

            n /= 10;
        }

        return sum;
    }

    static boolean isHappy(int n) {

        HashSet<Integer> seen = new HashSet<>();

        while (n != 1) {

            if (!seen.add(n)) {
                return false;
            }

            n = nextNumber(n);
        }

        return true;
    }

### Important Idea

`HashSet.add(n)` returns:

- `true` if `n` was not present.
- `false` if `n` was already present.

Therefore:

    if (!seen.add(n)) {
        return false;
    }

is a compact cycle-detection pattern.

---

# 43. Advanced Example — Floyd Cycle Detection

## Example 19

### Code

    static int nextNumber(int n) {

        int sum = 0;

        while (n > 0) {

            int digit = n % 10;

            sum += digit * digit;

            n /= 10;
        }

        return sum;
    }

    static boolean isHappy(int n) {

        int slow = n;
        int fast = nextNumber(n);

        while (fast != 1 && slow != fast) {

            slow = nextNumber(slow);

            fast = nextNumber(nextNumber(fast));
        }

        return fast == 1;
    }

### Recognition

This is exactly the same idea as cycle detection in linked lists:

$$
\boxed{\text{Slow/Fast Pointer Pattern}}
$$

---

# 44. Why the Process Does Not Grow Forever

For a positive integer with `d` digits, each digit is at most `9`.

Therefore:

$$
\text{sum of digit squares}\leq81d
$$

For sufficiently large numbers, the transformed number becomes much smaller.

For example, a large number such as:

$$
999999
$$

becomes:

$$
6\times9^2
$$

$$
=486
$$

So the process quickly enters a relatively small set of values.

This is why cycle detection works effectively.

---

# 45. Example — Large Number

## Example 20

### Question

Consider:

$$
999999
$$

First transformation:

$$
9^2+9^2+9^2+9^2+9^2+9^2
$$

$$
=6\times81
$$

$$
=486
$$

Now the problem has been reduced from a six-digit number to a three-digit number.

> [!important]
> Repeated digit transformations often reduce large values to a small state space, making cycle detection practical.

---

# 46. Recognition Checklist

> [!important] Must Recognize Quickly

**"Happy Number."**

Think:

$$
\boxed{\text{Repeated sum of squares of digits}}
$$

---

**"Eventually becomes 1."**

Think:

$$
\boxed{\text{Happy}}
$$

---

**"Values repeat."**

Think:

$$
\boxed{\text{Cycle Detection}}
$$

---

**"Check each digit."**

Think:

    digit = n % 10;
    n /= 10;

---

**"What operation?"**

Think:

$$
\boxed{digit^2}
$$

---

**"Infinite loop risk."**

Think:

$$
\boxed{HashSet\text{ or Floyd}}
$$

---

**"Simple optimized solution."**

Think:

$$
\boxed{n=1\rightarrow Happy}
$$

$$
\boxed{n=4\rightarrow Not\ Happy}
$$

for the standard positive-integer problem.

---

# 47. Formula Sheet

## Digit Square Sum

$$
\boxed{
f(N)=\sum_{i=1}^{k}d_i^2
}
$$

## Happy Condition

$$
\boxed{
N\rightarrow\cdots\rightarrow1
}
$$

## Unhappy Condition

$$
\boxed{
N\rightarrow\cdots\rightarrow\text{cycle}
}
$$

## Digit Extraction

$$
\boxed{digit=N\%10}
$$

## Remove Last Digit

$$
\boxed{N=\lfloor N/10\rfloor}
$$

## Maximum Digit-Square Sum

For a $d$-digit number:

$$
\boxed{81d}
$$

## Common Happy Numbers

$$
\boxed{1,7,10,13,19}
$$

## Common Unhappy Cycle

$$
\boxed{
4\rightarrow16\rightarrow37\rightarrow58\rightarrow89\rightarrow145\rightarrow42\rightarrow20\rightarrow4
}
$$

## HashSet Extra Space

$$
\boxed{O(k)}
$$

## Floyd Extra Space

$$
\boxed{O(1)}
$$

---

# 48. Quick Revision

> [!summary] One-Minute Revision

    Happy Number
    → Repeatedly replace N with the sum of squares
      of its digits.

    Formula
    → d₁² + d₂² + ... + dₖ².

    Happy condition
    → Eventually reaches 1.

    Unhappy condition
    → Enters a cycle without reaching 1.

    Example
    → 19 → 82 → 68 → 100 → 1.

    Unhappy example
    → 2 → 4 → 16 → 37 → ... → 20 → 4.

    Important cycle
    → 4 → 16 → 37 → 58 → 89 → 145 → 42 → 20 → 4.

    Digit extraction
    → digit = n % 10.

    Remove digit
    → n /= 10.

    Main operation
    → digit × digit.

    Cycle detection
    → HashSet or Floyd.

    Simple shortcut
    → Stop at 1 or 4.

    Common Happy Numbers
    → 1, 7, 10, 13, 19.

    Armstrong
    → digit powers.

    Strong
    → digit factorials.

    Happy
    → repeated digit squares.

    Perfect
    → proper divisor sum.

    Complexity
    → O(kd), where k is the number of transformations
      and d is the number of digits.

    HashSet space
    → O(k).

    Floyd space
    → O(1).

---

## Golden Memory Trick

**Happy Number means repeatedly square the digits and add them until you either reach 1 or fall into a cycle.**

## One-Line Recognition

**When you see "repeatedly sum the squares of the digits until 1," think Happy Number + cycle detection.**