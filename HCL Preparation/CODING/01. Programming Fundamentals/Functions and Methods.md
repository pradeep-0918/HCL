---
type: concept
subject: coding
topic: "Functions and Methods"
parent: "Programming Fundamentals"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - coding
  - hcl
  - programming-fundamentals
  - functions
  - methods
  - java
  - programming
wikilinks:
  - "[[Programming Fundamentals]]"
  - "[[Variables and Data Types]]"
  - "[[Recursion Basics]]"
  - "[[Loops]]"
---

# Functions and Methods

## 1. Core Concept

> [!summary]
> A **function** is a reusable block of code designed to perform a specific task.
>
> In Java, functions are called **methods** because they are defined inside a class.

Instead of writing the same logic repeatedly, place it inside a method and call it whenever needed.

### Basic Idea

~~~text
Define once → Call many times
~~~

Example:

~~~java
static void greet() {
    System.out.println("Hello");
}
~~~

Call the method:

~~~java
greet();
~~~

Output:

~~~text
Hello
~~~

### Why Use Methods?

Methods help with:

- Code reuse
- Better organization
- Easier debugging
- Reduced repetition
- Better readability
- Breaking a large problem into smaller parts

---

# 2. Basic Meaning

## What is a Function?

A function is a reusable block of instructions that performs a particular operation.

General structure:

~~~text
Function
│
├── Name
├── Parameters
├── Return Type
└── Body
~~~

Example:

~~~java
static int add(int a, int b) {
    return a + b;
}
~~~

Here:

| Part | Meaning |
|---|---|
| `static` | Method modifier |
| `int` | Return type |
| `add` | Method name |
| `int a, int b` | Parameters |
| `return a + b` | Returned result |

## Function vs Method

In general programming terminology:

- **Function** → reusable block of code.
- **Method** → function associated with a class/object.

In Java, we normally say **method**.

> [!important]
> Java does not have standalone functions like some languages. Methods are declared inside classes.

---

# 3. Main Method Structure

A Java method can be represented as:

~~~java
accessModifier static returnType methodName(parameters) {
    // method body
}
~~~

Example:

~~~java
public static int add(int a, int b) {
    return a + b;
}
~~~

Breakdown:

~~~text
public
→ access modifier

static
→ belongs to the class

int
→ return type

add
→ method name

(int a, int b)
→ parameters

return a + b;
→ method body + returned value
~~~

---

# 4. Method Without Parameters and Return Value

A method can perform an action without accepting input or returning a value.

Example:

~~~java
static void greet() {
    System.out.println("Hello");
}
~~~

Call:

~~~java
greet();
~~~

Output:

~~~text
Hello
~~~

Here:

- No parameters
- `void` return type
- Performs an action

### Pattern

~~~text
No input + No output
→ void method without parameters
~~~

---

# 5. Method With Parameters

Parameters allow data to be passed into a method.

Example:

~~~java
static void greet(String name) {
    System.out.println("Hello " + name);
}
~~~

Call:

~~~java
greet("Pradeep");
~~~

Output:

~~~text
Hello Pradeep
~~~

Here:

~~~text
name
→ parameter
~~~

~~~text
"Pradeep"
→ argument
~~~

> [!important]
> **Parameter** is the variable declared in the method.
>
> **Argument** is the actual value passed during the method call.

---

# 6. Parameter vs Argument

Example:

~~~java
static int square(int n) {
    return n * n;
}

square(5);
~~~

Here:

~~~text
n
→ parameter

5
→ argument
~~~

Think:

$$
\text{Parameter} = \text{placeholder}
$$

$$
\text{Argument} = \text{actual value}
$$

---

# 7. Method With Return Value

A method can calculate something and return the result.

Example:

~~~java
static int add(int a, int b) {
    return a + b;
}
~~~

Call:

~~~java
int result = add(10, 20);
~~~

Calculation:

$$
10+20=30
$$

Therefore:

$$
result=30
$$

### Answer

$$
\boxed{30}
$$

> [!important]
> A non-`void` method must return a value compatible with its return type.

---

# 8. `void` Methods

