# Session 14

In the example which was presented in the previous session, suppose we have historical data. 

Suppose we know the true average and standard deviation. Suppose we have 20 historical data points. 
It is a limited amount of data.

![1](Picturs/pic_49.PNG)

![2](Picturs/pic_50.PNG)

In the above graph, you might think that the estimated average is higher than the actual average.

![3](Picturs/pic_51.PNG)


The estimated average and standard deviation are quite higher than the actual ones. 

![4](Picturs/pic_52.PNG)

In this case, the decision-maker who relies on this model is overestimating the risk.

Suppose you have a forecasting system,

![5](Picturs/pic_53.PNG)

Instead of relying on historical data, suppose that we have a forecasting system. Also, suppose the system is biased and it tends to be low.
![6](Picturs/pic_54.PNG)

It is a linear regression that looks at forecasts against the observations.

Next, we are going to figure out if you have the function system available, then what is the value of this forecasting system in providing information and delivering a better decision.

$y_{1},y_{2},...,y_{n}$     historic observations

$x_{1},x_{2},...,x_{n}$     historic forecasts

#### 1- Estimate the model without the forecast

$y_{i}=\theta+\varepsilon_{i}$

$\hat{\theta}=\frac{\sum y_{i}}{n}=\bar{y}$

$\hat{\varepsilon_{i}}=y_{i}-\bar{y}$

$s^{2}=\frac{\sum(\varepsilon^{2}_{i})}{n-1}$

$Y_{n+1}=N(\hat{\theta},s^{2})$

$E[L(Y|a=no insurance)|\hat{\theta},s^{2}]=E.L.$

$E.L.\ge cost of insurrance$

Here, $\hat{\theta},s^{2}$ estimated with error. Therefore, if you do not handle them properly, you will get the error wrong.

If your model mis-specifies the original data generative process, you will also have the mis-specification of your actual risk and it may lead to the wrong decision. 

living with some kind of misspecification might be fine, depending on the application.

#### 2- Estimate w/ forecasts, what is the expected value of information?

Now the question is how much better your decision is going to be if you have a predictive model that helps inform the decision. It might have some signal that may be is not perfect because it is only information. Then, on average how much loss you avoid compare to if you made otherwise the same decision-making process but without the predictive model. The information is valuable if it leads you to the different decision that you would not have mad otherwise. 

If you have a forecast, the forecast depends on the signal you may receive. Therefore,

$a^{*}=a^{*}(x)$

How to use the forecast?

Method:

$y_{i}=\beta_{0}+\beta_{1}x_{i}+u_{i}$   $u_{i}\sim N(0, \gamma^{2})$ i.i.d

Use OLS (or your preferred technique), to estimate parameters.


You can use the maximum likelihood here, too. It will give you a biased estimator that has a smaller variance.

estimate $\hat{\beta_{0}},\hat{\beta_{1}}, \hat{\gamma^{2}}$

Generate the predictive distribution of Y|X. 

Suppose we make the best linear fit. Then, we have now condition information for the given y's and therefore with some estimate of distribution, you can map that distribution to the distribution of the losses.  The loss distribution will have a heavyweight on zero and then increasingly less and less weight on higher levels of loss. If there is a minimum threshold, all of the values before the threshold in the first graph (normal distribution) will map to a loss equal to zero, and above that they all map to higher and higher losses but with less and less probability. Here, we do not have any forecasting information. 

![7](Picturs/pic_55.PNG)

But the idea here is instead of getting the forecast, you can have for some given x values, the distribution of the Y|x which is much sharper. Then, you can map that conditional distribution. The conditional distribution will have again heavyweight on zero but much sharper distribution, in comparison to the previous graph. 

![8](Picturs/pic_56.PNG)

Then given the above distribution of loss, 

E[L(Y|X)]=E.L.(x)

For any given x,

Let $a^{*}(x)=argmin {E.L.(x),C_{0}}$

How much value does this create by refining the prediction system in this way? How you quantify that additional value?

Suppose we got the forecast, and when the forecast is high, you decide to buy the insurance. On the other hand, when the forecast is low, you decide not to buy the insurance. There is a critical boundary here. I know in advance, which x, I am going to map to which action. On the right part, the expected loss is higher than buying the insurance, and on the left part, the expected loss is lower than buying the insurance.


![9](Picturs/pic_57.PNG)


To document how much value our method will create we can use the historic data. We can compare the action they actually did with how well we claim that could have done. That is one way to do that. 

We can obtain the expected loss over the distribution of the forecast signal x and then compare it with the loss which was obtained without considering the forecasting signal. In calculating the value of the loss without considering the forecasting signal, it does not depend on x. 

