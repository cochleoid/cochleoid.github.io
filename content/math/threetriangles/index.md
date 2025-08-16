---
title: "The Three Main Methods for Triangle Area"
date: 2025-01-15
draft: false
description: "Presents the base-height, sine, and Heron methods for triangle area."
tags: ["math", "geometry"]
---

{{< katex >}}

## Method 1: Base × Height ÷ 2

> Formula:  
\[
\text{Area} = \frac{1}{2} \cdot \text{base} \cdot \text{height}
\]

Say you have a triangle with base 10 and height 5:

\[
\text{Area} = \frac{1}{2} \cdot 10 \cdot 5 = 25
\]

---

### Example Problem

> The area of a triangle is 150. The height is 5 units less than the base. Find base and height.

Let base = \( b \), then height = \( b - 5 \). Using:

\[
\frac{1}{2} \cdot b \cdot (b - 5) = 150
\]

\[
b(b - 5) = 300 \quad \Rightarrow \quad b^2 - 5b - 300 = 0
\]

Solving:

\[
b = 20 \Rightarrow \text{height} = 15
\]

**Base = 20, Height = 15**

---

## Method 2: Sine Formula

> Formula:  
\[
\text{Area} = \frac{1}{2} ab \sin(C)
\]

Where \( a \) and \( b \) are two sides, and \( C \) is the included angle.

---

### Example

> Find the area of a triangle with sides 3 and 4 and an included angle of \( 30^\circ \).

\[
\text{Area} = \frac{1}{2} \cdot 3 \cdot 4 \cdot \sin(30^\circ) = \frac{1}{2} \cdot 12 \cdot \frac{1}{2} = 3
\]

**Area = 3**

---

## Method 3: Heron’s Formula

> Use when **all three sides** are known.

\[
s = \frac{a + b + c}{2}
\]

\[
\text{Area} = \sqrt{ s(s - a)(s - b)(s - c) }
\]

---

### Example

> Triangle with sides 4, 7, and 5

1. Compute semi-perimeter:
\[
s = \frac{4 + 7 + 5}{2} = 8
\]

2. Plug into Heron’s Formula:

\[
\text{Area} = \sqrt{ 8(8 - 4)(8 - 7)(8 - 5) } = \sqrt{8 \cdot 4 \cdot 1 \cdot 3}
\]

3. Simplify:

\[
\text{Area} = \sqrt{96} = \sqrt{16 \cdot 6} = 4\sqrt{6}
\]

**Area = \( 4\sqrt{6} \)**

## Credits

All explanations and problems written by **Adrian Hernandez Vega**, unless otherwise noted.

Prefer video? Watch the full explanation here:
{{< youtube 5WepDGtnYtk >}}
