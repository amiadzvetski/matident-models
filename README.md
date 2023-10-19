# 1. Models for classification of materials.
1) XGboost_clf.sav
2) LightGBM_clf.sav
3) CatBoost_clf.sav
   
Output: label of identifiable materials ('Gd(NO3)3*6H2O', 'GdGNFs', 'La(NO3)3*6H2O', 'LaGNFs', 'Nd(NO3)3*6H2O', 'NdGNFs', 'air', 'bone', 'plex', 'water').

# 2. Models for predicting k-edge (regression task).
1) XGboost_r.sav
2) LightGBM_r.sav
3) CatBoost_r.sav
   
Output: numerical value of k-edge.

### Format of Input:
```
|  thl45   |  thl46   |  thl...  |  thl165  |
|---------:|---------:|---------:|:--------:|
| 0.002733 | 0.002730 | ...      | 0.001398 |
| 0.002976 | 0.002931 | ...      | 0.001399 |
```

# 3. How to load models?

Intstall joblib:
```python
!pip install joblib
```

Example:
```python
!pip install joblib
import joblib

reg = joblib.load('XGboost_r.sav')
predictions = reg.predict(X_test)
predictions
```
