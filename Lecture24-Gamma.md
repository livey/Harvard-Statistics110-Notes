#####Gamma distribution 
######Gamma function 
n! \approx \sqrt(2\pi*n)(n/e)^n 

\Gamma(a)=\int_0^\inf x^{a-1}*e^{-x}dx, for real a>0. 
\Gamma(n)=(n-1)! for postive integer 
\Gamma(x+1) = x\Gamma(x) 

\Gamma(1/2) = \sqrt{\pi}; \Gamma(3/2)=\sqrt(\pi)/2

1= \int_0^\inf x^{a-1}e^-x/\Gamma{a} dx = Gamma(a,1) PDF 

Y ~ Gamma(a,\lambda) PDF 
Let Y = X/\lambda, X ~ Gamma(a,1)
f_Y(y) = f_X(x) dx/dy = 1/\Gamma(a)*(\lambda*y)x^{a-1}e^{-\lambda*y}*\lambda 

######Gamma Expo connection 
Poisson process ~ Pois(\lambda*t) 
Number of arrivals in disjoint intervals are independent 

The fisrt event happen in T1, is a exponential distribution 
P(T1>t)  = e^{-\lambda*t}

inter arrival times are i.i.d. Exp(\lambda) 
Tn = time of the n'th arrival 
= sum_j X_j, Xj are i.i.d. Exp(\lambda)
~ \Gamma(n,\lambda) 

Proof that T =\sum_j Xj ,Xj is i.i.d. Expo(1) is Gamma(n,1) 
(use MGF) 
MGF of X1 is 1/(1-t) valid t<1 
===> MGF of Tn = (1/(1-t))^n 

Looking at the MGF of Gamma distribution 
Let Y ~ Gamma(n,1) 
E(e^{tY}) = \int_0^\int 1/Gamma(n)* e^{ty}y^{n-1}e^{-y}dy 
          = 1/Gamma(n)\int_0^\inf y^{n-1}e^{-(1-t)y}dy 
let x = (1-t)y dx = (1-t)dy 
          = (1-t)^{-n}/Gamma(n)\int_0^\inf x^{n-1} e^{-x}dx 
          = 1/(1-t)^n

Let X~ Gamma(a,1), find E(X^c) 
1/\Gamma(a)\int_0^\inf x^c x^{a-1}e^{-x}dx 
= \Gamma(a+c)/\Gamma(a) if a+c > 0; 

E(x) = \Gamma(a+1)/\Gamma(a) = a. 
E(X^2) = a^2+a 
Var(X) = a. 

X~ Gamma(a,\lambda) 

E(X)=a/\lambda 
Var(X)=a/\lambda^2 




