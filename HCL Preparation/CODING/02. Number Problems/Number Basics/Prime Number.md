---
type: concept
subject: coding
topic: "Prime Number"
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
  - prime-number
  - java
  - divisibility
  - factors
  - optimization
wikilinks:
  - "[[Number Basics]]"
  - "[[Composite Number]]"
  - "[[GCD and LCM]]"
  - "[[Divisibility]]"
  - "[[Modular Arithmetic]]"
---

# Prime Number

## 1. Core Concept

> [!summary]
> A **prime number** is a positive integer greater than `1` that has exactly **two positive factors**:
>
> `1` and the number itself.
>
> Examples:
>
> $$2,3,5,7,11,13,17,19,\ldots$$
>
> The fastest basic recognition rule is:
>
> **Check whether the number has any divisor other than `1` and itself.**

For a number $n$:

$$
n>1
$$

and there must be no integer $d$ satisfying:

$$
1<d<n
$$

such that:

$$
n\%d=0
$$

Therefore:

$$
\boxed{\text{Prime} \iff n>1\text{ and no divisor exists from }2\text{ to }\sqrt n}
$$

---

# 2. Basic Meaning

A prime number has exactly two positive divisors.

### Example

For `7`:

Factors:

$$
1,7
$$

Exactly two factors.

Therefore:

$$
\boxed{7\text{ is Prime}}
$$

For `8`:

Factors:

$$
1,2,4,8
$$

More than two factors.

Therefore:

$$
\boxed{8\text{ is Not Prime}}
$$

---

# 3. Important Properties

## Property 1 — Prime Numbers Are Greater Than 1

The smallest prime number is:

$$
\boxed{2}
$$

Numbers `0` and `1` are not prime.

---

## Property 2 — 2 Is the Only Even Prime Number

`2` has exactly two factors:

$$
1,2
$$

Therefore:

$$
\boxed{2\text{ is Prime}}
$$

Every other even number is divisible by `2` and therefore has more than two factors.

Examples:

$$
4,6,8,10,12,\ldots
$$

are not prime.

> [!important]
> **2 is the only even prime number.**

---

## Property 3 — Every Prime Greater Than 2 Is Odd

Since every even number greater than `2` is divisible by `2`, it cannot be prime.

Therefore:

$$
\boxed{\text{Prime}>2\Rightarrow Odd}
$$

---

## Property 4 — 1 Is Not Prime

`1` has only one positive factor:

$$
1
$$

A prime number must have exactly two positive factors.

Therefore:

$$
\boxed{1\text{ is Not Prime}}
$$

---

## Property 5 — 0 Is Not Prime

`0` has infinitely many divisors because every non-zero integer divides `0`.

Therefore:

$$
\boxed{0\text{ is Not Prime}}
$$

---

## Property 6 — Negative Numbers Are Not Prime

Prime numbers are defined as positive integers greater than `1`.

Therefore:

$$
-2,-3,-5,-7,\ldots
$$

are not prime.

---

# 4. Main Formula

For an integer $n$:

$$
\boxed{n\text{ is prime if }n>1\text{ and no integer }d\in[2,\sqrt n]\text{ divides }n}
$$

Basic divisibility condition:

$$
n\%d=0
$$

means:

$$
d\text{ divides }n
$$

If such a divisor exists:

$$
\boxed{\text{Not Prime}}
$$

If no divisor exists:

$$
\boxed{\text{Prime}}
$$

---

# 5. Basic Prime Checking

## Example 1

### Question

Is `7` prime?

### Step 1 — Check whether it is greater than 1

$$
7>1
$$

Yes.

### Step 2 — Check possible divisors

We only need to check up to:

$$
\sqrt7\approx2.64
$$

Therefore, check:

$$
2
$$

### Step 3 — Divisibility

$$
7\%2=1
$$

No divisor exists.

### Answer

$$
\boxed{7\text{ is Prime}}
$$

---

# 6. Basic Example — Non-Prime Number

## Example 2

### Question

Is `12` prime?

Possible divisors:

$$
2,3
$$

Check:

$$
12\%2=0
$$

A divisor exists.

Therefore:

