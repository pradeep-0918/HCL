---
type: concept
subject: aptitude
topic: "Product of Factors"
parent: "01. Number System/Factors and Multiples"
company: HCL
difficulty: medium
priority: high
status: not-started
tags:
  - aptitude
  - hcl
  - number-system
  - factors
  - product-of-factors
  - factorization
  - quantitative-aptitude
wikilinks:
  - "[[01. Number System]]"
  - "[[Factors and Multiples]]"
  - "[[Factors]]"
  - "[[Multiples]]"
  - "[[Number of Factors]]"
  - "[[Sum of Factors]]"
  - "[[Factorization]]"
  - "[[HCF]]"
  - "[[LCM]]"
---

# Product of Factors

## 1. Core Concept

> [!summary] Definition
> The **product of factors** of a positive integer `N` means multiplying all its positive factors together.

### Example

Factors of `12`:

$$
1,2,3,4,6,12
$$

Therefore:

$$
1\times2\times3\times4\times6\times12
$$

$$
\boxed{1728}
$$

So:

$$
\boxed{\text{Product of factors of 12}=1728}
$$

---

# 2. Most Important Formula

If `N` has:

$$
\boxed{\tau(N)}
$$

positive factors, then the product of all positive factors is:

$$
\boxed{
N^{\frac{\tau(N)}{2}}
}
$$

This is the **golden formula** for product of factors.

---

# 3. Why the Formula Works

Factors occur in pairs:

$$
d,\frac Nd
$$

Their product is always:

$$
d\times\frac Nd=N
$$

Therefore every factor pair contributes exactly:

$$
\boxed{N}
$$

If there are `τ(N)` factors, there are:

$$
\frac{\tau(N)}2
$$

pairs.

Therefore:

$$
\boxed{
\text{Product of factors}
=
N^{\tau(N)/2}
}
$$

---

# 4. Example — 12

We know:

$$
12
$$

has:

$$
6
$$

factors.

Therefore:

$$
\text{Product}
=
12^{6/2}
$$

$$
=12^3
$$

$$
\boxed{1728}
$$

---

# 5. Example — 18

Factors:

$$
1,2,3,6,9,18
$$

Number of factors:

$$
\tau(18)=6
$$

Therefore:

$$
\text{Product}
=
18^{6/2}
$$

$$
=18^3
$$

$$
\boxed{5832}
$$

---

# 6. Perfect Square Case

This is the most important special case.

Suppose:

$$
N
$$

is a perfect square.

Then:

$$
\sqrt N
$$

is a factor that pairs with itself:

$$
\sqrt N\times\sqrt N=N
$$

Therefore:

$$
\boxed{
\text{Product of factors}
=
N^{\frac{\tau(N)}2}
}
$$

still works.

---

# 7. Example — 36

Prime factorization:

$$
36=2^2\times3^2
$$

Number of factors:

$$
\tau(36)
=
(2+1)(2+1)
$$

$$
=9
$$

Therefore:

$$
\text{Product}
=
36^{9/2}
$$

This may look like a fractional exponent.

Rewrite:

$$
36^{9/2}
=
36^4\sqrt{36}
$$

$$
=36^4\times6
$$

Therefore the result is an integer.

> [!important] Key Point
> When `N` is a perfect square, `τ(N)` is odd.
>
> The square-root factor is the **unpaired factor**.

---

# 8. Alternative Perfect-Square Formula

If `N` is a perfect square:

$$
\boxed{
\text{Product of factors}
=
N^{(\tau(N)-1)/2}\times\sqrt N
}
$$

### Example

For:

$$
N=36
$$

and:

$$
\tau(36)=9
$$

we get:

$$
36^{(9-1)/2}\times6
$$

$$
=36^4\times6
$$

Same result.

---

# 9. Factor Pair Method

For `36`:

$$
(1,36)
$$

$$
(2,18)
$$

$$
(3,12)
$$

$$
(4,9)
$$

and:

$$
(6,6)
$$

Each pair gives:

$$
36
$$

There are four complete pairs plus one square-root factor.

Therefore:

$$
36^4\times6
$$

---

# 10. Prime Number Case

For a prime number:

$$
p
$$

its factors are:

$$
1,p
$$

Therefore:

$$
\text{Product}=1\times p
$$

$$
\boxed{p}
$$

Using the formula:

$$
\tau(p)=2
$$

so:

$$
p^{2/2}=p
$$

Correct.

---

# 11. Number 1

The only positive factor of `1` is:

$$
1
$$

Therefore:

$$
\boxed{\text{Product of factors of 1}=1}
$$

---

# 12. Using Prime Factorization

Suppose:

$$
N=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

First calculate:

$$
\boxed{
\tau(N)=
(a_1+1)(a_2+1)\cdots(a_k+1)
}
$$

