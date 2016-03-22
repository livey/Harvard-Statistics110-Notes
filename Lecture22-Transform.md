Lecture22 

Variance of HyperGeometric(w,b,n),
p = w/b. w+b = N; 
Var(\sum X_j) = \sum_j Var(Xj)+2*\sum_{i<j}Cov(Xi,Xj)
= \sum_i Var(Xi) = 2(n,2)Cov(X1,X2) 
=np(1-p)+2(n,2)* (w/(N)*(w-1)(N-1)-p^2) 
= (N-n)/(N-1)np(1-p)

Extreme cases: n =1; 
N is much larger than n. 
Var(X) = np(1-p) 

#####Transformations
Theom. Let X be a continuous r.v. with PDF fx,Y=g(X) 
g is differentiable, g is strictly increase. 
Then the PDF of Y. 
f_Y(y)=f_X(x)dx/dy where y=g(x). 
and this is written in terms of y. 

Also dx/dy = (dy/dx)^(-1)

Proof. 
CDF of Y is P(Y<=y)=P(g(X)<=y) 
                   = P(X<=g^{-1}(y))
                   = F_X(g^{-1}(y))
                   = F_X(x)
f_Y(y)= f_X(x) dx/dy. (Chain rule)

Example log Normal Y= e^Z, Z ~ N(0,1)

f_Y(y) = 1/sqrt{2\pi}e^{-(lny)^2/2}/y  
dy/dz = e^z = y 


######Transformation of multidimension, 
Y=g(X), g: R^n->R^n 
joint PDF of Y is f_Y(y) = f_X(x)*|dx/dy| 
|dx/dy|----Jocobian
dx/dy=[dx1/dy1,dx1/dy2,...,;dx2/dy1,dx2/dy2,....]
abs means the determinant of Jocobian 
|dy/dx|^{-1}=|dx/dy| 

#######Convolution(sum) T=X+Y 
discrete case 
P(T=t) = \sum_x P(X=x)P(t=y-x)
continuous case 
f_T(t) = \int f_x(x)f_Y(t-x)dx 
since F_T(t) = P(T<=t) = \int P(X+Y<=t|X=x)f(x)dx 
\int F_Y(t-x)f_X(x)dx 

#####Idea: prove existence of objects with desired property A
using prob. 

Show P(A)>0 for a random object. 
Suppose each object has a 'score'. Show there is an object with 'good' score 
There is an object whose score is at leat E(X) score of random object. 

Ex. 100 people, 15 committees of 20; ench person is on 3 committee. Show there exist 2 committee overlap >=3. 
Idea is find average overlap of 2 random committees. 
E(overlap) = 100*(3,2)/((15,2)) = 20/7. 
=> there exits pair of committes overlap of >=20/7. 
have overlap >=3. 






















