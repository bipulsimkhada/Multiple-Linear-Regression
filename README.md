# Multiple Linear Regression

Linear regression used to make prediction. One Hot Encoder used for encoding catergorical data.<br>
**File required:** insurance.csv<br>
**Feature:** Age, Sex, BMI, Children, Smoker, Region<br>
**Label:** Charges (Annual Premium)

## One Hot Encoder
One hot Encoder is used to convert categorical data to binary vector data. 

```python
from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import OneHotEncoder
ct = ColumnTransformer(transformers=[('encoder', OneHotEncoder(), [1,4,5])], remainder='passthrough')
X = np.array(ct.fit_transform(X))
```
## Model
```python
y_pred = regressor.predict(X_test)
regressor.score(X_test, y_test)
```


