# Derivatives, Analytical Geometry, and Antiderivatives


# The Derivative of a Function

## Introduction

The **derivative** measures how a function changes at a point. Geometrically, it is the slope of the tangent line to the graph of f at that point. Algebraically, it is the limit of the average rate of change as the interval shrinks to zero.

### Definition (Limit Form)

The derivative of f at x = a is:

```
f′(a) = lim (h→0) [f(a + h) − f(a)] / h
```

provided this limit exists. If f′(a) exists, we say f is **differentiable** at a.

Equivalently:

```
f′(a) = lim (x→a) [f(x) − f(a)] / (x − a)
```

### Notation

| Notation        | Meaning                         |
|-----------------|---------------------------------|
| f′(x)           | Derivative of f with respect to x |
| dy/dx           | Leibniz notation                |
| df/dx           | Same as dy/dx when y = f(x)     |
| D(f) or Df      | Operator notation               |
| ẏ               | Dot notation (often for time)   |

### Geometric Meaning

- f′(a) = slope of the tangent line to y = f(x) at x = a
- Equation of the tangent line at (a, f(a)):

```
y − f(a) = f′(a)(x − a)
```

**Example 1:** Find f′(2) for f(x) = x² using the definition.

```
f′(2) = lim (h→0) [f(2+h) − f(2)] / h
      = lim (h→0) [(2+h)² − 4] / h
      = lim (h→0) [4 + 4h + h² − 4] / h
      = lim (h→0) (4h + h²) / h
      = lim (h→0) (4 + h)
      = 4
```

Tangent line at (2, 4): y − 4 = 4(x − 2) → y = 4x − 4

**Example 2:** Find the derivative of f(x) = 3x + 1 from the definition.

```
f′(x) = lim (h→0) [3(x+h) + 1 − (3x + 1)] / h
      = lim (h→0) (3x + 3h + 1 − 3x − 1) / h
      = lim (h→0) 3h / h
      = 3
```

The derivative of a linear function is its slope (constant).

### Differentiability vs Continuity

- If f is differentiable at a, then f is continuous at a.
- The converse is **false**: continuity does not imply differentiability.

**Example:** f(x) = |x| is continuous at x = 0 but not differentiable there (sharp corner; left and right derivatives differ: −1 and +1).

\newpage

# Differentiation Rules

## Introduction

Computing derivatives from the limit definition every time is impractical. Differentiation rules let us find derivatives of polynomials, products, quotients, and powers efficiently.

## Basic Rules

| Rule                    | Formula                                      |
|-------------------------|----------------------------------------------|
| Constant rule           | d/dx [c] = 0                                 |
| Power rule              | d/dx [xⁿ] = n xⁿ⁻¹                          |
| Constant multiple       | d/dx [c·f(x)] = c·f′(x)                      |
| Sum rule                | d/dx [f + g] = f′ + g′                       |
| Difference rule         | d/dx [f − g] = f′ − g′                       |

**Example 1:** Differentiate f(x) = 5x⁴ − 3x² + 7x − 2

```
f′(x) = 5·4x³ − 3·2x + 7 − 0
      = 20x³ − 6x + 7
```

**Example 2:** Differentiate f(x) = √x + 1/x²

```
f(x) = x^(1/2) + x^(−2)
f′(x) = (1/2)x^(−1/2) − 2x^(−3)
      = 1/(2√x) − 2/x³
```

## Product Rule

```
d/dx [f(x)·g(x)] = f′(x)·g(x) + f(x)·g′(x)
```

**Memory aid:** “first times derivative of second, plus second times derivative of first.”

**Example:** f(x) = (x² + 1)(3x − 4)

```
u = x² + 1,   u′ = 2x
v = 3x − 4,   v′ = 3

f′(x) = 2x(3x − 4) + (x² + 1)(3)
      = 6x² − 8x + 3x² + 3
      = 9x² − 8x + 3
```

## Quotient Rule

```
d/dx [f(x)/g(x)] = [f′(x)·g(x) − f(x)·g′(x)] / [g(x)]²
```

