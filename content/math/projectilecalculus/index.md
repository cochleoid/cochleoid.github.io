---
title: "Deriving Projectile Formulas with Calculus"
date: 2025-06-21
draft: false
description: "A video tutorial on how to cleanly derive projectile motion with only conceptual understanding and differential calculus."
tags: ["physics", "calculus", "projectile motion", "derivation"]
---

{{< katex >}}

# Deriving Projectile Formulas with Calculus

In this video we are going to derive some projectile motion formulas using differential calculus.  

If we want to find things like maximum height or the time to reach that height, we need functions to model the position.  

---

## Step 1: Position Function Setup

Projectiles follow a parabola, which means we are looking to solve coefficients of a quadratic:

\[
f(t) = at^2 + bt
\]

If there is an initial height, we could add it later, but for simplicity we will not include it here.  

---

## Step 2: Observations

1. The acceleration due to gravity is constant. This corresponds to the **second derivative** of the position function.
   \[
   f''(t) = -g
   \]

2. The derivative of the position function is velocity. At \( t = 0 \), the velocity is the initial vertical velocity:
   \[
   f'(0) = v \sin \theta
   \]

---

## Step 3: Differentiate

Differentiate the position function:

\[
f(t) = at^2 + bt
\]

\[
f'(t) = 2at + b
\]

\[
f''(t) = 2a
\]

Since the second derivative must equal \(-g\):

\[
2a = -g \quad \Rightarrow \quad a = -\tfrac{1}{2}g
\]

Now use the initial condition for velocity:

\[
f'(0) = b = v \sin \theta
\]

So the position function becomes:

\[
f(t) = -\tfrac{1}{2} g t^2 + (v \sin \theta) t
\]

---

## Step 4: Maximum Height

The vertex of a parabola occurs at:

\[
t = -\frac{b}{2a}
\]

Here:

\[
t = \frac{v \sin \theta}{g}
\]

This is the time to reach maximum height.  

Now plug it back into \( f(t) \):

\[
f\left(\frac{v \sin \theta}{g}\right) = -\tfrac{1}{2} g \left(\frac{v \sin \theta}{g}\right)^2 + (v \sin \theta)\left(\frac{v \sin \theta}{g}\right)
\]

Simplify:

\[
= -\frac{v^2 \sin^2 \theta}{2g} + \frac{v^2 \sin^2 \theta}{g}
\]

\[
= \frac{v^2 \sin^2 \theta}{2g}
\]

So the maximum height is:

\[
\boxed{\tfrac{v^2 \sin^2 \theta}{2g}}
\]

---

## Step 5: Total Time of Flight

We can use the root property of quadratics. Since the projectile lands back at height zero, the other root of \( f(t) \) is the total time of flight.  

The sum of the roots is:

\[
t_1 + t_2 = -\frac{b}{a}
\]

We already know one root is \( 0 \). So the other root is:

\[
t = -\frac{b}{a} = -\frac{v \sin \theta}{-\tfrac{1}{2}g} = \frac{2v \sin \theta}{g}
\]

Thus the total time of flight is:

\[
\boxed{\tfrac{2v \sin \theta}{g}}
\]

---

## Review

We derived two key projectile motion results using calculus:

- Maximum height:
\[
\frac{v^2 \sin^2 \theta}{2g}
\]

- Total time of flight:
\[
\frac{2v \sin \theta}{g}
\]

Prefer video? Watch the full explanation here:  
{{< youtube c6EPO5dYJkY >}}
