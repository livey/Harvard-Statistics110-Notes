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
Def. A r.v. X has MGF M(t) = E(e^{tx}) as a function of t, if this is finite on some 

