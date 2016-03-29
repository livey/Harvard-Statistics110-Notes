####Lecture33 Markov Chain 3 
w_{ij}>=0 if there is an edge, w_{ij}=0 if no edges. w_{ij}=w_{ji}. 
Random walk: from state i, go to j with probability \propto w_{ij}. 
If {i,j} is an edge, then q_{ij}=w_{ij}/\sum_k w_{ik}
Note: \sum_k q_{ik}=w_{ij}=w_{ji} = \sum_k w_{jk}
==> si \propto \sum_k w_{ik}

Let w_{ij}=si q_{ij} = s_j q_{ji}=w_{ji}

P(X_{n+1}=j| X_n=i)=w_{ij}/\sum_k s_i*w_{ik}=si*q_{ij}/\sum_k s_j*w_{jk}= s_j 

#####non-reversible example: Google PageRank. 
WWW  Importance of page linking to it and their importance. 
s_j= \sum_i s_i q_{ij} q_{ij}
s = s*Q. whic says s is stationary distribution of random web surfing chain. (if s is normalized)

G= \alpha*Q + (1-\alpha)*J/M, where M is the nubmer of pages.
J = ones(M) 0<\alpha<1 
J/M -- teleportion, give a random page. 
no zeros in transition matrix G 
use convergence to stationarity! 

Let t be initial prob. vector. 
t*G = \alpha*t*Q +(1-\alpha)*t*J/M. (Q is a very sparse matrix) 
    t*J =ones(1,M)

t*G*G = t*G^2, t*G^3,...,t*G^n will converge to stationary state. 
