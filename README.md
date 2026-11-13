# Water Potability Prediction

Machine Learning mini project (M.Tech Data Science) that predicts whether a water sample is safe to drink from nine physico-chemical measurements.

## Dataset
Kaggle "Water Quality" dataset (`water_potability.csv`), 3,276 samples, 9 numeric features, binary target `Potability`.
Source: https://www.kaggle.com/datasets/adityakadiwal/water-potability

## Workflow
1. Exploratory data analysis (class balance, histograms, correlation heatmap, box plots)
2. Stratified 80/20 train-test split
3. Median imputation and standard scaling, fitted on the training set only
4. Models: Logistic Regression, Decision Tree, Random Forest
5. Improvement: grid search (5-fold CV) and a class-weighted Random Forest

## Results (test set, 656 samples)
| Model | Test accuracy | Macro F1 |
|---|---|---|
| Logistic Regression | 0.5244 | 0.52 |
| Decision Tree | 0.6463 | 0.54 |
| Random Forest | 0.6616 | 0.59 |
| Tuned Random Forest | 0.6631 | 0.59 |
| Balanced Random Forest | 0.6479 | 0.62 |

Always predicting "not safe" gives 0.6098, so the gain over this baseline is modest.

## Run it
```
pip install -r requirements.txt
jupyter lab
```
Open `Water_quality.ipynb` and run all cells. Keep `water_potability.csv` in the same folder.

## Files
- `Water_quality.ipynb` - code and outputs
- `water_potability.csv` - dataset
- `report/` - project report (PDF)

Author: Priyanshu Sahu
