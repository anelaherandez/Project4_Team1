# Project4_Team1





For the modeling.ipynb file, various Ordinary Least Squares Models were run to see which independent variables best predicted the Listing value. These were run using the statsmodels package.

        The first OLS model including all predictors but the "PPsq" factor was very strong becausse it states the price per square foot. All other models remove that predictor, as to better parse which indpendent variables predict the listing value.
        
        The models worked best when focusing on large cities (Phoenix or Tucson) or relevant areas (East Valley or the Mountianous areas).
        
        These modeling data also use a train-test model on predicting the (dozens of) bins of prices. However, the weighted accuracy was only 0.51.
        
        The random forrest model ended with a 0.997 R-squared score. This model was adapted using the following documentation: https://www.geeksforgeeks.org/random-forest-regression-in-python/
