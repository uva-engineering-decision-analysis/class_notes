# Session 9

 Given we have a dicision problem and a predictive tool that helps us to discriminate between different cases. Each decision maker has a menue of the options and the values that the predictive tool has is allow you to discriminate among cases. So, you can deliver the rigt introduction for that case. We also have the theme about handling the uncertainty. We want the forcast information to include information about uncertainty. The way to do this is to present a forcast as a probability distribution over the state relevant variance. So, we saw in order to get that kind of information, we had to create a specialize post processor that would convert the output of the predictive model into probability distributions over the relavant state variables. You may get some pprediction in your case, but the form of thse prediction my not be expressed in terms of the probabilities of the decision making variables. Therefore, in this case you are going to have to construct that postprocessing tool. There are various tools to do forcasting and so on for us and how to translate those into the probability distribution for the particular variable that the decision maker care about it is going to be an aplication specific endeavore.  
 
 Pic 13
 
 In the previous example, the forcaster delivered the high quality information about the wrong variable. The variable that is not the one that the decision maker really cared about. Whta the decistion maker cared about was the distribution of the probability, the probability of the exceeding different threshold. Then, that gap in the graph led to the flooding the town.
 
 Pic 14
 
How they got the probability distrbution? There are many varibles that scientists can measure but they must worke on relevant variables which here is the reletive humidity. There were too many reletive humidity types but we use methodes to clusster them into 24 profils. It is called dimensionality reduction. given we have a relative humidity plot and we want to check to which one of the profiles it is match. To do this, we use the euclidean distance. Then the percentage above the corresponding reletive humidity profile shows what percentage of of the plotes which is placed in this profile featured the boundry clouds.  
 
 
 
 
