---
type: concept
subject: aptitude
topic: "final Keyword"
parent: "OOPS"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - oops
  - java
  - final-keyword
  - inheritance
  - polymorphism
  - variables
  - methods
  - classes
  - interview
wikilinks:
  - "[[OOPS]]"
  - "[[Inheritance]]"
  - "[[Polymorphism]]"
  - "[[Method Overriding]]"
  - "[[static Keyword]]"
  - "[[Constructors]]"
---

# final Keyword

> [!summary]
> The `final` keyword in Java is used to restrict modification.
>
> It can be applied to:
>
>     final variable
>     → value/reference cannot be reassigned
>
>     final method
>     → cannot be overridden
>
>     final class
>     → cannot be extended
>
> The most important memory trick:
>
>     final variable
>     → cannot reassign
>
>     final method
>     → cannot override
>
>     final class
>     → cannot inherit

# 1. Core Concept

The `final` keyword means:

> **"This cannot be changed in the particular way Java defines for that declaration."**

The exact restriction depends on what `final` is applied to.

There are three major cases:

    final variable
        ↓
    cannot be reassigned

    final method
        ↓
    cannot be overridden

    final class
        ↓
    cannot be extended

This distinction is extremely important for Java interviews.

# 2. Basic Meaning

`final` provides restrictions at the language level.

Example:

    final int x = 10;

After initialization:

    x = 20;

is not allowed.

Similarly:

    final void show()

cannot be overridden.

And:

    final class Vehicle

cannot be extended.

# 3. Three Major Uses

| Usage | Meaning |
|---|---|
| `final variable` | Cannot be reassigned |
| `final method` | Cannot be overridden |
| `final class` | Cannot be extended |

Memory:

    VARIABLE
    → VALUE RESTRICTION

    METHOD
    → OVERRIDING RESTRICTION

    CLASS
    → INHERITANCE RESTRICTION

# 4. Main Formula

There is no mathematical formula, but remember:

$$
\boxed{
final\ variable \rightarrow \text{no reassignment}
}
$$

$$
\boxed{
final\ method \rightarrow \text{no overriding}
}
$$

$$
\boxed{
final\ class \rightarrow \text{no inheritance}
}
$$

# 5. Final Variable

Example:

    final int x = 10;

This is valid:

    System.out.println(x);

This is invalid:

    x = 20;

because a final variable cannot be reassigned after initialization.

# 6. Basic Example

    class Test {

        final int MAX = 100;

        void show() {

            System.out.println(MAX);
        }
    }

The value:

    MAX = 100

cannot later be reassigned.

# 7. Final Variable Recognition

> [!important]
> If the question says:
>
> "value should not be changed after initialization"
>
> think:
>
>     final variable

Example:

    final int MAX_USERS = 100;

# 8. Final Does Not Mean "Always Initialized at Declaration"

A final variable does not always have to be initialized on the same line.

Example:

    final int x;

    x = 10;

This can be valid if `x` is definitely assigned exactly once before use.

This leads to the concept of:

    blank final variable

# 9. Blank Final Variable

A final variable without an initial value is called a blank final variable.

Example:

    final int id;

    id = 101;

After:

    id = 101;

you cannot do:

    id = 102;

The variable receives one assignment.

# 10. Final Local Variable

Example:

    void test() {

        final int x = 10;

        System.out.println(x);
    }

Trying:

    x = 20;

causes a compilation error.

# 11. Final Parameter

Method parameters can also be final.

Example:

    void calculate(
        final int x
    ) {

        System.out.println(x);
    }

Inside the method:

    x = 20;

is not allowed.

The parameter cannot be reassigned.

# 12. Why Use Final Parameters?

A final parameter communicates:

> "This method must not reassign this parameter variable."

Example:

    void process(
        final String name
    ) {

        // name = "Other";
    }

The parameter reference cannot be reassigned.

# 13. Final Instance Variable

Example:

    class Student {

        final int rollNo;

        Student(int rollNo) {

            this.rollNo = rollNo;
        }
    }

This is a common and useful pattern.

Each object receives its own final value.

Example:

    Student s1 =
        new Student(101);

    Student s2 =
        new Student(102);

Then:

    s1.rollNo = 101

    s2.rollNo = 102

Each object's `rollNo` can be initialized once.

# 14. Final Instance Variable Is Not Automatically Static

This distinction is important.

    final int x;

means:

    each object can have
    its own final x

while:

    static final int x = 100;

means:

    one class-level constant

Therefore:

    final
    → cannot reassign

    static
    → class-level/shared

# 15. `final` vs `static final`

| Declaration | Meaning |
|---|---|
| `final int x` | Object-specific value that cannot be reassigned |
| `static final int x` | Class-level value that cannot be reassigned |

Example:

    class Student {

        final int rollNo;

        static final String COLLEGE =
            "ABC";
    }

Here:

    rollNo
    → different for each student

    COLLEGE
    → shared constant

# 16. Final Local Variable vs Final Instance Variable

| Feature | Final Local | Final Instance |
|---|---|---|
| Scope | Method/block | Object |
| Can differ between objects? | Not applicable | Yes |
| Must be assigned before use? | Yes | Yes |
| Can reassign? | No | No |
| Common use | Temporary fixed value | Immutable object state |

# 17. Final Reference Variable

This is one of the most important advanced concepts.

Consider:

    final Student s =
        new Student();

The `final` keyword applies to the reference variable.

You cannot do:

    s = new Student();

But you may be able to modify the object:

    s.name = "Arun";

if `name` itself is not final.

This means:

> **final reference does not automatically mean immutable object.**

# 18. Reference vs Object

Suppose:

    final Student s =
        new Student();

Think:

    s
    ↓
    [Student Object]

`final` prevents:

    s
    ↓
    another object

But it does not automatically prevent changes inside:

    [Student Object]

# 19. Important Example — Final Reference

    class Student {

        String name;
    }

    final Student s =
        new Student();

    s.name = "Pradeep";

This is allowed.

But:

    s = new Student();

is not allowed.

Why?

    s
    → final reference

    s.name
    → mutable object state

# 20. Final Reference Memory Trick

