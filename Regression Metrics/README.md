
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


## Curse of Dimensionality

The "curse of dimensionality" is a term used in mathematics and computer science to describe the challenges and issues that arise when working with high-dimensional data. It refers to the fact that many algorithms and techniques that work well in low-dimensional spaces become inefficient or impractical when applied to data with a large number of dimensions.

Here are some of the key challenges associated with the curse of dimensionality:

1. Increased computational complexity: As the number of dimensions increases, the computational resources required to process and analyze the data grow exponentially. This can lead to significantly longer processing times and increased memory requirements.

2. Data sparsity: In high-dimensional spaces, data points tend to become more spread out, and the volume of the space increases dramatically. This results in sparse data, making it difficult to find meaningful patterns or relationships in the data.

3. Diminished discriminatory power: High-dimensional data can lead to a decrease in the discriminatory power of many machine learning algorithms. This means that it becomes harder to distinguish between data points, and the predictive performance of models may suffer.

4. Overfitting: In high-dimensional spaces, models are more prone to overfitting, where they fit the noise in the data rather than the underlying patterns. This can result in poor generalization performance.

5. Curse of computational memory: High-dimensional datasets can strain computer memory, making it challenging to store and manipulate the data efficiently.

6. Increased data requirements: As the number of dimensions grows, the amount of data needed to accurately represent and learn from the data also increases. This can be a limiting factor when dealing with high-dimensional datasets.

7. Difficulty in visualization: Visualizing data in high-dimensional spaces is challenging. While techniques like dimensionality reduction can be used to project data onto lower-dimensional spaces for visualization, they may not capture all the important relationships in the data.

To address the curse of dimensionality, practitioners often employ techniques such as feature selection, feature engineering, dimensionality reduction, and regularization methods. These approaches help reduce the dimensionality of the data or mitigate some of the challenges associated with high-dimensional spaces. Additionally, choosing appropriate algorithms and models that are less sensitive to dimensionality issues is important when working with high-dimensional data.


![](https://github.com/praj2408/Machine-Learning-Hand-Written-Notes/blob/main/Regression%20Metrics/MSE%20MAE.jpg)
![](https://github.com/praj2408/Machine-Learning-Hand-Written-Notes/blob/main/Regression%20Metrics/RMSE.jpg)
![](https://github.com/praj2408/Machine-Learning-Hand-Written-Notes/blob/main/Regression%20Metrics/R2%20Score.jpg)
![](https://github.com/praj2408/Machine-Learning-Hand-Written-Notes/blob/main/Regression%20Metrics/Adjusted%20R2%20score.jpg)



# L1 and L2 Regularization
**Introduction to Regularization:**
Regularization is a technique used in machine learning and data science to prevent overfitting, which occurs when a model learns the training data too well, including noise and random fluctuations. Overfitting can lead to poor generalization to unseen data. Regularization helps to control the complexity of the model by adding a penalty term to the loss function, which discourages large coefficients and thus reduces overfitting.

**L1 Regularization (Lasso Regression):**
L1 regularization, also known as Lasso regression, adds a penalty term to the loss function proportional to the absolute values of the coefficients. Mathematically, the L1 regularization term is the sum of the absolute values of the coefficients multiplied by a regularization parameter (lambda or alpha). This penalty encourages sparsity in the model, meaning it tends to push the coefficients of less important features to zero, effectively eliminating them from the model.

In simpler terms, L1 regularization encourages the model to select only the most important features while setting the coefficients of less important features to zero. This can be very useful in situations where you have a large number of features and you want to identify the most relevant ones for making predictions.

**L2 Regularization (Ridge Regression):**
L2 regularization, also known as Ridge regression, adds a penalty term to the loss function proportional to the square of the coefficients. Mathematically, the L2 regularization term is the sum of the squared values of the coefficients multiplied by a regularization parameter (lambda or alpha). Unlike L1 regularization, L2 regularization doesn't force the coefficients to be exactly zero, but it shrinks them towards zero. This tends to produce models with more evenly distributed coefficients.

In simpler terms, L2 regularization penalizes large coefficients but doesn't force them to be exactly zero. Instead, it reduces their impact on the model's predictions, effectively making the model less sensitive to the input data. This can help improve the model's generalization performance by reducing overfitting.

**Comparison:**
- L1 regularization tends to produce sparse models with some coefficients being exactly zero, which can help with feature selection.
- L2 regularization tends to produce models with small, but non-zero coefficients, effectively reducing the impact of less important features without completely eliminating them.

**Conclusion:**
Both L1 and L2 regularization techniques are powerful tools for combating overfitting in machine learning models. Understanding when to use each technique depends on the specific problem you're trying to solve and the characteristics of your data. By incorporating these techniques into your modeling process, you can build more robust and generalizable machine learning models.
