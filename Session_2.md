# Session 2:

## Notations

x: Random variables     $x \in X$

Example: X={Infection is bacterial, infection is viral}={0,1}

$\theta$: Parameters, ounobserved. It describes our knowledge or beliefs about probabilitys of different x.

$\theta= prob{X=1} $

Example: $\theta=[0,1]$

$\pi(\theta)$ represents our knowledge our belief about $\theta$

$\pi(\theta)$: Somme probability distribution over $\theta$

$\Theta$: Parameter space


## Example:

x \in X={0,1} corresponding to whether or not the petient has or does not have a bacterial infection as oppose to viral.

 $\theta=[0,1]$  represents prob{x=1}
 
 Actions={Giving the medication to the petient or not}
 
 
 |               | 0             |      1       | Average      |
 | ------------- | ------------- |------------- |------------- |
 |       Yes     | -3            |2             |    1         |
 |       No      | 0             |0             |    0         |


Let present the same payoff in decision tree. We represent the decision problem imaginig you are going from lef to right, and as you go you are making choices.

Here we represents our action or decision with the rectangular boxes. There are two choices whether or not give the petient the medicine. If we give the medicine and the pecient has bacterial infection then the payoff will be equal to +2. On the other hand, if we give the medicine to the petient and the petient has the viral infection, then the payoff will be equal to -3. In the following decision tree, the $\theta$ shows our belief corresponding to the random variable value. If we do not give the petient the medicine the amount of the payoff will be equal to zero.

![1](Picturs/pic_4.png)

To solve the decision tree means to identify the optimal action to take that maximizes the payoff. In this case, the decision maker is supposed to be risk neutral. If the decision maker is risk averse, the decision maker does not want to make mistake. Therefore, he always decides  not to give medicine to the petient to avoide patoff "-3". 

 
For each action in the decision tree, the amount of expected payoff was claculated showed in the above figure. The question is which one of the action should be choosen. As it was shown, the action "Y" will be choosen if the expected payoff action "Y" is bigger than action "N" and vice versa. In other word, based on the math, if $\theta$ is bigger that 0.6, the action "Y" will be choosen.


Suppose there is a test in advance and the result of the test showes the exact value for the x. Here, the question is how much you will pay for the test. 








