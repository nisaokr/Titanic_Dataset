# Titanic Survival Prediction

This project aims to predict passenger survival on the famous Kaggle Titanic dataset using machine learning models.

## Project Structure

```
Titanic_Data/
├── Data/
│   └── Raw/
│       ├── train.csv      # Training data
│       └── test.csv       # Test data
├── Src/
│   └── baseline.ipynb     # Baseline analysis and model notebook
└── Submissions/
    ├── submission_lr_baseline.csv  # Logistic Regression results
    └── submission_rf.csv           # Random Forest results
```

## Dataset

The Titanic dataset contains the following features:
- **PassengerId**: Passenger identification number
- **Survived**: Survival status (0: No, 1: Yes)
- **Pclass**: Ticket class (1, 2, 3)
- **Name**: Passenger name
- **Sex**: Gender
- **Age**: Age
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Ticket**: Ticket number
- **Fare**: Ticket fare
- **Cabin**: Cabin number
- **Embarked**: Port of embarkation (C, Q, S)

## Models Used

1. **Logistic Regression**: Basic classification model
2. **Random Forest**: Advanced prediction using ensemble method

## Getting Started

1. Install required libraries:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

2. Run the Jupyter notebook:
```bash
jupyter notebook Src/baseline.ipynb
```

## Results

Model performances are stored in CSV format in the `Submissions/` folder.

## Contributing

1. Fork this repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Create a Pull Request

## License

This project is licensed under the MIT License.
