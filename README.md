# Predictive Modeling in Crime Data Analysis

## Project Overview
This project applies machine learning techniques to predict the location of crimes in Chicago based on historical data. By analyzing patterns in the **Chicago Police Department's dataset**, the model aims to anticipate criminal occurrences to support proactive law enforcement strategies.

## The Challenge
Crime datasets are often noisy and highly imbalanced. For example, crimes occurring on the "STREET" are disproportionately higher than other locations. This project required significant data cleaning and feature engineering to handle:
* **High Cardinality:** The raw dataset contained categorical variables that would result in over 1,500 columns if standard One-Hot Encoding were used.
* **Geographical Outliers:** Data points falling outside the Chicago geographical bounding box were identified and removed to ensure spatial accuracy.

## Methodology
The project followed a rigorous data science lifecycle:
1.  **Data Preprocessing:** Implemented **Label Encoding** to manage high-dimensional categorical data efficiently without crashing memory.
2.  **Feature Selection:** Analyzed correlation matrices to select the most predictive features, such as `Ward`, `District`, and `Community Area`.
3.  **Modeling:**
    * **Gaussian Naive Bayes:** Selected as the primary model due to its speed and efficiency with large datasets.
    * **Random Forest & SVM:** Implemented for performance comparison.

## Key Results
Initial modeling attempts yielded an accuracy of only **44%**. By refining the feature set—specifically focusing on the `Ward` column and addressing null values—the model performance improved significantly.

* **Final Accuracy:** **81.46%**
* **Kappa Score:** 0.7987
* **95% Confidence Interval:** (0.8061, 0.8229)

These results demonstrate that with proper preprocessing and feature engineering, statistical models can effectively classify crime locations even within complex urban datasets.
