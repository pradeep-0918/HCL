---
type: concept
subject: aptitude
topic: "Encapsulation"
parent: "OOPS"
company: HCL
difficulty: easy
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - encapsulation
  - object-oriented-programming
  - quantitative-aptitude
wikilinks:
  - "[[OOPS]]"
  - "[[Class]]"
  - "[[Object]]"
  - "[[Abstraction]]"
  - "[[Access Modifiers]]"
---

# Encapsulation

## 1. Core Concept

> [!summary]
> **Encapsulation** is the process of bundling data and the methods that operate on that data into a single unit, while controlling direct access to the data.

In Java, a class is commonly used to achieve encapsulation.

Example:

~~~java
class BankAccount {
    private double balance;

    public void deposit(double amount) {
        balance += amount;
    }

    public double getBalance() {
        return balance;
    }
}
~~~

Here:

- `balance` → data
- `deposit()` → operation on data
- `getBalance()` → controlled access
- `private` → prevents direct access from outside the class

### Intuition

Think of an ATM.

You can:

- Deposit money
- Withdraw money
- Check balance

But you cannot directly access the internal bank database.

The system controls how you interact with the data.

That is the basic idea of encapsulation:

```text
Hide direct access
        ↓
Control access through methods
        ↓
Protect object data
```

> [!important]
> **Encapsulation = Data + Methods + Controlled Access**

---

## 2. Basic Meaning

Encapsulation combines:

1. Data
2. Methods that operate on the data
3. Access control

Example:

~~~java
class Student {
    private int marks;

    public void setMarks(int marks) {
        this.marks = marks;
    }

    public int getMarks() {
        return marks;
    }
}
~~~

The variable:

~~~java
private int marks;
~~~

cannot be directly accessed from outside the class.

Instead, controlled methods are provided:

~~~java
setMarks()
getMarks()
~~~

This gives the class control over how its data is accessed or modified.

### Without Encapsulation

~~~java
class Student {
    int marks;
}
~~~

External code can directly modify:

~~~java
Student s = new Student();

s.marks = -100;
~~~

There is no validation.

### With Encapsulation

~~~java
class Student {
    private int marks;

    public void setMarks(int marks) {
        if (marks >= 0 && marks <= 100) {
            this.marks = marks;
        }
    }

    public int getMarks() {
        return marks;
    }
}
~~~

Now invalid values can be rejected.

---

## 3. Main Formula

There is no mathematical formula for encapsulation.

For technical aptitude questions, remember:

$$
\text{Encapsulation} =
\text{Data} + \text{Methods} + \text{Access Control}
$$

A common implementation pattern in Java is:

~~~java
class ClassName {
    private DataType variable;

    public void setVariable(DataType value) {
        variable = value;
    }

    public DataType getVariable() {
        return variable;
    }
}
~~~

### Key Relationship

$$
\boxed{\text{Encapsulation} \rightarrow \text{Controlled Access to Data}}
$$

---

## 4. Important Properties

### 4.1 Data and Methods Are Bundled Together

Consider:

~~~java
class Employee {
    private double salary;

    public void increaseSalary(double amount) {
        salary += amount;
    }
}
~~~

Here:

```text
Data:
salary

Method:
increaseSalary()
```

Both belong to the same class.

---

### 4.2 Access Can Be Restricted

The `private` modifier prevents direct access from outside the class.

~~~java
class Account {
    private double balance;
}
~~~

This is not directly accessible from unrelated external code:

~~~java
Account a = new Account();

// Not allowed:
// a.balance = 5000;
~~~

---

### 4.3 Public Methods Can Provide Controlled Access

Instead of exposing the variable directly:

~~~java
private double balance;
~~~

the class can provide:

~~~java
public void deposit(double amount) {
    balance += amount;
}
~~~

This allows the class to control how the value changes.

---

### 4.4 Encapsulation Supports Data Protection

Suppose a student's marks must be between 0 and 100.

~~~java
class Student {
    private int marks;

    public void setMarks(int marks) {
        if (marks >= 0 && marks <= 100) {
            this.marks = marks;
        }
    }
}
~~~

