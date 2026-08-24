---
type: concept
subject: coding
topic: "Digit Frequency"
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
  - digit-frequency
  - java
  - frequency-counting
wikilinks:
  - "[[Digit Problems]]"
  - "[[Count Digits]]"
  - "[[Sum of Digits]]"
  - "[[Reverse Number]]"
  - "[[Frequency Counting]]"
---

# Digit Frequency

## 1. Core Concept

> [!summary]
> **Digit Frequency** means counting how many times each digit from `0` to `9` occurs in a number.
>
> Example:
>
> $$1223334$$
>
> Frequencies:
>
> $$1\rightarrow1$$
>
> $$2\rightarrow2$$
>
> $$3\rightarrow3$$
>
> $$4\rightarrow1$$
>
> Therefore:
>
> $$\boxed{1:1,\ 2:2,\ 3:3,\ 4:1}$$

The key coding idea is:

**Extract each digit using `% 10` → increment its frequency → remove the digit using `/ 10`.**

---

# 2. Basic Meaning

Every decimal number contains digits from:

$$
0,1,2,3,4,5,6,7,8,9
$$

Digit frequency tells us how many times each digit appears.

### Example

For:

$$
112233
$$

we have:

| Digit | Frequency |
|---:|---:|
| 0 | 0 |
| 1 | 2 |
| 2 | 2 |
| 3 | 2 |
| 4 | 0 |
| 5 | 0 |
| 6 | 0 |
| 7 | 0 |
| 8 | 0 |
| 9 | 0 |

Therefore:

$$
\boxed{1\rightarrow2,\ 2\rightarrow2,\ 3\rightarrow2}
$$

---

# 3. Main Formula

For every extracted digit:

$$
\boxed{digit=N\%10}
$$

Then increment its frequency:

$$
\boxed{freq[digit]++}
$$

Then remove the digit:

$$
\boxed{N=\lfloor N/10\rfloor}
$$

The complete pattern is:

    while (n > 0) {

        int digit = n % 10;

        freq[digit]++;

        n /= 10;
    }

---

# 4. Important Properties

## Property 1 — There Are Only 10 Possible Digits

For decimal numbers:

$$
\boxed{0\leq digit\leq9}
$$

Therefore, an array of size `10` is enough:

    int[] freq = new int[10];

Indexes:

    0 1 2 3 4 5 6 7 8 9

---

## Property 2 — Digit Becomes the Array Index

If:

$$
digit=7
$$

then:

    freq[7]++;

If:

$$
digit=2
$$

then:

    freq[2]++;

Therefore:

$$
\boxed{freq[digit]++}
$$

is the core operation.

---

## Property 3 — Total Frequencies Equal Number of Digits

For:

$$
122333
$$

frequencies are:

$$
1+2+3=6
$$

The number has:

$$
6
$$

digits.

Therefore:

$$
\boxed{\sum freq[d]=\text{number of digits}}
$$

---

## Property 4 — Repeated Digits Are Counted Automatically

For:

$$
55555
$$

every extracted digit is:

$$
5
$$

Therefore:

$$
freq[5]=5
$$

---

## Property 5 — Zero Needs Special Handling

For integer input:

$$
0
$$

the normal loop:

    while (n > 0)

does not execute.

But `0` itself is one digit.

Therefore:

$$
\boxed{freq[0]=1}
$$

must be handled separately if zero is a valid input.

---

# 5. Basic Example — 112233

## Example 1

### Question

Find the frequency of every digit in `112233`.

Extract digits:

$$
3,3,2,2,1,1
$$

Update frequencies:

$$
freq[3]=2
$$

$$
freq[2]=2
$$

$$
freq[1]=2
$$

Therefore:

$$
\boxed{1\rightarrow2,\ 2\rightarrow2,\ 3\rightarrow2}
$$

All other digits have frequency:

$$
0
$$

---

# 6. Basic Example — 12345

## Example 2

### Question

Find the frequency of each digit in `12345`.

Every digit occurs once.

| Digit | Frequency |
|---:|---:|
| 0 | 0 |
| 1 | 1 |
| 2 | 1 |
| 3 | 1 |
| 4 | 1 |
| 5 | 1 |
| 6 | 0 |
| 7 | 0 |
| 8 | 0 |
| 9 | 0 |

