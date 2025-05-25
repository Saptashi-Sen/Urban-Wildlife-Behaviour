# Urban-Wildlife-Behaviour
## Project Overview
This project focuses on classifying the behavioral adaptation strategies of urban wildlife based on simulated environmental and behavioral data. The target variable, `Adaptation_Signal`, represents the strategy animals use in human-dominated areas (e.g., Exploitation, Avoidance, Habituation, Innovation).

The goal is to predict these strategies using features like species type, observation conditions, environmental factors, and anomaly scores. We experiment with different classification algorithms including Decision Tree, SVM, Naive Bayes, and an ensemble Voting Classifier.

---

## Dataset Description
The dataset contains **1,000 observations** of urban wildlife behavior. It includes the following features:

- `Animal_ID`: Unique identifier
- `Species`: Animal species (Fox, Raccoon, Pigeon, Squirrel)
- `Observation_Time`: Morning, Afternoon, Evening, or Night
- `Location_Type`: Urban zone (Park, Residential, Commercial, Industrial)
- `Noise_Level_dB`: Ambient noise in decibels
- `Human_Density`: Estimated human presence per 100 sqm
- `Food_Source_Score`: Ease of access to food (1–10)
- `Shelter_Quality_Score`: Shelter quality nearby (1–10)
- `Behavior_Anomaly_Score`: Unusualness of behavior (0–1)
- `Estimated_Daily_Distance_km`: Daily distance traveled
- `Adaptation_Signal`: **Target** variable (Exploitation, Avoidance, Habituation, Innovation)

---

## Algorithms Used
1. **Decision Tree**
2. **Support Vector Machine (SVM)**
3. **Naive Bayes**
4. **Voting Classifier (Ensemble of all three)**

---

## Workflow Summary
- Data cleaning and handling missing values
- Label encoding for categorical features
- Feature standardization using `StandardScaler`
- Data split into training, validation, and test sets
- Model training and evaluation using validation data
- Final testing on hold-out set
- Confusion matrix and classification reports generated
- Voting Classifier implemented for ensemble learning

---

## Model Performance (Test Set)
| Model         | Accuracy |
|---------------|----------|
| Decision Tree | 25.0%    |
| SVM           | 34.5%    |
| Naive Bayes   | 34.0%    |
| **Ensemble**  | **37.5%** |

---

## Key Insights
- Ensemble model outperformed individual classifiers.
- SVM showed highest individual performance.
- Class imbalance and subtle feature differences made classification challenging.
- Further improvements could involve hyperparameter tuning and sampling techniques.

---


## Future Work
- Use SMOTE to handle class imbalance
- Apply deep learning models like MLP
- Incorporate time-series trends if available

---

## 👨‍💻 Tools & Libraries
- Python, Pandas, Scikit-learn, Seaborn, Matplotlib