The class prevents invalid values from being assigned through the provided setter.

---

### 4.5 Encapsulation Does Not Mean Complete Hiding

Encapsulation does not necessarily mean that every piece of data must be completely inaccessible.

Instead, access is **controlled**.

For example:

~~~java
private int age;

public int getAge() {
    return age;
}
~~~

The value can still be read, but only through a controlled interface.

---

### 4.6 Getters and Setters Are Common Tools

A getter retrieves data.

A setter modifies data.

Example:

~~~java
private String name;

public String getName() {
    return name;
}

public void setName(String name) {
    this.name = name;
}
~~~

Therefore:

```text
getName() → Read/access
setName() → Modify/update
```

---

### 4.7 Encapsulation Improves Maintainability

If the internal implementation changes, external code can continue using the same public methods.

For example:

~~~java
account.deposit(5000);
~~~

The internal implementation of `deposit()` can change without requiring callers to know the internal details.

---

### 4.8 Encapsulation Is Closely Related to Access Modifiers

Common Java access modifiers include:

| Modifier | Same Class | Same Package | Subclass | Other Package |
|---|---|---|---|---|
| `private` | Yes | No | No* | No |
| default | Yes | Yes | Yes** | No |
| `protected` | Yes | Yes | Yes | Yes*** |
| `public` | Yes | Yes | Yes | Yes |

Notes:

- `private` members are accessible only within their declaring class.
- Default/package-private members are accessible within the same package.
- `protected` has special rules for subclasses in other packages.
- `public` members are broadly accessible.

For basic aptitude questions:

> [!important]
> **`private` is the most commonly associated modifier with restricting direct access to data.**

---

## 5. Basic Examples

### Example 1 — Identify Encapsulation

**Question**

Which code best demonstrates encapsulation?

~~~java
class Student {
    private int marks;

    public int getMarks() {
        return marks;
    }

    public void setMarks(int marks) {
        this.marks = marks;
    }
}
~~~

**Pattern**

Look for:

```text
private data
+
public methods
```

**Calculation**

```text
marks → private
getMarks() → controlled read
setMarks() → controlled update
```

**Therefore:**

$$
\boxed{\text{The class demonstrates encapsulation}}
$$

---

### Example 2 — Identify the Encapsulated Data

**Question**

Consider:

~~~java
class Account {
    private double balance;

    public void deposit(double amount) {
        balance += amount;
    }
}
~~~

Which variable is encapsulated?

**Pattern**

Look for the restricted data member.

**Calculation**

```text
private double balance;
```

Therefore:

$$
\boxed{\text{balance}}
$$

---

### Example 3 — Getter and Setter

**Question**

Consider:

~~~java
class Employee {
    private int salary;

    public int getSalary() {
        return salary;
    }

    public void setSalary(int salary) {
        this.salary = salary;
    }
}
~~~

Which method retrieves the salary?

**Pattern**

A getter generally returns the value.

**Calculation**

~~~java
getSalary()
~~~

returns:

~~~java
salary
~~~

**Therefore:**

$$
\boxed{\text{getSalary()}}
$$

---

### Example 4 — Identify the Setter

**Question**

Which method changes the value of `age`?

~~~java
class Student {
    private int age;

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}
~~~

**Pattern**

A setter usually starts with `set` and accepts a new value.

**Therefore:**

$$
\boxed{\text{setAge()}}
$$

---

## 6. Advanced Examples

### Example 5 — Validation Through Encapsulation

**Question**

Consider:

~~~java
class Student {
    private int marks;

    public void setMarks(int marks) {
        if (marks >= 0 && marks <= 100) {
            this.marks = marks;
        }
    }

    public int getMarks() {
        return marks;
    }
}
~~~

What happens when:

~~~java
Student s = new Student();

s.setMarks(85);
~~~

**Pattern**

The setter validates the value before updating the private field.

**Calculation**

Check:

$$
0 \leq 85 \leq 100
$$

Condition is true.

Therefore:

```text
marks = 85
```

**Answer:**

$$
\boxed{85}
$$

---

### Example 6 — Invalid Data

**Question**

Using the same class:

~~~java
s.setMarks(120);
~~~

What happens?

**Pattern**

The setter accepts only values between 0 and 100.

**Calculation**

$$
120 > 100
$$

Therefore the condition fails.

The value is not assigned.

If the object was newly created and no previous valid value was assigned, the default value of the instance variable is:

```text
marks = 0
```

**Therefore:**

$$
\boxed{\text{120 is rejected}}
$$

---

### Example 7 — Encapsulation and State Change

**Question**

Consider:

~~~java
class BankAccount {
    private int balance;

    public void deposit(int amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    public int getBalance() {
        return balance;
    }
}
~~~

Now:

~~~java
BankAccount account = new BankAccount();

account.deposit(5000);
account.deposit(2000);
~~~

Find the final balance.

**Pattern**

The private field is changed through controlled methods.

**Calculation**

Initial:

$$
balance=0
$$

After first deposit:

$$
0+5000=5000
$$

After second deposit:

$$
5000+2000=7000
$$

**Therefore:**

$$
\boxed{balance=7000}
$$

---

### Example 8 — Direct Access vs Controlled Access

**Question**

Which design provides better encapsulation?

**Option A**

~~~java
class Account {
    public int balance;
}
~~~

**Option B**

~~~java
class Account {
    private int balance;

    public void deposit(int amount) {
        if (amount > 0) {
            balance += amount;
        }
    }
}
~~~

**Pattern**

Look for restricted data and controlled access.

**Calculation**

Option A:

```text
balance → public
Direct modification → possible
```

Option B:

```text
balance → private
Modification → controlled through deposit()
```

**Therefore:**

$$
\boxed{\text{Option B}}
$$

---

### Example 9 — Read-Only Encapsulation

**Question**

Consider:

~~~java
class Employee {
    private int id;

    public int getId() {
        return id;
    }
}
~~~

Can external code directly modify `id`?

**Pattern**

`id` is private and no setter is provided.

**Calculation**

External code can call:

~~~java
employee.getId();
~~~

But cannot directly write:

~~~java
employee.id = 10;
~~~

**Therefore:**

$$
\boxed{\text{No, id cannot be directly modified from outside the class}}
$$

This is an example of a read-only style of controlled access.

---

## 7. Shortcuts

> [!tip]
> **Shortcut 1: Private + Public Methods**
>
> If you see:
>
> ```text
> private variable
> +
> public getter/setter
> ```
>
> immediately think:
>
> **Encapsulation**

> [!tip]
> **Shortcut 2: "Data Hiding"**
>
> If the question says **data hiding / restricting direct access to data**, think:
>
> **Encapsulation**
>
> Note: Data hiding and encapsulation are closely related, but they are not identical concepts.

> [!tip]
> **Shortcut 3: Getter**
>
> ```text
> getX()
> ```
>
> usually means:
>
> **Read the value**

> [!tip]
> **Shortcut 4: Setter**
>
> ```text
> setX(value)
> ```
>
> usually means:
>
> **Change/update the value**

> [!tip]
> **Shortcut 5: Validation**
>
> If a setter checks whether a value is valid before assigning it:
>
> **Encapsulation is being used to control state changes.**

> [!tip]
> **Shortcut 6: Two-Second Recognition**
>
> Ask:
>
> **"Can outside code directly modify the internal data?"**
>
> If direct access is restricted and controlled through methods, think:
>
> **Encapsulation**

---

## 8. Recognition Tricks

### Pattern 1 — "Bundle Data and Methods"

> [!important]
> If the question says:
>
> **"Combining data and methods into a single unit"**
>
> Think:
>
> **Encapsulation**

---

### Pattern 2 — "Restrict Direct Access"

> [!important]
> If the question says:
>
> **"Prevent direct access to data from outside the class"**
>
> Think:
>
> **Encapsulation**

---

### Pattern 3 — "Private Variables"

> [!important]
> If you see:

~~~java
private int salary;
~~~

and public methods control access, think:

**Encapsulation**

---

### Pattern 4 — "Getter and Setter"

> [!important]
> If you see:

~~~java
getName()
setName()
~~~

with a private field, think:

**Encapsulation / Controlled Access**

---

### Pattern 5 — "Validation"

> [!important]
> If a method validates input before changing an internal variable, think:

**Encapsulation**

Example:

~~~java
if (marks >= 0 && marks <= 100) {
    this.marks = marks;
}
~~~

---

### Pattern 6 — Encapsulation vs Abstraction

> [!important]
> Fast distinction:
>
> **Encapsulation → Controls access to data**
>
> **Abstraction → Hides unnecessary implementation details**
>
> They are related but not the same.

---

## 9. Common Exam Patterns

> [!important] Must Master

### Pattern 1 — Definition of Encapsulation

Identify encapsulation as bundling data and methods together.

### Pattern 2 — Data Hiding

Recognize restricted direct access to internal data.

### Pattern 3 — Private Data Members

Identify `private` fields as a common implementation technique.

### Pattern 4 — Getters and Setters

Understand how methods provide controlled access.

### Pattern 5 — Validation

Trace setters that validate input before modifying state.

### Pattern 6 — Read-Only Object Data

Recognize private data with a getter but no setter.

### Pattern 7 — Controlled State Change

Understand how methods control modifications to internal data.

### Pattern 8 — Encapsulation vs Abstraction

Distinguish access control from implementation hiding.

### Pattern 9 — Access Modifiers

Identify which modifier restricts access most strongly: `private`.

### Pattern 10 — Code Identification

Choose which code properly demonstrates encapsulation.

---

## 10. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking Encapsulation Means Only `private`

`private` is commonly used to implement encapsulation, but encapsulation is the broader concept of bundling data and behavior with controlled access.

Remember:

```text
private → mechanism
encapsulation → concept
```

---

### Mistake 2 — Confusing Encapsulation With Abstraction

They are related but different.

```text
Encapsulation → How access is controlled
Abstraction   → What implementation details are hidden
```

---

### Mistake 3 — Thinking Getters and Setters Are Mandatory

Getters and setters are common ways to provide controlled access, but encapsulation does not require every field to have both.

A class can expose only the operations it actually needs.

---

### Mistake 4 — Making Every Field Public

Example:

~~~java
class Account {
    public double balance;
}
~~~

This allows unrestricted external modification.

Better:

~~~java
class Account {
    private double balance;

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }
}
~~~