Therefore:

$$
\boxed{1:1,\ 2:1,\ 3:1,\ 4:1,\ 5:1}
$$

---

# 7. Basic Example — 99999

## Example 3

### Question

Find the frequency of each digit in `99999`.

Only digit `9` occurs.

There are five `9`s.

Therefore:

$$
\boxed{freq[9]=5}
$$

All other frequencies are:

$$
0
$$

---

# 8. Basic Example — 10001

## Example 4

### Question

Find the digit frequencies of `10001`.

Digits:

$$
1,0,0,0,1
$$

Frequency:

$$
freq[0]=3
$$

$$
freq[1]=2
$$

Therefore:

$$
\boxed{0:3,\ 1:2}
$$

---

# 9. Basic Example — Zero

## Example 5

### Question

Find the frequency of digits in `0`.

The number contains one digit:

$$
0
$$

Therefore:

$$
\boxed{freq[0]=1}
$$

> [!warning]
> Do not let the loop alone handle `0`, because `while (n > 0)` executes zero times.

---

# 10. Standard Java Program

## Example 6

### Question

Write a Java program to count the frequency of every digit in an integer.

### Code

    import java.util.Scanner;

    class Main {

        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);

            int n = sc.nextInt();

            n = Math.abs(n);

            int[] freq = new int[10];

            if (n == 0) {

                freq[0] = 1;

            } else {

                while (n > 0) {

                    int digit = n % 10;

                    freq[digit]++;

                    n /= 10;
                }
            }

            for (int i = 0; i <= 9; i++) {

                if (freq[i] > 0) {
                    System.out.println(i + " : " + freq[i]);
                }
            }
        }
    }

---

# 11. Reusable Function

## Example 7

### Code

    static int[] digitFrequency(int n) {

        n = Math.abs(n);

        int[] freq = new int[10];

        if (n == 0) {
            freq[0] = 1;
            return freq;
        }

        while (n > 0) {

            int digit = n % 10;

            freq[digit]++;

            n /= 10;
        }

        return freq;
    }

For:

    digitFrequency(122333)

the result is:

$$
freq[1]=1
$$

$$
freq[2]=2
$$

$$
freq[3]=3
$$

---

# 12. Pattern Recognition — Digit Frequency

> [!important]
> **If the question asks "How many times does each digit occur?"**
>
> Immediately think:
>
>     int[] freq = new int[10];
>
>     while (n > 0) {
>         int digit = n % 10;
>         freq[digit]++;
>         n /= 10;
>     }
>
> The key formula is:
>
> $$\boxed{freq[digit]++}
> $$

---

# 13. Pattern Recognition — Count One Specific Digit

If the question asks:

**"How many times does digit `5` occur?"**

You do not need to store all frequencies.

Use:

    int count = 0;

    while (n > 0) {

        int digit = n % 10;

        if (digit == 5) {
            count++;
        }

        n /= 10;
    }

Therefore:

$$
\boxed{\text{Count only the required digit}}
$$

---

# 14. Example — Count Digit 2

## Example 8

### Question

How many times does `2` occur in `1223242`?

Extract:

$$
1,2,2,3,2,4,2
$$

Occurrences of `2`:

$$
4
$$

Therefore:

$$
\boxed{4}
$$

---

# 15. Pattern Recognition — Most Frequent Digit

> [!important]
> If the question asks:
>
> **"Which digit occurs the most?"**
>
> Think:
>
> 1. Build `freq[10]`.
> 2. Traverse digits `0` to `9`.
> 3. Find the maximum frequency.
>
> Pattern:
>
>     int maxFreq = 0;
>     int answer = 0;
>
>     for (int digit = 0; digit <= 9; digit++) {
>         if (freq[digit] > maxFreq) {
>             maxFreq = freq[digit];
>             answer = digit;
>         }
>     }

---

# 16. Example — Most Frequent Digit

## Example 9

### Question

Find the most frequent digit in `1223334444`.

Frequencies:

| Digit | Frequency |
|---:|---:|
| 1 | 1 |
| 2 | 2 |
| 3 | 3 |
| 4 | 4 |

Maximum:

$$
4
$$

Therefore:

$$
\boxed{\text{Most frequent digit}=4}
$$

