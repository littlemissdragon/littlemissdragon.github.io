---
layout: article
title: The making of abandoned cities
custom_css: article.css
include_mathjax: true
publish: true
---

## Introduction ##

In some cities, an oversupply of housing, driven by the collapse of once-thriving industries, has pushed real estate prices to extremely low levels. In this article, we explore what makes certain cities full of abandoned, undervalued properties. We aim to understand the origins of these cities, examine their population changes over time, types of properties, and evaluate their competitiveness through a utility function.

## Historical Reasons for Undervalued Abandoned Properties ##

So far there are 69 cities/counties that have been labeled as rource-depleted cities. And their oversupply of housing is caused by the following trend of development:

1. Rapid Industrialization Built on Natural Resources

Most resource-depleted cities emerged as direct products of the country's rapid industrialization under the planned economy. They were strategically built around abundant mineral or forest deposits, such as FX (coal), YM (oil), and GJ (tin). To support the influx of workers, these cities built vast housing complexes and expanded urban infrastructure on a large scale, often with the expectation that growth would continue indefinitely. Over time, this pattern of development locked these places into heavily centralised, single‑industry economies, leaving them dependent on a single finite resource.

2. Economic Decline and Population Loss

Beginning in the 1980s, after decades of intensive extraction, these resources became exhausted, triggering widespread economic collapse. This natural decline was compounded by legacy issues from the planned era: state-owned enterprises that had once provided housing, healthcare, and schools went bankrupt, leading to massive layoffs and severe strain on local government finances. Severe environmental degradation further hindered any efforts at economic diversification.

As mines closed, jobs disappeared. Many of these cities experienced both population decline and economic contraction. The working-age population—especially younger people—left en masse for larger cities in search of employment. Since the 1990s, many of these cities have lost 20–30% of their population.

Compounding the exodus of young workers is a rapidly aging population. Those who stayed behind are predominantly elderly. The aging population not only deepens the economic malaise but also further depresses the housing market, as older residents downsize or pass away, leaving behind even more vacant properties.

3. The Result: A Persistent Housing Oversupply

Ultimately, the combination of economic decline, population loss, and an aging demographic created a persistent oversupply of housing amid shrinking demand. This oversupply, in turn, created the conditions for deeply discounted, often abandoned real estate.

An illustration of this population loss is shown in Figure 1: between 2000 and 2024, DX lost 45% of its population, and HG lost 24% of its population.


    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_4_0.png)
    


## Types of Residential Buildings ##

In resource-depleted cities, both single-family homes and multi-story apartment buildings were constructed for employees. The choice of which type to build was driven less by preference and more by era and environmental context - the nature of the industry and the spatial organization of work.

+ Mining cities: multi-story apartment buildings

  In mining cities like HG and FX, multi-story apartment blocks dominate due to the high worker density: Mines required a large workforce concentrated in specific areas. Building vertically was the most efficient way to house thousands of workers and their families in limited space. State-owned mining companies built multi-story "company dormitory" style housing.
 
+ Forestry cities: Independent Houses

  In contrast, forestry cities in places like the DX region traditionally built independent houses, not large apartment complexes, because of the dispersed nature of forestry work. Workers are stationed at different forest farms, logging sites, and forest ranger stations. As a result, housing was naturally built as individual, single-floor units that came with a small house and yard.


Based on the above pattern, the following cities that had forestry industry are characterized by independent housing:

+ YC
+ BS
+ DX
+ AES
+ DH
+ WQ

When comparing the population density and GDP per capita across all resource-depleted cities, a clear pattern emerges. All six of these forestry cities rank within the top 10 for the lowest population density (Figure 7). Furthermore, four out of the six rank within the top 20 for the lowest GDP per capita (Figure 8).

Given their distinct industrial history and housing structure, it is worth further examining relative competitiveness of the forestry using our utility function, in order to identify the most undervalued place.


## Utility Calculation ##

We continue to use the utility function defined in the [previous article](https://littlemissdragon.github.io/blog/2026/05/02/regional-competitiveness-analysis):

$$
U = \frac{1}{\lambda P + G + I} 
$$

Where:

+ $\lambda$: coefficient for Population and tourist density
+ $P$: Population and tourist density
+ $G$: GDP per Capita
+ $I$: Population natural increase rate


The utility function is designed to capture the inverse relationship between a city's competitiveness and its decline. We will also use the archetypes developed in the [previous article](https://littlemissdragon.github.io/blog/2026/05/02/regional-competitiveness-analysis) to analyze the forestry cities.

Cities with shrinking populations, negative natural growth rate, and weak GDP per capita will have higher utility scores, and are placed in the "Hollowing-Out/Frontier" archetype. It is a depopulating, remote region with a weak long-term economic outlook.

Overall these forestry cities belong to the "Hollowing-Out/Frontier" archetype. However, as shown in Figure 2, DX has the highest utility (0.23), mainly due to that its number of tourists (127 people/square meters, Figure 5) is the lowest, natural growth rate is also the lowest (18.43‰), and population density is the second lowest (7 people/square meters, Figure 4) among all the forestry cities, despite the GDP per Capita is ranked as fourth (48.7 k yuan/person, Figure 3). This suggests that its relatively high utility is less a sign of economic vitality and more a reflection of its extreme demographic decline.


    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_8_0.png)
    


## Conclusion ##

In this article, we examined the root causes behind the persistently low demand and high supply in the housing markets of resource-depleted cities. By tracing their historical development—from rapid industrialization built on finite natural resources to eventual economic collapse and population decline—we identified how a persistent oversupply of housing emerged amid shrinking demand and an aging demographic. 

We also explored the types of residential properties developed in these cities, and located forestry regions that offer undervalued independent housing and, correspondingly, the lowest population densities. Furthermore, through the utility function analysis, we identifies that among the forestry cities DX has the lowest competitiveness and potentially the most undervalued independent housing. 

## Appendix I ##


    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_11_0.png)
    



    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_12_0.png)
    



    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_13_0.png)
    



    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_14_0.png)
    



    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_16_0.png)
    



    
![png](/assets/images/2026-08-05-the-making-of-abandoned-cities_files/2026-08-05-the-making-of-abandoned-cities_17_0.png)
    

