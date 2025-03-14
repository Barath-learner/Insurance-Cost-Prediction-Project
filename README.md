# Insurance Cost Prediction Project

## Project Overview

This project aims to predict medical insurance costs using a Linear Regression model. The dataset contains demographic and health-related features, and the goal is to build a model that estimates insurance expenses based on these factors.

## Dataset Details

The dataset `insurance.csv` includes the following columns:

*   **age:** Age of the beneficiary (integer).
*   **sex:** Gender (male/female).
*   **bmi:** Body Mass Index (BMI) (float).
*   **children:** Number of children covered by the insurance (integer).
*   **smoker:** Smoking status (yes/no).
*   **region:** Residential region (southeast, southwest, northeast, northwest).
*   **expenses:** Individual medical costs billed by insurance (float) - This is the **target variable**.

## Data Preprocessing

### Handling Categorical Variables:

*   **sex:** Mapped to numerical values: 1 (female) and 0 (male).
*   **smoker:** Mapped to numerical values: 1 (yes) and 0 (no).
*   **region:** Encoded as integers: 1 (southeast), 2 (southwest), 3 (northeast), 4 (northwest).  *(Note: This is Label Encoding, which assumes an ordinal relationship.  One-Hot Encoding might be a better choice for 'region'.)*

### No Missing Values:

The dataset was checked for null values, and none were found.

## Model Building

*   **Algorithm:** Linear Regression (from scikit-learn).
*   **Train-Test Split:** 80% of the data was used for training, and 20% for testing.
*   **Features Used:** `age`, `sex`, `bmi`, `children`, `smoker`, `region`.
*   **Target Variable:** `expenses`.

## Evaluation Metrics

*   **R² Score (Coefficient of Determination):**
    *   **Training + Testing Data (Combined):** 0.75 (75% variance explained).
    *   **Test Data Only:** 0.63 (63% variance explained).  *(Note: This is the more important metric for evaluating generalization performance.)*

## Results

The Linear Regression model achieved moderate performance
