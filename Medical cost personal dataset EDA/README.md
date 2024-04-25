# Aplly models in Medical Cost Personal dataset

- The dataset can be downloaded from:
https://www.kaggle.com/mirichoi0218/insurance

## - load dataset
  
## - data prepossessing
  
•	Chick out for missing value in data and there aren’t.

•	transform categorical data :

	encoded the sex , smoker and region rows to le_sex , le_smoker and le_region.

•	One hot encoding in array that has region_encoded to 3 (region_0, region_1, region_2, region_3).

•	Finally dropped ('sex','smoker','region','region_encoded','region_0').

•	feature scaling of the data to comes all values into same scale

## - train and test split  
	
 	X= ['age','sex_encoded','bmi','children','smoker_encoded','region_1','region_2','region_3'] (features)
 
	 Y= ['charges'] (target)

then split to X_train, X_test, y_train, y_test.

## - apply models 

•	Decision Tree Regressor Model

 	 used parameter DecisionTreeRegressor(criterion='mse', splitter='best', max_depth=10,random_state=33)

•	Linear Regression Model  

  	used parameter LinearRegression(fit_intercept=True, normalize=True,copy_X=True,n_jobs=-1) 

•	Extra Trees Regressor Model

 	used parameter ExtraTreesRegressor(n_estimators = 200)

•	KNeighbors Regressor Model

 	used parameter KNeighborsRegressor(n_neighbors = 10 , weights ='distance' ,p=2, metric='minkowski')

