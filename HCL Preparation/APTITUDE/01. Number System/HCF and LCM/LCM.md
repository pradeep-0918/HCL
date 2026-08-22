---
type: concept
subject: aptitude
topic: "LCM"
parent: "01. Number System/HCF and LCM"
company: HCL
difficulty: medium
priority: very-high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - lcm
  - hcf
  - factors
  - multiples
  - factorization
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[HCF and LCM]]"
  - "[[HCF]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Factorization]]"
  - "[[HCF-LCM Relationship]]"
  - "[[HCF and LCM of Fractions]]"
  - "[[Application Problems]]"
---

# LCM

## 1. Core Concept

> [!summary] Definition
> **LCM** stands for **Least Common Multiple**.
>
> It is the **smallest positive number that is a multiple of two or more given numbers**.

LCM is also called:

- Least Common Multiple
- Lowest Common Multiple

Therefore:

$$
\boxed{\text{LCM}=\text{smallest positive common multiple}}
$$

---

# 2. Basic Example

Find the LCM of:

$$
4,\ 6
$$

Multiples of `4`:

$$
4,8,12,16,20,24,\ldots
$$

Multiples of `6`:

$$
6,12,18,24,\ldots
$$

First common positive multiple:

$$
\boxed{12}
$$

Therefore:

$$
\boxed{\operatorname{LCM}(4,6)=12}
$$

---

# 3. What Does LCM Actually Mean?

If:

$$
L=\operatorname{LCM}(a,b)
$$

then:

$$
a\mid L
$$

and:

$$
b\mid L
$$

and no smaller positive number is divisible by both.

Therefore:

$$
\boxed{
L=\text{smallest positive common multiple}
}
$$

---

# 4. LCM Using Prime Factorization

This is one of the most important methods.

Suppose:

$$
A=p_1^{a_1}p_2^{a_2}\cdots
$$

and:

$$
B=p_1^{b_1}p_2^{b_2}\cdots
$$

Then:

$$
\boxed{
\operatorname{LCM}(A,B)
=
\prod p_i^{\max(a_i,b_i)}
}
$$

> [!important] Golden Rule
>
> **LCM → Take every prime factor with the largest power appearing in any number.**

---

# 5. Example — Prime Factorization

Find the LCM of:

$$
60,\ 84
$$

Prime factorize:

$$
60=2^2\times3\times5
$$

$$
84=2^2\times3\times7
$$

Take maximum powers:

$$
2^2,\ 3,\ 5,\ 7
$$

Therefore:

$$
\operatorname{LCM}(60,84)
=
2^2\times3\times5\times7
$$

$$
\boxed{420}
$$

---

# 6. Example — Different Powers

Find:

$$
\operatorname{LCM}(72,120)
$$

Prime factorization:

$$
72=2^3\times3^2
$$

$$
120=2^3\times3\times5
$$

Take maximum powers:

$$
2^3\times3^2\times5
$$

Therefore:

$$
\boxed{360}
$$

---

# 7. LCM When Numbers Are Coprime

If:

$$
\operatorname{HCF}(a,b)=1
$$

then:

$$
\boxed{
\operatorname{LCM}(a,b)=a\times b
}
$$

### Example

For:

$$
8,\ 15
$$

we have:

$$
\operatorname{HCF}(8,15)=1
$$

Therefore:

$$
\operatorname{LCM}(8,15)
=
8\times15
$$

$$
\boxed{120}
$$

---

# 8. HCF-LCM Relationship

For two positive integers:

$$
a,b
$$

the most important relationship is:

$$
\boxed{
\operatorname{HCF}(a,b)
\times
\operatorname{LCM}(a,b)
=
a\times b
}
$$

Therefore:

$$
\boxed{
\operatorname{LCM}(a,b)
=
\frac{a\times b}{\operatorname{HCF}(a,b)}
}
$$

---

# 9. Example — LCM Using HCF