Then:

$$
\boxed{
\text{Product of factors}
=
N^{\tau(N)/2}
}
$$

> [!tip] Exam Strategy
> You usually **do not need to list the factors**.

---

# 13. Example — 72

Prime factorization:

$$
72=2^3\times3^2
$$

Number of factors:

$$
\tau(72)
=
(3+1)(2+1)
$$

$$
=12
$$

Therefore:

$$
\text{Product}
=
72^{12/2}
$$

$$
\boxed{72^6}
$$

There is no need to expand this unless the question asks for the actual value.

---

# 14. Example — 120

Prime factorization:

$$
120=2^3\times3\times5
$$

Number of factors:

$$
\tau(120)
=
(3+1)(1+1)(1+1)
$$

$$
=16
$$

Therefore:

$$
\text{Product}
=
120^{16/2}
$$

$$
\boxed{120^8}
$$

---

# 15. Product of Proper Factors

The product of all proper factors means the product of all positive factors except `N`.

Since:

$$
\text{Product of all factors}
=
N^{\tau(N)/2}
$$

remove `N`:

$$
\boxed{
\text{Product of proper factors}
=
N^{\tau(N)/2-1}
}
$$

### Example

For `12`:

$$
\tau(12)=6
$$

All-factor product:

$$
12^3
$$

Proper-factor product:

$$
12^3\div12
$$

$$
=12^2
$$

$$
\boxed{144}
$$

Check:

$$
1\times2\times3\times4\times6=144
$$

---

# 16. Product of Proper Factors — Perfect Square

For a perfect square, the square-root factor is special.

### Example

For `36`:

Proper factors:

$$
1,2,3,4,6,9,12,18
$$

Their product is:

$$
1\times2\times3\times4\times6\times9\times12\times18
$$

Using the total product:

$$
36^{9/2}
$$

Remove `36`:

$$
36^{9/2-1}
$$

$$
=36^{7/2}
$$

which can be written as:

$$
36^3\times6
$$

---

# 17. Product of Factors Less Than √N

Factors below:

$$
\sqrt N
$$

have corresponding factors above:

$$
\sqrt N
$$

For each pair:

$$
d\times\frac Nd=N
$$

Therefore, factor-pair questions can often be solved without listing every factor.

---

# 18. Important Relationship

For every positive integer `N`:

$$
\boxed{
\prod_{d\mid N}d
=
N^{\tau(N)/2}
}
$$

Here:

$$
d\mid N
$$

means:

> `d` is a divisor/factor of `N`.

This is the mathematical form of the product-of-factors formula.

---

# 19. Product of Factors and Number of Factors

These two formulas should be remembered together.

### Number of factors

$$
\boxed{
\tau(N)=\prod(a_i+1)
}
$$

### Product of factors

$$
\boxed{
P(N)=N^{\tau(N)/2}
}
$$

Therefore the workflow is:

$$
\boxed{
\text{Prime factorization}
\rightarrow
\tau(N)
\rightarrow
N^{\tau(N)/2}
}
$$

---

# 20. Important Perfect-Square Pattern

> [!important] Very Important

If:

$$
N
$$

is a perfect square, then:

$$
\tau(N)
$$

is odd.

Therefore:

$$
\frac{\tau(N)}2
$$

is a half-integer.

In such cases:

$$
\boxed{
N^{\tau(N)/2}
}
$$

should be interpreted using:

$$
\sqrt N
$$

Example:

$$
N=100
$$

If:

$$
\tau(100)=9
$$

then:

$$
100^{9/2}
=
100^4\times10
$$

---

# 21. Product of Factors of a Perfect Square

If:

$$
N=m^2
$$

and:

$$
\tau(N)=2k+1
$$

then:

$$
\boxed{
P(N)=N^k\sqrt N
}
$$

because:

$$
\frac{\tau(N)}2
=
\frac{2k+1}{2}
=
k+\frac12
$$

Therefore:

$$
N^{k+1/2}
=
N^k\sqrt N
$$

---

# 22. Example — 144

Prime factorization:

$$
144=2^4\times3^2
$$

Number of factors:

$$
\tau(144)
=
(4+1)(2+1)
$$

$$
=15
$$

Since `144` is a perfect square:

$$
\sqrt{144}=12
$$

Therefore:

$$
P(144)
=
144^{15/2}
$$

or:

$$
\boxed{
144^7\times12
}
$$

---

# 23. Product of Factors and Prime Factorization

Suppose:

$$
N=2^a3^b
$$

Then:

$$
\tau(N)=(a+1)(b+1)
$$

Therefore:

$$
\boxed{
P(N)
=
(2^a3^b)^{(a+1)(b+1)/2}
}
$$

This is usually enough unless the question asks for the exact numerical value.

