# Predictive Analytics for Heart Health: A Machine Learning Approach

### Author
Md Jafor Sadek

---

## Project Overview
This project predicts the likelihood of heart disease based on health indicators using machine learning. Predictive analytics in this area can play a crucial role in preventative healthcare and assist in early interventions.

## Dataset
- **Name**: Personal Key Indicators of Heart Disease
- **Features**: 18 (9 boolean, 5 string, 4 decimal)
- **Classes**: 2
- **Size**: 319,795 samples, totaling approximately 24 MB

## Methodology
1. **Exploratory Data Analysis (EDA)**: Insights from EDA revealed important feature correlations and helped in understanding the data structure.
2. **Data Preprocessing**: Preprocessed by handling missing values, encoding categorical features, and scaling numeric features.
3. **Model Implementation**: Applied various machine learning algorithms, including:
   - Decision Tree
   - Random Forest
   - XGBoost
   - Gradient Boost
   - AdaBoost
   - Support Vector Machine (SVM)
   - Logistic Regression
   - Nearest Neighbor

4. **Oversampling with SMOTE**: Addressed data imbalance using SMOTE, improving recall and AUC scores in the models.
5. **Hyperparameter Tuning**: Optimized model parameters using `GridSearchCV`.

## Results
### Before Oversampling
- **Best Model**: Random Forest
  - **Accuracy**: 91.1%
  - **Precision**: 0.59
  - **Recall**: 0.045
  - **AUC Score**: 0.52

### After Oversampling
- **Best Model**: Random Forest
  - **Accuracy**: 93.9%
  - **Precision**: 0.96
  - **Recall**: 0.91
  - **AUC Score**: 0.94

## Model Training Time
| Model               | Before Oversampling | After Oversampling |
|---------------------|---------------------|--------------------|
| Decision Tree       | 0.5 sec            | 3.7 sec           |
| Random Forest       | 17 sec             | 1 min 20 sec      |
| XGBoost             | 0.6 sec            | 2.4 sec           |
| Gradient Boost      | 18.7 sec           | 1 min 50 sec      |
| AdaBoost            | 18.6 sec           | 29.2 sec          |
| SVM                 | 130 min            | 198 min 31 sec    |
| Logistic Regression | 0.6 sec            | 5.7 sec           |
| Nearest Neighbor    | 27.8 sec           | 32.2 sec          |

## Conclusion
The Random Forest model achieved the best results in predicting heart disease risk both before and after oversampling. This suggests that Random Forest is effective for this dataset, achieving up to 93.9% accuracy with SMOTE for class balance.

## Limitations and Future Work
- **Limitations**: Although Random Forest performed well, some models (e.g., SVM) had longer training times, which may not be ideal for real-time predictions.
- **Future Work**: Additional features or ensemble methods can be explored to further improve model performance.

## Setup
This project was developed in Python with the following main libraries:
- scikit-learn
- XGBoost
- SMOTE (via `imbalanced-learn`)

Install dependencies with:
```bash
pip install -r requirements.txt
```

## Contact
For questions or feedback, please reach out in my [personal email](jaforsadek619@gmail.com)

**Thank you!**
