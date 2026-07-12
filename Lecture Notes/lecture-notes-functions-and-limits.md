
# Functions, Graphs, and Limits


# Functions and Their Graphs

## Introduction

A **function** is a rule that assigns to each input from a set (the **domain**) exactly one output in another set (the **codomain**). When we write f(x), we mean the output of the function f corresponding to the input x.

The **graph** of a function f is the set of all points (x, f(x)) plotted on the coordinate plane. Graphs help us visualize how a function behaves — where it increases, decreases, crosses the axes, and reaches maximum or minimum values.

### Key Graph-Related Terms

| Term            | Meaning                                              |
|-----------------|------------------------------------------------------|
| x-intercept     | Point where the graph crosses the x-axis (y = 0)     |
| y-intercept     | Point where the graph crosses the y-axis (x = 0)     |
| Increasing      | Graph rises as x increases                           |
| Decreasing      | Graph falls as x increases                           |
| Even function   | Symmetric about the y-axis: f(−x) = f(x)             |
| Odd function    | Symmetric about the origin: f(−x) = −f(x)            |

## Common Types of Functions and Their Graphs

### 1. Linear Function

```
f(x) = mx + c
```

- Graph: a straight line
- m = slope, c = y-intercept

**Example:** f(x) = 2x − 3

- Slope = 2 (rises 2 units for every 1 unit right)
- y-intercept = (0, −3)
- x-intercept: set f(x) = 0 → x = 3/2

### 2. Quadratic Function

```
f(x) = ax² + bx + c,   a ≠ 0
```

- Graph: a parabola
- Opens upward if a > 0, downward if a < 0
- Vertex gives the turning point

**Example:** f(x) = x² − 4x + 3

```
f(x) = (x − 1)(x − 3)
x-intercepts: x = 1 and x = 3
y-intercept: (0, 3)
Vertex: (2, −1)
```

### 3. Cubic Function

```
f(x) = ax³ + bx² + cx + d
```

- Graph: S-shaped curve (for simple cubics)
- May have up to 2 turning points

**Example:** f(x) = x³ − 3x

- Passes through origin
- Turning points at x = −1 and x = 1

### 4. Absolute Value Function

```
f(x) = |x|
```

- Graph: V-shaped, vertex at origin
- Symmetric about the y-axis

**Example:** f(x) = |x − 2|

- Vertex at (2, 0)
- V opens upward

### 5. Square Root Function

```
f(x) = √x
```

- Graph: starts at (0, 0), curves upward
- Domain: x ≥ 0

**Example:** f(x) = √(x + 1)

- Domain: x ≥ −1
- Starts at (−1, 0)

### 6. Rational Function

```
f(x) = p(x) / q(x)
```

- Graph may have vertical asymptotes (where denominator = 0) and horizontal asymptotes

**Example:** f(x) = 1/x

- Vertical asymptote: x = 0
- Horizontal asymptote: y = 0
- Graph has two branches in quadrants I and III

## Graph Transformations

Given a base function f(x), the following transformations apply:

| Transformation        | Effect on Graph                          |
|-----------------------|------------------------------------------|
| f(x) + k              | Shift up by k units                      |
| f(x) − k              | Shift down by k units                    |
| f(x + h)              | Shift left by h units                    |
| f(x − h)              | Shift right by h units                   |
| a·f(x), a > 1         | Vertical stretch by factor a             |
| a·f(x), 0 < a < 1     | Vertical compression                     |
| −f(x)                 | Reflection across the x-axis             |
| f(−x)                 | Reflection across the y-axis             |

**Example:** Starting from f(x) = x², describe g(x) = −2(x − 1)² + 3

1. Start with x² (standard parabola)
2. Shift right 1 unit: (x − 1)²
3. Stretch vertically by 2: 2(x − 1)²
4. Reflect across x-axis: −2(x − 1)²
5. Shift up 3 units: −2(x − 1)² + 3

Result: downward-opening parabola with vertex at (1, 3).

## Reading Information from Graphs

**Example:** The graph of f passes through (−2, 0), (0, 4), and (3, −1).

```
From the points:
  f(−2) = 0    → x-intercept at x = −2
  f(0) = 4     → y-intercept at (0, 4)
  f(3) = −1
```

If the graph rises from x = −2 to x = 0, then falls from x = 0 to x = 3, we can say:

- f is increasing on (−2, 0)
- f is decreasing on (0, 3)

\newpage

# Inverse Functions and Logarithms

## Introduction

