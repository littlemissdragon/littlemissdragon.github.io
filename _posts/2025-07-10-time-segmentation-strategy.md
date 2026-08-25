---
layout: article
title: Time-Segmentation Strategy
custom_css: article.css
include_mathjax: true
---
## Introduction ##

This article explores a structured investment methodology: the Time-Segmentation Strategy (TSS). We will define a framework for dividing capital based on future financial obligations and demonstrate how to construct optimal, goal-oriented portfolios for each segment by developing tailored utility functions.


## Time-Segmentation Strategy ##

A Time-Segmentation Strategy (also known as a "bucket" or "horizon-based" strategy) is an asset allocation approach that matches investments to specific future financial needs. Instead of managing a single portfolio for all goals, an investor divides their capital into separate segments, each corresponding to a distinct time horizon (e.g., short-term, medium-term, long-term). This allows each segment to be invested in a portfolio that optimally balances risk and return for its specific purpose, enhancing the overall plan's robustness.

## A Formal Framework for Segmentation ##

Consider an investor with a known annual cost of living $C$ and total life expense $W$ (including current wealth and future income). The strategy involves partitioning $W$ into $n$ segments. A Segment ($S_i$) is a collection of one or more consecutive years of expenses $Cs$, grouped based on a shared investment horizon and risk tolerance. (Note: This assumes flat expenses; the model can be extended to include inflation.)

$$
W = \sum_{i=1}^n S_i 
$$

where, for example:

+ $S_1$ (Short-Term): covers Year 1-3

+ $S_2$ (Medium-Term): covers Year 4-10

+ $S_3$ (Long-Term): covers the years beyond Year 10


## Utility Functions and Optimal Portfolios per Segments ##

Each segment $S_i$ has a unique investment objective, which is achieved by selecting an optimal portfolio from a curated set of assets. The process to build these portfolios has three steps: defining permissible investment options, creating a utility function if needed, and optimizing the portfolio to maximize utility.

**Step 1, define the permissible investments for each segment.**

Each segment $S_i$ has a filtered set of permissible investment options $O_i$, drawn from a global universe $\mathcal{O}$.

$$
O_i \subseteq \mathcal{O} 
$$

The filtering is governed by a rule $G_i$ based on the segment's goals:

$$
O_i = \{ A \in \mathcal{O} \mid G_i(A) = \text{True} \}
$$

Where:

+ $\mathcal{O}$: The global investment options space
  
+ $G_i$: The requirement for filtering the options for segment $S_i$
  
+ $O_i$: The set of investment options associated with segment $S_i$
  
+ $A$: The individual investment option

**Step 2, define a segment-specific utility function, if needed**

For each segment, if necessary, we define a utility function that quantifies the trade-off between expected return and risk. A common form is the utility function ($U$) of mean ($R$) and standard deviation ($\sigma$):

$$
U_k(R,\sigma): S_k \rightarrow P_k
$$

**Step 3, optimize the portfolio to maximize utility**

The optimal investment portfolio $P_i^*$ (i.e., the asset weights) for the capital in segment $S_i$ is the one that maximizes its utility function $U_i$ over its investment options $O_i$.


$$
P_i^* = \arg\max_{P} U_i[R(P), \sigma(P)]
$$

## Example ##

Assume an investor has an annual cost of living $C = 8,000$. We define a three-segment strategy for the total life expense $W$:

+ Segment 1 ($S_1$): Short-Term (Years 1-3). Capital: $S_1 = 3C$

+ Segment 2 ($S_2$): Medium-Term (Years 4-10). Capital: $S_2 = 7C$ 

+ Segment 3 ($S_3$): Long-Term (Year 11+). Capital: $S_3 = nC$

**Investment options**

Based on the writer's current knowledge and experience, $\mathcal{O}$ consists the following options: 

+ certificates of deposit (CDs) (China)
  
+ SP (S&P) 500 index fund ETF (USA)
  
+ NASDAQUE 100 index fund ETF (USA)
  
+ Hushen 300 index fund ETF (China)
  
+ CSI dividend low-volatility index ETF (China)
  
+ Hong Kong dividend low-volatility index fund ETF (China)
  
+ DAX 40 index fund ETF (Germany)

+ Cash
  
**Step 1, build Segment 1's portfolio**.

Goal: Capital preservation and high liquidity (funds needed in 1–3 years; no tolerance for loss).

**Step 1.1, define Permissible Investments**

Filter ($G_1$): 

$$
G_1: M_{1y} - D_{1y} > 0
$$

Where: 

+ $M_{1y}$: average annual growth rate of the investment option, including interest, dividend, and/or appreciation.
  
+ $D_{1y}$: annual standard deviation.

Applying this filter, the following options are selected (see Appendix I & II for data on means and standard deviations of all the investment options):

$$
O_1 = \{\text{3-month CD, 6-month CD, 1-year CD, 2-year CD, Cash}\}
$$

**Step 1.2, define Utility Function**

For $S_1$, utility depends almost entirely on liquidity and capital preservation (return is secondary). Thus, $U_1$ simplifies to: "Maximize liquidity (match CD maturity to expense timing) while ensuring no loss of principal."

**Step 1.3, optimize to find $P_1^*$**

Since $O_1$ consists of CDs (fixed maturity, no principal loss) and cash (instant liquidity), $P_1^*$ is designed to match CD maturities to annual expenses:

+ Cash: $0.25C$, to cover Q1 expenses.
  
+ 3-month CD: $0.25C$, to cover Q2 expenses.
  
+ 6-month CD: $0.5C$, to cover Q3 and Q4 expenses.
  
+ 1-year CD: $C$, to cover Year 2 expenses.
  
