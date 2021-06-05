# Housing-Prices-Competition-for-Kaggle
This repository provides a Notebook for the [Housing Prices Competition for Kaggle Learn Users](https://www.kaggle.com/c/home-data-for-ml-course) task.
<br/> The specified model uses all attributes: 79 columns.
<br/> The missing values were filled with *fillna* method. 
<br/> Categorical variables were processed using *label_encoder* for features that have cardinality 2 or more than 9. 
<br/> Others are just categorical features that must be divided by one-hot encoding with *get_dummies*.
<br/> Two models have been tested: *RandomForestRegressor* and *XGBRegressor* with the use of *cross_val_score* (selected metric: 'neg_mean_absolute_error').
<br/> ***Results***:

| Model                | CV-1   | CV-2   |CV-3    |CV-4   |CV-5  |Mean       |
| -------------------- |:------:| ------:|-------:|------:|-----:|----------:|
| RandomForestRegressor| 17 669 | 17 415 |17 527  |16 111 |18 759|**17 496** |
| XGBRegressor         | 15 873 | 16 344 |17 464  |14 491 |16 910|**16 217** |

<br/> Thus, the XGBRegressor model was chosen with public score **15 365** (Top 9%)