Given:

$$
a=24,\quad b=36
$$

and:

$$
\operatorname{HCF}(24,36)=12
$$

Then:

$$
\operatorname{LCM}
=
\frac{24\times36}{12}
$$

$$
=2\times36
$$

$$
\boxed{72}
$$

---

# 10. LCM of More Than Two Numbers

For three numbers:

$$
a,b,c
$$

we can calculate:

$$
\boxed{
\operatorname{LCM}(a,b,c)
=
\operatorname{LCM}(\operatorname{LCM}(a,b),c)
}
$$

### Example

Find:

$$
\operatorname{LCM}(6,8,12)
$$

First:

$$
\operatorname{LCM}(6,8)=24
$$

Then:

$$
\operatorname{LCM}(24,12)=24
$$

Therefore:

$$
\boxed{24}
$$

---

# 11. LCM by Prime Factorization — Three Numbers

Find:

$$
\operatorname{LCM}(12,18,30)
$$

Prime factorization:

$$
12=2^2\times3
$$

$$
18=2\times3^2
$$

$$
30=2\times3\times5
$$

Take maximum powers:

$$
2^2,\ 3^2,\ 5
$$

Therefore:

$$
\operatorname{LCM}
=
2^2\times3^2\times5
$$

$$
\boxed{180}
$$

---

# 12. LCM of Fractions

For positive fractions:

$$
\frac ab,\frac cd
$$

the LCM is:

$$
\boxed{
\frac{\operatorname{LCM}(a,c)}
{\operatorname{HCF}(b,d)}
}
$$

### Example

Find the LCM of:

$$
\frac65,\frac9{10}
$$

Numerator LCM:

$$
\operatorname{LCM}(6,9)=18
$$

Denominator HCF:

$$
\operatorname{HCF}(5,10)=5
$$

Therefore:

$$
\boxed{\frac{18}{5}}
$$

---

# 13. HCF and LCM of Fractions — Memory Rule

> [!important] Memorize

### HCF of fractions

$$
\boxed{
\frac{\operatorname{HCF}(\text{numerators})}
{\operatorname{LCM}(\text{denominators})}
}
$$

### LCM of fractions

$$
\boxed{
\frac{\operatorname{LCM}(\text{numerators})}
{\operatorname{HCF}(\text{denominators})}
}
$$

### Memory Trick

> **HCF ↔ HCF on top, LCM on bottom**
>
> **LCM ↔ LCM on top, HCF on bottom**

---

# 14. LCM of Decimals

For decimal numbers, first convert them into integers by multiplying by the same power of `10`.

### Example

Find LCM of:

$$
1.2,\ 1.8
$$

Multiply both by `10`:

$$
12,\ 18
$$

Find LCM:

$$
\operatorname{LCM}(12,18)=36
$$

Now divide by `10`:

$$
\boxed{3.6}
$$

---

# 15. LCM of Multiples

If:

$$
a\mid b
$$

then:

$$
\boxed{\operatorname{LCM}(a,b)=b}
$$

### Example

Since:

$$
6\mid24
$$

we have:

$$
\boxed{\operatorname{LCM}(6,24)=24}
$$

---

# 16. LCM of Consecutive Numbers

For two consecutive positive integers:

$$
n,\ n+1
$$

their HCF is:

$$
1
$$

Therefore:

$$
\boxed{
\operatorname{LCM}(n,n+1)=n(n+1)
}
$$

### Example

$$
\operatorname{LCM}(9,10)
=
9\times10
$$

$$
\boxed{90}
$$

---

# 17. LCM of Two Coprime Numbers

If:

$$
\gcd(a,b)=1
$$

then:

$$
\boxed{\operatorname{LCM}(a,b)=ab}
$$

Examples:

$$
\operatorname{LCM}(7,11)=77
$$

$$
\operatorname{LCM}(8,15)=120
$$