+ 2-year CD: $C$, to cover Year 3 expenses.


**Step 2, build Segment 2's portfolio**


Goal: Moderate growth with controlled risk. This segment has a longer time horizon than Segment 1 (funds needed in 4–10 years), allowing it to accept more market volatility in pursuit of higher returns.

**Step 2.1, define permissible investments**

Filter ($G_2$): To meet the above objective, assets must have demonstrated positive risk-adjusted returns over a relevant medium-term period. The filter rule $G_2$ requires that an asset's average 3-year return ($M_{3y}$) has exceeded its 3-year standard deviation ($D_{3y}$):

$$
G_2: M_{\text 3y} - D_{\text 3y} > 0
$$

Using the above filter and asset data in Appendix I, the following options are selected:

$$
O_2 = \{ \text{3-year CD}, \text{CSI Dividend Low-Volatility Index}, \text{SP 500 index} \}
$$

**Step 2.2, define utility function**

Based on the actual data of average return rates and standard deviations of $O_2$ (Appendix II), we choose to use linear mean-standard deviation utility function, i.e. You are willing to accept more risk if you are compensated with a linearly increasing amount of return:

$$
U_2 = \gamma R - \lambda \sigma
$$

$$
U_2 = \gamma \sum_{i=1}^N w_i r_i -  \lambda \sqrt{
    \sum_{i=1}^N w_i^2 \sigma_i^2 +
    \sum_{i=1}^N \sum_{j \neq i} w_i w_j \sigma_{ij}
}
$$

Where:

+ $\gamma$: Coefficient for return rate. 

+ $w_i$: Weight of asset i in the portfolio

+ $r_i$: Expected appreciation (growth rate and dividend rate) of asset i

+ $\lambda$: Risk aversion coefficient (higher $\lambda$ means more penalty for risk). 

+ $\sigma_i^2$: variance of asset i (individual risk). $\sigma_i$ is the standard deviation of asset i.

+ $\sigma_{ij}$: covariance between asset i and j (diversification effect)

The coefficients $\gamma = 1$ and $\lambda = 1$ explicitly encode the strategy's preference: return is as important as risk reduction in the utility calculation.

**Step 2.3, optimal portfolio**

Using the asset data in Appendix II, we solve for $w_i$ (weights) that maximize $U_2$:

    Optimal Allocation Details for Segment 2:
    S&P 500 weight                               0.35
    CSI Dividend Low-Volatility Index weight     0.60
    3-year CD weight                             0.05


**Step 3, build Segment 3's portfolio**

Goal: Maximize long-term growth. This segment has the longest investment horizon (funds needed in Year 11 and beyond), allowing it to fully tolerate short-term market volatility in exchange for the highest expected returns. 

**Step 3.1, define permissible investments**

Filter ($G_2$): To select assets suited for aggressive long-term growth, the filter $G_3$ requires a strong historical track record. An asset is included only if its average 10-year return ($M_{10y}$) has exceeded its 10-year standard deviation ($D_{10y}$):

$$
G_3: M_{\text 10y} - D_{\text 10y} > 0
$$

Using the above filter and the asset data in Appendix I, the following options are selected:

$$
O_3 = \{ \text{SP 500 index}, \text{NASDAQ 100 index}, \text{DAX 40} \}
$$

**Step 3.2, define utility function**

Based on the actual data of average return rates and standard deviations of $O_3$ (Appendix II), we continue to use mean-standard deviation utility function:

$$
U_3 = \gamma R - \lambda \sigma
$$

$$
U_3 = \gamma \sum_{i=1}^N w_i r_i - \lambda \sqrt{
    \sum_{i=1}^N w_i^2 \sigma_i^2 +
    \sum_{i=1}^N \sum_{j \neq i} w_i w_j \sigma_{ij}
}
$$

The coefficients $\gamma = 2$ and $\lambda = 1$ explicitly encode the strategy's preference: return is twice as important as risk reduction in the utility calculation.

**Step 3.3, optimize utility**



    Optimal Allocation Details for Segment 3:
    S&P 500 weight                               0.75
    NASDAQ100 weight                             0.25
    DAX 40 Index weight                          0.00


## Conclusion ##

By grounding decisions in time horizons, risk tolerance, and measurable utility, TSS empowers investors to pursue growth without sacrificing security—ultimately building a more predictable path toward financial stability. The practical example further illustrates TSS’s flexibility: even with a modest initial wealth, the strategy scales to cover decades of expenses by combining current capital with future income, ensuring each phase of an investor’s financial journey is supported. For long-term segments (Years 11+), TSS also leverages the power of compounding by permitting higher allocations to growth assets. 

Moving forward, as we gain knowledge on more investment options, we will continue to expand the investment universe and improve this strategy.


## Appendix I ##

The following figures shows the average return rates and standard deviations of various periods of all the investment options considered in this article. The length of time horizon is determined by the length of existence of the investments.


    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_9_0.png)
    



    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_12_0.png)
    



    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_14_0.png)
    



    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_15_0.png)
    



    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_17_0.png)
    



    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_20_0.png)
    



    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_22_0.png)
    


## Appendix II ##

Table 1 presents the data of the average annual return rates and standard deviations of all the investment options considered in this article.


    
![png](/assets/images/2025-07-10-time-segmentation-strategy_files/2025-07-10-time-segmentation-strategy_24_0.png)
    


## References ##

+ https://baijiahao.baidu.com/s?id=1802034225405933396&wfr=spider&for=pc
+ https://xueqiu.com/8821615579/328936666
+ https://www.nasdaq.com/market-activity/index/ndx/historical?page=252&rows_per_page=10&timeline=y10
