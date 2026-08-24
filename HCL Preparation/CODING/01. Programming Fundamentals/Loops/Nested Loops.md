---
type: concept
subject: coding
topic: "Nested Loops"
parent: "Loops"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - loops
  - nested-loops
  - java
  - pattern-printing
  - matrix
  - time-complexity
wikilinks:
  - "[[Loops]]"
  - "[[for Loop]]"
  - "[[while Loop]]"
  - "[[do while Loop]]"
  - "[[Arrays]]"
  - "[[Matrix]]"
---

# Nested Loops

## 1. Core Concept

> [!summary]
> A **nested loop** is a loop placed inside another loop.
>
> The outer loop controls the main repetition, while the inner loop performs repeated work for every outer-loop iteration.
>
> The most important rule is:
>
> **For every one execution of the outer loop, the inner loop runs completely.**

Basic structure:

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < m; j++) {
            // work
        }
    }

Example:

    for (int i = 1; i <= 3; i++) {

        for (int j = 1; j <= 2; j++) {
            System.out.println(i + " " + j);
        }
    }

Output:

    1 1
    1 2
    2 1
    2 2
    3 1
    3 2

Total inner-loop executions:

$$
3\times2=6
$$

---

## 2. Basic Meaning

Think of nested loops as:

    Outer loop
        ↓
    Inner loop runs completely
        ↓
    Outer loop moves once
        ↓
    Inner loop runs completely again

If the outer loop executes $n$ times and the inner loop executes $m$ times for each outer iteration:

$$
\text{Total iterations}=n\times m
$$

Therefore:

$$
\boxed{O(nm)}
$$

If both loops run $n$ times:

$$
\boxed{O(n^2)}
$$

---

## 3. Why Nested Loops Are Important

Nested loops are commonly used for:

- Pattern printing
- Matrix traversal
- 2D arrays
- Row and column operations
- Comparing every pair
- Generating combinations
- Brute-force solutions
- Searching a grid
- Multiplication tables
- Subarray generation
- String comparisons
- Coordinate-based problems
- Simulations

> [!important]
> If a problem involves **rows and columns**, **every pair**, **every combination**, or **repeated work for each element**, consider nested loops.

---

## 4. Basic Structure

### Outer Loop

    for (int i = 0; i < n; i++) {
        // work
    }

### Inner Loop

    for (int j = 0; j < m; j++) {
        // work
    }

### Nested Loop

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < m; j++) {
            // work
        }
    }

If:

$$
i=0,1,2,\ldots,n-1
$$

and for every `i`:

$$
j=0,1,2,\ldots,m-1
$$

then:

$$
\boxed{n\times m}
$$

operations are performed.

---

## 5. Execution Order

Consider:

    for (int i = 1; i <= 2; i++) {

        for (int j = 1; j <= 3; j++) {
            System.out.println(i + " " + j);
        }
    }

When `i = 1`:

    j = 1
    j = 2
    j = 3

Output:

    1 1
    1 2
    1 3

When `i = 2`:

    j = 1
    j = 2
    j = 3

Output:

    2 1
    2 2
    2 3

Final output:

    1 1
    1 2
    1 3
    2 1
    2 2
    2 3

Total:

$$
2\times3=6
$$

---

## 6. Basic Example — Rectangle Pattern

### Question

Print a rectangle containing 3 rows and 4 columns.

### Pattern

    * * * *
    * * * *
    * * * *

### Recognition

Rows:

$$
3
$$

Columns:

$$
4
$$

Therefore, use nested loops.

### Code

    for (int i = 1; i <= 3; i++) {

        for (int j = 1; j <= 4; j++) {
            System.out.print("* ");
        }

        System.out.println();
    }

### Number of Stars

$$
3\times4=12
$$

### Answer

$$
\boxed{12\ stars}
$$

---

## 7. Basic Example — Square Pattern

### Question

Print a `4 × 4` square.

### Code

    for (int i = 1; i <= 4; i++) {

        for (int j = 1; j <= 4; j++) {
            System.out.print("* ");
        }

        System.out.println();
    }

### Output

    * * * *
    * * * *
    * * * *
    * * * *

Total stars:

$$
4\times4=16
$$

### Answer

$$
\boxed{16}
$$

---

## 8. Example — Increasing Star Triangle

### Question

Print:

    *
    * *
    * * *
    * * * *
    * * * * *

### Recognition

For row `i`, print exactly `i` stars.

