# Real Estate Analysis of San Francisco from 2010 to 2016

![San Francisco Park Reading](Images/san-francisco-park-reading.jpg)

*[San Francisco Park Reading by Juan Salamanca](https://www.pexels.com/photo/park-san-francisco-reading-61109/) | [Free License](https://www.pexels.com/photo-license/)*

## Goal

SFO Real Estate Analysis dashboard provides charts, maps, and interactive visualizations to help customers explore the data and determine if they want to invest in rental properties in San Francisco. 

Note: The dashboard requires mapbox token to plot the neighborhood map using the latitude and longitude of the locations. 
you will need to create an account at [mapbox](https://www.mapbox.com/) and [create an access token](https://docs.mapbox.com/help/how-mapbox-works/access-tokens/#creating-and-managing-access-tokens).


### Rental Analysis

The first step to building the dashboard is to work out all of the calculations and visualizations in an Realestate_analysis notebook. Once the Analysis is complete, the dashboard code is used with Panel to create the final layout. Use the `realestate_analysis.ipynb` computes the following

#### Housing Units Per Year

Calculate the number of housing units per year and visualize the results as a bar chart using the Pandas plot function.

Note: By default, the limits auto-scale to the data. However, it is hard to see the difference between the yearly data. 
program uses the min, max, and standard deviation of the data to manually scale the y limits of the plot.

Bar Chart without adjustig y scale/using min, max & std

  ![unscaled-bar.png](Images/unscaled-bar.png)

Bar Chart with y-axis limits adjusted

  ![scaled-bar.png](Images/scaled-bar.png)


#### Average Gross Rent in San Francisco Per Year

visualize the average gross rent per year to better understand the trends for rental income over time. You will visualize the average (mean) gross rent per year and visualize it as a line chart.

1. Calculate the mean `gross` for each year.
2. Visualize the mean gross rent per year as a line chart.

  ![gross-rent.png](Images/gross-rent.png)

#### Average Sales Price Per Year

ddetermine the average sales price per year to better understand the sales price of the rental property over time. For example, a customer will want to know if they should expect an increase or decrease in the property value over time so they can determine how long to hold the rental property. You will visualize the average (mean) `sales_price_sqr_foot` and visualize it as a bar chart.

1. Calculate the mean `gross` for each year.
2. Visualize the mean gross rent per year as a line chart.

  ![average-sales.png](Images/average-sales.png)

#### Average Prices By Neighborhood

ccompare the average prices by neighborhood.

1. Group the data by year and by neighborhood and calculate the average (mean) `sales_price_sqr_foot`.
2. Visualize the mean `sales_price_sqr_foot` per year with the neighborhood as a dropdown selector. 

  ![avg-price-neighborhood.png](Images/avg-price-neighborhood.png)

#### Top 10 Most Expensive Neighborhoods

Determine which neighborhoods are the most expensive. Program calculates the mean sale price for each neighborhood and then sort the values to obtain the top 10 most expensive neighborhoods on average. 

  ![top-10-expensive-neighborhoods.png](Images/top-10-expensive-neighborhoods.png)

#### Parallel Coordinates and Parallel Categories Analysis

Plotly express is used to create the following parallel coordinates and parallel categories visualizations so that investors can interactively filter and explore various factors related to the sales price of the neighborhoods.

1. Create a Parallel Coordinates Plot

  ![parallel-coordinates.png](Images/parallel-coordinates.png)

2. Create a Parallel Categories Plot

  ![parallel-categories.png](Images/parallel-categories.png)

#### Neighborhood Map

Mapbox token is used to read in neighborhood location data and build an interactive map with the average prices per neighborhood. A scatter mapbox object from plotly express is used create the visualization.

  ![neighborhood-map.png](Images/neighborhood-map.png)

### Dashboard
This Dashboard presents a visual analysis of historical prices of house units, sale price per quare foot and grossrent in San Francisco, California from 2010 to 2016. You can navigate through the tabs above to explore mode details about the evolution of real estate market on the Golden city across these years. You can also select any a specific visual anaalysis from the drop down list box which provides a simple and easy wayto narrow down to a Visualization. Panel library is used to build an interactive dashboard for all of the visualizations.

Select Visualization:
![dashboard_tab1.png](Images/dashboard_tab1.png)

Sample Dashboard:

  ![dashboard-demo.gif](Images/dashboard-demo.gif)

---
