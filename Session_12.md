# Session 12

Suppose we have two possible actions $a \in {a_{1},a_{2}}$ and we want to predict the weather temperature $y_{n+1}$ and based on that we want to decide about the two following action. 

The pay of is only depends on the true value of some $L(a,y_{n+1})$

$a_{1}$: you do not buy extra cooling and you risk it

$a_{2}$: you buy the extra cooling 

![40](Picturs/pic_40.png)

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

Need some model of the data generating process

$y_{i}=y_{0}+	\varepsilon_{i}, 	\varepsilon_{i}\sim N(0,\sigma^{2}_{y})$

![41](Picturs/pic_41.png)

Here, the mean and variance are unknown.  

Equavalently $y_{i}\sim N(y_{i},\sigma^{2}_{y}})$

We need to find the distribution of the loses over the different actions. To do that, we need the distribution of the $y$

Want the probability forcast of $y_{n+1}$

To get it, estimate the $y_{0},\sigma^{2}_{y}}$ from $y_{1},y_{2},...,y_{n}$

There is multiple ways to do that 

Standard approach: OLS

mean: min_{\hat{y_{0}}}\sum(\hat{y_{0}}-y_{i})^{2}=\sum()\hat{varepsilon_{i}}^{2}

So, we will get the $y_{0},\sigma^{2}_{y}$

![42](Picturs/pic_42.png)

This is the the distribution y. This  describes the probaboloty forcast over the nest value of the y. With using it we can get the probability forcast for losses.

Suppose, you plot your estimated errors $\hat{varepsilon_{i}}=y_{i}-\hat{y_{0}}$

![43](Picturs/pic_43.png)

The varianvce of the error tends to be growing. It violates the assumption of the indipendent identically distribution. This is called heterokedasticity. 
When you work with data, you need to look at your data. 
Sometimes, the decision is not big deal and you live with this. In overal, if heterokedasticity happenes, we would have the wrong estimate of probabilities.

















