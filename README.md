# Predictive Modeling in Crime Data Analysis

## 📌 Project Overview
This project focuses on predicting crime locations in Chicago based on historical crime data. By analyzing patterns in criminal activity, the goal is to construct a predictive model that can anticipate criminal occurrences, paving the way for proactive law enforcement strategies.

The project utilizes the **Chicago Police Department's comprehensive dataset**, applying advanced data preprocessing, feature engineering, and machine learning techniques to classify crime locations.

## 📂 Repository Structure
* `src/`: R scripts for data preprocessing, visualization, and model training.
* `docs/`: Full project report and presentation slides.
* `data/`: (Data source instructions below).

## 🛠️ Technologies Used
* **Language:** R
* **Libraries:** `ggplot2`, `caret`, `e1071` (Naive Bayes), `randomForest`, `naivebayes`, `stringr`, `corrplot`
* **Techniques:** Label Encoding, Feature Scaling (Z-score Normalization).

## 📊 Key Methodologies

### 1. Data Preprocessing
* **Cleaning:** Removed null values and duplicates based on Case ID.
* **Geographical Filtering:** Eliminated data points falling outside the Chicago geographical bounding box.
* **Feature Engineering:** Extracted `ZipCode`, `Direction`, and `Avenue` from the raw Block address.
* **Encoding Strategy:** Used **Label Encoding** instead of One-Hot Encoding.
    * *Rationale:* One-Hot Encoding would have created over 1500 columns due to high cardinality, causing memory crashes and computational inefficiency.

### 2. Models Implemented
* **Gaussian Naive Bayes:** Chosen for its efficiency with large datasets and robustness.
* **Random Forest:** Implemented for comparison and feature importance analysis.
* **Support Vector Machine (SVM):** Tested with radial kernels for classification.

## 📈 Results
The Naive Bayes classifier achieved a significant performance improvement after preprocessing and feature selection.

* **Final Accuracy:** **81.46%**
* **95% CI:** (0.8061, 0.8229)
* **Kappa Score:** 0.7987

*Note: Initial attempts yielded ~44% accuracy. The improvement to ~81% was achieved by refining the `Ward` feature and addressing class imbalances.*

## 🚀 How to Run
1. Clone this repository.
2. Download the dataset from the [Chicago Data Portal](https://data.cityofchicago.org/).
3. Place `Crimes.csv` in the `data/` directory.
4. Run `src/01_preprocessing_and_nb.R` to process data and train the Naive Bayes model.
5. Run `src/02_advanced_models.R` to test Random Forest and SVM models.

## 👥 Contributors
* Prabhakara Sai Sandeep Pandellapalli
* Maithili Saran Reddy Lingala
* Sanjanaa Sridhar
