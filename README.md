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

# Used CNN to categorize whether to buy, sell, or hold the stock

We implemented the three separate CNN models to predict whether to buy, sell, or hold a particular stock based on the image. 

## Pretrained ResNet Model
We first used a pretrained resnet model using weights from imagenet with an input shape (224, 224, 3). We used an Adam optimizer with a learning rate of 0.001. The validation accuracy using a resnet model yielded 0.46795. 

## Building Simple Model
We then built a simple CNN model with three Convolution 2D layers, two dropout layers, and two dense layers. After running the simple model with the training and validation image datasets, the validation accuracy for this model was 0.4615. 

## Building VGG Model
We also built a VGG Model to compare its performance compared with the pretrained ResNet model and simple model. The final validation accuracy using a VGG model built from scratch was 0.66239. This shows that using the VGG model performed the best to help make a prediction on whether to buy, sell, or hold the stock.