**Memory aid:** “low d(high) minus high d(low), over low squared.”

**Example:** f(x) = (2x + 1)/(x − 3)

```
u = 2x + 1,   u′ = 2
v = x − 3,    v′ = 1

f′(x) = [2(x − 3) − (2x + 1)(1)] / (x − 3)²
      = (2x − 6 − 2x − 1) / (x − 3)²
      = −7 / (x − 3)²
```

## Derivatives of Common Functions

| Function     | Derivative              |
|--------------|-------------------------|
| sin x        | cos x                   |
| cos x        | −sin x                  |
| tan x        | sec² x                  |
| eˣ           | eˣ                      |
| aˣ           | aˣ ln a                 |
| ln x         | 1/x                     |
| logₐ x       | 1/(x ln a)              |

**Example:** Differentiate f(x) = x³ sin x + eˣ

```
f′(x) = 3x² sin x + x³ cos x + eˣ
```

\newpage

# The Derivative as a Rate of Change

## Introduction

The derivative f′(x) is the **instantaneous rate of change** of f with respect to x. In applications, this often means velocity, growth rate, marginal cost, or similar quantities.

### Average vs Instantaneous Rate of Change

| Type              | Formula / Meaning                                      |
|-------------------|--------------------------------------------------------|
| Average (on [a,b])| [f(b) − f(a)] / (b − a)  — slope of secant line        |
| Instantaneous     | f′(a) — slope of tangent line at x = a                 |

**Example 1: Position and velocity**

A particle’s position (in meters) at time t (seconds) is s(t) = t³ − 6t² + 9t.

```
Velocity: v(t) = s′(t) = 3t² − 12t + 9

At t = 2:
v(2) = 3(4) − 12(2) + 9 = 12 − 24 + 9 = −3 m/s

Negative velocity means the particle is moving left (or backward).
```

Acceleration:

```
a(t) = v′(t) = 6t − 12
a(2) = 0 m/s²
```

**Example 2: Population growth**

A population (in thousands) is modeled by P(t) = 20e^(0.03t), where t is years after 2020.

```
P′(t) = 20 · 0.03 · e^(0.03t) = 0.6 e^(0.03t)

Growth rate in 2025 (t = 5):
P′(5) = 0.6 e^(0.15) ≈ 0.697 thousand per year ≈ 697 people/year
```

**Example 3: Marginal cost**

If C(x) is the cost of producing x items, then C′(x) is the **marginal cost** — approximately the cost of producing one more item when x items have already been made.

```
C(x) = 0.01x² + 5x + 200
C′(x) = 0.02x + 5

Marginal cost at x = 100:
C′(100) = 0.02(100) + 5 = 7 (currency units per item)
```

### Related Rates (Preview)

If quantities are related by an equation and change with time, differentiate both sides with respect to t (using the chain rule) to relate their rates.

**Example:** A circle’s radius increases at 2 cm/s. How fast is the area increasing when r = 5 cm?

```
A = πr²
dA/dt = 2πr · dr/dt
dA/dt = 2π(5)(2) = 20π cm²/s
```

\newpage

# Chain Rule

## Introduction

The **chain rule** differentiates a composition of functions. If y = f(g(x)), then:

```
dy/dx = f′(g(x)) · g′(x)
```

In Leibniz notation, if y = f(u) and u = g(x):

```
dy/dx = (dy/du) · (du/dx)
```

### How to Apply

1. Identify the outer function f and the inner function g
2. Differentiate the outer, leaving the inner unchanged
3. Multiply by the derivative of the inner

**Example 1:** Differentiate y = (3x² + 1)⁵

```
Outer: u⁵,   Inner: u = 3x² + 1
dy/dx = 5(3x² + 1)⁴ · 6x
      = 30x (3x² + 1)⁴
```

**Example 2:** Differentiate y = √(4x − 1) = (4x − 1)^(1/2)

```
dy/dx = (1/2)(4x − 1)^(−1/2) · 4
      = 2 / √(4x − 1)
```

**Example 3:** Differentiate y = sin(x²)

