# Home Price Rental Predictions
## Machine Learning model created for determining similar zip codes (in terms of median rent), and areas within the U.S. that have experienced large rent fluctuation (positive or negative) in recent years.
Source data taken from Zillow Observed Rent Index (ZORI):

https://www.zillow.com/research/methodology-zori-repeat-rent-27092/

The Zillow dataset has a median rent price sorted by geographic region, by month, for 7 years of data from 2014-2020. It includes the top 100 metro areas in the U.S. and within that, has broken down the median rents by zip code.  The data has also been factored/adjusted for market-skewing features such as unit types and sizes.  Markets may have drastically different dwelling types, and that variation from market-to-market has been accounted for.

The ML model I created in this project will illustrate the changes over time in the median rent of specific markets and/or given zip codes, and given current trends, can predict which areas may continue to see increases or decreases in median rent for future years.