---

# 17. Pattern Recognition — Least Frequent Digit

> [!important]
> If the question asks:
>
> **"Which digit occurs the least among the digits present?"**
>
> Ignore digits whose frequency is `0`.
>
> Then find the minimum positive frequency.
>
> Example:
>
>     1122333
>
> Frequencies:
>
>     1 → 2
>     2 → 2
>     3 → 3
>
> Minimum positive frequency:
>
> $$2$$
>
> Therefore digits `1` and `2` are least frequent.

---

# 18. Example — Least Frequent Digit

## Example 10

### Question

Find the least frequent digit in `111223333`.

Frequencies:

$$
1\rightarrow3
$$

$$
2\rightarrow2
$$

$$
3\rightarrow4
$$

Minimum:

$$
2
$$

Therefore:

$$
\boxed{\text{Least frequent digit}=2}
$$

---

# 19. Pattern Recognition — Unique Digit

A digit is **unique** if its frequency is exactly:

$$
1
$$

> [!important]
> If the question says:
>
> **"Find digits that occur only once."**
>
> Build the frequency array and check:
>
>     freq[digit] == 1

---

# 20. Example — Unique Digits

## Example 11

### Question

Find the digits that occur exactly once in `1123455`.

Frequencies:

$$
1\rightarrow2
$$

$$
2\rightarrow1
$$

$$
3\rightarrow1
$$

$$
4\rightarrow1
$$

$$
5\rightarrow2
$$

Therefore unique digits are:

$$
\boxed{2,3,4}
$$

---

# 21. Pattern Recognition — Duplicate Digits

A digit is duplicated if:

$$
freq[digit]>1
$$

> [!important]
> If the question says:
>
> **"Find repeated digits."**
>
> Think:
>
> $$\boxed{freq[digit]>1}
> $$

---

# 22. Example — Duplicate Digits

## Example 12

### Question

Find duplicate digits in `12233456`.

Frequencies:

$$
1\rightarrow1
$$

$$
2\rightarrow2
$$

$$
3\rightarrow2
$$

$$
4\rightarrow1
$$

$$
5\rightarrow1
$$

$$
6\rightarrow1
$$

Therefore:

$$
\boxed{2,3}
$$

are duplicate digits.

---

# 23. Pattern Recognition — Check if All Digits Are Unique

> [!important]
> If every digit occurs at most once:
>
> $$\boxed{freq[digit]\leq1}
> $$
>
> Example:
>
> `123456`
>
> All frequencies are `1`.
>
> Therefore:
>
> $$\boxed{\text{All digits are unique}}
> $$

---

# 24. Example — All Digits Unique

## Example 13

### Question

Check whether `123456789` contains repeated digits.

Every digit occurs once.

Therefore:

$$
\boxed{\text{Yes, all digits are unique}}
$$

---

# 25. Example — Repeated Digit Exists

## Example 14

### Question

Check whether `123452` contains a repeated digit.

Digit `2` occurs twice.

Therefore:

$$
\boxed{\text{Repeated digit exists}}
$$

---

# 26. Pattern Recognition — Frequency of Digits in Two Numbers

Sometimes the question asks whether two numbers contain the same digits with the same frequencies.

> [!important]
> Build:

    freq1[10]

and:

    freq2[10]

Then compare:

    freq1[i] == freq2[i]

for every:

$$
0\leq i\leq9
$$

This is useful for **digit-anagram** problems.

---

# 27. Example — Same Digit Frequencies

## Example 15

### Question

Check whether `112233` and `332211` contain the same digit frequencies.

First number:

$$
1\rightarrow2,\ 2\rightarrow2,\ 3\rightarrow2
$$

Second number:

$$
1\rightarrow2,\ 2\rightarrow2,\ 3\rightarrow2
$$

All frequencies match.

Therefore:

$$
\boxed{\text{Yes}}
$$

---

# 28. Example — Different Digit Frequencies

## Example 16

### Question

Check whether `112233` and `112234` have the same digit frequencies.

First:

$$
1\rightarrow2,\ 2\rightarrow2,\ 3\rightarrow2
$$

Second:

$$
1\rightarrow2,\ 2\rightarrow2,\ 3\rightarrow1,\ 4\rightarrow1
$$