```
dy/dx = cos(x²) · 2x = 2x cos(x²)
```

**Example 4:** Differentiate y = e^(3x+2)

```
dy/dx = e^(3x+2) · 3 = 3e^(3x+2)
```

**Example 5: Nested composition** — y = ln(sin(2x))

```
dy/dx = (1/sin(2x)) · cos(2x) · 2
      = 2 cos(2x) / sin(2x)
      = 2 cot(2x)
```

### Generalized Power Rule

```
d/dx [u(x)]ⁿ = n [u(x)]ⁿ⁻¹ · u′(x)
```

\newpage

# Derivatives of Inverse Functions and Logarithms

## Derivative of an Inverse Function

If f is differentiable and invertible, and f′(a) ≠ 0, then f⁻¹ is differentiable at b = f(a), and:

```
(f⁻¹)′(b) = 1 / f′(a) = 1 / f′(f⁻¹(b))
```

**In words:** The derivative of the inverse at a point is the reciprocal of the derivative of the original function at the corresponding point.

**Example 1:** f(x) = x³ + 2x + 1. Find (f⁻¹)′(1).

```
f(0) = 1, so f⁻¹(1) = 0
f′(x) = 3x² + 2
(f⁻¹)′(1) = 1 / f′(0) = 1/2
```

**Example 2:** Verify for f(x) = eˣ, f⁻¹(x) = ln x

```
f′(x) = eˣ
(f⁻¹)′(x) = 1 / f′(ln x) = 1 / e^(ln x) = 1/x ✓
```

## Derivatives of Logarithmic Functions

| Function        | Derivative                    |
|-----------------|-------------------------------|
| ln x            | 1/x                           |
| ln|u(x)|        | u′(x)/u(x)                    |
| logₐ x          | 1/(x ln a)                    |
| logₐ|u(x)|      | u′(x)/(u(x) ln a)             |

**Example 1:** Differentiate y = ln(5x² + 3)

```
dy/dx = 10x / (5x² + 3)
```

**Example 2:** Differentiate y = log₂(x³ + 1)

```
dy/dx = 3x² / [(x³ + 1) ln 2]
```

**Example 3: Logarithmic differentiation** — find y′ for y = xˣ (x > 0)

```
ln y = ln(xˣ) = x ln x
(1/y) · y′ = ln x + x · (1/x) = ln x + 1
y′ = y(ln x + 1) = xˣ (ln x + 1)
```

## Derivatives of Inverse Trigonometric Functions (Optional Reference)

| Function     | Derivative                         |
|--------------|------------------------------------|
| arcsin x     | 1 / √(1 − x²)                      |
| arccos x     | −1 / √(1 − x²)                     |
| arctan x     | 1 / (1 + x²)                       |

\newpage

# Introduction to Analytical Geometry

## Introduction

**Analytical (coordinate) geometry** studies geometric figures using algebra and the coordinate plane. Points, distances, lines, circles, and other curves are described by equations.

## Distance and Midpoint

Distance between P(x₁, y₁) and Q(x₂, y₂):

```
d = √[(x₂ − x₁)² + (y₂ − y₁)²]
```

Midpoint of PQ:

```
M = ( (x₁ + x₂)/2 , (y₁ + y₂)/2 )
```

**Example:** Distance and midpoint of A(1, −2) and B(4, 2)

```
d = √[(4−1)² + (2−(−2))²] = √(9 + 16) = 5
M = ((1+4)/2, (−2+2)/2) = (2.5, 0)
```

## Slope of a Line

```
m = (y₂ − y₁) / (x₂ − x₁)   (x₂ ≠ x₁)
```

| Situation              | Slope        |
|------------------------|--------------|
| Horizontal line        | m = 0        |
| Vertical line          | undefined    |
| Parallel lines         | m₁ = m₂      |
| Perpendicular lines    | m₁ · m₂ = −1 |

## Equations of a Line

| Form              | Equation                         | Use                              |
|-------------------|----------------------------------|----------------------------------|
| Slope-intercept   | y = mx + c                       | Known slope and y-intercept      |
| Point-slope       | y − y₁ = m(x − x₁)               | Known point and slope            |
| Two-point         | Use point-slope with computed m  | Two known points                 |
| General           | ax + by + c = 0                  | Standard form                    |

