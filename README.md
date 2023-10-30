Got it ✅ — here’s a polished `README.md` for your repo that directly references your 
# Assignment 4: Classification – Decision Trees

## Overview
This project is part of the **University of Arizona – Master’s Coursework**.  
In this assignment, we build and evaluate a **Decision Tree Classifier** to predict whether a victim in the *Fatal Police Shootings* dataset showed **signs of mental illness**.  

We then **regularize (prune)** the decision tree and compare its performance before and after pruning.

The implementation, questions, and solutions are documented in the Jupyter Notebook:  
📓 **`classification_task_decision_trees.ipynb`**

---

## Dataset
The dataset used is **`fatal-police-shootings-data.csv`**, which contains details of fatal police shootings in the U.S.  

### Columns
1. **id** – unique identifier of each victim  
2. **name** – name of a victim  
3. **date** – date of fatal shooting  
4. **manner_of_death** – `Shot`, `Shot and Tasered`  
5. **armed** – weapon information (`undetermined`, `unknown`, `unarmed`)  
6. **age** – age of victim  
7. **gender** – `M`, `F`, or `None` (unknown)  
8. **race** – `W`, `B`, `A`, `N`, `H`, `O`, or `None`  
9. **city** – location of incident  
10. **state** – two-letter postal code abbreviation  
11. **signs_of_mental_illness** – target variable (`True` / `False`)  
12. **threat_level** – incident threat level (`attack`, `other`, `undetermined`)  
13. **flee** – `Foot`, `Car`, `Not fleeing`  
14. **body_camera** – whether body camera footage exists  

---

## Objectives
- Handle missing values and clean the dataset.  
- Encode categorical variables for model training.  
- Build a **Decision Tree Classifier** using `scikit-learn`.  
- Evaluate the model using accuracy and confusion matrix.  
- Visualize the decision tree using Graphviz.  
- **Regularize (prune)** the tree by tuning parameters (`max_depth`, `min_samples_split`, etc.) to prevent overfitting.  
- Compare train/test accuracy and feature importances before and after pruning.  

---

## Steps to Run

### 1. Clone this repo
```bash
git clone git@github.com:JDede1/classification-decision-trees.git
cd classification-decision-trees
````

### 2. Create virtual environment

```bash
python -m venv .venv
.venv\Scripts\Activate   # Windows PowerShell
# OR
source .venv/bin/activate   # Mac/Linux
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `Assignment4_DecisionTrees.ipynb` and run the cells.

---

## Tools & Libraries

* Python 3
* pandas, numpy
* scikit-learn (DecisionTreeClassifier, metrics, model\_selection)
* matplotlib, seaborn
* Jupyter Notebook

> For exporting `.dot` → `.png`, you may need **Graphviz** installed:
>
> ```bash
> sudo apt-get install graphviz   # Linux
> choco install graphviz          # Windows (Chocolatey)
> ```

---

## Results

* A fully grown decision tree tends to **overfit** (high train accuracy, lower test accuracy).
* A **regularized (pruned)** decision tree generalizes better and improves test performance.
* Feature importance analysis shows which predictors contribute most to detecting mental illness signs.

---
