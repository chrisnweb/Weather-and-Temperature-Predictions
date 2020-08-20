# Weather-and-Temperature-Predictions

***Disclaimer:*** *All the information in this repository, README including the Machine Learning Algorithm are provided and published for educational purpose only.*

### **Introduction/Description of project**

Weather can make a huge impact in our lives. It is not only important to us, but it is also an essential to our daily survival.
In this project I am going to present how weather in Houston, Texas, specifically of rainfall and temperature, can be predicted in advance using historical daily weather (i.e.  precipitation, rain, and temperature) data from the National Oceanic and Atmospheric Administration (NOAA)

### **Goal**
*	Weather prediction such as rainfall is one of the major concerns in the field of meteorology. Several techniques I believed that they will help to predict the weather are based on Machine Learning and Deep Learning methods.
* My goal is to use various Machine Learning and Deep Learning methods to assist with rainfall and temperature predictions.

#### **Machine Learning methods used:**
* ***SVM with Support Vector Classifier (SVC)*** – It is a widely used for classification and regression problems. 

* ***Logistic Regression*** – It is a popular classification algorithm used for binary classification problems. Logistic Regression is an improved version of Linear Regression

* ***Random Forest*** – It is considered a classification algorithm that consisting of many decision trees.

*	***Linear Regression*** – It is a statistical process to determine an estimated relationship of two variable sets. In our project we used it to forecast/predict the relationship between 2 variables (Max and Min Temperatures)

#### **Deep Learning method used:**

* ***Long-Short Term Memory (LSTM)*** – It is a type of Recurrent Neural Network (RNN) architecture used in the field of deep learning. LSTM is a great choice for Time Series forecasting/predicting (such as temperature).
  - Time Series is a collection of data points indexed based on the time they were collected.

### **Dataset**
* The historical Houston public daily weather data are downloaded from the [NOAA website](https://nomads.ncep.noaa.gov/)

### **Major used Libraries/Packages:**
* Panda (for file handling)
*	Numpy (for scientific computing)
*	Matplotlib (for visualization plotting)
*	Scikit-Learn (for Machine Learning)
*	Keras (for Deep Learning)
*	TensorFlow (for Deep Learning)

### **Data Visualization for EDA**
* Missing data visualizations with [missingno](https://libraries.io/pypi/missingno)
    - The white horizontal lines in each column represent the null values.
      <img src="Images/missing_data.png" width="500">

* Visualizing the daily temperatures - maximum, average, and minimum
      <img src="Images/daily_temperature.png" width="400">

* Precipitation summary
    - The highest one day precipitation (rainfall): 16.07 inches - August 27, 2017
      <img src="Images/precipitation_summary.png" width="400">

* 3D plot visualization of the weather condition
    - Blue dots = It rained when the precipitation (in Inches) increased
    - Red dots = It didn't rain when the precipitation (in Inches) at low level
      <img src="Images/3d_plot.png" width="400">

## *********************************************
## **Rainfall Predictions**

### **Support Vector Classification (SVC)**
   -  No Rain = 337 days
   -  Rain = 96 days
  <img src="Images/svc_prediction.png"> 
  
### **Logistic Regression**
   -  No Rain = 338 days
   -  Rain = 87 days
  <img src="Images/logreg_prediction.png">
      
### **Random Forest**
   -  No Rain = 337 days
   -  Rain = 158 days
  <img src="Images/rf_prediction.png">

  ### **Evaluating with ROC Curve on 3 models**
  <img src="Images/comparison_roc_curve.png" width="300">
  
  ## *********************************************
## **Temperature Predictions**

### **Linear Regression**
   -  Visualizing the prediction
   <img src="Images/linreg_prediction.png" width="400">
  
   -  Residual analysis on the Linear Regression model - Train and Test data
   <img src="Images/residual_plot.png" width="300"> 
  
  ### **Recurrent Neural Network LSTM – Time Series**
   -  Visualization of the prediction
   <img src="Images/lstm_prediction.png" width="500">
 
   -  Zoom in closer
   <img src="Images/lstm_prediction_zoom_in.png" width="500">
  
### Result
The graph patterns from our predicted temperature are closed to the actual. Our model did indicate overall trends such as going up or down. The prediction has taught me that the LSTMs can be very effective in times series predicting/forecasting.
 
  
## **Conclusion** 
##### In this project, we have presented the most fundamental machine learning algorithms such as Support Vector Classifier, Logistic Regression, and Random Forest used to predict the rainfall, the Linear Regression to predict the temperature. We also have presented a deep learning algorithm i.e. RNN-LSTM for time series forecasting the temperature. We implemented these prediction methods with the help of the Scikit-Learn, Keras, TensorFlow machine learning/deep learning libraries.

##### I know that weather forecasters i.e. meteorologists are not perfect, but their predictions/forecast are mostly more accurate than the Linear Regression model that was presented in this project. This indicates that the weather is a non-linear system. Furthermore, my Linear Regression model prediction was based on the historical data from one weather station (location) in contrast to multiple stations (locations) that most forecasters use.

##### From this project, I have learned that non-linear system modeling with RNN-LSTM can be very effective in Times Series forecasting. I hope, at the end, prediction of Time Series data in meteorology can assist in decision-making processes carried out by organizations and be responsible for the prevention of weather disasters such as flooding, extreme heat waves, and tornadoes.


## Questions to improve learning
#### *What can be add to improve the project and can be done differently?*

##### 1.  My project will not stop here, I will use the RNN-LSTM time series data to predict the rainfall.

##### 2.	For the future, I need to compare with other methods such as Holt-Winter, SARIMA, and DNNRegression in order to demonstrate the improvement of rainfall/temperature prediction in the proposed approach.

##### 3.	I can improve the model by adding more LSTM layers, changing loss function, and increasing the probability of dropout to distribute the training data better.

##### 4.	I need to further expand and develop the code to get better prediction/forecasting results.

##### 5.	I can add other weather locations throughout the Houston area and also can use a much larger historical weather data.


## **CHEERIOS!**

## Reference

[missingno](https://libraries.io/pypi/missingno)

[Yellowbrick](https://pypi.org/project/yellowbrick/)

[sklearn.metrics.mean_squared_error](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)

[Timeseries anomaly detection using an Autoencoder](https://keras.io/examples/timeseries/timeseries_anomaly_detection/)
