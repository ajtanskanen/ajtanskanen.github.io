---
title: 'Analyzing a social security reform with reinforced learning'
date: 2021-05-25
permalink: /posts/2021/05/Analyzing-a-social-security-reform-with-reinforced-learning/
tags:
  - social security
  - ai
  - reinforced learning
---
A social security reform influences the behavior of people, but it is hard to figure out how. For example, would people work more if the Nordic social security model would be replaced with basic income? Or would they work significantly less? Financial viability of a social security reform depends on how employment would be affected by the reform.

A traditional economists’ way to describe behavior of individuals is to assume that each individual maximizes her utility. Utility is often a function of net income and a constant representing her valuation of free time. In particular, it is assumed that a rational individual works if it gives higher utility than not working. This is how we proceed here.

To analyze how a social security reform influences individuals’ behavior, we analyze a life-cycle model that describes the income of each individual during her life-cycle and the consequences of her decisions on her income.

Life-cycle model
=====
A life-cycle model describes the life-cycle of an individual or an agent. During the life-cycle an individual chooses whether to work, go unemployed and when to retire.

An individual prefers free time over working. Her income comes from the social security benefits and from wage when she works. Hence, both social security scheme and how wages develop must be part of the model. The employment and unemployment rates then emerge from the aggregate behavior of a large group of individuals.

Social security and wages
----
Social security benefits provide a safety net for individuals. In the Nordic model considered here, the safety net is quite comprehensive. It has been argued that high level of social security reduces the employment level. Wages develop with age based on average salaries and random shocks.

To analyze a social security reform, the social security scheme must first be described in sufficient detail. Figure 1 shows an example of the effective marginal tax rates. It shows how much of an increase of wage is “taxed” either directly via taxes or via reduction of means-tested decrease of benefits. An effective marginal tax rate that exceeds 100 percent means that an increase in wage in fact results in a reduced net income. Luckily, these situations are rare.

Utility
-----
To choose whether to work or not, an individual makes the choice that maximizes her expected future utility

where gamma is the discount factor, u is the utility function, and s is the state at time t. Here we use logarithmic utility function


where function n gives the net income in state s, and constant k is the penalty term for the lost free time due to working. Proper selection of constants k ensures that the model can reproduce the observed employment and unemployment rates. Logarithm ensures that regardless of net income, a similar percentual increase in net income, an individual observes a similar additional utility.

Implementation
-----
Simulation is implemented as a discrete-time process, in which time-step is 3 months. At each time-step, the individual can choose to work or go unemployed.

Life-cycle of an individual is implemented as an OpenAI Gym environment econogym. To implement the social security scheme, a description of the Finnish social security was written as a python module benefit. On top of that, OpenAI Gym environment econogym was implemented to describe the state of an individual. Optimal policy for econogym can be solved using lifecycle module, which makes use of ACKTR algorithm implemented in Stable Baselines reinforced learning library. Unfortunately, ACKTR is not implemented in Stable baselines 3, and here Stable baselines 2 is used.

All codes are available in Github. In addition, Colab notebook can be used to run the example code.

Solving the model
The optimal actions (that is, policy) can be solved with dynamic programming. However, dynamic programming needs to find the optimal action for all states. Even when the state space is discretized, the space is simply too large for dynamic programming. An approximate method is needed, and reinforced learning fits the bill.

The life cycle model is implemented as a Python module lifecycle-rl available from Github. See section Implementation above for more details.

import numpy as np
import matplotlib.pyplot as plt
from lifecycle_rl import Lifecycle
Reinforced Learning
Reinforced learning can be used to solve our problem. Reinforced algorithms do not need to solve the problem in all of the state space, since neural nets enable generalization from the observed sample. Generalization makes the problem feasible in practice. In tests with a simplified model, reinforced learning has found a policy that is close to the policy found with dynamic programming. Here we employ ACKTR algorithm.

Reinforced learning maximizes the discounted present value of future rewards


This is essentially the same as above when reward r is utility u of net income.

Baseline
-----
We fit the model in such a way that the model reproduces the employment and unemployment rates for both women and men in a model that represents how social security scheme is set up in Finland. It is an example of the Nordic model of social security that provides a comprehensive coverage for individuals.

Everything needed is included in Lifecycle object. To set up the model, Lifecycle object that runs environment unemployment-v3 that describes the lifecycle of individuals. Let us first declare some variables and set up the model.

baseline_model='baseline_model'
baseline_results='baseline_results'
baseline_start='v3_malli_baseline3test_nomort'
baseline_LCmodel=Lifecycle(env='unemployment-v3')
Then, to actually run the baseline model

baseline_LCmodel.run_results(steps1=10_000_000,
pop=100_000,
batch1=8,
rlmodel='leaky-acktr',
save=baseline_model,
cont=True,
start_from=baseline_start,
results=baseline_results)
Figure 2 shows that the baseline model reproduces employment rate quite well. So, lets move on to analyze a social security reform.


Figure 2. Employment rate in the model compared with observed
Social security reform
A recent reform of Finnish pension scheme was the increase of the lowest retirement age. Let us now analyze how this increase influences employment rate. To do this, simply define the lowest retirement age to be 65. For this purpose, we create a new Gym environment based on unemployment-v3 and set the lowest retirement age at 65.

ret_LC=Lifecycle(env='unemployment-v3',min_retirementage=65)
Then we run both fitting and simulation like above.

ret_LC.run_results(steps1=10_000_000,
pop=100_000,
batch1=8,
rlmodel='leaky-acktr',
save=baseline_model,
cont=True,
start_from=baseline_start,
results=baseline_results)
To get an idea how the reform influences unemployment, we need to compare the results to those of the baseline model.

ret_LC.compare_with(baseline_LCmodel,label1='retirement 65',label2='retirement 63.5')
Figure 3 shows the comparison of the reformed model retirement 65 with the baseline model retirement 63.5. As expected, retiring shifts toward older ages, which shows as postponing move to the unemployment tunnel in this case (Figure 3).

The simulation can be run on a Colab notebook. It should be noted that the training requires several tens of millions episodes to converge.


Figure 3. Comparison of unemployment rates for a retirement age 63.5 y and retirement age 65 y.
Reliability of results
To get a reliable estimate of the influence of the social security reform, the population of simulated agents should be large enough. The error in the employment rate consists of two parts: randomness in the simulation and deviation of the policy from the optimal policy.

Randomness in the simulation is proportional to one over the square root of the number of individuals. Hence, there should be at least ten thousand individuals in a simulation for it to yield reliable results. To address the randomness due to the policy, a number of runs should be made.

Conclusions
=====
Reinforced learning is a good tool for analyzing a social security reform. However, to get reliable results, one needs to make a sufficient number of runs and use sufficiently large populations to make sure that the results are stable. Unlike dynamic programming, reinforced learning can solve employment rate in a fully-dynamic model of social security. Such a model can take into account behavioral effects in analysis of a social security reform.


