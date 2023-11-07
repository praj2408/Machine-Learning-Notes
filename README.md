# Machine-Learning-Practical-Notes

![](https://github.com/praj2408/Machine-Learning-Practical-Notes/blob/main/Notes/Concept%20Drift.jpg)
![](https://github.com/praj2408/Machine-Learning-Practical-Notes/blob/main/Notes/Data%20Drift.jpg)
![](https://github.com/praj2408/Machine-Learning-Practical-Notes/blob/main/Notes/MSE%20MAE.jpg)
![](https://github.com/praj2408/Machine-Learning-Practical-Notes/blob/main/Notes/RMSE.jpg)
![](https://github.com/praj2408/Machine-Learning-Practical-Notes/blob/main/Notes/R2%20Score.jpg)
![](https://github.com/praj2408/Machine-Learning-Practical-Notes/blob/main/Notes/Adjusted%20R2%20score.jpg)
## R2 Score and Adjusted R2 Score
The R-squared (R2) and adjusted R-squared (adjusted R2) are both statistical measures commonly used in regression analysis to assess the goodness of fit of a model. Here's when to use each of them:

**R-squared (R2):**

- Use R2 when you want to assess the goodness of fit of a regression model.
- R2 measures the proportion of the variance in the dependent variable that is explained by the independent variables in the model. It ranges from 0 to 1, with higher values indicating a better fit.
- R2 is easy to interpret, and a higher R2 suggests that a larger portion of the variability in the dependent variable is explained by the model.

**Adjusted R-squared (adjusted R2):**

- Use adjusted R2 when you want to account for the number of independent variables in your model.
- Adjusted R2 adjusts the R2 value by penalizing the addition of unnecessary variables to the model. It takes into account the degrees of freedom, and it generally provides a more realistic assessment of model fit, especially in cases with multiple predictors.
- As you add more variables to a regression model, the R2 may artificially increase even if the new variables do not contribute meaningfully to explaining the dependent variable. Adjusted R2 helps mitigate this issue by providing a more conservative estimate of goodness of fit.

In summary, use R2 to gauge the overall goodness of fit of your regression model, but be cautious when you have many predictors. In such cases, adjusted R2 is a better choice as it adjusts for the complexity of the model and provides a more reliable indication of how well the model generalizes to new data while avoiding overfitting.
