# Student Performance Prediction System

## Data Mining Project - Classification

**Goal:** Predict whether a student will Pass or Fail using academic data with Machine Learning Classification techniques.

---

## Project Overview

This project implements a complete data mining pipeline to predict student academic performance using:
- **Decision Tree Classifier**
- **Random Forest Classifier**

### Dataset Features
| Feature | Description | Range |
|---------|-------------|-------|
| Attendance | Class attendance percentage | 30-100% |
| Study_Hours | Daily study hours | 0-10 hours |
| Assignment_Marks | Assignment scores | 0-100 |
| Internal_Marks | Internal exam scores | 0-100 |
| Previous_GPA | Previous semester GPA | 4.0-10.0 |
| **Result** | **Target Variable** | **Pass/Fail** |

---

## Project Structure

```
student-performance-prediction/
├── student_dataset.csv              # Original dataset (500 students)
├── student_dataset_preprocessed.csv # Cleaned dataset
├── student_performance_prediction.py # Complete Python code
├── eda_analysis.png                 # Exploratory Data Analysis graphs
├── model_results.png                # Model evaluation graphs
├── final_dashboard.png              # Final prediction dashboard
├── prediction_results.csv           # Sample prediction outputs
└── README.md                        # This file
```

---

## Requirements

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Or use the complete environment:
```bash
pip install -r requirements.txt
```

---

## How to Run

### Option 1: Run in Jupyter Notebook / Google Colab
```python
# Simply run the .py file cell by cell
# Or copy-paste sections into notebook cells
```

### Option 2: Run in VS Code / Terminal
```bash
python student_performance_prediction.py
```

---

## Data Preprocessing Steps

1. **Missing Value Handling**: Filled with median values
2. **Data Cleaning**: Removed duplicates
3. **Outlier Handling**: Capped using IQR method
4. **Encoding**: Label encoding for categorical target
5. **Feature Scaling**: StandardScaler for numerical features
6. **Train-Test Split**: 80% train / 20% test (stratified)

---

## Model Results

| Model | Accuracy | Precision (Pass) | Recall (Pass) | F1-Score | AUC-ROC |
|-------|----------|------------------|---------------|----------|---------|
| Decision Tree | 80.00% | 79% | 85% | 81% | 0.866 |
| Random Forest | 80.00% | 79% | 85% | 81% | 0.882 |

### Feature Importance (Random Forest)
1. Study Hours - 33.4%
2. Previous GPA - 29.0%
3. Assignment Marks - 16.1%
4. Attendance - 11.0%
5. Internal Marks - 10.4%

---

## Prediction Flow

```
Input Student Data
    ↓
[Attendance, Study_Hours, Assignment, Internal, GPA]
    ↓
Model Prediction (Random Forest)
    ↓
Result: Pass / Fail
    ↓
Confidence Score: XX.XX%
```

---

## Sample Predictions

| Student | Attendance | Study | Assignment | Internal | GPA | Prediction | Confidence |
|---------|-----------|-------|-----------|----------|-----|-----------|------------|
| High Performer | 95% | 6.5h | 88 | 85 | 8.5 | **Pass** | 92.82% |
| Average | 70% | 3.0h | 65 | 60 | 6.5 | **Fail** | 96.54% |
| Low Performer | 45% | 1.0h | 35 | 40 | 5.0 | **Fail** | 82.82% |

---

## Graphs & Visualizations Included

- Pass/Fail Distribution (Pie Chart)
- Attendance vs Result (Box Plot)
- Study Hours vs GPA (Scatter Plot)
- Feature Correlation Heatmap
- Average Marks by Result (Bar Chart)
- Study Hours Distribution (Histogram)
- Confusion Matrices
- Feature Importance Comparison
- ROC Curves
- Model Accuracy Comparison
- Decision Tree Structure
- Prediction Confidence Dashboard

---

## Author

**Student Name**  
*Data Mining Project*  
Date: May 2026

---

## License

This project is for academic purposes.
