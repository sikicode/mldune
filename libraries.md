1. Pandas as pd: create dataframes
- Know how to use dataframe functions (read_csv, describe, columns, head, series, concat...)
- axis: https://stackoverflow.com/questions/22149584/what-does-axis-in-pandas-mean
- Convention: prediction target is 'y', features is 'X' including feature columns
```python
melbourne_features = ['Rooms', 'Bathroom', 'Landsize', 'Lattitude', 'Longtitude']
X = melbourne_data[melbourne_features]   # melbourne_data is a dataframe
```
2. Scikit-Learn (sklearn): model for dataframes
- Decision tree: https://scikit-learn.org/stable/modules/tree.html
  - well, use training data to predict on training data would result in same output
```python
from sklearn.tree import DecisionTreeRegressor
#specify the model. 
#For model reproducibility, set a numeric value for random_state when specifying the model
iowa_model = DecisionTreeRegressor(random_state = 2)    # random_state makes sure every run have the same output
# Fit the model
iowa_model.fit(X, y)
predictions = iowa_model.predict(X)
```
- 
3. 
