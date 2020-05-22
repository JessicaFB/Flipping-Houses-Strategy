# Flipping Houses

## An analysis of best predictors of home sale prices using the king county housing dataset

### Author: Jessica Forrest-Baldini

The contents of this repository detail a multiple linear regression analysis using a range of features in the King County Housing dataset to best predict home sale prices.

## Business Problem

A group of real estate investors are new to the area; King County, Washington, home to Seattle and many other towns, cities and neighborhoods. They want to know the best strategy for increasing the value of a home to maximize profits when flipping houses in King County. 

## Data

kc_house_data.csv

Source: https://www.kaggle.com/harlfoxem/housesalesprediction

## Methods 

- Multiple Linear Regression Analysis
- Analysis of the Coefficients

Since many of the data columns/features were skewed, and the model residuals were not normally distributed, I decided to log-transform, normalize and min-max scale the data set.

I also removed extreme outliers that were skewing the normality of the residuals by removing the top and bottom percentile of homes by price and square feet of the lot size. This removed about 2% of the data.

Transforming the data made it so I could not predict exact impact on price, however I did an analysis of the coefficients using a coefficient plot (which I created a function for since seaborn depreciated their coefplot function previously), with 95% confidence intervals. This made it very apparent which features have the greatest impact on home sale prices, so I could effectively gain insights and make valuable strategy suggestions to the real estate investors.

I searched for interactions and added the top interaction into the dataset, which became the best predictor by a landslide and contributed to insights and business strategy recommendations. 

 ## Results

The most influential feature on home sale price was grade
When adding in the top interaction, the most influential feature on home sale price was grade interacting with square feet of living space, which makes total sense and contributes to our business recommendations
There was a clear neighborhood effect at play as well, as we could see with latitude and average square feet of the 15 nearest neighbors’ homes

## Recommendations

Based on the results and findings, I recommend:

- Invest in larger lower grade homes (relative to the neighborhood) and increase the homes grade according to the King County grading scale
- Invest in larger homes on the fringes of relatively more affluent neighborhoods that are bordering more average neighborhoods and increase the grade
- Invest in homes in neighborhoods that are being gentrified and increase the grade  

Grading system used in King County: https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r

Increasing the grade is done by upgrading materials, fixtures and style (both interior and exterior) of the home.

## Further Research

For further research I would recommend doing a neighborhood analysis with a map to gain an understanding of the different neighborhoods in King County; and their respective home price ranges, sizes, grades and conditions. This will allow the strategy outlined above to be applied most effectively.

Also, discover which neighborhoods are undergoing gentrification, or which neighborhoods border more affluent neighborhoods where homes on the fringes could be purchased and upgraded. 

https://www.governing.com/gov-data/seattle-gentrification-maps-demographic-data.html

Data for this can be found at: 

## Thank you!

For any additional questions, please feel free to connect with me at jlforrestbaldini@gmail.com or on LinkedIn at https://www.linkedin.com/in/jessica-forrest-baldini-0468111a4/
