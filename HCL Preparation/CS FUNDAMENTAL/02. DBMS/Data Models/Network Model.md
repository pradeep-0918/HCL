---
type: concept
subject: dbms
topic: "Network Model"
parent: "Data Models"
company: HCL
difficulty: medium
priority: high
status: not-started
tags:
  - dbms
  - data-models
  - network-model
  - graph-model
  - database
  - hierarchical-model
  - relational-model
  - hcl
  - tcs
  - infosys
  - zoho
  - accenture
  - cs-fundamentals
  - interview
wikilinks:
  - "[[Data Models]]"
  - "[[Hierarchical Model]]"
  - "[[Relational Model]]"
  - "[[ER Model]]"
  - "[[Database]]"
  - "[[DBMS Architecture]]"
---

# Network Model

## 1. Core Concept

> [!summary]
> The **Network Data Model** organizes data as a **graph-like structure** in which records can have multiple relationships and a child record can be connected to multiple parent records.

The easiest mental model is:

~~~text
Hierarchical Model
        ↓
      TREE

Network Model
        ↓
      GRAPH
~~~

The major difference is:

~~~text
Hierarchical:
One Child → Generally One Parent

Network:
One Child → Can Have Multiple Parents
~~~

This makes the network model more flexible than the classical hierarchical model for representing complex relationships.

---

# 2. Basic Meaning

The network model represents database information using:

- Records
- Record types
- Sets
- Owner-member relationships
- Links
- Multiple paths

Instead of forcing every record into a single tree, the network model allows records to participate in multiple relationships.

Think:

~~~text
        A
       / \
      B   C
       \ /
        D
~~~

Here, `D` can be connected to both `B` and `C`.

This type of structure is difficult in a strict hierarchical model but natural in a network-style model.

---

# 3. Main Idea

The central idea is:

**Data can have multiple interconnected relationships.**

Example:

~~~text
        Department
        /        \
       /          \
  Student        Course
       \          /
        \        /
         Enrollment
~~~

A student can belong to a department and take many courses.

A course can have many students.

The network model can represent such interconnected relationships more naturally than a strict tree.

---

# 4. Tree vs Graph Intuition

### Hierarchical Model

~~~text
             Root
               |
        +------+------+
        |             |
     Parent A      Parent B
        |             |
     Child A       Child B
~~~

A child generally has one parent.

### Network Model

~~~text
       A
      / \
     B   C
      \ /
       D
~~~

A node can participate in multiple connections.

Memory:

~~~text
Hierarchical
→ Tree
→ Single-parent orientation

Network
→ Graph
→ Multiple connections
~~~

---

# 5. Why Was the Network Model Needed?

The hierarchical model works well when data naturally forms:

~~~text
Parent
   ↓
Child
   ↓
Grandchild
~~~

But real-world data often looks like:

~~~text
Student
   ↕
Course

Employee
   ↕
Project

Doctor
   ↕
Patient

Supplier
   ↕
Product
~~~

These are often many-to-many relationships.

A strict tree cannot represent these relationships naturally.

The network model provides a more flexible structure.

---

# 6. Core Components

Important concepts include:

1. Record
2. Record Type
3. Set Type
4. Owner
5. Member
6. Set Relationship
7. Links
8. Navigational Access
9. Multiple Paths

These are important for interviews.

---

# 7. Record

A **record** represents a collection of related data items.

Example:

~~~text
Student Record

Student_ID
Name
Department
CGPA
~~~

Another:

~~~text
Course Record

Course_ID
Course_Name
Credits
~~~

Records are the basic units of stored information.

---

# 8. Record Type

A **record type** defines the structure of a group of similar records.

Example:

~~~text
STUDENT
----------------
Student_ID
Name
Department
CGPA
~~~

All student records follow this structure.

Similarly:

~~~text
COURSE
----------------
Course_ID
Course_Name
Credits
~~~