**Example 1:** Line through (2, −1) with slope 3

```
y − (−1) = 3(x − 2)
y + 1 = 3x − 6
y = 3x − 7
```

**Example 2:** Line through (1, 4) and (3, −2)

```
m = (−2 − 4)/(3 − 1) = −6/2 = −3
y − 4 = −3(x − 1)
y = −3x + 7
```

## Circles

Standard form (center (h, k), radius r):

```
(x − h)² + (y − k)² = r²
```

General form:

```
x² + y² + Dx + Ey + F = 0
```

**Example:** Center (3, −2), radius 5

```
(x − 3)² + (y + 2)² = 25
```

Expanding:

```
x² − 6x + 9 + y² + 4y + 4 = 25
x² + y² − 6x + 4y − 12 = 0
```

## Parabolas (Brief)

| Opening        | Standard form (vertex at origin) | Focus / directrix idea      |
|----------------|----------------------------------|-----------------------------|
| Up / down      | x² = 4ay                         | Vertical axis               |
| Left / right   | y² = 4ax                         | Horizontal axis             |

Vertex form: y = a(x − h)² + k (opens up if a > 0, down if a < 0).

## Angle Between Two Lines

If lines have slopes m₁ and m₂:

```
tan θ = |(m₂ − m₁) / (1 + m₁ m₂)|
```

(Provided 1 + m₁ m₂ ≠ 0; if 1 + m₁ m₂ = 0, the lines are perpendicular.)

\newpage

# Linear Inequalities and Linear Programming

## Linear Inequalities in Two Variables

A **linear inequality** has the form:

```
ax + by < c,   ax + by ≤ c,   ax + by > c,   or   ax + by ≥ c
```

### Graphing Steps

1. Graph the boundary line ax + by = c (solid for ≤ or ≥, dashed for < or >)
2. Pick a test point not on the line (often (0, 0) if possible)
3. Shade the half-plane where the inequality is true

**Example 1:** Graph 2x + y ≤ 4

```
Boundary: y = −2x + 4 (solid line)
Test (0, 0): 0 ≤ 4 true → shade the side containing the origin
```

**Example 2:** System of inequalities

```
x ≥ 0
y ≥ 0
x + y ≤ 6
2x + y ≤ 8
```

The solution is the **feasible region**: the polygon in the first quadrant bounded by these lines.

### Corner Points

For a polygonal feasible region, find vertices by solving pairs of boundary equations.

```
Intersection of x + y = 6 and 2x + y = 8:
  Subtract: x = 2 → y = 4
  Corner: (2, 4)

Other corners (with axes): (0, 0), (0, 6), (4, 0)
```

## Linear Programming

**Linear programming (LP)** optimizes a linear **objective function** subject to linear inequality constraints.

### Standard Problem Form

```
Maximize (or minimize)  Z = ax + by
Subject to:  linear inequalities (constraints)
             x ≥ 0, y ≥ 0  (often)
```

### Graphical Method (Two Variables)

1. Graph the feasible region
2. Find all corner (vertex) points
3. Evaluate Z at each corner
4. The maximum/minimum of a linear objective over a closed bounded polygonal region occurs at a corner

**Example:** Maximize Z = 3x + 2y subject to:

```
x + y ≤ 6
2x + y ≤ 8
x ≥ 0, y ≥ 0
```

Corners: (0, 0), (0, 6), (2, 4), (4, 0)

```
Z(0, 0) = 0
Z(0, 6) = 12
Z(2, 4) = 6 + 8 = 14
Z(4, 0) = 12

Maximum: Z = 14 at (2, 4)
```

**Example: Minimize** C = 4x + 5y subject to:

```
x + 2y ≥ 10
3x + y ≥ 9
x ≥ 0, y ≥ 0
```

Find corners of the feasible region (unbounded, but minimum still at a vertex for this type of problem when it exists), evaluate C, and select the smallest value.

