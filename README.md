# Fetal-Health-Machine-Learning-Algorithms
Project Title: Predicting Fetal Health Using Machine Learning Algorithms In this project, I explored the application of machine learning techniques to predict fetal health status based on cardiotocography data. The goal was to classify fetal health into 3 categories: normal, suspect, pathological.

# Importing Data
- Firstly, It is important to know the type of machine learning the dataset falls under and this can be detected based on the target/label variables in that datasets. However, since the lables is of three categories, it is important to use different algorithms for predictions thereby importing two or more machine learning algorithms:
```python
- from sklearn.model_selection import train_test_split
- from sklearn.linear_model import LinearRegression
- from sklearn.metrics import mean_squared_error
- sklearn.model_selection for splitting data into training and testing sets
- sklearn.linear_model for linear regression and other linear models
- sklearn.tree for decision trees
- sklearn.metrics for evaluating model performance
```

# Loading Data
- The fetal-health dataset was downloaded from Kaggle as a csv file. Unlike the usual: 
  ```python
  fetalHealth = pd.read_csv(fetal-health.csv)
  fetalHeath.head(10)
  ```
  I created a function to load the dataset and return it as this will give easy accessible and often use of the variable.
  - The function created:
      ```python
      def load_dataset():
      global fetalHealth #When you declare df to be global, it can work outside function
  
       fetalHealth =pd.read_csv('fetal_health.csv')
      return fetalHealth
    load_dataset()
  ```
# Data Analysis and Model Selection
- When it comes to machine learning algorithms, it is very important to get an insights of the dataset like checking the null values, accurate datatypes in each columns, column titles and shapes as this will effect balanced performance.
- To get the column titles, dimensions and null values:
  ```python
  fetalHealth.columns
  fetalHealth.shape
  fetalHealth.isna().sum()
  ```
- For machine learning algorithms, it is expect to firstly divide the dataset into two which are, features and labels in which X indicate features and y indicates labels.
- The features are the characteristics and the labels, the conclusion.
- Using train_split_data, the dataset must be splitted into training data and testing data.
  ```p
- Also, since it is lables is a multiclass categories several algorithms were used as this will give insights on which machine learning algorithms performed well.
- The algorithm used were created in a function and this gives use of the use of the variable multiple times.
- Some of the functions are:

  ```python
  def support_vector_regressor():
    global SVR_model
    global SVR_predict
    SVR_model = SVR()
    SVR_model.fit(Xtrain, ytrain)
    SVR_predict = SVR_model.predict(Xtest)
    return SVR_predict
  support_vector_regressor()
  ```

  # Conclusion
  - Of all the machine learning algorithms, the decison tree regressor predicted it well after been tested on training data