The important distinction:

~~~text
Record Type
→ Structure / Definition

Record
→ Individual Stored Instance
~~~

---

# 9. Set Type

The network model commonly uses **set types** to represent relationships between record types.

A set type consists conceptually of:

~~~text
OWNER
  ↓
MEMBER
~~~

Example:

~~~text
Department
    ↓
  Student
~~~

Here:

~~~text
Department
→ Owner

Student
→ Member
~~~

---

# 10. Owner and Member

This is an important network-model concept.

Example:

~~~text
Department
     |
     +--- Student 1
     +--- Student 2
     +--- Student 3
~~~

Conceptually:

~~~text
Department
→ Owner

Student
→ Member
~~~

The owner-member relationship connects records through a set type.

---

# 11. Multiple Set Membership

A major strength of the network model is that a record can participate in multiple relationships.

Example:

~~~text
Student
  |
  +--- belongs to → Department
  |
  +--- enrolled in → Course
  |
  +--- lives in → Hostel
~~~

The same student record can participate in multiple sets.

This provides much greater flexibility than a strict tree.

---

# 12. Many-to-Many Relationship

The network model is much better suited to many-to-many relationships.

Example:

~~~text
Student
   ↕
Course
~~~

Suppose:

~~~text
Student A
→ Database
→ Operating Systems

Student B
→ Database
→ Networks
~~~

And:

~~~text
Database
→ Student A
→ Student B
~~~

The same course is connected to multiple students.

The same student is connected to multiple courses.

This is many-to-many.

---

# 13. Why Hierarchical Struggles Here

Consider:

~~~text
Student A
   ↙   ↘
Course 1  Course 2
```

Now Course 1 also belongs to:

~~~text
Student B
```

The structure becomes:

~~~text
Student A ─── Course 1 ─── Student B
      \                       /
       \                     /
          Course 2
~~~

This is no longer a simple tree.

It is graph-like.

Therefore:

~~~text
Tree
→ Hierarchical

Graph
→ Network
~~~

---

# 14. Main Characteristics

The network model has these important characteristics:

1. Graph-like structure
2. Multiple relationships
3. Multiple paths
4. Record types
5. Set types
6. Owner-member relationships
7. Navigational access
8. Better support for many-to-many relationships
9. More flexible than hierarchical structures
10. More complex to design and navigate

---

# 15. Network Model Structure

Example:

~~~text
                 Department
                /          \
               /            \
              ↓              ↓
          Student          Course
              \              /
               \            /
                \          /
                 Enrollment
~~~

The key idea is not necessarily the exact diagram but the existence of multiple interconnected paths.

---

# 16. Navigational Access

Like the hierarchical model, the network model is traditionally associated with **navigational access**.

The application follows links between records.

Example:

~~~text
Student
   ↓
Enrollment
   ↓
Course
```

or:

~~~text
Student
   ↓
Department
   ↓
Faculty
~~~

The programmer navigates through relationships.

---

# 17. Path-Based Navigation

Suppose:

~~~text
Student
   ↓
Enrollment
   ↓
Course
   ↓
Instructor
~~~

The application can follow:

~~~text
Student
→ Enrollment
→ Course
→ Instructor
~~~

Another path might be:

~~~text
Student
→ Department
→ Instructor
~~~

Multiple paths are possible.

This is one of the major differences from a strict hierarchy.

---

# 18. Multiple Parent Concept

One of the most important interview points:

~~~text
Hierarchical Model
→ Child generally has one parent

Network Model
→ Record can participate in multiple relationships
```

Example:

~~~text
             Department
                 |
                 ↓
              Student
                 ↑
                 |
               Course
~~~

The student can be connected to both Department and Course.

---

# 19. Network Model as Graph

Think of the network model as:

~~~text
Nodes
+
Relationships
+
Multiple Paths
~~~

For example:

~~~text
       A
      / \
     B   C
     | \ |
     |  \|
     D---E