`void` means the method does not return a value.

Example:

~~~java
static void printMessage() {
    System.out.println("Hello");
}
~~~

The method performs an action but does not return a result.

Correct:

~~~java
printMessage();
~~~

A `void` method can use:

~~~java
return;
~~~

to exit early, but it does not return a value.

---

# 9. Four Important Method Types

Methods can be classified based on parameters and return value.

| Type | Parameters | Return Value |
|---|---|---|
| Type 1 | No | No |
| Type 2 | Yes | No |
| Type 3 | No | Yes |
| Type 4 | Yes | Yes |

### Type 1 — No Parameter, No Return

~~~java
static void greet() {
    System.out.println("Hello");
}
~~~

### Type 2 — Parameter, No Return

~~~java
static void printSquare(int n) {
    System.out.println(n * n);
}
~~~

### Type 3 — No Parameter, Return

~~~java
static int getNumber() {
    return 10;
}
~~~

### Type 4 — Parameter, Return

~~~java
static int square(int n) {
    return n * n;
}
~~~

> [!important] Must Master
> The most commonly useful pattern in coding problems is:
>
> **Parameters + Return Value**

---

# 10. Basic Examples

## Example 1 — Create an Addition Method

### Question

Create a method that returns the sum of two integers.

### Pattern

Two inputs + one result.

### Formula

$$
sum=a+b
$$

### Code

~~~java
static int add(int a, int b) {
    return a + b;
}
~~~

Call:

~~~java
int result = add(10, 20);
~~~

Calculation:

$$
10+20=30
$$

### Answer

$$
\boxed{30}
$$

---

## Example 2 — Square of a Number

### Question

Create a method that returns the square of a number.

### Pattern

One input → one result.

### Formula

$$
square=n^2
$$

### Code

~~~java
static int square(int n) {
    return n * n;
}
~~~

Call:

~~~java
int result = square(6);
~~~

Calculation:

$$
6^2=36
$$

### Answer

$$
\boxed{36}
$$

---

## Example 3 — Check Even Number

### Question

Create a method that returns whether a number is even.

### Pattern

Even → `% 2 == 0`.

### Code

~~~java
static boolean isEven(int n) {
    return n % 2 == 0;
}
~~~

For:

$$
n=18
$$

We get:

$$
18\%2=0
$$

Therefore:

$$
isEven(18)=true
$$

### Answer

$$
\boxed{true}
$$

---

# 11. Advanced Examples

## Example 4 — Maximum of Two Numbers

### Question

Create a method that returns the larger of two numbers.

### Pattern

Comparison → return larger value.

### Code

~~~java
static int max(int a, int b) {
    if (a > b) {
        return a;
    }

    return b;
}
~~~

Call:

~~~java
int result = max(25, 40);
~~~

Since:

$$
40>25
$$

Therefore:

$$
result=40
$$

### Answer

$$
\boxed{40}
$$

---

# 12. Method Using Multiple Conditions

## Example 5 — Maximum of Three Numbers

### Question

Return the largest among three integers.

### Pattern

Compare values.

### Code

~~~java
static int maxOfThree(int a, int b, int c) {
    int max = a;

    if (b > max) {
        max = b;
    }

    if (c > max) {
        max = c;
    }

    return max;
}
~~~

Call:

~~~java
int result = maxOfThree(10, 50, 30);
~~~

Step-by-step:

~~~text
max = 10

50 > 10
→ max = 50

30 > 50
→ false
~~~

Therefore:

$$
max=50
$$

### Answer

$$
\boxed{50}
$$

---

# 13. Method Calling Another Method

A method can call another method.

Example:

~~~java
static int square(int n) {
    return n * n;
}

static int sumOfSquares(int a, int b) {
    return square(a) + square(b);
}
~~~

Call:

~~~java
int result = sumOfSquares(3, 4);
~~~

Calculation:

$$
3^2+4^2
$$

$$
9+16=25
$$

### Answer

$$
\boxed{25}
$$

> [!important]
> Breaking a large problem into smaller methods is a powerful problem-solving technique.

---

