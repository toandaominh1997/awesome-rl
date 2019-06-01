<<<<<<< HEAD
# Reinforcement learning

## Table of Contents

[Table of Contents](#table-of-contents)
  - [1. Overview - Agent-Environment Interface](#1-overview---agent-environment-interface)
  - [2. Defination](#2-defination)
  - [3. Dynamic programming](#3-dynamic-programming)
  - [4. Monte Carlo](#4-monte-carlo)
  - [5. Temporal Difference - Q Learning](#5-temporal-difference---q-learning)
  - [6. Deep Q Learning](#6-deep-q-learning)


## 1. Overview - Agent-Environment Interface
![]()
The Agent at each step t receives a representation of the environment's state, $S_t \in S$ and it selects an action $A_t \in A(s)$. Then, as a consequence of its action the agent receives a *reward*, $R_{t+1} \in R \in R$
## 2. Defination
  1. Action (A): All the possible moves that the agent can take
  2. State (S): Current situation returned by the environment.
  3. Reward (R): An immediate return send back from the environment to evaluate the last action.
  4. Policy (π): The strategy that the agent employs to determine next action based on the current state.
  5. Value (V): The expected long-term return with discount, as opposed to the short-term reward R. Vπ(s) is defined as the expected long-term return of the current state sunder policy π.
  6. Q-value or action-value (Q): Q-value is similar to Value, except that it takes an extra parameter, the current action a. Qπ(s, a) refers to the long-term return of the current state s, taking action a under policy π.
## 3. Dynamic programming
- ### 3.1 Policy Iteration
    | ![space-1.jpg](RESOURCES/policy_iteration.png) |
    |:--:| 
    |* Algorithm 1: Policy Iteration *               |
- ### 3.2 Value Iteration
    | ![space-1.jpg](RESOURCES/value_iteration.png) |
    |:--:| 
    |* Algorithm 2: Value Iteration *               |

## 4. Monte Carlo 
Monte Carlo (MC) is a Model Free method, It does not require
complete knowledge of the environment. It is based on
averaging sample returns for each state-action pair. The
following algorithm gives the basic implementation:
| ![](RESOURCES/monte-carlo-method-first-visit.png) |
|:--:| 
|* Algorithm 3: Monte Carlo method first visit * |
### Sarsa
Sarsa (State-action-reward-state-action) is a on-policy TD control. The update rule:
![](https://latex.codecogs.com/gif.latex?Q%28s_t%2C%20a_t%29%20%5Cleftarrow%20Q%28s_t%2C%20a_t%29%20&plus;%20%5Calpha%20%5Cleft%5Br_t%20&plus;%20%5Cgamma%20Q%28s_%7Bt&plus;1%7D%2C%20a_%7Bt&plus;1%7D%29%20-%20Q%28s_t%2C%20a_t%29%20%5Cright%5D)
#### n-step Sarsa
![](https://latex.codecogs.com/gif.latex?%5Cfn_cm%20q%5E%7B%28n%29%7D%20%3D%20R_%7Bt&plus;1%7D%20&plus;%20%5Cgamma%20R%7Bt&plus;2%7D%20&plus;%20%5Cldots%20&plus;%20%5Cgamma%5E%7Bn-1%7D%20R_%7Bt&plus;n%7D%20&plus;%20%5Cgamma%5En%20Q%28S_%7Bt&plus;n%7D%29)
#### n-step Sarsa update Q(S, a) towards the n-step Q-return
![](https://latex.codecogs.com/gif.latex?%5Cfn_cm%20q%5E%7B%28n%29%7D%20%3D%20R_%7Bt&plus;1%7D%20&plus;%20%5Cgamma%20R%7Bt&plus;2%7D%20&plus;%20%5Cldots%20&plus;%20%5Cgamma%5E%7Bn-1%7D%20R_%7Bt&plus;n%7D%20&plus;%20%5Cgamma%5En%20Q%28S_%7Bt&plus;n%7D%29)
#### Forward View sarsa(![](https://latex.codecogs.com/gif.latex?\fn_cm&space;\lambda))
![](https://latex.codecogs.com/gif.latex?%5Cfn_cm%20q_t%5E%5Clambda%20%3D%20%281-%5Clambda%29%20%5Csum_%7Bn%3D1%7D%5E%5Cinfty%20%5Clambda%5E%7Bn-1%7D%20q_t%5E%7B%28n%29%7D)

Forward-view Sarsa(![](https://latex.codecogs.com/gif.latex?\fn_cm&space;\lambda))

![](https://latex.codecogs.com/gif.latex?%5Cfn_cm%20Q%28s_t%2C%20a_t%29%20%5Cleftarrow%20Q%28s_t%2C%20a_t%29%20&plus;%20%5Calpha%20%5Cleft%5Bq_t%5E%5Clambda%20-%20Q%28s_t%2C%20a_t%29%20%5Cright%5D)

![](RESOURCES/sarsa.png)

## 5. Temporal Difference - Q Learning
Temporal Difference (TD) methods learn directly from raw
experience without a model of the environment’s dynamics.
TD substitutes the expected discounted reward Gt from the
episode with an estimation:

<img src="http://www.sciweavers.org/tex2img.php?eq=1.%20init%5C%5C%0A2.%20a%5E2&bc=White&fc=Black&im=gif&fs=12&ff=arev&edit=0" align="center" border="0" alt="1. init\\2. a^2" width="50" height="40" />
## 6. Deep Q Learning
=======
# awesome-rl

![](https://latex.codecogs.com/gif.download?Q%28s_t%2C%20a_t%29%20%5Cleftarrow%20Q%28s_t%2C%20a_t%29%20+%20%5Calpha%20%5Cleft%5Br_t%20+%20%5Cgamma%20Q%28s_%7Bt+1%7D%2C%20a_%7Bt+1%7D%29%20-%20Q%28s_t%2C%20a_t%29%20%5Cright%5D)
