---
layout: article
title: Hierarchy of wealth building
custom_css: article.css
include_mathjax: true
---

## Introduction ##

The classic story *The Richest Man in Babylon* showed us a hierarchy of wealth building. Its key lessons are three levels of an investing pyramid: 

+ Level one: "save 10% of your salary"

  Survive and stabilize by keeping part of what you earn as the foundation of investing.

  <br>
  
+ Level two: "seek expert's advice"
  
  Grow your savings **steadily** by seeking advice from who are competent. 
  
  <br>
  
+ Level three: "make gold work for you"
  
  Accelerate the growth by reinvesting the children and grandchildren of your savings to grow a golden army.

Following the hierarchy of wealth building is crucial for long-term financial success because it prioritizes stability, minimizes catastrophic risks, and optimizes compound growth not only in **wealth itself**, but also the **options** of acquiring wealth. 


## Define the problem ##

In this article, we want to define:

+ A hierarchy for lifetime wealth building

<br>
  
+ The threshold to advance from one level onto the next.

<br>
  
+ The different sets of options for each wealth level



## Structure of the Hierarchy of Wealth Building  ##

This structure can be visually represented as a chain, where each node is a level $L_i$, branching out as options accumulated and a threshold to advance to the next level:

```
L0 (S0) 
  |
  |(TH0)
  |
L1 (S1)
  |
  |(TH1)
  |
L2 (S2)
  |
  |(TH2)
  |
...
  |
  |(TH(n-1))
  |
Ln (Sn)
```

At each level, the union of all sets $S_i$ for $i \le k$ defines the total available options $\mathcal{O}_k$.

## Implications ##

A **hierarchy** $\mathcal{H}$ of wealth building can be defined as an ordered sequence of discrete levels:

$$
\mathcal{H} = \langle L_0, L_1, \dots, L_n \rangle
$$

Each level $L_i$ is associated with the **total assets** $TA_i$:

$$
TA_i = EF + NCA + RV
$$

Where:

+ $TA_{i}$: Total assets at Level i.

+ $EF$: Emergency fund (cash/liquid assets).

+ $NCA$: Non-cash assets (investments, real estate, businesses).

+ $RV$: Monthly revenue (active + passive income streams).


For Non-cash assets $NCA$, each level $L_i$ is associated with a **set of investing options** $S_i \subseteq \mathcal{G}$, where $\mathcal{G}$ represents the global option space (i.e., the set of all possible options, such as certificate of deposit, index fund, real estate, etc.).

$$
L_i \mapsto S_{i} \subseteq \mathcal{G}
$$

At any level $L_k$, the total accessible option set $\mathcal{O}_k$ is the **cumulative union** of all option sets up to and including that level:

$$
\mathcal{O}_{k} = \bigcup_{i=0}^{k} S_{i}
$$

At any level $L_{i}$, there is a corresponding **threshold** $TH_{i}$ to advance onto the next levl $L_{i+1}$:

$$
L_{i} \mapsto TH_{i}
$$



## Hierarchy of Wealth Building in Detail ##

We assume that there is no debt from the start:

**Level 0 - Grow salary**

+ Total assets:
  
  $$
  TA_{0} = EF_0 + NCA_0 + RV_0
  $$
  
  $$
      = 0 + 0 + RV_{active} 
  $$

  where $RV_{active}$ is the active revenue from jobs and/or small businesses

<br>

+ Set of investing options $S_0$:
  
  $$
  S_0 = \varnothing
  $$

<br>

+ Threshold to advance $TH_0$:

  $$
  RV_{active} = C
  $$
  
  where $C$ is the monthly cost of living.

  <br>

  Grow monthly revenue to cover the cost of living completely, then move up to Level 1 by saving any extra money into emergency fund $EF$, which means:
```
L0 (S0) 
  |
  |(TH0: RV_active = C)
  |
L1 (S1)
```


**Level 1 - Grow savings**

+ Total assets:
  
  $$
  TA_{1} = EF_1 + NCA_1 + RV_1
  $$
  
  $$
      = EF_1 + 0 + RV_{active} 
  $$
  
<br>

+ Set of investing options $S_1$:
  
  $$
  S_1 = \varnothing
  $$

<br>

+ Threshold to advance $TH_1$:
  
  $$
  EF_1 = 3C 
  $$
  
  <br>
  
  Grow emergency fund $EF_1$ to cover 3 months' cost of living through active income (jobs or small businesses), then move up to Level 2 by investing the new revenue $RV_{active}$ in the certificate of deposit (CD, shortest term 3 months), which means:
  
```
L1 (S1) 
  |
  |(TH1: EF1 = 3C)
  |
L2 (S2)
```



**Level 2 - Stabilize savings**

+ Total assets $TA_2$:
  
  $$
  TA_{2} = EF_2 + NCA_2 + RV_2
  $$

  $$
  = 3C + \sum_{i=1}^5 CD_{i} + (RV_{active} + RV_{passive})
  $$
  
  where:
  
  + $CD_{i}$: CDs with terms of maturity: 3 months, 6 months, 1 year, 2 years, 3 years, and 5 years.
  + $RV_{passive}$: Revenue from non-cash assets, such as interests, dividends.

