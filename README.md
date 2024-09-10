# Yulu Business Case Study

## Overview
This project aims to analyze the factors influencing the demand for Yulu shared electric cycles in the Indian market. The analysis focuses on identifying key variables affecting demand, and how they contribute to predicting rental patterns. By understanding these factors, the company can optimize its operations, tailor marketing strategies, and better meet customer demands.

## Dataset Description
The dataset consists of 12 key variables:
- `datetime`: Date and time of the rental (in hourly intervals).
- `season`: Season indicator (1: Spring, 2: Summer, 3: Fall, 4: Winter).
- `holiday`: Whether the day is a holiday (1) or not (0).
- `workingday`: Whether the day is a working day (1) or not (0).
- `weather`: Weather conditions categorized into 4 types:
  1. Clear or partly cloudy
  2. Mist or cloudy
  3. Light snow or rain
  4. Heavy rain or snow
- `temp`: Actual temperature in Celsius.
- `atemp`: "Feels like" temperature in Celsius.
- `humidity`: Humidity level (0 to 100).
- `windspeed`: Wind speed in km/h.
- `casual`: Number of casual users (unregistered).
- `registered`: Number of registered users.
- `count`: Total number of rented cycles (casual + registered).

## Business Problem
The company wants to:
1. Identify key variables influencing the demand for shared electric cycles.
2. Understand how well these variables describe consumer demand and behavior.

## Insights from Analysis

### 1. Demand Patterns
- **Weather Impact**: Clear weather (weather category 1) and misty conditions (weather category 2) saw the highest rental counts. Severe weather conditions such as rain or snow (weather categories 3 and 4) significantly reduced demand.
- **Temperature**: Rentals peak when the temperature is around 20-30°C, suggesting that moderate temperatures attract more users.
- **Humidity and Windspeed**: Rentals decrease as humidity and windspeed increase, with casual users more sensitive to weather changes than registered users.
  
### 2. Seasonal Trends
- **Spring (Season 1)**: Lowest average rentals with occasional spikes.
- **Fall (Season 3)**: Highest rental demand, likely due to favorable weather conditions.
- **Summer (Season 2) & Winter (Season 4)**: Similar demand patterns, but winter shows less variability.

### 3. User Type Behavior
- **Casual Users**: More influenced by temperature and weather conditions, preferring warmer and clearer days.
- **Registered Users**: Less sensitive to changes in temperature and weather but exhibit more stable rental patterns.

### 4. Weekday vs Weekend
- **Weekdays**: Show significantly higher rental counts than weekends. T-tests confirm that more bikes are rented on weekdays compared to weekends.
  
### 5. Statistical Insights
- Pearson and Spearman correlation tests show a positive relationship between temperature and rentals, and a negative correlation between humidity and rentals.
- Kruskal-Wallis tests confirm that weather and seasonal conditions have a significant impact on bike rentals.

## Visualizations
- **Correlation Heatmaps**: Show relationships between weather, temperature, and bike rental counts.
- **Histograms**: Provide distribution insights for temperature, humidity, and windspeed.
- **Boxplots**: Highlight outliers in rental patterns across different seasons and weather conditions.
- **Pie Charts**: Depict the distribution of rental counts across holidays, working days, and seasons.

## Tools & Libraries Used
- **Python**: For data manipulation and analysis.
- **Pandas**: Data wrangling.
- **NumPy**: Mathematical operations.
- **Matplotlib & Seaborn**: Visualization libraries.
- **SciPy**: Statistical testing (e.g., t-tests, ANOVA).
- **Statsmodels**: Goodness-of-fit tests (Shapiro-Wilk, Levene).

## Key Analytical Methods
- **Correlation Analysis**: To determine relationships between variables.
- **T-tests**: To test hypotheses on weekdays vs weekends, holidays vs working days.
- **Kruskal-Wallis Test**: To check for significant differences in demand across different seasons and weather conditions.
- **Outlier Detection**: IQR method to detect and handle outliers in rental counts.

## Business Recommendations
1. **Inventory Management**: Use weather forecasts to adjust bike availability. Ensure more bikes are available during favorable conditions (e.g., clear weather).
2. **Pricing Strategy**: Implement dynamic pricing based on weather and demand conditions. Offer discounts on days with lower expected rentals (e.g., during adverse weather).
3. **Targeted Marketing**: Promote bike rentals during fall and moderate weather conditions. Special discounts could be offered during spring to boost lower rentals.

## How to Run
1. Clone the repository.
2. Install required libraries:
   bash
   pip install pandas numpy matplotlib seaborn scipy statsmodels
   
3. Run the Jupyter notebook to explore the analysis and visualizations.

## Contact
For any questions or suggestions, please feel free to reach out.