~~~

There can be several routes between records.

This flexibility is the defining intuition of the network model.

---

# 20. Network Model vs Hierarchical Model

| Feature | Hierarchical Model | Network Model |
|---|---|---|
| Basic Structure | Tree | Graph-like |
| Parent | Generally one | Multiple relationships possible |
| Child | Generally one parent | Can participate in multiple sets |
| Many-to-Many | Difficult | Better supported |
| Paths | More restricted | Multiple paths |
| Flexibility | Lower | Higher |
| Complexity | Lower | Higher |
| Access | Navigational | Navigational |

Memory:

~~~text
Hierarchical
→ TREE

Network
→ GRAPH
~~~

---

# 21. Network Model vs Relational Model

| Feature | Network Model | Relational Model |
|---|---|---|
| Structure | Graph-like records | Tables |
| Relationships | Links / Sets | Foreign Keys |
| Access | Navigational | Declarative |
| Query Style | Navigation through records | SQL |
| Flexibility | Higher than hierarchical | Very high |
| Many-to-Many | Supported through relationships | Supported using relational design |
| Ease of Querying | More complex | Generally easier |

---

# 22. Navigational vs Declarative

This is an important conceptual difference.

### Network Model

The traditional network model is mainly navigational.

The programmer thinks:

~~~text
Start here
    ↓
Follow this relationship
    ↓
Move to another record
    ↓
Follow another relationship
~~~

### Relational Model

The programmer generally specifies:

~~~text
What data is needed
~~~

using SQL.

Example:

~~~sql
SELECT s.name, c.course_name
FROM Student s
JOIN Enrollment e
  ON s.student_id = e.student_id
JOIN Course c
  ON e.course_id = c.course_id;
~~~

The DBMS decides how to execute the query.

Memory:

~~~text
Network
→ Navigate

Relational
→ Ask
~~~

---

# 23. Important Recognition Trick

> [!important]
> If the question says:
>
> "Graph-like database structure"
>
> Think:
>
> **Network Model**

> [!important]
> If the question says:
>
> "Multiple relationships between records"
>
> Think:
>
> **Network Model**

> [!important]
> If the question says:
>
> "A record can participate in multiple sets"
>
> Think:
>
> **Network Model**

> [!important]
> If the question says:
>
> "Many-to-many relationship"
>
> Think:
>
> **Network Model**

---

# 24. Basic Example — Identify the Model

### Question

A database contains:

~~~text
Student
 ↕
Course
~~~

A student can take multiple courses and each course can have multiple students.

Which data model is more suitable than a strict hierarchical model?

### Pattern

~~~text
Many-to-Many
+
Multiple Connections
~~~

### Answer

**Network Model**

---

# 25. Basic Example — Owner and Member

### Question

Consider:

~~~text
Department
   |
   +--- Student 1
   +--- Student 2
~~~

In a set relationship, which is the owner?

### Answer

~~~text
Department
→ Owner
~~~

The students are members.

---

# 26. Basic Example — Record Type

### Question

Consider:

~~~text
STUDENT
----------------
ID
Name
CGPA
~~~

What does this represent?

### Answer

**Record Type**

It defines the structure of student records.

---

# 27. Basic Example — Record

Suppose:

~~~text
101 | Pradeep | 8.5
```

This is an individual:

**Record**

The distinction:

~~~text
Record Type
→ Structure

Record
→ Actual occurrence
~~~

---

# 28. Medium Example — Multiple Relationships

### Question

A student:

- belongs to a department
- enrolls in courses
- stays in a hostel

Can the same student participate in multiple relationships in the network model?

### Answer

Yes.

Conceptually:

~~~text
              Department
                  |
                  ↓
Student ←──── Enrollment ────→ Course
   |
   ↓
Hostel
~~~

The student participates in multiple relationships.

---

# 29. Medium Example — Many-to-Many

### Question

There are:

~~~text
3 Students
5 Courses
```