### Code

    for (int i = 1; i <= 5; i++) {

        for (int j = 1; j <= i; j++) {
            System.out.print("* ");
        }

        System.out.println();
    }

### Row Analysis

| Row | Stars |
|---:|---:|
| 1 | 1 |
| 2 | 2 |
| 3 | 3 |
| 4 | 4 |
| 5 | 5 |

Total:

$$
1+2+3+4+5
$$

$$
=\frac{5(6)}{2}
$$

$$
=15
$$

### Answer

$$
\boxed{15\ stars}
$$

---

## 9. Example — Decreasing Star Triangle

### Question

Print:

    * * * * *
    * * * *
    * * *
    * *
    *

### Code

    for (int i = 5; i >= 1; i--) {

        for (int j = 1; j <= i; j++) {
            System.out.print("* ");
        }

        System.out.println();
    }

### Total Stars

$$
5+4+3+2+1=15
$$

### Answer

$$
\boxed{15}
$$

---

## 10. Example — Number Triangle

### Question

Print:

    1
    1 2
    1 2 3
    1 2 3 4
    1 2 3 4 5

### Pattern

For row `i`, print numbers from `1` to `i`.

### Code

    for (int i = 1; i <= 5; i++) {

        for (int j = 1; j <= i; j++) {
            System.out.print(j + " ");
        }

        System.out.println();
    }

### Answer

    1
    1 2
    1 2 3
    1 2 3 4
    1 2 3 4 5

> [!important]
> If the number of elements in a row equals the row number, think:
>
> $$j\leq i$$

---

## 11. Example — Repeated Row Number

### Question

Print:

    1
    2 2
    3 3 3
    4 4 4 4
    5 5 5 5 5

### Code

    for (int i = 1; i <= 5; i++) {

        for (int j = 1; j <= i; j++) {
            System.out.print(i + " ");
        }

        System.out.println();
    }

### Answer

    1
    2 2
    3 3 3
    4 4 4 4
    5 5 5 5 5

---

## 12. Example — Continuous Number Pattern

### Question

Print:

    1
    2 3
    4 5 6
    7 8 9 10

### Pattern

The number must continue across rows.

Use a separate counter.

### Code

    int value = 1;

    for (int i = 1; i <= 4; i++) {

        for (int j = 1; j <= i; j++) {
            System.out.print(value + " ");
            value++;
        }

        System.out.println();
    }

### Answer

    1
    2 3
    4 5 6
    7 8 9 10

> [!tip]
> If a value must continue across rows, keep its counter outside the inner loop.

---

## 13. Example — Multiplication Table Grid

### Question

Print multiplication values from `1 × 1` to `5 × 5`.

### Code

    for (int i = 1; i <= 5; i++) {

        for (int j = 1; j <= 5; j++) {
            System.out.print((i * j) + "\t");
        }

        System.out.println();
    }

### Output

    1    2    3    4    5
    2    4    6    8    10
    3    6    9    12   15
    4    8    12   16   20
    5    10   15   20   25

Total calculations:

$$
5\times5=25
$$

### Answer

$$
\boxed{25}
$$

---

## 14. Example — Matrix Traversal

### Question

Print every element of:

    1 2 3
    4 5 6
    7 8 9

### Recognition

For a matrix:

    i → row
    j → column

### Code

    int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {
            System.out.print(matrix[i][j] + " ");
        }

        System.out.println();
    }

### Answer

    1 2 3
    4 5 6
    7 8 9

> [!important]
> For a 2D array:
>
> `i` → row
>
> `j` → column

---

## 15. Example — Matrix Sum

### Question

Find the sum of all elements:

    1 2 3
    4 5 6
    7 8 9

### Code

    int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int sum = 0;

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {
            sum += matrix[i][j];
        }
    }

    System.out.println(sum);

### Calculation

$$
1+2+3+4+5+6+7+8+9=45
$$

### Answer

$$
\boxed{45}
$$

---

## 16. Example — Maximum Element in Matrix

### Question

Find the maximum element:

    3 8 2
    9 1 5
    4 7 6

### Code

    int[][] matrix = {
        {3, 8, 2},
        {9, 1, 5},
        {4, 7, 6}
    };

    int max = matrix[0][0];

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {

            if (matrix[i][j] > max) {
                max = matrix[i][j];
            }
        }
    }

    System.out.println(max);

### Answer

$$
\boxed{9}
$$

---

## 17. Example — Count Even Numbers in Matrix

### Question