Frequencies differ.

Therefore:

$$
\boxed{\text{No}}
$$

---

# 29. Frequency Array Visualization

For number:

$$
1223334
$$

the array looks like:

| Index | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Frequency | 0 | 1 | 2 | 3 | 1 | 0 | 0 | 0 | 0 | 0 |

The index represents the digit.

The value represents how many times it occurs.

Therefore:

$$
\boxed{freq[digit]=\text{occurrence count}}
$$

---

# 30. Why Array Size 10?

Decimal digits are only:

$$
0\text{ through }9
$$

Therefore:

$$
10
$$

positions are enough.

    int[] freq = new int[10];

Indexes:

    0 → digit 0
    1 → digit 1
    2 → digit 2
    ...
    9 → digit 9

> [!tip]
> Whenever the possible values are a small fixed range, an array is often faster and simpler than a `HashMap`.

---

# 31. Frequency Array vs HashMap

| Situation | Recommended |
|---|---|
| Digits `0–9` | Array |
| Lowercase letters `a–z` | Array |
| Arbitrary integers | HashMap |
| Unknown large value range | HashMap |
| Fixed small range | Array |

For digit frequency:

$$
\boxed{\text{Array of size 10}}
$$

is usually the cleanest solution.

---

# 32. Example — Frequency Using HashMap

Although an array is preferable for digits, a `HashMap` can also be used.

### Code

    import java.util.HashMap;

    static HashMap<Integer, Integer> digitFrequency(int n) {

        HashMap<Integer, Integer> map = new HashMap<>();

        n = Math.abs(n);

        if (n == 0) {
            map.put(0, 1);
            return map;
        }

        while (n > 0) {

            int digit = n % 10;

            map.put(digit, map.getOrDefault(digit, 0) + 1);

            n /= 10;
        }

        return map;
    }

> [!important]
> For only digits `0–9`, the array approach is simpler and more efficient.

---

# 33. Example — Find Maximum Frequency

## Example 17

### Question

Find the maximum frequency in `112223333`.

Frequencies:

$$
1\rightarrow2
$$

$$
2\rightarrow3
$$

$$
3\rightarrow4
$$

Maximum:

$$
4
$$

Therefore:

$$
\boxed{4}
$$

---

# 34. Example — Count Distinct Digits

## Example 18

### Question

How many distinct digits occur in `1122334455`?

Distinct digits:

$$
1,2,3,4,5
$$

Therefore:

$$
\boxed{5}
$$

### Frequency Approach

Count digits where:

$$
freq[digit]>0
$$

---

# 35. Example — Distinct Digits

## Example 19

### Question

Find the number of distinct digits in `123455678`.

Frequencies:

- `1` → 1
- `2` → 1
- `3` → 1
- `4` → 1
- `5` → 2
- `6` → 1
- `7` → 1
- `8` → 1

Distinct digits:

$$
1,2,3,4,5,6,7,8
$$

Therefore:

$$
\boxed{8}
$$

---

# 36. Example — Digit With Maximum Frequency and Tie

## Example 20

### Question

Find the most frequent digit in `112233`.

Frequencies:

$$
1\rightarrow2
$$

$$
2\rightarrow2
$$

$$
3\rightarrow2
$$

There is a tie.

If the problem asks for the **smallest digit among ties**, answer:

$$
\boxed{1}
$$

If it asks for the **largest digit among ties**, answer:

$$
\boxed{3}
$$

> [!warning]
> Always check the tie-breaking condition.

---

# 37. Tie-Breaking Pattern

Suppose:

    freq[1] = 3
    freq[2] = 3
    freq[3] = 1

For smallest digit among maximum-frequency digits:

    for (int i = 0; i <= 9; i++) {
        if (freq[i] > maxFreq) {
            maxFreq = freq[i];
            answer = i;
        }
    }

Because digits are traversed from `0` to `9`, the first maximum is retained.

Therefore:

$$
\boxed{1}
$$

For largest digit among ties, traverse from:

$$
9\rightarrow0
$$

---

# 38. Advanced Example — Find First Non-Repeating Digit

## Example 21

### Question

Find the first digit that occurs exactly once in `112345533`.

Frequencies:

$$
1\rightarrow2
$$

$$
2\rightarrow1
$$