Each student can take multiple courses and each course can contain multiple students.

Which traditional data model handles this type of relationship more naturally than a strict hierarchical tree?

### Answer

**Network Model**

The key clue is:

~~~text
Many-to-Many
```

---

# 30. Medium Example — Multiple Paths

### Question

Suppose an employee can be reached through:

~~~text
Company
→ Department
→ Employee
```

and also through:

~~~text
Company
→ Project
→ Employee
```

What property is demonstrated?

### Answer

**Multiple Navigational Paths**

This is characteristic of a network-style structure.

---

# 31. Advanced Example — Student Course System

Suppose:

~~~text
Student A
→ Database
→ OS

Student B
→ Database
→ Networks

Student C
→ OS
→ Networks
~~~

Represent conceptually:

~~~text
Student A ───── Database ───── Student B
    |               |
    |               |
   OS ───────────── Student C
    |               |
    +──── Networks ─+
~~~

The same course can connect to multiple students.

This is a graph-like relationship.

---

# 32. Advanced Example — Hospital

Consider:

~~~text
Doctor
   ↕
Patient
```

A doctor can treat many patients.

A patient can be treated by multiple doctors.

This produces:

~~~text
Doctor
   ↕
Patient
~~~

A strict tree is not ideal for this structure.

A network model can represent the interconnected relationships more naturally.

---

# 33. Advanced Example — Company Projects

Consider:

~~~text
Employee
   ↕
Project
~~~

One employee can work on multiple projects.

One project can have multiple employees.

Therefore:

~~~text
Employee
   ↕
Project
~~~

is many-to-many.

The network model can naturally represent multiple connections.

---

# 34. Advanced Example — Supply Chain

Consider:

~~~text
Supplier
   ↕
Product
   ↕
Warehouse
   ↕
Customer
```

A supplier can provide many products.

A product can come from many suppliers.

A product can be stored in multiple warehouses.

A warehouse can contain many products.

This is highly interconnected.

A graph-like model is more natural than a strict tree.

---

# 35. Advantages

> [!success]
> Advantages of Network Model

### 1. Supports Complex Relationships

Multiple relationships can be represented.

### 2. Better Many-to-Many Support

Many-to-many relationships are more natural than in hierarchical databases.

### 3. Multiple Paths

Records can be reached through different paths.

### 4. Less Structural Restriction

A record can participate in multiple relationships.

### 5. Efficient Navigational Access

When access paths are known, navigation can be efficient.

### 6. Suitable for Highly Connected Data

The model can represent complex interconnected structures.

---

# 36. Disadvantages

> [!warning]
> Disadvantages of Network Model

### 1. Complexity

The structure can become difficult to understand.

### 2. Navigational Dependency

Applications may depend heavily on predefined access paths.

### 3. Difficult Maintenance

Changing relationships may require significant changes.

### 4. Less Declarative

Compared with relational databases, the traditional network model requires more explicit navigation.

### 5. More Difficult Query Development

Complex networks can become difficult for developers to navigate.

### 6. Lower General-Purpose Popularity

Relational databases became dominant for many general-purpose applications because of SQL, flexibility, and simpler logical representation.

---

# 37. Advantages vs Disadvantages

| Advantages | Disadvantages |
|---|---|
| Multiple relationships | Complex structure |
| Many-to-many support | Navigational dependency |
| Multiple paths | Maintenance complexity |
| Good for connected data | Less declarative |
| Efficient known-path navigation | More difficult query development |

---

# 38. Real-Time Example — College

A student:

~~~text
Student
   |
   +--- Department
   |
   +--- Courses
   |
   +--- Hostel
   |
   +--- Clubs
~~~

A student may participate in many independent relationships.

This is more graph-like than a strict single-parent hierarchy.

---

# 39. Real-Time Example — Social Network

Consider:

~~~text
Person A
 /     \
B       C
 \     /
   D
~~~

Person D is connected to B and C.

Social relationships are naturally graph-like.

Although a social network is not necessarily implemented using the traditional network database model, it is an excellent intuition for understanding the **network structure**.

---

# 40. Real-Time Example — Transportation

Consider:

~~~text
City A
 /    \
B      C
 \    /
   D
```