$$
\operatorname{LCM}(9,20)=180
$$

---

# 18. Common Multiples

If:

$$
L=\operatorname{LCM}(a,b)
$$

then all positive common multiples are:

$$
\boxed{
L,2L,3L,4L,\ldots
}
$$

### Example

For:

$$
a=6,\quad b=8
$$

LCM:

$$
L=24
$$

Common multiples:

$$
24,48,72,96,\ldots
$$

---

# 19. Every Common Multiple Is a Multiple of LCM

This is an important property.

If `L` is the LCM of `a` and `b`, then:

$$
\boxed{
\text{Every common multiple of }a,b\text{ is a multiple of }L
}
$$

### Example

For `4` and `6`:

$$
L=12
$$

Common multiples:

$$
12,24,36,48,\ldots
$$

Every one is divisible by `12`.

---

# 20. LCM and Repeating Events

This is one of the most important aptitude applications.

If two events repeat every:

$$
a
$$

and:

$$
b
$$

units of time, they occur together again after:

$$
\boxed{\operatorname{LCM}(a,b)}
$$

### Example

A bell rings every `6` minutes and another every `8` minutes.

They ring together every:

$$
\operatorname{LCM}(6,8)
$$

$$
=24
$$

Therefore:

$$
\boxed{24\text{ minutes}}
$$

---

# 21. LCM Application — Bells

Three bells ring every:

- `6` minutes
- `8` minutes
- `12` minutes

They ring together again after:

$$
\operatorname{LCM}(6,8,12)
$$

$$
=24
$$

Therefore:

$$
\boxed{24\text{ minutes}}
$$

---

# 22. LCM Application — Traffic Lights

Three traffic lights change every:

- `20` seconds
- `30` seconds
- `45` seconds

They synchronize after:

$$
\operatorname{LCM}(20,30,45)
$$

Prime factorization:

$$
20=2^2\times5
$$

$$
30=2\times3\times5
$$

$$
45=3^2\times5
$$

Take maximum powers:

$$
2^2\times3^2\times5
$$

$$
\boxed{180\text{ seconds}}
$$

---

# 23. LCM Application — Least Number Divisible by Several Numbers

If a question asks:

> Find the smallest number divisible by `a`, `b`, and `c`.

Immediately think:

$$
\boxed{\operatorname{LCM}(a,b,c)}
$$

### Example

Find the smallest number divisible by:

$$
8,\ 12,\ 18
$$

Prime factorization:

$$
8=2^3
$$

$$
12=2^2\times3
$$

$$
18=2\times3^2
$$

Therefore:

$$
\operatorname{LCM}
=
2^3\times3^2
$$

$$
\boxed{72}
$$

---

# 24. LCM Application — Smallest Number Leaving a Remainder

A common pattern:

> Find the smallest number which leaves remainder `r` when divided by several numbers.

If the same remainder `r` is required, then:

$$
N-r
$$

must be divisible by all the given divisors.

Therefore:

$$
\boxed{
N=\operatorname{LCM}(a,b,c)+r
}
$$

### Example

Find the smallest number that leaves remainder `2` when divided by `6`, `8`, and `12`.

First:

$$
\operatorname{LCM}(6,8,12)=24
$$

Therefore:

$$
N=24+2
$$

$$
\boxed{26}
$$

Check:

$$
26\bmod6=2
$$

$$
26\bmod8=2
$$

$$
26\bmod12=2
$$

---

# 25. Important Exception — Remainder Must Be Smaller

For:

$$
N-r
$$

to produce remainder `r` when divided by every divisor, we need:

$$
\boxed{r<\text{each divisor}}
$$

Otherwise the stated remainder is invalid.

---

# 26. LCM Application — Same Remainder

If a number leaves the **same remainder** when divided by:

$$
a,b,c
$$

then:

$$
\boxed{
N=\operatorname{LCM}(a,b,c)+r
}
$$

