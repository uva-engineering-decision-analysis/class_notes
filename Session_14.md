# Session 14

In the example which was presented in the previous session, suppose we have historical data. 

Suppose we know the tru average and standard deviasion. Suppose we have 20 historical data points. 
It is limitted data.

![49](Picturs/pic_49.png)

![50](Picturs/pic_50.png)

In the above graph, you might think that the estimted average is higher than the actual average.

![51](Picturs/pic_51.png)


The estimated average and standard deviasion are quite higher than the actual ones. 

![52](Picturs/pic_52.png)

In this case, the decision maker who rely on this model is  actually overestimating the risk.

Suppose you have a forcasting system,

![53](Picturs/pic_53.png)

Instead of relying on historical data, suppose that we have forcasting system. Also, suppose the system is bias and it tends to be low.

![54](Picturs/pic_54.png)

It is linear regression that looks at focast against the observations.

Next, we are going to figure out if you have the forcating system available, then what is the value of this forcasting system in providing information and delivering better decision.

$y_{1},y_{2},...,y_{n}$     historic observations

$x_{1},x_{2},...,x_{n}$     historic forcasts

1- Estimate the model without the forcast

$y_{i}=\theta+\varepsilon_{i}$

$\hat{\theta}=\frac{\sumy_{i}}{n}=\bar{y}$

$\hat{\varepsilon_{i}}=y_{i}-\bar{y}$

$s^{2}=\frac{\sum(\varepsilon^{2}_{i})}{n-1}$

$Y_{n+1}=N(\hat{\theta},s^{2})$

$E[L(Y|a=no insurance)|\hat{\theta},s^{2}]=E.L.$

$E.L.\ge cost of insurrance$

Here, $\hat{\theta},s^{2}$ estimated with error. Therefore, If you do not handle them properly, you will get the error wrong.

If your model mis-spessifies the original data generative process, you will also have the mis-specification of your actual risk and it may lead to the wrong decision. 










