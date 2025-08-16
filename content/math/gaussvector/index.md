+++
title = "Vector Summation with Gauss's Formula"
date = 2025-06-11
draft = false
description = "Explaining how Gauss's formula can be applied to vectors through component addition."
tags = ["math", "algebra", "summation", "vectors", "counting"]
+++

{{< katex >}}

## Vector Summation Trick (Inspired by Gauss)

In this article we're going to be dealing with a little vector sum.

We're given:

\[
\sum_{i=1}^{100} 
\begin{bmatrix}
i - 1 \\
i \\
i + 1
\end{bmatrix}
\]

And if we don't recognize this sum immediately, it's usually a good idea to try a few terms and look for a pattern.

---

## Trying a Few Terms

When \( i = 1 \):

\[
\begin{bmatrix}
0 \\
1 \\
2
\end{bmatrix}
\]

When \( i = 2 \):

\[
\begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix}
\]

When \( i = 3 \):

\[
\begin{bmatrix}
2 \\
3 \\
4
\end{bmatrix}
\]

... and so on, until \( i = 100 \):

\[
\begin{bmatrix}
99 \\
100 \\
101
\end{bmatrix}
\]

So, what are we really summing here?

---

## Adding Vectors

When you add column vectors, you add component-wise. So this becomes:

\[
\sum_{i=1}^{100} 
\begin{bmatrix}
i - 1 \\
i \\
i + 1
\end{bmatrix}
=
\begin{bmatrix}
\sum_{i=1}^{100} (i - 1) \\
\sum_{i=1}^{100} i \\
\sum_{i=1}^{100} (i + 1)
\end{bmatrix}
\]

Now we can break each of these down.

---

## Middle Term: Gauss Trick

Everyone knows how to add:

\[
1 + 2 + 3 + \dots + 100
\]

And for that, there's a trick supposedly discovered by Gauss in elementary school.

Pair numbers from the ends:

- \( 1 + 100 = 101 \)
- \( 2 + 99 = 101 \)
- \( 3 + 98 = 101 \)
- ...

There are 50 such pairs:

\[
\sum_{i=1}^{100} i = 50 \times 101 = 5050
\]

So the **middle element** in our vector sum is:

\[
\sum_{i=1}^{100} i = 5050
\]

---

## Top Term: Each \( i - 1 \)

This is just shifting each term down by 1, so it's:

\[
\sum_{i=1}^{100} (i - 1) = \sum_{i=1}^{100} i - 100 = 5050 - 100 = 4950
\]

---

## Bottom Term: Each \( i + 1 \)

Each term is bumped up by 1:

\[
\sum_{i=1}^{100} (i + 1) = \sum_{i=1}^{100} i + 100 = 5050 + 100 = 5150
\]

---

## Final Answer

So, the entire sum simplifies to:

\[
\begin{bmatrix}
4950 \\
5050 \\
5150
\end{bmatrix}
\]

---

## Credits

All explanations and problems written by **Adrian Hernandez Vega**, unless otherwise noted.

Prefer video? Watch the full explanation here:  
{{< youtube V5jD8eyu-mE >}}
