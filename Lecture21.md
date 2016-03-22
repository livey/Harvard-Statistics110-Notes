Lecture21

#####Covariance and Correlation 
Define: Cov(X,Y) = E(X-EX)(Y-EY)=E(XY)-EX*EY 
Property 
1. Cov(X,X)=Var(X) 
2. Cov(X,Y)=Cov(Y,X)
3. C(X,c) = 0 is c is constant 
4. Cov(cX,Y)=c*Cov(X,Y)
5. Cov(X,Y+Z) = Cov(X,Y)+Cov(X,Z) 
(4,5) ba bilinearity 
6. Cov(X+Y,Z+W)=Cov(X,Z)+Cov(X,W)+Cov(Y,Z)+Cov(Y,W)
   Cov(\sum_i ai*X_i,\sum_j b_j*Y_j)=\sum_{i,j} a_i*b_j*Cov(X_i,Y_j)
7. Var(X1+X2)= Var(X1)+Var(X2)+2Cov(X1,X2)
  (if X1 and X2 is independent, then Var(X1+X2)=Var(X1)+Var(X2))
   Var(X1+...+Xn)=\sum_n Var(Xn)+2\sum_{i<j} Cov(X_i,Xj) (notice i<j )

Theorem: if X,Y are independent, then ther're uncorrelated. Cov(X,Y)=0

Coverse is false: e.g. Z~N(0,1), X=Z, Y = Z^2. 
Cov(X,Y)=E(XY)-E(X)E(Y) = E(Z^3)-E(Z)E(Z^2) = 0. 
Ther're very dependent: Y is a function of X, and Y determines the 
magnitude of X. 

Correlation: 
Corr(X,Y)=Cov(X,Y)/(SD(X)SD(Y))=Cov((X-E(X))/SD(X),(Y-EY)/SD(Y))
Treat (X-EX)/SD(X) as standarlization 
Theorem: -1<=Corr(X,Y)<=1(form of Cauchy-Schwartz) 

Proof: WLOG assume X,Y are standardize Let Cov(X,Y)=\rao
Var(X+Y)=V(X)+V(Y)+2Cov(X,Y) =2+2\rao
Var(X-Y)=Var(X)+Var(Y)-2Cov(X,Y) = 2-2\rao 
so : 2+2\rao>=0 2-2\rao >=0; 

Cov(X,Y) , Mutinomial 
(X1,X2,...,Xk)~ Mult(n,p)
Find Cov(Xi,Xj) for all i,j 

If i=j, Cov(Xi,Xj)=Var(Xi)= np_i(1-p_i)

Now i !=j 
Find Cov(X1,X2)=c 
Var(X1+X2) = Var(X1)+Var(X2)+2c = np_1(1-p_1)+np_2)(1-p_2)+2c 
Var(X1=X2) = n(p1+p2)(1-p2-p1) 

So, c = -n*p1*p2

General Cov(Xi,Xj)= -n*pi*pj  for i~= j 

Ex. X~Bin(n,p), write as X= X1+x2+...+Xn, Xj~Bern(p)

Let I_A,I_B indicate r.v. of event A 
I_A^2 = I_A 
I_A^3 = I_A 
I_A*I_B = 
I_{A\interB} 

Var(Xj)=E(Xj^2)- E(Xj)^2 =E(Xj)-E(Xj)^2=p-p^2 
so V(X) = npq 

Ex. X~ HGeom(w,b,n) 
X= X1+X2+...+Xn, Xj={1, if j'th ball is white; 0 , otherwise}
Var(X)= nVar(X1)+ 2(n,2)*Cov(X1,X2) 
Cov(X1,X2)=E(X1X2)-EX1EX2 =(2/(w+b)*(w-1)/(w+b-1))-w/(w+b)*w/(w+b)






