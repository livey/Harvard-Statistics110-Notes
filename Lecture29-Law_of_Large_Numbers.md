Lecture29 Law of Large numbers 

Strong law of large numbers
Let X1,X2,...be i.i.d. mean \mu, Var \sigma^2
Let X_bar = 1/n\sum_j^n X_j (sample mean) 
Law of Large Numbers: X_bar -> \mu as n-->\inf with probability 1. 

It means the sample mean converge to it's true mean. 

Ex. Xj~Bern(p). then (X1+X2+...+Xn)/n --> p with prob. 1. 

(weak law of large numbers)
For any c>0, P(|X_bar-\mu|>c) -->0 as n-->\inf 

Proof. 
P(|X_bar-u|>c)<=Var(X_bar)/c^2=\sigma^2/n/c^2-->=0 

But what is the distribution of X_bar? 

Central Limit Theorem (assume \sigma is finite)
n^{1/2}(X_bar-u)/\sigma --> N(0,1) in distribution 

Equivalently: (\sum_j Xj-n*u)/\sqrt(n\sigma^2)-> ~ N(0,1)

Proof. assume MGF M(t) of X exist. 
Can assume u=0, \sigma= 1 since condisder 1/n\sum_j (X_j-u)/\sigma

Let Sn = \sum_j^n Xj, show MGF of Sn/\sqrt{n} goes to N(0,1) MGF. 

E(e^{sSn/sqrt{n}})=E(e^{tX1/sqrt(n)}...e^{tX_n/sqrt(n)})
=MGF(t/sqrt{n})^n 
Take log 
lim_{n-->\inf} lnM(t/sqrt{n})
		=lim_{n-->\inf} logM(t/\sqrt{n})/(1/n)	
		==(let y=1\sqrt{n}, then let y be real)
		=lim_{y-->0} logM(yt)/y^2
		=lim_{y-->0}tM'(yt)/(2yM(yt))
		=t/2*\lim_{y-->0} M'(yt)/y
		=t^2/2*lim_{y-->0}M''(yt)/1
		=t^2/2 
		which is the log of e^{t^2/2} is the MGF of N(0,1)




#####Binomial Approximated by Normal 
Let X ~ Bin(n,p), think of X = sum_j Xj, Xj ~ Ber(p) i.i.d.
P(a<=X<=b)\approx P((a-np)/\sqrt{npq}<=\frac{X-np}{\sqrt{npq}}<=\frac{b-np}{\sqrt(npq)})
          \approx F(\frac{b-np}{\sqrt(npq)}) -F((a-np)/\sqrt{npq})

Contrast with Pois approximation: n is large, p is small, \lambda = np. 
Normal approximation, n is large, p close to 1/2. 

Continuity Correction. 
P(X=a)=P(a-1/2<=X<=a+1/2)
