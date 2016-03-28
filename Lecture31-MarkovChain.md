####Lecture31 Markov Chains(example of stochastic process)
X0,X1,X2,...(think of Xn as a state of system at discrete time)

Markov property: 
P(X_{n+1}=j| Xn=i,X_{n-1}=in-1,...,X0=i0)
	=P(X_{n+1}=j| X_n=i)=q_{ij}(transition probablity)
past, future are conditioning independent give the current state. 

Transition matrix 
[]-very row sums to 1. 
(MCMC-markov chain monto carlo) 
 
Suppose at time n, Xn has distribution s(row vector 1xM matrix, PMF). 
P(X_{n+1})= \sum_i P(X_{n+1}=j| Xn=i)P(Xn=i)
		  =\sum_i s_i*q_{ij}  
s*Q^n n-step future probability 
P(X_{n+1}=j| Xn-i)=q_{ij} 
P(X_{n+2}=j| Xn=i)=\sum_k P(X_{n+2=j}|X_{n+1}=k,Xn=i)P(X_{n+1}=k|X_n=i)
		=\sum_k P(X_{n+2=j}|X_{n+1}=k)P(X_{n+1}=k|X_n=i)
		=\sum_k q_{ik}q{kj} is just the (i,j) entry of Q^2
P(X_{n+m}=j|X_n=i) = Q^m(i,j)


#####Stationary distribution. 		
s is stationary for the chain, if s*Q=s. 

Question: 
1.Does a stationary distribution exists?
2.Is it unique?
3.Does the chain converge to s?
4.How can we compute it? 