There are multiple routes between cities.

Similarly, the network data model can represent multiple paths between records.

Again, this is a conceptual analogy, not a claim that a specific transportation system must use a network DBMS.

---

# 41. Real-Time Example — Organization

A traditional organization might look hierarchical:

~~~text
CEO
 ↓
Manager
 ↓
Employee
~~~

But suppose an employee works with multiple projects:

~~~text
Employee
 ↙     ↘
Project A  Project B
```

Now the data is no longer a simple tree.

The employee participates in multiple relationships.

This is where network-style modeling becomes useful.

---

# 42. Real-Time Example — University

Consider:

~~~text
Student
 ↕
Course
```

and:

~~~text
Professor
 ↕
Course
```

and:

~~~text
Student
 ↕
Department
```

The database contains many interconnected relationships.

This is naturally represented using a graph-like conceptual model.

---

# 43. Important Limitation

Do not confuse:

**Network Model**

with:

**Modern Graph Databases**

They share graph-like ideas, but they are not identical technologies.

The traditional network data model is a classical database model based on records, sets, and navigational relationships.

Modern graph databases use their own models and query languages.

---

# 44. Network Model Recognition — Master Trick

> [!tip]
> Use the **G-M-M-P** shortcut:
>
> **G** = Graph-like
>
> **M** = Multiple relationships
>
> **M** = Many-to-many
>
> **P** = Multiple Paths
>
> If these clues appear together, think:
>
> **Network Model**

---

# 45. Hierarchical vs Network — Fast Recognition

~~~text
TREE
 ↓
Hierarchical

GRAPH
 ↓
Network

TABLE
 ↓
Relational

ENTITY + RELATIONSHIP
 ↓
ER Model
~~~

This four-way distinction is extremely useful in DBMS MCQs.

---

# 46. Common Exam Patterns

> [!important] Must Master

1. Definition of network model
2. Graph-like structure
3. Record
4. Record type
5. Set type
6. Owner
7. Member
8. Multiple relationships
9. Multiple paths
10. Navigational access
11. Many-to-many relationships
12. Advantages
13. Disadvantages
14. Network vs hierarchical
15. Network vs relational
16. Owner-member relationship
17. Record participation in multiple sets
18. Graph-style data representation
19. Navigational dependency
20. Complex relationship representation

---

# 47. Common Mistakes

> [!warning] Avoid These

### Mistake 1 — Network Model Means Computer Network

Wrong.

Here, **network** refers to a network of interconnected data records.

It is a database model.

---

### Mistake 2 — Network Model Means Modern Graph Database

Not exactly.

The traditional network data model is a classical database model.

Modern graph databases are a different category of database systems.

---

### Mistake 3 — Network Model Is Exactly the Same as Hierarchical

Wrong.

~~~text
Hierarchical
→ Tree

Network
→ Graph-like
~~~

---

### Mistake 4 — Every Network Model Relationship Is Many-to-Many

Wrong.

The model can represent various relationships.

Its important advantage is that it can represent complex and multiple relationships more naturally.

---

### Mistake 5 — Network Model Is Declarative Like SQL

Traditional network models are primarily associated with navigational access.

~~~text
Network
→ Navigate

Relational
→ Declare What You Need
~~~

---

### Mistake 6 — Owner Means Database Administrator

Wrong.

In the network model:

~~~text
Owner
→ Record participating as the owner of a set relationship
~~~

It does not mean the human database administrator.

---

# 48. Interview Questions

## Q1. What is the network data model?

### Strong Answer

