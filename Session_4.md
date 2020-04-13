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