$$
\boxed{12\text{ is Not Prime}}
$$

No further checking is necessary.

> [!tip]
> The moment you find one divisor other than `1` and the number itself, stop.

---

# 7. Example — Number 2

## Example 3

### Question

Is `2` prime?

Factors:

$$
1,2
$$

Exactly two factors.

Therefore:

$$
\boxed{2\text{ is Prime}}
$$

---

# 8. Example — Number 1

## Example 4

### Question

Is `1` prime?

Factors:

$$
1
$$

There is only one positive factor.

A prime must have exactly two.

Therefore:

$$
\boxed{1\text{ is Not Prime}}
$$

> [!warning]
> `1` is neither prime nor composite.

---

# 9. Example — Number 0

## Example 5

### Question

Is `0` prime?

Prime numbers must be greater than `1`.

Since:

$$
0\not>1
$$

Therefore:

$$
\boxed{0\text{ is Not Prime}}
$$

---

# 10. Basic Java Program

## Example 6

### Question

Write a Java program to check whether a number is prime.

### Code

    import java.util.Scanner;

    class Main {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            boolean isPrime = true;

            if (n < 2) {
                isPrime = false;
            } else {

                for (int i = 2; i < n; i++) {

                    if (n % i == 0) {
                        isPrime = false;
                        break;
                    }
                }
            }

            if (isPrime) {
                System.out.println("Prime");
            } else {
                System.out.println("Not Prime");
            }
        }
    }

### Logic

    n < 2
    → Not Prime

    otherwise
    → Try divisors from 2 onward

    divisor found
    → Not Prime

    no divisor found
    → Prime

---

# 11. Optimized Prime Check

The previous approach checks:

$$
2,3,4,\ldots,n-1
$$

This is unnecessary.

We only need to check divisors up to:

$$
\sqrt n
$$

### Optimized Code

    import java.util.Scanner;

    class Main {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            boolean isPrime = true;

            if (n < 2) {
                isPrime = false;
            } else {

                for (int i = 2; i * i <= n; i++) {

                    if (n % i == 0) {
                        isPrime = false;
                        break;
                    }
                }
            }

            if (isPrime) {
                System.out.println("Prime");
            } else {
                System.out.println("Not Prime");
            }
        }
    }

### Complexity

Basic method:

$$
\boxed{O(n)}
$$

Optimized method:

$$
\boxed{O(\sqrt n)}
$$

> [!important]
> For coding interviews and placement problems, prefer the $\sqrt n$ method.

---

# 12. Why Check Only Up to √N?

Suppose:

$$
n=a\times b
$$

If both `a` and `b` were greater than:

$$
\sqrt n
$$

then:

$$
a\times b>n
$$

which is impossible.

Therefore, whenever a composite number has a factor greater than $\sqrt n$, it must also have another factor smaller than $\sqrt n$.

### Example

Consider:

$$
36
$$

Factor pairs:

$$
1\times36
$$

$$
2\times18
$$

$$
3\times12
$$

$$
4\times9
$$

$$
6\times6
$$

Since:

$$
\sqrt{36}=6
$$

Once we check up to `6`, all factor pairs are effectively covered.

> [!tip]
> **Prime check shortcut:**
>
> You do not need to test all numbers below $n$.
>
> Stop at:
>
> $$\boxed{\sqrt n}$$

---

# 13. Example — Prime Check Using √N

## Example 7

### Question

Check whether `29` is prime.

### Step 1

$$
29>1
$$

### Step 2

Calculate:

$$
\sqrt{29}\approx5.38
$$

Check:

$$
2,3,4,5
$$

### Step 3

    29 % 2 = 1
    29 % 3 = 2
    29 % 4 = 1
    29 % 5 = 4

No divisor exists.

### Answer

$$
\boxed{29\text{ is Prime}}
$$

---

# 14. Example — Prime Check

## Example 8

### Question

Check whether `49` is prime.

### Step 1

$$
49>1
$$

### Step 2

$$
\sqrt{49}=7
$$

Check divisors:

$$
2,3,4,5,6,7
$$

At:

$$
49\%7=0
$$

A divisor exists.

Therefore:

$$
\boxed{49\text{ is Not Prime}}
$$

