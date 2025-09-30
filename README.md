# Titanic Survival Prediction

This project aims to predict passenger survival on the famous Kaggle Titanic dataset using machine learning models. The Titanic dataset is one of the most popular datasets in data science, providing an excellent opportunity to practice classification algorithms and feature engineering techniques.

## 🎯 Project Overview

The sinking of the Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during her maiden voyage, the Titanic sank after colliding with an iceberg, killing 1502 out of 2224 passengers and crew. This tragedy shocked the international community and led to better safety regulations for ships.

This project analyzes what sorts of people were likely to survive the disaster and builds predictive models to classify passenger survival.

## 📁 Project Structure

```
Titanic_Data/
├── Data/
│   └── Raw/
│       ├── train.csv      # Training data (891 passengers)
│       └── test.csv       # Test data (418 passengers)
├── Src/
│   └── baseline.ipynb     # Complete analysis and modeling notebook
└── Submissions/
    ├── submission_lr_baseline.csv  # Logistic Regression predictions (418 predictions)
    └── submission_rf.csv           # Random Forest predictions (418 predictions)
```

## 📊 Dataset Description

The Titanic dataset contains information about passengers aboard the RMS Titanic. Here are the key features:

### Training Data (891 passengers)
- **PassengerId**: Unique passenger identification number
- **Survived**: Survival status (0: Did not survive, 1: Survived) - **Target Variable**
- **Pclass**: Ticket class (1: First class, 2: Second class, 3: Third class)
- **Name**: Passenger name
- **Sex**: Gender (male/female)
- **Age**: Age in years (some missing values)
- **SibSp**: Number of siblings/spouses aboard the Titanic
- **Parch**: Number of parents/children aboard the Titanic
- **Ticket**: Ticket number
- **Fare**: Passenger fare
- **Cabin**: Cabin number (many missing values)
- **Embarked**: Port of embarkation (C: Cherbourg, Q: Queenstown, S: Southampton)

### Test Data (418 passengers)
- Same features as training data except for the `Survived` column (which we need to predict)

## 🤖 Machine Learning Models

This project implements and compares two different machine learning approaches:

### 1. Logistic Regression (Baseline Model)
- **Type**: Linear classification algorithm
- **Purpose**: Establishes a baseline performance for comparison
- **Advantages**: Simple, interpretable, fast training
- **Use Case**: First model to understand the data and feature importance

### 2. Random Forest
- **Type**: Ensemble learning method using multiple decision trees
- **Purpose**: Advanced model for better prediction accuracy
- **Advantages**: Handles non-linear relationships, reduces overfitting, provides feature importance
- **Use Case**: Improved performance through ensemble methods

## 🔧 Technical Implementation

### Data Preprocessing
- Handling missing values in Age, Cabin, and Embarked features
- Feature engineering for family size and title extraction
- Encoding categorical variables
- Scaling numerical features

### Feature Engineering
- **Family Size**: Combining SibSp and Parch to create total family members aboard
- **Title Extraction**: Extracting titles from passenger names (Mr., Mrs., Miss, etc.)
- **Age Groups**: Creating age categories for better model performance
- **Fare Groups**: Categorizing fare amounts

### Model Training
- Train-validation split for model evaluation
- Cross-validation for robust performance estimation
- Hyperparameter tuning for optimal model performance

## 📈 Results & Performance

### Submission Files Generated
- **Logistic Regression Baseline**: `submission_lr_baseline.csv` (418 predictions)
- **Random Forest**: `submission_rf.csv` (418 predictions)

### Model Performance Metrics
Both models have been trained and tested on the provided datasets. The models generate predictions for 418 test passengers, formatted according to Kaggle submission requirements.

### Key Insights from Analysis
1. **Gender**: Female passengers had significantly higher survival rates
2. **Class**: First-class passengers were more likely to survive
3. **Age**: Children had better survival chances
4. **Family Size**: Moderate family sizes (2-4 members) had optimal survival rates
5. **Embarkation**: Passengers from Cherbourg showed different survival patterns

## 🚀 Getting Started

### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Required Python libraries

### Installation

1. Clone this repository:
```bash
git clone https://github.com/nisaokr/Titanic_Dataset.git
cd Titanic_Dataset
```

2. Install required libraries:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

3. Run the analysis notebook:
```bash
jupyter notebook Src/baseline.ipynb
```

### Running the Models

The notebook contains:
- Complete data exploration and visualization
- Data preprocessing and feature engineering
- Model training and evaluation
- Prediction generation for submission

## 📋 Model Outputs

The `Submissions/` folder contains the final predictions:
- Each file contains 418 rows (one for each test passenger)
- Format: `PassengerId,Survived`
- Ready for Kaggle submission

## 🔍 Key Findings

1. **Survival Rate**: Approximately 38% of passengers survived
2. **Gender Effect**: ~74% of women vs ~19% of men survived
3. **Class Effect**: Higher-class passengers had better survival rates
4. **Age Factor**: Children under 16 had higher survival rates
5. **Family Size**: Optimal survival for families of 2-4 members

## 🛠️ Future Improvements

Potential enhancements for better model performance:
- Advanced feature engineering (cabin location, ticket patterns)
- More sophisticated algorithms (XGBoost, Neural Networks)
- Ensemble methods combining multiple models
- Advanced imputation strategies for missing values
- Feature selection optimization

## 🤝 Contributing

1. Fork this repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 📚 References

- [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)
- [Titanic Dataset Documentation](https://www.kaggle.com/c/titanic/data)
- [Scikit-learn Documentation](https://scikit-learn.org/)
