---
title: "Introduction to the Asymptotes of a Rational Function"
date: 2024-05-21
draft: false
description: "A quick tutorial on horizontal, vertical, and oblique asymptotes."
tags: ["math", "algebra"]
---

{{< katex >}}


## Definitions

A **rational function** is the division of two polynomials, such as \( f(x) = \frac{5x^2 + 7}{4x^3 + 2x} \). The **degree** of a polynomial is the highest exponent in the function; in this example, the degrees are 2 and 3, respectively. The **leading coefficient** is the coefficient of the term with the highest exponent; here, they are 5 and 4.

## Vertical Asymptotes

Division by zero is undefined. In the function \( f(x) = \frac{x+2}{x+1} \), the denominator is zero when \( x = -1 \), which makes the expression undefined. So, \( x = -1 \) is a vertical asymptote. To find vertical asymptotes, set the denominator equal to zero and solve for \( x \). These values represent lines that the function approaches but never touches.

**Exercise 1:** Where is the vertical asymptote of the function \( r(x) = \frac{x+5}{x^2 + 2x + 1} \)?  
**Exercise 2:** Where is the vertical asymptote of the function \( a(x) = \frac{3x + 3(x+7)^9 + \pi}{x^3 + x^2 + x} \)?

## Horizontal/Oblique Asymptotes

### Bottom-Heavy Degree

A **bottom-heavy** rational function is one where the denominator's degree is greater than the numerator's. For example, \( h(x) = \frac{5x^2 + 7}{4x^3 + 2x} \) has a horizontal asymptote at \( y = 0 \). This is because as \( x \to \infty \), the denominator grows faster, and the function tends toward zero. If a constant is added after the rational function, the horizontal asymptote shifts. For example, \( h(x) = \frac{5x^2 + 7}{4x^3 + 2x} + 3 \) has a horizontal asymptote at \( y = 3 \).

**Exercise 3:** Where is the horizontal asymptote of the function \( s(x) = \frac{x^4 + x^3}{x^9 + 9} \)?  
**Exercise 4:** Where is the horizontal asymptote of the function \( b(x) = \frac{x^5 + 5}{x^6 + 6} + 7 \)?

### Equal Degree

When the degrees of the numerator and denominator are the same, the horizontal asymptote is the ratio of the leading coefficients. For example, \( A(x) = \frac{7x + 5}{8x + 2} \) has a horizontal asymptote at \( y = \frac{7}{8} \).

**Exercise 5:** Where is the horizontal asymptote of the function \( F(x) = \frac{(1+2+3+4)x^5 + 6}{(1-2-3-4)x^5 - 6} \)?  
**Exercise 6:** Where is the horizontal asymptote of the function \( p(x) = \frac{\pi x^3}{\pi x^3 + \pi} + \pi \)?

### Top-Heavy Degree

If the numerator's degree is higher than the denominator's, there is no horizontal asymptote. Instead, the function has an **oblique** (slanted) asymptote of the form \( y = mx + b \). To find it, divide the numerator by the denominator and ignore the remainder. For example, \( j(x) = \frac{x^2 + 2x + 1}{x + 4} \) simplifies to \( x - 2 + \frac{9}{x + 4} \), so the oblique asymptote is \( y = x - 2 \).

**Exercise 7:** Where is the oblique asymptote of the function \( Y(x) = \frac{x^2 + 2x + 3}{x + 4} \)?  
**Exercise 8:** The oblique asymptote of \( Q(x) = \frac{x^2 + 9x + 2}{x + 6} \) is of the form \( y = Ax + T \). The vertical asymptote is \( x = K \). What is the value of \( (A + T + K)^2 \)?

## Holes

When a rational function has a factor that cancels in both the numerator and denominator, a **hole** occurs. For example, \( \frac{(x+1)}{(x+1)(x+2)} = \frac{1}{x+2} \), but \( x = -1 \) is still a point of discontinuity. So while the simplified expression looks like \( \frac{1}{x+2} \), the graph must show a hole at \( x = -1 \).

**Exercise 9:** Find the hole(s) of \( \frac{(x+2)(x+5)}{3(x+2)} \)  
**Exercise 10:** Find the hole(s) of \( \frac{(2x^2 + 4x + 2)(4x + 8)}{(2x + 2)(x^2 + 4x + 4)} \)

## Mixed Practice

**Exercise 11:** The horizontal and vertical asymptotes of \( f(x) = \frac{x^2 + 4x + 4}{x^2 + 2x + 1} \) intersect at a single point \( (P_1, P_2) \). What is \( P_1 + P_2 \)?  
**Exercise 12:** The functions \( a(x) = \frac{6x^7 + 8x + 3}{3x^2 - 27} \) and \( b(x) = \frac{x^3 + 2x + 5}{3x^2 - K} \) have the same vertical asymptote. If the horizontal asymptote of \( a(x) \) is moved up by \( K^2 \), what is the new asymptote?  
**Exercise 13:** The oblique asymptote of \( c(x) = \frac{x^2 + 6x + 9}{x + 8} \) is of the form \( y = mx + b \). A line \( \ell \), perpendicular to this asymptote, passes through \( (0, 3) \). What is the sum of \( \ell \)'s slope and y-intercept?  
**Exercise 14:** The equations \( Z(x) = \frac{x^5 + 5x + 5}{x^5 + 5} \) and \( I(x) = \frac{x + 1}{x^2 + 2x + L} + L \) have the same horizontal asymptote. Where is the hole of \( I(x) \)?  
**Exercise 15:** Let \( V(x) = \frac{x^8 + x^7 + x^6 + \cdots + x + 1}{x^{80} + x^{79} + \cdots + x + 1} \). To the nearest hundredth, what is the value of \( V(80) \)?  
**Exercise 16:** Line A is defined by the vertical asymptote of \( R(x) = \frac{2x^2 + 2x + 2}{x + 2} \). Line B is the oblique asymptote of \( R(x) \). Line C is the horizontal asymptote of \( \frac{1}{R(x)} \). What is the area of the triangle bounded by lines A, B, and C?

## Credits

All explanations and problems written by **Adrian Hernandez Vega**, unless otherwise noted.

Prefer video? Watch the full explanation here:
{{< youtube ZiYYw7L8hCM >}}


