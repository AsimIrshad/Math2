# Integrals


# What is an Integral?

## Introduction

An **integral** is the counterpart of a derivative. Differentiation asks how fast a function is changing. Integration asks two related questions:

1. What function has this given derivative? (**indefinite integral**)
2. What is the net accumulated quantity (area, distance, total change) between two values of x? (**definite integral**)

If F′(x) = f(x), then F is an **antiderivative** of f, and we write:

```
∫ f(x) dx = F(x) + C
```

The symbol ∫ is the integral sign, f(x) is the **integrand**, dx marks the variable of integration, and C is the **constant of integration**.

### Geometric Idea (Area)

The definite integral of a continuous function f from x = a to x = b equals the **net signed area** between the graph of y = f(x) and the x-axis, from a to b:

- Area **above** the x-axis is counted as positive
- Area **below** the x-axis is counted as negative

```
∫ₐᵇ f(x) dx  =  net signed area
```

If f(x) ≥ 0 on [a, b], this is simply the ordinary area under the curve.

### Link to Derivatives

The **Fundamental Theorem of Calculus** connects the two operations:

```
If F′(x) = f(x), then  ∫ₐᵇ f(x) dx = F(b) − F(a)
```

Differentiation and integration undo each other (up to a constant). This is why we first learn antiderivatives, then use them to evaluate definite integrals.

\newpage

# Indefinite Integrals and Definite Integrals

## Indefinite Integral

The **indefinite integral** of f is the family of all antiderivatives of f:

```
∫ f(x) dx = F(x) + C,    where F′(x) = f(x)
```

C is needed because the derivative of a constant is zero. Different choices of C give different members of the same family — they differ by a vertical shift of the graph.

**Example 1:** Find ∫ 4x³ dx

```
∫ 4x³ dx = 4 · (x⁴/4) + C = x⁴ + C
```

Check: d/dx (x⁴ + C) = 4x³ ✓

**Example 2:** Find ∫ (3x² − 2x + 5) dx

```
= 3 · (x³/3) − 2 · (x²/2) + 5x + C
= x³ − x² + 5x + C
```

### Why the Constant Matters

```
d/dx (x²)     = 2x
d/dx (x² + 7) = 2x
d/dx (x² − 3) = 2x
```

All three functions have the same derivative, so:

```
∫ 2x dx = x² + C
```

If an initial condition is given (for example F(0) = 4), we can solve for one particular C.

**Example 3:** Find F if F′(x) = 2x and F(0) = 4

```
F(x) = x² + C
F(0) = 0 + C = 4  →  C = 4
F(x) = x² + 4
```

## Definite Integral

The **definite integral** of f from a to b is a **number**, not a family of functions:

```
∫ₐᵇ f(x) dx
```

Here a is the **lower limit** and b is the **upper limit**.

### Evaluation (Fundamental Theorem of Calculus)

If f is continuous on [a, b] and F is any antiderivative of f, then:

```
∫ₐᵇ f(x) dx = F(b) − F(a)
```

We often write:

```
[F(x)]ₐᵇ  =  F(b) − F(a)
```

**Important:** The constant C cancels, so we may omit it when evaluating a definite integral.

**Example 1:** Evaluate ∫₁³ 2x dx

```
∫₁³ 2x dx = [x²]₁³ = 9 − 1 = 8
```

Geometric check: the region is a trapezoid (or triangle of height 6 on base 2, plus a rectangle). Net area = 8.

**Example 2:** Evaluate ∫₀² (3x² − 4) dx

```
= [x³ − 4x]₀²
= (8 − 8) − (0 − 0)
= 0
```

The areas above and below the x-axis cancel. Net signed area is 0; the total geometric area is not 0.

**Example 3:** Evaluate ∫₀^π sin x dx

```
= [−cos x]₀^π
= (−cos π) − (−cos 0)
= (−(−1)) − (−1)
= 1 + 1
= 2
```

The area under one arch of y = sin x from 0 to π is 2.

## Indefinite vs Definite — Side by Side

| Feature              | Indefinite integral              | Definite integral                    |
|----------------------|----------------------------------|--------------------------------------|
| Notation             | ∫ f(x) dx                        | ∫ₐᵇ f(x) dx                          |
| Result               | A family of functions, F(x) + C  | A number                             |
| Limits               | None                             | Lower a, upper b                     |
| Geometric meaning    | Antiderivative (family of curves)| Net signed area from a to b          |
| Constant C           | Required                         | Cancels; usually omitted             |
| Dummy variable       | x is the variable                | Dummy: ∫ₐᵇ f(t) dt is the same       |

