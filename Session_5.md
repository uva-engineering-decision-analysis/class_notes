# Session 5

In the previous example "When should I leave my house to get to the airport", we do not use directly the estimated value, because there is an uncertainty and error in estimation how long it will to take you to get to the airport. The cost of the error is not symmetric; it will cost you a lot more to be a little bit late than to be a little bit early there. Therefore, your optimal action, should take that estimation error into account. You choose the action that maximazes payoff in estimation rather than the estimate of unobserved parameter and then, plug that into the decision making formula, assuming it is correct, ignoring the error and then make an action based on that assumption (estimated value).

Here, We need to quantify the amount of the error (uncertainty) and take inti account to make a rigorous optimal decision. This is why the statistical decision theory is a powerful tool because it gives you the rigorous way to deal with the error.

Actions: $a \in A$

States: $x \in X$, Parameters: $\theta \in \Theta$

$x_{1},x_{2},...,x_{n}$ random variables on X

Suppose we have uncertainty about our parameter values and in our game directly or indirectly we are depends on the values of the unobserved parameters.

So, we suppose that we got some posibility to get better information about unobserved parameters and there can be different ways.  Here, we suppose we are going to get information by using statistical sampling from the state space and the statistical inference.

EX: Who is going to win the election and it depends on the population. Therefore, you can learn by doing some statistical smapling and from that you can get information.

When we are doing sampling, we suppose that they are independent and identically distributed (iid).

f(x): Defines the probability distribution for all $x_{i}$ (for now drop i)

If X is discrete, e.g. X={1,...,m}

$f(x_{j})=pr{X=x_{j}}, j=1,2,...,J$

More generality, $B\subseteq X$

Then, $pr{x\subseteq B}=\Sigma_{j\in B}f(x_{j}) j=1,2,...,J$

If X is contineous

$B\subseteq X$

Then, $pr{x\subseteq B}=\int_{x\in B}f(x)dx $

![10](Picturs/pic_10.png)

Suppose that there are probability density depends on the values of the unobserved parameter ($\theta$), e.g. If we belive that the values are normally distributed, then it depends on two parameters including the $\mu$ and $\sigma$ of the distribution. 

$f(x)=f(x\\theta)$

Ex: $x_{1},x_{2},...,x_{n}\sim N(\mu,\sigma)$

$\theta=<\mu,\sigma^{2}>$

Let $\pi(\theta)$ denotes our prior believs about values of $\theta$