<br>

+ Set of investing options $S_2$:
  
  $$
  S_2 = \{ \text{CD}_{\text{3 months}}, \text{CD}_{\text{6 months}}, ..., \text{CD}_{\text{5 years}} \}
  $$
  
  The strategy for investing will be developed in the near future.
  
<br>

+ Threshold to advance $TH_2$:
  
  $$
  TA_2 = 60C
  $$

  <br>
  
  Grow total asset to cover at least 5 years' cost of living (if you have a stable salary, the number of years can be reduced to 2), then move up to level 3: 

```
L2 (S2) 
  |
  |(TH2: TA2 = 60C)
  |
L3 (S3)
```


**Level 3 - Grow passive income**

+ Total Assets $TA_3$:
  
  $$
  TA_3 = EF_3 + NCA_3 + RV_3
  $$
  
  $$
  = 3C + \sum_{i=1}^j NCA_{i} + (RV_{active} + RV_{passive})
  $$
  
  where:
  
  + $NCA_{i}$: non-cash assets in CDs, index funds, real estates, dividend ETFs, etc.

<br>

+ Set of investing options $S_3$:

  $$
  S_3 = S_2 \cup \{ \text{broad index funds}, \text{dividend ETFs}, \text{real estates}, ... \}
  $$
  
<br>

+ Threshold to advance $TH_3$:

  $$
    RV_{passive} = C
  $$
  
  <br>
  
  Grow passive income through non-cash assets (moderate risks and return rate) till it can completely cover the cost of living:

  
```
L3 (S3) 
  |
  |(TH3: RV_passive = C)
  |
L4 (S4)
```



**Level 4 - Accelerate passive income**

+ Total Assets $TA_4$:

  $$
  TA_4 = EF_4 + NCA_4 + RV_4
  $$

  $$
  = 3C + \sum_{i=1}^j NCA_{i} + (RV_{active} + RV_{passive})
  $$

<br>

+ Set of investing options $S_4$:

  $$
  S_4 = S_3 \cup \{ \text{sector index funds}, \text{growth stocks}, \text{dividend stocks}, \text{growth real estates}, ... \}
  $$
  
<br>

+ Threshold to advance $TH_4$:

  $$
    RV_{passive} = CSB
  $$

  where:
  + $CSB$: Cost for starting and operating a high-growth small business (e.g. < 1 million).
  
  <br>
  
  Add high-growth assets, such as growth stocks, dividend stocks, into the portfolio to produce more cash flow and appreciation. The cash flow can cover the cost of starting and running a high-growth and high-impact venture, such as micro-lending institution, a credit card company, and a paid course or certification program for wealth building:

  
```
L4 (S4) 
  |
  |(TH4: RV_passive = CSB)
  |
L5 (S5)
```


**Level 5 - Grow proactive income**

+ Total Assets $TA_5$:

  $$
  TA_5 = EF_5 + NCA_5 + RV_5
  $$

  $$
  = 3C + \sum_{i=1}^j NCA_{i} + (RV_{active} + RV_{proactive} + RV_{passive})
  $$

  where:

  + $RV_{proactive}$: proactive revenue from high growth businesses

<br>

+ Set of investing options $S_5$:

  $$
  S_5 = S_4 \cup \{ \text{paid course program}, \text{micro-lending company}, \text{credit card company}, ... \}
  $$
  
<br>

+ Threshold to advance $TH_5$:

  $$
    RV = CMB
  $$

  where:

  + $CMB$: Cost for starting and operating a high-growth middle-size business (e.g. 1 million < $CMB$ < 5 million).
    
<br>

  Add high-impact and high-growth ventures, such as a micro-lending institution, a credit card company, and a paid course or certification program for wealth building, to the investing options $S_5$, in order to diversify from passive income to high-scale proactive profit:

  
```
L5 (S5) 
  |
  |(TH5: RV = CMB)
  |
L6 (S6)
  |
 ...
  |
Ln (Sn)
```

Level 6 to Level n will be define in the future.

## Visualize the Hierarchy of Wealth Building ##

The complete hierarchy of wealth building is presented as following:

```
L0-Grow Salary (S0) 
  |
  |(TH0: RV_active = C)
  |
L1-Grow Savings (S1)
  |
  |(TH1: EF1 = 3C)
  |
L2-Stabilize Savings (S2)
  |
  |(TH2: TA2 = 60C)
  |
L3-Grow Passive Income (S3)
  |
  |(TH3: RV_passive = C)
  |
L4-Accelerate Passive Income (S4)
  |
  |(TH4: RV_passive = CSB)
  |
L5-Grow Proactive Income (S5)
  |
  |(TH5: RV = CMB)
  |
L6 (S6)
  |
 ...
  |
Ln (Sn)

```

## Conclusion ##

The hierarchy of wealth building shows a path from earning salary to financial freedom and then to high-scale proactive profit. It is also a path from being a worker, who sells his labor and time to cover life expenses, to someone, who proactively acquires more wealth through his army of wealth. 

Moving forward, the work done in this article also provides a framework for developing actual investing options and strategies to progress on the hierarchy.
