---
type: concept
subject: aptitude
topic: "HCF and LCM of Fractions"
parent: "01. Number System/HCF and LCM"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - hcf
  - lcm
  - fractions
  - factorization
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[HCF and LCM]]"
  - "[[HCF]]"
  - "[[LCM]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Factorization]]"
  - "[[Application Problems]]"
---

# HCF and LCM of Fractions

## 1. Core Concept

> [!summary] Main Idea
> For fractions, the HCF and LCM are found by treating the **numerators** and **denominators** separately.

For positive fractions:

$$
\frac{a}{b},\frac{c}{d}
$$

the standard formulas are:

### HCF

$$
\boxed{
HCF=
\frac{HCF(a,c)}
{LCM(b,d)}
}
$$

### LCM

$$
\boxed{
LCM=
\frac{LCM(a,c)}
{HCF(b,d)}
}
$$

---

# 2. Golden Memory Rule

> [!important] Memorize This

### HCF of Fractions

$$
\boxed{
\frac{HCF(\text{numerators})}
{LCM(\text{denominators})}
}
$$

### LCM of Fractions

$$
\boxed{
\frac{LCM(\text{numerators})}
{HCF(\text{denominators})}
}
$$

### Memory Trick

> **HCF → HCF on top, LCM on bottom**
>
> **LCM → LCM on top, HCF on bottom**

---

# 3. HCF of Two Fractions

Find:

$$
HCF\left(\frac{6}{5},\frac{9}{10}\right)
$$

### Step 1 — HCF of numerators

$$
HCF(6,9)=3
$$

### Step 2 — LCM of denominators

$$
LCM(5,10)=10
$$

### Step 3 — Apply formula

$$
HCF=
\frac{3}{10}
$$

Therefore:

$$
\boxed{\frac{3}{10}}
$$

---

# 4. LCM of Two Fractions

Find:

$$
LCM\left(\frac{6}{5},\frac{9}{10}\right)
$$

### Step 1 — LCM of numerators

$$
LCM(6,9)=18
$$

### Step 2 — HCF of denominators

$$
HCF(5,10)=5
$$

### Step 3 — Apply formula

$$
LCM=
\frac{18}{5}
$$

Therefore:

$$
\boxed{\frac{18}{5}}
$$

---

# 5. Example — HCF

Find:

$$
HCF\left(\frac{8}{15},\frac{12}{25}\right)
$$

Numerator HCF:

$$
HCF(8,12)=4
$$

Denominator LCM:

$$
LCM(15,25)=75
$$

Therefore:

$$
\boxed{
HCF=\frac4{75}
}
$$

---

# 6. Example — LCM

Find:

$$
LCM\left(\frac{8}{15},\frac{12}{25}\right)
$$

Numerator LCM:

$$
LCM(8,12)=24
$$

Denominator HCF:

$$
HCF(15,25)=5
$$

Therefore:

$$
\boxed{
LCM=\frac{24}{5}
}
$$

---

# 7. Why Are HCF and LCM Reversed?

For integers:

$$
HCF\rightarrow\text{minimum powers}
$$

and:

$$
LCM\rightarrow\text{maximum powers}
$$

For a fraction:

$$
\frac{a}{b}
$$

the denominator behaves oppositely because:

$$
\frac{1}{b}
$$

contains negative prime exponents.

Therefore:

- HCF → minimum numerator powers + **maximum denominator powers**
- LCM → maximum numerator powers + **minimum denominator powers**

That gives:

$$
\boxed{
HCF=
\frac{HCF(\text{numerators})}
{LCM(\text{denominators})}
}
$$

and:

$$
\boxed{
LCM=
\frac{LCM(\text{numerators})}
{HCF(\text{denominators})}
}
$$

---

# 8. Prime Factorization Explanation

Consider:

$$
\frac{12}{25}
$$

and:

$$
\frac{18}{35}
$$

Prime factorization:

$$
12=2^2\times3
$$

$$
18=2\times3^2
$$

For numerators:

### HCF

$$
2^1\times3^1=6
$$

### LCM

$$
2^2\times3^2=36
$$

Denominators:

$$
25=5^2
$$

