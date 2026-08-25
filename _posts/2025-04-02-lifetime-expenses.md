---
layout: article
title: How much money do we spend in a lifetime?
custom_css: article.css
include_mathjax: true
---

## Introduction ##

Most people want to make money, but few think about why they need money and how much money they need. In this article we want to answer the following questions:

+ How much is the lifetime expense for an average person?
+ How different can the lifetime expense be in different countries with different levels of economic development?
+ How different can the lifetime expense be under different lifestyles?
+ How much money is still required under the minimum lifestyle?


## Three stages ##

The average life expectancy in America is 78 years old. Let's divide the life of an average person into three stages:

+ Childhood and early adulthood (0-23)
  
   The person was born healthily, and his parents could afford the average cost of living and insurance. He went to public schools, and finished public college at the age of 23. 
  
+ Adulthood (24-60)
  
  He started working after college, and continued his life at the average cost of living, rented an apartment, and used public transportation. To simplify the initial calculation, we use renting as the only option for housing, and public transportation for transportation. He paid health and home insurances.
  
+ Retirement (61-78)
  
  After retiring at 60, his expenses included average cost of living, rent, public transportation and insurances.

## Calculation of expenses ##

The three stages will be calculated separately:

**Childhood and early adulthood (0-23)**: 

$$
E_{childhood} =  \sum_{i=1}^{23} (C_{cl} + C_{chin}) (1 + f)^{i-1} + C_{education}
$$
    
Where:

+ $E_{childhood}$ is the total expense from age 0 to 23
+ $C_{cl}$ is the annual cost of living for children, which is 80% of the cost for adults
+ $C_{chin}$ is the annual health insurance payment for children, which is 80% of the cost for adults
+ $C_{education}$ is the total tuition for college
+ $f$ is the average inflation rate. 

**Adulthood (24-60)**: 


$$
E_{adulthood} = \sum_{i=24}^{60} (C_{al} + C_{arent} + C_{atr} + C_{ahin} + C_{arin}) (1+f)^{i-24} 
$$

Where:

+ $E_{adulthood}$ is the total expense from age 24 to 60
+ $C_{al}$ is the annual cost of living for adults
+ $C_{arent}$ is the annual rent for adults
+ $C_{atr}$ is the annual cost for public transportation for adults
+ $C_{ahin}$ is the annual health insurance payment for adults
+ $C_{arin}$ is the annual renting home insurance 
+ $f$ is the average inflation rate. 

Considering the inflation rate and its influence on cost of living and insurance, we have the following relationship between the cost of living and health insurance of childhood and adulthood:

$$
C_{al} = \frac{C_{cl}}{0.8}(1+f)^{23}
$$

$$
C_{ahin} = \frac{C_{chin}}{0.8}(1+f)^{23}
$$

**Retirement (61-78)**: 

$$
E_{retirement} = \sum_{i=61}^{78} (C_{rl} + C_{rrent} + C_{rtr} + C_{rhin} + C_{rrin} ) (1+r)^{i-61}
$$

Where:

+ $E_{retirement}$ is the total expense from age 61 to 78
+ $C_{rl}$ is the annual cost of living for the retired people
+ $C_{rrent}$ is the annual rent for the retired
+ $C_{rtr}$ is the annual cost for public transportation for the retired
+ $C_{rhin}$ is the annual health insurance payment for the retired
+ $C_{rrin}$ is the annual renting home insurance 
+ $f$ is the average inflation rate

Considering the inflation rate and its influence on cost of living and insurance, we have the following relationship between the cost of living, rent, transportation, and insurance of childhood and adulthood:

$$
C_{rl} = C_{al}(1+f)^{36}
$$

$$
C_{rrent} = C_{arent}(1+f)^{36}
$$

$$
C_{rtr} = C_{atr}(1+f)^{36}
$$

$$
C_{rhin} = C_{ahin}(1+f)^{36}
$$

$$
C_{rrin} = C_{arin}(1+f)^{36}
$$

## The lifetime expense in different countries ##

We calculated the average lifetime expenses in four countries:

+ the United States
+ China
+ Ecuador
+ Argentina

