#####Beta distribution 
Beta(a,b), a>0,b>0. 
PDF: f(x)=c*x^{a-1}(1-x)^{b-1}
flexible family of continuous distribution on [0,]
1.a=b=1; uniform distribution 
2.a=2,b=1; f(x)=c*x is linear function 
3.a=b=1/2; it is a "U" shape. 
4.a=b=2;   it is a upsidedown 'U' shape 
5.often used as prior for a parameter in (0,1)
6.conjugate prior to the Binomial 
7.connnections to other distribution 

######Conjugate prior for Binomial 
X|p ~ Bin(n,p) 
p ~ Beta(a,b)-[Prior]
Find the posterior distribution p|X 
f(p|X=k) = P(X=k|p)f(p)/P(X=k) [P(X=k) does not depend on p]
         = c*(n,k)p^k(1-p)^{n-k}p^{a-1}(1-p)^{b-1}
         ~ Beta(k+a,n-k+b)

so f(p|X) = Beta(X+a,n-X+b)    

#####Find \int_0^1 x^k(1-x)^{n-k}dx without using caculus,using a story(Byes' Billballs) 

int_0^1 (n,k)*x^k(1-x)^{n-k}dx 
n+1 billiarballs, all white, paint one pink, throw them on[0,1] down. 

Fisrt throw, then paint pink. 
Let X = number of balls that are pink. 
P(X=k)=\int_0^1 P(X=k|p)f(p)dp 
=\int_0^1 (n,k)p^k(1-p)^{n-k}dp= 1/(n+1) 

#####Stat 123. Applied Quant Finance on Wall Street, Financial Deravative 

S_T(Stock) g(S_T) E[g(S_T)] 
one is 1.25, the other is 0.8 
E(*) = 1.02 