$$
35=5\times7
$$

### Denominator HCF

$$
5
$$

### Denominator LCM

$$
5^2\times7=175
$$

Therefore:

### HCF

$$
\boxed{\frac6{175}}
$$

### LCM

$$
\boxed{\frac{36}{5}}
$$

---

# 9. Fractions Should Be in Standard Form

Before applying formulas, it is safest to reduce fractions to their lowest terms.

Example:

$$
\frac{6}{8}=\frac34
$$

So instead of using:

$$
\frac68
$$

use:

$$
\frac34
$$

> [!tip] Exam Tip
> **Simplify fractions first**, especially when the question gives fractions that are not already in lowest terms.

---

# 10. Example — Reduce First

Find the HCF of:

$$
\frac{6}{8},\frac{9}{12}
$$

Reduce:

$$
\frac68=\frac34
$$

and:

$$
\frac9{12}=\frac34
$$

Both fractions are equal.

Therefore:

$$
\boxed{HCF=\frac34}
$$

and:

$$
\boxed{LCM=\frac34}
$$

---

# 11. HCF of Three Fractions

For:

$$
\frac{a}{p},
\frac{b}{q},
\frac{c}{r}
$$

the formula is:

$$
\boxed{
HCF=
\frac{
HCF(a,b,c)
}{
LCM(p,q,r)
}
}
$$

### Example

Find:

$$
HCF\left(
\frac{6}{5},
\frac{9}{10},
\frac{12}{15}
\right)
$$

Numerator HCF:

$$
HCF(6,9,12)=3
$$

Denominator LCM:

$$
LCM(5,10,15)=30
$$

Therefore:

$$
\boxed{\frac3{30}}
$$

Simplify:

$$
\boxed{\frac1{10}}
$$

---

# 12. LCM of Three Fractions

For:

$$
\frac{a}{p},
\frac{b}{q},
\frac{c}{r}
$$

we use:

$$
\boxed{
LCM=
\frac{
LCM(a,b,c)
}{
HCF(p,q,r)
}
}
$$

---

# 13. Example — LCM of Three Fractions

Find:

$$
LCM\left(
\frac{4}{6},
\frac{6}{9},
\frac{10}{15}
\right)
$$

First reduce:

$$
\frac46=\frac23
$$

$$
\frac69=\frac23
$$

$$
\frac{10}{15}=\frac23
$$

All three fractions are equal.

Therefore:

$$
\boxed{LCM=\frac23}
$$

---

# 14. HCF of Fractions With Same Denominator

Suppose:

$$
\frac a d,\frac b d
$$

Then:

$$
HCF=
\frac{HCF(a,b)}
{LCM(d,d)}
$$

Since:

$$
LCM(d,d)=d
$$

we get:

$$
\boxed{
HCF\left(\frac ad,\frac bd\right)
=
\frac{HCF(a,b)}d
}
$$

### Example

$$
HCF\left(\frac6{10},\frac8{10}\right)
$$

Numerator HCF:

$$
HCF(6,8)=2
$$

Therefore:

$$
\boxed{\frac2{10}=\frac15}
$$

---

# 15. LCM of Fractions With Same Denominator

For:

$$
\frac ad,\frac bd
$$

we have:

$$
LCM=
\frac{LCM(a,b)}
{HCF(d,d)}
$$

Since:

$$
HCF(d,d)=d
$$

therefore:

$$
\boxed{
LCM\left(\frac ad,\frac bd\right)
=
\frac{LCM(a,b)}d
}
$$

---

# 16. Example — Same Denominator

Find:

$$
LCM\left(\frac6{10},\frac8{10}\right)
$$

Numerator LCM:

$$
LCM(6,8)=24
$$

Therefore:

$$
LCM=
\frac{24}{10}
$$

Simplify:

$$
\boxed{\frac{12}{5}}
$$

---

# 17. HCF of Fractions With Same Numerator

Suppose:

$$
\frac a b,\frac a d
$$

Then:

$$
HCF=
\frac{HCF(a,a)}
{LCM(b,d)}
$$

Since:

$$
HCF(a,a)=a
$$

we get:

