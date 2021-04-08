# Project 2 - Ames Housing Data and Kaggle Challenge

Brian Cho

The home appraiser's job is to determine your home's fair market value. When the lender orders the appraisal, it takes an average of three days before the appraiser's site visit takes place. Following the appraiser's site visit, it takes an average of three days for the appraiser to submit the appraisal report to the lender ([*source*](https://www.homelight.com/blog/what-do-home-appraisers-do/)).

In this project, I'll explore the Ames, Iowa Housing Data and determine the best model to predict the sale price of homes in Ames. This model will serve the home owners and real estate agents of Ames, Iowa and it will equip them with the ability to value their homes on their own. The model would also shorten the appraisal process by incorporating a machine learning system to compute the sale price of a house. The models that were developed are the linear regression model that includes feature engineering the numerical and categorical variables. The Ridge and LASSO regression methods were used to optimize the model with a better bias-variance tradeoff.   

Success will be evaluated by using the linear regression metrics: Coefficient of Determination (R2 score), the Mean Squared Error (MSE), and the Root Mean Squared Error (RMSE).

The dataset incorporates the information from the Ames Assessor's Office. The data includes 2930 observations and 82 variables which was collected from house sales from 2006 to 2010. 

**Datasets Used:**

[Ames, Iowa Housing Data (2006 - 2010)](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

**Summary:**  

The analysis is broken down into four notebooks:

1. Cleaning and EDA
2. Pre-Processing, Feature Engineering, and Model Benchmarks
3. Model Tuning and Kaggle Submission
4. Cleaning the Test Dataset

**Conclusions and Recommendations:**

The best model to predict home sale prices in Ames, Iowa was the Ridge model. This model had the best bias-variance tradeoff with a mean train RMSE of 19866 and a mean test RMSE of 25848. The R2 scores show that our variance in our predictions can be explained by 90% in our train dataset and 87% in our test dataset.  

The Pearson correlation matrix was utilized to filter dependence among the numerical predictor variables. High coefficients within variables in the Pearson correlation analysis were removed. The distribution of the target variable (Sale Price of Homes) were not normally distributed. A log transformation of the target variable had to be conducted in order to have a normal distribution of our target variable. After creating an initial model, the Ridge and LASSO regularization methods were utilized to provide a better bias-variance trade off.

Compared to the baseline model, the generated Ridge model performs better at predicting house prices. The baseline model had approximately 80000 in mean error compared to the LASSO model which had a mean error of 23000 in sale price prediction. 

**Recommendations**  

Even with the Ridge regularization, there is still evidence that the model is overfit. In order to move this project forward, one can reduce complexity by reducing the number of categorical features that were selected in the model. A Spearman correlation analysis can be conducted to reduce the categorical variable complexity in the model. The coefficients of the predictor variables could have been analyzed in the initial OLS model to take out any variables that didn't have a strong correlation in predicting the sale price. Overall, this project can serve as an extremely useful tool to shorten appraisal times and give people the power to appraise their own homes.



