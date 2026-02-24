+++
title = "circlesddsdsd"
description = "cafde"
date = 2026-02-04
+++
{{< katex >}}
Problem concept and solutions by Adrian Hernandez Vega.



## Matrix and Problems



Consider the matrix below as \( n \xrightarrow{} \infty \), where \( p_n \) indicates the \( n \)th prime number.


\(  \) 
A = \begin{bmatrix}
\left\lfloor \frac{3930}{p_1} \right\rfloor & \left\lfloor \frac{3930}{p_2} \right\rfloor & \left\lfloor \frac{3930}{p_3} \right\rfloor & \cdots & \left\lfloor \frac{3930}{p_n} \right\rfloor 


\left\lfloor \frac{3930}{p_1^{2}} \right\rfloor & \left\lfloor \frac{3930}{p_2^{2}} \right\rfloor & \left\lfloor \frac{3930}{p_3^{2}} \right\rfloor & \cdots & \left\lfloor \frac{3930}{p_n^{2}} \right\rfloor 


\left\lfloor \frac{3930}{p_1^{3}} \right\rfloor & \left\lfloor \frac{3930}{p_2^{3}} \right\rfloor & \left\lfloor \frac{3930}{p_3^{3}} \right\rfloor & \cdots & \left\lfloor \frac{3930}{p_n^{3}} \right\rfloor 


\vdots & \vdots & \vdots & \ddots & \vdots 


\left\lfloor \frac{3930}{p_1^{n}} \right\rfloor & \left\lfloor \frac{3930}{p_2^{n}} \right\rfloor & \left\lfloor \frac{3930}{p_3^{n}} \right\rfloor & \cdots & \left\lfloor \frac{3930}{p_n^{n}} \right\rfloor
\end{bmatrix}
 \(  \)





### Trailing Zeros


Find the number of trailing zeros in \( 3930! \)



### Sum of Entries


Let \( \alpha \) be the sum of all entries in \( A \).



1. Prove/disprove: \( \alpha \) diverges.




1. Prove/disprove: \( \alpha < 3930! \)




1. Express \( \alpha \) in terms of factorials and prime-counting or divisor functions.






### Product of Entries


Let \( \beta \) be the product of all entries in \( A \).



1. Prove/disprove: \( \beta \) diverges.




1. Prove/disprove: \( \beta < 3930! \)






### Eigenvalues





1. If possible, find the sum of the eigenvalues of \( A \) (truncated if needed).




1. If possible, find the product of the eigenvalues of \( A \) (truncated if needed).






## Solutions





### Trailing Zeros


Find the number of trailing zeros in \( 3930! \)



We are tasked with finding the number of 10's inside the factorization of \( 3930! \). Since there will be more 2's than 5's, it suffices to count the number of 5's using **Legendre's Formula**, dividing by powers of 5:


\(  \) 
\left\lfloor \dfrac{3930}{5} \right\rfloor + \left\lfloor \dfrac{3930}{25} \right\rfloor + \left\lfloor \dfrac{3930}{125} \right\rfloor + \left\lfloor \dfrac{3930}{625} \right\rfloor
+\left\lfloor \dfrac{3930}{3125} \right\rfloor
 \(  \)




\(  \) 
786+157+31+6+1=\boxed{980}
 \(  \)





### Sum of Entries


Let \( \alpha \) be the sum of all entries in \( A \).

\item **\( \alpha \) converges:** Let \( k \) be the first prime larger than 3930. Then,


\(  \) 
\left\lfloor \dfrac{3930}{k^n} \right\rfloor=0
 \(  \)


for positive integer \( n \), implying that every entry in \( k \)'s column is 0. Since all subsequent columns contain larger primes, their entries must also be zero. Apply the same argument to a row's columns to show that their values vanish with higher exponents. Every column has a finite number of non-zero elements, and there is a finite number of columns prior to \( k \)'s:

The sum \( \alpha \) is thus finite: \( \boxed{\textbf{convergent}} \)

\item **Express \( \alpha \) in terms of factorials and prime-counting or divisor functions.** Notice that since every column contains the Legendre sum for prime \( p_n \): \( \boxed{\Omega(3930!)} \)

\item **Prove/disprove: \( \alpha < 3930! \)** Observe that 2 would have the highest exponent in \( \Omega(3930!) \), since it is the smallest prime. Using geometric series for an upper bound, we can see \( 3930>(\text{exponent of 2}) \).




\(  \) 
\sum_{n=1}^{\infty}\left\lfloor \frac{3930}{2^n} \right\rfloor < \sum_{n=1}^{\infty} \left( \frac{3930}{2^n} \right)
 \(  \)







\(  \) 
< 3930
 \(  \)




The number of primes \( \leq 3930 \) is at most 3930. As a crude bound, each prime would have an exponent of at most 3930:




\(  \) 
\Omega(3930!) < 3930^2
 \(  \)







\(  \) 
\implies \Omega(3930!) < 3930!
 \(  \)







\(  \) 
\implies \boxed{\alpha < 3930!}
 \(  \)








### Product of Entries


Let \( \beta \) be the product of all entries in \( A \).

\item **\( \beta \) converges:** There exist infinitely many zero columns; the product of all entries must then be \( \boxed{0} \).
\item **\( \beta < 3930! \), as \( 0<3930! \)**




### Eigenvalues



\item **If possible, find the sum of the eigenvalues of \( A \) (truncated if needed).** Recall that the sum of the eigenvalues is equal to the trace of the matrix. Adding the diagonal entries:




\(  \) 
\sum_{n=1}^{\infty} \left\lfloor \frac{3930}{p_n^{\,n}} \right\rfloor =
\left\lfloor \frac{3930}{2^1} \right\rfloor
+ \left\lfloor \frac{3930}{3^2} \right\rfloor
+ \left\lfloor \frac{3930}{5^3} \right\rfloor
+ \left\lfloor \frac{3930}{7^4} \right\rfloor
 \(  \)







\(  \) 
\quad
+ \left\lfloor \frac{3930}{11^5} \right\rfloor
+ \left\lfloor \frac{3930}{13^6} \right\rfloor
+ \cdots
 \(  \)







\(  \) 
= 1965 + 436 + 31 + 1 + 0 + 0 + \cdots
 \(  \)







\(  \) 
= \boxed{2433}
 \(  \)





\item **If possible, find the product of the eigenvalues of \( A \) (truncated if needed).** Recall that the product of the eigenvalues is equal to the determinant of the matrix. Using the same column argument as in Solution 2.2.1, a prime number \( j > 3930 \) creates blank columns; a zero column turns the determinant into \( \boxed{0} \).