for the smallest positive solution greater than the divisors when appropriate.

---

# 27. LCM Application — Different Remainders

If the remainders are different, for example:

$$
N\equiv r_1\pmod a
$$

$$
N\equiv r_2\pmod b
$$

then the simple LCM + remainder formula does not directly apply.

This becomes a **Chinese Remainder Theorem / congruence** type problem.

> [!warning] Exam Tip
> **Same remainder → LCM shortcut.**
>
> **Different remainders → do not blindly use LCM + remainder.**

---

# 28. LCM Application — Fractions of Time

Suppose two machines complete cycles every:

$$
\frac12
$$

and:

$$
\frac34
$$

hours.

Convert to a common unit first, then use the appropriate LCM logic.

> [!tip]
> For time problems, convert all quantities to the same unit before calculating.

---

# 29. LCM and HCF of Two Numbers

For two positive integers:

$$
a,b
$$

if:

$$
H=\operatorname{HCF}(a,b)
$$

and:

$$
L=\operatorname{LCM}(a,b)
$$

then:

$$
\boxed{HL=ab}
$$

Therefore:

$$
\boxed{
a\times b=H\times L
}
$$

This relationship is extremely useful when one of HCF or LCM is missing.

---

# 30. Finding a Missing Number

Suppose:

$$
a=18
$$

HCF:

$$
6
$$

LCM:

$$
72
$$

Find `b`.

Use:

$$
HCF\times LCM=a\times b
$$

Therefore:

$$
6\times72=18b
$$

$$
432=18b
$$

$$
b=24
$$

Therefore:

$$
\boxed{24}
$$

---

# 31. LCM of Three Numbers — Important Warning

For **two numbers**:

$$
\boxed{HCF\times LCM=ab}
$$

But you should **not** blindly use:

$$
HCF\times LCM=abc
$$

for three numbers.

For three or more numbers, use prime factorization or repeated LCM calculation.

> [!warning] Common Trap
> The simple product relationship is directly valid for **two numbers**.

---

# 32. LCM and HCF Through Exponents

Suppose:

$$
A=2^a3^b5^c
$$

and:

$$
B=2^d3^e5^f
$$

Then:

### HCF

$$
\boxed{
2^{\min(a,d)}
3^{\min(b,e)}
5^{\min(c,f)}
}
$$

### LCM

$$
\boxed{
2^{\max(a,d)}
3^{\max(b,e)}
5^{\max(c,f)}
}
$$

---

# 33. Example — HCF and LCM Together

Let:

$$
A=2^4\times3^2\times5
$$

and:

$$
B=2^2\times3^3\times7
$$

### HCF

Take minimum exponents:

$$
2^2\times3^2
$$

Therefore:

$$
\boxed{36}
$$

### LCM

Take maximum exponents:

$$
2^4\times3^3\times5\times7
$$

Therefore:

$$
\boxed{15120}
$$

---

# 34. LCM and Divisibility

If:

$$
a\mid b
$$

then:

$$
\boxed{\operatorname{LCM}(a,b)=b}
$$

More generally, if:

$$
a\mid b
$$

and:

$$
b\mid c
$$

then:

$$
\boxed{\operatorname{LCM}(a,b,c)=c}
$$

### Example

Since:

$$
4\mid12
$$

and:

$$
12\mid60
$$

we have:

$$
\boxed{\operatorname{LCM}(4,12,60)=60}
$$

---

# 35. LCM of Multiples of a Common Number

If:

$$
A=ka
$$

and:

$$
B=kb
$$

then:

$$
\boxed{
\operatorname{LCM}(ka,kb)
=
k\operatorname{LCM}(a,b)
}
$$

### Example

Find:

$$
\operatorname{LCM}(12,18)
$$

Write:

$$
12=6\times2
$$

$$
18=6\times3
$$

Therefore:

$$
\operatorname{LCM}(12,18)
=
6\operatorname{LCM}(2,3)
$$

