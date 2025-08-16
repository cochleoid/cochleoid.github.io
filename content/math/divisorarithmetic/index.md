---
title: "Divisor Arithmetic"
date: 2025-07-11
draft: false
description: "A quick primer on divisor functions and how to work with them."
tags: ["math", "number theory"]
---

{{< katex >}}

# Divisor Arithmetic

## Number of Divisors

The **divisor function**, \( d(n) \), tells you the number of divisors \( n \) has. When \( n \) is written in prime factorization as \( 3^2 \cdot 5^1 \cdot 2^1 \), for example, \( d(n) = (2+1)(1+1)(1+1) = 12 \).

## Sum of Divisors

The **sigma function**, \( \sigma(n) \), gives the sum of the divisors of \( n \). When \( n = 7^3 \cdot 2^2 \cdot 3^1 \), then  
\( \sigma(n) = (7^0 + 7^1 + 7^2 + 7^3)(2^0 + 2^1 + 2^2)(3^0 + 3^1) \).

## Product of Divisors

The **uppercase pi function**, \( \Pi(n) \), gives the product of the divisors of \( n \). The formula is:  
\( \Pi(n) = n^{\frac{d(n)}{2}} \)

## Even and Odd Divisors

The functions above can be modified with \( o \) and \( e \) subscripts, representing **odd** and **even** divisors.  
For example, \( d_e(56) \) counts how many even divisors 56 has, and \( \Pi_o(81) \) multiplies all of 81’s odd divisors.

To find the number of **odd divisors**, consider only the **odd prime factorization**.  
For instance, since \( 36 = 3^2 \cdot 2^2 \), we find \( d_o(36) = 2 + 1 = 3 \).  
Then, \( d_e(36) = d(36) - d_o(36) = 9 - 3 = 6 \).

## Examples

**Example 1:** *How many positive integers are divisors of \( 21^{75} \)?*  
(Source: MATHCOUNTS 1997 State Round)  
To solve this, break down \( 21^{75} \) into \( (7 \cdot 3)^{75} = 7^{75} \cdot 3^{75} \).  
Then, \( d(21^{75}) = (75+1)(75+1) = 76 \cdot 76 = 5776 \).

**Example 2:** *Karlanna places 600 marbles into \( m \) total boxes such that each box contains an equal number of marbles. There is more than one box, and each box contains more than one marble. For how many values of \( m \) can this be done?*  
(Source: Crawford's *Introduction to Number Theory*)  
This is asking for \( d(600) - 2 \), because we exclude \( m = 1 \) and \( m = 600 \).  
Since \( 600 = 2^3 \cdot 3 \cdot 5^2 \), then \( d(600) = (3+1)(1+1)(2+1) = 4 \cdot 2 \cdot 3 = 24 \).  
Thus, the answer is \( 24 - 2 = 22 \).

**Example 3:** *What is the value of \( d_o(432) \cdot d_e(432) \)?*

## Exercises

**Exercise 1:** \( d(7^2) \)  
**Exercise 2:** \( d(49^2) \)  
**Exercise 3:** \( d(36 + d(36)) \)  
**Exercise 4:** \( \sigma(d(18)) \)  
**Exercise 5:** \( \Pi(d(66)) \)  
**Exercise 6:** \( d_o(7) \)  
**Exercise 7:** \( d(4327904790) \cdot d_e(3) \)

## Credits

All explanations and problems written by **Adrian Hernandez Vega**, unless otherwise noted.

Prefer video? Watch the full explanation here:
{{< youtube cBJ_MDgM6dg >}}
