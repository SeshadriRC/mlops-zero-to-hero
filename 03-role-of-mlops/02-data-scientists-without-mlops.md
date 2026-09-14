[repo](https://github.com/iam-veeramalla/hello-world-mlops/tree/main)

# Role of a Data Scientist

Think of a Data Scientist as the person who turns raw data into insights and a working model.
Their focus is data, logic, and predictions, not deployment, automation, or production systems.

### Understand the Business Problem

The first job is not coding.

A data scientist starts by answering questions like:

What problem are we trying to solve?

What decision will this model help make?

What does “success” look like?

Example:

“Can we predict whether a user will cancel their subscription?”

“Can we classify customer queries into intents?”

At this stage, everything is conceptual.

### Collect and Understand Data

Once the problem is clear, the data scientist works with data:

CSV files

Databases

Logs

Excel sheets

API data

Key activities:

Look at columns and data types

Check missing values

Understand patterns

Identify noisy or irrelevant data

This step is about getting familiar with the data, not building models yet.

### Clean and Prepare the Data

Real-world data is messy.

A data scientist:

Removes duplicates

Handles missing values

Fixes incorrect data

Converts text into numerical form (for ML models)

Normalizes or scales numbers if needed

This step often takes more time than model building.

### Explore the Data (EDA – Exploratory Data Analysis)

Here, the data scientist tries to understand patterns and relationships.

They may:

Plot graphs

Check correlations

Compare distributions

Identify outliers

Goal:

Learn what features are useful

Decide what data helps prediction

This step helps decide which model might work well.

### Build a Simple Model

Now comes the actual machine learning part.

The data scientist:

Chooses a basic algorithm (e.g., logistic regression, decision tree, Naive Bayes)

Trains the model using historical data

Keeps it simple and understandable

At this stage:

Accuracy matters, but clarity matters more

Complex models are avoided for beginners

### Evaluate the Model

After training, the data scientist checks:

Accuracy

Precision / Recall (if needed)

Confusion matrix

They answer questions like:

Is this model better than guessing?

Is it making obvious mistakes?

Is it good enough for a demo or proof of concept?

No production thinking yet — just “Does it work?”

### Save the Model

Once satisfied, the data scientist:

Saves the trained model as a file (e.g., .pkl)

Shares it with the team

At this point:

The model exists as a file

It is NOT deployed

It is NOT automated

The job is almost done.


---

# Udemy summmarize 

## Data Scientist’s Practical ML Workflow — Summary

The lecture shows how a **Data Scientist builds and tests a simple ML model**, using the Iris dataset as an example.

### Main workflow

**1. Understand the business requirement**

* Discuss the requirement with the Product Owner/business team.
* Clearly define what the model needs to predict.

**2. Collect the data**

* Use an existing dataset when available.
* Otherwise gather data from databases, APIs, logs, etc.
* In this example, the **Iris dataset** is already available.

**3. Set up the Python environment**

* Install the required Python version.
* Create a **Python virtual environment**.
* Install dependencies using `requirements.txt`.

**4. Write the training script**
The script generally:

* Loads the dataset.
* Splits data into **training and test data**.
* Selects an ML algorithm.
* Trains the model.
* Evaluates its performance.
* Saves the trained model.

Example:

```text
Iris dataset
     ↓
Train/Test Split (80/20)
     ↓
Logistic Regression
     ↓
Model Training
     ↓
Model Evaluation
     ↓
model.pkl
```

**5. Evaluate the model**

* Test the trained model using test data.
* Track metrics such as accuracy.
* If performance is poor, improve the model and retrain.

**6. Save the model**

* The trained model is saved as an artifact, for example:

```text
artifacts/model.pkl
```

**7. Test predictions**
A separate script can load the saved model and give predictions for new input values.

Example:

```text
Input features → Saved model → Prediction
```

For the Iris dataset:

```text
0 → Setosa
1 → Versicolor
2 → Virginica
```

### Why MLOps is needed

The lecture highlights that the Data Scientist's workflow contains many **manual activities**:

```text
Create environment
      ↓
Install dependencies
      ↓
Run training script
      ↓
Evaluate model
      ↓
Save model
      ↓
Run prediction script
```

Every time the Data Scientist changes the code/model, these steps may need to be repeated manually.

Moving to another machine also means recreating the environment and dependencies.

### 🎯 Key MLOps takeaway

> **The Data Scientist focuses on building and evaluating the model, while the MLOps Engineer focuses on automating this repetitive process and making it reproducible, reliable, and easier to run across environments.**

For your learning, the important MLOps opportunities here are **virtual-environment management, dependency management, reproducible training, automated pipelines, model artifact/version management, and automated evaluation**.


## How the data is represented in a dataset

```bash
python -m pip install scikit-learn
python -m pip install pandas

from sklearn.datasets import load_iris
import pandas as pd
iris=load_iris()
df = pd.DataFrame(iris.data, columns=iris.feature_names)
df["target"] = iris.target
print(df.head())
print("\nTarget Names:", iris.target_names)
```

<img width="1015" height="367" alt="image" src="https://github.com/user-attachments/assets/c1647154-305f-41ee-8fc3-1ba6d89be5f0" />

```bash
target 0 means setosa
target 1 means versicolor
target 2 means virginica
```

## How data scientist write a script to train the algorithm on a dataset 

```bash
python3 -m venv -venv
source venv/Scripts/activate
```

```bash
python -m pip install -r requirements.txt

py -3.11 --version
py --list

https://www.python.org/ftp/python/3.12.8/

py -3.12 -m venv .venv
python --version

py -3.12 -m pip install -r requirements.txt
```

- Train the model

<img width="792" height="136" alt="image" src="https://github.com/user-attachments/assets/df7ef4e0-329c-4419-8980-e85f66384642" />

- Test the model

<img width="882" height="357" alt="image" src="https://github.com/user-attachments/assets/eaccb6d8-87b9-4e3a-bf9e-360bc452bc57" />
