# MasterClass Part (FinTech): Sessions 3 & 4

Exercises and the final project of the Part Institute MasterClass FinTech bootcamp. All work is in Python (pandas, scikit-learn, XGBoost, SHAP).

## Structure

```
datasets/        raw data used by the exercises and the project
notebooks/       Jupyter notebooks (one per exercise, one for the project)
presentation/    final project slides
reports/         written reports
Bootcamp_Summary.html
requirements.txt
```

## notebooks/

| File | Content |
|---|---|
| `exercise1_comedy_show.ipynb` | Decision tree on a small comedy-show dataset: predicts whether to go to a show; Gini vs entropy, tree plots, feature importance, synthetic rows and leave-one-out validation. |
| `exercise2_boston_house_prices.ipynb` | Random Forest regression on Boston house prices (506 rows): RMSE and R², effect of the number of trees, cross-validation and column sensitivity. |
| `exercise3_titanic.ipynb` | Titanic survival classification with Random Forest: cleaning, feature importance, confusion matrix, depth tuning and Kaggle submission files. |
| `exercise4_give_me_some_credit.ipynb` | Credit default prediction on the imbalanced Give Me Some Credit data: baseline forest, imbalance handling, threshold tuning, precision-recall analysis. |
| `exercise5_women_vs_men_ansur.ipynb` | Classifying women vs men from ANSUR II body measurements: single decision tree vs Bagging, accuracy and confusion matrices. |
| `credit_risk_scoring_project.ipynb` | Final project: credit risk scoring on German Credit: EDA, preprocessing, model comparison, imbalance handling, SHAP/LIME explanations, fairness and business cost analysis. |

## datasets/

| Folder / file | Content |
|---|---|
| `ex1_comedy/data.csv` | 13 rows: Age, Experience, Rank, Nationality, Go (target). |
| `ex2_boston/boston_house_prices.csv` | Boston housing: 506 neighborhoods, 13 features, target MEDV (median home value). |
| `ex3_titanic/Titanic.csv` | Titanic training data (891 passengers) with the Survived label. |
| `ex3_titanic/test.csv` | Titanic test data (418 passengers) without labels, used for Kaggle submissions. |
| `ex4_give_me_some_credit/GiveMeSomeCredit.csv` | About 150k borrowers; target `SeriousDlqin` (serious delinquency within two years). |
| `ex5_ansur/ANSUR_II_MALE.csv` | ANSUR II body measurements of 4,082 men (US Army personnel survey). |
| `ex5_ansur/ANSUR_II_FEMALE.csv` | ANSUR II body measurements of 1,986 women. |
| `project_german_credit/german.data` | German Credit (Statlog): 1,000 applicants, 20 categorical/numeric attributes, good/bad credit label. |
| `project_german_credit/german.data-numeric` | Numeric-encoded version of the same data. |
| `project_german_credit/german.doc` | Official attribute description and cost-matrix notes. |
| `project_german_credit/Index` | File index from the UCI repository. |
| `project_german_credit/statloggermancreditdata.zip` | Original archive from the source. |

## reports/

| File | Content |
|---|---|
| `Report_Exercises_Session3_4.docx` | Report for the five exercises: method, results, tables and figures, numbered equations, Titanic Kaggle scores and a summary chapter. |
| `Report_Final_Project.docx` / `.pdf` | Executive business report of the credit risk project: model choice, metrics, explainability, fairness and business recommendations. |

## presentation/

| File | Content |
|---|---|
| `Credit_Risk_Final_Project.pptx` | 14-slide deck presenting the final project results. |

## Other files

| File | Content |
|---|---|
| `Bootcamp_Summary.html` | Summary of what was learned in the bootcamp, with a glossary and the final project overview. |
| `requirements.txt` | Python packages needed to run the notebooks: `pip install -r requirements.txt`. |

## Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/
```

Each notebook loads its data by file name (for example `pd.read_csv('Titanic.csv')`), so place the needed file from `datasets/` in the same folder as the notebook before running it, or change the path in the read cell.