$$
=6\times6
$$

$$
\boxed{36}
$$

---

# 36. LCM of Consecutive Multiples

For:

$$
ka,\ k(a+1)
$$

since:

$$
\operatorname{HCF}(a,a+1)=1
$$

we get:

$$
\boxed{
\operatorname{LCM}(ka,k(a+1))
=
ka(a+1)
}
$$

### Example

For:

$$
12,\ 18
$$

write:

$$
6\times2,\ 6\times3
$$

Then:

$$
6\times2\times3
$$

$$
\boxed{36}
$$

---

# 37. Number of Multiples of LCM in a Range

If:

$$
L=\operatorname{LCM}(a,b)
$$

then the number of common multiples between `1` and `N` is:

$$
\boxed{
\left\lfloor\frac NL\right\rfloor
}
$$

### Example

How many numbers from `1` to `100` are divisible by both `6` and `8`?

First:

$$
L=\operatorname{LCM}(6,8)=24
$$

Then:

$$
\left\lfloor\frac{100}{24}\right\rfloor
$$

$$
\boxed{4}
$$

---

# 38. LCM in Cyclic Problems

Whenever something repeats after fixed intervals, think:

$$
\boxed{\text{LCM}}
$$

Common examples:

- Bells
- Traffic lights
- Machines
- Workers
- Alarms
- Buses
- Timetables
- Maintenance cycles
- Repeating schedules

### Recognition Pattern

> **"When will they meet again?"**
>
> **"When will they occur together?"**
>
> **"After how much time will the cycle repeat?"**
>
> → **LCM**

---

# 39. Important Formula Sheet

> [!important] Must Remember

### Prime Factorization

$$
\boxed{
LCM=
\text{all primes with maximum powers}
}
$$

### Two-Number Relationship

$$
\boxed{
HCF\times LCM=a\times b
}
$$

### LCM From HCF

$$
\boxed{
LCM=\frac{ab}{HCF}
}
$$

### Coprime Numbers

$$
\boxed{
HCF(a,b)=1
\Rightarrow
LCM(a,b)=ab
}
$$

### Fractions

$$
\boxed{
LCM\left(\frac ab,\frac cd\right)
=
\frac{LCM(a,c)}{HCF(b,d)}
}
$$

### Common Multiples

$$
\boxed{
L,2L,3L,\ldots
}
$$

where:

$$
L=LCM
$$

---

# 40. Important Patterns

> [!important] High-Yield Patterns

### Pattern 1 — Smallest Common Multiple

$$
\boxed{\text{LCM}}
$$

### Pattern 2 — Smallest Number Divisible by Several Numbers

$$
\boxed{\text{LCM}}
$$

### Pattern 3 — Repeating Events

$$
\boxed{\text{LCM}}
$$

### Pattern 4 — Same Remainder

$$
\boxed{LCM+r}
$$

### Pattern 5 — Prime Factorization

$$
\boxed{\text{LCM → maximum powers}}
$$

### Pattern 6 — Coprime Numbers

$$
\boxed{LCM=product}
$$

### Pattern 7 — One Number Divides Another

If:

$$
a\mid b
$$

then:

$$
\boxed{LCM(a,b)=b}
$$

### Pattern 8 — Count Common Multiples

Find LCM first, then count its multiples.

---

# 41. HCF vs LCM

> [!important] Never Confuse These

| Concept | HCF | LCM |
|---|---|---|
| Meaning | Greatest common factor | Least common multiple |
| Think | Factors | Multiples |
| Prime powers | Minimum | Maximum |
| Typical wording | Greatest / largest / maximum | Smallest / least / first |
| Equal groups | HCF | — |
| Repeating events | — | LCM |
| Greatest measure | HCF | — |
| Common occurrence | — | LCM |
| Two-number relation | `HCF × LCM = Product` | `HCF × LCM = Product` |

### Memory Trick