---

# 15. Shortcut — Even Number

> [!tip]
> If $n>2$ and `n` is even, immediately conclude:
>
> $$\boxed{\text{Not Prime}}$$
>
> You do not need to perform further checks.

Example:

$$
38
$$

Since `38` is even and greater than `2`:

$$
\boxed{38\text{ is Not Prime}}
$$

---

# 16. Shortcut — Last Digit

For a decimal integer greater than `10`, if its last digit is:

$$
0,2,4,5,6,8
$$

then it is definitely not prime.

Why?

- Last digit `0` → divisible by `10`
- Last digit `2` → even
- Last digit `4` → even
- Last digit `5` → divisible by `5`
- Last digit `6` → even
- Last digit `8` → even

Possible prime-ending digits for numbers greater than `10`:

$$
\boxed{1,3,7,9}
$$

> [!warning]
> A number ending in `1`, `3`, `7`, or `9` is **not automatically prime**.
>
> Example:
>
> $$91=7\times13$$
>
> Therefore, `91` is not prime.

---

# 17. Example — Last Digit Shortcut

## Example 9

### Question

Is `125` prime?

The number ends in `5`.

Since:

$$
125\%5=0
$$

and:

$$
125>5
$$

it is not prime.

### Answer

$$
\boxed{125\text{ is Not Prime}}
$$

---

# 18. Example — Number Ending in 1

## Example 10

### Question

Is `91` prime?

Last digit is `1`.

This means it is only a **candidate** for being prime.

Check:

$$
\sqrt{91}\approx9.54
$$

Test:

$$
91\%7=0
$$

Therefore:

$$
91=7\times13
$$

### Answer

$$
\boxed{91\text{ is Not Prime}}
$$

> [!important]
> Last-digit tests eliminate numbers quickly, but they cannot prove primality by themselves.

---

# 19. Example — Number Ending in 3

## Example 11

### Question

Is `43` prime?

Possible divisors up to:

$$
\sqrt{43}\approx6.55
$$

Check:

$$
2,3,4,5,6
$$

Results:

    43 % 2 = 1
    43 % 3 = 1
    43 % 4 = 3
    43 % 5 = 3
    43 % 6 = 1

No divisor.

### Answer

$$
\boxed{43\text{ is Prime}}
$$

---

# 20. Prime Numbers Less Than 50

The prime numbers less than `50` are:

$$
2,3,5,7,11,13,17,19,23,29,31,37,41,43,47
$$

There are:

$$
\boxed{15}
$$

prime numbers less than `50`.

---

# 21. Prime Numbers Less Than 100

The prime numbers less than `100` are:

$$
2,3,5,7,11,13,17,19
$$

$$
23,29,31,37,41,43,47
$$

$$
53,59,61,67,71,73,79
$$

$$
83,89,97
$$

There are:

$$
\boxed{25}
$$

prime numbers less than `100`.

> [!tip]
> Memorizing small primes is useful for quick aptitude calculations and factorization.

---

# 22. Example — Print Prime Numbers from 1 to N

## Example 12

### Question

Print all prime numbers from `1` to `20`.

### Code

    for (int n = 2; n <= 20; n++) {

        boolean isPrime = true;

        for (int i = 2; i * i <= n; i++) {

            if (n % i == 0) {
                isPrime = false;
                break;
            }
        }

        if (isPrime) {
            System.out.print(n + " ");
        }
    }

### Answer

    2 3 5 7 11 13 17 19

---

# 23. Example — Count Prime Numbers

## Example 13

### Question

Count prime numbers from `1` to `20`.

Prime numbers:

    2 3 5 7 11 13 17 19

Count:

$$
8
$$

### Answer

$$
\boxed{8}
$$

---

# 24. Example — Sum of Prime Numbers

## Example 14

### Question

Find the sum of prime numbers from `1` to `10`.

Prime numbers:

    2 3 5 7

Calculation:

$$
2+3+5+7=17
$$

### Answer

$$
\boxed{17}
$$

---

# 25. Example — Find the Nth Prime

## Example 15

### Question

Find the 5th prime number.

Prime sequence:

