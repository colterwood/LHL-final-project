# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
Determine the relationship between City Bikes stations and points of interest in Turku, Finland using Yelp and Foursquare.

## Process
1. Determine the Points of Interest we will be considering for this research, we chose Restaurant, Bar, Clothing Store, Shoe Store.

2. Extract relevant data for station locations using citybik.es api and convert to DataFrame.

3. Extract point of interest data from Yelp and Foursquare based on the locations of City Bikes stations.

4. Merge the City Bikes data and Point of Interest data into a new DataFrame to simplify modelling and comparison between datasets.

5. Build a regression model and determine the relationship between the location of City Bikes stations and their proximity to relevant Points of Interest in Turku, Finland.

## Results
Unsurprisingly, it was determined that there was little correlation between the chosen Points of Interest and City Bikes stations in Turku, Finland. As both a college town and a transport-based city, City Bikes are relied on as day to day transportation to-and-from work or home. It is also not the type of city that has an influx of Points of Interest throughout the city, rather they are more concentrated to commercial areas and further from residential neighborhoods. Regression results can be viewed in the table below:

### OLS Regression Results
| Metric                    | Value       |
|---------------------------|-------------|
| **Dependent Variable**    | slots       |
| **R-squared (uncentered)**| 0.348       |
| **Adjusted R-squared**    | 0.346       |
| **F-statistic**           | 312.8       |
| **Prob (F-statistic)**    | 2.02e-56    |
| **Log-Likelihood**        | -2306.7     |
| **Observations**          | 588         |
| **AIC**                   | 4615.0      |
| **BIC**                   | 4620.0      |
| **Coefficients**          |             |
| Distance from Station     | 0.0824      |
| **Standard Error**        | 0.005       |
| **T-statistic**           | 17.685      |
| **P-value**               | 0.000       |
| **Confidence Interval**   | [0.073, 0.092] |
| **Durbin-Watson**         | 0.392       |
| **Omnibus**               | 73.246      |
| **Jarque-Bera (JB)**      | 105.590     |
| **Skew**                  | 0.867       |
| **Kurtosis**              | 4.142       |

**Notes:**
1. R² is computed without centering since the model does not contain a constant.
2. Standard Errors assume that the covariance matrix of the errors is correctly specified.


## Challenges 
Foursquare and Yelp datasets contain significant missing data and occassional inaccurate data, such as physical business address actually being the mailing address of the business owner. Majority of inaccuracies are solved by merging the 2 datasets though.


## Future Goals
Full transparency, nothing. Because this is a low value project that doesn't align with the interests of either City Bikes or the businesses, I don't believe there is any value spending additional time on it.
