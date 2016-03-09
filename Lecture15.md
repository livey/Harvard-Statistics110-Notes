##Midterm review 
###Coupon collector(toy collector) 
n toy types, equally likely, 
find the expected  time T (# of toys) until you have the complete set. 
T=T1+T2+...+Tn, 
T1= time until 1st new toy = 1;
T2=additonal time until the 2st new toy
T3=.......

T1= 1 ;
T2-1 ~ Geom((n-1)/n),...
Tj-1 ~ Geom((n-(j-1))/n),
E(T)=E(T1)+E(T2)+...+E(Tn) 
    = 1+ n/(n-1)+...+ n/1 = n(1+1/2+1/3+...+1/n) 
    \approx nln(n) for large n 
    
##Unersality 
X~F(CDF) F(X)~Unif(0,1) 

###Ex. Logistic distribution: 
F(x) = e^x/(1+e^x); 
How to simulate this distribution, 
1. U~ Unif(0,1) consider F^{-1}(u) =ln (u/(1-u)) 

###Symmetry 
Let X,Y,Z be i.i.d. positive r.v.s Find E(X/(X+Y+Z)) ? 
By symmetry E(X/(X+Y+Z))=E(Y(X+Y+Z))=E(Z/(X+Y+Z)). 

So, E(X/(X+Y+Z))+E(Y(X+Y+Z))+E(Z/(X+Y+Z))=E((X+Y+Z)/(X+Y+Z))=1 
So, E(X/(X+Y+Z)) =1/3; 

###LOTUS 
U~Unif(0,1), X=U^2, Y=e^X, find E(Y) as an integral ? 
E(Y) = \int_0^1 e^x f(x)dx 

The better way: E(Y) = E(e^{U^2}) = \int_0^1 e^{u^2}f(u)du 

X~Bin(n,p), Find the distribution of n-x?
P(n-X=k)=P(X=n-k) =(n,n-k)p^{n-k}q^k =(n,k)q^k p^{n-k} 

Use story n-X~ Bin(n,q) by swap success and failure 

###Poisson problem
number of emails I get in time t is distributed Poisson(t\lambda) 
Find the PDF of T, time of the first email come. CDF?
P(T>t) ( in time(0,t) there is no email) = P(N_t=0) (with Nt= nubmer of emails in [0,t])
=e^{-t\lambda}(t\lambda)^0/0! = e^{-t\lambda} 
So, the CDF is 
F(t) = 1-e^{-t\lambda}, t>0 








