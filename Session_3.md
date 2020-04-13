# Session 3


Sometimes the actual decision problem was not very well articulated. In the decision problems there is always a cost or benefit and your goal is to find a trade off between them. So, when you are articulating the decision problem you are going to find what is the cost or benefit in the decision problem and what is the state variable space. The decision problems means the set of options that someone has to make. For example there is a fix budget for food and you are going to purchase nutrition and callories in order to maximize the quentify nutrition health benefits. 


## Formulization for statistical decision model:

Action set $\Rightarrow A={a_{0},a_{1},...,a_{m}} or A\subseteqR^{M}$

Example: you have a fixed budget and you got two assets including safe and risky assets. You are going to decide what proportion of your portfolio to put at the risky asset and how much put at the safe asset.

Ex 1:Portfolio allocation, 2 assets including safe and risky

Action: fraction of the portfolio in a risky asset

$0 \leq a \leq 1$    $A=[0,1]\equiv \bigtriangleup^{1}$ 

Ex 2:Portfolio allocation, 3 assets including cash,bonds,and stacks

Let $a_{i}$ fraction of portfolio allocated to asset i,i={1,2,3}

We must have 0 \leq a_{i} \leq 1, \sum_{i=1}^{3} a_{i}=1$

$A={<a_{1},a_{2}, a_{3}>| 0 \leq a_{i} \leq 1 for i=1,2,3, \sum_{i=1}^{3} a_{i}=1}$ 

$\equiv \bigtriangleup^{2}$   The unit simplex in $R^{3}$

![7](Picturs/pic_7.png)

There are a set of points, each of them are non negative and their summation is equal to the one.

The following is the two dimensional object in the three dimensional space

![8](Picturs/pic_8.png)

Problems where you got to allocate some scarce resource according to some kind of finding comstraints, the action set often ends up looking something like the above figures.


States: $x \in X$

x refers to the observable data about the state of the worlds

X state space or sample space

In some application we are going to have dataset, we are going to analyze then and we will come up with some estimated parameters and some actions based on that. In other cases, we may not yet know the values of our data but we may anticipate.

Example: Medical test, the previous example related to whether or not perform the test in order to gain new information.

You have to decide based on the trade of associate with that test before you actually get the information

Therefore, x in some application is the observable data which is not yet observed. 

When x is uncertain, we represent its value as a random variable, X.

EX: Medical test, X={test is negative, test is positive}={0,1}

Let X random variable corresponding to the test result.

We write $X 	\sim \beta(\theta)$

X is distrbuted as a Bernoulli the parameter $\theta$

$Pr{X=1}=\theta$

$Pr{X=0}=1-\theta$






























  
