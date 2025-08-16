---
title: "Logarithmic Differentiation with Some Examples"
date: 2024-04-12
draft: false
description: "Using properties of logarithms to solve some derivatives the power rule can’t."
tags: ["math", "calculus", "differentiation","logarithms"]
---
{{< katex >}}

## Logarithmic Differentiation

Let’s say you have an expression like \( x^x \).

You **can’t** use the regular power rule here because the exponent isn't a constant. So what do we do?

We use **logarithmic differentiation**.

---

## First Example: \( x^x \)

Let:

\[
y = x^x
\]

Take the natural log (ln) of both sides. You *can* technically use any base, but base \( e \) (i.e., \( \ln \)) is the most convenient.

\[
\ln y = \ln(x^x)
\]

Using log rules to move the exponent down:

\[
\ln y = x \ln x
\]

Now, differentiate both sides. Remember the rule:

\[
\frac{d}{dx}[\ln(f(x))] = \frac{f'(x)}{f(x)}
\]

So:

\[
\frac{d}{dx}[\ln y] = \frac{dy}{dx} \cdot \frac{1}{y} = \frac{y'}{y}
\]

And for the right-hand side \( x \ln x \), we use the product rule:

\[
\frac{d}{dx}[x \ln x] = x \cdot \frac{1}{x} + \ln x = 1 + \ln x
\]

Putting it all together:

\[
\frac{y'}{y} = 1 + \ln x
\]

Now multiply both sides by \( y \):

\[
y' = y(1 + \ln x)
\]

Since \( y = x^x \), we substitute:

\[
\boxed{y' = x^x(1 + \ln x)}
\]

---

## Harder Example: \( (\sin x)^x \)

Let:

\[
y = (\sin x)^x
\]

Again, take the natural log of both sides:

\[
\ln y = \ln\left((\sin x)^x\right)
\]

Use the same trick: bring the exponent down:

\[
\ln y = x \ln(\sin x)
\]

Now differentiate both sides:

- Left-hand side:

\[
\frac{y'}{y}
\]

- Right-hand side (product rule):

\[
\frac{d}{dx}[x \ln(\sin x)] = x \cdot \frac{d}{dx}[\ln(\sin x)] + \ln(\sin x)
\]

Use the chain rule on \( \ln(\sin x) \):

\[
\frac{d}{dx}[\ln(\sin x)] = \frac{\cos x}{\sin x} = \cot x
\]

So now the derivative becomes:

\[
\frac{y'}{y} = x \cot x + \ln(\sin x)
\]

Multiply both sides by \( y \):

\[
y' = y(x \cot x + \ln(\sin x))
\]

And substitute \( y = (\sin x)^x \):

\[
\boxed{y' = (\sin x)^x (x \cot x + \ln(\sin x))}
\]

---

## Summary

Logarithmic differentiation is your go-to tool when:

- The **exponent is not constant**
- You have **variable bases and exponents**
- You need to simplify messy products involving exponents and logs

## Credits

All explanations and problems written by **Adrian Hernandez Vega**, unless otherwise noted.

Prefer video? Watch the full explanation here:
{{< youtube x_dYtcO5BbA >}}
