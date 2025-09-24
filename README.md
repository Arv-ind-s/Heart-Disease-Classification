# Heart Disease Prediction Using Machine Learning

This project explores various Python-based machine learning and data science libraries to build a machine learning model capable of predicting whether or not someone has heart disease based on their medical attributes.

## Table of Contents
- [Problem Definition](#problem-definition)
- [Data](#data)
- [Evaluation](#evaluation)
- [Features](#features)
- [Modeling](#modeling)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Problem Definition

**Can we predict whether or not a patient has heart disease given their clinical parameters?**

This is a binary classification problem where we aim to predict the presence (1) or absence (0) of heart disease in patients based on various medical attributes.

## Data

The dataset originates from the **Cleveland Heart Disease Dataset** from the UCI Machine Learning Repository. An identical version is also available on Kaggle for easy access.

- **Source**: UCI Machine Learning Repository (Cleveland data)
- **Alternative Source**: Kaggle
- **Type**: Clinical patient data
- **Target Variable**: Binary (0 = No heart disease, 1 = Heart disease present)

## Evaluation

**Success Criteria**: If we can achieve **95% accuracy** at predicting whether or not a patient has heart disease during the proof of concept, we will pursue the project further.

**Metrics Used**:
- Accuracy
- Additional classification metrics (precision, recall, F1-score)

## Features

### Data Dictionary

| Feature | Description | Values/Units |
|---------|-------------|--------------|
| `age` | Age in years | Numeric |
| `sex` | Gender | 1 = Male, 0 = Female |
| `cp` | Chest pain type | Categorical (0-3) |
| `trestbps` | Resting blood pressure | mmHg on admission to hospital |
| `chol` | Serum cholesterol | mg/dl |
| `fbs` | Fasting blood sugar > 120 mg/dl | 1 = True, 0 = False |
| `restecg` | Resting electrocardiographic results | Categorical (0-2) |
| `thalach` | Maximum heart rate achieved | Numeric |
| `exang` | Exercise induced angina | 1 = Yes, 0 = No |
| `oldpeak` | ST depression induced by exercise relative to rest | Numeric |
| `slope` | Slope of the peak exercise ST segment | Categorical (0-2) |
| `ca` | Number of major vessels colored by fluoroscopy | 0-3 |
| `thal` | Thalassemia | 3 = Normal, 6 = Fixed defect, 7 = Reversible defect |
| `target` | Heart disease diagnosis | 1 = Disease present, 0 = No disease |

## Modeling

### Algorithms Implemented
1. **Logistic Regression**
2. **K-Nearest Neighbors (KNN)**
3. **Random Forest Classifier**

### Model Optimization
- **Hyperparameter Tuning Methods**:
  - Random Search CV
  - Grid Search CV
- **Model Comparison**: Performance comparison across all three algorithms
- **Cross-validation**: Used for robust model evaluation

## Experimentation

The project follows a systematic approach to machine learning experimentation:

1. **Data Exploration**: Understanding the dataset structure and characteristics
2. **Data Preprocessing**: Cleaning and preparing data for modeling
3. **Feature Engineering**: Optimizing features for better model performance
4. **Model Training**: Training multiple algorithms
5. **Hyperparameter Tuning**: Optimizing model parameters using grid search and random search
6. **Model Evaluation**: Comparing models using various metrics
7. **Model Selection**: Choosing the best performing model

## Technologies Used

- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Scikit-learn**: Machine learning algorithms and tools
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter Notebook**: Development environment

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/heart-disease-prediction.git

# Navigate to the project directory
cd heart-disease-prediction

# Install required packages
pip install -r requirements.txt
```

## Usage

```python
# Import necessary libraries
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.neighbors import KNeighborsClassifier

# Load the dataset
df = pd.read_csv('heart_disease_data.csv')

# Run the complete analysis
python heart_disease_prediction.ipynb
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- UCI Machine Learning Repository for providing the Cleveland Heart Disease Dataset
- Kaggle community for data accessibility
- Open source contributors to the Python data science ecosystem

---

**Note**: This is a proof-of-concept project for educational and research purposes. The model should not be used for actual medical diagnosis without proper validation and medical professional oversight.