> The network data model is a graph-like database model that represents records using interconnected relationships. Unlike the classical hierarchical model, a record can participate in multiple relationships, making the network model more suitable for complex and many-to-many relationships.

---

## Q2. What is the main difference between hierarchical and network models?

### Strong Answer

> The hierarchical model organizes data as a tree where a child generally has one parent, whereas the network model uses a graph-like structure where records can participate in multiple relationships and multiple paths can exist.

---

## Q3. What is a record type?

### Answer

> A record type defines the structure of a group of similar records.

Example:

~~~text
STUDENT
-----------
ID
Name
CGPA
~~~

---

## Q4. What is a record?

### Answer

> A record is an individual stored occurrence of a record type.

Example:

~~~text
101 | Pradeep | 8.5
~~~

---

# 49. Interview Questions — Sets

## Q5. What is a set type?

### Answer

> A set type defines a relationship between record types using an owner-member structure.

Example:

~~~text
Department
    ↓
Student
~~~

Department can act as owner and Student as member.

---

## Q6. What is an owner in the network model?

### Answer

> The owner is the record type or record that participates as the owner in a set relationship.

---

## Q7. What is a member?

### Answer

> A member is the record type or record that participates as the member of a set relationship.

---

# 50. Interview Questions — Relationships

## Q8. Does the network model support many-to-many relationships?

### Answer

Yes.

It can represent interconnected relationships where:

~~~text
A → Many B
B → Many A
~~~

This is one of its important advantages over a strict hierarchical model.

---

## Q9. What is navigational access?

### Answer

> Navigational access means reaching records by following predefined links or relationships from one record to another.

---

## Q10. Why is the network model more flexible than the hierarchical model?

### Answer

Because a record can participate in multiple relationships and multiple paths can exist between records.

---

# 51. Advanced Interview Question

## Question

Why can a network model represent relationships that are difficult in a hierarchical model?

### Answer

A hierarchical model imposes a tree structure.

A strict tree expects:

~~~text
One Child
    ↓
One Parent
~~~

A network model allows:

~~~text
One Record
   ↓
Multiple Relationships
```

Therefore, structures such as:

~~~text
Student ↔ Course
Employee ↔ Project
Doctor ↔ Patient
```

can be represented more naturally.

---

# 52. Advanced Interview Question

## Question

What is the biggest conceptual difference between hierarchical and network models?

### Answer

The difference is structural flexibility.

~~~text
Hierarchical
→ Tree
→ Single-parent orientation

