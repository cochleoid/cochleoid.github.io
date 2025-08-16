---
title: "A Triangle's Orthocenter Given Its Coordinates"
date: 2023-04-19
draft: false
description: "Deriving the orthocenter of a triangle from vertex coordinates."
tags: ["mathematics", "geometry", "analytic-geometry"]
---

{{< katex >}}

# A Triangle's Orthocenter Given Its Coordinates
**Adrian Jose Hernandez Vega**

## Introduction

The orthocenter of a triangle is defined as the point of intersection of all of the triangle's altitudes.  

An altitude of a triangle is a perpendicular segment connecting a vertex to the opposite side.  

Suppose triangle \(\triangle ABC\)'s vertices have arbitrary coordinates \(A(x_1,y_1)\), \(B(x_2,y_2)\), and \(C(x_3,y_3)\). This triangle lies on the Cartesian coordinate plane.

## Orthocenter Algebra

The altitudes of segments \(\overline{AB}\), \(\overline{BC}\), and \(\overline{CA}\) can be represented in slope-intercept form. If any two vertices form a perfectly vertical line, exclude such a segment, as it will lead to undefined results.

### Lemma

Given slope \(m\) and point \((P_1,P_2)\), the line perpendicular to \(m\) that passes through \((P_1,P_2)\) is represented by:

\[
y = \frac{P_1 - x}{m} + P_2
\]

**Proof:** The outlined equation is a rephrasing of the point-slope formula, with the slope term inverted and negated to ensure perpendicularity.

The altitude perpendicular to \(\overline{AB}\) passes through \((x_3,y_3)\), the altitude perpendicular to \(\overline{BC}\) passes through \((x_1,y_1)\), and the altitude perpendicular to \(\overline{CA}\) passes through \((x_2,y_2)\). Using the previous lemma, these altitudes can be represented as:

\[
\begin{aligned}
\overline{AB}_\perp \cap (x_3,y_3) &\implies y = \frac{(x_3-x)(x_2-x_1)}{y_2 - y_1} + y_3 \\
\overline{BC}_\perp \cap (x_1,y_1) &\implies y = \frac{(x_1-x)(x_3-x_2)}{y_3 - y_2} + y_1 \\
\overline{CA}_\perp \cap (x_2,y_2) &\implies y = \frac{(x_2-x)(x_3-x_1)}{y_3 - y_1} + y_2
\end{aligned}
\]

### Theorem

For triangle \(\triangle ABC\) with coordinates \(A(x_1,y_1)\), \(B(x_2,y_2)\), and \(C(x_3,y_3)\), the orthocenter can be found by solving any two non-vertical equations in the overdetermined system:

\[
\left\{
\begin{aligned}
y &= \frac{(x_3-x)(x_2-x_1)}{y_2 - y_1} + y_3 \\
y &= \frac{(x_1-x)(x_3-x_2)}{y_3 - y_2} + y_1 \\
y &= \frac{(x_2-x)(x_3-x_1)}{y_3 - y_1} + y_2
\end{aligned}
\right.
\]