# 14. Local Variables in Methods

Variables declared inside a method are local variables.

Example:

~~~java
static int add(int a, int b) {
    int sum = a + b;
    return sum;
}
~~~

Here:

~~~text
a
b
sum
~~~

are local to the method.

They cannot normally be accessed directly from outside that method.

> [!warning]
> Do not confuse local variables with class-level variables.

---

# 15. Return Statement

The `return` statement sends a value back to the caller.

Example:

~~~java
static int doubleValue(int n) {
    return n * 2;
}
~~~

Call:

~~~java
int result = doubleValue(10);
~~~

The method calculates:

$$
10\times2=20
$$

Then:

~~~text
return 20
~~~

The caller receives:

$$
result=20
$$

### Flow

~~~text
Caller
  ↓
doubleValue(10)
  ↓
Method calculates 20
  ↓
return 20
  ↓
Caller receives 20
~~~

---

# 16. Early Return

A method can return early when a condition is satisfied.

Example:

~~~java
static boolean isPositive(int n) {
    if (n > 0) {
        return true;
    }

    return false;
}
~~~

For:

$$
n=5
$$

The condition is true, so the method immediately returns `true`.

### Simplified Version

~~~java
static boolean isPositive(int n) {
    return n > 0;
}
~~~

> [!tip]
> If a method only returns the result of a condition, you can often return the condition directly.

---

# 17. Method Overloading

Java supports **method overloading**.

Method overloading means having multiple methods with the same name but different parameter lists.

Example:

~~~java
static int add(int a, int b) {
    return a + b;
}

static int add(int a, int b, int c) {
    return a + b + c;
}
~~~

Calls:

~~~java
add(10, 20);
add(10, 20, 30);
~~~

Both methods have the name `add`, but their parameter lists differ.

> [!important]
> Method overloading requires a different parameter list.
>
> You cannot overload a method using only a different return type.

---

# 18. Invalid Overloading

This is not valid:

~~~java
static int add(int a, int b) {
    return a + b;
}

static double add(int a, int b) {
    return a + b;
}
~~~

Why?

The parameter list is identical.

Only the return type differs.

> [!warning]
> Return type alone cannot distinguish overloaded methods.

---

# 19. Pass by Value in Java

Java uses **pass-by-value**.

For primitive values, the method receives a copy of the value.

Example:

~~~java
static void change(int x) {
    x = 100;
}

public static void main(String[] args) {
    int a = 10;

    change(a);

    System.out.println(a);
}
~~~

Output:

~~~text
10
~~~

Why?

The method receives a copy of `a`.

~~~text
Original:
a = 10

Method receives:
x = 10

Change:
x = 100

Original remains:
a = 10
~~~

> [!important]
> Java is always pass-by-value. For object references, the reference value itself is passed by value.

---

# 20. Static Methods

A `static` method belongs to the class rather than a particular object.

Example:

~~~java
static int add(int a, int b) {
    return a + b;
}
~~~

It can be called directly from another static context:

~~~java
int result = add(10, 20);
~~~

This is why many coding-platform solutions use:

~~~java
public static
~~~

for methods.

---

# 21. Instance Methods

An instance method belongs to an object.

Example:

~~~java
class Calculator {

    int add(int a, int b) {
        return a + b;
    }
}
~~~

Create an object:

~~~java
Calculator c = new Calculator();

int result = c.add(10, 20);
~~~

The method is called using the object.

> [!important]
> `static` → call using class/static context.
>
> Instance method → generally call using an object.

---

# 22. Method Signature

A method signature in Java consists of:

~~~text
Method name + Parameter types
~~~

Example:

~~~java
static int add(int a, int b)
~~~

Signature:

~~~text
add(int, int)
~~~

Another:

~~~java
static int add(int a, int b, int c)
~~~

Signature:

~~~text
add(int, int, int)
~~~

These have different signatures and can therefore be overloaded.

---

# 23. Scope and Methods

Variables declared inside a method are accessible only within their scope.

Example:

~~~java
static int calculate() {

    int x = 10;

    if (x > 5) {
        int y = 20;
        return x + y;
    }

    return x;
}
~~~