Network
→ Graph-like
→ Multiple connections
```

---

# 53. Advanced Interview Question

## Question

Why did relational databases become more popular?

### Answer

Important reasons include:

- Simpler table-based logical representation
- Declarative SQL
- Flexible querying
- Easier schema manipulation
- Strong mathematical foundation
- Normalization
- Better separation between logical and physical access

The relational model became highly popular for general-purpose database systems.

---

# 54. IIT-Level Thinking Pattern

When you see a database-model question, ask:

~~~text
Step 1
Is it a tree?
    ↓
Hierarchical

Step 2
Is it graph-like with multiple relationships?
    ↓
Network

Step 3
Is it tables + rows + columns?
    ↓
Relational

Step 4
Is it entities + attributes + relationships?
    ↓
ER Model
~~~

This decision tree can solve many conceptual MCQs quickly.

---

# 55. Pattern Recognition Table

| Question Clue | Immediate Thought |
|---|---|
| Tree | Hierarchical |
| Root | Hierarchical |
| Parent-child | Hierarchical |
| One parent | Hierarchical |
| Graph-like | Network |
| Multiple relationships | Network |
| Multiple paths | Network |
| Many-to-many | Network |
| Owner-member | Network |
| Record sets | Network |
| Tables | Relational |
| Rows + columns | Relational |
| SQL | Relational |
| Entity + Attribute | ER |
| Entity + Relationship | ER |

---

# 56. Quick MCQ Shortcuts

> [!tip]
> **Shortcut 1**
>
> Tree = Hierarchical.

> [!tip]
> **Shortcut 2**
>
> Graph-like = Network.

> [!tip]
> **Shortcut 3**
>
> Multiple relationships = Network.

> [!tip]
> **Shortcut 4**
>
> Many-to-many = Network is a strong classical-model clue.

> [!tip]
> **Shortcut 5**
>
> Owner + Member = Network.

> [!tip]
> **Shortcut 6**
>
> Tables + SQL = Relational.

> [!tip]
> **Shortcut 7**
>
> Entities + Attributes + Relationships = ER Model.

---

# 57. Comparison Memory Map

~~~text
                    DATA MODELS

                         |
        +----------------+----------------+
        |                |                |
        ↓                ↓                ↓
   Hierarchical      Network         Relational
        |                |                |
        ↓                ↓                ↓
      TREE            GRAPH            TABLE
        |                |                |
   Parent-Child    Multiple Links    Rows/Columns
        |                |                |
   One-to-Many      Complex Links       SQL
~~~

---

# 58. Placement Exam Focus

### Very High Priority

- Network model definition
- Graph-like structure
- Record
- Record type
- Set type
- Owner
- Member
- Multiple relationships
- Many-to-many support
- Network vs hierarchical

### High Priority

- Navigational access
- Multiple paths
- Advantages
- Disadvantages
- Network vs relational

### Interview Priority

- Why network model?
- Why is it more flexible than hierarchical?
- What is owner-member relationship?
- What is navigational access?
- Why did relational databases become more popular?

---

# 59. Formula Sheet

~~~text
NETWORK MODEL

Basic Structure:
Graph-like


Main Components:
Record
Record Type
Set Type
Owner
Member


Core Relationship:
Owner
   ↓
Member


Major Property:
Multiple Relationships


Major Strength:
Complex Relationship Representation


Many-to-Many:
Supported more naturally than in a strict hierarchy.


Access:
Navigational / Path-Based


Memory:
Hierarchical
→ Tree

Network
→ Graph

Relational
→ Table
~~~

---

# 60. Quick Revision

> [!summary] One-Minute Revision

~~~text
NETWORK MODEL
→ Classical graph-like database model.

MAIN IDEA
→ Records can participate in multiple relationships.

STRUCTURE
→ Graph-like rather than strict tree.

RECORD
→ Individual stored data occurrence.

RECORD TYPE
→ Structure/definition of similar records.

SET TYPE
→ Defines owner-member relationship.

OWNER
→ Record participating as owner of a set.

MEMBER
→ Record participating as member of a set.

MAIN STRENGTH
→ Complex interconnected relationships.

MANY-TO-MANY
→ Better supported than in classical hierarchical model.

ACCESS
→ Navigational / path-based.

MULTIPLE PATHS
→ A record may be reachable through different relationships.

ADVANTAGES
→ Flexible relationships
→ Multiple paths
→ Many-to-many support
→ Good for connected data
→ Efficient known-path navigation

DISADVANTAGES
→ Complex structure
→ Navigational dependency
→ Maintenance difficulty
→ Less declarative than relational model

COMPARISON

Hierarchical
→ Tree

Network
→ Graph

Relational
→ Table

ER
→ Entity + Attribute + Relationship

FAST RECOGNITION

Tree
→ Hierarchical

Graph-like
→ Network

Multiple Relationships
→ Network

Many-to-Many
→ Network

Tables + SQL
→ Relational

Entities + Relationships
→ ER
~~~

---

# 61. Golden Memory Trick

**Network Model = Graph + Multiple Relationships + Multiple Paths + Many-to-Many.**

# 62. One-Line Recognition

**Whenever a DBMS question describes graph-like records, owner-member sets, multiple relationships, or many-to-many navigation, think Network Data Model.**