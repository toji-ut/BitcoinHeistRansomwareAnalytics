## Overview

This project involves detecting ransomware in bitcoin transactions by analyzing blockchain data and predicting labels with machine learning models. It classifies transactions as ransomware-related or non-ransomware-related.

## Dataset

- **Source**: [Bitcoin Heist Ransomware Address Dataset](https://archive.ics.uci.edu/dataset/526/bitcoinheistransomwareaddressdataset)
- **Statistics**:
  - Instances: 2,916,697
  - Features: 8 (e.g., address encoded, year, day, length, weight, count, looped, neighbors, income).
  - Ransomware Instances: 41,413
  - Non-Ransomware Instances: 2,875,284

## Workflow

1. **Preprocessing**
   - Cleaned unnecessary columns.
   - Encoded categorical features.
   - Created a balanced subset for training with 1,000 ransomware and 1,000 non-ransomware instances.

2. **Models Used**
   - Random Forest (Accuracy: 92.75%)
   - k-Nearest Neighbors (Accuracy: 79.75%)
   - Logistic Regression (Accuracy: 67.00%)

3. **Evaluation**
   - Metrics: Confusion Matrix, Accuracy.
   - Random Forest outperformed other models due to its robustness against imbalanced datasets.

## Results

- The Random Forest classifier achieved the highest accuracy (92.75%) and was the most effective model for this task.
- Logistic Regression underperformed due to dataset imbalance and the complexity of the features.

## Challenges

- **Imbalance**: The dataset was heavily skewed toward non-ransomware transactions.
- **Scalability**: Processing 3 million rows posed significant computational challenges.

## Conclusion

- Random Forest provided the best results, showcasing the effectiveness of tree-based methods for classification tasks with imbalanced data.
- Improvements in feature engineering and additional advanced models could further enhance accuracy.
