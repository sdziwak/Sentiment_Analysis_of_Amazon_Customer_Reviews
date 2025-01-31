# Sentiment Analysis of Amazon Customer Reviews

## Project Description
This project aims to classify Amazon customer reviews into positive or negative sentiments using machine learning techniques. The dataset consists of labeled reviews with `__label__1` for negative sentiments (1- and 2-star reviews) and `__label__2` for positive sentiments (4- and 5-star reviews).

The final model uses Logistic Regression, which achieved strong accuracy and balanced precision-recall performance, making it suitable for the dataset and available computational resources.

---

## Dataset
- **Source**: [Amazon Reviews for Sentiment Analysis (Kaggle)](https://www.kaggle.com/datasets/bittlingmayer/amazonreviews)
- **Dataset Size**:
  - Train set: 3,600,000 reviews
  - Test set: 400,000 reviews
- **Features**:
  - Review text
  - Sentiment label (positive/negative)

---

## Challenges Faced
1. **Computational Limitations**:
   - Training more complex models like Random Forest with 100 estimators or Gradient Boosting proved computationally expensive due to the dataset size.
   - Gradient Boosting was particularly time-intensive and was abandoned in favor of simpler, faster models.

2. **Model Selection**:
   - Logistic Regression was chosen as the final model due to its balance of simplicity, computational efficiency, and strong performance.

---

## Final Results
### Logistic Regression
- **Training Accuracy**: 88.71%
- **Test Accuracy**: 88.65%

| Metric          | Precision | Recall | F1-Score | Support   |
|------------------|-----------|--------|----------|-----------|
| **Negative (0)**| 0.89      | 0.88   | 0.89     | 200,000   |
| **Positive (1)**| 0.88      | 0.89   | 0.89     | 200,000   |
| **Accuracy**    |           |        | 0.89     | 400,000   |
| **Macro Avg**   | 0.89      | 0.89   | 0.89     | 400,000   |
| **Weighted Avg**| 0.89      | 0.89   | 0.89     | 400,000   |


---

## Model Demonstration
Below are some example predictions made by the Logistic Regression model:

| Comment                                                   | Predicted Sentiment |
|-----------------------------------------------------------|---------------------|
| This product is amazing! I loved every moment using it.   | Positive            |
| Terrible experience. The item broke after one use.        | Negative            |
| Decent quality and quite worth the price.                | Positive            |
| Absolutely fantastic service, highly recommend!          | Positive            |
| Too bad quality for this price.                          | Negative            |

---

## Conclusion
Logistic Regression was chosen as the final model due to its balance of accuracy (88.65% on the test set) and computational efficiency. Attempts to train more complex models, such as Random Forest (`n_estimators=100`) and Gradient Boosting (`n_estimators=100`, `learning_rate=0.1`, `max_depth=3`), were either less effective or infeasible due to high computational demands.