$$
\boxed{
HCF=
\frac{a}{LCM(b,d)}
}
$$

---

# 18. LCM of Fractions With Same Numerator

Similarly:

$$
LCM=
\frac{LCM(a,a)}
{HCF(b,d)}
$$

Since:

$$
LCM(a,a)=a
$$

we get:

$$
\boxed{
LCM=
\frac{a}{HCF(b,d)}
}
$$

---

# 19. Example — Same Numerator

Find the HCF and LCM of:

$$
\frac5{6},\frac5{8}
$$

### HCF

$$
HCF=
\frac5{LCM(6,8)}
$$

$$
=\frac5{24}
$$

Therefore:

$$
\boxed{HCF=\frac5{24}}
$$

### LCM

$$
LCM=
\frac5{HCF(6,8)}
$$

$$
=\frac5{2}
$$

Therefore:

$$
\boxed{LCM=\frac52}
$$

---

# 20. Important Relationship for Fractions

For two positive fractions:

$$
x=\frac ab
$$

and:

$$
y=\frac cd
$$

their HCF and LCM satisfy:

$$
\boxed{
HCF(x,y)\times LCM(x,y)=x\times y
}
$$

This mirrors the integer relationship.

---

# 21. Verify With an Example

Take:

$$
x=\frac65
$$

and:

$$
y=\frac9{10}
$$

We found:

$$
HCF=\frac3{10}
$$

and:

$$
LCM=\frac{18}{5}
$$

Multiply:

$$
\frac3{10}\times\frac{18}{5}
$$

$$
=\frac{54}{50}
$$

$$
=\frac{27}{25}
$$

Now:

$$
x\times y
=
\frac65\times\frac9{10}
$$

$$
=\frac{54}{50}
$$

$$
=\frac{27}{25}
$$

Therefore:

$$
\boxed{HCF\times LCM=x\times y}
$$

---

# 22. Important Caveat

> [!warning] Important
> The HCF × LCM product relationship is safest to apply after the fractions are represented in standard reduced form and the HCF/LCM definitions are being used consistently.

For aptitude questions, the standard formulas are:

$$
\boxed{
HCF=
\frac{HCF(\text{numerators})}
{LCM(\text{denominators})}
}
$$

$$
\boxed{
LCM=
\frac{LCM(\text{numerators})}
{HCF(\text{denominators})}
}
$$

---

# 23. Fraction HCF Using Prime Powers

Suppose:

$$
x=\frac{2^3\times3}{5^2\times7}
$$

and:

$$
y=\frac{2^2\times3^2}{5\times7^2}
$$

### HCF

Numerator → minimum powers:

$$
2^2\times3
$$

Denominator → maximum powers:

$$
5^2\times7^2
$$

Therefore:

$$
\boxed{
HCF=
\frac{2^2\times3}{5^2\times7^2}
}
$$

---

# 24. Fraction LCM Using Prime Powers

Using the same fractions:

$$
x=\frac{2^3\times3}{5^2\times7}
$$

and:

$$
y=\frac{2^2\times3^2}{5\times7^2}
$$

### LCM

Numerator → maximum powers:

$$
2^3\times3^2
$$

Denominator → minimum powers:

$$
5\times7
$$

Therefore:

$$
\boxed{
LCM=
\frac{2^3\times3^2}{5\times7}
}
$$

---

# 25. HCF and LCM of Mixed Fractions

If the fractions contain mixed numbers, first convert them to improper fractions.

### Example

$$
2\frac12=\frac52
$$

and:

$$
1\frac34=\frac74
$$

Then apply the fraction formulas.

> [!tip] Pattern
>
> **Mixed fraction → Improper fraction → Simplify → HCF/LCM**

---

# 26. HCF of Fractions — Word Problem

Suppose three lengths are:

$$
\frac34\text{ m},
\frac58\text{ m}
$$

and the question asks for the greatest standard fractional length that measures both exactly.

Think:

$$
\boxed{HCF}
$$

Use:

$$
HCF=
\frac{HCF(3,5)}
{LCM(4,8)}
$$

Numerator HCF:

$$
1
$$

Denominator LCM:

