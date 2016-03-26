###Lecture30 Chi-Square,T distribution, and MVN 
\Chi^2(n) 
Let V = Z1^2+Z2^2+...+Zn^2, Zj i.i.d. N(0,1)
Then (define) V~\Chi^2(n)

Fact \Chi^2(1) is Gamma(1/2,1/2)
So, \Chi^2(n) is Gamma(n/2,1/2) 

Student-t distribution (Gosset 1908)
Let T = Z/\sqrt{V/n}, with Z~N(0,1), V~ \Chi^2(n)
Then T~t_n 

Properties. 
1.Symmetric, -T ~ t_n 
2.n=1 ==> Cauchy, mean does not exist 
3.n>=2 ==> E(T) = E(Z)E(1/\sqrt{Vn})=0. 
E(Z^k) use MGF 
E(Z^{2n}) = E((Z^2)^n) Z^2 ~ Gamma(1/2,1/2)

4.Heavier-tail than Normal 
5.For n large, t_n looks very much like normal N(0,1)
distibution of t_n goes to N(0,1) when n--\inf 

Let T_n = Z/\sqrt{Vn/n} with Z1,Z2,... i.i.d. N(0,1)
Vn = Z1^2+Z2^2+...+Zn^2 Zj ~ N(0,1) i.i.d. v.r. 

Then Vn/n -->1 with probablity 1. by the law of large numbers. E(Z1^2) =1.  Then \sqrt{Vn\n} ---> 1 with prob. 1. 

So Tn --> Z with prob. 1. 

So tn converges to N(0,1)

-------------------------
#####Multivariate Normal distributioin (MVN)
Define. Random vector (X1,X2,...,Xk)=X is Multivariate Normal
if every linear combination t1X1+t2X2+...+tkXk is always normal. 

Ex. Let Z,W be i.i.d. N(0,1). Then (Z+2W,3Z+5W) is MV, since 
s(Z+2W)+t(3Z+5W) = (s+3t)Z+(2s+5t)W  is normal. 

Non-example 
Z~N(0,1), Let S be random sign, independent of Z, Then Z,SZ are marginally Normal. But the (Z,SZ) is not MVN. 
look Z+SZ 

MGF of X (MVN) is E(e^{t'*X}) 
t'X is a normal distribution 

Recall X~N(u,\sigma^2), E(e^{tX}) = e^{tu+1/2*t^2}
So, 
	E(e^{t'*X})  = e^{t'u+1/2*(t.*t)'{\boldsymbol{(sigma1^2)}


Theorem. Within MVN, uncorrelated implies independent. 
X = (X1,X2) MVN, if every component of X1 is uncorrelated with every component with X2. Then X1 is independent of X2. 
(independent==> uncorrelated but the reverse if not true)

Ex. 
Let X,Y i.i.d. N(0,1), Then (X+Y,X-Y) is MVN. 
uncorrelated Cov(X+Y,X-Y)=Var(X)+Cov(X,Y)-Cov(X,Y)-Var(Y)
   						 =0. 
So, X+Y and X-Y are independent.  