In our calculation, we used the following data ([Numero.com](https://www.numbeo.com/cost-of-living/country_result.jsp?country=United+States)):

+ the United States:
    + average public college tuition: $11260/year
    + average cost of living for an adult: $1171.1/month
    + average health insurance: $8951/year
    + average rent: 1436.84/month
    + average home insurance: $240/year
    + average cost of public transportation: $65/month
      
+ China:
    + average public college tuition: $823.05/year
    + average cost of living for an adult: $521.2/month
    + average health insurance: $54.85/year
    + average rent: $268.03/month
    + average home insurance: 0
    + average cost of public transportation: $24.63/month

+ Ecuador:
    + average public college tuition: 0
    + average cost of living for an adult: $532.5/month
    + average health insurance: $552/year
    + average rent: $273.93/month
    + average home insurance: 0
    + average cost of public transportation: $25/month

+ Argentina:
    + average public college tuition: 0
    + average cost of living for an adult: $678.1/month
    + average health insurance: 0
    + average rent: 334.73/month
    + average home insurance: 0
    + average cost of public transportation: $21/month

Note: home insurance is only common in the US, often required by landlords or banks.


    
![png](/assets/images/2025-04-02-lifetime-expenses_files/2025-04-02-lifetime-expenses_5_0.png)
    


Figure 1 shows, if a person is born in 2024 and lives till the age of 78, how the total expense grows with time in those four countries. Due to the high cost of living and health insurance, the lifetime expense grows much faster in the US. Also as shown in Figure 2, the total expense will be 6.04 million dollars in the US, much higher than the total expense in other countries: 1.21 million in China, 1.30 million in Ecuador, and 1.54 million in Argentina.


    
![png](/assets/images/2025-04-02-lifetime-expenses_files/2025-04-02-lifetime-expenses_7_0.png)
    


## Advanced lifestyle ##

In reality, on top of the simplified calculation above, many people are not satisfied with renting and public transportation, which will result in other major purchases, such a house and a car. Considering these major costs, while the expense during childhood remains the same as the basic lifestyle, the expense during adulthood and retirement can be calculated as following:

**Adulthood (24-60)**: 

$$
E_{adulthood} = \sum_{i=24}^{60} (C_{al} + C_{insurances}) (1+f)^{i-24} + C_{house} + C_{cars}
$$

Where:

+ $C_{al}$ is the average cost of living for an adult
+ $C_{insurances}$ includes health, home, and car insurances
+ $C_{house}$ is the average cost for a single-family house
+ $C_{cars}$ is the cost for cars, including three cars plus inflation since the average lifespan of a car is 15 years.

**Retirement (61-78)**: 

$$
E_{retirement} = \sum_{i=61}^{78} (C_{rl} + C_{insurances}) (1+r)^{i-61}
$$

Where:

+ $C_{rl}$ is the average cost of living for a retired person
+ $C_{insurances}$ includes health, home, and car insurances

If a house and a car is fully purchased before retirement, the major expenses during this period will only include cost of living and insurances (health, home, and car). 

In Figure 3, we compared the basic and advanced lifestyle in the US. In the calculation of the basic lifetime expense, we used the same data as Figure 2. In the calculation of the advanced lifetime expense, we used the following data:

+ average public college tuition: $11260/year
+ average cost of living for an adult: $1171.1/month
+ average health insurance: $8951/year
+ average price for a single-family house: $420,000
+ average price for a Toyota Corolla Sedan (2024): $25,968
+ average home insurance: $2110/year
+ average car insurance: $2685/year


    
![png](/assets/images/2025-04-02-lifetime-expenses_files/2025-04-02-lifetime-expenses_10_0.png)
    


In Figure 3, under the more advanced lifestyle that involves house and multiple car purchases in America, the total lifetime expense will increase from 6.05 million dollars to 7.10 dollars (17%).

Comparing Figure 2 and 3, we can see the influence of changing lifestyle on the total expense seems to be lower than changing country. When a person moves from the US to Argentina and maintain the basic lifestyle, the total expense can decrease 75% (6.05 million to 1.54 million), while a person lower the standard of life quality from advanced to basic within the US can only decrease the total expense by 15% (7.10 million to 6.05 million). Therefore, if your goal is to significantly lower the total expense, moving to other countries with a lower cost of living can be more effective than lowering the standard of life within the same country.

## Remaining expense ##

Sam is very good lowering his expenses. After a lot of hard effort, at the age of 35, he was able to lower his expense to the following level:

+ cost of living: $70/month
  
+ health insurance: $54.85/year
  
+ rent: $30/month
  
+ home insurance: 0
  
+ cost of public transportation: $20/month

If Sam continues this lifestyle, how much money will he still need before death (78 years old)?


    
![png](/assets/images/2025-04-02-lifetime-expenses_files/2025-04-02-lifetime-expenses_14_0.png)
    


Figure 4 shows that under Sam's current lifestyle, the remaining expense of his life is 99,721.74 USD. Meanwhile if Sam moves to those four countries and lives under the basic lifestyle there, the remaining expense of his life will be 462,221.01 USD in China, 498,892.1 USD in Ecuador, 585,894.5 USD in Argentina, and 2,779,641.72 in the US.

Even though Sam did a lot of work to lower his expense, as shown in Figure 4, with the minimum lifestyle, Sam's remaining expense can still grow into a large number due to its compounding effect throughout decades. Therefore, while trying to lower the expense, a reasonable amount of effort needs to be invested into growing wealth to compensate the expense.

## Conclusion ##

From our calculation, we are able to acquire the following understanding:

+ The lifetime expense for the average people can vary significantly due to the country they choose to live in.
  
+ The lifetime expense can vary due to the lifestyle, such as renting vs. owning a home; public vs. private transportation.

+ In order to reduce the lifetime expense, lowering the standard of quality of life might be less effective than moving to another country.
  
+ Even with the minimum lifestyle, the total expense can still grow into a large number due to its compounding effect. While trying to lower the expense, a reasonable amount of effort needs to be invested into growing wealth.

## References ##

+ https://www.cdc.gov/nchs/fastats/life-expectancy.htm
+ https://baijiahao.baidu.com/s?id=1824533769859452187&wfr=spider&for=pc
+ https://www.numbeo.com/cost-of-living/country_result.jsp?country=United+States