**Dummy variable:** The letter used inside a definite integral does not matter:

```
∫₀¹ x² dx  =  ∫₀¹ t² dt  =  ∫₀¹ u² du  =  1/3
```

\newpage

# Rules Satisfied by Definite Integrals

## Introduction

Definite integrals obey algebraic rules that match the geometry of area. These rules let us split intervals, reverse limits, pull out constants, and compare integrals without always computing from scratch.

Assume f and g are continuous on the relevant intervals, and c, k are constants.

## Basic Algebraic Rules

| Rule                         | Formula                                                      |
|------------------------------|--------------------------------------------------------------|
| Constant multiple            | ∫ₐᵇ k f(x) dx = k ∫ₐᵇ f(x) dx                                |
| Sum                          | ∫ₐᵇ [f(x) + g(x)] dx = ∫ₐᵇ f(x) dx + ∫ₐᵇ g(x) dx             |
| Difference                   | ∫ₐᵇ [f(x) − g(x)] dx = ∫ₐᵇ f(x) dx − ∫ₐᵇ g(x) dx             |
| Zero-width interval          | ∫ₐᵃ f(x) dx = 0                                              |
| Reversal of limits           | ∫ₐᵇ f(x) dx = − ∫<sub>b</sub><sup>a</sup> f(x) dx            |
| Additivity (split interval)  | ∫ₐᵇ f(x) dx = ∫ₐᶜ f(x) dx + ∫<sub>c</sub><sup>b</sup> f(x) dx |

The split-interval rule holds even if c is not between a and b, as long as the integrals exist.

**Example 1: Constant multiple and sum**

```
∫₀² (4x + 6) dx
= 4 ∫₀² x dx + 6 ∫₀² 1 dx
= 4 [x²/2]₀² + 6 [x]₀²
= 4(2) + 6(2)
= 8 + 12
= 20
```

**Example 2: Reversal of limits**

```
∫₃¹ 2x dx = − ∫₁³ 2x dx = − [x²]₁³ = −(9 − 1) = −8
```

Directly: [x²]₃¹ = 1 − 9 = −8. Same result.

**Example 3: Split the interval**

Given ∫₀² f(x) dx = 5 and ∫₂⁶ f(x) dx = 3, find ∫₀⁶ f(x) dx.

```
∫₀⁶ f(x) dx = ∫₀² f(x) dx + ∫₂⁶ f(x) dx = 5 + 3 = 8
```

**Example 4: Using the reverse and split rules together**

Given ∫₁⁴ f(x) dx = 7 and ∫₁⁶ f(x) dx = 10, find ∫₄⁶ f(x) dx.

```
∫₁⁶ f(x) dx = ∫₁⁴ f(x) dx + ∫₄⁶ f(x) dx
10 = 7 + ∫₄⁶ f(x) dx
∫₄⁶ f(x) dx = 3
```

## Comparison and Sign Rules

| Rule                    | Statement                                                                 |
|-------------------------|---------------------------------------------------------------------------|
| Nonnegative integrand   | If f(x) ≥ 0 on [a, b], then ∫ₐᵇ f(x) dx ≥ 0                              |
| Comparison              | If f(x) ≤ g(x) on [a, b], then ∫ₐᵇ f(x) dx ≤ ∫ₐᵇ g(x) dx                 |
| Absolute value bound    | \|∫ₐᵇ f(x) dx\| ≤ ∫ₐᵇ \|f(x)\| dx                                        |
| Constant bounds         | If m ≤ f(x) ≤ M on [a, b], then m(b−a) ≤ ∫ₐᵇ f(x) dx ≤ M(b−a)            |

**Example 5:** Without evaluating, explain why ∫₀¹ x² dx > 0.

```
On [0, 1], x² ≥ 0 and x² is not identically zero.
Therefore the integral (area) is strictly positive.
(Actual value: 1/3.)
```

**Example 6: Bounds without computing the exact value**

On [1, 3], 1 ≤ x² ≤ 9, so:

```
1 · (3 − 1) ≤ ∫₁³ x² dx ≤ 9 · (3 − 1)
2 ≤ ∫₁³ x² dx ≤ 18
```

Exact value: [x³/3]₁³ = 9 − 1/3 = 26/3 ≈ 8.67, which lies in (2, 18).

## Even and Odd Functions

If f is integrable on [−a, a]:

| Type of f      | Condition           | Integral over [−a, a]              |
|----------------|---------------------|------------------------------------|
| Even           | f(−x) = f(x)        | ∫₋ₐᵃ f(x) dx = 2 ∫₀ᵃ f(x) dx      |
| Odd            | f(−x) = −f(x)       | ∫₋ₐᵃ f(x) dx = 0                   |

