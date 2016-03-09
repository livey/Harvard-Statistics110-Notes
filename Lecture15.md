##Midterm review 
###Coupon collector(toy collector) 
n toy types, equally likely, 
find the expected  time T (# of toys) until you have the complete set. 
T=T1+T2+...+Tn, 
T1= time until 1st new toy = 1;
T2=additonal time until the 2st new toy
T3=.......

T1= 1 ;
T2-1 ~ Geom((n-1)/n),...
Tj-1 ~ Geom((n-(j-1))/n),
E(T)=E(T1)+E(T2)+...+E(Tn) 
    = 1+ n/(n-1)+...+ n/1 = n(1+1/2+1/3+...+1/n) 
    \approx nln(n) for large n 
    



