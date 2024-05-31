# Auto MPG Prediction Using TensorFlow

This project demonstrates how to build and evaluate a linear regression model using TensorFlow 2.x to predict the fuel efficiency (MPG - miles per gallon) of cars based on various features from the Auto MPG dataset. The dataset used is a public dataset provided by the UCI Machine Learning Repository.

### Dataset

The dataset consists of various features about cars, including:
- `MPG`: Miles per gallon (target variable).
- `Cylinders`: Number of cylinders in the car.
- `Displacement`: Engine displacement.
- `Horsepower`: Engine horsepower.
- `Weight`: Weight of the car.
- `Acceleration`: Acceleration of the car.
- `Model Year`: Year of the car model.
- `Origin`: Origin of the car (1 for USA, 2 for Europe, 3 for Japan).

### Data Preprocessing

The preprocessing steps involve:
1. Loading the data from the provided URL.
2. Handling missing values by dropping rows with `NA` values.
3. Converting the `Origin` column to one-hot encoding, creating separate columns for `USA`, `Europe`, and `Japan`.
4. Splitting the data into training and test sets, with 80% of the data used for training and 20% for testing.
5. Separating the target variable (`MPG`) from the features for both training and testing datasets.

### Exploratory Data Analysis

Exploratory data analysis includes:
1. Displaying the first few rows of the dataset to understand its structure.
2. Describing the statistics of the training dataset.
3. Plotting scatter plots of features like `Horsepower`, `Weight`, and `Displacement` against `MPG` to visualize their relationships.

### Normalization

Normalization is applied to the feature data to ensure that each feature has a mean of 0 and a standard deviation of 1. This is done using TensorFlow's `preprocessing.Normalization`.

### Model Building

A linear regression model is built using TensorFlow's Keras API:
1. The model is a sequential model consisting of a normalization layer followed by a dense layer with one unit.
2. The model summary is displayed to understand its structure.

### Model Compilation and Training

The model is compiled using the Adam optimizer and a mean squared error loss function. It is then trained on the training data for 100 epochs, with 20% of the training data used for validation.

### Model Evaluation

The model is evaluated on the test dataset to determine its performance. The evaluation metrics help in understanding how well the model generalizes to unseen data.