$$
8
$$

Therefore:

$$
\boxed{\frac18\text{ m}}
$$

---

# 27. LCM of Fractions — Word Problem

Suppose two repeating fractional intervals are:

$$
\frac23
$$

and:

$$
\frac56
$$

The first common interval is found using LCM.

Numerator LCM:

$$
LCM(2,5)=10
$$

Denominator HCF:

$$
HCF(3,6)=3
$$

Therefore:

$$
\boxed{\frac{10}{3}}
$$

---

# 28. Important Pattern — Same Denominator

For:

$$
\frac a d,\frac b d
$$

### HCF

$$
\boxed{
\frac{HCF(a,b)}d
}
$$

### LCM

$$
\boxed{
\frac{LCM(a,b)}d
}
$$

This is a very useful shortcut.

---

# 29. Important Pattern — Same Numerator

For:

$$
\frac a b,\frac a d
$$

### HCF

$$
\boxed{
\frac a{LCM(b,d)}
}
$$

### LCM

$$
\boxed{
\frac a{HCF(b,d)}
}
$$

---

# 30. Important Pattern — Unit Fractions

For:

$$
\frac1a,\frac1b
$$

### HCF

Numerator HCF:

$$
HCF(1,1)=1
$$

Denominator LCM:

$$
LCM(a,b)
$$

Therefore:

$$
\boxed{
HCF\left(\frac1a,\frac1b\right)
=
\frac1{LCM(a,b)}
}
$$

### LCM

$$
\boxed{
LCM\left(\frac1a,\frac1b\right)
=
\frac1{HCF(a,b)}
}
$$

---

# 31. Example — Unit Fractions

Find HCF and LCM of:

$$
\frac14,\frac16
$$

### HCF

$$
LCM(4,6)=12
$$

Therefore:

$$
\boxed{\frac1{12}}
$$

### LCM

$$
HCF(4,6)=2
$$

Therefore:

$$
\boxed{\frac12}
$$

---

# 32. Fraction Factorization Pattern

When the numbers are large fractions, factorize the numerator and denominator separately.

For example:

$$
\frac{12}{35}
$$

factorize:

$$
12=2^2\times3
$$

$$
35=5\times7
$$

This makes HCF and LCM calculations much faster.

---

# 33. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Using HCF for both numerator and denominator in the HCF formula.
- ❌ Using LCM for both numerator and denominator in the LCM formula.
- ❌ Forgetting the reversal in the denominator.
- ❌ Applying the formula before simplifying awkward fractions.
- ❌ Confusing HCF of fractions with HCF of numerators only.
- ❌ Forgetting to reduce the final fraction.
- ❌ Treating mixed fractions as ordinary integers.
- ❌ Forgetting to convert mixed numbers into improper fractions.
- ❌ Confusing HCF and LCM of unit fractions.

---

# 34. Exam Strategy

> [!tip] Fast Decision Tree

### Asked: HCF of fractions

Immediately write:

$$
\boxed{
\frac{HCF(Numerators)}
{LCM(Denominators)}
}
$$

### Asked: LCM of fractions

Immediately write:

$$
\boxed{
\frac{LCM(Numerators)}
{HCF(Denominators)}
}
$$

### Same denominator

Use:

$$
\boxed{
HCF=\frac{HCF(N)}d
}
$$

and:

$$
\boxed{
LCM=\frac{LCM(N)}d
}
$$

### Same numerator

Use:

$$
\boxed{
HCF=\frac a{LCM(D)}
}
$$

and:

$$
\boxed{
LCM=\frac a{HCF(D)}
}
$$

### Unit fractions

Remember:

$$
\boxed{
HCF\left(\frac1a,\frac1b\right)=\frac1{LCM(a,b)}
}
$$

$$
\boxed{
LCM\left(\frac1a,\frac1b\right)=\frac1{HCF(a,b)}
}
$$

---

# 35. Important Formula Sheet

> [!important] Must Remember

### HCF of Two Fractions

$$
\boxed{
HCF\left(\frac ab,\frac cd\right)
=
\frac{HCF(a,c)}
{LCM(b,d)}
}
$$

