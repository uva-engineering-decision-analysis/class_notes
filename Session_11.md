# Session 11


Example: We have a population of fathers and their sons. Their occupation is divided into five categories. The numbers in the table show the joined probability distribution. Also, the sum of all numbers, in the table, equals to one. 

![1](Picturs/pic_31.PNG)

Two variables are independent if knowing one of them does not give you information about the other one. Also, two variables are independent if the following relationship is true between them:

$P(A \cap B)=P(A) \times P(B)$

What is the probability that the son is professional?

$Pr(Y_{2}=Professional)=\sum Pr(Y_{2}=Professional,Y_{2}=i)=0.352 \neq 0.164$

It is shown that the conditional probability is not equal to unconditional probability.

The above concept is essentially what your predictive model is going to do. You are going to go from unconditional probability to conditional probability. You are going to condition on some data you have to give the probability of some future event. There are different ways to create these joined probability events such as machine learning and so on. But essentially what you are going to do is to build somehow the joined probability distributions between the data that you know about (Prior knowledge) and the data you want to know about.


### Bayesian methods: Introduction via simple example



Suppose you want to estimate the fraction of a population that is infected with some disease.

$\theta \in [0,1]$ : true value

Test a random sample of $20$ from the population. 

$Y \in \{0,1,\ldots,20\}$ : # of positive results.

Question: What does realized value of $Y$ tell us about the true value of $\theta$?

### Sampling model

$Y | \theta$ ~ binomial$(20,\theta)$: For $y = 0, 1, \ldots, 20$, (i.i.d.)

$$l(y|\theta) = \Pr(Y=y | \theta) = {20 \choose y} \theta^y (1-\theta)^{(20-y)}$$

where $\binom{n}{k} = \frac{n!}{k!(n-k)!}$

$l(y|\theta)$ called the *likelihood function*.

![2](Picturs/pic_32.PNG)

The above left graph is the graph of the likelihood function or the histogram of the likelihood function for different values of data. If $\theta$ is equal to 0.05, there is a substantial probability of getting zero successful tasks out of 20 and if you get zero success out of 20 that just not tell you the expected value for the real $\theta$ is zero. 


Idea: For any $0< \theta < 1$, all values of $Y$ are *possible*, but some are more likely than others. 

The likelihood function tells us how likely is each possible observation, for a given $\theta$.

If, say, $Y = 15$, that provides evidence that $\theta$ is not small.

Core of Bayesian reasoning: work out all the different combinations of $Y, \theta$ that could have generated the observed sample data. 

### Prior information

Suppose we have some background knowledge about the likely values of $\theta$. 

Represent this knowledge by means of a *prior distribution* $\pi(\theta)$ over $[0,1]$.

Obviously, there are many (infinitely many) possible such distributions. 

For convenience, we typically choose to model priors as chosen from a parametrized family of distributions.

### The Beta distribution

$$\theta \sim \text{beta}(a,b)$$

Then

$$E[\theta] = \frac{a}{a+b}$$

###

For our case, let's suppose our prior beliefs correspond to:

$$\theta \sim \text{beta}(2,20)$$

###

$$\theta \sim \text{beta}(2,20)$$ 

implies

![3](Picturs/pic_33.PNG)

### Bayes Theorem

Let $\pi(\theta | y)$ denote our *posterior distribution* over values of $\theta$.

This means: our *updated* beliefs about the likelihood that $\theta$ takes various values, *after* we've received our test results.

Bayes Theorem says:

$$\pi(\theta | y) = \frac{l(y|\theta) \pi(\theta)}{Pr\{Y = y\}} 
                  = \frac{l(y|\theta) \pi(\theta)}{\int_\Theta l(y|\tilde{\theta})\pi(\tilde{\theta}) d\tilde{\theta}}$$


Can be shown: 

If $\theta \sim \text{beta}(2,20)$ and $Y = 0$, then $\theta | y \sim \text{beta}(2,40)$.

More generally:

If $\theta \sim \text{beta}(a,b)$ and $Y = y$, then $\theta | y \sim \text{beta}(a+y,b+20-y)$.

![4](Picturs/pic_34.png)

The new expected value is being the weighted average of your prior expectation and the sample mean. If w is very small, then you are putting most of your weight on your sample data, otherwise you put most of the weight on the prior expectation.


### Sensitivity analysis

![5](Picturs/pic_35.png)

The X-axis shows the w, and the Y-axis shows the prior expectation. Given the prior expectation is 0.5 and the number of the positive tests is equal to zero. If you have high strong prior beliefs, your posterior mean is going to be about 0.26. 
If you have less strong prior beliefs, your posterior mean is going to be about 0.16. 
If you have very weak strong prior beliefs, your posterior mean is going to be about 0.02. 

## Building a predictive model

Ex: We have a sample of 342 diabetes patients, and for each of them we have an observation for 64 different variables. These variables may or may not give you useful information. Suppose that the progress of diabetes is the linear function along with different variables. So, each wight indicates how important is the corresponding variable. We have an error process in this model, which is independent and identically distributed. The error follows the standard normal distribution. There is data dependence, such as the data dependence between family members who live at the same house. Most of these variables may not be useful and relevant. 



![6](Picturs/pic_36.png)

Consider you find out the distribution of the $\theta$ given the sample expectation, now you want to figure out what is the likelihood of getting a different value for the next.

![7](Picturs/pic_38.png)

![8](Picturs/pic_39.png)

In the above-left side graph, the predictions were plot against the observations. Here, if the model was perfect, every point will be exactly on the line. 

![9](Picturs/pic_37.png)

To have a useful prediction, you should be cautious that it cannot depend on anything unobserved. You have to get rid of all of the unobserved parameters.






