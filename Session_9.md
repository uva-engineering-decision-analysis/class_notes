Given we have a dicision problem and a predictive tool that helps us to discriminate between different cases. Each decision maker has a menue of the options and the values that the predictive tool has is allow you to discriminate among cases. So, you can deliver the rigt introduction for that case. We also have the theme about handling the uncertainty. We want the forcast information to include information about uncertainty. The way to do this is to present a forcast as a probability distribution over the state relevant variance. So, we saw in order to get that kind of information, we had to create a specialize post processor that would convert the output of the predictive model into probability distributions over the relavant state variables. You may get some pprediction in your case, but the form of thse prediction my not be expressed in terms of the probabilities of the decision making variables. Therefore, in this case you are going to have to construct that postprocessing tool. There are various tools to do forcasting and so on for us and how to translate those into the probability distribution for the particular variable that the decision maker care about it is going to be an aplication specific endeavore.  

 Pic 23

 In the previous example, the forcaster delivered the high quality information about the wrong variable. The variable that is not the one that the decision maker really cared about. Whta the decistion maker cared about was the distribution of the probability, the probability of the exceeding different threshold. Then, that gap in the graph led to the flooding the town.

 Pic 24

How they got the probability distrbution? There are many varibles that scientists can measure but they must worke on relevant variables which here is the reletive humidity. There were too many reletive humidity types but we use methodes to clusster them into 24 profils. It is called dimensionality reduction. given we have a relative humidity plot and we want to check to which one of the profiles it is match. To do this, we use the euclidean distance. Then the percentage above the corresponding reletive humidity profile shows what percentage of of the plotes which is placed in this profile featured the boundry clouds. Here, we did get a discrimination, we get 24 fdifferent types. If we have the same number above all of the profiles, it is a failure. It does not matter in which boxes your graph is located, you will get the same probability of getting the boundry clouds. Therefore this mapping does not give you the discrimination which is the whole point of your predictive tool. The goal of your predictive tool is to discriminate between different cases in the decision relavent way.  We have different numbers, therefore, we clearly have discimination between them that is relevent to the reaction that we care about. If you have the perfect discriminator, it would be great.
How they got the probability distrbution? There are many varibles that scientists can measure but they must worke on relevant variables which here is the reletive humidity. There were too many reletive humidity types but we use methodes to clusster them into 24 profils. It is called dimensionality reduction. given we have a relative humidity plot and we want to check to which one of the profiles it is match. To do this, we use the euclidean distance. Then the percentage above the corresponding reletive humidity profile shows what percentage of of the plotes which is placed in this profile featured the boundry clouds. For example the number above the first profile (56%) shows that fifty six percent of the plots which match the first profile feature the boundry cloud.

What goes into the this graph is not a raw data. It is actually the output of the numerical weather prediction model.Here, the problem is the forcasting model has the error. We have a couple of different errors that we have to deal with. We have eror that given the reletive humidity profiles, we got the imperfect of weather or not we are going to get the boundry level clouds. Then, given the forcast of the future atmosphere condition is also imperfect. So, we have to deal with both types of errors. 

pic 25

The above picture is dealing with the second type of the error. If you forcast the certain type of the reletive humidity profile, how good is that forcast? Conditional on predicting that we end up the first state, what is the likelihood that we actually end up the first state? As it is shown in the picture is is equal to 13.3%. If our forcasting system is perfect, then this number will be equal to 100%. If it is completely useles, the numbers for all states wil be the same. There is no discrimination between them. 

Then we put both kind of the uncertainty together. FIgure 2 is mapping from the reallity to what we care about. The below graph is the mapping from the forcast to what we care about.

pic 26

If the model forcasts that we will end up the first state of the atmosphere. Then, 44% of time, we will get the boundry clouds. So, we still here have discrimination. The numbers above each plot shows the probability of getting boundry clouds conditional on the forcast telling us the relative humidity profile looking kind of like them. 

p(x=1|SOM=1)=0.44

IF the graph is completely uninformative graph, then:

$p(x=1|SOM=1)=p(x=1)=\beta$

THe unconditional probability is equal to average frequency throughout the year of getting boundry cloud.

pic 27

Now we are going to use this framework for pre-season planning. So, you can predict before starting the field season in expectation at the end of the field season how many successful flights you are ging to have. If you follow the rules, you can expect that a the end of the field season. V(160,68) is going to be our expected pay off if you behave optimally. 

If you start from point (D=160, F=68), you know what the probability distribution is over the likelihood outcome. If the number of the flight decrease by one, you can still say what will be the probability distribution over the outcomes at the end of the season. Consider there is cost for flight and cost for the day in the season. 

$C(F)=C_{F}F$

$C(F)=C_{D}D$

$C_{T}=C_{F}F+C_{D}D$

Based on them, we want to maximize the expected pay off under constraints of budget.

pic 28


The x-axis is the set of the combinations of initial days in the field season.  the y-axis is the number of the flights in the budget.  IF we have 100 days and 68 flights we will have the corresponding point on the curve $U_{1}$. You can have the same expected value by adding more days and reducing the number of flights, because all of the points on the curve $U_{1}$ have the same expected value. 

Suppose given the prices, any combination on left side of the line which cross the curves is affordable. The points on the line has the cost equal to $C_{T}=C_{F}F+C_{D}D$. I want here as much data as possible in expectation and I want to give $C_{T}$ money. The graph tells me how much data should I expect at the end of the season for any combination of the day and flight. I want to maximize the expected data subject to constrain on total cost of the field season. As was mentioaned, any combination on the left side of the line is affordable given the budget. Which combination would give me the most possible data? You should look for the highest curve  U which the line cross. In other words, you should want to get the highest curve that you can while staying within the budget constraint. This point is located on the curve $U_{3}$. This point give us the most data expectation subject to the budget constraint.

pic 28

The verification of your result is critical. What you really want to know is how much value your framework added. You should measure the value which is added quite vigorously. In this problem we do not have the vigorous way for measuring, because we can not know what would have happen without our predictive method. In this case for analytic purpose we have a beneficial situation that we do know, because the predictive model did not be used. Therefore, for that one field season we actually know what they did without the predictive model and we can use that result for comparison. 

pic 29

## Bayesian method

This is one of the ways which is used in the dicision making process. This approach used in sittuation where there is not enough data or in the rare event. It is statistical model which is trained on the data. I is used in the situations where we have limitted amount of data and we do not want to overrely on the data, because you recognize this is the small sample and it may not really reflect what is really going on. 









