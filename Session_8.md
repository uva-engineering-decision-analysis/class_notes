# Session 8

There is a report called "Completing the forcast". When we produce a forcast, of course, there is an error. What we can do is see if we can actually represent the error in our forcast, in a rigorous way. The weather system is a cheotic system which implies something in feature called sensitive dependence on initial conditions. IT means if you misspicify your initiale condition by just a little bit, then as you forcast over time, evenif you have the physics completely accurate, that small error in the way you specify the correct state of the system will will inevitably lead to larger errors over time. Those errors do not grow linearly with time; they explode. This error is inevitable, since you can not completely specify the state of the atmosphere. Even thoug you could do that accurately, there is not enough sensor. Let's represent our actual uncertainty about the forcasting. With different initial condition, you get different model runs comming out and then you measure the uncertainty in the forcast based on those models.

![16](Picturs/pic_16.png)

There was a flood in Red River in Grand Forks in 1997. They had prepared for the flood because they were getting forcast from Natural weather servise about how high river would rise. Then, they estimated how hight the flood would go and gave the expected value. They forcasted the rivers only got up to "50 ft". Therefore, they decided to make sand bags and they thought if the hight of the sand bags were 50 ft, they would be safe. But, they did not. The forcast and the actual rising were shown in the graph. What happen was it bumped up the forcast very fast and there was not enough time left to increase the hight of the sand bags. Therefore, there were a lot of blames that the Natural weather servise did poor job. It was not actually fair, because they gave the best forcast best on the data. The problem was that expected value is not the infrmation that they needed. They needed the information about how high the sand bag should be. They did not to know the best estimation for sand bags, they needed to know what is the probability of getting higher than 50 ft, 51 ft and so on. When they had that information, they could have themselves calibrated how much risk they were willing to take. It was turn out that the Natural weather servise, they actually had that kind of theinformation but nobody ask them to produce that. They found ou that the 54 ft was within the reasonable margin of the error goven the analatics they were using. The left side graph was that kind of information thay have started to produce since that event. In this graph, the green line shows the expected value and the blue boxes show the amount of the error. 

### The promise: data-driven decision making

Data science hype: "Better information $\rightarrow$ Better decisions!"

*Claim:* That's wrong. 

Because, more inrrelavant information will more distract you away from the points of data you really need for that decision. 


Data-driven decision-making also requires complementary analytics and products: 

 * *Prediction* : calibration of error, $\rightarrow$ *probabilistic* forecasts
 
 * *Optimization* : application-specific models and tools, attention to user objectives
 
 * *Visualization/communication* : intelligence *actionable* in terms of user's decision problem
 
In this example: If they built the sand bags higher than the estimation it would be costly; if they built lower than thet it would be more disaster and the cos of the error is not symmetric here. The cost of the error is greter in on direction. You want the calibration of the error in the form of the probabilistic forcast. You do not want the whole distribution. You have to identify where in that distribution is relevant to the decision you want to make. Then, you do the optimization. In this case, they wil solve the risk management problem. 

Better information does not make better decision. We need other tools to convert those better information into better decision. 

### Realizing the promise of data-driven decision-making

On prediction, data science gallops along: machine learning, classification, prediction, inference$\ldots$

*Claim:* The promise of data science to empower data-driven decision-making lags its potential, because of insufficient focus on *complementary* analytics:

 * Rigorous quantification of *uncertainty* and *error* in outputs of predictive models
 * Accurate formal representation of decision problems -- including decision-maker's objectives and tolerance for risk
 * Appropriate use of optimization techniques 
 * Visualizations or other products customized to decision contexts
  

*Goal:* Identify good *actions*, conditional on predictions made with error 

Now, we are going to talk about a particular application.

## EX: The Cloud Hunter's Problem

### Meet the Cloud Hunter

The Cloud Hunter is an atmospheric scientist.

The Cloud Hunter wants to collect data from inside *liquid boundary layer clouds*.

That takes aircraft. Which are expensive.

### The Cloud Hunter's Decision Problem

The Cloud Hunter’s Problem concerns how to allocate a fixed budget of flight hours between dates over the course of a field season. 

Fly/No-fly decisions must be made 1 day ahead, based on imperfect day-ahead forecasts of whether conditions are good or bad for collecting required data.