**Example 7:**

```
∫₋₂² x³ dx = 0                              because x³ is odd
∫₋₁¹ x² dx = 2 ∫₀¹ x² dx = 2 · (1/3) = 2/3  because x² is even
```

## Average Value

The **average value** of a continuous function f on [a, b] is:

```
f_avg = (1/(b − a)) ∫ₐᵇ f(x) dx
```

There exists at least one c in [a, b] with f(c) = f_avg (Mean Value Theorem for Integrals).

**Example 8:** Average value of f(x) = 3x² on [0, 2]

```
f_avg = (1/2) ∫₀² 3x² dx
      = (1/2) [x³]₀²
      = (1/2)(8)
      = 4
```

\newpage

# Integration of Trigonometric Functions

## Introduction

Trigonometric integrals reverse the familiar derivatives of sin, cos, tan, and the related functions. Many of them follow at once from differentiation; others need a trigonometric identity first.

Angles are in **radians**.

## Standard Formulas

| Integral                         | Result                                           |
|----------------------------------|--------------------------------------------------|
| ∫ sin x dx                       | −cos x + C                                       |
| ∫ cos x dx                       | sin x + C                                        |
| ∫ tan x dx                       | ln\|sec x\| + C  (or −ln\|cos x\| + C)           |
| ∫ cot x dx                       | ln\|sin x\| + C                                  |
| ∫ sec x dx                       | ln\|sec x + tan x\| + C                          |
| ∫ csc x dx                       | −ln\|csc x + cot x\| + C                         |
| ∫ sec² x dx                      | tan x + C                                        |
| ∫ csc² x dx                      | −cot x + C                                       |
| ∫ sec x tan x dx                 | sec x + C                                        |
| ∫ csc x cot x dx                 | −csc x + C                                       |

**Check for ∫ tan x dx:**

```
tan x = sin x / cos x
∫ tan x dx = ∫ (sin x / cos x) dx
Let u = cos x,  du = −sin x dx
= − ∫ du/u = −ln|u| + C = −ln|cos x| + C = ln|sec x| + C
```

## Linear Argument (Chain Rule in Reverse)

If the inner function is ax + b:

```
∫ sin(ax + b) dx = −(1/a) cos(ax + b) + C
∫ cos(ax + b) dx =  (1/a) sin(ax + b) + C
```

**Example 1:** ∫ sin(3x) dx

```
= −(1/3) cos(3x) + C
```

**Example 2:** ∫ cos(2x − π/4) dx

```
= (1/2) sin(2x − π/4) + C
```

**Example 3:** Evaluate ∫₀^(π/2) cos x dx

```
= [sin x]₀^(π/2) = sin(π/2) − sin 0 = 1 − 0 = 1
```

**Example 4:** Evaluate ∫₀^(π/4) sec² x dx

```
= [tan x]₀^(π/4) = tan(π/4) − tan 0 = 1 − 0 = 1
```

## Powers of Sine and Cosine (Identities)

When the power is even, the **double-angle identities** are useful:

```
sin² x = (1 − cos 2x) / 2
cos² x = (1 + cos 2x) / 2
sin x cos x = (1/2) sin 2x
```

**Example 5:** ∫ sin² x dx

```
∫ sin² x dx = ∫ (1 − cos 2x)/2 dx
            = (1/2)x − (1/4) sin 2x + C
```

**Example 6:** ∫ cos² x dx

```
∫ cos² x dx = ∫ (1 + cos 2x)/2 dx
            = (1/2)x + (1/4) sin 2x + C
```

**Example 7:** Evaluate ∫₀^π sin² x dx

```
= [(1/2)x − (1/4) sin 2x]₀^π
= (π/2 − 0) − (0 − 0)
= π/2
```

When an **odd power** of sine or cosine appears, peel off one factor and use:

```
sin² x + cos² x = 1
```

**Example 8:** ∫ sin³ x dx

```
∫ sin³ x dx = ∫ sin² x · sin x dx
            = ∫ (1 − cos² x) sin x dx

Let u = cos x,  du = −sin x dx
= − ∫ (1 − u²) du
= − (u − u³/3) + C
= −cos x + (1/3) cos³ x + C
```

## Mixed Products

**Example 9:** ∫ sin(2x) cos(2x) dx

```
Let u = sin(2x),  du = 2 cos(2x) dx
∫ sin(2x) cos(2x) dx = (1/2) ∫ u du = (1/4) u² + C
                     = (1/4) sin²(2x) + C
```

(Equivalently: (1/2) ∫ sin(4x) dx using the double-angle formula.)

\newpage

