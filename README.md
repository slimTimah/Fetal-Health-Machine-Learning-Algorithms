# Fetal-Health-Machine-Learning-Algorithms
Project Title: Predicting Fetal Health Using Machine Learning Algorithms In this project, I explored the application of machine learning techniques to predict fetal health status based on cardiotocography data. The goal was to classify fetal health into 3 categories: normal, suspect, pathological.

# Importing Data
- Firstly, It is important to know the type of machine learning the dataset falls under and this can be detected based on the target/label variables in that datasets. owever,because the lables is of three
- categories, it is important to use different algorithms thereby importing two or more machine learning algorithms:
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
  # Data Analysis