$$
3\rightarrow3
$$

$$
4\rightarrow1
$$

$$
5\rightarrow2
$$

The first digit in the original number with frequency `1` is:

$$
2
$$

Therefore:

$$
\boxed{2}
$$

> [!important]
> "First non-repeating" means preserve the original order.
>
> Frequency alone is not enough; perform a second traversal.

---

# 39. First Non-Repeating Pattern

> [!important]
> If the question says:
>
> **"Find the first digit that occurs only once."**
>
> Use two passes:
>
> **Pass 1**
>
> Build frequency.
>
> **Pass 2**
>
> Traverse the original digits again.
>
> Return the first digit where:
>
> $$freq[digit]==1
> $$

---

# 40. Advanced Example — First Repeating Digit

## Example 22

### Question

Find the first digit that repeats in `1234526`.

Frequencies show:

$$
2\rightarrow2
$$

Now traverse from the beginning:

    1 → frequency 1
    2 → frequency 2

Therefore the first repeating digit is:

$$
\boxed{2}
$$

---

# 41. Common Exam Pattern — Digit Frequency

> [!important] Must Master

### Pattern 1 — Frequency of Every Digit

    int[] freq = new int[10];

    while (n > 0) {
        int digit = n % 10;
        freq[digit]++;
        n /= 10;
    }

### Pattern 2 — Count One Digit

    if (digit == target) {
        count++;
    }

### Pattern 3 — Most Frequent Digit

Find maximum `freq[digit]`.

### Pattern 4 — Least Frequent Digit

Find minimum positive `freq[digit]`.

### Pattern 5 — Unique Digit

Check:

    freq[digit] == 1

### Pattern 6 — Duplicate Digit

Check:

    freq[digit] > 1

### Pattern 7 — Distinct Digit Count

Count:

    freq[digit] > 0

### Pattern 8 — Same Digit Frequencies

Compare two frequency arrays.

### Pattern 9 — First Non-Repeating Digit

Build frequency, then traverse original digits.

### Pattern 10 — First Repeating Digit

Build frequency, then find the first digit with:

    freq[digit] > 1

---

# 42. Shortcuts

> [!tip]
> **Shortcut 1 — Fixed Digit Range**
>
> Since there are only `10` digits:
>
> $$\boxed{int[10]}
> $$
>
> is enough.

> [!tip]
> **Shortcut 2 — Frequency Operation**
>
> Memorize:
>
> $$\boxed{freq[digit]++}
> $$

> [!tip]
> **Shortcut 3 — Unique**
>
> Frequency exactly `1`:
>
> $$\boxed{freq[digit]=1}
> $$

> [!tip]
> **Shortcut 4 — Duplicate**
>
> Frequency greater than `1`:
>
> $$\boxed{freq[digit]>1}
> $$

> [!tip]
> **Shortcut 5 — Distinct**
>
> Frequency greater than `0`:
>
> $$\boxed{freq[digit]>0}
> $$

> [!tip]
> **Shortcut 6 — Maximum Frequency**
>
> Track:
>
> $$\boxed{maxFreq}
> $$
>
> while scanning digits `0–9`.

> [!tip]
> **Shortcut 7 — Tie Breaking**
>
> Traverse from `0 → 9` for smallest digit on ties.
>
> Traverse from `9 → 0` for largest digit on ties.

---

# 43. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Using Frequency Array of Wrong Size

Wrong:

    int[] freq = new int[9];

Correct:

    int[] freq = new int[10];

Valid digit indexes are:

$$
0\text{ through }9
$$

---

### Mistake 2 — Using the Digit as a Value Instead of an Index

Wrong:

    freq++;

Correct:

    freq[digit]++;

---

### Mistake 3 — Forgetting to Remove the Digit

Without:

    n /= 10;

the loop does not progress.

---

### Mistake 4 — Missing Zero Input

For:

$$
n=0
$$

the loop:

    while (n > 0)

does not execute.

Handle zero separately.

---

### Mistake 5 — Counting Zero-Frequency Digits as Least Frequent

Suppose:

    112233

Digit `4` has frequency:

$$
0
$$

It should not be considered the least frequent **present** digit.

Use:

$$
freq[digit]>0
$$

before checking the minimum.

---

