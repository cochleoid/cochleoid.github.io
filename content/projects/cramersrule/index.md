---
title: "Cramer's Rule in R2"
date: 2023-03-23
draft: false
description: "Derived solutions to 2x2 linear systems using elimination and determinants (Cramer's Rule)."
tags: ["mathematics", "linear-algebra", "analytic-geometry", "nostalgia"]
---

{{< katex >}}

# Cramer's Rule in R2 Through Elimination
**Adrian Jose Hernandez Vega**

## Elimination

Recall the *elimination* method of solving a system of equations: negating either \(x\) or \(y\) by manipulating the equations and then solving. With enough algebra, any system can be solved via elimination.

### Lemma

Suppose there is a system of two equations:

\[
\begin{cases} 
a_1 x + b_1 y = c_1 \\
a_2 x + b_2 y = c_2
\end{cases}
\]

To isolate a variable, multiply the first equation by \(a_2\) or \(b_2\), the second by \(a_1\) or \(b_1\), and then subtract the equations:

\[
\begin{cases} 
a_2(a_1 x + b_1 y = c_1) \\
a_1(a_2 x + b_2 y = c_2)
\end{cases}
\]

**Proof:** Appending \(a_2\) to the first equation and \(a_1\) to the second aligns the \(x\)-terms so that they cancel when the equations are subtracted. The same logic applies using \(b_1\) and \(b_2\) to cancel \(y\)-terms.

Following this lemma, one can solve explicitly for \(x\) and \(y\):

\[
\begin{aligned} 
x &= \frac{b_2 c_1 - b_1 c_2}{b_2 a_1 - b_1 a_2} \\
y &= \frac{a_1 c_2 - a_2 c_1}{a_1 b_2 - a_2 b_1}
\end{aligned}
\]

### Theorem 1

Given neither denominator is zero, the solution to

\[
\begin{cases} 
a_1 x + b_1 y = c_1 \\
a_2 x + b_2 y = c_2
\end{cases}
\]

is explicitly

\[
(x,y) = \left( \frac{b_2 c_1 - b_1 c_2}{b_2 a_1 - b_1 a_2}, \frac{a_1 c_2 - a_2 c_1}{b_2 a_1 - b_1 a_2} \right)
\]

### Theorem 2 (Cramer's Rule)

For an arbitrary system

\[
\begin{cases} 
a_1 x + b_1 y = c_1 \\
a_2 x + b_2 y = c_2
\end{cases}
\]

the solution can also be obtained via determinants:

\[
(x,y) = \left( \frac{\det(D_x)}{\det(D)}, \frac{\det(D_y)}{\det(D)} \right)
\]

where explicitly:

\[
(x,y) = \left( \frac{\det \begin{bmatrix} c_1 & b_1 \\ c_2 & b_2 \end{bmatrix}}{\det \begin{bmatrix} a_1 & b_1 \\ a_2 & b_2 \end{bmatrix}}, \frac{\det \begin{bmatrix} a_1 & c_1 \\ a_2 & c_2 \end{bmatrix}}{\det \begin{bmatrix} a_1 & b_1 \\ a_2 & b_2 \end{bmatrix}} \right)
\]

**Proof:** Recall that the determinant of a \(2 \times 2\) matrix is the difference of the products of its diagonals. Cramer's Rule is simply a restatement of the previous theorem using determinants:

\[
\left( \frac{\det \begin{bmatrix} c_1 & b_1 \\ c_2 & b_2 \end{bmatrix}}{\det \begin{bmatrix} a_1 & b_1 \\ a_2 & b_2 \end{bmatrix}}, \frac{\det \begin{bmatrix} a_1 & c_1 \\ a_2 & c_2 \end{bmatrix}}{\det \begin{bmatrix} a_1 & b_1 \\ a_2 & b_2 \end{bmatrix}} \right)\]

\[=
\left( \frac{b_2 c_1 - b_1 c_2}{b_2 a_1 - b_1 a_2}, \frac{a_1 c_2 - a_2 c_1}{b_2 a_1 - b_1 a_2} \right)
\]
