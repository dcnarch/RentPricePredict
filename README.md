# Rental Home Price Prediction Project
## Data Analysis and Machine Learning model created for determining trends and similar zip codes (in terms of median rent), and use past results to model future expectations
Source data taken from Zillow Observed Rent Index (ZORI):

https://www.zillow.com/research/methodology-zori-repeat-rent-27092/

The Zillow dataset has a median rent price sorted by geographic region, by month, for 7 years of data from 2014-2020. It includes the top 100 metro areas in the U.S. and within that, has broken down the median rents by zip code (2,263 total zip codes).  The data has also been factored/adjusted by Zillow for market-skewing features such as unit types and sizes.  Markets may have drastically different dwelling types, and that variation from market-to-market has been accounted for.

## Exploratory Data Analysis

After imputing missing values with the bfill method (using the nearest future rent to fill null), I plotted a histogram showing the distribution of all 2,263 zip codes.

![Distribution of Rental Markets](https://github.com/dcnarch/RentPricePredict/blob/main/images/2020-2017-2014%20Histogram%20Comparative.png)

I also explored the historic trends of a the 3 major metro markets with the most zip codes.
(Los Angeles-Long Beach-Anaheim, CA, New York, NY and Miami-Ft.Lauderdale, FL)

![Market Trends](https://github.com/dcnarch/RentPricePredict/blob/main/images/USMedianRentTrend.png)

Los Angeles appears to have hit a peak, New York was declining, but both the Miami metro markets and all the U.S. as a whole were still increasing as of December 2020.

### Most expensive zip code at end of 2020: 90265 Malibu, CA ($9,986/month)
### Least expensive zip code at end of 2020: 44052 Lorain, OH ($727/month)

## Modeling
The ML models I created for this project utilized the Recurring Neural Network (RNN) method via Keras. Obviously the emergence of COVID-19 during 2020 drastically altered the landscape for home rental prices.  It remains to find out if that unforeseen shock altered the actual market landscape, not exactly something that could be predicted nor accounted for in a standard ML model.

The first model illustrated predictions for 2019 based on 2014-2018 data, to simply see how accurate the ML model is versus reality. For simplicity, I chose a sample zip code in the L.A. metro market to plot (92618) using those 5 years actual results as training data, and 2019 as the testing data.

![2019 Prediction](https://github.com/dcnarch/RentPricePredict/blob/main/images/92618-RentPredict2019.png)

One year of testing data didn't seem to be quite enough.

A second model illustrates predictions through the end of 2020 based on the same training data, so we may see the "what if" prediction for rental prices in 2020.  We would be using the actual data from year 2019 and 2020 as the testing data, to see how our modeled prediction of prices compares to the reality.

![2019 & 2020 Prediction](https://github.com/dcnarch/RentPricePredict/blob/main/images/92618-RentPredict2019and2020.png)

Wow! Much closer between predicted and actual performance for this zip code market.  Despite the 2020 year affected by COVID-19, it seems best to use 2 years' worth of testing data to see the true results.

### Below is the same model, run on the median prices of all metro zip codes in the L.A. Market: 
![LA Market Prediction]https://github.com/dcnarch/RentPricePredict/blob/main/images/LAMetro-RentPrediction2019and2020.png

When predicting the LA market as a whole, the model was a bit more conservative, underestimating the actual rent price increase to come from end of 2018 to end of 2020, but still ended up very close to actual! Looks like the median of all 165 LA metro area zips modeled about the same as my prior single sample.
