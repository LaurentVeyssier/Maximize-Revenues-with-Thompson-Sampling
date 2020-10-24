# Maximize-Revenues-with-Thompson-Sampling
Maximize revenues of Online Retail Business with Thompson Sampling algorithm

# Description
In this notebook, the objective is to maximize revenues of an online retail business by selecting the best strategy to convert users to the premium plan.
The project uses Thompson sampling algorithm to identify the best strategy among several options.
The best strategy identified is the one with the highest conversion rate.

# Problem statement
Many business problems can benefit from the approach developped in this project.
Here we assume the objective is to identify the best marketing campaign among several of them (9 strategies used in the project). These strategies can have different features differentiating them from each other. The objective is to identify and leverage as quickly as possible the strategy with the highest conversion rate.
Success of a campaign is measured by the conversion or not of the exposed customer to the premium plan.
Therefore the best strategy is the strategy genering the maximum conversion for an identical number of prints. One common application is advertizing or Ads.

# Approach
We measure conversion over a high number of customer prints (customer being exposed to a campaign advertising the premium plan) while randomly selecting a strategy to propose to the customer. This is the random strategy.

We do the same using Thompson sampling algorithm. The algorithm will select the strategy to present, updating at every time step (every customer prints) based on the conversion results. The algorithm is able to identify the best strategy very quickly (exploration phase) to predominantly offer this strategy only (exploitation). This allows to optimize the time necessary to explore and identify the best solution and start ripping the profits very quickly. In the project, the algorithm starts proposing heavily the best strategy after less than 500 customer experiments only.

Here we can see the strategies proposed (between 0 to 8) at every time step from the start of the experimentation. Starting the customer 500, the algorithm has already identified the best strategy (strategy n°6) and has started to exploit and maximize revenues.

![](thompsonconvergence.gif)


# Results

The convergence of Thompson Sampling algorithm is very quick. This is illustrated by the Regret Curves shown below.

![](random.png)    ![](thompson.png)

- Thompson Sampling is converging very well towards the best strategy
- No convergence of the Random Strategy towards the Best Strategy
