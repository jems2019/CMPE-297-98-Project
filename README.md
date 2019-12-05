Applying CNN for Stock Market Price Predictions

Project Members:
Emmeline Tsen
Matt DiPietro
Jonathan Gee
Sindhuja Ramini

# Data collection

The historical data that was collected was historical stock data collected from yahoo finance. We collected various     different stock data in a variety of different spaces. Once collected data cleaning and preperation was done on it. To ensure that there are no discontinuities in the data such as 0's, since this is time series data. If there is a zero in the data we would propegate the previous days value forward. Then we took the historical data and broke it down into months. This was then passed to another function that will turn the month data into an image. 


# Transitioning the time series data into graphs. 

We took the month data frame and graphed the time series data by month, we put multiple values on the image. Open values, close values, and a simple moving average on the data. Which will be talked about below. These images were then passed to the CNN for training and classification. 

3. Used CNN to categorize whether to buy, sell, or hold the stock


# Used TFX Serving

We used TFX Serving to train and model with REST. After training our data using a CNN, we saved the models which were then loaded and into a SavedModel format. Then we used TensorFlow serving to make a request. 