> [!tip]
> Remember:
>
>     final reference
>     ≠
>     immutable object
>
> `final` protects the reference from reassignment.
>
> It does not automatically freeze the object.

# 21. Final Array

The same rule applies to arrays.

Example:

    final int[] arr =
        {10, 20, 30};

This is not allowed:

    arr = new int[]{1, 2, 3};

But this can be allowed:

    arr[0] = 100;

Therefore:

    final array reference
    ≠
    immutable array contents

# 22. Final Object and Mutation

Example:

    final StringBuilder sb =
        new StringBuilder("Hello");

This may be allowed:

    sb.append(" World");

But this is not:

    sb =
        new StringBuilder("Java");

Because:

    append()
    → modifies existing object

    sb = ...
    → reassigns reference

# 23. Final String Reference

Example:

    final String name = "Java";

This cannot be reassigned:

    name = "Python";

Strings themselves are immutable, but that is a separate property from `final`.

Important:

    final
    → reference/variable reassignment restriction

    String immutability
    → String object's content cannot be changed

# 24. Final + Immutable Object

When a final reference points to an immutable object:

    final String name = "Java";

both concepts apply:

    final
    → reference cannot change

    String
    → object content cannot be modified

This creates a stronger immutability situation.

# 25. Final Method

A final method cannot be overridden by a subclass.

Example:

    class Parent {

        final void show() {

            System.out.println(
                "Parent"
            );
        }
    }

A child cannot declare an overriding version of:

    show()

with the same method signature.

# 26. Why Use Final Method?

A final method is used when the parent class wants to guarantee that a particular implementation cannot be replaced by subclasses.

Conceptually:

    Parent
       |
       └── final method
              ↓
        implementation fixed

This can protect important behavior.

# 27. Basic Final Method Example

    class Payment {

        final void validate() {

            System.out.println(
                "Security validation"
            );
        }
    }

    class CreditCardPayment
        extends Payment {

        // Cannot override validate()
    }

The parent guarantees that subclasses cannot replace the validation implementation.

# 28. Real-Time Example — Security Validation

Imagine:

    class BankAccount {

        final void validateSecurity() {

            // Security checks
        }
    }

A subclass should not be able to replace a security-critical method with an unsafe implementation.

Therefore:

    final

can prevent overriding.

# 29. Final Method and Inheritance

A final method is still inherited when accessible.

The restriction is:

    cannot override

It does not mean:

    cannot inherit

This is an important distinction.

# 30. Final Method Recognition

> [!important]
> If the question says:
>
> "subclasses must not change this method's implementation"
>
> think:
>
>     final method

# 31. Final Method Can Be Called

