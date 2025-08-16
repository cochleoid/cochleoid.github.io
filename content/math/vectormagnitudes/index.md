---
title: "Vectors, Magnitudes and Dot Products"
date: 2025-07-11
draft: false
description: "A tutorial covering vector magnitudes, dot products, and rotations."
tags: ["math", "vectors", "algebra"]
---

{{< katex >}}

# Vectors

## Magnitude

The **magnitude** of a vector is denoted by double bars, like \( ||\vec{a}|| \). It represents the length of the vector, which can be found using the **Pythagorean theorem**.

For example, the magnitude of the vector \( [3, 4] \) is \( \sqrt{3^2 + 4^2} = 5 \).

**Exercise 1:** What is the magnitude of vector \( [5, 12] \)?  
**Exercise 2:** What is the product of \( ||\vec{a}|| \) and \( ||\vec{b}|| \) if \( a = [1, 2] \) and \( b = [2, 3] \)?

## The Dot Product

The **dot product** of two vectors is the sum of the products of corresponding components. For example, for vectors \( [1, 2, 3] \) and \( [4, 5, 6] \), the dot product is  
\( (1 \cdot 4) + (2 \cdot 5) + (3 \cdot 6) = 32 \),  
which can be written as \( [1, 2, 3] \cdot [4, 5, 6] = 32 \).

- If the dot product is **zero**, the vectors are **perpendicular**.  
- If it's **positive**, the angle between them is **acute**.  
- If it's **negative**, the angle is **obtuse**.

### Exercises

**Exercise 3:** What is the value of \( [1, 2] \cdot [3, 4] \)?  
**Exercise 4:** Do the vectors \( [7, 8] \) and \( [9, 10] \) form an acute, right, or obtuse angle?

## The Dot Product Equation

The dot product formula can also be expressed as:  
\[ D = M \cos(\theta) \]  
where:
- \( D \) is the dot product,
- \( M \) is the product of the magnitudes, and  
- \( \theta \) is the angle between the vectors.

### Example: Finding the Angle Between Two Vectors

Find the angle between \( [1, 2] \) and \( [3, 4] \):

\[
\begin{aligned}
D &= M \cos(\theta) \\
(1 \cdot 3) + (2 \cdot 4) &= ||[1,2]|| \cdot ||[3,4]|| \cdot \cos(\theta) \\
11 &= 5\sqrt{5} \cdot \cos(\theta) \\
\frac{11}{5\sqrt{5}} &= \cos(\theta) \\
\arccos\left(\frac{11}{5\sqrt{5}}\right) &= \theta \\
\theta &\approx 79.6^\circ
\end{aligned}
\]

### Example: Solving for a Missing Component

Let vectors \( [1, A] \) and \( [3, 4] \) have a dot product of 10 and form a \( 45^\circ \) angle. What is the value of \( A \)?

\[
\begin{aligned}
D &= M \cos(\theta) \\
10 &= 5 \cdot \sqrt{1^2 + A^2} \cdot \cos(45^\circ) \\
10 &= 5 \cdot \sqrt{1 + A^2} \cdot \frac{\sqrt{2}}{2} \\
2 &= \sqrt{1 + A^2} \cdot \frac{\sqrt{2}}{2} \\
4 &= \sqrt{1 + A^2} \cdot \sqrt{2} \\
\frac{4}{\sqrt{2}} &= \sqrt{1 + A^2} \\
8 &= 1 + A^2 \\
A^2 &= 7 \\
A &= \pm \sqrt{7}
\end{aligned}
\]

### Example: Vector Rotation

Let \( \vec{p} = [1, 2] \) and suppose it's rotated counterclockwise by \( 56^\circ \), resulting in a new vector \( \vec{r} = [A, B] \) such that the dot product is 30. What is the new vector?

\[
\begin{aligned}
D &= M \cos(\theta) \\
30 &= \sqrt{5} \cdot \sqrt{A^2 + B^2} \cdot \cos(56^\circ) \\
30 &= \sqrt{5A^2 + 5B^2} \cdot \cos(56^\circ) \\
\frac{30}{\cos(56^\circ)} &= \sqrt{5A^2 + 5B^2} \\
\frac{900}{\cos^2(56^\circ)} &= 5A^2 + 5B^2
\end{aligned}
\]

Also, we know that:

\[
A + 2B = 30
\]

This creates the system:

\[
\left\{
\begin{aligned}
5A^2 + 5B^2 &= \frac{900}{\cos^2(56^\circ)} \\
A + 2B &= 30
\end{aligned}
\right.
\]

Solving this system yields the approximate solutions:
- \( [-11.79, 20.90] \)
- \( [23.80, 3.10] \)

Only the first is a **counterclockwise** rotation, so the final answer is approximately  
**\( \vec{r} \approx [-11.79, 20.90] \)**

## Exercises

**Exercise 5:** What is the angle between the vectors \( [7, 8] \) and \( [2, 9] \)?  
**Exercise 6:** What is the angle between the vectors \( [4, 2] \) and \( [8, 4] \)? Why does this operation lead to an error?  
**Exercise 7:** What is the angle between the vectors \( [4, 2] \) and \( [2x, x] \)?  
**Exercise 8:** Let \( \vec{a} = [3, 5] \), and let \( \vec{b} \) be the result when \( \vec{a} \) is rotated 30 degrees. What is the **sum** of the components of \( \vec{b} \)? Round to the nearest tenth.  
**Exercise 9:** What is the angle between the lines \( 5x + 4y = 9 \) and \( 8x + 3y = 5 \)?

## Credits

Explanations and problems by Adrian Hernandez Vega.
