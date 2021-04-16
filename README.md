# Home Price Rental Prediction Project
## Data Analysis and Machine Learning model created for determining similar zip codes (in terms of median rent), and areas within the U.S. that have experienced large rent fluctuation (positive or negative) in recent years.
Source data taken from Zillow Observed Rent Index (ZORI):

https://www.zillow.com/research/methodology-zori-repeat-rent-27092/

The Zillow dataset has a median rent price sorted by geographic region, by month, for 7 years of data from 2014-2020. It includes the top 100 metro areas in the U.S. and within that, has broken down the median rents by zip code (2,263 total zip codes).  The data has also been factored/adjusted by Zillow for market-skewing features such as unit types and sizes.  Markets may have drastically different dwelling types, and that variation from market-to-market has been accounted for.

The ML model I created in this project will illustrate the changes over time in the median rent of specific markets and/or given zip codes.

One model will illustrate predictions for 2019 based on 2014-2018 data, to simply see how accurate the ML model is versus reality.

A second model will illustrate predictions through the end of 2020 based on the same data, so we may see the "what if" prediction for rental prices in 2020.  We would be using the actual data from year 2019 and 2020 as the testing data, to see how our modeled prediction of prices compares to the reality. Obviously the emergence of COVID-19 during 2020 drastically altered the landscape for home rental prices.  It remains to find out if that unforeseen shock altered the actual market landscape, not exactly something that could be predicted nor accounted for in a standard ML model.

We'll also explore the historic trends of a few of the major metro markets, namely LA, NY and Miami, and how they ended 2020.


