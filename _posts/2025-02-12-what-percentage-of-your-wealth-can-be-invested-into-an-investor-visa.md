---
layout: article
title: What percentage of your wealth can be invested into an investor visa?
custom_css: article.css
include_mathjax: true
---
If you are considering investing in an investor visa, what percentage of your wealth can be invested, in order to gain more advantage than the current state?

## Define the problem ##

Goal: Gain more advantage by extending the time purchased by the current wealth

How can an investor visa potentially help us achieve the above goal: 

+ decrease the cost of living
+ increase the passive income

However, one prerequisite for acquiring this advantage is that an **appropriate** percentage of wealth is into an investor visa for a required amount of time, to guarantee more months purchased by the total wealth in the foreign country than in the current nation. 


Then what percentage can fulfill this prerequisite?

Our calculation includes two sections:
+ Section 1: The cost of living is covered by the remaining wealth and monthly interest
+ Section 2: The cost of living is covered by the remaining wealth, monthly interest, and principal


## Section 1 - remaining wealth and monthly interest ##

The total wealth is $W$, by investing $p$ percent of $W$ into a certificate of deposit (CD) for $T$ years with an annual interest rate $I$, you can acquire an investor visa. As the investment starts, your cost of living can change from $C_{domestic}$ to $C_{foreign}$. Meanwhile, interest will be received monthly, starting from the end of the first month. When the CD expires, another one-year term at the same interest rate will be initiated to gain more interest. During this period of time (i.e. spending the remaining wealth and monthly interest), the number of additional months, $\Delta{N}$, is calculated as following:

$$
\Delta{N} = N_{foreign} - N_{domestic} 
$$

$$
= \frac{(1-p)W}{C_{foreign} - \frac{pWI}{12}} - \frac{W}{C_{domestic}}
$$


Now let us visualize a specific example of section 1. Say you have $62,000$ USD in savings (the average US savings circa 2022), and the average American cost of living is $1164.4$ USD/month (Numbeo circa 2024). You are considering moving to Ecuador, whose average cost of living is $532.2$ USD/month (Numbeo circa 2024). Its investor visa requires $40,000$ USD minimum in the CD for at least $2$ years at an interest rate of $6.5%$ (Banco Pichincha 2025).


    
![png](/assets/images/2025-02-12-what-percentage-of-your-wealth-can-be-invested-into-an-investor-visa_files/2025-02-12-what-percentage-of-your-wealth-can-be-invested-into-an-investor-visa_6_0.png)
    


Figure 1 shows us the following points:

+ In general, the higher p is, the lower $\Delta{N}$ you will get. And the reduction rate of $\Delta{N}$ grows as p increases.

+ The green line is the advantage threshold, which indicates as long as $p<0.76$ (i.e. investment < $47,120$ USD), $\Delta{N} > 0$, which means you can already gain more time from the remaining wealth and interest in the Ecuador than from the total wealth in America.

+ Ecuador, whose investor visa requires $40,000$ USD, is below the advantage threshold, as shown by the orange line. By investing $40,000$ USD into Ecuador, $\Delta{N} = 16.5$.

+ Besides the amount required for an investor visa, there is another factor: $2$ years in the CD. This means within those two years, you can only depend on the remaining wealth and monthly interest, and the principal cannot be withdrawn. The red line shows the maximum $p$ value ($p=0.91$) considering this condition. So as long as $p < 0.91$, you can safely acquire an investor visa. After acquiring the visa, you are free to withdraw the principal and spend it on the cost of living.

+ If we want to increase the advantage threshold p, which can potentially give us more options, we can find countries that provide a $C_{for} < 532.2$ USD, or $I > 0.065$, given the current total wealth and cost of living in America.


In section one we only considered the remaining wealth and interest, what if we add the principal to the equation, how much more time would we get?


## Section 2 - remaining wealth, interest, and principal ##

After the remaining wealth and interest are completely spent on cost of living, the principal will be withdrawn to pay for the cost of living. The total $\Delta{N}$ is calculated as following:

$$
\Delta{N} = N_{foreign} - N_{domestic} + N_{principal}
$$

$$
= \frac{(1-p)W}{C_{foreign} - \frac{pWI}{12}} - \frac{W}{C_{domestic}} + \frac{pW}{C_{foreign}}
$$

Note: Once you have lived in the foreign country longer than T years and you are already qualified for a permanent residency, the principal can be withdrawn at any time. But in our calculation, to maximize $\Delta{N}$, we only withdraw the principal after the remaining wealth is completely spent.


    
![png](/assets/images/2025-02-12-what-percentage-of-your-wealth-can-be-invested-into-an-investor-visa_files/2025-02-12-what-percentage-of-your-wealth-can-be-invested-into-an-investor-visa_10_0.png)
    


Now let's continue to use Ecuador as an example to visualize section 2. The data used in the calculation are the same with the example in section 1:

+ $W = 62,000$ USD
+ $C_{domestic} = 1164.4$ USD
+ $C_{foreign} = 532.2$ USD
+ $I = 0.065$
+ Required investment for an investor visa: $40,000$ USD
+ Required time in the CD: $2$ years

From Figure 2, we can see that:

+ The orange line indicates that, for the actual required investment ($40,000$ USD), $\Delta{N} = 91.6$, which means given the current wealth you will be able to live in Ecuador for ~$12$ years, but ~$4.4$ years in America.
  
+ The orange line is very close to the pink line, which is the p value that gives you the maximum $\Delta{N}=91.7$ months.

+ At any percentage between 0 to 1, $\Delta{N}$ is positive due to the lower cost of living. However, as we have calculated in section 1, to fulfill the 2-year policy to acquire an investor visa, $p$ has to be equal to or lower than $0.91$. This means, if, for some reason, you want to invest as much as possible into the CD while acquiring an investor visa, the maximum percentage is 91%. Thus you will get 77 additional months from the total wealth in Ecuador than in America. This is significantly lower than the red line, so if your goal is to maximize $\Delta{N}$, it is not advisable to invest more than $40,000$ USD in the CD.


Here you might wonder, what if we only withdraw part of the principal and keep the rest in CD to generate interest? Yes, you can definitely do that, which will offer you even higher $N_{foreign}$, but we'll save that calculation for another article. 

## Advanced calculation - interest only ##

What if we want the passive income (interest) to cover the cost of living completely, how much the total wealth or how high the interest rate needs to be?

$$
C_{for} = \frac{pWI}{12}
$$

The above goal (i.e. financial freedom) can be achieved in the following scenarios:

+ The total wealth $W$ > $98,252$ USD, given I = 0.065 and p = 1
+ The annual interest rate $I$ > $0.103$, given W = $62,000$ USD and p = 1

## Conclusion ##

The access to lower cost of living and higher interest rate of CD can potentially offer us enormous advantage. Through the above calculation, we will be able to find the right combination of total wealth, required investment, interest rate, and cost of living to optimize the time purchased by the wealth. Even more advantageous, with the right combination of total wealth and interest rate, we can potentially achieve financial freedom.

In reality, the interest rate of CD is not always stable, so as an investor, beyond the purpose of obtaining an investor visa, how can we diversify our portfolio to lower the risk and increase the return? In the following articles, we will be exploring other asset classes.
