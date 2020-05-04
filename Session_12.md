# Session 12

Suppose we have two possible actions $a \in {a_{1},a_{2}}$ and we want to predict the weather temperature $y_{n+1}$ and based on that we want to decide about the two following action. 

The pay of is only depends on the true value of some $L(a,y_{n+1})$

$a_{1}$: you do not buy extra cooling and you risk it

$a_{2}$: you buy the extra cooling 

![40](Picturs/pic_40.PNG)

Historical data on $y=y_{1},y_{2},...,y_{n}$. This is the history of the temperature in this example.

We want:

* probabilistic forcast of $y_{n+1}$

* use prediction to choose optimal $a^{*}$

What to do?

We want the probabilistic forcast, we want to know the distribution probability for $y_{n+1}$. 

Some times the pey off is not symmetric. If the tempreture is high, the loss is high. If the temprature is low, the loss is low.

Based on the loss function which action should be chosen?

$\hat{L_{emp}}=\frac{\sum_{i=1}^{n} (a_{1},y_{i})}{n}$

Define events:

$E_{1}={y|y_{n+1}	\le y_{int}}$   $a^{*}=a_{1}$    

$E_{2}={y|y_{n+1}\gey_{int}}$     $a^{*}=a_{2}$  

Want $Pr{E_{1}}=Pr{y	\le y_{int}}=\frac{\frac{1}{n}}{\sum_{y	\le y_{int}(1)}=p_{1}$ Estimate of Pr($E_{1}$)

If $\hat{L_{emp}} \ge c_{2}, then $a^{*}=a_{2}$


Given you have a hundered of the historical data and you are pretty confident about the loss function estimation. Now consider you have 6 of the historical data. 







