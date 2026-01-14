# Regression Models
The *Regression-[Seoul-bike-dataset].ipynb* Colab Notebook consists of Regression models like Linear Regression, Multiple Linear Regression, Regression using Neural Networks for one feature and a Neural Network for one feature and for all features.

## Dataset
The dataset used is the "Seoul Bike Sharing Demand" dataset ([https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand]) from UCI Machine Learning Repository. The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information. It has 13 features and 8760 instances that are clean and of real or integer data type. 

## Data Preprocessing
Before modelling, features such as 'Date', 'Seasons' and 'Holiday' are dropped as they are not useful. The column labels are updated for writing cleaner codes. The instances of the 'functional' feature are changed from 'Yes' and 'No' to 1's and 0's respectively for more efficiency. 

The *Seoul Bike Data* is available for all 24 hours, but only the 13th hour is taken for modelling regression. The 'hour' feature is dropped and graphs are plotted between the *Bike Count* and the features. Finally, the features with no obvious correlation, such as 'wind', 'visibilty', and 'functional' are dropped.

For Neural Network models, the respective datasets are normalized using the **Standard Scaler**.

## Train, Test and Validation Split
The entire dataset is randomly split into Train, Test and Validation datasets, where the *train* dataset consists of 60% of the data, the *valid* dataset consists of the next 20% of the data and the *test* dataset consists of the remaining 20% of the data. 

A function is defined to separate the feature vector (x) and the target feature (y) into *train*, *val* and *test* datasets, with an option to include specific labels as the feature vector. For Linear Regression and Linear Regression using Neural Networks, only the 'temp' feature is taken, whereas for Multiple Linear Regression, all the features are included. The Neural Networks model is implemented using both the datasets.

## Evaluation Metrics
For the Linear Regression model and the Multiple Linear Regression model, the R^2 is calculated to be roughly around 0.3885 and 0.4180 respectively, meaning that the Multiple Linear Regressiom model is slightly better. 

For Neural Network models, validation loss is plotted using the **Mean Squared Error**. With all the features, the MSE for Neural Net Linear Regression comes to be approximately 130415, while for the Neural Network model, it is arond 137158. This means that both the models perform similarly, but the Neural Network model performs slightly worse. 

Scatter plots are plotted for each model to visualize the results. A scatter plot with both Linear Regression using Network Networks model and the Neural Networks model is also plotted to compare them.