`y` exists only inside the `if` block.

This follows the same scope rules learned in variables and data types.

---

# 24. Exam-Style Examples

## Example 6 — Factorial Using a Method

### Question

Create a method to calculate the factorial of `5`.

### Pattern

Factorial:

$$
n!=n\times(n-1)\times...\times1
$$

For:

$$
5!=5\times4\times3\times2\times1
$$

$$
5!=120
$$

### Code

~~~java
static int factorial(int n) {
    int result = 1;

    for (int i = 1; i <= n; i++) {
        result *= i;
    }

    return result;
}
~~~

Call:

~~~java
int answer = factorial(5);
~~~

### Answer

$$
\boxed{120}
$$

---

# 25. Example — Prime Checking Method

## Example 7

### Question

Create a method that checks whether a number is prime.

### Pattern

A prime number has exactly two positive divisors: `1` and itself.

We only need to check divisors up to:

$$
\sqrt{n}
$$

### Code

~~~java
static boolean isPrime(int n) {

    if (n < 2) {
        return false;
    }

    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) {
            return false;
        }
    }

    return true;
}
~~~

For:

$$
n=17
$$

Check possible divisors up to:

$$
\sqrt{17}\approx4.12
$$

Check:

~~~text
2 → not divisible
3 → not divisible
4 → not divisible
~~~

Therefore:

$$
17=\text{prime}
$$

### Answer

$$
\boxed{true}
$$

> [!tip]
> Putting prime-checking logic inside a method makes it reusable across many problems.

---

# 26. Example — Reverse Number Using a Method

## Example 8

### Question

Create a method to reverse an integer.

Given:

$$
1234
$$

Expected:

$$
4321
$$

### Pattern

Repeatedly extract the last digit using `% 10`.

### Code

~~~java
static int reverse(int n) {

    int rev = 0;

    while (n > 0) {
        int digit = n % 10;
        rev = rev * 10 + digit;
        n /= 10;
    }

    return rev;
}
~~~

Step-by-step:

~~~text
n = 1234

digit = 4
rev = 4

digit = 3
rev = 43

digit = 2
rev = 432

digit = 1
rev = 4321
~~~

### Answer

$$
\boxed{4321}
$$

---

# 27. Pattern Recognition

> [!important] Must Master

### Pattern 1 — Repeated Logic

If the same logic appears multiple times:

~~~text
Think → Create a method
~~~

---

### Pattern 2 — Need a Result

If the logic calculates and sends a value back:

~~~text
Think → return type + return
~~~

Example:

~~~java
static int sum(int a, int b) {
    return a + b;
}
~~~

---

### Pattern 3 — Only Perform an Action

If the method only prints or performs an action:

~~~text
Think → void
~~~

Example:

~~~java
static void printHello() {
    System.out.println("Hello");
}
~~~

---

### Pattern 4 — Reusable Validation

If multiple parts of the program need the same check:

~~~text
Think → boolean method
~~~

Example:

~~~java
static boolean isEven(int n) {
    return n % 2 == 0;
}
~~~

---

### Pattern 5 — Multiple Similar Operations

If methods have the same name but different inputs:

~~~text
Think → method overloading
~~~

---

### Pattern 6 — Large Problem

If the problem contains multiple independent tasks:

~~~text
Break into smaller methods.
~~~

Example:

~~~text
main()
│
├── readInput()
├── calculate()
├── validate()
└── printResult()
~~~

---

# 28. Recognition Tricks

> [!important]
> If the same code must be used multiple times, think **method**.

> [!important]
> If a method needs to send a result back, think **return value**.

> [!important]
> If it only performs an action, think **void**.

> [!important]
> If a method receives data, think **parameters**.

> [!important]
> If the method name is the same but parameters differ, think **overloading**.

> [!important]
> If a method returns `true` or `false`, think **boolean method**.

> [!important]
> If a large problem has independent tasks, think **break it into methods**.

---

# 29. Shortcuts