> **HCF → DOWN to common factors**
>
> **LCM → UP to common multiples**

---

# 42. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Using minimum powers for LCM.
- ❌ Using maximum powers for HCF.
- ❌ Forgetting prime factors that appear in only one number.
- ❌ Confusing LCM with the largest common multiple.
- ❌ Forgetting that LCM is the **smallest positive** common multiple.
- ❌ Using `HCF × LCM = product` directly for three or more numbers.
- ❌ Using `LCM + remainder` when remainders are different.
- ❌ Forgetting to convert units in time problems.
- ❌ Forgetting that if one number divides another, the larger number is the LCM.
- ❌ Using the fraction HCF formula for LCM questions.

---

# 43. Exam Strategy

> [!tip] Fast Decision Tree

### Question says:

**"Smallest number divisible by..."**

Think:

$$
\boxed{LCM}
$$

### "When will events happen together again?"

Think:

$$
\boxed{LCM}
$$

### "Least common multiple"

Directly:

$$
\boxed{LCM}
$$

### "Prime factorization"

Take:

$$
\boxed{\text{maximum exponents}}
$$

### "Coprime numbers"

Use:

$$
\boxed{LCM=product}
$$

### "Same remainder"

Use:

$$
\boxed{LCM+r}
$$

### "Given HCF and two numbers"

Use:

$$
\boxed{
LCM=\frac{ab}{HCF}
}
$$

---

# 44. HCL Preparation Priority

**Priority:** 🔥🔥 Extremely High

LCM is heavily connected with:

- HCF
- Remainders
- Divisibility
- Fractions
- Cyclic problems
- Time and work-style applications
- Bells and alarms
- Number-system problems

### Master These First

1. LCM definition
2. Prime factorization method
3. Maximum-exponent rule
4. HCF-LCM relationship
5. LCM of multiple numbers
6. Coprime numbers
7. LCM of fractions
8. Repeating-event problems
9. Same-remainder problems
10. Smallest-divisible-number problems

---

# 45. Practice Checklist

- [ ] Find LCM by listing multiples
- [ ] Find LCM by prime factorization
- [ ] Find LCM of 3 or more numbers
- [ ] Use HCF-LCM relationship
- [ ] Practice coprime numbers
- [ ] Find LCM of fractions
- [ ] Practice repeating-event problems
- [ ] Practice bell problems
- [ ] Practice traffic-light problems
- [ ] Practice same-remainder questions
- [ ] Practice smallest-divisible-number questions
- [ ] Practice common-multiple counting
- [ ] Revise maximum-exponent rule

---

# 46. Related Topics

- [[HCF and LCM]]
- [[HCF]]
- [[Factors]]
- [[Multiples]]
- [[Factorization]]
- [[Remainders]]
- [[Divisibility Rules]]
- [[HCF-LCM Relationship]]
- [[HCF and LCM of Fractions]]
- [[Application Problems]]

---

# 47. Quick Revision

> [!summary] One-Minute Revision

### Definition

$$
\boxed{
LCM=\text{smallest positive common multiple}
}
$$

### Prime Factorization

$$
\boxed{
LCM=\text{all primes with maximum powers}
}
$$

### Two Numbers

$$
\boxed{
HCF\times LCM=a\times b
}
$$

### Coprime Numbers

$$
\boxed{
HCF=1\Rightarrow LCM=ab
}
$$

### Fractions

$$
\boxed{
LCM=
\frac{LCM(\text{numerators})}
{HCF(\text{denominators})}
}
$$

### Common Multiples

$$
\boxed{
L,2L,3L,\ldots
}
$$

### Same Remainder

$$
\boxed{
N=LCM+r
}
$$

### Golden Memory Trick

> **LCM → take every required prime → use the maximum exponent.**

### One-Line Recognition

> **"Smallest", "least", "together again", "common multiple", or "divisible by all" → THINK LCM.**