# Integration of Logarithmic Functions

## Introduction

Logarithmic integrals rest on two facts:

```
d/dx [ln|x|] = 1/x
d/dx [logₐ |x|] = 1/(x ln a)
```

So the most basic logarithmic integral is the power-rule exception n = −1:

```
∫ xⁿ dx = xⁿ⁺¹/(n+1) + C,    n ≠ −1
∫ x⁻¹ dx = ∫ (1/x) dx = ln|x| + C
```

## Standard Formulas

| Integral                         | Result                                      |
|----------------------------------|---------------------------------------------|
| ∫ (1/x) dx                       | ln\|x\| + C                                 |
| ∫ dx/(ax + b)                    | (1/a) ln\|ax + b\| + C                      |
| ∫ f′(x)/f(x) dx                  | ln\|f(x)\| + C                              |
| ∫ logₐ x dx                      | (x ln x − x)/ln a + C                       |
| ∫ ln x dx                        | x ln x − x + C                              |

The last two use **integration by parts** (next section). We record the results here and derive them there.

**Example 1:** ∫ (1/x) dx, x > 0

```
= ln x + C
```

**Example 2:** ∫ dx/(2x + 3)

```
Let u = 2x + 3,  du = 2 dx
∫ dx/(2x + 3) = (1/2) ∫ du/u = (1/2) ln|u| + C
              = (1/2) ln|2x + 3| + C
```

**Example 3: The ln-derivative pattern**

```
∫ (2x)/(x² + 1) dx

Numerator is the derivative of the inside of the denominator.
Let u = x² + 1,  du = 2x dx
= ∫ du/u = ln|x² + 1| + C
= ln(x² + 1) + C     (since x² + 1 > 0)
```

**Example 4:** Evaluate ∫₁ᵉ (1/x) dx

```
= [ln|x|]₁ᵉ = ln e − ln 1 = 1 − 0 = 1
```

**Example 5:** Evaluate ∫₀¹ dx/(x + 1)

```
= [ln|x + 1|]₀¹ = ln 2 − ln 1 = ln 2
```

## Change of Base

```
logₐ x = ln x / ln a
```

So integrals of logₐ x reduce to integrals of ln x:

```
∫ logₐ x dx = (1 / ln a) ∫ ln x dx
```

**Example 6:** ∫ log₂ x dx  (formula; derivation in the next section)

```
= (1 / ln 2) (x ln x − x) + C
```

## Combining Logs with Polynomials

**Example 7:** ∫ (3x² + 2x)/(x³ + x² + 4) dx  — check whether the numerator is a multiple of the derivative of the denominator.

```
d/dx (x³ + x² + 4) = 3x² + 2x

Yes — they match exactly.
∫ (3x² + 2x)/(x³ + x² + 4) dx = ln|x³ + x² + 4| + C
```

If the numerator is a constant multiple of that derivative, factor the constant out.

\newpage

# Integration by Parts

## Introduction

**Integration by parts** is the integral version of the product rule. It is the main tool when the integrand is a product of two functions of different types (for example, x and sin x, or x and eˣ, or ln x and 1).

### Derivation from the Product Rule

```
d/dx [u(x) v(x)] = u′ v + u v′
```

Integrate both sides:

```
u v = ∫ u′ v dx + ∫ u v′ dx
```

Rearrange:

```
∫ u dv = u v − ∫ v du
```

or, in function form:

```
∫ u(x) v′(x) dx = u(x) v(x) − ∫ v(x) u′(x) dx
```

### How to Choose u and dv

We choose u to be the factor that **becomes simpler when differentiated**, and dv to be the factor that is **easy to integrate**.

A common priority list for u is **LIATE**:

| Order | Type                         | Typical u          |
|-------|------------------------------|--------------------|
| L     | Logarithmic                  | ln x, logₐ x       |
| I     | Inverse trigonometric        | arctan x, arcsin x |
| A     | Algebraic (polynomials)      | x, x², 3x + 1      |
| T     | Trigonometric                | sin x, cos x       |
| E     | Exponential                  | eˣ, aˣ             |

Choose u as the type that appears **first** in LIATE; the rest goes into dv.

## Worked Examples

**Example 1:** ∫ x eˣ dx

```
u = x          dv = eˣ dx
du = dx        v = eˣ

∫ x eˣ dx = x eˣ − ∫ eˣ dx
          = x eˣ − eˣ + C
          = eˣ (x − 1) + C
```

Check: d/dx [eˣ(x − 1)] = eˣ(x − 1) + eˣ = x eˣ ✓

**Example 2:** ∫ x sin x dx

