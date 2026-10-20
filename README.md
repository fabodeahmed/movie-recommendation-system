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

### Phase One

1. Global Mean Baseline
2. User + Movie Bias
3. Tuned User + Movie Bias
4. SVD (Matrix Factorization)
5. Tuned SVD
6. SVD + Bias Ensemble

### Phase Two

1. SVD++ (Improved Collaborative Filtering)
2. SVD++ Hyperparameter Tuning
3. SVD++ + User and Movie Bias Ensemble

## Model Performance

### Phase One Results

Performance was evaluated using **RMSE**, where lower values indicate better performance.

| Model                   | Validation RMSE |
| ----------------------- | --------------: |
| Global Mean             |        1.060875 |
| User + Movie Bias       |        0.880608 |
| Tuned User + Movie Bias |        0.880417 |
| Initial SVD             |        0.906448 |
| Tuned SVD               |        0.898068 |
| **SVD + Bias Ensemble** |    **0.877906** |

### Phase One Best Model

The **SVD + Bias Ensemble** achieved the best validation performance with an RMSE of:

### **0.877906**

The ensemble combined predictions from the tuned User + Movie Bias model and the tuned SVD model.

### Phase Two Results

| Model                     | Configuration                         | Validation RMSE |
| ------------------------- | ------------------------------------- | --------------: |
| Tuned SVD++               | 40 factors, 8 epochs                  |        0.842391 |
| **SVD++ + Bias Ensemble** | **70% SVD++ + 30% User + Movie Bias** |    **0.834601** |

The tuned SVD++ model achieved a validation RMSE of **0.842391** using 40 factors and 8 epochs. Combining SVD++ with the User + Movie Bias model further improved performance, achieving a validation RMSE of **0.834601**.

**Experimental consistency:** A consistent random seed (`random_state=42`) was maintained across approaches where applicable to support reproducibility and fair model comparison.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Surprise
* Matplotlib
* Jupyter Notebook

## Project Structure

```text
movie-recommendation-system/
├── README.md
├── notebook/
│   ├── Movie_Recommendation_Phase_One.ipynb
│   └── Movie_Recommendation_Phase_Two.ipynb
├── presentation/
│   └── movie_recommendation_presentation.pdf
└── results/
    └── model_results.csv
```

## Project Presentation

🎥 [Watch the Phase One Presentation on YouTube](https://youtu.be/rJpq3Xykl8A)

## Future Work

Potential improvements include incorporating movie metadata and content-based filtering, exploring hybrid recommendation approaches, and evaluating additional ensemble techniques. Further experimentation could also investigate advanced recommendation architectures and methods for improving prediction accuracy.

## Author

**Fabode Ahmed Oladele**

Data Analyst | Aspiring Data Scientist

[fabodeahmed@gmail.com](mailto:fabodeahmed@gmail.com)

GitHub: [fabodeahmed](https://github.com/fabodeahmed)
