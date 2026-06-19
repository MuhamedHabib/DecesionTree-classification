# Decision Tree Classification — Drug Prediction

> Jupyter notebooks training scikit-learn decision trees to predict the right drug for a patient from clinical features — built around the IBM "ML0101EN" Decision Trees lab.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

## Overview

This repository contains learning notebooks on **decision tree classification** with scikit-learn.

The main task uses the **`drug200.csv`** dataset (200 patient records). Given a patient's
`Age`, `Sex`, `BP` (blood pressure), `Cholesterol`, and `Na_to_K` (sodium-to-potassium ratio),
a `DecisionTreeClassifier` predicts which **drug** (`drugA`, `drugB`, `drugC`, `drugX`, `drugY`)
the patient responded to. The notebooks cover the full flow: loading and encoding the data,
a train/test split, fitting the tree (`criterion="entropy"`, `max_depth=4`), evaluating
accuracy, and visualizing the trained tree.

One additional notebook (in French) applies the same decision-tree workflow to a **different**
dataset — scikit-learn's built-in `load_breast_cancer` — as a separate practice exercise.

## Notebooks

| Notebook | Dataset | Task | Reported accuracy* |
|----------|---------|------|--------------------|
| `ML0101EN-Clas-Decision-Trees.ipynb` | `drug200.csv` | Predict drug from patient features | 0.9833 |
| `ML0101EN-Clas-Decision-Trees-drug-py-.ipynb` | `drug200.csv` | Predict drug from patient features | 0.9833 |
| `ML0101EN-Clas-Decision-Trees-drug-py-v1 (1).ipynb` | `drug200.csv` | Predict drug from patient features | 0.9833 |
| `ArbreDeDecision_4DS_etudiant.ipynb` | sklearn `load_breast_cancer` | Decision-tree classification exercise (in French) | 0.9532 |

\* Accuracy values are taken from the saved cell outputs in each notebook for the train/test
split used there; rerunning with a different random seed may produce different numbers.

## Tech Stack

- **Python** / **Jupyter Notebook**
- **scikit-learn** — `DecisionTreeClassifier`, `train_test_split`, `metrics`, `datasets`
- **pandas** — data loading and preprocessing (drug notebooks)
- **NumPy** — array operations
- **matplotlib** — plotting / tree image display
- **pydotplus** + **six** — exporting and rendering the decision tree graph

## Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/MuhamedHabib/DecesionTree-classification.git
cd DecesionTree-classification

# 2. (Optional) create a virtual environment
python -m venv .venv
source .venv/bin/activate        # on Windows: .venv\Scripts\activate

# 3. Install the dependencies
pip install jupyter scikit-learn pandas numpy matplotlib pydotplus six

# 4. Launch Jupyter
jupyter notebook
```

Then open any of the notebooks listed above and run the cells top to bottom.
The drug notebooks read `drug200.csv` from the repository root.

> **Note on `pydotplus`:** rendering the decision-tree graph requires the system
> **Graphviz** binaries in addition to the `pydotplus` Python package.

## Notes

The three `ML0101EN-*` notebooks are based on the **IBM "ML0101EN" / Cognitive Class
("BigDataUniversity") "Decision Trees" lab** and follow its structure and the `drug200.csv`
dataset. They are kept here as coursework / learning material — credit for the original
lab design and dataset goes to IBM Skills Network. The French notebook
(`ArbreDeDecision_4DS_etudiant.ipynb`) is a student exercise applying the same technique
to a different dataset.

---
<p align="center">Built by <b>Mohamed Habib Khattat</b> — <a href="https://github.com/MuhamedHabib">GitHub (@MuhamedHabib)</a> · <a href="https://www.linkedin.com/in/mohamed-habib-khattat-2b206a173">LinkedIn</a></p>
