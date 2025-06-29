---
layout: article
title: From Utility to the Optimal Strategy
custom_css: article.css
include_mathjax: true
---

## Introduction ##

The goal of this article is to understand for a certain level of the [Hierarchy of Wealth Building](https://littlemissdragon.github.io/blog/2025/05/24/hierarchy-of-wealth-building), how to: 

+ Define the utility function
  
+ Develop the optimal strategy 

To achieve the above goal, we need to:

+ First, define the relationship among hierarchy, utility, strategy, and investing options, as the foundation of developing the utility function and optimizing the strategy.

  
+ Second, define the utility function.

  
+ Third, calculate the optimal strategy.
  

## The Relationship among Hierarchy, Utility, Strategy and Investing Options ##

As described in the [last article](https://littlemissdragon.github.io/blog/2025/05/24/hierarchy-of-wealth-building), the **Hierarchy** of Wealth Building, $\mathcal{H}$, can be defined as an ordered sequence of discrete levels:

$$
\mathcal{H} = \langle L_0, L_1, \dots, L_n \rangle
$$

Each level $L_i$ is associated with a set of **investing options** $S_i \subseteq \mathcal{G}$, where $\mathcal{G}$ represents the global option space (i.e., the set of all possible options, such as certificate of deposit, index fund, real estate, etc.). 

Meanwhile, it is associated with a set of **investing strategies** $\prod_i$. Each strategy $\pi_i$ is a mixture of some or all the options, or a single option:

$$
\prod i = \{\pi_1, \pi_2, \dots, \pi_n\}
$$

$$
\pi_i = \{(w_1, A_1), (w_2, A_2), \dots, (w_n, A_n)\}
$$

Where:

+ $w_i$: Weight of option $A_i$

+ $A_i$: Investing option

+ Constraints: $\sum_{i} w_i = 1$ and $w_i \geq 0$


For each level $L_i$, to best achieve its goal, we can define an **utility function** $U_i$ to calculate the **optimal strategy** $\pi'$, i.e. the strategy that maximizes the expected utility:

$$
\pi' = \arg\max_{\pi} U_i
$$


Therefore, the relationship among hierarchy, utility, strategy, and investing options can be described as follows:

$$
\underbrace{\text{Hierarchy}}_{\text{When}} \xrightarrow{\text{Goal}} 
\underbrace{\text{Utility}}_{\text{Why}} \xrightarrow{\text{Optimize}} \underbrace{\text{Strategy}}_{\text{How}} \xrightarrow{\text{Select}} \underbrace{\text{Options}}_{\text{What}}
$$


## Utility function ##

Now let's see how to calculate the optimal strategy through a utility function, using [Level 2 (stabilize savings) of the hierarchy of wealth building](https://littlemissdragon.github.io/blog/2025/05/24/hierarchy-of-wealth-building) as an example. (Level 0 and 1 don't involve any investment.)

On Level 2: 

+ Goal: Stably grow total asset to cover at least 5 years' cost of living (if you have a stable salary, the number of years can be reduced to 2)

+ Set of investing options $S_2$:
  
  $$
  S_2 = \{ \text{CD}_{\text{6 months}}, \text{CD}_{\text{1 year}}, \text{CD}_{\text{3 years}}\}
  $$

Let's first define the utility function of an investment portfolio for Level 2. Factors to consider:

+ Return rate

  
+ Variance

  
+ Liquidity

$$
U = \mathbb{E}[R_p] - \frac{1}{2}\lambda V_p - L(T)
$$

Where:

+ $U$: Utility of a portfolio

  
+ $\mathbb{E}[R_p]$: Expected return rate

  
+ $V_p$: Portfolio variance

  
+ $\lambda$: Risk aversion coefficient (higher $\lambda$ means more penalty for risk)

  
+ $L(T)$: Liquidity penalty

$$
\mathbb{E}[R_p] = \sum_{i=1}^N w_i (d_i + g_i)
$$

Where:

+ $w_i$: Weight of asset i in the portfolio

  
+ $d_i$: Dividend yield of asset i

  
+ $g_i$: Expected appreciation (growth rate) of asset i


$$
V_p = \sum_{i=1}^N w_i^2 \sigma_i^2 + \sum_{i=1}^N \sum_{j \neq i} w_i w_j \sigma_{ij}
$$

Where:

+ $\sigma_i^2$: variance of asset i (individual risk). $\sigma_i$ is the standard deviation of asset i.

  
+ $\sigma_{ij}$: covariance between asset i and j (diversification effect)


$$
L(T) = \gamma \sum_{i=1}^N w_it_i
$$

Where:

+ $\gamma$: liquidity penalty coefficient


+ $t_i$: Time for the asset i to maturity



Therefore the utility function is:

$$
U = \sum_{i=1}^N w_i (d_i + g_i) - \frac{1}{2}\lambda (\sum_{i=1}^N w_i^2 \sigma_i^2 + \sum_{i=1}^N \sum_{j \neq i} w_i w_j \sigma_{ij}) - \gamma \sum_{i=1}^N w_it_i
$$


## The Optimal Strategy ##

Through calculating the maximum utility, we can find the optimal strategy. 

To show an example of this process, the following data of CDs are applied to the utility function above. We set $\lambda=2$ and $\gamma=0.2$. And the relationship among weights of 1-year and 3-year CD vs. utility is visualized in Figure 1. 


    
![png](/assets/images/2025-06-11-from-utility-to-optimal-strategy_files/2025-06-11-from-utility-to-optimal-strategy_5_0.png)
    



    
![png](/assets/images/2025-06-11-from-utility-to-optimal-strategy_files/2025-06-11-from-utility-to-optimal-strategy_6_0.png)
    


From Figure 1, we can see that the utility of Level 2 reaches maximum ($U=1.54$) when the investment strategy is:

+ 6-month CD: 0%
+ 1-year CD: 84%
+ 3-year CD: 16%

Thus, we demonstrated a complete process — from defining the utility function to deriving the optimal strategy. The utility function can be adjusted to reflect varying risk tolerance, liquidity preferences, and other goal-dependent factors.

## Conclusion ##

By examining the relationships between hierarchy, utility, strategy, and options, we observe that the hierarchy establishes the goal and key factors for the utility function. Calculating utility then enables us to determine the optimal strategy — a weighted combination of different options.

In the next phase, we will define specific utility functions and derive optimal strategies for each level of the wealth-building hierarchy.
