##Exponential Distribution 
with one rate parameter \lambda 
X~Expo(\lambda) has PDF \lambda e^{-\lambda x},x>0 (otherwise 0) 
CDF: F(x)= \int_0^x \lambda e^{-\lambda t) dt = 1-e^{-\lambda x ) ,x>0. 
Let Y=\lambda X , then Y~Expo(1), since P(Y<=y)= 1-e^{-y} 

Let Y~Expo(1) ,find E(Y) and Var(Y) 
E(Y) = \int_0^\inf ye^{-y} dy = 1 
Var(Y) = E(Y^2)-E(Y)^2 = \int_0^\inf y^2e^{-y}dy  -1 = 1. 
So X=Y/\lambda has E(X) = 1/\lambda , Var(X)= 1/\lambda^2. 

###Memoryless Property. 
P(X>=s+t|X>=s) = P(X>=t) 
Here P(X>=s)[survival function]  = 1-F_X (s) = e^{-\lambda s} 
     P(X>=s+t|X>=s) = P(X>= s+t ,X>=s) / P(X>=s) = e^{-\lambda s} 

X~ Expo(\lambda) 
E(X|X>a) = a+E(X-a|X>a) = a+1/\lambda by use memoryless property 
