---
layout: article
title: Utility of land investing
custom_css: article.css
include_mathjax: true
---

In this article, we want to calculate the utility of land investing. This calculation will allow us to not only select from different asset classes, such as land vs. index fund, but also select from multiple options of land. 

Based on our current understanding, the utility of land is a function of monetary return, territory, risk, and liquidity, as below:

$$
U_{land} = \frac{M × T}{R × L}
$$

Where:
+ M: monetary growth
+ T: territory size
+ R: risk, i.e. standard deviation
+ L: liquidity, i.e. time required to liquidate the asset

Monetary growth, $M$, is calculated as the following:

$$
M = w × \frac{\text{Total net gain}}{\text{Total cost}}
$$

$$
= w × \frac{FV + Y - (P + C)}{P+C}
$$

Where: 

+ $w$: weight of monetary growth
+ $FV$: future value of the asset considering the appreciation and carrying cost such as tax and maintenance.
+ $Y$: total revenue from the asset during the ownership, such as rent or profit from agricultural production
+ $P$: initial price (investment) of the asset
+ $C$: fees for owning the asset, such as closing cost for purchasing land, or fees for purchasing stocks.


To calculate the future value of land, we need to consider its annual appreciation, and annual costs such as taxes and maintenance cost.

$$
FV = P×(1+a−t−m)^n 
$$

Where:

+ P: initial investment

+ a: annual appreciation rate

+ t: property tax rate

+ m: maintenance cost rate

+ n: years

The yield of land can come from rent, agricultural production, timber harvesting, etc. It can be calculated as following:

$$
Y = Rv × \frac{(1+g)^n−1}{g}
$$

Where: 

+ Rv: revenue of the first year of owning the land

+ g: annual rental growth rate, if any


So, the monetary utility of land investing is:

$$
M = w × (\frac{P×(1+a−t−m)^n + Rv × \frac{(1+g)^n−1}{g}}{P+C} - 1)
$$

Based on the above equation, in order to increase the monetary utility, we can lower $P$, $C$, $t$, and/or $m$, or increase $a$, $Rv$, or $g$.




Next, we look at the calculation of the territory variable:

$$
T = β × e^{s}
$$

Where:

+ $β$: weight of territory 
+ $s$: area of the land (acres)
  
Calculation of risk:

$$
R = λ × σ^2
$$

Where:
+ $λ$: risk preference or weight of risk
+ $σ$: variance of the market price of the asset

Calculation of liquidity:
$$
L = k × log(D)
$$

Where:

+ $k$: weight of liquidity
+ $D$: days it takes to liquidate the asset

Therefore, the total utility $U$ is:

$$
U_{land} = \frac{M × T}{R × L}
$$

$$
U_{land} = \frac{ w(\frac{P×(1+a−t−m)^n + R × \frac{(1+g)^n−1}{g}}{P+C} - 1) (β × e^{s})}{(λ × σ^2)(k × log(D))}
$$


## Land A vs. Land B ##

Now let's look at an example of using the above utility function to compare two pieces of lands. The table below shows the data of Land A and B. By plugging the data into the above function, we calculated the utilities of the two assets, as shown in Figure 1. 


    
![png](/assets/images/2025-05-03-utility-of-land-investing_files/2025-05-03-utility-of-land-investing_6_0.png)
    



    
![png](/assets/images/2025-05-03-utility-of-land-investing_files/2025-05-03-utility-of-land-investing_8_0.png)
    


Land A's utility is higher than Land B's (481.04 v.s 159.10) due to the bigger land size (1.00 vs. 0.17 acre) and higher monetary growth resulted from higher revenue (300 vs. 100) and revenue growth rate (0.08 vs. 0.05). 

## Utility of index-fund investing ##

Now let's also calculate the utility of index-fund investing. Since there is no territory involved in owning an index fund, the utility of index fund is only a function of three variables: monetary growth, risk, and liquidity, as the following:

$$
U_{index} = \frac{M}{R × L}
$$

$$
U_{index} = \frac{w(\frac{P × (1 + r)^n}{P+C_{index}} - 1)}{(λ × σ^2)(k × log(D))}
$$

Where: 
+ $P$: initial investment
+ $r$: average annual growth rate (including dividends reinvested into the index fund)
+ $n$: years
+ $C_{index}$: fees to purchase and carry index fund
+ $λ$: risk preference
+ $σ$: variance (standard deviation) of the market price of the asset
+ $k$: weight of liquidity
+ $D$: days it takes to liquidate the asset



## Land vs. Index Fund ##

Let's compare the utility of Land A and Index fund C. The data of the two assets are shown in Table 2:


    
![png](/assets/images/2025-05-03-utility-of-land-investing_files/2025-05-03-utility-of-land-investing_11_0.png)
    



    
![png](/assets/images/2025-05-03-utility-of-land-investing_files/2025-05-03-utility-of-land-investing_13_0.png)
    


Figure 2 shows that the utility of Land B is slightly higher than Index Fund C, because despite Index Fund C has a higher monetary growth (1.59 vs. 1.19) and less liquidity days (1 vs. 90), it doesn't have the territory variable and has higher risk (0.15 vs. 0.1 respectively).

## Conclusion ##

The above analysis showed an example on how to use utility to select a more advantageous asset. It can serve a good foundation for further development, such as:

+ adding more variables to the utility function as we understand more about what can be gained from a piece of land

+ adjusting the weights of the variable as our wealth grow and priorities change.
