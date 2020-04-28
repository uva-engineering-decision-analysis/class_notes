# Session 8



Right bottom circle is the end of the season. At that time, we would be out of the season and out of the flight. Therefore, the expected flight for rest of the season would be zero. In addition, for all of the bottom circles, the expected value again would be zero. On the circle corresponding one day left and one flight left, the expected value would be 28. What would be the value of being at the circle corresponding to two days left and one flight left? We know there are two ways to reach to the end of the season. We will choose to go for one day left and no fligt if its likelihood is bigger than 0.28. So, in this way, you will go backward.




















### 

Suppose an optimal decision rule $a(d, f | s)$ has been found. 

Let $V(d, f)$ denote the expected number of successes that would be realized from repeated application of this rule, starting from initial conditions $<d, f>$. 

By construction, $V(\cdot)$ equals the maximand of the decision-maker's objective function, beginning from these initial conditions, under the substitution $a = a(d, f | s)$:

$$V(d,f) = E^{\pi} \left[ \sum_{i = d,\ldots, 1} a(i,f_i | s_i) \cdot X_i \right]$$
where the expectation is taken over the probability distribution of all possible sequences of forecast signals (determined by $\pi$), and where $f_i$ denotes the number of flights remaining on date $i$ when the optimal program is followed.

###

$V(d,f)$ called the *value function* for this problem.

Because $a(\cdot)$ is assumed to be optimal, $V(\cdot)$ must satisfy a particular recursive relationship:
$$ V(d,f) = E^{\pi} \left[ a^*_d \cdot X_d  + V(d-1, f- a^*_d) \right]$$
where $a^*_d = a(d,f | s_d)$ is the optimal decision.
###
Once the forecast signal $s_d$ is received, $a^*$ will be chosen optimally:

  * If $a^* = 1$, then $V(d,f | s_d) = E \left[X_d | s_d \right]  + V(d-1, f- 1)$.
  * If $a^* = 0$, then $V(d,f | s_d) = V(d-1, f)$.

Since $V(\cdot)$ is by construction a maximum, we must have:
$$V(d,f | s_d) = \max \{ E \left[ X_d | s_d \right]  + V(d-1, f- 1), V(d-1, f) \}$$
               
$=  \max \{ p(s_d) + V(d-1, f- 1), V(d-1, f) \}$
               
###

This formula implies the optimal decision rule: $a^* = 1$ ("fly") only if

$$ p(s_d) \geq V(d-1, f) -V(d-1, f- 1)$$
i.e., when the expected payoff of the current day's opportunity exceeds the loss in marginal cost associated with arriving tomorrow with one fewer flight in the bank.

Call $p(s_d)$ the *hurdle probability*.




Successes are flights launched on days with good conditions. 

Type I errors are decisions to fly only to find no clouds.

Type II errors are decisions to stand down only to find that the desired conditions existed.