```
u = x          dv = sin x dx
du = dx        v = −cos x

∫ x sin x dx = −x cos x − ∫ (−cos x) dx
             = −x cos x + ∫ cos x dx
             = −x cos x + sin x + C
```

**Example 3:** ∫ ln x dx   (the standard log integral)

Write ln x as a product: ln x · 1.

```
u = ln x       dv = 1 dx
du = (1/x) dx  v = x

∫ ln x dx = x ln x − ∫ x · (1/x) dx
          = x ln x − ∫ 1 dx
          = x ln x − x + C
```

**Example 4:** ∫ x² ln x dx

```
u = ln x         dv = x² dx
du = (1/x) dx    v = x³/3

∫ x² ln x dx = (x³/3) ln x − ∫ (x³/3)(1/x) dx
             = (x³/3) ln x − (1/3) ∫ x² dx
             = (x³/3) ln x − (1/3)(x³/3) + C
             = (x³/3) ln x − x³/9 + C
```

**Example 5: Definite integral** — ∫₀^(π/2) x cos x dx

```
u = x          dv = cos x dx
du = dx        v = sin x

∫₀^(π/2) x cos x dx = [x sin x]₀^(π/2) − ∫₀^(π/2) sin x dx
                    = (π/2 · 1 − 0) − [−cos x]₀^(π/2)
                    = π/2 − (−cos(π/2) + cos 0)
                    = π/2 − (0 + 1)
                    = π/2 − 1
```

## Repeated Integration by Parts

If u is a polynomial of degree 2 or more, apply the formula more than once.

**Example 6:** ∫ x² eˣ dx

First pass:

```
u = x²         dv = eˣ dx
du = 2x dx     v = eˣ

∫ x² eˣ dx = x² eˣ − 2 ∫ x eˣ dx
```

Second pass (from Example 1): ∫ x eˣ dx = eˣ(x − 1)

```
∫ x² eˣ dx = x² eˣ − 2 eˣ(x − 1) + C
           = eˣ (x² − 2x + 2) + C
```

## Cyclic Integrals (Solve for I)

Sometimes the original integral reappears after two applications. Call it I and solve the equation.

**Example 7:** ∫ eˣ sin x dx

```
Let I = ∫ eˣ sin x dx

u = sin x      dv = eˣ dx
du = cos x dx  v = eˣ

I = eˣ sin x − ∫ eˣ cos x dx
```

Now integrate by parts again on ∫ eˣ cos x dx:

```
u = cos x      dv = eˣ dx
du = −sin x dx v = eˣ

∫ eˣ cos x dx = eˣ cos x − ∫ eˣ (−sin x) dx
              = eˣ cos x + ∫ eˣ sin x dx
              = eˣ cos x + I
```

Substitute back:

```
I = eˣ sin x − (eˣ cos x + I)
I = eˣ sin x − eˣ cos x − I
2I = eˣ (sin x − cos x)
I = (1/2) eˣ (sin x − cos x) + C
```

## Choosing u Incorrectly (What Goes Wrong)

If we swap the choice in ∫ x eˣ dx and set u = eˣ, dv = x dx, then:

```
u = eˣ         dv = x dx
du = eˣ dx     v = x²/2

∫ x eˣ dx = (x²/2) eˣ − ∫ (x²/2) eˣ dx
```

The new integral is **harder**, not easier. That is the signal to switch the assignment of u and dv.

\newpage

# Quick Reference Summary

| Topic                         | Key Idea                                              | Example                                      |
|-------------------------------|-------------------------------------------------------|----------------------------------------------|
| Integral                      | Reverse of derivative; definite = net signed area     | ∫₀¹ 2x dx = 1                                |
| Indefinite integral           | ∫ f(x) dx = F(x) + C, where F′ = f                    | ∫ 3x² dx = x³ + C                            |
| Definite integral             | ∫ₐᵇ f(x) dx = F(b) − F(a)                             | ∫₁³ 2x dx = 8                                |
| Rules (definite)              | Linearity, reverse limits, split interval, even/odd   | ∫ₐᵃ f = 0; ∫ₐᵇ = −∫<sub>b</sub><sup>a</sup>  |
| Trig integrals                | Reverse known derivatives; use identities for powers  | ∫ sin x dx = −cos x + C                      |
| Log integrals                 | ∫ (1/x) dx = ln\|x\| + C; ∫ ln x dx = x ln x − x + C | ∫₁ᵉ (1/x) dx = 1                             |
| Integration by parts          | ∫ u dv = uv − ∫ v du  (LIATE for choosing u)          | ∫ x eˣ dx = eˣ(x − 1) + C                    |

---

*End of Lecture Notes*