| Position | Prime |
|---:|---:|
| 1 | 2 |
| 2 | 3 |
| 3 | 5 |
| 4 | 7 |
| 5 | 11 |

### Answer

$$
\boxed{11}
$$

---

# 26. Pattern Recognition — Prime Check

> [!important]
> **If the question says:**
>
> "Check whether N is prime."
>
> Immediately think:
>
> 1. Is $n<2$?
> 2. Check divisors from `2` to $\sqrt n$.
> 3. Stop immediately when a divisor is found.

Template:

    if (n < 2) {
        // Not Prime
    }

    for (int i = 2; i * i <= n; i++) {

        if (n % i == 0) {
            // Not Prime
        }
    }

---

# 27. Pattern Recognition — Prime in a Range

> [!important]
> **If the question says:**
>
> "Print all primes between L and R."
>
> Think:
>
> **Run a prime-check function for every number in the range.**

Basic structure:

    for (int n = L; n <= R; n++) {

        if (isPrime(n)) {
            System.out.print(n + " ");
        }
    }

For larger constraints, consider a sieve.

---

# 28. Pattern Recognition — Count Primes

> [!important]
> **If the question says:**
>
> "How many primes are there from 1 to N?"
>
> Think:
>
> 1. Iterate through numbers.
> 2. Test primality.
> 3. Increment count when prime.

---

# 29. Pattern Recognition — Sum of Primes

> [!important]
> **If the question says:**
>
> "Find the sum of prime numbers in a range."
>
> Think:
>
>     if (isPrime(n)) {
>         sum += n;
>     }

---

# 30. Pattern Recognition — Prime Factors

> [!important]
> **If the question says:**
>
> "Find prime factors of N."
>
> Think:
>
> Repeatedly divide by the smallest possible divisor.
>
> Check divisors up to $\sqrt n$.
>
> After the loop, if the remaining value is greater than `1`, it is also a prime factor.

Example:

$$
84
$$

Factorization:

$$
84=2\times42
$$

$$
=2\times2\times21
$$

$$
=2\times2\times3\times7
$$

Prime factors:

$$
\boxed{2,3,7}
$$

---

# 31. Example — Prime Factorization

## Example 16

### Question

Find the prime factorization of `60`.

Start with `2`:

$$
60/2=30
$$

Again:

$$
30/2=15
$$

Now divide by `3`:

$$
15/3=5
$$

Remaining:

$$
5
$$

Therefore:

$$
60=2\times2\times3\times5
$$

or:

$$
\boxed{60=2^2\times3\times5}
$$

---

# 32. Example — Prime Factors

## Example 17

### Question

Find the distinct prime factors of `84`.

Prime factorization:

$$
84=2^2\times3\times7
$$

Distinct prime factors:

$$
\boxed{2,3,7}
$$

> [!important]
> "Prime factors" may mean the factors including repetition.
>
> "Distinct prime factors" means list each prime only once.

---

# 33. Prime Factorization Code

### Code

    int n = 84;

    for (int i = 2; i * i <= n; i++) {

        while (n % i == 0) {
            System.out.print(i + " ");
            n /= i;
        }
    }

    if (n > 1) {
        System.out.print(n);
    }

### Output

    2 2 3 7

---

# 34. Distinct Prime Factorization

To print each prime factor only once:

    int n = 84;

    for (int i = 2; i * i <= n; i++) {

        if (n % i == 0) {

            System.out.print(i + " ");

            while (n % i == 0) {
                n /= i;
            }
        }
    }

    if (n > 1) {
        System.out.print(n);
    }

### Output

    2 3 7

---

# 35. Prime vs Composite

A prime number has exactly two positive factors.

A composite number has more than two positive factors.

| Number | Factors | Type |
|---:|---|---|
| 2 | 1, 2 | Prime |
| 3 | 1, 3 | Prime |
| 4 | 1, 2, 4 | Composite |
| 5 | 1, 5 | Prime |
| 6 | 1, 2, 3, 6 | Composite |
| 7 | 1, 7 | Prime |
| 8 | 1, 2, 4, 8 | Composite |
| 9 | 1, 3, 9 | Composite |
| 10 | 1, 2, 5, 10 | Composite |