Example:

    class Parent {

        final void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {
    }

    Child c = new Child();

    c.show();

This is valid.

The child inherits the final method and can call it.

# 32. Final Method Cannot Be Overridden

Example:

    class Parent {

        final void show() {
        }
    }

    class Child extends Parent {

        void show() {
        }
    }

This causes a compilation error.

Reason:

    final method
    ↓
    overriding prohibited

# 33. Final Method vs Private Method

A private method cannot be overridden because it is not accessible to subclasses.

A final method cannot be overridden because Java explicitly prohibits overriding.

The reasons are different.

| Method | Can subclass override? |
|---|---|
| `public` | Yes, unless `final` |
| `protected` | Yes, unless `final` |
| package-private | Yes within applicable package rules, unless `final` |
| `private` | No |
| `final` | No |

# 34. Final Method vs Static Method

These are also different concepts.

    final method
    → cannot be overridden

    static method
    → class-level and hidden rather than runtime-overridden

A method can legally be:

    static final

because `final` can prevent static method hiding in a subclass.

# 35. Final Class

A final class cannot be extended.

Example:

    final class Vehicle {

    }

This is invalid:

    class Car extends Vehicle {

    }

because:

    Vehicle
    → final

Therefore:

    Car
    → cannot inherit Vehicle

# 36. Why Use Final Class?

A final class can prevent subclassing.

Reasons may include:

    Security
    Design control
    Preventing modification through inheritance
    Preserving invariants
    Creating immutable types
    API design

# 37. Real-Time Example — String

Java's:

    String

class is final.

Conceptually:

    public final class String

This prevents developers from creating a subclass of String.

This helps preserve the intended behavior and invariants of the String API.

# 38. Real-Time Example — Security Class

Imagine:

    final class SecurityToken {

        // sensitive logic
    }

No class can extend it.

This can prevent subclasses from altering the intended inheritance-based behavior.

# 39. Final Class Recognition

> [!important]
> If the question says:
>
> "No class should inherit from this class"
>
> think:
>
>     final class

# 40. Final Class Can Have Methods

A final class can contain:

    instance methods
    static methods
    final methods
    constructors
    fields

The restriction is specifically:

    cannot be extended

# 41. Final Class Does Not Mean All Methods Are Final

Suppose:

    final class A {

        void show() {
        }
    }

The method does not need the `final` modifier because no subclass can exist to override it.

Therefore:

    final class
    → no subclass

and consequently:

    method overriding through inheritance
    → impossible

# 42. Final Class and Object Creation

A final class can still be instantiated.

Example:

    final class Student {
    }

This is valid:

    Student s =
        new Student();

`final` does not mean:

    cannot create objects

It means:

    cannot extend the class

# 43. Final Class vs Abstract Class

These are almost opposite concepts in an important way.

    abstract class
    → designed to be extended

    final class
    → cannot be extended

Therefore a class cannot meaningfully be declared both:

    abstract final

because one requires subclassing for abstract implementation while the other prohibits subclassing.

# 44. Final Variable vs Final Method vs Final Class

This table should be memorized.

| `final` applied to | Restriction |
|---|---|
| Variable | Cannot be reassigned |
| Method | Cannot be overridden |
| Class | Cannot be extended |

Master trick:

    Variable → Value
    Method   → Override
    Class    → Inheritance

# 45. `final` and Constructors

Constructors cannot be final.

Example:

    final Test() {
    }

is invalid.

Why?

Constructors are not inherited, so there is no constructor overriding to prevent.

# 46. `final` and Static

`final` and `static` solve different problems.

    static
    → class-level

    final
    → restriction

Therefore:

    static int count;

means:

    shared variable

while:

    final int id;

means:

    cannot reassign

And:

    static final int MAX = 100;

means:

    shared
    +
    cannot reassign

# 47. `static final` Constant

This is one of the most common Java patterns.

Example:

    public static final int MAX_SIZE =
        100;

Meaning:

    public
    → accessible

    static
    → class-level

    final
    → cannot reassign

Use:

    Constants.MAX_SIZE

# 48. Naming Convention

Constants are usually written in:

    UPPER_SNAKE_CASE

Examples:

    MAX_SIZE
    MIN_VALUE
    DEFAULT_TIMEOUT
    MAX_RETRIES

This is a convention rather than a compiler rule.

# 49. Final Variable Initialization

A final variable must be definitely assigned exactly once before it is used.

Possible forms:

    final int x = 10;

or:

    final int x;

    x = 10;

Both can be valid depending on scope and definite-assignment rules.

But:

    final int x;

    System.out.println(x);

is invalid because `x` was not initialized.

# 50. Final Local Variable

Example:

    void test() {

        final int x;

        x = 10;

        System.out.println(x);
    }

Valid.

But:

    x = 20;

after the first assignment is invalid.

# 51. Final Instance Variable in Constructor

Example:

    class Student {

        final int id;

        Student(int id) {

            this.id = id;
        }
    }

This is a common pattern.

Each object gets one final ID.

# 52. Final Instance Variable Must Be Initialized

Example:

    class Student {

        final int id;
    }

If no constructor, initializer, or other valid initialization assigns `id`, object construction cannot satisfy the final field requirement.

This leads to a compilation error.

# 53. Multiple Constructors and Final Field

Consider:

    class Student {

        final int id;

        Student() {
        }

        Student(int id) {

            this.id = id;
        }
    }

The no-argument constructor fails because it does not initialize:

    id

Every constructor must ensure the final instance field is definitely assigned.

# 54. Correct Multiple Constructor Pattern

    class Student {

        final int id;

        Student() {

            this(0);
        }

        Student(int id) {

            this.id = id;
        }
    }

Now:

    Student()

delegates to:

    Student(int)

and the final field is initialized exactly once.

# 55. Final Field + Constructor Chaining

This is a powerful pattern:

    final int id;

    Student() {

        this(100);
    }

    Student(int id) {

        this.id = id;
    }

Flow:

    Student()
        ↓
    this(100)
        ↓
    Student(int)
        ↓
    id = 100

# 56. Final Static Variable

A static final field must also be initialized appropriately.

Example:

    static final int MAX = 100;

or through a static initializer:

    static final int MAX;

    static {

        MAX = 100;
    }

The value is assigned once.

# 57. Blank Static Final Variable

Example:

    class Config {

        static final String ENV;

        static {

            ENV = "PRODUCTION";
        }
    }

This is a valid pattern.

The static final variable receives one class-level initialization.

# 58. Final and Methods

A final method can still:

    be called
    be inherited
    be overloaded

But it cannot be:

    overridden

This distinction is important.

# 59. Final Method Can Be Overloaded

Example:

    class Parent {

        final void show() {
        }

        void show(int x) {
        }
    }

A subclass cannot override:

    show()

but can declare a different overloaded method:

    show(int x)

if allowed by normal access/signature rules.

# 60. Overloading vs Overriding Trap

Suppose:

    class Parent {

        final void show() {
        }
    }

    class Child extends Parent {

        void show(int x) {
        }
    }

This is not overriding.

It is a different signature:

    show()
    vs
    show(int)

Therefore overloading is possible.

# 61. Final Method and `@Override`

If you attempt:

    @Override
    void show() {
    }

where parent `show()` is final, the compiler reports an error.

Why?

`@Override` tells the compiler that you intend to override a parent method, but final prevents that.

# 62. Final Class and `@Override`

A final class cannot have subclasses.

Therefore no subclass can override its methods.

This is another reason final classes are useful for preserving behavior.

# 63. Final and Inheritance

Consider:

    class Parent {

        final int x = 10;
    }

    class Child extends Parent {
    }

The field is inherited if accessible, but cannot be reassigned through the child.

Final does not mean:

    not inherited

It means:

    cannot be reassigned.

# 64. Final Field in Parent

Example:

    class Parent {

        protected final int id = 100;
    }

    class Child extends Parent {

        void show() {

            System.out.println(id);
        }
    }

The child can read it if accessible.

But:

    id = 200;

is not allowed.

# 65. Final Variable and Shadowing

A child may declare another field with the same name, depending on visibility and declaration rules.

Example:

    class Parent {

        final int x = 10;
    }

    class Child extends Parent {

        int x = 20;
    }

This does not modify the parent's final field.

The child field is a separate declaration.

This is an advanced distinction between:

    field hiding
    and
    reassignment

# 66. Final Field Is Not Automatically Immutable Object

Example:

    final List<String> names =
        new ArrayList<>();

This is still mutable:

    names.add("Java");

What is prohibited?

    names = new ArrayList<>();

Therefore:

    final reference
    ≠
    immutable object

# 67. Creating Immutable Classes

`final` is often used when designing immutable classes.

Example:

    final class Student {

        private final int id;
        private final String name;

        Student(
            int id,
            String name
        ) {

            this.id = id;
            this.name = name;
        }

        public int getId() {

            return id;
        }

        public String getName() {

            return name;
        }
    }

Important ingredients:

    final class
    +
    private final fields
    +
    initialization in constructor
    +
    no setters
    +
    immutable field types or defensive copies

# 68. Why Make Immutable Class Final?

If an immutable class is not final, a subclass might introduce mutable state or override methods in ways that violate assumptions about immutability.

Making the class final prevents subclass-based modification.

This is one reason classes such as String are final.

# 69. Immutable Class Pattern

> [!important]
> Common immutable-class recipe:
>
>     1. Make class final
>     2. Make fields private
>     3. Make fields final
>     4. Initialize in constructor
>     5. Do not provide setters
>     6. Use immutable field types
>     7. Make defensive copies for mutable objects

# 70. Real-Time Example — Immutable Employee ID

    final class EmployeeId {

        private final int value;

        EmployeeId(int value) {

            this.value = value;
        }

        public int getValue() {

            return value;
        }
    }

Once created:

    EmployeeId id =
        new EmployeeId(101);

the internal value cannot be reassigned.

# 71. Final and Security

Final can help protect design assumptions.

Example:

    class Authentication {

        final boolean isValidToken(
            String token
        ) {

            // security validation
            return true;
        }
    }

A subclass cannot replace that method implementation.

However, `final` is only one design tool; it is not a complete security mechanism.

# 72. Final and Template Method Pattern

A classic design pattern uses a final method to prevent subclasses from changing the overall algorithm.

Example:

    abstract class Report {

        final void generate() {

            loadData();
            processData();
            export();
        }

        abstract void loadData();

        abstract void processData();

        abstract void export();
    }

Here:

    generate()
    → final

Subclasses can customize individual steps but cannot change the overall workflow.

This is called the:

    Template Method Pattern

# 73. Real-Time Example — Payment Workflow

    abstract class Payment {

        final void process() {

            validate();
            authorize();
            complete();
        }

        abstract void validate();

        abstract void authorize();

        abstract void complete();
    }

A subclass can implement:

    validate()
    authorize()
    complete()

but cannot replace the overall:

    process()

workflow.

This is an excellent interview-level use case for `final`.

# 74. Final and API Design

A library designer may use:

    final class

when subclassing would violate invariants.

A library designer may use:

    final method

when a specific implementation must remain unchanged.

A library designer may use:

    final field

when a value should be assigned once.

Therefore `final` is both a language feature and a design-control mechanism.

# 75. Final vs Encapsulation

These concepts are related but different.

Encapsulation:

    controls access

Final:

    controls reassignment/overriding/inheritance

Example:

    private final int id;

means:

    private
    → outside code cannot directly access

    final
    → field cannot be reassigned after initialization

# 76. Final vs Immutability

Do not confuse these.

`final`:

    prevents reassignment

Immutability:

    object state cannot change after creation

Example:

    final Student s =
        new Student();

The reference cannot change, but Student may still be mutable.

# 77. Final vs Constant

A constant is commonly represented as:

    static final

But:

    final

alone does not necessarily mean constant.

Example:

    final int id;

Each object can have a different `id`.

A typical shared constant is:

    static final int MAX_USERS = 100;

# 78. Final vs Read-Only

A final field can be read after initialization but cannot be reassigned.

However, if it references a mutable object, the object's internal state may still change.

Therefore:

    final
    ≠
    deeply read-only

# 79. Final and Primitive Values

Example:

    final int x = 10;

The value cannot be changed:

    x = 20;

invalid.

For primitives, this is straightforward because the variable directly stores the value.

# 80. Final and Reference Values

Example:

    final Student s =
        new Student();

The reference cannot change:

    s = anotherStudent;

invalid.

But:

    s.name = "New Name";

may be valid if `name` is mutable.

# 81. Primitive vs Reference Final

| Type | What final prevents |
|---|---|
| Primitive | Changing stored value |
| Reference | Reassigning reference |
| Mutable object reference | Does not freeze object's internal state |

This is a high-priority interview concept.

# 82. Output Question 1 — Final Variable

    final int x = 10;

    x = 20;

Result:

    Compilation Error

Reason:

    final variable
    → cannot be reassigned

# 83. Output Question 2 — Final Reference

    class Student {

        String name;
    }

    final Student s =
        new Student();

    s.name = "Arun";

This is valid.

Why?

    s
    → final reference

    s.name
    → mutable object field

# 84. Output Question 3 — Final Reference Reassignment

    class Student {
    }

    final Student s =
        new Student();

    s = new Student();

Result:

    Compilation Error

Reason:

    final reference
    → cannot be reassigned

# 85. Output Question 4 — Final Method

    class Parent {

        final void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {

        void show() {

            System.out.println(
                "Child"
            );
        }
    }

Result:

    Compilation Error

Reason:

    final method
    → cannot be overridden

# 86. Output Question 5 — Final Class

    final class Parent {
    }

    class Child extends Parent {
    }

Result:

    Compilation Error

Reason:

    final class
    → cannot be extended

# 87. Output Question 6 — Final Method Can Be Called

    class Parent {

        final void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {
    }

    new Child().show();

Output:

    Parent

The method is inherited and callable.

# 88. Output Question 7 — Final Method Overloading

    class Parent {

        final void show() {

            System.out.println("A");
        }
    }

    class Child extends Parent {

        void show(int x) {

            System.out.println("B");
        }
    }

    Child c = new Child();

    c.show();
    c.show(10);

Output:

    A
    B

Why?

    show()
    → inherited final method

    show(int)
    → separate overloaded method

# 89. Output Question 8 — Final Static Constant

    class Config {

        static final int MAX = 100;
    }

    System.out.println(
        Config.MAX
    );

Output:

    100

# 90. Output Question 9 — Final Field in Constructor

    class Student {

        final int id;

        Student(int id) {

            this.id = id;
        }
    }

    Student s =
        new Student(101);

    System.out.println(s.id);

Output:

    101

The field was initialized once.

# 91. Output Question 10 — Final Field Assigned Twice

    class Student {

        final int id;

        Student(int id) {

            this.id = id;
            this.id = 200;
        }
    }

Result:

    Compilation Error

A final field cannot be assigned twice.

# 92. Output Question 11 — Final Parameter

    void show(
        final int x
    ) {

        x = 20;
    }

Result:

    Compilation Error

Reason:

    final parameter
    → cannot be reassigned

# 93. Output Question 12 — Final Array

    final int[] arr =
        {10, 20, 30};

    arr[0] = 100;

This is valid.

But:

    arr = new int[]{1, 2, 3};

is invalid.

# 94. Output Question 13 — Static Final

    class Test {

        static final int x = 10;
    }

    Test.x = 20;

Result:

    Compilation Error

Reason:

    final
    → no reassignment

# 95. Output Question 14 — Final Class Object

    final class Test {
    }

    Test t =
        new Test();

This is valid.

Final class means:

    cannot extend

not:

    cannot instantiate

# 96. Output Question 15 — Final Class + Method

    final class Test {

        void show() {

            System.out.println(
                "Hello"
            );
        }
    }

    new Test().show();

Output:

    Hello

The class being final does not prevent object creation.

# 97. Output Question 16 — Final Instance Fields

    class Student {

        final int id;
        final String name;

        Student(
            int id,
            String name
        ) {

            this.id = id;
            this.name = name;
        }
    }

    Student s =
        new Student(
            101,
            "Arun"
        );

Both fields are assigned once.

# 98. Output Question 17 — Final Field + Multiple Objects

    class Student {

        final int id;

        Student(int id) {

            this.id = id;
        }
    }

    Student s1 =
        new Student(101);

    Student s2 =
        new Student(102);

Output:

    s1.id = 101
    s2.id = 102

Final does not mean all objects must have the same value.

It means each object's field cannot be reassigned after initialization.

# 99. Output Question 18 — Final vs Static Final

    class Student {

        final int id;
        static final String COLLEGE =
            "ABC";

        Student(int id) {

            this.id = id;
        }
    }

Create:

    Student s1 =
        new Student(101);

    Student s2 =
        new Student(102);

Then:

    s1.id = 101
    s2.id = 102

while:

    Student.COLLEGE = "ABC"

for all students.

# 100. Output Question 19 — Final Method + Runtime Reference

    class Parent {

        final void show() {

            System.out.println(
                "Parent"
            );
        }
    }

    class Child extends Parent {
    }

    Parent p = new Child();

    p.show();

Output:

    Parent

The child cannot override the final method.

# 101. Output Question 20 — Final Method + Overloading

    class Parent {

        final void show() {

            System.out.println("A");
        }
    }

    class Child extends Parent {

        void show(int x) {

            System.out.println("B");
        }
    }

    Child c = new Child();

    c.show(10);

Output:

    B

This is overloading, not overriding.

# 102. Common Exam Patterns

> [!important] Must Master

1. Meaning of `final`
2. Final variable
3. Final local variable
4. Final parameter
5. Final instance variable
6. Final static variable
7. Blank final variable
8. Blank final static variable
9. Final reference
10. Final array
11. Final object mutation
12. Final method
13. Final method inheritance
14. Final method overriding
15. Final method overloading
16. Final class
17. Final class inheritance restriction
18. Final class object creation
19. `static final`
20. Constants
21. Final vs immutable
22. Final vs encapsulation
23. Final vs static
24. Final vs abstract
25. Final vs private
26. Final and constructors
27. Final fields in constructors
28. Final fields and constructor chaining
29. Immutable class design
30. Template Method Pattern
31. Security-related design
32. Reference reassignment
33. Mutable object through final reference
34. Final arrays
35. Output-based final questions

# 103. Shortcuts

> [!tip]
> **Shortcut 1 — Three Words**
>
>     final variable
>     → no reassignment
>
>     final method
>     → no overriding
>
>     final class
>     → no inheritance

> [!tip]
> **Shortcut 2 — Final Reference**
>
>     final reference
>     → reference cannot change
>
>     object may still change

> [!tip]
> **Shortcut 3 — Constants**
>
> If you see:
>
>     static final
>
> think:
>
>     class-level constant

> [!tip]
> **Shortcut 4 — Final Method**
>
> If parent method is:
>
>     final
>
> immediately think:
>
>     Child cannot override it.

> [!tip]
> **Shortcut 5 — Final Class**
>
> If class is:
>
>     final
>
> immediately think:
>
>     extends → compilation error

> [!tip]
> **Shortcut 6 — Constructor**
>
> If you see:
>
>     final int id;
>
> find where `id` is initialized.
>
> If it is never definitely assigned:
>
>     Compilation Error

> [!tip]
> **Shortcut 7 — Final Array**
>
>     final int[] arr
>
> means:
>
>     arr = anotherArray
>     → not allowed
>
>     arr[0] = value
>     → may be allowed

> [!tip]
> **Shortcut 8 — Final Does Not Mean Static**
>
>     final
>     → restriction
>
>     static
>     → class-level

> [!tip]
> **Shortcut 9 — Final Does Not Mean Immutable**
>
> Ask:
>
>     Is the reference final?
>     OR
>     Is the object immutable?
>
> They are different concepts.

> [!tip]
> **Shortcut 10 — Abstract vs Final**
>
>     abstract
>     → designed for inheritance
>
>     final
>     → prevents inheritance
>
> Never treat them as interchangeable.

# 104. Recognition Tricks

> [!important]
> **If the question says "cannot be changed", first check whether it means a variable reassignment → `final variable`.**

> [!important]
> **If the question says "subclass cannot change the implementation", think `final method`.**

> [!important]
> **If the question says "class cannot be inherited", think `final class`.**

> [!important]
> **If the question says "constant shared by all objects", think `static final`.**

> [!important]
> **If a final reference points to a mutable object, remember that object mutation may still be possible.**

> [!important]
> **If a final field is not initialized in every valid constructor path, think compilation error.**

> [!important]
> **If a final method appears with the same signature in a child, think compilation error.**

> [!important]
> **If a final class appears after `extends`, think compilation error.**

> [!important]
> **If `final` and `abstract` appear together on a class, think invalid design/language combination because abstract requires subclassing while final prohibits it.**

# 105. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Thinking `final` Means Constant

Wrong:

    final = constant

Correct:

    final
    → cannot be reassigned

A final instance variable can have a different value for every object.

---

### Mistake 2 — Thinking Final Reference Makes Object Immutable

Wrong:

    final Student s
    → Student cannot change

Correct:

    s cannot point to another object

but:

    s.name

may still change.

---

### Mistake 3 — Thinking Final Class Cannot Be Instantiated

Wrong:

    final class
    → cannot create object

Correct:

    final class
    → cannot extend

You can still write:

    new FinalClass();

---

### Mistake 4 — Thinking Final Method Cannot Be Called

Wrong:

    final method
    → cannot call

Correct:

    final method
    → can call
    → cannot override

---

### Mistake 5 — Thinking Final Means Static

Wrong:

    final
    =
    shared

Correct:

    final
    → reassignment restriction

    static
    → class-level association

---

### Mistake 6 — Forgetting Final Fields Need Initialization

A final field must receive a valid assignment before use.

---

### Mistake 7 — Confusing Overloading With Overriding

A final method cannot be overridden, but a subclass may still define an overloaded method with a different parameter list.

---

### Mistake 8 — Thinking Final Makes an Array Immutable

A final array reference can still have its elements modified.

---

### Mistake 9 — Thinking Final Method Is Private

They solve different problems.

    private
    → access restriction

    final
    → overriding restriction

---

### Mistake 10 — Thinking Final Class Is Abstract

They are conceptually opposite in inheritance behavior.

    abstract
    → must be extended/implemented

    final
    → cannot be extended

# 106. Final vs `static`

This comparison is extremely important.

| Feature | `final` | `static` |
|---|---|---|
| Main idea | Restriction | Class-level association |
| Variable | Cannot reassign | Shared |
| Method | Cannot override | Class-level method |
| Class | Cannot extend | Not applicable as class modifier |
| Object required? | Depends | Static member does not require object |
| Common combination | `static final` | `static final` |

Memory:

    final
    → FIXED

    static
    → SHARED

# 107. Final vs Abstract

| Feature | `final` | `abstract` |
|---|---|---|
| Class inheritance | Prevented | Expected |
| Method implementation | Must have implementation if final | Abstract method has no implementation body |
| Purpose | Restrict modification | Provide incomplete abstraction |
| Subclassing | No for final class | Required/useful |
| Typical goal | Preserve behavior | Allow specialization |

Memory:

    final
    → STOP EXTENSION

    abstract
    → REQUIRE EXTENSION

# 108. Final vs Private

| Feature | `final` | `private` |
|---|---|---|
| Main concern | Modification/overriding | Access |
| Variable | Cannot reassign | Only declaring class can directly access |
| Method | Cannot override | Not accessible to subclasses |
| Class | Can be final | Top-level classes cannot be private |
| Purpose | Restriction | Encapsulation |

# 109. Final vs Immutable

| Concept | Meaning |
|---|---|
| `final` variable | Cannot reassign variable |
| Final reference | Cannot point to another object |
| Immutable object | Object state cannot change |
| `static final` | Shared non-reassignable field |

Example:

    final List<Integer> list =
        new ArrayList<>();

The reference is final.

The list itself may still be mutable.

# 110. Final and Object-Oriented Design

`final` is important for controlling extension points.

A class designer can decide:

    What can change?
    What can be overridden?
    What can be inherited?

For example:

    final method
    → fixed algorithm step

    abstract method
    → customizable algorithm step

This combination is heavily used in framework and library design.

# 111. Template Method Pattern

Consider:

    abstract class DataProcessor {

        final void process() {

            read();
            validate();
            save();
        }

        abstract void read();

        abstract void validate();

        abstract void save();
    }

The algorithm:

    process()

is fixed.

Subclasses customize:

    read()
    validate()
    save()

This is a powerful example of:

    final
    +
    abstraction
    +
    polymorphism

# 112. Real-Time Example — Banking

Imagine:

    abstract class BankTransaction {

        final void execute() {

            authenticate();
            validate();
            process();
            audit();
        }

        abstract void authenticate();

        abstract void validate();

        abstract void process();

        abstract void audit();
    }

The overall workflow cannot be replaced.

But each transaction type can implement its own details.

This is a strong real-world design pattern.

# 113. Real-Time Example — E-Commerce Order

    abstract class OrderProcessor {

        final void processOrder() {

            validateOrder();
            calculatePrice();
            processPayment();
            shipOrder();
        }

        abstract void validateOrder();

        abstract void calculatePrice();

        abstract void processPayment();

        abstract void shipOrder();
    }

The final method ensures the high-level workflow remains fixed.

# 114. Real-Time Example — Security

    class SecurityService {

        final boolean validateToken(
            String token
        ) {

            // validation logic
            return true;
        }
    }

Subclasses cannot override the validation method.

This can be useful when preserving critical behavior is a design requirement.

# 115. Real-Time Example — Employee Identity

    final class EmployeeId {

        private final int id;

        EmployeeId(int id) {

            this.id = id;
        }

        public int getId() {

            return id;
        }
    }

This is a common immutable-value-object style.

# 116. Advanced Concept — Final Field and Thread Safety

Final fields have special guarantees in Java's memory model when properly initialized through constructors.

A correctly constructed object with final fields provides stronger visibility guarantees for those final fields than ordinary mutable fields.

For placement interviews, remember:

> [!important]
> Properly initialized final fields are useful when designing safely published immutable objects.

Do not simplify this into:

    final = automatically thread-safe

because final does not make an entire object thread-safe.

# 117. Advanced Concept — Final Does Not Guarantee Deep Immutability

Example:

    final class User {

        private final List<String> roles;

        User(List<String> roles) {

            this.roles = roles;
        }

        public List<String> getRoles() {

            return roles;
        }
    }

The field is final, but the list may still be mutable.

Better immutable design may require:

    defensive copying

and:

    unmodifiable views

or immutable collections.

# 118. Advanced Concept — Defensive Copy

Instead of directly storing a mutable collection:

    this.roles = roles;

a stronger immutable design can create a copy:

    this.roles =
        List.copyOf(roles);

Now external callers cannot mutate the internal list through the original mutable reference.

This demonstrates:

    final
    +
    immutable/defensive data handling

# 119. Advanced Concept — Final Reference and Garbage Collection

Consider:

    final Student s =
        new Student();

As long as `s` remains reachable, the referenced object remains reachable through that reference.

`final` does not mean:

    object can never be garbage collected

Once the containing scope/object is no longer reachable, normal garbage collection rules apply.

# 120. Advanced Concept — Final Variable and Optimization

The compiler/JVM may perform optimizations involving final values in appropriate circumstances, but developers should not assume a simplistic "final always gets replaced at compile time" rule.

For interviews:

    final
    → semantic restriction

Optimization:
    → implementation detail

# 121. Advanced Concept — Constant Variables

Java has a specific concept of constant variables, generally involving:

    final
    +
    primitive or String
    +
    constant expression

Example:

    static final int MAX = 100;

Such compile-time constants can be treated specially by the compiler.

Do not assume every final variable is a compile-time constant.

# 122. Constant Variable vs Final Variable

Example:

    final int x = 10;

may be a constant variable if it satisfies Java's constant-expression rules.

But:

    final int x =
        getValue();

is final but not a compile-time constant.

Therefore:

    final
    ≠
    compile-time constant

# 123. Advanced Interview Question — Is Every Final Variable a Constant?

No.

A final variable only guarantees that it is assigned at most once.

A compile-time constant must satisfy additional Java language rules.

# 124. Advanced Interview Question — Can a Final Variable Be Initialized in Constructor?

Yes.

Example:

    class Student {

        final int id;

        Student(int id) {

            this.id = id;
        }
    }

Each object can receive its own final value.

# 125. Advanced Interview Question — Can a Final Variable Be Initialized in a Method?

A local final variable can be initialized in a method.

Example:

    void test() {

        final int x;

        x = 10;
    }

But a final instance field cannot be arbitrarily assigned in an ordinary method because the compiler must ensure definite assignment for every valid construction path.

# 126. Advanced Interview Question — Can a Final Method Be Overloaded?

Yes.

Example:

    final void show()

and:

    void show(int x)

have different signatures.

Overloading is not overriding.

# 127. Advanced Interview Question — Can a Final Method Be Static?

Yes.

Example:

    static final void show() {
    }

This means:

    static
    → class-level

    final
    → prevents method hiding

# 128. Advanced Interview Question — Can a Final Class Have Final Methods?

Yes.

Example:

    final class A {

        final void show() {
        }
    }

The method does not need to be final because the class itself cannot be subclassed, but the declaration is still legal.

# 129. Advanced Interview Question — Can a Final Class Be Extended?

No.

Example:

    final class A {
    }

    class B extends A {
    }

Compilation error.

# 130. Advanced Interview Question — Can a Final Class Be Instantiated?

Yes.

Example:

    final class A {
    }

    A obj = new A();

This is completely valid.

# 131. Advanced Interview Question — Can a Constructor Be Final?

No.

Constructors cannot be inherited or overridden, so `final` is not applicable to them.

# 132. Advanced Interview Question — Can an Abstract Class Be Final?

No.

An abstract class is designed to require subclass implementation, while a final class prohibits subclassing.

# 133. Advanced Interview Question — Can an Abstract Method Be Final?

No.

An abstract method requires overriding, while a final method prohibits overriding.

# 134. Advanced Interview Question — Can a Final Reference Point to a Mutable Object?

Yes.

Example:

    final ArrayList<Integer> list =
        new ArrayList<>();

You cannot reassign:

    list = anotherList;

but you may modify:

    list.add(10);

# 135. Advanced Interview Question — Does Final Make an Object Immutable?

No.

Final restricts reassignment of the variable/reference.

Object immutability is a property of the object's design.

# 136. Advanced Interview Question — Why Is String Final?

String is final so it cannot be subclassed and its carefully designed immutable behavior cannot be altered through inheritance.

# 137. Advanced Interview Question — Why Is `Integer` Final?

Wrapper classes such as `Integer` are final, which prevents subclassing and helps preserve their immutable value semantics and API behavior.

# 138. Advanced Interview Question — What Is a Blank Final Variable?

A final variable declared without an initial value and assigned exactly once later.

Example:

    final int id;

    id = 100;

# 139. Advanced Interview Question — What Is a Final Parameter?

A method parameter declared final cannot be reassigned inside that method.

Example:

    void show(final int x) {
    }

# 140. Advanced Interview Question — Why Use Final Fields?

Final fields can help create objects whose important state is assigned once during construction.

This improves:

    correctness
    readability
    immutability design
    thread-safety reasoning

# 141. Master Decision Tree

When you see `final`:

    What is it applied to?

          |
          +----------------------+
          |          |           |
       variable    method       class
          |          |           |
          ↓          ↓           ↓
    no reassign   no override   no extend

Then ask:

    Is static also present?

          |
          ↓

    static final
          ↓
    shared class-level
    non-reassignable value

# 142. Final Variable Problem-Solving Framework

For a final variable:

    Step 1
    Find declaration.

    Step 2
    Check whether initialized.

    Step 3
    Find all assignments.

    Step 4
    Verify exactly one valid assignment.

    Step 5
    Check whether object/reference
    mutation is separate from reassignment.

# 143. Final Method Problem-Solving Framework

For a final method:

    Step 1
    Find parent declaration.

    Step 2
    Check final.

    Step 3
    Search child for same signature.

    Step 4
    If same signature exists:
        compilation error

    Step 5
    If different parameters:
        possible overloading

# 144. Final Class Problem-Solving Framework

For a final class:

    Step 1
    Identify final class.

    Step 2
    Search for extends.

    Step 3
    If another class extends it:
        compilation error

    Step 4
    Object creation:
        still allowed

# 145. Exam-Speed Recognition Table

| Question Wording | Think |
|---|---|
| Value cannot change | `final variable` |
| Shared fixed value | `static final` |
| Method cannot be changed by subclass | `final method` |
| Class cannot be inherited | `final class` |
| Object reference cannot change | `final reference` |
| Object itself cannot change | Immutability |
| Class-level constant | `static final` |
| Subclass must customize | `abstract` |
| Subclass must not customize | `final` |
| Same method, different parameters | Overloading |
| Same method, same signature | Overriding |
| Final method + subclass override | Compilation error |
| Final class + extends | Compilation error |
| Final reference + object mutation | May be valid |

# 146. Common Interview Traps

> [!warning]
> **Trap 1**
>
>     final = immutable
>
> False.
>
> Final prevents reassignment; it does not automatically make an object immutable.

> [!warning]
> **Trap 2**
>
>     final class = cannot create object
>
> False.
>
> You can instantiate a final class.

> [!warning]
> **Trap 3**
>
>     final method = cannot call
>
> False.
>
> It can be called normally.

> [!warning]
> **Trap 4**
>
>     final = static
>
> False.
>
> Final means restriction; static means class-level association.

> [!warning]
> **Trap 5**
>
>     final method = private
>
> False.
>
> Final controls overriding; private controls access.

> [!warning]
> **Trap 6**
>
>     final reference = immutable object
>
> False.
>
> The reference cannot change; object state may still change.

> [!warning]
> **Trap 7**
>
>     final method can be overridden if child uses @Override
>
> False.
>
> `@Override` cannot bypass final.

> [!warning]
> **Trap 8**
>
>     abstract final class
>
> Invalid combination.

# 147. Professional Design Pattern

A common high-quality Java class design is:

    public final class EmployeeId {

        private final int value;

        public EmployeeId(int value) {

            this.value = value;
        }

        public int getValue() {

            return value;
        }
    }

Why this is strong:

    final class
    → no subclass modification

    private field
    → encapsulation

    final field
    → one-time assignment

    no setter
    → no reassignment API

This pattern is useful for immutable value objects.

# 148. Final + Encapsulation + Immutability

These concepts work together:

    private
       ↓
    controls access

    final
       ↓
    controls reassignment

    immutable object
       ↓
    controls state changes

Example:

    final class User {

        private final String name;

        User(String name) {

            this.name = name;
        }

        public String getName() {

            return name;
        }
    }

This is much stronger than using `final` alone.

# 149. Real-Time Example — Configuration Object

    final class AppConfig {

        private final String environment;
        private final int port;

        AppConfig(
            String environment,
            int port
        ) {

            this.environment = environment;
            this.port = port;
        }

        public String getEnvironment() {

            return environment;
        }

        public int getPort() {

            return port;
        }
    }

Once constructed, the configuration values are fixed.

# 150. Real-Time Example — Order ID

    final class OrderId {

        private final String value;

        OrderId(String value) {

            this.value = value;
        }

        public String getValue() {

            return value;
        }
    }

This prevents accidental reassignment of the identifier.

# 151. Real-Time Example — Payment Workflow

    abstract class Payment {

        final void process() {

            validate();
            authorize();
            complete();
        }

        abstract void validate();

        abstract void authorize();

        abstract void complete();
    }

Important pattern:

    final process()
        +
    abstract steps

This means:

    overall workflow fixed
    individual steps customizable

# 152. High-Level Interview Answer

### Explain the `final` keyword in Java.

A strong answer:

> "`final` is used to restrict modification. A final variable cannot be reassigned after valid initialization, a final method cannot be overridden by subclasses, and a final class cannot be extended. A final reference can still point to a mutable object, so final does not automatically mean object immutability."

# 153. High-Level Interview Answer

### Difference between final variable and constant?

A final variable can be assigned only once, but not every final variable is a compile-time constant.

A typical Java constant is:

    static final

and often initialized with a compile-time constant expression.

# 154. High-Level Interview Answer

### Does final make an object immutable?

No.

For:

    final Student s =
        new Student();

the reference cannot be reassigned, but the Student object's mutable fields may still change.

# 155. High-Level Interview Answer

### Why use a final method?

A final method prevents subclasses from overriding a particular implementation. It is useful when a parent class must preserve a specific behavior or algorithm step.

# 156. High-Level Interview Answer

### Why use a final class?

A final class prevents inheritance. This can be useful for immutable classes, security-sensitive designs, API control, and preserving class invariants.

# 157. High-Level Interview Answer

### Can final methods be overloaded?

Yes.

Final prevents overriding, not overloading.

Example:

    final void show()

can coexist with:

    void show(int x)

# 158. High-Level Interview Answer

### Can a final variable be initialized in a constructor?

Yes.

A final instance field can be initialized once in a constructor.

# 159. High-Level Interview Answer

### Can final reference object's state change?

Yes, if the referenced object is mutable.

Example:

    final List<Integer> list =
        new ArrayList<>();

    list.add(10);

This may be valid.

# 160. High-Level Interview Answer

### Why can a final class be instantiated?

Because `final` restricts inheritance, not object creation.

Example:

    final class A {
    }

    A a = new A();

is valid.

# 161. High-Level Interview Answer

### Can constructors be final?

No.

Constructors are not inherited or overridden, so `final` is not applicable.

# 162. High-Level Interview Answer

### Can abstract and final be used together?

No for a class or method in the contradictory cases relevant here.

An abstract class/method requires subclass implementation/overriding, while final prevents extension/overriding.

# 163. Formula Sheet

```text
FINAL KEYWORD

final variable
→ Cannot be reassigned

final method
→ Cannot be overridden

final class
→ Cannot be extended

Master Memory:

VARIABLE
→ VALUE FIXED

METHOD
→ OVERRIDE FIXED

CLASS
→ INHERITANCE FIXED


Final reference:

final Student s = new Student();

Allowed:
s.name = "Arun";

Not allowed:
s = new Student();


Final array:

final int[] arr = {1, 2, 3};

Allowed:
arr[0] = 100;

Not allowed:
arr = new int[]{4, 5, 6};


Final parameter:

void test(final int x)

x cannot be reassigned inside test.


Blank final:

final int x;

x = 10;

Can be valid if definitely assigned exactly once.


Final instance field:

class Student {

    final int id;

    Student(int id) {
        this.id = id;
    }
}


Static final:

static final int MAX_SIZE = 100;

→ Shared class-level fixed value


final class:

final class A {
}

class B extends A {
}

→ Compilation Error


final method:

class A {

    final void show() {
    }
}

class B extends A {

    void show() {
    }
}

→ Compilation Error


Final method can be overloaded:

final void show()

void show(int x)

→ Valid


Final ≠ Immutable

final reference
→ reference cannot change

immutable object
→ object state cannot change


Final ≠ Static

final
→ restriction

static
→ class-level


Final vs Abstract:

final
→ prevents extension

abstract
→ designed for extension


Final constructor:

Not allowed.


Typical immutable class:

final class
+
private final fields
+
constructor initialization
+
no setters
+
immutable fields/defensive copies


Template Method:

final process()
+
abstract steps

→ fixed algorithm
→ customizable steps