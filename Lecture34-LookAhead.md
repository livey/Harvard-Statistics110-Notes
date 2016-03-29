Lecture34 Look Ahead 
1.Conditioning 
2.Symmetry 
3.r.v.s and their distributions
4.stories 
5.Linearity 
6.indicator r.v.s
7.LOTUS
8.Law of Large Numbers
9.Centrial Limited Theorem
10.Markov Chain

1-5 what is randomies, uncertainty 
6-7 computing averages
8-10 long run behaviors 

Linear regression case
Y=b0+b1*X+e 
E(e|X) = 0; 
Cov(Y,X) = Cov(b1*X,X)+Cov(e,X)
		 =b1*Var(X)
==> b1=cov(X,Y)/Var(X). 

####Recommended Book: Mostly Harmless Econometrics 

Indicator variable, Howtz Thompson,inverse prob. 
the values y1,y2,...,yN treated as fixed 
sample of size n. Try to estimate the \sum_i yi 
prob. that person j is in the sample is Pj(know) 	 
Let (x1,z1),...,(xn,zn) be data. 
with xj is the y value, z_j is the ID number. 
\sum_{j=1}^n x_j/p_{zj} is unbiased. 
\sum_{j=1}^n x_j/p_{zj}= \sum_{j=1}^N yj/pj*Ij, where Ij is the indicator of j'th perons being in the sample. 
Expacted value: \sum_{j=1}^N pj*yj/pj = \sum_j yj 

Is it good? 
Ex. Basu's Elephant 

Bayesian's Frequency 
