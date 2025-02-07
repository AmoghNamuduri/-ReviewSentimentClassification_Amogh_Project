# Review Sentiment Classification Project

## Overview
This project focuses on building a predictive model for sentiment analysis of movie reviews. Using a labeled dataset of positive and negative reviews, the project explores the application of Decision Tree Classifiers to determine the sentiment of a given review.

The project leverages **Stratified K-Fold Cross-Validation** to evaluate the performance of the model at various depths. The key objective is to identify the optimal `max_depth` for the Decision Tree that balances prediction performance while minimizing the risks of overfitting and underfitting.

---

## Acknowledgment
The dataset and the foundational module used in this project were developed by the **University of California, Berkeley** for its **Data 8** course.

---

## Key Libraries Used
- **Python Standard Libraries**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **scikit-learn**
  - `CountVectorizer`
  - `DecisionTreeClassifier`
  - `StratifiedKFold`
  - `metrics`

---

## Dataset
The dataset includes movie reviews labeled as either `positive` or `negative`. The preprocessing steps involved:
1. Sampling 1,000 positive reviews.
2. Sampling 1,000 negative reviews.
3. Adding a classification column: `1` for positive reviews and `0` for negative reviews.
4. Combining these into a balanced dataset of 2,000 reviews for training and evaluation.

---

## Methodology

### 1. **Data Preprocessing**
- Text reviews were tokenized and converted into a word frequency matrix using `CountVectorizer`.

### 2. **Model Construction**
- A **Decision Tree Classifier** was trained on the tokenized text.
- The `max_depth` of the tree was varied to observe its impact on performance.

### 3. **Cross-Validation**
- **Stratified K-Fold Cross-Validation** (k=10) ensured consistent positive/negative instance ratios across folds.
- Performance metrics such as **F1 Score**, **Precision**, and **Recall** were recorded for each fold.

### 4. **Performance Metrics**
- **Average F1 Score**: Mean F1 score across all folds.
- **Minimum F1 Score**: Lowest F1 score among folds.
- **Maximum F1 Score**: Highest F1 score among folds.

---

## Analysis and Results
### Key Observations
- At a `max_depth` of 4:
  - The model achieved a balance between underfitting and overfitting.
  - Training and testing performance metrics were consistent.
- At `max_depth > 6`, the model exhibited signs of overfitting as training performance improved but testing performance declined.

### Graphical Insights
1. **Average F1 Scores vs. Max Depth**:
   - Visual comparison of training and testing performance trends.
2. **Average and Minimum F1 Scores vs. Max Depth**:
   - Highlighting the variability in performance across folds.

---

## Instructions to Run the Code

1. **Prerequisites**:
   - Python environment with required libraries installed.
   - Access to the dataset (`IMDBReviewsSentiment.csv`).

2. **Steps**:
   - Mount Google Drive to access the dataset.
   - Run each cell sequentially in a Python environment or Jupyter Notebook.
   - Visualize the results and performance metrics.

3. **Adjust Parameters**:
   - Modify the range of `max_depth` in the provided code to explore further.
   - Change the number of folds (`n_splits`) in the `StratifiedKFold` setup.

---

## Conclusion
This project demonstrates the use of Decision Tree Classifiers for sentiment analysis. By systematically evaluating performance at different depths, it identifies the optimal configuration to balance accuracy and generalization. The approach is robust and scalable, making it suitable for larger datasets and more complex models in the future.

---

## License
This project is for educational purposes and is based on resources developed by UC Berkeley's Data 8 course.

---

## Contact
For queries or feedback, please reach out to Amogh / abn5523@psu.edu