---

### Mistake 5 — Assuming `private` Means "Cannot Ever Be Accessed"

A private member cannot be directly accessed from outside its declaring class.

The class itself can access it, and controlled public/protected methods can expose selected operations.

---

### Mistake 6 — Confusing Data Hiding With Complete Invisibility

Encapsulation does not necessarily mean the data can never be accessed.

For example:

~~~java
public int getMarks()
~~~

allows controlled reading while preventing direct field access.

---

## 11. Formula Sheet

```text
Encapsulation = Data + Methods + Controlled Access

private field
→ Restricts direct external access

Getter:
getX()
→ Read/access value

Setter:
setX(value)
→ Modify/update value

Encapsulation
→ Controls access to object state

Common Java Pattern:

private DataType variable;

public DataType getVariable() {
    return variable;
}

public void setVariable(DataType value) {
    variable = value;
}

Encapsulation ≠ Abstraction

Encapsulation → Access control
Abstraction → Hide unnecessary implementation details
```

---

## 12. Quick Revision

> [!summary] One-Minute Revision

- **Encapsulation** bundles data and methods into a single unit.
- It provides **controlled access** to internal data.
- A Java class is commonly used to implement encapsulation.
- `private` is commonly used to restrict direct access.
- Getters are commonly used to read data.
- Setters are commonly used to modify data.
- Validation can be performed before changing state.
- Encapsulation helps protect and control object state.
- Getters and setters are common tools, not mandatory requirements.
- Encapsulation and abstraction are related but different:
  - **Encapsulation → Access control**
  - **Abstraction → Hide unnecessary implementation details**

### Golden Memory Trick

**Encapsulation means keeping data and its operations together while controlling how the outside world accesses that data.**

### One-Line Recognition

**If you see private data with controlled access through methods, think Encapsulation.**