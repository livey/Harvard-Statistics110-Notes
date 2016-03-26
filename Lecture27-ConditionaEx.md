Lecture27 Conditional Expectation 

Ex. Let X~ N(0,1), Y=X^2. Then E(Y|X)=E(X^2|X)=X^2=Y 
E(X|Y)=E(X|X^2) = 0. since if observe a=X^2, then X = +-\sqrt(a), they equally likely. 

Ex. Stick break off random piece, break off another piece. 
X~ Unif(0,1), Y|X ~ Unif(0,X). 
E(Y|X=x)= x/2, so E(Y|X) = X/2, E(E(Y|X))=1/4 = E(Y). 

#####useful Properties 
1.E(h(X)Y|X) = h(X)E(Y|X)[taking out what's known] 
2.E(Y|X) = E(Y), if X,Y are independent. 
3.E(E(Y|X)) = E(Y) ---Iterated Expectation/ Adom's law. useful E(Y) = E(E(Y|X)). 
4.E((Y-E(Y|X))h(X)) = 0. Y-E(Y|X) (residual) is uncorrelated with h(X). Cov(Y-E(Y|X),h(X)) = E(Y-E(Y|X)h(X))^2 - E^2(Y-E(Y|X)h(X)) and E(Y-E(E|X))=0. 

Y r.v. <X,Y> =E(XY), this means in this product, Y-E(Y|X) is appendix to h(X). E(Y|X) is a functtion of X.

Proof (4).   E(Yh(X)) - E(E(Y|X)h(X))	
		=E(Yh(X)) - E(E(h(X)Y|X))
		=E(Yh(X)) -E(Yh(X)) = 0 
Proof.(3) [discrete case] 
Let E(Y|X) = g(X). 
E(g(X)) = \sum_x g(x)P(X=x)=\sum_x E(Y|X=x)P(X=x) 
		=\sum_x \sum_y y*P(Y=y|X=x)P(X=x)	
		= \sum_x \sum_y y*P(Y=y,X=x) 
		=\sum_y y*P_Y(Y=y) 
		=E(Y) 

Define Var(Y|X) = E(Y^2|X) - E^2(Y|X)
 				= E((Y-E(Y|X))^2|X) 
 				
5.Var(Y) = E(Var(Y|X))+Var(E(Y|X))(EvE's Law)		

Ex. Pick random city, pick random sample of people in that city. 
X = number of people with disease 
Q = proportion of people in random city with disease. 

Find E(X), Var(X), assuming Q ~ Beta(a,b) X|Q~ Bin(n,Q) 
E(X)= E(E(X|Q)) = E(nQ) = nE(X) = na/(a+b). 
Var(X)  = E(Var(X|Q))+ Var(E(X|Q))
		=E(nQ(1-Q))+ Var(nQ)
		=n*a*b/(a+b+1)/(a+b)
		
Ex. Store with a random number of customers N=number of customers. 
Let Xj be the amount of j'th customers spends, Xj has mean \mu, Var \sigma^2 
assume N,X1,X2,...,XN are independent. 
Find the mean and var of X = \sum_j^N Xj 

E(X) = \sum_{n=0}^\inf E(X|N=n)P(N=n) = \sum_0^\inf \mu*n*P(N=n) = \mu*E(N)

E(X) = E(E(X|N)) = E(N*\mu) = E(N)*\mu  
Var(X)  = E(Var(X|N)) + Var(E(X|N)) 
		= E(N\sigma^2) + Var(N*\mu)
		= \sigma^2*E(N) + \mu^2*Var(N)
