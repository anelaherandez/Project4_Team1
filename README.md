# Project4_Team1





For the modeling.ipynb file, various Ordinary Least Squares Models were run to see which independent variables best predicted the Listing value. These were run using the statsmodels package.

        The first OLS model including all predictors but the "PPsq" factor was very strong becausse it states the price per square foot. All other models remove that predictor, as to better parse which indpendent variables predict the listing value.
        
        The models worked best when focusing on large cities (Phoenix or Tucson) or relevant areas (East Valley or the Mountianous areas).
        
        These modeling data also use a train-test model on predicting the (dozens of) bins of prices. However, the weighted accuracy was only 0.51.
        
        The random forrest model ended with a 0.997 R-squared score. This model was adapted using the following documentation: https://www.geeksforgeeks.org/random-forest-regression-in-python/

Matplotlib notebook 
On this notebook we broke the data into Bedroom sizes categories to be able to illustrate the range in Listed Price. We got the highest valued by category using .iloc function. 
To illustrate the DataFrame with an ascending filter the .sort_values function was used along with inplace and ascending functions. 
Once all the data was broken into categories in each of the cities and the state of Arizona. MatPlotLib was used to make Bar visualizations to show 
1.	Highest Bedroom size by each City (Phoenix, Tucson, Prescott, Scottsdale) 
2.	Use all cities data to compare all four cities for 2 to 4 Bedrooms
   ![image](https://github.com/anelaherandez/Project4_Team1/assets/144754677/f057ca60-1062-4b50-a99c-48a69fdf2320)

3.	Highest Bedroom city for the whole State for bedroom size 1 to 6
![image](https://github.com/anelaherandez/Project4_Team1/assets/144754677/32eb832a-4791-4c4b-a7d5-ff6edf000ae3)
