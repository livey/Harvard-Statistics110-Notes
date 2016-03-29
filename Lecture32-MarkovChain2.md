####Lecture32 Markov Chain 2 
.Chain is irreducible if possible(with probability) to get from anywhere to anywhere. 
.A state is recurrent if starting there, chain has probability 1 of returning to that state. Otherwise, it is called transient. 
.absorbing 
.periodic Chain 

s (probability row vector) is stationary for a chain qith transition matrix Q. 
if sQ=s. 

Theorem: For any irreducible Markov Chain(with finite many states) 
1.A stationary s exists. 
2.It is unique. 
3.si=1/ri, where ri is average time to return if the chain starts at i. 
4.If Q^m is strictly positive for some m, then P(Xn=i)->si as n-->\inf, tQ^n-->s (t is a probability vector)

####Reversible Markov Chains 
Def. Markov chain with transition matrix Q is reversible if there is a probability vector s such that s_i Q_{ij} = s_{j}q_{ji} for all state i,j. 

Theorem: If reversible with respect to s, then s is staionary. 

Proof: Let s_iq_{ij} = s_jq_{ji} for all i,j, show sQ=s. 
\sum_i s_i*q_{ij} = \sum_i s_j*q{ji}= s_j*\sum_i q_{ji}=sj 
which implies sQ =s. 

#####Random walk on an Undirected Network. 
Let d_i be degree of i'th node. 
Then d_i q_{ij} = d_jq_{ji} for all i,j. 
Let i~=j. q_{i,j} q_{j,i} are both zero, or both not zero. 
If {i,j} is on edge then q_{ij}= 1/d_i. 
So, with M nodes 1,2,...,M degree are di. Then, s , si=di/(\sum_i di). So, s is the sationary distribution probability. 
