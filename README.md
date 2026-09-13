# Movie Recommendation System

A machine learning project that predicts user ratings for movies using collaborative filtering techniques and the MovieLens dataset.

## Project Overview

The objective of this project is to predict the rating a user would give to a movie they have not yet rated.

The project explores different collaborative filtering approaches, evaluates their performance using **Root Mean Squared Error (RMSE)**, and combines strong models through ensemble modelling.

## Objective

Build and evaluate recommendation models capable of predicting user–movie ratings and identify the approach that provides the best validation performance.

## Dataset

The project uses the **MovieLens dataset**, containing:

* **10,000,038 user ratings** in the training data
* **5,000,019 user–movie pairs** in the test data
* Ratings ranging from **0.5 to 5.0**
* Additional movie information including genres, tags, tag-genome information, and IMDb metadata

## Exploratory Data Analysis

Initial analysis showed that:

* Ratings have an uneven distribution.
* The mean rating is approximately **3.53**.
* User and movie activity varies across the dataset.
* The Global Mean provides a useful baseline for comparison.

## Models

The following approaches were evaluated:

1. **Global Mean Baseline**
2. **User + Movie Bias**
3. **Tuned User + Movie Bias**
4. **SVD (Matrix Factorization)**
5. **Tuned SVD**
6. **SVD + Bias Ensemble**

## Model Performance

Performance was evaluated using **RMSE**, where lower values indicate better performance.

| Model                   | Validation RMSE |
| ----------------------- | --------------: |
| Global Mean             |        1.060875 |
| User + Movie Bias       |        0.880608 |
| Tuned User + Movie Bias |        0.880417 |
| Initial SVD             |        0.906448 |
| Tuned SVD               |        0.898068 |
| **SVD + Bias Ensemble** |    **0.877906** |

## Final Model

The **SVD + Bias Ensemble** achieved the best validation performance with an RMSE of:

### **0.877906**

The ensemble combined predictions from the tuned User + Movie Bias model and the tuned SVD model.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Surprise
* Matplotlib
* Jupyter Notebook

## Project Structure

```text
movie-recommendation-system/
│
├── README.md
├── notebook/
│   └── movie_recommendation_system.ipynb
│
├── presentation/
│   └── movie_recommendation_presentation.pdf
│
└── results/
    └── model_results.csv
```

## Future Work

The next phase of the project will focus on improving the recommendation performance by exploring additional modelling approaches, richer movie information, and stronger ensemble techniques.

## Author

**Fabode Ahmed Oladele**

Data Analyst | Aspiring Data Scientist

[fabodeahmed@gmail.com](mailto:fabodeahmed@gmail.com)

GitHub: [fabodeahmed](https://github.com/fabodeahmed)
