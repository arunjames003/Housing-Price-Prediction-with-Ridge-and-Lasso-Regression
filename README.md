# Housing Price Prediction with Ridge and Lasso Regression


## Table of Contents
- General Information
- Conclusions
- Python Library Used for Analysis
- Contact


## General Information
Surprise Housing, a US-based company, aims to expand its operations to the Australian real estate market. Their strategy involves purchasing houses below market value and then selling them at a profit. To achieve this, they’ve collected a dataset of house sale prices in Australia. Our task is to build a regression model using regularization techniques (specifically ridge and lasso regression) to predict the actual value of prospective properties. Based on these predictions, Surprise Housing will decide whether to invest in these properties.

* Background:
Surprise Housing’s business model relies on data analytics and market insights. By analyzing historical house sale data, they can identify undervalued properties and capitalize on potential gains. The Australian market presents an opportunity for expansion, and accurate price predictions are crucial for their success.

* Business Problem:
The core business problem is to determine the fair market value of prospective properties. If Surprise Housing overestimates the value, they risk overpaying for properties. Conversely, underestimating the value may cause them to miss profitable investment opportunities. Our goal is to create a robust regression model that provides accurate price estimates.

* Dataset:
The dataset contains information on house sales in Australia. Key variables include:

- Price: The sale price of the house (our target variable).
- Features: Various attributes related to the property, such as square footage, number of bedrooms, location, etc. We’ll explore the dataset, preprocess it, and then apply ridge and lasso regression to identify significant features and optimize the model.


* Business Goal:
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.🏠💰


## Conclusions
- SalePrice is the target column
- Data divided in to numerical and categorical
- Top 50 features are selected through RFE and adjusted R-square
    * Top 50 feature are : 'LotArea', 'OverallQual', 'OverallCond', 'YearBuilt', 'YearRemodAdd', 'BsmtQual', 'BsmtExposure', 'BsmtFinType1', 'BsmtFinSF1', 'HeatingQC', 'CentralAir', '1stFlrSF', '2ndFlrSF', 'BsmtFullBath', 'HalfBath', 'KitchenQual', 'Functional', 'FireplaceQu', 'GarageFinish', 'GarageArea', 'GarageQual', 'MSZoning_RL', 'MSZoning_RM', 'Alley_Not_applicable', 'LotConfig_CulDSac', 'Neighborhood_Edwards', 'Neighborhood_NAmes', 'Neighborhood_NWAmes', 'Neighborhood_NridgHt', 'Neighborhood_OldTown', 'Neighborhood_Somerst', 'Condition1_Norm', 'Exterior1st_HdBoard', 'Exterior1st_MetalSd', 'Exterior1st_Plywood', 'Exterior1st_VinylSd', 'Exterior1st_Wd Sdng', 'Exterior2nd_Plywood', 'Exterior2nd_Wd Sdng', 'MasVnrType_BrkFace', 'MasVnrType_Not_applicable', 'MasVnrType_Stone', 'Foundation_PConc', 'GarageType_Attchd', 'GarageType_Detchd', 'GarageType_Not_applicable', 'PavedDrive_Y', 'SaleType_New', 'SaleCondition_Normal', 'SaleCondition_Partial'
- Ridge and Lasso Regression Model are built with optimum alpha calculated in GridSearchCV method. Optimum alpha = 20.0 for ridge and 0.001 for lasso model.
- Model evaluation is done with R2 score and Root Mean Square Error.
- Lasso Regression produced slightly R2 score on test data than Ridge Regression. Choosing Lasso as the final model.
- The top 10 features, ranked by descending importance, in the final model out of a total of 50 features are as follows:
    1. 1stFlrSF
    2. 2ndFlrSF
    3. OverallQual
    4. OverallCond
    5. SaleCondition_Partial
    6. LotArea
    7. BsmtFinSF1
    8. SaleCondition_Normal
    9. MSZoning_RL
    10. Neighborhood_Somerst
- The table displays the model coefficients alongside their respective features. 
    * For instance, a unit change in the feature `1stFlrSF` will result in a change of 0.138275 in the natural log of SalePrice, assuming all other features remain constant. 
    * Similarly A negative coefficient indicates a negative correlation between the predictor and the target variable. for example : a unit change in the feature `Functional` will result in a change of -0.022718 in the natural log of SalePrice, assuming all other features remain constant. 
- The predicted value of SalePrice is transformed back into its original scale by performing an antilogarithm operation.


## Technologies Used
- numpy - version 1.24.3
- pandas - version 2.1.4
- matplotlib - version 3.7.2
- seaborn - version 0.12.2
- sklearn - 1.3.0
- statsmodels - 0.14.0


## Contact
Created by [@arunjames003] - feel free to contact me!