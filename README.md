# House Price Prediction KingCounty

## Project Overview
A real estate company would like to idntify trends in home sales in King County, WA. There are many considerations when choosing a property to invest in. As thus 

![house_sale_gif](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNGl0NWE1YTBsMWtva3lrc3o4eWUwNHU3ZWtjemJ2a2c1aWd4dmJ6MyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/e8ik35i8LaO3BqRwY6/giphy.gif)

## Business Understanding

## Data
In order to conduct this study, we have access to data on 21,597 residences sold in King County, WA, between 2014 and 2015. Each home's profile featured details on its dimensions, number of bedrooms, bathrooms, and basements, as well as the sizes of the 15 homes that were closest to it. It also included information on its location, whether it was on the water, and its view.

## Methods
DATA cleaning and preprocessing involved:
* exploratory data analysis
* removing features that have no meaning or relation to the price of a property
* feature scaling and transforming
* Dealing qith null values
* transforming qualitative data into numerical information
* feature engineering

## Modelling

### Model1: Relation of size of living area to price
The size of living area i.e the square footage was found to be highly correlated to the value of a property. The R-squareed of .432 reveals that 43.2% of variability observed in the target variable is explained by this model.
This is not as high as expected.
The formula: 
$price_log = 7.0424 log_sqft_living + 0.7946 $

### Model2:
Adding all columns into the Multiple Linear Regresion model. Gave a higher adjusted R-squared of .582 indicating that 58.2% of variability observed in the target variable is explained by this model.
This is not as high as expected.

Intercept             7.7255      
log_sqft_living       0.2579      
bathrooms            -0.0276      
bedrooms             -0.0184      
floors                0.0309     
waterfront            0.3374     
condition             0.0973      
grade                 0.1790      
has_basement          0.1234      
view_EXCELLENT        0.1658      
view_FAIR             0.0563

### Model3: Area of the property to the value
This model had the highest Adjusted R- squared giving a .653 revealing that 65.3% of variability observed in the target variable is explained by this model.

Intercept             5.7589      
log_sqft_living       0.5720      
region_east          -0.0298      
region_north         -0.2110      
region_south         -0.5231      
log_sqft_living15     0.4134


## Conclusion:
The

## Next steps
1. The number of rooms ie bedrooms and bathrooms can be an area of interest as it is known that it would impact the value of a property.
2. Evaluate homes based on what year they were built(by decade built) and compare whether renovation is necessary
3. Evaluate what other areas of home can greatly impact price for renovated and non-renovated homes (e.g., kitchen, garage, etc.)

## Repository Structure
├── visualizations
│   ├── waterfront_or_no_waterfront.png
│   ├── condition_vs_price.png
│   ├── region_with_the_highest_value_houses.png
│   ├── city_with_highest_value_houses.png
├── Data
│   ├── kc_house_data.csv
│   ├── zip_city.csv
│   ├── column_name.md
├── .env
├── .gitignore
├── CleanedPriceLog.xlsx
├── LICENSE.md
├── README.md
├── student.pdf
├── presentation.pdf