Count the even numbers:

    1 2 3
    4 5 6
    7 8 9

### Code

    int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int count = 0;

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {

            if (matrix[i][j] % 2 == 0) {
                count++;
            }
        }
    }

    System.out.println(count);

Even numbers:

    2, 4, 6, 8

### Answer

$$
\boxed{4}
$$

---

## 18. Example — Compare Every Pair

### Question

Print every possible ordered pair from:

    1 2 3

### Code

    int[] arr = {1, 2, 3};

    for (int i = 0; i < arr.length; i++) {

        for (int j = 0; j < arr.length; j++) {
            System.out.println(arr[i] + " " + arr[j]);
        }
    }

### Output

    1 1
    1 2
    1 3
    2 1
    2 2
    2 3
    3 1
    3 2
    3 3

Total:

$$
3\times3=9
$$

### Answer

$$
\boxed{9\ pairs}
$$

---

## 19. Example — Unique Pairs

### Question

Print every unique pair from:

    1 2 3

Expected:

    1 2
    1 3
    2 3

### Pattern

Start the inner loop from:

$$
j=i+1
$$

### Code

    int[] arr = {1, 2, 3};

    for (int i = 0; i < arr.length; i++) {

        for (int j = i + 1; j < arr.length; j++) {
            System.out.println(arr[i] + " " + arr[j]);
        }
    }

### Answer

    1 2
    1 3
    2 3

Number of unique pairs:

$$
\frac{n(n-1)}{2}
$$

For $n=3$:

$$
\frac{3(2)}{2}=3
$$

### Answer

$$
\boxed{3}
$$

> [!tip]
> For unique pairs, remember:
>
> $$\boxed{j=i+1}$$

---

## 20. Example — Find Duplicate Elements

### Question

Find duplicate values in:

    1 2 3 2 4 1

### Pattern

Compare every element with the elements after it.

### Code

    int[] arr = {1, 2, 3, 2, 4, 1};

    for (int i = 0; i < arr.length; i++) {

        for (int j = i + 1; j < arr.length; j++) {

            if (arr[i] == arr[j]) {
                System.out.println("Duplicate: " + arr[i]);
            }
        }
    }

### Answer

    Duplicate: 2
    Duplicate: 1

> [!warning]
> This is a brute-force solution with $O(n^2)$ time.
>
> For large inputs, a `HashSet` or frequency map can often provide a faster solution.

---

## 21. Example — Two Sum Brute Force

### Question

Find a pair whose sum is:

$$
target=9
$$

Array:

    2 7 11 15

### Recognition

Check every unique pair.

### Code

    int[] arr = {2, 7, 11, 15};
    int target = 9;

    for (int i = 0; i < arr.length; i++) {

        for (int j = i + 1; j < arr.length; j++) {

            if (arr[i] + arr[j] == target) {
                System.out.println(arr[i] + " " + arr[j]);
            }
        }
    }

### Calculation

$$
2+7=9
$$

### Answer

$$
\boxed{2,\ 7}
$$

Time complexity:

$$
\boxed{O(n^2)}
$$

---

## 22. Example — Main Diagonal

### Question

Print the main diagonal:

    1 2 3
    4 5 6
    7 8 9

### Recognition

Main diagonal positions satisfy:

$$
i=j
$$

### Code

    int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {

            if (i == j) {
                System.out.print(matrix[i][j] + " ");
            }
        }
    }

### Answer

    1 5 9

$$
\boxed{1,\ 5,\ 9}
$$

---

## 23. Example — Anti-Diagonal

### Question

Print the anti-diagonal:

    1 2 3
    4 5 6
    7 8 9

### Recognition

For an $n\times n$ matrix:

$$
i+j=n-1
$$

### Code

    int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int n = matrix.length;

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {

            if (i + j == n - 1) {
                System.out.print(matrix[i][j] + " ");
            }
        }
    }

### Answer

    3 5 7

$$
\boxed{3,\ 5,\ 7}
$$

---

## 24. Example — Row Sum

### Question

Find the sum of every row:

    1 2 3
    4 5 6
    7 8 9

### Code

    int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    for (int i = 0; i < matrix.length; i++) {

        int sum = 0;

        for (int j = 0; j < matrix[i].length; j++) {
            sum += matrix[i][j];
        }

        System.out.println(sum);
    }

### Calculation

$$
1+2+3=6
$$

$$
4+5+6=15
$$

$$
7+8+9=24
$$

### Answer

    6
    15
    24

---