### Model setup: Conditions for data collection over the course of the field season

$D$ : length of the field season in days

$d = D, \ldots, 1$ : index of dates

$X_d$ : quality of conditions for data collection: 

 * $X_d = 1$ if conditions on date $d$ are good, 0 otherwise
 * Each $X_d$ a binary random state variable, i.e., a Bernoulli trial

A field season is a particular realization $x_D, \ldots, x_1$ of the stochastic process 
$X_D,\ldots, X_1$.

Will assume the $X_d$ are independent and identically distributed (i.i.d.). 

 * Assumption not actually required, but keeps things simpler and clearer.

Vector notation: $\bf{X} =$$< X_D, \ldots, X_1>$ denotes the stochastic process; $\bf{x} =$$< x_D, \ldots, x_1>$ denotes a particular realization.

### Model setup: Decisions, resource constraints

$F \leq D$ : number of flights in the Cloud Hunter’s budget. 

$f = F, \ldots, 1$ : index of flights remaining in budget

$a_d$ :  binary control variables ("actions")

* $a_d = 1$ iff they opt to fly on date $d$, 0 otherwise

$\bf{a} =$$< a_D, \ldots, a_1>$ : actions chosen on dates $d = D, \ldots, 1$

Resource constraint: $\sum_d a_d \leq F$.

(Assume flights left over at the end of the season have no residual value.)

### Payoffs and objectives

*Payoffs*: For a given sequence of choices $\bf{a}$ and realizations $\bf{x}$, the realized amount of data collected $U$ is given by 
$$U = \mathbf{a \cdot x} =\sum_d a_d x_d$$.

*Decision-maker's objective*: Choose a fly/no-fly decision rule to maximize data collected in expection, subject to the resource constraint on total allowable flights:

Choose $\bf{a}$ to $max_{\bf{a}} = E[\bf{a} \cdot \bf{X}]$, subject to $\sum_d a_d \leq F$.

\textbf{Important:} This is a *substantive assumption* about the decision-maker's goals.

  * Models a decision-maker with a high tolerance for *risk*. 

### Forecasts

Decision taken on basis of a day-ahead forecast.

Before taking each decision, decision-maker receives a forecast signal $s_d \in \mathbb{S}$.

Calibration: map this signal to a probability of good conditions:

$$p(s) =  \Pr\{X_d = 1 | s_d = s\}$$.

(Will assume stationarity.)


### Distribution of forecast signals

More than one day ahead, don't know which forecast signals $s \in \mathbb{S}$ will be received.

But, *do* know the the likelihood of receiving different signals.

$\pi(s)$ : probability that forecasting system will generate signal $s$. 

$\pi(\cdot)$ defines a probability distribution over the set $\mathbb{S}$ of possible forecast signals.

### The task of the decision analyst

Given this set-up, the job of the decision analyst is to devise an *optimal decision rule* $a^* = a(d,f |p)$ that delivers a recommended action---fly or no-fly---as a function of 

 * $d$ the number of days left in the field season, 
 * $f$ the number of flights left in the budget, and 
 * $p(s)$ the forecast probability that a flight today would be successful.
 
A decision rule $a(\cdot)$ is deemed optimal if its consistent application maximizes in expectation the yield of successful flights realized from a given budget $F$.

### Comment

This is a challenge of *intertemporal optimization*: each choice $a_d$ alters the expected payoffs for subsequent decisions. 

Need to use tools of optimization that account for this intertemporal structure.

*Dynamic programming* turns out to be the right tool for the job.

## Optimization via dynamic programming

### Intertemporal optimization via dynamic programming

Basic idea: break the decision problem into two pieces: (i) the next day's decision, and (ii) the rest of the field season after that.

Assume you've got the right answer (!). Given that this answer is optimal, derive the properties that solution must have.

Solve via backward induction.

![15](Picturs/pic_15.png)
 
Right bottom circle is the end of the season. At that time, we would be out of the season and out of the flight. Therefore, the expected flight for rest of the season would be zero. In addition, for all of the bottom circles, the expected value again would be zero. On the circle corresponding one day left and one flight left, the expected value would be 28. What would be the value of being at the circle corresponding to two days left and one flight left? We know there are two ways to reach to the end of the season. We will choose to go for one day left and no fligt if its likelihood is bigger than 0.28. 




