---
title: "Finding Elementary Inverse Functions"
date: 2024-03-04
draft: false
description: "Finding, verifying, and applying inverse functions."
tags: ["math", "functions", "algebra"]
---

{{< katex >}}

# Inverses

## What Are Inverses?

The **inverse** of a function undoes the action of that function.  
For example, since \( x^2 \) reverts \( \sqrt{x} \) back to \( x \), and vice versa, they are inverse functions.  
The inverse of \( f(x) \) is denoted \( f^{-1}(x) \).

**Exercise 1:** What is the inverse of \( x + 1 \)?  
**Exercise 2:** What is the inverse of \( 5x \)?  
**Exercise 3:** What is the inverse of \( x^3 \)?

## Finding Inverses

To find the inverse of a function:
1. Replace \( f(x) \) with \( y \).
2. Swap \( x \) and \( y \).
3. Solve for the new \( y \).

For example:

\[
\begin{aligned}
y &= x^2 + 1 \\
x &= y^2 + 1 \\
x - 1 &= y^2 \\
y &= \sqrt{x - 1}
\end{aligned}
\]

So the inverse of \( f(x) = x^2 + 1 \) is \( f^{-1}(x) = \sqrt{x - 1} \).

**Exercise 4:** What is the inverse of \( 4x + 2 \)?  
**Exercise 5:** What is the inverse of \( 5x^2 + 6 \)?  
**Exercise 6:** What is the inverse of \( \frac{1}{x} \)?

## Verifying Inverses

Since an inverse undoes its original function, you can verify an inverse by using **composition**.  
If \( f^{-1}(x) \) is truly the inverse of \( f(x) \), then:

- \( f(f^{-1}(x)) = x \)
- \( f^{-1}(f(x)) = x \)

**Exercise 7:** In our previous example, does \( f(f^{-1}(x)) = x \)?  
**Exercise 8:** In our previous example, does \( f^{-1}(f(x)) = x \)?  
**Exercise 9:** Do the two previous questions **always** verify an inverse?

## Review

**Exercise 10:** If \( f(1) = 2 \), what is the value of \( f^{-1}(2) \)?  
**Exercise 11:** If \( f(x) = \frac{\prod_{n=1}^5 \frac{n}{n + 1}}{\sum_{n=1}^{x} \frac{e}{n}} \), what is the value of \( f^{-1}(f(546)) \)?  
**Exercise 12:** What is the inverse of \( \frac{2}{7x^2} \)?

## Credits

All explanations and problems written by **Adrian Hernandez Vega**, unless otherwise noted.

Prefer video? Watch the full explanation here:
{{< youtube gR7IWjJeFrQ >}}