An **inverse function** reverses the action of the original function. If f maps a to b, then f⁻¹ maps b back to a.

A function has an inverse **only if it is bijective** (one-to-one and onto). In practice, we often restrict the domain to make a function one-to-one so that an inverse exists.

### Definition

If f: A → B is a bijection, then the inverse function f⁻¹: B → A satisfies:

```
f⁻¹(f(x)) = x   for all x ∈ A
f(f⁻¹(y)) = y   for all y ∈ B
```

### Finding an Inverse — Step by Step

1. Replace f(x) with y
2. Swap x and y
3. Solve for y
4. Replace y with f⁻¹(x)

**Example 1:** Find the inverse of f(x) = 3x − 5

```
y = 3x − 5
Swap: x = 3y − 5
Solve: x + 5 = 3y  →  y = (x + 5)/3

f⁻¹(x) = (x + 5)/3
```

**Verification:**

```
f(f⁻¹(x)) = f((x+5)/3) = 3·(x+5)/3 − 5 = x + 5 − 5 = x ✓
```

**Example 2:** Find the inverse of f(x) = x², x ≥ 0

```
y = x²,  x ≥ 0
Swap: x = y²,  y ≥ 0
Solve: y = √x

f⁻¹(x) = √x,  x ≥ 0
```

Note: Without the restriction x ≥ 0, f(x) = x² would not be one-to-one and would have no inverse.

### Graph of an Inverse

The graph of f⁻¹ is the **reflection of the graph of f across the line y = x**.

**Example:** f(x) = 2x + 1 and f⁻¹(x) = (x − 1)/2

- f passes through (0, 1) and (2, 5)
- f⁻¹ passes through (1, 0) and (5, 2) — the swapped coordinates

## Exponential Functions

The **exponential function** with base a (a > 0, a ≠ 1) is:

```
f(x) = aˣ
```

| Property         | a > 1 (Growth)       | 0 < a < 1 (Decay)    |
|------------------|----------------------|----------------------|
| Domain           | ℝ                    | ℝ                    |
| Range            | (0, ∞)               | (0, ∞)               |
| y-intercept      | (0, 1)               | (0, 1)               |
| Horizontal asymptote | y = 0            | y = 0                |
| Behavior         | Increases rapidly    | Decreases toward 0   |

**Example:** f(x) = 2ˣ

```
f(0) = 1
f(1) = 2
f(2) = 4
f(−1) = 1/2
```

**Example:** f(x) = (1/2)ˣ = 2^(−x)

- Decay function, mirror of 2ˣ across the y-axis

### The Natural Exponential

```
f(x) = eˣ,   where e ≈ 2.71828
```

eˣ is widely used in calculus, growth models, and compound interest.

## Logarithmic Functions

The **logarithm** is the inverse of the exponential function.

### Definition

For a > 0, a ≠ 1, and x > 0:

```
y = logₐ(x)   if and only if   aʸ = x
```

Read as: "log base a of x equals y" means "a raised to the power y equals x."

**Example 1:**

```
log₂(8) = 3    because 2³ = 8
log₁₀(100) = 2 because 10² = 100
log₅(1) = 0    because 5⁰ = 1
```

**Example 2:** Solve 3ˣ = 81

```
3ˣ = 81 = 3⁴
x = 4

Using logarithms:
x = log₃(81) = 4
```

### Common and Natural Logarithms

| Name            | Base | Notation   |
|-----------------|------|------------|
| Common log      | 10   | log x or log₁₀(x) |
| Natural log     | e    | ln x or logₑ(x)  |

**Example:**

```
ln(e³) = 3
log(1000) = 3
ln(1) = 0
log(1) = 0
```

### Properties of Logarithms

For a > 0, a ≠ 1, M > 0, N > 0, and k any real number:

| Property              | Formula                        |
|-----------------------|--------------------------------|
| Product rule          | logₐ(MN) = logₐ M + logₐ N     |
| Quotient rule         | logₐ(M/N) = logₐ M − logₐ N   |
| Power rule            | logₐ(Mᵏ) = k · logₐ M          |
| Change of base        | logₐ M = (log M) / (log a)     |
| Inverse identities    | a^(logₐ x) = x,  logₐ(aˣ) = x |

**Example 1: Expand log(4x³/√y)**

```
log(4x³/√y) = log 4 + log x³ − log y^(1/2)
            = log 4 + 3 log x − (1/2) log y
```

**Example 2: Solve 2ˣ = 10**

