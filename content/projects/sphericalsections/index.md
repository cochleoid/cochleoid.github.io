---
title: "Deriving Curved Surface Area Sections Over a Sphere"
date: 2025-08-16
draft: false
description: "A derivation of the surface area of a spherical strip without using parametrization or spherical coordinates."
tags: ["mathematics", "calculus", "geometry"]
---

{{< katex >}}

# Deriving Curved Surface Area Sections Over a Sphere

## Abstract
A problem Mr. Rosario and I briefly discussed regarding how one would solve for a partitioned surface area from a birds-eye view in between bounds \(x=b\) and \(x=a\). The goal is to derive an explicit formula without spherical coordinates or parametrization.

## The (Failed) First Idea

I thought about cutting the sphere like ham slices. Look at it from the front: is that not a circle with "radius" 0 and arc length 0? Repeat this logic for all the circles behind it. If we add up all the rings around these circles, we should approach the total surface area.

The radius for each of these sub-circles can be modeled by \(f(x)=\sqrt{r^2-x^2}\), so each ring length will be:

\[
2\pi \sqrt{r^2-x^2}
\]

So then wouldn't the total curved surface area on this hemisphere be the below?

\[
\int_{a}^{b} 2\pi \sqrt{r^2-x^2} \, dx
\]

Short answer: not quite. Let's do a quick sanity check, where we set \(r=1\) for a unit hemisphere, \(b=1\), and \(a=-1\). This should evaluate to \(2\pi\) because a sphere's surface area is \(4\pi r^2\).

\[
\begin{aligned}
\int_{-1}^{1} 2\pi \sqrt{1-x^2} \, dx &= 2\pi \int_{-1}^{1} \sqrt{1-x^2} \, dx \\
&= 2\pi \left(\frac{\pi}{2}\right) \\
&= \pi^2
\end{aligned}
\]

We are not dealing with a Bessel series! We can discard this as a possible integral, but the fundamental idea is correct.

## The Correction

Apply the arc length differential! Recall the arc length formula:

\[
\sqrt{1+(f'(x))^2}
\]

Before proceeding, we're faced with a quick derivative exercise, where \(r\) is a constant:

\[
\begin{aligned}
\frac{d}{dx} \sqrt{r^2 - x^2} &= -2x \left( \frac{1}{2} (r^2 - x^2)^{-1/2} \right) \\
&= -x (r^2 - x^2)^{-1/2} \\
&= -\frac{x}{\sqrt{r^2 - x^2}}
\end{aligned}
\]

Let's incorporate this into the corrected integral:

\[
\begin{aligned}
2\pi \int_a^b \sqrt{r^2 - x^2} \, \sqrt{1 + (f'(x))^2} \, dx
&= 2\pi \int_a^b \sqrt{r^2 - x^2} \, \sqrt{1 + \left( \frac{-x}{\sqrt{r^2 - x^2}} \right)^2} \, dx \\
&= 2\pi \int_a^b \sqrt{r^2 - x^2} \, \sqrt{1 + \frac{x^2}{r^2 - x^2}} \, dx \\
&= 2\pi \int_a^b \sqrt{ \left(1 + \frac{x^2}{r^2 - x^2} \right) (r^2 - x^2) } \, dx
\end{aligned}
\]

The inner product looks messy, but let \(u = r^2 - x^2\):

\[
\begin{aligned}
\left( 1 + \frac{x^2}{r^2 - x^2} \right)(r^2 - x^2) &= \left(1 + \frac{x^2}{u}\right) u \\
&= u + x^2 \\
&= (r^2 - x^2) + x^2 \\
&= r^2
\end{aligned}
\]

Continuing the integral:

\[
\begin{aligned}
2\pi \int_a^b \sqrt{r^2} \, dx &= 2\pi \int_a^b r \, dx \\
&= 2\pi r \int_a^b 1 \, dx \\
&= 2\pi r (b - a)
\end{aligned}
\]

## The Formula

Beautiful! That is our final explicit formula: \(2\pi r (b-a)\). Try setting \(b=r\) and \(a=-r\).

