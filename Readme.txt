=========================================
Dataset characteristics
=========================================	
day.csv have the following fields:
	
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

# Bike-Sharing Demand Prediction Model

## Problem Statement
BoomBikes, a bike-sharing provider in the United States, has faced a significant decline in revenue due to the COVID-19 pandemic. To recover from these losses and prepare for the surge in demand once the pandemic subsides, BoomBikes aims to predict the demand for shared bikes. The company has gathered a dataset on daily bike demand across the American market, and they need to understand which factors drive demand to adjust their business strategy accordingly.

## Business Goal
The goal of this project is to model the demand for shared bikes using independent variables (features) to:
1. **Identify significant predictors of bike demand**: Determine which variables (e.g., weather, time of year, holidays, etc.) influence bike usage the most.
2. **Evaluate how well the predictors describe bike demand**: Assess the predictive power of the model and its accuracy in forecasting bike demand.

### Key Questions:
1. Which variables significantly affect bike demand?
2. How well do these variables explain the fluctuations in bike demand?

## Data Overview
The dataset includes daily bike-sharing usage, with independent variables such as:
- **Weather-related factors**: Temperature, humidity, wind speed, weather conditions.
- **Time-related factors**: Day of the week, month of the year, working day/holiday, year.
- **Other factors**: Season, specific events, and external factors.

## Key Conclusions from the Model

### **Positive Influences**
1. **Temperature**: Higher temperatures significantly increase counts (+47.2% per unit).
2. **Year**: Bike counts increase over time, with counts rising by +23.4% in later years.
3. **Season and Month**:
   - **Winter** and **Summer** positively influence counts, with increased usage during these seasons.
   - **September** sees a notable rise in counts, likely due to favorable weather and fall activities.
4. **Day of Week**:
   - **Saturdays** show higher counts, likely due to recreational activity and leisure trips.
5. **Working Days**: Bike usage slightly increases on working days (+4.6%), likely due to commuting needs.

### **Negative Influences**
1. **Weather**:
   - **Light Snow/Rain**: These weather conditions significantly reduce bike demand, with counts dropping by **-29.1%** during such conditions.
   - **Mist/Cloudy**: Cloudy or misty weather decreases demand by **-8.1%**.
2. **Season and Month**:
   - **Spring**, **January**, and **July** show lower demand, likely due to less favorable weather and holidays.
3. **Holidays**: On holidays, bike demand drops by **-5.6%**, possibly due to fewer people commuting or biking for leisure.
4. **Windspeed**: High wind speeds reduce demand by **-15.6%**, as biking becomes less appealing in windy conditions.

### **Insights**
- **Weather and temperature** are the most significant predictors of bike-sharing demand. Warmer weather encourages more usage, while adverse conditions like snow, rain, and wind discourage it.
- Bike usage is higher during weekends and working days but drops significantly on holidays, suggesting people tend to use bikes more for leisure and commuting during weekdays.
- **Specific months** such as **January** and **July**, along with the **Spring season**, show reduced activity, likely due to unfavorable weather and the influence of holidays.

### **Actionable Recommendations**
1. **Promotions**:
   - Encourage bike usage during low-demand months like **January** and **July** with special promotions or discounts.
   - Offer **incentives** during periods with bad weather (snow, rain, high wind) to encourage usage despite unfavorable conditions.
   
2. **Resource Allocation**:
   - Focus on increasing bike availability during **weekends**, especially **Saturdays**, when demand is highest due to recreational activity.
   - Increase bike fleet during **September** and warmer seasons to meet higher demand.
   
3. **Weather-Based Strategies**:
   - Implement **weather-based pricing** strategies, offering **discounts or reduced rates** on days with high wind or adverse weather to maintain customer interest.
   - Create targeted marketing campaigns that encourage biking during ideal weather conditions and promote indoor biking or weather-resistant biking gear during bad weather.

## Future Model Improvements
1. **Non-Linear Models**: Explore non-linear models like **Random Forests** or **Gradient Boosting** to capture more complex relationships between features and demand.
2. **Real-Time Data**: Incorporate real-time data such as **traffic patterns** and **social trends** to improve the model's accuracy and responsiveness.
3. **External Factors**: Integrate factors like **COVID-19 restrictions** or **local events** to improve demand prediction during unusual circumstances.

## Conclusion
By understanding the demand dynamics and the factors influencing bike-sharing, BoomBikes can effectively prepare for the recovery post-pandemic. The insights from the model will help the company align its operations with demand fluctuations, optimize bike availability, and implement strategies that maximize revenue during peak seasons and mitigate losses during off-peak times.

BoomBikes can use the model to enhance their business strategy, improve customer satisfaction, and ultimately lead the market as the demand for shared bikes increases again.


	
=========================================
License
=========================================
Use of this dataset in publications must be cited to the following publication:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}

=========================================
Contact
=========================================
	
For further information about this dataset please contact Hadi Fanaee-T (hadi.fanaee@fe.up.pt)