### LCM of Two Fractions

$$
\boxed{
LCM\left(\frac ab,\frac cd\right)
=
\frac{LCM(a,c)}
{HCF(b,d)}
}
$$

### HCF of Three Fractions

$$
\boxed{
HCF=
\frac{HCF(a,b,c)}
{LCM(p,q,r)}
}
$$

### LCM of Three Fractions

$$
\boxed{
LCM=
\frac{LCM(a,b,c)}
{HCF(p,q,r)}
}
$$

---

# 36. High-Yield Patterns

> [!important] Must Master

### Pattern 1

**HCF of fractions**

$$
\boxed{
HCF/HCF
\rightarrow
HCF\text{ numerator, LCM denominator}
}
$$

### Pattern 2

**LCM of fractions**

$$
\boxed{
LCM/LCM
\rightarrow
LCM\text{ numerator, HCF denominator}
}
$$

### Pattern 3

**Same denominator**

$$
\boxed{
HCF=\frac{HCF(N)}d
}
$$

$$
\boxed{
LCM=\frac{LCM(N)}d
}
$$

### Pattern 4

**Same numerator**

$$
\boxed{
HCF=\frac a{LCM(D)}
}
$$

$$
\boxed{
LCM=\frac a{HCF(D)}
}
$$

### Pattern 5

**Unit fractions**

$$
\boxed{
HCF\left(\frac1a,\frac1b\right)
=
\frac1{LCM(a,b)}
}
$$

$$
\boxed{
LCM\left(\frac1a,\frac1b\right)
=
\frac1{HCF(a,b)}
}
$$

---

# 37. HCL Preparation Priority

**Priority:** 🔥 High

Master this topic because it connects:

- HCF
- LCM
- Fractions
- Factorization
- Prime powers
- Application problems

### Master These First

1. HCF fraction formula
2. LCM fraction formula
3. Numerator/denominator reversal
4. Simplifying fractions
5. Same denominator shortcut
6. Same numerator shortcut
7. Unit-fraction shortcut
8. Three-fraction problems
9. Prime-factorization approach
10. Fraction word problems

---

# 38. Practice Checklist

- [ ] Find HCF of two fractions
- [ ] Find LCM of two fractions
- [ ] Find HCF of three fractions
- [ ] Find LCM of three fractions
- [ ] Practice same-denominator fractions
- [ ] Practice same-numerator fractions
- [ ] Practice unit fractions
- [ ] Practice mixed fractions
- [ ] Practice prime-factorized fractions
- [ ] Simplify final answers
- [ ] Solve fraction application problems
- [ ] Memorize numerator/denominator reversal

---

# 39. Related Topics

- [[HCF and LCM]]
- [[HCF]]
- [[LCM]]
- [[Factors]]
- [[Multiples]]
- [[Factorization]]
- [[Rational Numbers]]
- [[Application Problems]]

---

# 40. Quick Revision

> [!summary] One-Minute Revision

### HCF of Fractions

$$
\boxed{
HCF=
\frac{HCF(\text{numerators})}
{LCM(\text{denominators})}
}
$$

### LCM of Fractions

$$
\boxed{
LCM=
\frac{LCM(\text{numerators})}
{HCF(\text{denominators})}
}
$$

### Same Denominator

$$
\boxed{
HCF=\frac{HCF(N)}d
}
$$

$$
\boxed{
LCM=\frac{LCM(N)}d
}
$$

### Same Numerator

$$
\boxed{
HCF=\frac a{LCM(D)}
}
$$

$$
\boxed{
LCM=\frac a{HCF(D)}
}
$$

### Unit Fractions

$$
\boxed{
HCF\left(\frac1a,\frac1b\right)=\frac1{LCM(a,b)}
}
$$

$$
\boxed{
LCM\left(\frac1a,\frac1b\right)=\frac1{HCF(a,b)}
}
$$

### Golden Memory Trick

> **Fraction HCF: HCF goes on top, LCM goes below.**
>
> **Fraction LCM: LCM goes on top, HCF goes below.**

### One-Line Recognition

> **Whenever HCF/LCM of fractions appears, separate numerator and denominator first.**