### Mistake 6 — Losing Original Order

Frequency tells how many times a digit occurs, but not where it occurs.

For:

**first non-repeating digit**, perform another traversal of the original number.

---

### Mistake 7 — Ignoring Tie Conditions

If multiple digits have the same maximum frequency, the answer depends on the question:

- Smallest digit?
- Largest digit?
- First appearing digit?

Do not assume.

---

### Mistake 8 — Forgetting Negative Input

If the sign should be ignored:

    n = Math.abs(n);

But follow the exact problem statement.

---

# 44. Time and Space Complexity

Let:

$$
d=\text{number of digits}
$$

Each digit is processed once.

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

The frequency array always has size `10`.

Therefore its extra space is:

$$
\boxed{O(1)}
$$

because `10` is constant.

---

# 45. Frequency Array vs HashMap Complexity

| Method | Time | Extra Space | Best For |
|---|---:|---:|---|
| Array of 10 | $O(d)$ | $O(1)$ | Digits |
| HashMap | $O(d)$ average | $O(k)$ | General values |
| Sorting | $O(d\log d)$ | Depends | Usually unnecessary |

> [!important]
> For digits, use the fixed-size array unless the problem specifically requires another structure.

---

# 46. Recognition Checklist

> [!important] Must Recognize Quickly

**"How many times does each digit occur?"**

Think:

$$
\boxed{freq[10]}
$$

---

**"How many times does digit X occur?"**

Think:

$$
\boxed{digit==X}
$$

---

**"Most frequent digit."**

Think:

$$
\boxed{\max(freq)}
$$

---

**"Least frequent present digit."**

Think:

$$
\boxed{\min(freq[digit]>0)}
$$

---

**"Digit occurs only once."**

Think:

$$
\boxed{freq[digit]=1}
$$

---

**"Repeated digit."**

Think:

$$
\boxed{freq[digit]>1}
$$

---

**"Number of distinct digits."**

Think:

$$
\boxed{freq[digit]>0}
$$

---

**"Same digits with same counts."**

Think:

$$
\boxed{\text{Compare frequency arrays}}
$$

---

**"First non-repeating digit."**

Think:

$$
\boxed{\text{Frequency + second traversal}}
$$

---

**"First repeating digit."**

Think:

$$
\boxed{\text{Frequency + original order}}
$$

---

# 47. Formula Sheet

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

## Update Frequency

$$
\boxed{
freq[digit]++
}
$$

## Unique Digit

$$
\boxed{
freq[digit]=1
}
$$

## Duplicate Digit

$$
\boxed{
freq[digit]>1
}
$$

## Present Digit

$$
\boxed{
freq[digit]>0
}
$$

## Number of Possible Decimal Digits

$$
\boxed{10}
$$

## Frequency Array

$$
\boxed{
int[]\ freq=new\ int[10]
}
$$

## Time Complexity

$$
\boxed{O(\log N)}
$$

## Space Complexity

$$
\boxed{O(1)}
$$

---

# 48. Quick Revision

> [!summary] One-Minute Revision

    Digit Frequency
    → Count how many times each digit 0–9 occurs.

    Core structure
    → int[] freq = new int[10]

    Extract digit
    → digit = n % 10

    Increment frequency
    → freq[digit]++

    Remove digit
    → n /= 10

    Example
    → 122333
    → 1 occurs 1 time
    → 2 occurs 2 times
    → 3 occurs 3 times

    Unique digit
    → freq[digit] == 1

    Duplicate digit
    → freq[digit] > 1

    Present digit
    → freq[digit] > 0

    Most frequent
    → Maximum frequency.

    Least frequent
    → Minimum positive frequency.

    Distinct count
    → Count frequencies greater than 0.

    First non-repeating
    → Frequency + second traversal.

    Same digit frequencies
    → Compare two frequency arrays.

    Zero
    → Handle separately when input is exactly 0.

    Decimal digits
    → Only 0–9, so array size 10 is enough.

    Complexity
    → O(log N).

    Space
    → O(1).

---

## Golden Memory Trick

**For every digit, use `%10` to identify it and `freq[digit]++` to remember how many times it appears.**

## One-Line Recognition

**When a problem asks about how often digits occur, immediately think `int[10]` + `%10` + `freq[digit]++`.**