> [!important]
> `1` is neither prime nor composite.

---

# 36. Example — Prime or Composite

## Example 18

### Question

Classify `17`.

Factors:

$$
1,17
$$

Exactly two.

Therefore:

$$
\boxed{Prime}
$$

---

### Question

Classify `18`.

Factors:

$$
1,2,3,6,9,18
$$

More than two.

Therefore:

$$
\boxed{Composite}
$$

---

# 37. Prime Number Shortcut Table

| Condition | Conclusion |
|---|---|
| $n<2$ | Not Prime |
| $n=2$ | Prime |
| $n>2$ and even | Not Prime |
| $n>2$ and odd | Candidate |
| Divisible by 3 | Not Prime, unless $n=3$ |
| Divisible by 5 | Not Prime, unless $n=5$ |
| No divisor up to $\sqrt n$ | Prime |

> [!warning]
> Being odd is not enough to prove a number is prime.
>
> Example:
>
> $$15,21,25,27,33,39$$
>
> are all odd but composite.

---

# 38. Divisibility Shortcuts for Prime Checking

## Divisibility by 2

Last digit is even:

$$
0,2,4,6,8
$$

---

## Divisibility by 3

Sum of digits is divisible by `3`.

Example:

$$
123
$$

Digit sum:

$$
1+2+3=6
$$

Since:

$$
6\%3=0
$$

`123` is divisible by `3`.

---

## Divisibility by 5

Last digit is:

$$
0\text{ or }5
$$

---

## Divisibility by 7

No simple mental rule is generally as convenient as the rules for `2`, `3`, and `5`, so use direct division when checking primality.

---

## Divisibility by 11

For many aptitude questions, the alternating digit sum rule can be useful.

Example:

$$
121
$$

$$
(1-2+1)=0
$$

Therefore `121` is divisible by `11`.

---

# 39. Example — Eliminate Quickly

## Example 19

### Question

Is `231` prime?

Digit sum:

$$
2+3+1=6
$$

Since:

$$
6\%3=0
$$

and:

$$
231>3
$$

it is divisible by `3`.

Therefore:

$$
\boxed{231\text{ is Not Prime}}
$$

No square-root checking is necessary.

---

# 40. Example — Eliminate by 5

## Example 20

### Question

Is `175` prime?

Last digit:

$$
5
$$

Therefore it is divisible by `5`.

Since:

$$
175>5
$$

it is not prime.

### Answer

$$
\boxed{Not\ Prime}
$$

---

# 41. Advanced Example — Large Candidate

## Example 21

### Question

Check whether `997` is prime.

### Step 1

$$
997>1
$$

### Step 2

Calculate:

$$
\sqrt{997}\approx31.57
$$

Therefore check prime divisors up to `31`:

$$
2,3,5,7,11,13,17,19,23,29,31
$$

None divides `997`.

Therefore:

$$
\boxed{997\text{ is Prime}}
$$

> [!tip]
> When checking primality manually, you only need to test **prime divisors** up to $\sqrt n$.
>
> If a number is not divisible by `2`, checking `4` is unnecessary.
>
> If it is not divisible by `3`, checking `6` is unnecessary.

---

# 42. Optimized Prime Check Using Odd Divisors

After handling `2`, we can check only odd divisors.

### Code

    static boolean isPrime(int n) {

        if (n < 2) {
            return false;
        }

        if (n == 2) {
            return true;
        }

        if (n % 2 == 0) {
            return false;
        }

        for (int i = 3; i * i <= n; i += 2) {

            if (n % i == 0) {
                return false;
            }
        }

        return true;
    }

### Why?

After checking `2`, every even divisor is unnecessary.

Check:

    3, 5, 7, 9, 11, ...

instead of:

    2, 3, 4, 5, 6, 7, ...

This reduces unnecessary checks.

---

# 43. Complexity of Prime Checking

### Method 1 — Check Until N

    for (int i = 2; i < n; i++)

Worst-case complexity:

$$
\boxed{O(n)}
$$

---

### Method 2 — Check Until √N

    for (int i = 2; i * i <= n; i++)

Complexity:

$$
\boxed{O(\sqrt n)}
$$

---

### Method 3 — Check Only Odd Divisors

    for (int i = 3; i * i <= n; i += 2)

Still:

$$
\boxed{O(\sqrt n)}
$$

but with fewer iterations in practice.

---

# 44. Sieve of Eratosthenes

If the problem asks for **many prime queries** or **all primes up to a large N**, checking every number individually may be inefficient.

Use the:

$$
\boxed{\text{Sieve of Eratosthenes}}
$$

### Idea

1. Assume all numbers from `2` to `N` are prime.
2. Start from `2`.
3. Mark all multiples of `2` as non-prime.
4. Move to the next unmarked number.
5. Mark its multiples.
6. Continue up to $\sqrt N$.

### Complexity

Time:

$$
\boxed{O(n\log\log n)}
$$

Space:

$$
\boxed{O(n)}
$$

---

# 45. Sieve Example

## Example 22

### Question

Find all primes up to `20`.

Start:

    2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20

Use `2`:

Mark multiples:

    4 6 8 10 12 14 16 18 20

Use `3`:

Mark:

    6 9 12 15 18

Remaining unmarked numbers:

    2 3 5 7 11 13 17 19

### Answer

$$
\boxed{2,3,5,7,11,13,17,19}
$$

---

# 46. Sieve Java Implementation

### Code

    int n = 20;

    boolean[] isPrime = new boolean[n + 1];

    for (int i = 2; i <= n; i++) {
        isPrime[i] = true;
    }

    for (int i = 2; i * i <= n; i++) {

        if (isPrime[i]) {

            for (int j = i * i; j <= n; j += i) {
                isPrime[j] = false;
            }
        }
    }

    for (int i = 2; i <= n; i++) {

        if (isPrime[i]) {
            System.out.print(i + " ");
        }
    }

### Output

    2 3 5 7 11 13 17 19

> [!important]
> In the sieve, marking can start from:
>
> $$i^2$$
>
> because smaller multiples have already been marked by smaller prime factors.

---

# 47. Advanced Pattern — Prime Count Queries

Suppose you need to answer many questions such as:

    Is 17 prime?
    Is 31 prime?
    Is 97 prime?
    Is 101 prime?
    ...

If the maximum number is known, build a sieve once.

Then each query becomes:

    if (isPrime[x]) {
        // Prime
    }

This gives approximately:

$$
\boxed{O(1)}
$$

per lookup after preprocessing.

---

# 48. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Check Prime

$$
n>1
$$

and test divisors up to:

$$
\sqrt n
$$

---

### Pattern 2 — Print Primes in a Range

Loop through the range and call a prime-check method.

---

### Pattern 3 — Count Primes

Check every number and increment a counter.

---

### Pattern 4 — Sum Primes

Check every number and add it when prime.

---

### Pattern 5 — Prime Factorization

Repeatedly divide by the smallest available divisor.

---

### Pattern 6 — Distinct Prime Factors

When a divisor is found, record it once and divide out all copies.

---

### Pattern 7 — Many Prime Queries

Use:

$$
\boxed{\text{Sieve of Eratosthenes}}
$$

---

### Pattern 8 — Large Candidate Prime

Use:

$$
\boxed{\sqrt n}
$$

and test only relevant divisors.

---

### Pattern 9 — Quick Elimination

Check:

    n < 2
    n == 2
    even
    divisible by 3
    divisible by 5

before performing more checks.

---

# 49. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Calling 1 Prime

Wrong:

$$
1\rightarrow Prime
$$

Correct:

$$
\boxed{1\text{ is neither prime nor composite}}
$$

---

### Mistake 2 — Forgetting 2

Some beginners assume every even number is composite.

Correct:

$$
\boxed{2\text{ is Prime}}
$$

It is the only even prime.

---

### Mistake 3 — Checking Only Whether the Number Is Odd

Wrong reasoning:

    91 is odd
    → therefore prime

Incorrect.

Because:

$$
91=7\times13
$$

Therefore:

$$
\boxed{91\text{ is Composite}}
$$

---

### Mistake 4 — Checking Only Up to N/2

This works for correctness but is unnecessary.