\newpage

# Antiderivatives

## Introduction

An **antiderivative** of f is a function F such that F′(x) = f(x). Antiderivatives reverse differentiation and are the foundation of indefinite integrals.

### Definition

F is an antiderivative of f on an interval if:

```
F′(x) = f(x)  for all x in the interval
```

If F is one antiderivative, then **all** antiderivatives are:

```
F(x) + C
```

where C is an arbitrary constant (the **constant of integration**).

### Indefinite Integral Notation

```
∫ f(x) dx = F(x) + C
```

means F′(x) = f(x).

## Basic Antiderivative Formulas

| Function f(x)     | Antiderivative F(x) + C        |
|-------------------|--------------------------------|
| 0                 | C                              |
| k (constant)      | kx + C                         |
| xⁿ (n ≠ −1)       | xⁿ⁺¹/(n+1) + C                 |
| 1/x               | ln\|x\| + C                    |
| eˣ                | eˣ + C                         |
| aˣ                | aˣ / ln a + C                  |
| sin x             | −cos x + C                     |
| cos x             | sin x + C                      |
| sec² x            | tan x + C                      |

**Example 1:** ∫ (6x² − 4x + 5) dx

```
= 6·(x³/3) − 4·(x²/2) + 5x + C
= 2x³ − 2x² + 5x + C
```

**Example 2:** ∫ (√x + 1/x²) dx

```
= ∫ (x^(1/2) + x^(−2)) dx
= (2/3)x^(3/2) − 1/x + C
```

**Example 3:** ∫ e^(2x) dx

```
= (1/2) e^(2x) + C
```

(Check: derivative of (1/2)e^(2x) is e^(2x).)

## Particular Antiderivatives (Initial Conditions)

Given F′(x) = f(x) and a point F(x₀) = y₀, solve for C.

**Example:** Find f if f′(x) = 3x² − 2 and f(1) = 4

```
f(x) = x³ − 2x + C
f(1) = 1 − 2 + C = 4
C = 5
f(x) = x³ − 2x + 5
```

## Connection to Motion

If a(t) is acceleration, then:

```
v(t) = ∫ a(t) dt    (velocity)
s(t) = ∫ v(t) dt    (position)
```

Use initial conditions to fix constants.

**Example:** a(t) = 6t, v(0) = 2, s(0) = 0

```
v(t) = 3t² + C₁ → v(0) = 2 → C₁ = 2 → v(t) = 3t² + 2
s(t) = t³ + 2t + C₂ → s(0) = 0 → C₂ = 0 → s(t) = t³ + 2t
```

## Linearity of Antiderivatives

```
∫ [c·f(x) + g(x)] dx = c ∫ f(x) dx + ∫ g(x) dx
```

\newpage

# Quick Reference Summary

| Topic                         | Key Idea                                              | Example                                      |
|-------------------------------|-------------------------------------------------------|----------------------------------------------|
| Derivative (definition)       | lim (h→0) [f(a+h)−f(a)]/h = slope of tangent          | f(x)=x² → f′(2)=4                            |
| Differentiation rules         | Power, product, quotient, sum                         | (uv)′ = u′v + uv′                            |
| Rate of change                | f′ = instantaneous rate; velocity = s′                | s=t³−6t²+9t → v(2)=−3                        |
| Chain rule                    | (f∘g)′ = f′(g)·g′                                     | d/dx (3x²+1)⁵ = 30x(3x²+1)⁴                  |
| Inverse / log derivatives     | (f⁻¹)′(b)=1/f′(a); (ln u)′ = u′/u                     | (ln(5x²+3))′ = 10x/(5x²+3)                   |
| Analytical geometry           | Distance, slope, lines, circles via coordinates       | (x−3)²+(y+2)²=25                             |
| Linear inequalities / LP      | Feasible region; optimum at a corner                  | Max 3x+2y on corners → (2,4), Z=14           |
| Antiderivatives               | F′=f; ∫f = F+C; use initial conditions for C          | ∫6x² dx = 2x³+C                              |

---

*End of Lecture Notes*
