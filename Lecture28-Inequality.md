
####Lecture28 Inequalities
1.Cauchy-Scharz: |E(XY)|<=\sqrt{E(X^2)E(Y^2)}
if X,Y are uncorrelated, E(XY) = E(X)E(Y)
this inequality is useful when two variables are correlated. 
--Interpretaion if X,Y have mean 0. then 
Corre(X,Y) = E(XY)/(E(X^2)E(Y^2)^{1/2}
|Corr(X,Y)|<=1; 

2.Jenssen's Inequality:
if g is a convex function, then:
Eg(x) >= g(EX) (when X is a constant, then the equality holds)
If h is concave , Eh(X)<=h(EX)
if g(X)=X^2 
then, E(X^2)>=E^2(X)

E(1/X)>=1/E(X), X is positive. 
E(lnX)<=lnE(X) 

Proof. g(x) >= a+bx 
g(X) >= a+bX 
E(g(X)) >= E(a+bX) 
		 =a+bE(X)=a+b\mu 
		 =g(EX)

3.Markov Inquality : P(|X|>=a)<=E|X|/a, for any a>0. 
if E|X|/a>1. then this gives no information 

a*I_{|X|>=a} =<|X|, I--the indicator variable 
So the expected value a*E(I) < E|X| 

intuition 
Ex. 100 people. Is it possible at least 95% are younger than mean average.(Yes)
......at leat 50% older than twice the average age?(No)

3.Chebyshev Inequality: P(|X-u|>a)<=Var(X)/a^2 
P(|X-u|>c*SD(X))<=1/c^2 

Proof. P(|X-u|>a) = P((X-u)^2>a^2)
=< (E(X-u)^2)/a^2 = Var(X)/a^2 



