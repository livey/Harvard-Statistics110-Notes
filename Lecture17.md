Memoryless property of exponential distribution 
E(T|T>20) > E(T) 
If memeryless, we would have E(T|T>20)  = 20 + E(T). 

####Theorem If X a positve valued r.v. with memeryless property, then:
X~ Expo(\lambda), 

Proof.
Let F be the CDF of X, G(x) =P(X>x) = 1-F(x) 
memoryless property is G(s+t) = G(s)G(t) ( Because P(X>=s+t|X>=t) = P(X>=s) ==> P(X>=s+t) = P(X>=s)P(X>=t) 

we should prove only exponential distribution will satisfy that equation. 
With that equation, we solve for G. 

Let s=t. => G(2t) = G(t)^2, G(3t) = G(t)^3, ...., G(kt)= G(t)^k
G(t/2) =\sqrt{G(t)}, ... , G(t/3)=G(t)^{1/3}, 
G(m/n*t) = G(t)^{m/n}. So, by continuty, G(xt)=G(t)^x for all raeal x>0. 
Let t=1; G(x) = G(1)^x= e^{xlnG(1)} 
let lnG(1) =-\lambda, So, G(x) = e^{-\lambda x}

####Moment generating function (MGF) 
Def. A r.v. X has MGF M(t) = E(e^{tx}) as a function of t, if this is finite on some interval (-a,a),a>0. 
why it is called Moment generating ? 
E(e^{tx}) = E(\sum x^n*t^n/n!) =\sum E(x^n)t^n/n! 

####Why GMf is important? X has MGF M(t) 
1. The n'th moment, E(x^n), is coeficient of t^n/n! in Taylor series of M(). M^(n)(0) = E(x^n). 
2. MGF determines the distribution, i.e if X,Y have the same MGF, then have the same CDF, thus PDF. 
3. If X has MGF M_x, Y has MGF_y ,the are i.i.d, then MGF of X+Y is E(e^{(X+Y)t)=E(e^(tX))E(e^(tY))=M_x*M_y. 

Ex. X~Ber(p), so M(t) = pe^t+q. 
X~Bin(n,p) ==> M(t)=(pe^t+q)^n. 

Z~N(0,1), ==> M(t) = \sum e^{tz}p(z) dz = e^{t^t/2}/sqrt{2\pi} 

####Paplace Rule of Succession 
Given p, assume X1,X2,..., i.i.d. Bern(p). 
p is unknown. Bayesian: treat p as a r.v. 
Let p~Unif(0,1),(prior). Let Sn=X1+X2+...+Xn. 
So Sn~Bin(n,p), p~U(0,1). Find the posterior distribution 
Compute p|Sn and P(X_{n+1} | Sn=n) ?
f(p|S_n=k) = P(S_n=k|p)f(p)/(P(S_n=k) [P(S_n=k) does not depend on p]
[ P(S_n=k)= \int_0^1 P(Sn=K|p)f(p)dp ]
\approx p^k*(1-p)^(n-k) 
f(p|Sn=n) = (n+1)p^n (according to f(p|Sn=k) \approx p^k*(1-p)^(n-k) )
P(X_{n+1}=1|S_n = n) = \int_0^1 (n+1)p*p^n dp = (n+1)/(n+2) 
if the sun rose in the last n days, so it will rise with probablity (n+1)/(n+2) 
