####Exponetial MGF 
X~Expo(1), find MGF, moment generating function, 
M(t) = E(e^{tx}) 
\int _0^\inf e^{tx} e^{-x} dx = 1/(1-t), t< 1. 
M'(0)= E(X), M''(0) = E(^2) , M'''(0) = E(X^3)...
1\(1-t) = \sum_{n=0}^\inf t^n = \sum_{n=0}^\inf n!t^n/n! 
==> E(X^n)= n! 

Y~Expo(\lambda), let X=\lambda*Y ~ Expo(1), so Y^n = X^n/\lambda^n. 
E(Y^n) = n!/\lambda^n 

####Normal moments, Z~N(0,1), find all its moments. 
E(Z^n) = 0, if n is odd.(by symmetry) 
MGF M(t) = e^{t^2/2} =\sum_{n=0}^\inf (t^2/2)^n/n! =\sum_{n=0}^\inf t^{2n}/2^n/n!. 
= \sum_{n=0}^\inf (2n)!t^{2n}/2^n/(2n)! 
==> E(Z^(2n)) =(2n)!/2^n/n! 
verify: n= 1; E(Z^2) = 1; E(Z^4) = 3; E(Z^6) = 15. 

####Possion Distribution 
X~Pois(\lambda) E(e^(tx)) = \sum_{k=0}^\inf e^{tk} \lambda^k/k*e^{-\lambda}=e^{-\lambda} e^{\lambda*e^t}
Let Y~Pois(\mu) independent of X, find the distribution of X+Y. 
Multiply the MGFs : e^{\lambda(e^t-1)}e\mu(e^t-1) = e^{\lambda+\mu}(e^t-1) ===> X+Y ~ Pois(\lambda+\mu) 
Notify: independent. 
Counter example if X,Y dependent: X=Y ===> X+Y =2X is not Possion. since 2X is even.[if X is possion E(2X) = 2\lambda Var(2X) =4\lambda]

####Joint Distribution 
X, Y Bernoulli 
X, Y r.v.s
F(x,y) = P(X<=x,Y<=y) 
joint PMF(discrete case) P(X=x,Y=y)
Marginal CDF
P(X<=x) is marignal distribution of X. 
joint PDF. 
f(x,y) such that 
P((x,))\in B) = \int_{B} f(x,y) dxdy 

independence X,Y are independent if and only if F(x,y)= F_x(x)F_y(y) 
Equava. to P(X=x,Y=y) = P(X=x)P(Y=y) 
f(x,y) = f_x(x)f_y(y) for all real x and y. 

P(X=x) = \sum_y P(X=x,Y=y)
f_y(y)  = \int_\-inf^\inf f_x,y(x,y)dx 

Exam. Uniform on square{(x,y): x,y\in [0,1]} joint PDF const. on the square and 0 outside the square. 
f(x,y) = 1; (x,y)\in[0,1]^2. X,Y is independent. 

Ex. Unif in a disc. X^2+Y^2<=1; 
joint PDF: f(x,y) = 1/(\pi)(ihnside the disc, otherwise 0 ). 
So they are dependent. Given X=x, -\sqrt{1-x^2} <=y<=\sqrt{1-x^2}