## 25. Example — Column Sum

### Question

Find the sum of every column:

    1 2 3
    4 5 6
    7 8 9

### Code

    int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int rows = matrix.length;
    int columns = matrix[0].length;

    for (int j = 0; j < columns; j++) {

        int sum = 0;

        for (int i = 0; i < rows; i++) {
            sum += matrix[i][j];
        }

        System.out.println(sum);
    }

### Calculation

$$
1+4+7=12
$$

$$
2+5+8=15
$$

$$
3+6+9=18
$$

### Answer

    12
    15
    18

> [!important]
> Row-wise operation:
>
> Fix the row and move through columns.
>
> Column-wise operation:
>
> Fix the column and move through rows.

---

## 26. Pattern Recognition — Rectangle

If the pattern has the same number of elements in every row:

    * * * *
    * * * *
    * * * *

Think:

    for (int i = 0; i < rows; i++) {

        for (int j = 0; j < columns; j++) {
            // print
        }

        System.out.println();
    }

Recognition:

$$
\boxed{rows\times columns}
$$

---

## 27. Pattern Recognition — Increasing Triangle

If the row lengths are:

$$
1,2,3,\ldots,n
$$

Think:

$$
\boxed{j\leq i}
$$

Typical structure:

    for (int i = 1; i <= n; i++) {

        for (int j = 1; j <= i; j++) {
            // print
        }

        System.out.println();
    }

---

## 28. Pattern Recognition — Decreasing Triangle

If the row lengths are:

$$
n,n-1,n-2,\ldots,1
$$

Think:

    for (int i = n; i >= 1; i--) {

        for (int j = 1; j <= i; j++) {
            // print
        }

        System.out.println();
    }

---

## 29. Pattern Recognition — Spaces and Stars

For centered patterns, divide every row into:

    Spaces
       +
    Stars
       +
    Newline

Example:

    for (int i = 1; i <= n; i++) {

        for (int j = 1; j <= n - i; j++) {
            System.out.print(" ");
        }

        for (int j = 1; j <= i; j++) {
            System.out.print("* ");
        }

        System.out.println();
    }

> [!tip]
> Do not try to solve a complex pattern at once. Break every row into smaller components.

---

## 30. Nested while Loops

Nested loops can also be written using `while`.

### Example

    int i = 1;

    while (i <= 3) {

        int j = 1;

        while (j <= 2) {
            System.out.println(i + " " + j);
            j++;
        }

        i++;
    }

Output:

    1 1
    1 2
    2 1
    2 2
    3 1
    3 2

The same nested-loop principle applies.

---

## 31. Nested do while Loops

A `do while` loop can also contain another loop.

### Example

    int i = 1;

    do {

        int j = 1;

        do {
            System.out.println(i + " " + j);
            j++;
        } while (j <= 2);

        i++;

    } while (i <= 2);

Output:

    1 1
    1 2
    2 1
    2 2

---

## 32. Mixed Nested Loops

Different loop types can be nested.

Example:

    for (int i = 1; i <= 3; i++) {

        int j = 1;

        while (j <= 2) {
            System.out.println(i + " " + j);
            j++;
        }
    }

The outer loop is a `for` loop.

The inner loop is a `while` loop.

This is valid Java.

---

## 33. Time Complexity

### Case 1 — Two Equal Nested Loops

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {
            // work
        }
    }

Outer loop:

$$
O(n)
$$

Inner loop:

$$
O(n)
$$

Total:

$$
O(n)\times O(n)
$$

$$
\boxed{O(n^2)}
$$

---

### Case 2 — Different Bounds

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < m; j++) {
            // work
        }
    }

Total:

$$
n\times m
$$

Complexity:

$$
\boxed{O(nm)}
$$

---

### Case 3 — Three Nested Loops

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {

            for (int k = 0; k < n; k++) {
                // work
            }
        }
    }

Total:

$$
n^3
$$

Complexity:

$$
\boxed{O(n^3)}
$$

---

### Case 4 — Nested $n$ and $\log n$

    for (int i = 0; i < n; i++) {

        for (int j = 1; j < n; j *= 2) {
            // work
        }
    }

Outer:

$$
O(n)
$$

Inner:

$$
O(\log n)
$$

Total:

$$
\boxed{O(n\log n)}
$$

---

## 34. Triangular Nested Loop Complexity

Consider:

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {
            // work
        }
    }

Number of operations:

$$
(n-1)+(n-2)+\cdots+1
$$

Using:

$$
1+2+\cdots+(n-1)=\frac{n(n-1)}{2}
$$

Therefore:

$$
\frac{n(n-1)}{2}=O(n^2)
$$

### Answer

$$
\boxed{O(n^2)}
$$

---

## 35. Sequential Loops vs Nested Loops

### Sequential Loops

    for (int i = 0; i < n; i++) {
    }

    for (int j = 0; j < n; j++) {
    }

Work:

$$
n+n=2n
$$

Therefore:

$$
\boxed{O(n)}
$$

### Nested Loops

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {
        }
    }

Work:

$$
n\times n=n^2
$$

Therefore:

$$
\boxed{O(n^2)}
$$

> [!important]
> **Sequential loops usually add. Nested loops usually multiply.**

---

## 36. Space Complexity

A nested loop does not automatically mean $O(n^2)$ space.

Example:

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {
            int value = i + j;
            System.out.println(value);
        }
    }

Only a constant amount of extra memory is used.

Therefore:

$$
\boxed{O(1)}
$$

space.

> [!important]
> Time complexity measures operations.
>
> Space complexity measures additional memory.

---

## 37. Nested Loops and Arrays

For a 1D array:

    for (int i = 0; i < arr.length; i++) {
        System.out.println(arr[i]);
    }

For a 2D array:

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {
            System.out.println(matrix[i][j]);
        }
    }

Mental model:

    1D array
    → usually one loop

    2D array
    → usually two loops

    3D array
    → usually three loops

---

## 38. Advanced Pattern — All Subarrays

A brute-force method for generating all subarrays uses nested loops.

Array:

    1 2 3

### Code

    int[] arr = {1, 2, 3};

    for (int start = 0; start < arr.length; start++) {

        for (int end = start; end < arr.length; end++) {

            for (int k = start; k <= end; k++) {
                System.out.print(arr[k] + " ");
            }

            System.out.println();
        }
    }

Output:

    1
    1 2
    1 2 3
    2
    2 3
    3

Mental model:

    Choose start
        ↓
    Choose end
        ↓
    Process the range

> [!important]
> This is a common brute-force structure:
>
> **start → end → process**

---

## 39. Advanced Pattern — Pair Difference

### Question

Count pairs whose difference is `2`.

Array:

    1 3 5 7

### Code

    int[] arr = {1, 3, 5, 7};
    int count = 0;

    for (int i = 0; i < arr.length; i++) {

        for (int j = i + 1; j < arr.length; j++) {

            if (arr[j] - arr[i] == 2) {
                count++;
            }
        }
    }

    System.out.println(count);

Valid pairs:

    1, 3
    3, 5
    5, 7

Therefore:

$$
count=3
$$

### Answer

$$
\boxed{3}
$$

---

## 40. Advanced Pattern — Every Combination of Two Elements

If the problem says:

    Compare every pair
    Check every two elements
    Compare each element with the remaining elements

Think:

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {

            // process arr[i] and arr[j]
        }
    }

Common applications:

- Pair sum
- Pair difference
- Duplicate detection
- Brute-force inversion counting
- Maximum pair
- Minimum pair
- Pair comparisons

---

## 41. Advanced Pattern — Brute Force

Nested loops are often used as the first brute-force solution.

Example:

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {

            if (arr[i] + arr[j] == target) {
                // answer found
            }
        }
    }

Complexity:

$$
O(n^2)
$$

Then ask:

> **Can repeated work be avoided?**

Possible optimization techniques:

- Hashing
- Sorting
- Two pointers
- Binary search
- Prefix sum
- Sliding window

---

## 42. Recognition Tricks

> [!important]
> **If the question says "rows and columns":**
>
> Think:
>
> $$\boxed{\text{Nested Loops}}$$

> [!important]
> **If the question says "2D array" or "matrix":**
>
> Think:
>
> `i → row`
>
> `j → column`

> [!important]
> **If the question says "every pair":**
>
> Think:
>
>     for (int i = 0; i < n; i++) {
>
>         for (int j = i + 1; j < n; j++) {
>         }
>     }

> [!important]
> **If ordered pairs are required:**
>
> Use:
>
>     for (int i = 0; i < n; i++) {
>
>         for (int j = 0; j < n; j++) {
>         }
>     }

> [!important]
> **If row length increases:**
>
> Think:
>
> $$j\leq i$$

> [!important]
> **If row length decreases:**
>
> Think:
>
> Decreasing inner-loop count.