```
x = log₂(10) = ln(10)/ln(2) ≈ 3.322
```

**Example 3: Solve ln(x − 1) = 2**

```
x − 1 = e²
x = 1 + e² ≈ 8.389
```

### Graph of Logarithmic Functions

The graph of y = logₐ(x) is the reflection of y = aˣ across the line y = x.

| Feature              | y = aˣ          | y = logₐ(x)     |
|----------------------|-----------------|-----------------|
| Domain               | ℝ               | (0, ∞)          |
| Range                | (0, ∞)          | ℝ               |
| Passes through       | (0, 1)          | (1, 0)          |
| Vertical asymptote   | None            | x = 0           |
| Horizontal asymptote | y = 0           | None            |

\newpage

# Composition of Functions

## Introduction

**Function composition** applies one function to the result of another. If f and g are functions, the composition f ∘ g (read "f composed with g") means: first apply g, then apply f to the output.

### Definition

```
(f ∘ g)(x) = f(g(x))
```

Similarly:

```
(g ∘ f)(x) = g(f(x))
```

**Important:** In general, f ∘ g ≠ g ∘ f. The order matters.

### Domain of a Composition

The domain of (f ∘ g)(x) consists of all x in the domain of g such that g(x) is in the domain of f.

## Evaluating Compositions

**Example 1:** Given f(x) = 2x + 1 and g(x) = x², find (f ∘ g)(3) and (g ∘ f)(3)

```
(f ∘ g)(3) = f(g(3)) = f(9) = 2(9) + 1 = 19

(g ∘ f)(3) = g(f(3)) = g(7) = 7² = 49
```

**Example 2:** Given f(x) = √x and g(x) = x − 4, find (f ∘ g)(x) and its domain

```
(f ∘ g)(x) = f(g(x)) = f(x − 4) = √(x − 4)
```

Domain: we need x − 4 ≥ 0, so x ≥ 4.

Domain of f ∘ g = [4, ∞).

## Finding Composition Formulas

**Example 3:** f(x) = 3x − 2, g(x) = x² + 1. Find (f ∘ g)(x) and (g ∘ f)(x)

```
(f ∘ g)(x) = f(g(x)) = f(x² + 1) = 3(x² + 1) − 2 = 3x² + 1

(g ∘ f)(x) = g(f(x)) = g(3x − 2) = (3x − 2)² + 1 = 9x² − 12x + 5
```

Notice: (f ∘ g)(x) = 3x² + 1, but (g ∘ f)(x) = 9x² − 12x + 5. They are different.

**Example 4:** f(x) = 1/x, g(x) = x + 3. Find (f ∘ g)(x)

```
(f ∘ g)(x) = f(x + 3) = 1/(x + 3)
```

Domain: x + 3 ≠ 0, so x ≠ −3.

## Composition with Multiple Functions

**Example 5:** f(x) = √x, g(x) = x² + 1, h(x) = 2x − 5. Find (f ∘ g ∘ h)(x)

Work from the inside out:

```
h(x) = 2x − 5
g(h(x)) = (2x − 5)² + 1 = 4x² − 20x + 26
f(g(h(x))) = √(4x² − 20x + 26)
```

So (f ∘ g ∘ h)(x) = √(4x² − 20x + 26).

Domain: 4x² − 20x + 26 ≥ 0. Since 4x² − 20x + 26 = 4(x − 2.5)² + 1.5 > 0 for all real x, the domain is ℝ.

## Decomposing a Function

Sometimes we express a complicated function as a composition of simpler ones.

**Example 6:** Write h(x) = (3x − 1)⁵ as a composition

```
Let f(x) = x⁵       (outer function — the power)
Let g(x) = 3x − 1   (inner function)

h(x) = (f ∘ g)(x) = f(g(x)) = f(3x − 1) = (3x − 1)⁵
```

**Example 7:** Write h(x) = e^(2x+1) as a composition

```
f(x) = eˣ         (outer — exponential)
g(x) = 2x + 1     (inner — linear)

h(x) = (f ∘ g)(x) = e^(2x+1)
```

## Composition and Inverse Functions

A key property linking composition and inverses:

```
(f ∘ f⁻¹)(x) = x    for all x in the domain of f⁻¹
(f⁻¹ ∘ f)(x) = x    for all x in the domain of f
```

**Example:** f(x) = 2x + 3, f⁻¹(x) = (x − 3)/2

