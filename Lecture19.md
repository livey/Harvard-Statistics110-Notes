####Joint, conditional, marginal distribution 
1.joint CDF F(x,y) =P(X<=x,Y<=y) 
continuous case: f(x,y) = \partial F(x,y)/\partial x\partial y 
2.joint PDF  P((x,y) \in A) = \int\int_A f(x,y)dxdy
3.marginal PDF of X: \int_\-inf ^\inf f(x,y)dy 
4.conditional PDF of Y|X is 
f_{y|x}(y|x) = f_{x,y}(x,y)/f_x(x) = f_{x|y)(x|y)f_y(y)/f_x(x)

X,Y independent if f_{x,y}(x,y) = f(x)f(y) for all x,y. 

Unif. in a disc x^2+y^2<=1; f(x,y)=1/\pi.(x^2+y^2)<=1 this constrain is very important).  
f_x(x) = \int_{-\sqrt{1-x^2}^{\sqrt{1-x^2} 1/\pi dy = 2/\pi \sqrt{1-x^2}, -1<=x<=1; (the marginal is not uniform)
f_{Y|X}(y|x) = 1/\pi/{2/\pi \sqrt{1-x^2}}  if -\sqrt{1-x^2} <= y<= \sqrt(1-x^2) 
So Y|X ~ Unif(-\sqrt{1-x^2},  \sqrt(1-x^2)) 
and they are not independent. f_xf_y != f(x,y). 

#### 2-D LOTUS 
Let (X,Y) have joint PDF f(x,y), and let g(x,y) be a real valued of x,y. 
Then E(g(X,Y)) = \int\int g(x,y)f(x,y)dxdy 

###### If X, Y are independent, the E(XY) = E(X)E(Y) (independent implies uncorrelated) 
Proof( continuous case) E(XY) = \int\int xyf(x,y) dxdy =\int\int xyf(x)f(y)dxdy = E(X)E(Y). 

Ex. X,Y i.i.d. ~ Unif(0,1), find E(|X-Y|) =(LOTUS) \int\int |x-y|dxdy = \int_{x>y}(x-y) dxdy + \int_{y>x}(y-x)dxdy 
= 2\int_{x>y}(x-y)dxdy = 2\int_0^1 \int_y^1 (x-y)dxdy = 1/3. 

Let M= max(X,Y), L=min(X,Y). |X-Y| = M-L. 
E(M-L)= 1/3; E(M)-E(L) = 1/3; E(M+L) = E(M)+E(L) = E(X+Y) =1;  
E(M) = 2/3; E(L) = 1/3; 

##### Chicken-egg 
N ~ Pois(\lambda) eggs, each hatches will prob. p. Let X= number of hatch. so X|N = Bin(N,p). Let Y = number of don't hatch.
So X+Y = N. Find the joint PMF of X,Y. 
P(X=i,Y=j) = \sum_{=0}^\inf P(X=i,Y=j|N)P(N =n ) 
= P(X=i,Y=j|N=i+j)P(N=i+j) = P(X=i|N=i+j)P(N=i+j) = (i+j)!/i!/j!*p^i*q^{n-i}\lambda^{i+j}/(i+j)!*e^{-\lambda}
= e^{-\lambda*p}(p\lambda)^i/i!*(q\lambda)^j/j!*e^{-\lambda*q}
==> X,Y are independent, X~ Pois(p\lambda) Y~Pois(q\lambda) 



