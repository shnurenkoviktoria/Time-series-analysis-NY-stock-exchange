# Stock Price Prediction with LSTM

This README demonstrates the use of Long Short-Term Memory (LSTM) neural networks for predicting stock prices using historical data.

## Dataset

- The dataset is loaded from the file `prices-split-adjusted.csv`.
- It contains historical stock prices including open, close, low, high, and volume.

## Preprocessing

- Features including open, close, low, high, and volume are selected from the dataset.
- Min-max scaling is applied to normalize the data between 0 and 1.
- Sequences of data with a window size of 10 are created, where each sequence represents historical data points.
- The target variable consists of the next data point after each sequence.

## Model Architecture

- The LSTM model consists of one LSTM layer with 50 units followed by a Dense layer with the number of features as the output dimension.
- The model is compiled with the Adam optimizer and mean squared error loss function.

## Training

- The dataset is split into training and testing sets with a test size of 20%.
- The model is trained for 50 epochs with a batch size of 32 and a validation split of 20%.

## Evaluation

- The model's performance is evaluated on the test set using the mean squared error (MSE) metric.
- Predictions are made on the test set and inverse transformed to obtain actual stock prices.

## Visualization

- Actual and predicted stock prices are plotted against time to visualize the model's performance.

## Dependencies

- pandas
- numpy
- scikit-learn
- TensorFlow
- matplotlib
