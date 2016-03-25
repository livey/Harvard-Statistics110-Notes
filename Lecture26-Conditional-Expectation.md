Lecture26 Conditional Expectation

#####Two Envelope Paradox one envelope contains twice as much as other one.

X dollor in one box, and the other has Y dollors. X = 2Y. 
Argument1: E(Y)=E(X) by symmetry. 
Argument2: E(Y) = E(Y|Y=2X)P(Y=2X)+E(Y|Y=X/2)P(X=Y/2) 
				!= E(2X)*.5+.5*E(X/2)= 5/9*E(X) 
				=E(2X|Y=2X)*.5+E(X/2|Y=X/2)*0.5 
E(Y|Y=2X) != E(2X) 
Let I be indicator of Y = 2X. then X,I are dependent. 

#####Patterns in coin flips. 
Repeated fair coin flips. 
How many flips until HT? (HH?) Find E(W_ht) E(W_hh) 

E(W_ht) = E(W1)+E(W2) = 4; 
E(W_hh) = E(W_hh|first toss H)*.5+E(W_hh|first toss T)*.5 
 		= (2*.5+(2+E(W_hh))*.5)*.5    +(1+E(W_hh|))*.5 

=====> E(W_hh) = 6. 

ted.com Peter Donnell 

E(Y|X=x) = \sum y*P(Y=y|X=x) 
E(Y|X=x) = \int y*f(y|X=x)dy =) \int y*f_{x,y}(x,y)/f_x(x) dy 

Let g(x) = E(Y|X=x) 
Then define E(Y|X)=g(X) 
e.g. if g(x)=x^2, then g(X)=X^2 
So E(Y|X) is a r.v., function of X. 

Ex. X,Y ~ i.i.d. Pois(\lambda) 
E(X+Y|X) E(X|X)+E(Y|X) = X + \lambda 
E(h(X)|X) = h(X) 

E(X|X+Y), Let T=X+Y, Y = T-X. Find the conditional PDF. 
P(X=k|T=n)  = P(T=n|X=k)P(X=k)/P(T=n) 
			= P(Y=n-k|X=k)P(X=k)/P(T=n) 
			=e^{-\lambda}\lambda^{n-k}/(n-k)!*e^{-\lambda}\lambda^{k}/k!/(e^{-2*\lambda}*(2*\lambda)^n/n!) 
			=(n,k)1/^n 
X|T=n ~ Bin(n,1/2) 
E(X|T=n) = n/2. ===> E(X|T)= T/2. 

E(X|X+Y) = E(Y|X+Y) by symmetry(becuase of i.i.d.) 
E(X|X+Y)+E(Y|X+Y) = E(X+Y|X+Y)=X+Y. 
E(X|T) = T/2. 

Key property: iterated Expectation(Adom's Law) 
E(E(Y|X))= E(Y)

