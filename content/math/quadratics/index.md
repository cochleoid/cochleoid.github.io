+++
title = "Quadratics"
date = 2023-06-11
description = "Solving quadratic equations by various methods, including graphing, factoring, and completing the square."
draft = false
+++
{{< katex >}}
## Quadratics

### Solving by Plotting/Graphing

To solve the equation \( x^2 + 6x + 9 = 0 \) by graphing, create an xy-table with points. It's advisable to plot at least 5 points, though 3 can suffice. The axis of symmetry, determined by \( \frac{-b}{2a} \), marks the midpoint.

| x   | y   |
|-----|-----|
| -5  | 4   |
| -4  | 1   |
| -3  | 0   |
| -2  | 1   |
| -1  | 4   |

The zero is located at \( x = -3 \), which happens to be our axis of symmetry in this case. If the table had not included the solution, we would plot our 5 points, connect them all, and see where the x-intercepts would be.

### Solving by Grouping

Take the quadratic \( 5x^2 - 3x - 2 = 0 \). We need to find what multiplies to \( ac \) and adds to \( b \). The two numbers that satisfy these properties in this case are \( -5 \) and \( 2 \). Replace the \( b \) term with these terms that add to \( b \). Imagine a bar dividing the first pair of terms and second pair of terms and factor. After factoring, set both factors equal to zero to find your roots.

\[
\begin{aligned}
5x^2 - 3x - 2 &= 0 \\
5x^2 - 5x + 2x - 2 &= 0 \\
5x(x - 1) + 2(x - 1) &= 0 \\
(5x + 2)(x - 1) &= 0 \\
x &= -\frac{2}{5},\ 1
\end{aligned}
\]

### Solving by Completing the Square

To complete the square, your \( a \) coefficient must be 1 and your \( c \) term must be on the right side.

\[
\begin{aligned}
8x^2 - 32x - 64 &= 0 \\
x^2 - 4x - 8 &= 0 \\
x^2 - 4x &= 8
\end{aligned}
\]

After this, you must add \( \left(\frac{b}{2}\right)^2 \) to both sides. Then, factor the left-hand side to \( \left(x + \frac{b}{2}\right)^2 \), which is \( (x - 2)^2 \) in this case.

\[
\begin{aligned}
x^2 - 4x + (-2)^2 &= 8 + (-2)^2 \\
x^2 - 4x + 4 &= 12 \\
(x - 2)^2 &= 12
\end{aligned}
\]

The rest is algebra. Don't forget the \( \pm \) when taking the square root to account for the possibility of a second solution.

\[
\begin{aligned}
\sqrt{(x - 2)^2} &= \pm\sqrt{12} \\
x - 2 &= \pm\sqrt{12} \\
x &= \pm\sqrt{12} + 2
\end{aligned}
\]

### Solving by the Quadratic Formula

The quadratic formula is written below. Substitute your coefficients. We will use the quadratic \( x^2 + 2x + 1 = 0 \) as example.

\[
\begin{aligned}
x &= \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} \\
x &= \frac{-2 \pm \sqrt{4 - 4}}{2} \\
x &= \frac{-2 \pm \sqrt{0}}{2} \\
x &= \frac{-2 \pm 0}{2} \\
x &= \frac{-2}{2} \\
x &= -1
\end{aligned}
\]

### What is a complex number?

Try solving the equation \( x^2 = -1 \). No matter which method you use, your answer will be undefined. To circumvent this, mathematicians defined a new, special number: \( i = \sqrt{-1} \). To the previous equation, we can now say: \( x = \pm i \). We can scale this new "imaginary unit" by normal numbers as well: numbers such as \( 4i \) are equally valid.

We can combine real numbers and imaginary numbers to form a new set of numbers: the complex numbers. These are numbers of the form \( a + bi \), such as \( 2 + 3i \). Try solving \( x^2 + 2x + 1 = 0 \) using the Quadratic Formula.

### Writing Vertex Form from a Table

| x   | y   |
|-----|-----|
| -3  | 6   |
| -2  | 3   |
| -1  | 2   |
| 0   | 3   |
| 1   | 6   |

The vertex has the highest or lowest \( y \) value, so our vertex is \( (-1, 2) \). The vertex is located at \( (h, k) \) so we can substitute these numbers into the vertex form formula.

\[
\begin{aligned}
y &= a(x - h)^2 + k \\
y &= a(x - (-1))^2 + 2 \\
y &= a(x + 1)^2 + 2
\end{aligned}
\]

We are still left with an \( a \) coefficient. We can solve for this coefficient by plugging in a non-vertex point for \( x \) and \( y \). Let's choose \( (-3, 6) \).

\[
\begin{aligned}
6 &= a(-3 + 1)^2 + 2 \\
6 &= a(-2)^2 + 2 \\
6 &= 4a + 2 \\
a &= 1
\end{aligned}
\]

We found our \( a \) coefficient which we can plug in and get our final answer:

\[
\begin{aligned}
y &= 1(x + 1)^2 + 2 \\
y &= (x + 1)^2 + 2
\end{aligned}
\]
