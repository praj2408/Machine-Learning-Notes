![](https://github.com/praj2408/Machine-Learning-Hand-Written-Notes/blob/main/Classification%20Metrics/Accuracy%20and%20Confusion%20Metrics.jpg)
![](https://github.com/praj2408/Machine-Learning-Hand-Written-Notes/blob/main/Classification%20Metrics/Precision%20and%20Recall.jpg)

## Classification Metrics

1. **Accuracy**: Accuracy is one of the most straightforward classification metrics. It measures the ratio of correct predictions to the total number of predictions made by the model. 

   Accuracy = Number of Correct Predictions \ Total Number of Predictions

   While accuracy is easy to understand, it may not be the best metric in cases of imbalanced datasets, where one class significantly outnumbers the others.

3. **Precision**: Precision is a metric that measures the accuracy of positive predictions made by the model. It answers the question: "Of all the instances that the model predicted as positive, how many were correct?"

   Precision = True Positives / (True Positives + False Positives)

   Precision is especially important when false positives are costly or should be minimized.

4. **Recall (Sensitivity or True Positive Rate)**: Recall measures the ability of the model to identify all relevant instances within the dataset. It answers the question: "Of all the actual positive instances, how many did the model correctly predict?"

   Recall = True Positives / True Positives + False Negatives

   Recall is crucial when false negatives should be minimized, such as in medical diagnoses.

5. **F1 Score**: The F1 score is the harmonic mean of precision and recall, providing a balanced metric that considers both false positives and false negatives. It is particularly useful when there is an uneven class distribution.

   F1 Score = 2 (Precision * Recall) / (Precision + Recall)
   
7. **Specificity (True Negative Rate)**: Specificity measures the model's ability to correctly identify negative instances. It is especially relevant in situations where minimizing false positives is critical.

   Specificity = True Negatives / True Negatives + False Positives

8. **AUC-ROC (Area Under the Receiver Operating Characteristic Curve)**: ROC is a graphical representation of a classifier's performance across various threshold settings. AUC-ROC quantifies the overall ability of the model to distinguish between the positive and negative classes. A higher AUC-ROC value indicates a better-performing model.

9. **AUC-PR (Area Under the Precision-Recall Curve)**: The AUC-PR is another way to assess the model's performance, focusing on precision and recall. It is particularly useful when dealing with imbalanced datasets.

10. **Confusion Matrix**: A confusion matrix is a table that visualizes the model's performance by showing the true positive, true negative, false positive, and false negative counts. It's a useful tool for understanding where the model is making errors.

11. **Cohen's Kappa**: Cohen's Kappa measures the agreement between the model's predictions and the actual labels, while taking into account the possibility of random agreement. It's useful when dealing with imbalanced datasets.




## Restrictions of Accuracy

1. **Imbalanced Datasets**: Accuracy can be misleading when dealing with imbalanced datasets, where one class is significantly more prevalent than the others. In such cases, a model that simply predicts the majority class for every instance can achieve high accuracy, but it may not be providing any valuable information about the minority class. It's essential to consider other metrics like precision, recall, F1 score, or AUC-ROC when dealing with imbalanced data.

2. **Misleading for Rare Events**: In applications where the goal is to detect rare events (e.g., fraud detection or disease diagnosis), accuracy can be misleading. A model that rarely predicts the rare event correctly but performs well on the majority class can have high accuracy but may not be useful for the intended purpose. In such cases, recall or precision is often more informative.

3. **Doesn't Account for Different Types of Errors**: Accuracy treats false positives and false negatives equally. Depending on the problem, these types of errors may have significantly different consequences. For instance, in a medical diagnosis scenario, a false negative (failing to identify a disease when it's present) can be more critical than a false positive (incorrectly diagnosing a healthy person as having the disease). Precision and recall provide more nuanced insights into these error types.

4. **Threshold Sensitivity**: Accuracy is independent of the threshold used to make predictions. However, in some situations, choosing different thresholds for classification can significantly affect model performance. Metrics like precision-recall curves and ROC curves can help visualize this threshold sensitivity.

5. **Incomplete Performance Assessment**: Accuracy alone doesn't provide a full understanding of a model's performance. It may not reveal issues related to model bias, overfitting, or other factors that can affect the quality of predictions. A combination of metrics is often necessary for a comprehensive evaluation.

6. **Inappropriate for Multi-Class Problems**: When dealing with multi-class classification problems, accuracy can be misleading, especially when classes have varying sizes or levels of importance. Metrics like macro-averaged F1 score or weighted accuracy that consider class-specific performance are more informative.

7. **Dependent on Data Distribution**: The accuracy of a model is influenced by the distribution of the data. If the data distribution changes over time, the accuracy may not be a reliable metric for monitoring the model's performance.

## Restrictions of Confusion Matrix

1. **Limited to Binary Classification**: A confusion matrix is most commonly used in binary classification (two classes), where you can easily distinguish between true positives, true negatives, false positives, and false negatives. It becomes less intuitive and informative in multi-class classification problems with more than two classes.

2. **Doesn't Show Class Imbalance**: The confusion matrix provides counts of various prediction outcomes, but it doesn't directly indicate class imbalance. In imbalanced datasets, it may be challenging to discern the extent of class skew from the confusion matrix alone.

3. **Insufficient for Comparing Models**: While a confusion matrix is excellent for assessing a single model, it may not be ideal for comparing the performance of multiple models or algorithms. For model comparisons, you'll often want to use summary metrics like accuracy, precision, recall, or the F1 score.

4. **Ignores Thresholds**: The confusion matrix is threshold-agnostic. It doesn't account for the fact that the performance of a model can vary depending on the chosen classification threshold. ROC curves and precision-recall curves are useful tools for assessing threshold-dependent model performance.

5. **Doesn't Address Model Calibration**: A confusion matrix doesn't directly measure the calibration of a model, which refers to how well the model's predicted probabilities align with actual probabilities. A well-calibrated model provides meaningful probabilities that can be used for decision-making.

6. **No Information on Prediction Uncertainty**: The confusion matrix doesn't convey information about the uncertainty associated with model predictions. For certain applications, understanding prediction uncertainty can be critical. This is particularly relevant in fields like healthcare and finance.

7. **Doesn't Reveal Bias or Fairness Issues**: A confusion matrix doesn't explicitly reveal issues related to bias, fairness, or ethical considerations in model predictions. These concerns may require additional analysis and fairness metrics to be properly addressed.

8. **Doesn't Indicate Model Complexity**: The confusion matrix doesn't provide insights into the complexity of the model, such as overfitting or underfitting issues. These aspects can impact a model's generalization ability and predictive performance.

9. **Static Snapshot**: The confusion matrix provides a static snapshot of model performance at a specific point in time. It doesn't reflect how the model's performance might change over time or in different contexts. Monitoring and evaluation should be ongoing processes.

10. **Doesn't Account for Costs and Benefits**: The confusion matrix doesn't consider the specific costs and benefits associated with different types of classification errors. In some applications, misclassifying certain instances may have more significant consequences than others.


## Restrictions of Precision

1. **Doesn't Consider All Relevant Information**: Precision solely focuses on the true positives and false positives and doesn't take into account true negatives and false negatives. This means it provides a limited view of the overall performance of the model, particularly in situations where true negatives or false negatives are of significance.

2. **Sensitive to Class Imbalance**: Precision can be affected by class imbalance. In imbalanced datasets where one class significantly outnumbers the other, achieving high precision may be relatively easy by predicting the majority class as negative for most instances. However, this may not be a meaningful or useful model in practice.

3. **May Sacrifice Recall**: In some cases, optimizing for high precision may lead to lower recall. Precision and recall have an inverse relationship; as you increase precision, you often decrease recall and vice versa. Finding the right balance between precision and recall is important, as excessively high precision at the expense of recall may result in missed relevant instances.

4. **Threshold Sensitivity**: Precision is sensitive to the choice of classification threshold. Adjusting the threshold can significantly impact the precision of a model's predictions. Therefore, precision should be considered in conjunction with other metrics, such as the F1 score, when determining the optimal threshold for a specific application.

5. **May Not Indicate Model's Overall Performance**: High precision doesn't necessarily imply that the model is performing well overall. It's possible to achieve high precision with a model that has poor overall predictive ability if it is overly conservative in making positive predictions.

6. **Ignores True Negatives**: Precision doesn't provide any information about true negatives, which are correctly predicted negative instances. In some applications, both positive and negative predictions are equally important, and a comprehensive evaluation metric, like the F1 score or the Matthews Correlation Coefficient (MCC), might be more appropriate.

7. **Doesn't Consider Consequences of Errors**: Precision treats false positives and false negatives equally. Depending on the application, these errors may have different consequences. Precision may not provide insight into the specific costs or benefits associated with these errors.

8. **Not Suitable for Applications with Varying Importance of Positives**: In applications where the importance or value of correctly identifying positive instances varies, precision alone may not be sufficient. You might need to consider other metrics that account for this variation.

9. **Dependent on Class Definitions**: Precision can be influenced by how the positive class is defined. Modifying the class definition can impact the precision score.


## Restrictions of Recall

Recall, also known as sensitivity or the true positive rate, is a crucial classification metric that measures the ability of a model to correctly identify all relevant instances of a positive class. While recall is essential for many applications, it has certain restrictions and limitations that should be considered:

1. **Trade-off with Precision**: Recall and precision have an inverse relationship. Increasing recall often comes at the cost of decreased precision and vice versa. This trade-off can make it challenging to find the right balance between precision and recall for a specific application. In some situations, it may be more critical to optimize one over the other, depending on the consequences of false positives and false negatives.

2. **May Not Reveal the Full Picture**: Recall provides information about the model's ability to capture true positive instances, but it doesn't take into account false positives, true negatives, and false negatives. Therefore, it doesn't provide a complete picture of a model's overall performance. To get a more comprehensive view, you should consider other metrics like precision, F1 score, or the Matthews Correlation Coefficient (MCC).

3. **Insensitive to True Negatives**: Recall is primarily concerned with positive instances. It doesn't consider the accuracy of predictions for the negative class (true negatives). In some applications, both true positives and true negatives are equally important, and a metric that accounts for both, like accuracy, may be more informative.

4. **Threshold Sensitivity**: Recall is sensitive to the choice of classification threshold. Adjusting the threshold can significantly impact recall. In applications where you need to balance precision and recall, finding the optimal threshold can be crucial.

5. **Inappropriate for Imbalanced Datasets**: In imbalanced datasets where the negative class significantly outnumbers the positive class, achieving high recall may be relatively easy by predicting everything as the negative class. In such cases, recall may not be a meaningful metric, and other measures like the area under the precision-recall curve or the F1 score may be more informative.

6. **Doesn't Consider Consequences of Errors**: Recall treats false negatives and false positives equally. Depending on the application, these errors may have different consequences. Recall may not provide insight into the specific costs or benefits associated with these errors.

7. **Doesn't Address Model Calibration**: Recall doesn't directly measure the calibration of a model, which is the alignment of predicted probabilities with actual probabilities. A well-calibrated model provides meaningful probabilities that can be used for decision-making.

8. **Not Suitable for Applications with Varying Importance of Positives**: In applications where the importance or value of correctly identifying positive instances varies, recall alone may not be sufficient. You might need to consider other metrics that account for this variation.

In summary, recall is a crucial metric for assessing a model's ability to capture relevant positive instances, but it should be used in conjunction with other metrics and domain-specific knowledge to provide a comprehensive evaluation of the model's performance, especially in situations where the trade-off with precision, class imbalance, threshold sensitivity, or varying consequences of errors are relevant considerations.



## F1 Score

The F1 score is a classification metric that combines both precision and recall into a single value, providing a balance between these two metrics. It's particularly useful when you need to consider both false positives and false negatives and when there is an uneven class distribution or a need to find a balance between precision and recall. The F1 score is often used in situations where optimizing for high precision or high recall individually may not be the best strategy.

The formula for the F1 score is:

\[ F1\text{ Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \]

Here's a more detailed explanation of the components and characteristics of the F1 score:

1. **Precision**: Precision measures the accuracy of positive predictions made by a model. It answers the question, "Of all the instances that the model predicted as positive, how many were correct?" Precision quantifies the proportion of true positives among all positive predictions.

2. **Recall**: Recall, also known as sensitivity, measures the ability of the model to correctly identify all relevant instances of the positive class. It answers the question, "Of all the actual positive instances, how many did the model correctly predict?" Recall quantifies the proportion of true positives among all actual positives.

3. **Harmonic Mean**: The F1 score is the harmonic mean of precision and recall. The harmonic mean gives more weight to lower values. As a result, the F1 score is less sensitive to outliers and extreme values. It is particularly suitable for cases where one of the component metrics is much lower than the other.

4. **Balancing Precision and Recall**: The F1 score seeks to balance the trade-off between precision and recall. This balance is crucial in situations where there are consequences to both false positives and false negatives, and you don't want to overly favor one at the expense of the other. For example, in medical diagnoses, it's essential to strike a balance between correctly identifying positive cases (recall) and minimizing false alarms (precision).

5. **Range**: The F1 score ranges from 0 to 1, with 1 indicating perfect precision and recall, and 0 indicating the worst possible performance. An F1 score of 1 means that the model has both perfect precision and recall, while a score of 0.5 suggests that the model has achieved an equal balance between the two.

6. **Choosing the Right Threshold**: The F1 score helps you choose an appropriate classification threshold for your model. Adjusting the threshold can impact both precision and recall, and you can use the F1 score to find the threshold that best aligns with your specific requirements.

7. **Application in Imbalanced Datasets**: In imbalanced datasets, where one class significantly outnumbers the other, the F1 score can be a more informative metric than accuracy. It considers both the ability to capture the minority class (recall) and the accuracy of positive predictions (precision).

8. **Geometric Interpretation**: The F1 score can be geometrically interpreted as the point where the precision-recall curve reaches its peak. This point represents a balance between precision and recall.

In summary, the F1 score is a valuable metric for evaluating classification models, especially when there is a need to balance precision and recall. It provides a single score that summarizes the model's performance, making it easier to compare and assess different models or model configurations.
