# python-api-challenge
Used the method outlined here to manually create a gitignore file after creating the repository 
https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files

The following stackoverflow solution was used to fix my blank image outputs for the linear regression section in the weather data code
https://stackoverflow.com/questions/9012487/savefig-outputs-blank-image

For programming, the methodology used follows example code written for class exercises

## Weather
For each city, the required parameters are saved to variables and then appended to the city data dataframe. This data is output to a CSV for the vacation script. Then, the required scatterplots are created. For temperature data, 273 was subtracted as the original values were retrieved in degrees Kelvin. Plots and axis are labelled as shown in the outputs shown in the starter code. 

For linear regression function, we start by creating the parameters of the linear regression and a string with the linear fit equation. Then, a scatter plot with the x and y values is created and the linear regression line is plotted. Because the data values will change each time the cells are run some adjustments needed to be made to the location of the printed linear fit equation. See the jupyter notebook for analysis of linear regression plots

## Vacation
The vacation scripts take the output from the weather script into a data frame and plots their locations using HV plot as requested. The data point size is set according to humidity as the required.

### Ideal conditions used
Above 290 K
Below 60% humidity
Below 50% cloudiness
Wind below 10 km/h

Using the above conditions, the cities in the data frame outside of those conditions and with null values are removed. For hotel searching, we begin by building our parameters for radius of 10000 meters, the "accommodation.hotel" category, and our api key. Then the loop that is set up will search for filter and bias according to latitude, longitude, and radius. The API request is made for the hotel according to our parameters and stored to a json. We retrieve the hotel name to the hotel column added to the data frame if it is found and save an error message. The remaining hotels are plotted again in the same method as before but with the addition of the hotel name and country being displayed when hovering over data points. It appears a majority of the locations are near or south of the equator. The most popular location was Australia which I had planned to go to before the 2020 pandemic so maybe I'll consider planning a trip down under again.
