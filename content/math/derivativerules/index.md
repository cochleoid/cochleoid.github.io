---
title: "Basic Differentiation Rules"
description: "Introduction to the power rule, product rule, and trigonometric derivatives."
date: 2024-03-10
tags: ["calculus", "differentiation", "derivatives", "math"]
---
{{< katex >}}
# Basic Differentiation Rules

The **power rule** allows one to differentiate any polynomial with the following formula, where \( n \) is a constant:

\[
\frac{d}{dx} x^n = n x^{n-1}
\]

For example, the derivative of \( x^2 \) is \( 2x \) because

\[
\frac{d}{dx} x^2 = 2x^{2-1} = 2x
\]

## Positive Integer Powers

Using the power rule, evaluate the following:

- What is the derivative of \( x \)?
- What is the derivative of \( x^3 \)?
- What is the derivative of \( x + x^2 + x^3 \)?
- What is the derivative of \( x + 2x^2 + 3x^3 \)?
- What is the derivative of \( 3x + 3x^2 + 3x^3 \)?

## Fractional and Negative Powers

The power rule also applies to fractional and negative exponents. To differentiate \( \sqrt{x} \), rewrite it as \( x^{1/2} \) and apply the rule:

\[
\begin{aligned}
\frac{d}{dx} \sqrt{x} 
&= \frac{d}{dx} x^{1/2} \\
&= \frac{1}{2} x^{-1/2} \\
&= \frac{1}{2\sqrt{x}} = \frac{2\sqrt{x}}{4x}
\end{aligned}
\]

So the derivative of \( \sqrt{x} \) is \( \frac{1}{2\sqrt{x}} \) or \( \frac{2\sqrt{x}}{4x} \).

Let's try \( \frac{1}{x} \):

\[
\begin{aligned}
\frac{d}{dx} \frac{1}{x}
&= \frac{d}{dx} x^{-1} \\
&= -x^{-2} \\
&= -\frac{1}{x^2}
\end{aligned}
\]

So the derivative of \( \frac{1}{x} \) is \( -\frac{1}{x^2} \).

### Exercises

- If \( f(x) = \frac{2}{x^2} \), what is \( f'(x) \)?
- What is the derivative of \( 7x^{-7} + 3x \)?
- Prove the following: \( \frac{d}{dx} nx = n \)

# Differentiating Exponential Functions

## The Immortal Exponential Function

The derivative of \( e^x \) is \( e^x \), satisfying the differential equation \( f(x) = f'(x) \). Its derivative remains the same no matter how many times you differentiate.

- What is the 72,934th derivative of \( e^x \)?
- Simplify: \( \sum_{n=1}^{1000} f^{(n)}(x) \), given \( f(x) = e^x \)

## The Product Rule

To differentiate a product of functions, use the **product rule**:

\[
\frac{d}{dx} \big(f(x)g(x)\big) = f'(x)g(x) + f(x)g'(x)
\]

Example:

\[
\begin{aligned}
\frac{d}{dx} \big(x^3 \cos(x)\big) 
&= (\frac{d}{dx} x^3)\cos(x) + x^3(\frac{d}{dx} \cos(x)) \\
&= 3x^2 \cos(x) - x^3 \sin(x)
\end{aligned}
\]

### Exercises

- What is the derivative of \( \cos(x) \sin(x) \)?
- What is the derivative of \( e^x x^2 \)?
- What is the derivative of \( e^x \sin(x) + 2x^2 \cos(x) \)?

## The Quotient Rule

_Coming soon..._

# Differentiating Trigonometric Functions

Here are some key derivatives of basic trigonometric functions:

\[
\begin{aligned}
\frac{d}{dx} \sin(x) &= \cos(x) \\
\frac{d}{dx} \cos(x) &= -\sin(x) \\
\frac{d}{dx} [-\sin(x)] &= -\cos(x) \\
\frac{d}{dx} [-\cos(x)] &= \sin(x)
\end{aligned}
\]

### Exercises

- What is \( f'(x) \) if \( f(x) = \sin(x) \)?
- What is \( f''(x) \) if \( f(x) = \sin(x) \)?
- What is \( f^{(3)}(x) \) if \( f(x) = \sin(x) \)?
- What is \( f^{(4)}(x) \) if \( f(x) = \sin(x) \)?
- What is \( f^{(5)}(x) \) if \( f(x) = \sin(x) \)?
- What is \( f^{(400)}(x) \) if \( f(x) = \sin(x) \)?
- Give one solution to the differential equation \( f(x) = -f''(x) \)
