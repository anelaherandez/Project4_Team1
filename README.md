# Project4_Team1--Arizona Real Estate Pricing Predictive Modeling 
Team Members: Necole Barnes, Ryan Dekker, Andrea Hernandez, Daniela Trujillo

![Picture2_p4](https://github.com/anelaherandez/Project4_Team1/assets/144189200/12f27e40-7044-4168-9659-04660bcf8c08)

## Project Proposal and Outline
In a post-Pandemic world, with ever changing market prices, the prediction of housing prices in various regions of Arizona can help guide a family in their search for a new home. For this project, we will be using US housing listings from Zillow in 2023, specifically Arizona, to understand the relationships between various housing characteristics and the listed price for a home. Our goal is create a predictive model on housing prices that will predict market price for 2024.
Research Questions:
1. What are the differences in the cost of a home throughout the various regions of Arizona?
2. By exploring the categorical variables, how does each variable affect the price per square foot and ultimate listing price?
3. What categorical and/or numerical variable best predicts the Zillow market price of a home?

To answer our research questions and create a predictive model, we broke the project into Data Visualization/Exploration and Data Analysis/Predictive Modeling by dividing up the project between each team member and using the following applications:
        Tableau--Andrea Hernandez
        Pandas/Matplotlib/Numpy--Daniela Trujillo
        Sql Alchemy--Necole Barnes
        Scikit-Learn/Statsmodels--Ryan Dekker
        
## Data Visualization and Exploration
- Tableau:
To explore the categorical and numerical variables in our dataset, we created a Tableau story with four dashboards that primarly focused on the average price per square foot and average listed price. Additionally, our tableau story examined the difference in these two averages depending on how many bedrooms/bathrooms a listing had, as well as the differences between the East and West Valley listings.

https://public.tableau.com/app/profile/andrea.hernandez1906/viz/Project4_ArizonaProperties2023/ASU_Project4?publish=yes

- Matplotlib notebook: 

On this notebook we broke the data into Bedroom sizes categories to be able to illustrate the range in Listed Price. We got the highest valued by category using .iloc function. 
To illustrate the DataFrame with an ascending filter the .sort_values function was used along with inplace and ascending functions. 
Once all the data was broken into categories in each of the cities and the state of Arizona. MatPlotLib was used to make Bar visualizations to show 
1.	Highest Bedroom size by each City (Phoenix, Tucson, Prescott, Scottsdale) 
2.	Use all cities data to compare all four cities for 2 to 4 Bedrooms
   ![image](https://github.com/anelaherandez/Project4_Team1/assets/144754677/f057ca60-1062-4b50-a99c-48a69fdf2320)

3.	Highest Bedroom city for the whole State for bedroom size 1 to 6
![image](https://github.com/anelaherandez/Project4_Team1/assets/144754677/32eb832a-4791-4c4b-a7d5-ff6edf000ae3)


## Data Analysis/Predictive Modeling
- SQLAlchemy Notebook

In this notebook data was retrieved from a zillow SQL database using SQLAlchemy. Once the connection to the database was exstablished, data was retrieved, read and displayed from a table. Columns with a object datatype were dropped, listing only datatypes that are int64 or float64 for visualization.
1. Histograms was created for indiviual variables to give a better visual understanding of the data
2. A correlation heatmap was created to identify patterns and relationships between different variables
![heatmap_p4](https://github.com/anelaherandez/Project4_Team1/assets/144189200/e9bb961e-c142-478d-8eb7-69a83aa790b8)

3. Scatterplot was created to give a visualization of a popular area of interest

   

- Scikit-Learn/Statsmodels
For the modeling.ipynb file, various Ordinary Least Squares Models were run to see which independent variables best predicted the Listing value. These were run using the statsmodels package.
The first OLS model including all predictors but the "PPsq" factor was very strong becausse it states the price per square foot. All other models remove that predictor, as to better parse which indpendent variables predict the listing value.
         The models worked best when focusing on large cities (Phoenix or Tucson) or relevant areas (East Valley or the Mountianous areas).
         These modeling data also use a train-test model on predicting the (dozens of) bins of prices. However, the weighted accuracy was only 0.51.
        The random forrest model ended with a 0.997 R-squared score. This model was adapted using the following documentation: https://www.geeksforgeeks.org/random-forest-regression-inpython/

## Conclusions and References
This Zillow data showed a wide range of prices for the listings, but several factors repeatedly showed themselves to be significant
	# of bedrooms and bathrooms, 
	Square footage of the home was more important than lot size
	
City was an important factor, but these data were able to be successfully modeled when grouping these listings into relevant categories
	Tucson
	Scottsdale
	East Valley (Mesa, Tempe, Chandler, Gilbert)
	Uplands (Prescott, Payson, Sedona, Flagstaff)
https://www.kaggle.com/datasets/febinphilips/us-house-listings-2023
https://www.zillow.com/research/data/