```
(f ∘ f⁻¹)(x) = f((x−3)/2) = 2·(x−3)/2 + 3 = x − 3 + 3 = x ✓
(f⁻¹ ∘ f)(x) = f⁻¹(2x+3) = ((2x+3)−3)/2 = 2x/2 = x ✓
```

## Real-World Application

**Example: Temperature conversion pipeline**

A sensor outputs a value s in a custom scale. To display Fahrenheit:

```
g(s) = 1.8s + 32        (convert to Fahrenheit)
f(T) = (T − 32) / 1.8   (convert Fahrenheit to Celsius)
```

If the sensor reads s = 20:

```
g(20) = 1.8(20) + 32 = 68°F
f(g(20)) = f(68) = (68 − 32)/1.8 = 20°C   (round-trip confirms inverse relationship)
```

\newpage

# Concept of Limits of a Function

## Introduction

The **limit** of a function describes the value that f(x) approaches as x gets closer and closer to some number a (without necessarily reaching a). Limits are the foundation of calculus — they allow us to define continuity, derivatives, and integrals.

### Intuitive Idea

As x approaches a, f(x) approaches L.

We write:

```
lim (x→a) f(x) = L
```

This means: we can make f(x) as close to L as we want by taking x sufficiently close to a (but not equal to a).

**Example (intuitive):** f(x) = x + 2

```
As x → 3:   f(x) → 5
lim (x→3) (x + 2) = 5
```

Even though we never need to plug in x = 3, the function value at x = 3 is also 5.

## One-Sided Limits

Sometimes the behavior of f(x) differs depending on whether x approaches a from the left or the right.

| Notation              | Meaning                              |
|-----------------------|--------------------------------------|
| lim (x→a⁻) f(x)       | Limit as x approaches a from the left  |
| lim (x→a⁺) f(x)       | Limit as x approaches a from the right |

A two-sided limit exists if and only if both one-sided limits exist and are equal:

```
lim (x→a) f(x) = L   ⟺   lim (x→a⁻) f(x) = lim (x→a⁺) f(x) = L
```

**Example 1:** f(x) = |x|/x (sign function)

```
For x > 0:  f(x) = x/x = 1
For x < 0:  f(x) = −x/x = −1

lim (x→0⁺) f(x) = 1
lim (x→0⁻) f(x) = −1

Since left and right limits differ, lim (x→0) f(x) does NOT exist.
```

**Example 2:** f(x) = √(x − 1)

```
Domain: x ≥ 1
lim (x→1⁺) √(x − 1) = 0
lim (x→1⁻) does not exist (function undefined for x < 1)

lim (x→1) √(x − 1) = 0   (right-hand limit only)
```

## Limits by Direct Substitution

If f is a polynomial or a rational function with a nonzero denominator at x = a, we can substitute directly:

**Example 1:**

```
lim (x→2) (3x² − x + 4) = 3(4) − 2 + 4 = 14
```

**Example 2:**

```
lim (x→−1) (x² − 4)/(x + 1) = (1 − 4)/(−1 + 1) = −3/0
```

Direct substitution gives 0 in the denominator — the limit requires further analysis.

## Limits of Rational Functions (0/0 Form)

When direct substitution gives 0/0, factor and simplify.

**Example 1:**

```
lim (x→2) (x² − 4)/(x − 2)

= lim (x→2) (x − 2)(x + 2)/(x − 2)
= lim (x→2) (x + 2)
= 4
```

**Example 2:**

```
lim (x→3) (x² − 9)/(x − 3)

= lim (x→3) (x − 3)(x + 3)/(x − 3)
= lim (x→3) (x + 3)
= 6
```

## Limits at Infinity

We also study what happens to f(x) as x grows without bound.

```
lim (x→∞) f(x) = L    means f(x) approaches L as x → +∞
lim (x→−∞) f(x) = L   means f(x) approaches L as x → −∞
```

**Example 1:**

```
lim (x→∞) (3x² + 1)/(x² − 2x)

Divide numerator and denominator by x²:
= lim (x→∞) (3 + 1/x²)/(1 − 2/x)
= 3/1 = 3
```

**Example 2:**

```
lim (x→∞) (2x + 1)/(x² + 3)

Divide by x²:
= lim (x→∞) (2/x + 1/x²)/(1 + 3/x²)
= 0/1 = 0
```

**Example 3:**

```
lim (x→∞) (5x³ − 2x)/(2x³ + x²)

Leading terms dominate:
= lim (x→∞) 5x³/2x³ = 5/2
```