> [!tip]
> **Shortcut: Method Design**
>
> Ask three questions:
>
> 1. What input does the method need?
> 2. What should it return?
> 3. What logic should it perform?

---

> [!tip]
> **Shortcut: Four Method Types**
>
> ```text
> No parameter + No return
> → void method
>
> Parameter + No return
> → action method
>
> No parameter + Return
> → value-producing method
>
> Parameter + Return
> → most commonly useful coding pattern
> ```

---

> [!tip]
> **Shortcut: Boolean Methods**
>
> If the method answers a yes/no question, return a boolean directly.
>
> Example:
>
> ~~~java
> static boolean isEven(int n) {
>     return n % 2 == 0;
> }
> ~~~

---

> [!tip]
> **Shortcut: Avoid Duplicate Code**
>
> If you find yourself copying the same block of code twice, consider creating a method.

---

# 30. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Forgetting `return`

Wrong:

~~~java
static int add(int a, int b) {
    a + b;
}
~~~

Correct:

~~~java
static int add(int a, int b) {
    return a + b;
}
~~~

Why?

An `int` method must return an integer value.

---

### Mistake 2 — Returning the Wrong Type

Wrong:

~~~java
static int getValue() {
    return 5.5;
}
~~~

Correct:

~~~java
static double getValue() {
    return 5.5;
}
~~~

---

### Mistake 3 — Confusing Parameter and Argument

~~~java
static int square(int n) {
    return n * n;
}
~~~

Here:

~~~text
n → parameter
5 → argument
~~~

when calling:

~~~java
square(5);
~~~

---

### Mistake 4 — Trying to Access Local Variables Outside a Method

Example:

~~~java
static void test() {
    int x = 10;
}
~~~

This is invalid:

~~~java
System.out.println(x);
~~~

because `x` is local to `test()`.

---

### Mistake 5 — Overloading Only by Return Type

Invalid:

~~~java
static int add(int a, int b) {
    return a + b;
}

static double add(int a, int b) {
    return a + b;
}
~~~

The parameter list is identical.

---

### Mistake 6 — Forgetting That Java Is Pass-by-Value

Changing a primitive parameter inside a method does not change the original primitive variable.

~~~java
static void change(int x) {
    x = 100;
}
~~~

The caller's original variable remains unchanged.

---

### Mistake 7 — Creating Unnecessary Methods

Not every one-line operation needs a separate method.

Create methods when they improve:

- Reusability
- Readability
- Organization
- Testing

---

# 31. Formula Sheet

### Function Structure

~~~text
returnType methodName(parameters)
~~~

### Method With Return

~~~java
static int add(int a, int b) {
    return a + b;
}
~~~

### Void Method

~~~java
static void printMessage() {
    System.out.println("Hello");
}
~~~

### Boolean Method

~~~java
static boolean isEven(int n) {
    return n % 2 == 0;
}
~~~

### Method Call

~~~java
add(10, 20);
~~~

### Method Overloading

$$
\text{Same method name}+\text{Different parameter list}
$$

### Factorial

$$
n!=n\times(n-1)\times...\times1
$$

### Prime Check Optimization

$$
\text{Check divisors up to }\sqrt{n}
$$

---

# 32. Quick Revision

> [!summary] One-Minute Revision

~~~text
Method
→ Reusable block of code.

Java
→ Uses methods inside classes.

Parameter
→ Variable declared in method.

Argument
→ Actual value passed to method.

void
→ No return value.

return
→ Sends a value back.

static
→ Method belongs to the class.

Method call
→ Executes the method.

Method overloading
→ Same name + different parameter list.

Return type
→ Type of value returned.

boolean method
→ Useful for yes/no checks.

Local variable
→ Exists only within its scope.

Pass-by-value
→ Java passes values to methods.

Best coding pattern
→ Parameters + Return value.

Main purpose
→ Reuse, organize, simplify code.
~~~

## Golden Memory Trick

**A method is a reusable machine: give it input through parameters, let it process the data, and receive the result through `return`.**

## One-Line Recognition

**When the same logic needs to be reused or a problem can be divided into smaller tasks, create a method with the required parameters and return type.**