> [!important]
> **If main diagonal is required:**
>
> Think:
>
> $$i=j$$

> [!important]
> **If anti-diagonal is required:**
>
> Think:
>
> $$i+j=n-1$$

> [!important]
> **If all subarrays are required:**
>
> Think:
>
> `start → end → process`

---

## 43. Shortcuts

> [!tip]
> **Shortcut: Matrix**
>
> Remember:
>
> `i → row`
>
> `j → column`

> [!tip]
> **Shortcut: Unique Pair**
>
> Use:
>
> $$\boxed{j=i+1}$$

> [!tip]
> **Shortcut: Number of Unique Pairs**
>
> For $n$ elements:
>
> $$\boxed{\frac{n(n-1)}{2}}$$

> [!tip]
> **Shortcut: Rectangle**
>
> Number of cells:
>
> $$\boxed{rows\times columns}$$

> [!tip]
> **Shortcut: Triangle**
>
> Number of elements:
>
> $$\boxed{\frac{n(n+1)}{2}}$$

> [!tip]
> **Shortcut: Complexity**
>
> Nested:
>
> $$O(n)\times O(m)=O(nm)$$
>
> Sequential:
>
> $$O(n)+O(m)=O(n+m)$$

> [!tip]
> **Shortcut: Pattern Printing**
>
> Always ask:
>
> 1. How many rows?
> 2. How many elements in each row?
> 3. What should be printed?
> 4. Are spaces required?
> 5. Where should the newline occur?

---

## 44. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Rectangle

    for (int i = 0; i < rows; i++) {

        for (int j = 0; j < columns; j++) {
            // work
        }
    }

### Pattern 2 — Square

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {
            // work
        }
    }

### Pattern 3 — Increasing Triangle

    for (int i = 1; i <= n; i++) {

        for (int j = 1; j <= i; j++) {
            // work
        }
    }

### Pattern 4 — Decreasing Triangle

    for (int i = n; i >= 1; i--) {

        for (int j = 1; j <= i; j++) {
            // work
        }
    }

### Pattern 5 — Matrix Traversal

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {
            // matrix[i][j]
        }
    }

### Pattern 6 — Every Ordered Pair

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {
            // process pair
        }
    }

### Pattern 7 — Every Unique Pair

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {
            // process pair
        }
    }

### Pattern 8 — Main Diagonal

    if (i == j) {
        // main diagonal
    }

### Pattern 9 — Anti-Diagonal

    if (i + j == n - 1) {
        // anti-diagonal
    }

### Pattern 10 — Row Sum

    for (int i = 0; i < matrix.length; i++) {

        int sum = 0;

        for (int j = 0; j < matrix[i].length; j++) {
            sum += matrix[i][j];
        }

        System.out.println(sum);
    }

### Pattern 11 — Column Sum

    for (int j = 0; j < columns; j++) {

        int sum = 0;

        for (int i = 0; i < rows; i++) {
            sum += matrix[i][j];
        }

        System.out.println(sum);
    }

### Pattern 12 — Compare Every Pair

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {

            if (condition) {
                // process
            }
        }
    }

---

## 45. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting That the Inner Loop Restarts

Consider:

    for (int i = 1; i <= 3; i++) {

        for (int j = 1; j <= 2; j++) {
            System.out.println(i + " " + j);
        }
    }

The inner loop runs:

    1, 2
    1, 2
    1, 2

The `j` loop starts again for every new `i`.

---

### Mistake 2 — Incorrect Array Boundary

Wrong:

    for (int j = 0; j <= arr.length; j++) {
        System.out.println(arr[j]);
    }

Correct:

    for (int j = 0; j < arr.length; j++) {
        System.out.println(arr[j]);
    }

Valid indexes are:

$$
0,1,2,\ldots,length-1
$$

---

### Mistake 3 — Mixing Rows and Columns

For:

    matrix[i][j]

normally:

    i → row
    j → column

Do not accidentally reverse them.

---

### Mistake 4 — Wrong Starting Point for Unique Pairs

Wrong:

    for (int j = 0; j < n; j++) {
    }

This can produce both:

    1 2
    2 1

as separate pairs.

Correct:

    for (int j = i + 1; j < n; j++) {
    }

Now:

$$
j>i
$$

---

### Mistake 5 — Assuming Every Nested Loop Is $O(n^2)$

Consider:

    for (int i = 0; i < n; i++) {

        for (int j = 1; j < n; j *= 2) {
        }
    }