### Rules for Limits at Infinity

For polynomials of degree n:

- If degree(numerator) < degree(denominator): limit = 0
- If degree(numerator) = degree(denominator): limit = ratio of leading coefficients
- If degree(numerator) > degree(denominator): limit = ±∞

## Important Standard Limits

| Limit                          | Value  |
|--------------------------------|--------|
| lim (x→0) sin(x)/x             | 1      |
| lim (x→0) (1 − cos x)/x        | 0      |
| lim (x→∞) (1 + 1/x)ˣ           | e      |
| lim (x→0) (eˣ − 1)/x           | 1      |
| lim (x→0) ln(1 + x)/x          | 1      |

**Example: Using lim (x→0) sin(x)/x = 1**

```
lim (x→0) sin(3x)/x

= lim (x→0) 3·sin(3x)/(3x)
= 3 · 1 = 3
```

## Properties of Limits

If lim (x→a) f(x) = L and lim (x→a) g(x) = M, then:

| Rule                | Formula                                      |
|---------------------|----------------------------------------------|
| Sum                 | lim [f(x) + g(x)] = L + M                    |
| Difference          | lim [f(x) − g(x)] = L − M                    |
| Product             | lim [f(x)·g(x)] = L·M                        |
| Quotient            | lim [f(x)/g(x)] = L/M,  M ≠ 0                |
| Constant multiple   | lim [c·f(x)] = c·L                           |
| Power               | lim [f(x)]ⁿ = Lⁿ                               |
| Root                | lim ⁿ√f(x) = ⁿ√L                              |

**Example:**

```
lim (x→1) (2x² + 3x − 1)

= 2·lim(x²) + 3·lim(x) − lim(1)
= 2(1) + 3(1) − 1 = 4
```

## Limits and Continuity

A function f is **continuous at x = a** if:

```
lim (x→a) f(x) = f(a)
```

All three conditions must hold:

1. f(a) is defined
2. lim (x→a) f(x) exists
3. The limit equals the function value

**Example 1: Continuous**

```
f(x) = x² at x = 2
f(2) = 4
lim (x→2) x² = 4
f is continuous at x = 2 ✓
```

**Example 2: Discontinuous (removable)**

```
f(x) = (x² − 1)/(x − 1) at x = 1

f(1) is undefined (0/0)
But lim (x→1) (x² − 1)/(x − 1) = lim (x→1)(x + 1) = 2

The limit exists but f(1) is undefined → removable discontinuity.
We can "fix" it by defining f(1) = 2.
```

**Example 3: Discontinuous (jump)**

```
f(x) = { x + 1,  x < 2
       { 5,       x ≥ 2

lim (x→2⁻) f(x) = 3
lim (x→2⁺) f(x) = 5

Left and right limits differ → jump discontinuity at x = 2.
```

## The Squeeze (Sandwich) Theorem

If g(x) ≤ f(x) ≤ h(x) near x = a, and:

```
lim (x→a) g(x) = lim (x→a) h(x) = L
```

then:

```
lim (x→a) f(x) = L
```

**Example: Prove lim (x→0) x²·sin(1/x) = 0**

```
−1 ≤ sin(1/x) ≤ 1
−x² ≤ x²·sin(1/x) ≤ x²

lim (x→0) (−x²) = 0
lim (x→0) x² = 0

By the Squeeze Theorem: lim (x→0) x²·sin(1/x) = 0
```

\newpage

# Quick Reference Summary

| Topic                    | Key Idea                                          | Example                              |
|--------------------------|---------------------------------------------------|--------------------------------------|
| Functions & Graphs       | Visual representation of f as points (x, f(x))  | f(x) = x² is a parabola              |
| Graph Transformations    | Shift, stretch, reflect base graphs               | f(x−2)+3 shifts right 2, up 3       |
| Inverse Functions        | Reverses f; reflects graph across y = x           | f(x)=2x−1 → f⁻¹(x)=(x+1)/2          |
| Logarithms               | Inverse of aˣ; logₐ(x) = y ⟺ aʸ = x              | log₂(8) = 3                          |
| Composition              | (f ∘ g)(x) = f(g(x)); order matters               | f(x)=2x, g(x)=x² → f(g(3))=18       |
| Limits                   | Value f(x) approaches as x → a                  | lim (x→2) (x²−4)/(x−2) = 4          |
| Continuity               | lim (x→a) f(x) = f(a)                             | x² is continuous everywhere          |

---

*End of Lecture Notes*
