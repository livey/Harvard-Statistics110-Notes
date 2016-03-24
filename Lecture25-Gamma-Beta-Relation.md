####Lecture25 
######Order Statistics and 
Connect Beta and Gamma distribution. Find the constant of Beta distribution 

######Bank-post office example X~Gamma(a,\lambda)---wait at bank, Y~ Gamma(b,\lambda)---wait at post office. They are independent. 

Find the distribution of X+Y=T. (T ~ Gamma(a+b,\lambda)). X/(x+T) = W. Find the joint distribution of (T,W). Let \lambda = 1 to simplify. 

Joint PDF f_{T,W}(t,w)  = f_{X,Y}(x,y)|d(x,y)/d(w,t)|
						= 1/(\Gamma(a)\Gamma(b)) x^a*e^{-x}y^be^{-y}1/x*1/y*(|w,t;1-w,-t|=)t
						= 1/(\Gamma(a)\Gamma(b))w^{a-1}*(1-w)^{b-1}*t^{a+b}e^{-t}/t 
						=f_W(w)f_T(t)
f_W(w)= \Gamma(a+b)/\Gamma(a)/\Gamma(b)w^(a-1)(1-w)^(b-1)
      =Beta(a,b)
f_T(t)= Gamma(a,b,1) 

know the nomalization const. of Beta(a,b) 

Find the expected value of W ~ Beta(a,b) 
1.LOTUS E(W)=a/(a+b)
2.E(W)= E(X/(X+Y)) = E(X)/E(X+Y)=a/(a+b)[here the equality holds because of special conditions] 
Why it is true? 
E(X/(X+Y)E(X+Y)= E(X) in this special problem of Gamma-Beta ?
X/(X+Y) is independent of X+Y ===> there are uncorrelated. 

#####Order Statistics 
Let X1,...,Xn are i.i.d. The orer statistics are 
X(1)<=X(2),...,<=X(n), where X(1)=min(X1,X2,...,Xn)
X(n)=max(X1,...,Xn). 

e.g. if n is odd, the midiem is X(n+1/2). Get other 'Quantiles'. 
Difficult since dependent. 
Tricky in discrete case becase of 'ties'. 
Let X1,...,Xn be i.i.d. with PDF f, CDF F. Find the CDF and PDF of X(j). 
CDF:
X(X(j)<=x) = P(at least j of Xi's are <=x) 
				=\sum_{k=j}^n F(x)^k*(1-F(x))^(n-k)

PDF:
f_{x(j)}(x)dx = n*(n-1,j-1)F(x)^{j-1}(1-F(x))^{n-j} f(x)dx 
so. f_{x(j)}(x)=n*(n-1,j-1)F(x)^{j-1}(1-F(x))^{n-j}f(x)

#######Ex.
U1,U2,...,Un i.i.d Unif(0,1)
f_{U(j)}(x)=n*(n-1,j-1)*x^{j-1}(1-x)^{n-j}, for 0<x<1 

===> U(j)~ Beta(j,n-j+1) 

######Conditional Expectation 
E(X|A) 
E(X)=E(X|A)P(A)+E(X|A^c)P(A^c)
E(X)= \sum_x x*p(X=x) 
    =\sum_x x*(P(X=x|A)*P(A)+P(X=x|A^c)*P(A^c))
    =P(A)*\sum_x x*P(X=x|A)+P(A^c)*\sum_x P(X=x|A^c)
    =P(A)*E(X=x|A)+P(A^c)*E(X=x|A^c)

Two Envelope Paradox 
one envelope contains twice as much as other one. 

<img src="http://chart.googleapis.com/chart?cht=tx&chl=\lambda" style="border:none;">