Inner loop:

$$
O(\log n)
$$

Therefore total:

$$
\boxed{O(n\log n)}
$$

---

### Mistake 6 — Counting Sequential Loops as $O(n^2)$

Two separate loops:

    for (int i = 0; i < n; i++) {
    }

    for (int j = 0; j < n; j++) {
    }

Complexity:

$$
O(n+n)=O(n)
$$

---

### Mistake 7 — Forgetting Newline in Pattern Printing

Wrong:

    for (int i = 1; i <= 3; i++) {

        for (int j = 1; j <= 4; j++) {
            System.out.print("* ");
        }
    }

Correct:

    for (int i = 1; i <= 3; i++) {

        for (int j = 1; j <= 4; j++) {
            System.out.print("* ");
        }

        System.out.println();
    }

---

### Mistake 8 — Modifying the Outer Variable Inside the Inner Loop

Avoid:

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {
            i++;
        }
    }

Changing the outer variable can cause skipped iterations and confusing behavior.

---

### Mistake 9 — Not Resetting the Accumulator

For row sums, reset the sum for each row.

Correct:

    for (int i = 0; i < rows; i++) {

        int sum = 0;

        for (int j = 0; j < columns; j++) {
            sum += matrix[i][j];
        }

        System.out.println(sum);
    }

---

## 46. Output-Tracing Strategy

For nested-loop output questions:

### Step 1 — Identify the Outer Variable

Example:

    for (int i = 1; i <= 3; i++)

Therefore:

$$
i=1,2,3
$$

### Step 2 — Freeze One Outer Value

Take:

$$
i=1
$$

### Step 3 — Execute the Complete Inner Loop

Find every value of `j`.

### Step 4 — Move to the Next Outer Value

Now:

$$
i=2
$$

Again execute the complete inner loop.

### Example

    for (int i = 1; i <= 3; i++) {

        for (int j = 1; j <= i; j++) {
            System.out.print(j + " ");
        }

        System.out.println();
    }

Trace:

| `i` | `j` values | Output |
|---:|---|---|
| 1 | 1 | `1` |
| 2 | 1, 2 | `1 2` |
| 3 | 1, 2, 3 | `1 2 3` |

Final:

    1
    1 2
    1 2 3

> [!tip]
> Never try to execute both loops mentally at the same time.
>
> Freeze the outer value, complete the inner loop, then move to the next outer value.

---

## 47. Advanced Output Question

### Question

Find the output:

    for (int i = 1; i <= 3; i++) {

        for (int j = 1; j <= 2; j++) {
            System.out.print(i + j + " ");
        }
    }

### Trace

For $i=1$:

$$
1+1=2
$$

$$
1+2=3
$$

For $i=2$:

$$
2+1=3
$$

$$
2+2=4
$$

For $i=3$:

$$
3+1=4
$$

$$
3+2=5
$$

### Answer

    2 3 3 4 4 5

---

## 48. Advanced Output Question

### Question

Find the output:

    for (int i = 1; i <= 3; i++) {

        for (int j = i; j <= 3; j++) {
            System.out.print(j + " ");
        }

        System.out.println();
    }

### Trace

For $i=1$:

    1 2 3

For $i=2$:

    2 3

For $i=3$:

    3

### Answer

    1 2 3
    2 3
    3

---

## 49. Advanced Pattern — Spaces and Stars

### Question

Print:

    *
    * *
    * * *
    * * * *
    * * * * *

### Recognition

Each row has an increasing number of stars.

### Code

    int n = 5;

    for (int i = 1; i <= n; i++) {

        for (int j = 1; j <= i; j++) {
            System.out.print("* ");
        }

        System.out.println();
    }

The important idea is:

$$
\text{Stars in row }i=i
$$

---

## 50. Advanced Pattern — Pyramid

### Question

Print:

    *
    ***
    *****
    *******
    *********

### Recognition

For row `i`:

Spaces:

$$
n-i
$$

Stars:

$$
2i-1
$$

### Code

    int n = 5;

    for (int i = 1; i <= n; i++) {

        for (int j = 1; j <= n - i; j++) {
            System.out.print(" ");
        }

        for (int j = 1; j <= 2 * i - 1; j++) {
            System.out.print("*");
        }

        System.out.println();
    }

Important formula:

$$
\boxed{\text{Stars}=2i-1}
$$

---

## 51. Optimization Insight

Nested loops often indicate a brute-force solution.

