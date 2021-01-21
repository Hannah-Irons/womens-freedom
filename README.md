## Udacity Data Science nanodegree: Write a Data Science Blog Post

# An analysis into Women's Freedom using the Human Freedom Index

## Installation

Python 3.8.5 64 bit

Libraries used:
- numpy
- pandas
- os
- matplotlib.pyplot
- sklearn

## Motivation

Freedom is a difficult thing to quantify; it has no units and can't be measured, but it can be categorised and even defined in a way that can be comparable between countries. The Human Freedom Index sets a scale of 0-10 for its freedom factors, they are split into Personal Freedoms and Economic Freedoms. The motivation for this project is to single out and analyse women's freedom and consider if an inherently 'free' country means it's free for everybody.  

The following questions are addressed in the project:

   1. Do the different regions of the world have a distinct looking relationship between Women's rights and 
    their overall freedom status?

The assumption here is that the Women's Social and Security factor's relationship with the overall freedom 
score is culturally driven. Borders between countries have not always been static and in some regions are 
still volatile. Countries that border each other can have a shared cultural history and it is expected that 
the relationship plotted will form clusters. Some tighter than others, and it will be interesting to further
investigate the outliers in the regions. 

   2. For the Region where the Women's SS scores are typically high and the Region where they are typically
    low, is there a high or low variance between countries within the same region and are there cultural 
    similarities in the outliers where Women's SS in particularly low.

An outlier in a country that has equal women's rights will have a very different story to a country in a region 
still struggling for women's rights. But for the region with lowest women's rights are there other factors that 
add to their cultural identity that might give some insights into the discrepancy in women's freedom.

   3. Are there factors that are not in the Human Freedom Index that could better correlate to women's freedom?

This analysis was done outside python as it uses a list of Muslim countries (>95% Muslim representation) that 
implement Sharia Law and a sample of Muslim countries that do not. This is cited and given in the Blog post 
portion of the assignment and as the information needed was directly visible in the Human Freedom Index report
it was a trivial task to note the value into a table. The resulting graph also given in the medium Blog post.

https://hannahirons88.medium.com/the-measures-of-freedom-c564657ce860

The complimentary analysis outside of python demonstrated that there are area's missing or underrepresented in 
the Human Freedom Index as a handful of countries I wanted to look at (that had Sharia law in some variation) 
were not included in the data/report. On the global stage, freedom, or lack of it, is a controversial topic 
especially with regards to a sub set of people (women in this scenario). It is likely that the excluded countries 
would contain a freedom bias in the areas potentially most vulnerable. This led me to form the final question of 
this analysis, which returns to python and this notebook.

   4. Where social freedom data is not available, could it be possible to find correlations in other factors
    strong enough to offer a prediction into whether Women's safety and security are at risk?
    
This is where it not just important to understand your data but where it can be trusted too. The point of this 
question is to build a model to predict a social freedom using only economic factors. The top correlated factors
were pulled out to understand what the strongest factors in the model would be and if they made any sense in them 
being there.

## File descriptions

- Jupyter notebook 
Project_run_file. the first cell contains all the functions used. The following cells break up the analysis. 

- /data/datasets_93172_883723_hfi_cc_2019.csv
2019 data from the Human Freedom Index resourced from Kaggle
LINK: https://www.kaggle.com/gsutters/the-human-freedom-index

- /results
All plots created, formatted and saved by this project.

- Github repo
https://github.com/Hannah-Irons/womens-freedom

## Results

   1. There is a distinct relationship between the women's SS factor and the overall hf_score differentiated by region. First world regions have both a high women's SS score and hf_score, with women's SS being a couple points higher. there is a low variance across these regions (Western Europe, North America, Oceania). In the poorest regions (Sub-Saharan Africa and the middle east and Northern Africa) women's SS and hf_score are some of the lowest and more in line with each out in their relative scales. The variance between the factors is higher and there's a number of outliers.
    
   2. The outliers that demonstrate the lowest women's scores can have varying comparisons between the overall hf_score and we took a deeper look on a case-by-case basis into women's rights in these countries to see if there were any cultural or shared history between these countries. Each country has differences impacting its women’s rights, from militarisation to fgm numbers and marital laws. These types of factors are accounted for in the human freedom index.
    
   3. The analysis revealed that a number of the countries I was reading about had a high Muslim population and as a subset of that some had introduced Sharia Law in some part. Although there are religious factors within the report, they cover scenarios like violent crimes targeted based on religion. But it seemed like some potential correlations missing from the factors in the report. There is some evidence that the overall Religious Freedom factor is not covering the full picture of religious freedom in the report and that on average that if a country holds some form of Sharia Law then it lowers Women's social and security and it correlated more strongly to implemented Sharia Law and correlated much less so to whether the country had a majority (>90%) Muslim population.  
    
   4. The more I dug into the data the more apparent it was where data was missing. Factors related to personal freedoms were more likely to be NaN than economic freedoms. Some countries were not included at all, i.e., North Korea, Afghanistan, Cuba, which would indicate a bias not represented in the missing data. These countries are not likely to have a high freedom score if the data was available. I wanted to play around with the idea of building a simple model using economic factors to predict the personal freedom represented in the Women's social and security factor, to see if vulnerability to women's rights could be predictable or possibly hidden by a strong economical representation. The correlations were poor even for the most strongly correlated factors and the model was a poor predictor (0.54 2dp). This isn't particularly surprising given that the different types are categorised and defined at the beginning of the Human Freedom Index report to represent different freedoms and repressions that it set out to quantify. What remains interesting are the outliers in the report and where freedoms are lacking and any trends that can go part way in explaining what is causing the rights of one kind of people to be lower than another.

Please find my summary for a non-technical audience in a blog post: https://hannahirons88.medium.com/the-measures-of-freedom-c564657ce860

## Acknowledgements
The original data source and reports:

2019 data from the Human Freedom Index resourced from Kaggle
LINK: https://www.kaggle.com/gsutters/the-human-freedom-index