---

# 24. Product of Factors Divisible by a Number

This is an advanced pattern.

Suppose you need the product of factors of `N` satisfying an additional condition, such as:

> factors divisible by `2`.

The normal product formula:

$$
N^{\tau(N)/2}
$$

cannot be applied blindly because you are no longer taking **all** factors.

Instead:

1. Determine which factors satisfy the condition.
2. Count or pair those factors.
3. Use prime-exponent structure where necessary.

> [!warning] Exam Tip
> Do not apply the ordinary product-of-all-factors formula to a restricted subset without checking the condition.

---

# 25. Product of Factors — Quick Example

Find the product of all positive factors of:

$$
18
$$

### Step 1 — Factorize

$$
18=2\times3^2
$$

### Step 2 — Number of factors

$$
\tau(18)
=
(1+1)(2+1)
$$

$$
=6
$$

### Step 3 — Product

$$
P(18)
=
18^{6/2}
$$

$$
=18^3
$$

$$
\boxed{5832}
$$

---

# 26. Product of Factors — Large Number

Find the product of all positive factors of:

$$
360
$$

Prime factorization:

$$
360=2^3\times3^2\times5
$$

Number of factors:

$$
\tau(360)
=
(3+1)(2+1)(1+1)
$$

$$
=24
$$

Therefore:

$$
P(360)
=
360^{24/2}
$$

$$
\boxed{360^{12}}
$$

---

# 27. Common Traps

> [!warning] Avoid These Mistakes

- ❌ Listing all factors when the formula is faster.
- ❌ Forgetting to calculate `τ(N)` first.
- ❌ Using `N^(τ/2)` without understanding the perfect-square case.
- ❌ Forgetting that perfect squares have an unpaired square-root factor.
- ❌ Confusing product of factors with sum of factors.
- ❌ Forgetting that the formula is for **positive factors**.
- ❌ Applying the formula directly to only a subset of factors.
- ❌ Expanding huge powers unnecessarily.

---

# 28. Exam Strategy

> [!tip] Fast Decision Tree

### Asked: "Product of all factors?"

Use:

$$
\boxed{
N^{\tau(N)/2}
}
$$

### Asked: "But τ(N) is unknown?"

First find:

$$
\boxed{
\tau(N)=\prod(a_i+1)
}
$$

### Asked: "N is a perfect square?"

Use:

$$
\boxed{
N^{(\tau(N)-1)/2}\sqrt N
}
$$

### Asked: "Product of proper factors?"

Use:

$$
\boxed{
N^{\tau(N)/2-1}
}
$$

### Asked: "Only some factors?"

Do **not** automatically use the normal product formula.

---

# 29. HCL Preparation Priority

**Priority:** 🔥 High

### Master These First

1. Factor-pair concept
2. Product of all factors
3. `τ(N)` formula
4. Perfect-square case
5. Product of proper factors
6. Large-number questions
7. Difference between `τ`, `σ`, and product of factors
8. Restricted-factor questions

---

# 30. Practice Checklist

- [ ] Understand factor pairing
- [ ] Memorize product formula
- [ ] Practice calculating `τ(N)`
- [ ] Practice non-square numbers
- [ ] Practice perfect squares
- [ ] Practice product of proper factors
- [ ] Practice prime numbers
- [ ] Practice large numbers
- [ ] Practice mixed factor questions
- [ ] Revise common traps

---

# 31. Related Topics

- [[Factors and Multiples]]
- [[Factors]]
- [[Multiples]]
- [[Number of Factors]]
- [[Sum of Factors]]
- [[Factorization]]
- [[HCF]]
- [[LCM]]
- [[Prime and Composite Numbers]]

---

# 32. Quick Revision

> [!summary] One-Minute Revision

### Main Formula

$$
\boxed{
P(N)=N^{\tau(N)/2}
}
$$

where:

$$
\tau(N)=\text{number of positive factors of }N
$$

### Find `τ(N)`

If:

$$
N=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

then:

$$
\boxed{
\tau(N)=
(a_1+1)(a_2+1)\cdots(a_k+1)
}
$$

### Perfect Square

If:

$$
N=m^2
$$

then:

$$
\boxed{
P(N)=N^{(\tau(N)-1)/2}\times m
}
$$

### Proper Factors

$$
\boxed{
P_{\text{proper}}(N)
=
N^{\tau(N)/2-1}
}
$$

### Golden Memory Trick

> **Factors pair to `N`. Count the pairs using `τ(N)/2`, then multiply `N` that many times.**

### Complete Factor Toolkit So Far

$$
\boxed{\tau(N)=\text{How many factors}}
$$

$$
\boxed{\sigma(N)=\text{Sum of factors}}
$$

$$
\boxed{P(N)=\text{Product of factors}}
$$