Example:

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {

            if (arr[i] + arr[j] == target) {
                return true;
            }
        }
    }

Complexity:

$$
O(n^2)
$$

Now ask:

> **Can I avoid checking the same information repeatedly?**

Possible improvements:

    Brute Force
        ↓
    O(n²)
        ↓
    Identify repeated work
        ↓
    Hashing / Sorting / Two Pointers
        ↓
    Faster solution

> [!important]
> Nested loops are not automatically bad. They are often the simplest correct starting point.

---

## 52. Common Placement Patterns

> [!important] Must Master

### Pattern 1 — Rows and Columns

Think:

$$
\boxed{\text{Nested Loops}}
$$

### Pattern 2 — Every Pair

Think:

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {
        }
    }

### Pattern 3 — Every Ordered Pair

Think:

    for (int i = 0; i < n; i++) {

        for (int j = 0; j < n; j++) {
        }
    }

### Pattern 4 — 2D Array

Think:

    row → i
    column → j

### Pattern 5 — Increasing Pattern

Think:

$$
j\leq i
$$

### Pattern 6 — Main Diagonal

Think:

$$
i=j
$$

### Pattern 7 — Anti-Diagonal

Think:

$$
i+j=n-1
$$

### Pattern 8 — All Subarrays

Think:

    start → end → process

### Pattern 9 — Brute-Force Pair Checking

Think:

$$
O(n^2)
$$

Then ask whether hashing, sorting, or two pointers can optimize it.

---

## 53. Formula Sheet

| Concept | Formula |
|---|---|
| Two nested loops | $O(nm)$ |
| Equal nested loops | $O(n^2)$ |
| Three equal nested loops | $O(n^3)$ |
| Nested $n$ and $\log n$ | $O(n\log n)$ |
| Unique pairs | $\frac{n(n-1)}{2}$ |
| Triangle elements | $\frac{n(n+1)}{2}$ |
| Rectangle cells | $rows\times columns$ |
| Main diagonal | $i=j$ |
| Anti-diagonal | $i+j=n-1$ |

### Core Templates

Rectangle:

    for (int i = 0; i < rows; i++) {

        for (int j = 0; j < columns; j++) {
        }
    }

Unique pairs:

    for (int i = 0; i < n; i++) {

        for (int j = i + 1; j < n; j++) {
        }
    }

Matrix traversal:

    for (int i = 0; i < matrix.length; i++) {

        for (int j = 0; j < matrix[i].length; j++) {
        }
    }

---

## 54. Quick Revision

> [!summary] One-Minute Revision

    Nested loop
    → A loop inside another loop.

    Outer loop
    → Controls the major repetition.

    Inner loop
    → Runs completely for every outer iteration.

    Core rule
    → One outer iteration → complete inner loop.

    Rows + columns
    → Think nested loops.

    2D array
    → Outer loop for rows.
    → Inner loop for columns.

    Matrix
    → matrix[i][j]
    → i = row
    → j = column.

    Rectangle
    → rows × columns.

    Increasing triangle
    → Inner loop usually depends on i.

    Decreasing triangle
    → Inner-loop count decreases.

    Every ordered pair
    → j starts from 0.

    Every unique pair
    → j starts from i + 1.

    Main diagonal
    → i == j.

    Anti-diagonal
    → i + j == n - 1.

    Subarray brute force
    → start → end → process.

    Sequential loops
    → Complexities usually add.

    Nested loops
    → Complexities usually multiply.

    n × n
    → O(n²).

    n × m
    → O(nm).

    n × log n
    → O(n log n).

    Three n-sized nested loops
    → O(n³).

    Unique pair count
    → n(n - 1) / 2.

    Triangle count
    → n(n + 1) / 2.

    Nested loops do not automatically mean O(n²).
    → Always inspect how variables change.

    Nested loops do not automatically mean O(n²) space.
    → Time and space are different.

    Pattern printing
    → Identify rows.
    → Identify elements per row.
    → Identify what to print.
    → Handle spaces.
    → Print newline.

    Brute force
    → Nested loops are often the first solution.

    Optimization
    → Look for hashing, sorting, two pointers, binary search,
      prefix techniques, or other patterns.

    Main danger
    → Incorrect boundaries and incorrect complexity analysis.

---

## Golden Memory Trick

**Nested loops mean: for every outer-loop iteration, execute the entire inner loop.**

## One-Line Recognition

**If a problem involves rows and columns, every pair, every combination, matrix cells, or repeated comparisons between elements, think nested loops.**