---
title: "Tangent Substitution in Integration"
date: 2025-08-30
draft: false
description: "A tutorial explaining how to use the tangent substitution for integrals with the expression x^2 + a^2."
tags: ["math", "integration", "substitution", "trigonometry"]
---

{{< katex >}}

# Tangent Substitution in Integration

We are going to cover one of the main three types of **trigonometric substitution**.  

You might be asking: *why do we need trig for this?*  
After all, this looks like just a rational expression:

\[
\int \frac{1}{x^2 + 16} \, dx
\]

And you’d be right: tt is rational indeed. But with methods we’ve learned so far (like \( u \)-substitution or integration by parts), there won’t be a compatible term to make progress.  

That’s where the tangent substitution comes in.

---

## Step 1: Substitution

We substitute:

\[
x = 4 \tan \theta
\]

Why 4? Because when we square this, the \( 4^2 \) matches the \( 16 \) in the denominator.

---

## Step 2: Rewrite the Denominator

Squaring:

\[
x^2 + 16 = (4 \tan \theta)^2 + 16 = 16 \tan^2 \theta + 16
\]

Factor:

\[
16(\tan^2 \theta + 1)
\]

And from the **Pythagorean identity**:

\[
\tan^2 \theta + 1 = \sec^2 \theta
\]

So the denominator becomes:

\[
16 \sec^2 \theta
\]

---

## Step 3: Adjust the Integral

Now our integral looks like:

\[
\int \frac{1}{16 \sec^2 \theta} \, dx
\]

That is:

\[
\frac{1}{16} \int \cos^2 \theta \, dx
\]

But here’s a problem: the integral is still in terms of \( dx \), while our substitution is in terms of \( \theta \).

---

## Step 4: Differentiate the Substitution

From:

\[
x = 4 \tan \theta
\]

Differentiate:

\[
dx = 4 \sec^2 \theta \, d\theta
\]

---

## Step 5: Replace \( dx \)

Substitute into the integral:

\[
\frac{1}{16} \int \cos^2 \theta \cdot (4 \sec^2 \theta) \, d\theta
\]

Simplify:

\[
\frac{4}{16} \int \cos^2 \theta \cdot \sec^2 \theta \, d\theta
\]

Since \(\cos^2 \theta \cdot \sec^2 \theta = 1\):

\[
\frac{1}{4} \int 1 d\theta
\]

---

## Step 6: Integration

This is straightforward:

\[
\frac{1}{4} \theta + C
\]

---

## Step 7: Back-Substitute

Recall:

\[
x = 4 \tan \theta \quad \Rightarrow \quad \theta = \arctan\!\left(\frac{x}{4}\right)
\]

So the final answer is:

\[
\int \frac{1}{x^2 + 16} \, dx = \frac{1}{4} \arctan\!\left(\frac{x}{4}\right) + C
\]

---

**Final Result:**

\[
\frac{1}{4} \arctan\!\left(\frac{x}{4}\right) + C
\]

Prefer video? Watch the full explanation here:  
{{< youtube 9QswYqkFTrc >}}
---