Prefer:

$$
\boxed{\sqrt n}
$$

---

### Mistake 5 — Forgetting to Stop After Finding a Divisor

If:

$$
n\%i=0
$$

then the number is already known to be non-prime.

Use:

    break;

or immediately:

    return false;

---

### Mistake 6 — Checking Every Number in Prime Factorization

Prime factorization can be optimized by dividing repeatedly and reducing `n`.

---

### Mistake 7 — Integer Overflow in `i * i`

For very large integer ranges, this:

    i * i <= n

can overflow.

A safer condition can be:

    i <= n / i

This is especially relevant for larger data types.

---

# 50. Recognition Checklist

> [!important] Must Recognize Quickly

### "Is N prime?"

Think:

$$
\boxed{n<2\Rightarrow Not\ Prime}
$$

Then:

$$
\boxed{2\leq i\leq\sqrt n}
$$

Check:

$$
n\%i
$$

---

### "Print all primes up to N"

Think:

    for each number
    → prime check

For large `N`:

$$
\boxed{\text{Sieve}}
$$

---

### "Count primes"

Think:

    prime check
    +
    counter

---

### "Find prime factors"

Think:

    divide repeatedly
    +
    reduce n

---

### "Find distinct prime factors"

Think:

    record factor once
    +
    divide all copies

---

### "Number ends in 0, 2, 4, 5, 6, 8"

For a number greater than the corresponding small prime:

Think:

$$
\boxed{Not\ Prime}
$$

---

### "Number ends in 1, 3, 7, 9"

Think:

$$
\boxed{Candidate\ Prime}
$$

Not guaranteed.

---

# 51. Formula Sheet

## Definition

$$
\boxed{\text{Prime}\Rightarrow \text{Exactly two positive factors}}
$$

## Basic Condition

$$
\boxed{n>1}
$$

## Prime Test

$$
\boxed{n\%d\neq0\quad\text{for all }2\leq d\leq\sqrt n}
$$

## Optimized Loop

    for (int i = 2; i * i <= n; i++)

## Odd-Divisor Loop

    for (int i = 3; i * i <= n; i += 2)

## Prime Complexity

Basic:

$$
\boxed{O(n)}
$$

Optimized:

$$
\boxed{O(\sqrt n)}
$$

## Sieve Complexity

Time:

$$
\boxed{O(n\log\log n)}
$$

Space:

$$
\boxed{O(n)}
$$

## Smallest Prime

$$
\boxed{2}
$$

## Only Even Prime

$$
\boxed{2}
$$

## Prime Factorization

$$
n=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

where each $p_i$ is prime.

---

# 52. Quick Revision

> [!summary] One-Minute Revision

    Prime number
    → Positive integer greater than 1.
    → Exactly two positive factors.
    → 1 and itself.

    Smallest prime
    → 2.

    Only even prime
    → 2.

    0
    → Not Prime.

    1
    → Neither Prime nor Composite.

    Negative numbers
    → Not Prime.

    Prime check
    → n > 1.
    → Test divisors up to √n.

    Divisor condition
    → n % i == 0.

    Divisor found
    → Not Prime.
    → Stop immediately.

    No divisor found
    → Prime.

    Even number greater than 2
    → Not Prime.

    Number ending in 0, 2, 4, 5, 6, 8
    → Usually immediately composite for numbers greater
      than the corresponding small prime.

    Number ending in 1, 3, 7, 9
    → Candidate only, not guaranteed prime.

    Prime greater than 2
    → Always odd.

    Prime checking complexity
    → O(√n).

    Many prime queries
    → Sieve of Eratosthenes.

    Prime factorization
    → Repeated division.

    Distinct prime factors
    → Record each factor once.

    Important small primes
    → 2, 3, 5, 7, 11, 13, 17, 19, 23, 29.

    Main coding pattern
    → Check n % i == 0.

    Main optimization
    → Stop at √n.

---

## Golden Memory Trick

**A prime number has exactly two factors, and to prove it is prime, you only need to search for a divisor up to √N.**

## One-Line Recognition

**When you see "check, count, print, or find primes," think `n > 1` followed by divisor checks up to `√n`.**