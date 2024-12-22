

## Insights 



1. The end goal of the model is to predict the probability of the student getting admission to a particular university based on his/her grades and marks of various exams.
2. Before training the model we do various preprocessing techniques.
3. As the ‘Serial No.’ column has all unique values we drop it from the dataframe.
4. The data has 500 rows and 8 rows.
5. We want to predict the 'Chance of Admit ' so it becomes the target variable and the rest 7 are features.
6. We will predict the target from the other 7 features.
7. All the columns in the dataset are numeric
8. All the columns do not have null/na values.
9. All the features are fairly normally distributed.(Through visual analysis)
10. All the features do not have any outliers. The data is already cleaned.
11. Through correlation heat-map we see that no features have a correlation greater than 90%.
12. All the features have a positive linear relationship.
13. All the students with top grades seem to do some or other research at their colleges.
14. We do a train-test split of 80-20.
15. After scaling the variables with Standard Scaler we check for their respective VIF scores. No feature has a VIF score greater than 5 so we can say that there is no multicollinearity.
16. With the help of Statsmodel OLS we drop the features which have p-value greater than 0.05. So we drop the 2 features of ‘University Rating’ and ‘SOP’
17. Training the model with the help of training features and targets. We also predict the target variable with the help of test data.
18. We check the mean of residual which is pretty close to 0.
19. The visual scatter plot shows heteroskedasticity.
20. The goldfield_quandt test gives a p-value greater than 0.05 so we see it as homoscedasticity
21. The residuals are not normally distributed.
22. Following are the metric scores.
* The mean absolute error is : 0.04554846724251889
* The root mean absolute error is : 0.06514359880691861
* The R2 score is:  0.7696471898847517
* The Adjusted R2 score is:  0.7573943808360682
23. The CGPA feature has the highest model weightage.


## Recommendations



1. The company should focus more on the CGPA of students and then TOEFL score as they are the most influential features.
2. The model R2 and Adj. R2 scores are less than 0.8 so the company can do Polynomial regression.
3. The company can also use models like Lasso and Ridge which help with regularization after Polynomial regression.
4. The company should use more data for training as it will further fine tune the model.
5. Generally students with a Research project have a higher chance of admission.
6. Students with higher university ratings have a higher chance of admission.4
7. The company can filter out students based on research, university rating and CGPA. Lastly put them into categories like high, medium and low chance of admission.
8. By categorising the students they can incur fees accordingly for the process.