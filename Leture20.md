#####Multinomial and Cauch 

Ex. Find the E(|Z1-Z2|), with Z1,Z2~(i.i.d.)N(0,1) 
Theorem X~N(u1,\sigma262), Y~N(u2,\sigma2^2) i.i.d. 
X+Y ~ N(u1+u2,\sigma1^2+\sigma2^2) 
Proof. use the MGFs: MGF of X+Y is 
e^{u1t+.5*\sigma1^2t^2*e^{u2t+.5*\sigma2^2t^2}=e^{(u1+u2)t+.5*(\sigma1^2+sigma2^2)t^2}. So, this ends of the proof. 

Note Z1-Z2 ~ N(0,2), E(|Z1-Z2|) = E(|sZ|) ,Z~ N(0,1) 
                                =sE(|Z|)= 2/\sqrt{\pi} 
  
####Multinomial distribution 
Define/Story of Mult(n,p), p=(p1,p2,...,pk) probability vector. p_j>=0,\sum P_j = 1; 
X~Mult(n,p), X=(X1,...Xk) if have n objects, independently putting into K categories. 
if p_j=P(category j) X_j = numbers of objects in category j. 
Joint PMF P(X1=n1,...,Xk=nk) =n!/(n1!*n2!*...*nk!)*p1^n1*p2^n2*...*pk^nk. if \sum nk=n; 

#######Property: 
marginal distribution 
X~ Mult_k(n,p). Find the marginal distribution of Xj
Then Xj~Bin(n,p_j) 
E(Xj) = np_j, Var(X_j) = np_j(1-pj) 
Lumping Property. X=(X1,...X10) ~Multi(n,(p1,...p10))
Let Y=(X1,X2,X3+X4+...+X10), Then, Y~Mult(n,(p1,p2,p3+p4+...+p10))
X~Mult(n,p). Then given X1=n1. (X2,X3,...,Xk)~Mult_{k-1}(n-n1,(q2,q3,..,q_k))
with q2 = P(being in category 2|not in category 1)
        =p2/(1-p1)=p2/(p2+p3+...+pk)
        qk=pk/(p2+p3+...+pk)
        
#####Cauchy Interview Problem
Cauchy distribution: X/Y with T=X,Y i.i.d. Normal. Find the PDF of T.
1.do not have a expectation, and do not have variance
2.average a lot of i.i.d. Ti, the distribution do not change 

P(X/Y<=t) = P(X/|Y|<=t) {from the semmytry of the normal}
          =P(X<=t|Y|)=\int_\-inf^\inf \int_{-\inf}^{t|y|} f(x,y)dxdy
          =\int_{-\inf}^\inf f(y) \Phi(t|y|) dy = \sqrt(2/\pi)\int_0^\inf e^(-y^2/2)\Phi(ty) dy 
<The PDF is the derivative of CDF. 
 F'(t) = \sqrt(2/\pi)\int_0^{\inf} e^{-y^2/2}*y*1/\sqrt(2\pi)e^(-t^2*y^2/2)
       = 1/\pi \int_0^\inf ye^{-(1+t^2)*y^2/2}dy 
       = 1/\pi*/(1+t^2) 
P(X<=t|Y|) =  \int P(X<=t|Y| | y)p(y) dy 
           = \int \Phi(t|y|)\phi(y) dy (P(X<=t|y|=\Phi(t|y|))
           
        
