# python-api-challenge
Module 6 Challenge - UWA Data Analytics Bootcamp

The WeatherPy folder contains 2 python notebooks "VacationPy" and "WeatherPy" which contain the main code. There is one more file contained within the WeatherPy folder which is output_data. This file stores the output figures and csv data from the code.

The WeatherPy code first creates a list of random cities around the world and stores them in a list. The OpenWeatherMap API is then used to retrieve weather information on those cities which is then stored in a Data Frame. Plots are then created for various metrics as compared to the latitude of the cities. Linear regressions are then also performed with the following discussions:

Temperature vs. Latitude linear relationship Discussion

Northern Hemisphere: The plot for the Northern Hemisphere displays a clear inverse relationship between latitude and maximum temperature with a slope of -0.8. This is to say, as you move away from the equator to higher latitudes, max temperature will decrease. The R-value is approx. -0.857, which indicates a strong negative correlation between the two variables.

Southern Hemisphere: The plot of the Southern Hemisphere shows a positive relationship between latitude and maximum temperature with a slope of 0.3. This is still indicative that moving away from the equator to a more negative latitude will result in max temperature decreasing (this being the case as the equator exists at latitude 0). The R-value is approx. 0.686, indicating a moderately strong positive correlation. The lower R-value and slope could be due to the reduced sample size in the southern hemisphere as most of the land mass and human population exist in the northern hemisphere. There are also cities with more extreme latitude values in the northern hemisphere.

Humidity vs. Latitude linear relationship discussion

Northern Hemisphere: The plot demonstrates a positive slope of 0.57 suggesting humidity increases with higher latitudes (moving away from the equator results in higher humidity as a trend). The r-value is 0.409 which indicates a moderate correlation between the two variables.

Southern Hemisphere: Interestingly, the southern hemisphere plot also has a positive slope (0.12), suggesting that humidity would decrease as a trend when moving away from the equator. The r-value is 0.114 which suggests a very weak correlation. Due to the low r-value, this is an unreliable trend and with the limitations discussed in the Temperature vs. Latitude linear relationship discussion, we cannot confidently conclude that this trend is impactful.

Cloudiness vs. Latitude linear relationship Discussion

Northern Hemisphere: The plot shows a positive relationship between cloudiness and latitude with a slope of 0.58 and an r-value of 0.280 which indicates a weak to moderate correlation. This suggests that as you move away from the equator, cloudiness would tend to increase. As can be seen in the plot, the data is visually sporadic but there does appear to be more cloudiness = 100 data points when latitude > 40 and far more cloudiness = 0 data points when latitude < 40.

Southern Hemisphere: The southern hemisphere plot has a slope of 0.78 and an r-value of 0.295, this being similar to the northern hemisphere result and demonstrating a positive relationship between cloudiness and latitude with a weak to moderate correlation. The fact that this data was pulled during summer in the southern hemisphere supports these trends. This is as the higher temperatures in the southern hemisphere results in the least amount of cloudiness there, with cloudiness then increasing as a trend towards the equator then further into the northern hemisphere as sun exposure is lower during this time of year.

Wind Speed vs. Latitude linear relationship Discussion

Both hemispheres demonstrate weak correlations between latitude and wind speed, with r-values of (-0.077 & -0.289). The northern hemisphere plot suggests that wind speed would decrease slightly as you move away from the equator (slope of -0.01). The southern hemisphere indicates that wind speed would increase as you move away from the equator (slope of -0.05).

As discussed before, this may be due to it being summer in the southern hemisphere at the time of data being pulled. Regardless, these are fairly weak trends and other factors are likely much more impactful on wind speed at any location.


VacationPy uses the information obtained via WeatherPy and the OpenWeatherMap API to create a heatmap of the humidity of the different cities. It then queries the Geoapify API to locate hotels at cities with ideal weather conditions.


Resources used:
Geoapify API Docs
https://apidocs.geoapify.com/docs/places/#categories

OpenWeather API Documentation
https://openweathermap.org/current#geo

hvplot.points
https://openweathermap.org/current#geo