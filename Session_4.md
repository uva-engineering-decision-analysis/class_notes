# Session 4

A= actions    $a \in A$

X= states  $x \in X$



payoffs, depending on your model, depend on realized state of the world (X) or the value of unobserved parameter.
 
In the case of medical test, the realized payoff depends on whether or not the petient has a pacterial or viral infection. 

There is unobserved parameter $\theta$ which discribes the likelihood about that petient to have bacterial or viral infection.

The realized payoff is not depend on $\theta$ but it depends on state. Then, in this case, it makes sense to model your payoff based on states not the unobserved parameter.However, the expected value depends on the probabilities. 

In other applications, the payoff may depend on unobserved parameter. As an example, given you are working for a company and you are marketing for a new drug and you are trying to decide the estimate the benefits or the retuns to the company.
It depends on the market share that the drug will get. Therefore, it ma make sense to considr the market share a parameter.
What really matters here is you are correctly specifying what is the thing that actually determines payoff.

Payoff: Depending on situation,

might model as function of (a,x) or 4(a,\theta)$

Suppose payoff depends on (a,x)

let u(a,x), realized payoff as a function of realized x.

Before value of x is known, model it as a random variable X

Let p(x)=pr(X=x), Assuming X is discrete

Then $E[u(a,x)]=-sum p(x)u(a,x)$

If the goal is to max E[u(a,x)], then the optimal action is $a^{*}$ is the one that maximize E[u(a,x)]:

$a^{*}=arg max E[u(a,x)]$ 

If the goal is to avoide the bad outcome at all cost then $a^{*}$ is

$a^{*}=$

Think of each action as a lottery 

$a_{1} \longmapsto <u(a_{1},x_{1}),u(a_{1},x_{2}),...,u(a_{1},x_{N})>$

$p(x_{1}),p(x_{2}),...,$p(x_{N})$

$a_{2} \longmapsto <>)>$
.
.
.

X is the temperature, 

Each action is whether or not wear the jacket

If yaou are the expecte value maximization decision maker, then the way you choose the action is selecting the action with highest expected payoff.

If you have two identical jacket, wearing each of them is one action and their pay of will be equal. Therefore, they are actually the same action and you can consider tham as a one choice.

 If your goal is to avoide that outcome that have cost, for each of the actions we identify the worse possible outcome that is associated with that outcome. We do not care about the probabilities. 
 
 \underline{u}(a_{1})$\min_{x\in X} u(a_{1},x)$ 
 
The above equation shows the minimum possible worse case pay off if we choose action one. we have the same relationsheps for other actions.

\underline{u}(a_{2})$\min_{x\in X} u(a_{2},x)$ 
.
.
.

In this problem we want to avoide worse outcomes. Therefor, choose $a^{*}$ as follows:

$a^{*}= arg max_{i=1,2,...,M}\underline{u}(a_{i})$

To choose this way is called following a "Max Min rule".


## Payoffs in terms of unobserved parameters

Suppose we model $u(a,\theta)$: payoff is function of action and parametr $\theta$

If suppose that we want to choose an action to max $u(a,\theta)$

Assume that we have some oppurtunities to do some statistical sampling from some data which tells use something about $\theta$ and it helps us to sharppen our believes and based on that we can choose the right action.

Suppose we do not know much about $\theta$, but we can collect data. 

Ex: $x_{1},...,x_{n}\sim N(\mu,  \sigma})$ and it helps us to estimate $\theta$


First,collect data: $x_{1},...,x_{n}$

Second, estimate $N(\mu,  \sigma})$

Third, choose optimal action given new information about $N(\mu,  \sigma})$

How to do the above precedure? 
Frequentist: $\mu^{^}=\frac{\Sigma_{i=1}^{n}\lambda_{i}}{n}$

Ex: You have a flight, when you will leave your house? You will estimate the time it will take to arrive there. There is a cost to get the airport early and there is a cost to get there late. Why do not get the estimated value to get there at the right time. The payoff is not symmetric; if you get there a little bit early, there is a small cost. However, if you get there a little bit late, the cost will be huge. Therefore, considering the estimated $\mu$, and choosing the action that maximizes the payoff is not in fact the optimal decision making procedure. What you need is a rigorous way of deciding how much error there is and then dealing with payoff and the aptimal action given this error. This is what statistical decision theory will do for us. In the airport example, you will not consider the etimated arriving time ($\mu$). In fact, you know there is an error and you will take into account that error.







