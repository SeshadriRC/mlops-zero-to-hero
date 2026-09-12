# Fundamentals

### What Is Machine Learning?

Think of machine learning as teaching a computer to learn patterns from data instead of programming every rule manually.

With normal programming, you write rules yourself.
With machine learning, you give the computer examples, and it figures out the rules.

Example: Flower Species Prediction

Suppose you want a system that predicts whether a flower is Setosa, Versicolor, or Virginica based on features like:

Petal length

Petal width

Sepal length

Sepal width

You could try writing if-else conditions — but it's nearly impossible to capture every pattern.

Instead, you give the computer:

150 flower samples

Each sample has measurements

Each sample has the correct species label

The machine learning algorithm then learns the relationship between measurements and species.

That learned relationship is called a model.

### What Is a Model?

A model is the final output of machine learning.

It is not the data.
It is not the algorithm.
It is the pattern the algorithm learned from the data.

Think of the model as:

A mathematical function the computer created

It takes inputs (flower measurements)

It outputs predictions (species)

Example: Flower Species Model

After training, the model may learn things like:

If petal length is very small, it's likely Setosa.

If petal length is large and petal width is medium, it’s probably Virginica.

You never coded these rules.
The algorithm found them automatically based on the training data.

When you pass a new flower’s measurements into the model:

Input: Petal length = 5.1, Petal width = 1.8  
Output: Species = Versicolor


The model is simply applying what it learned earlier.

---

# Udemy summarize

### Machine Learning — Simple Summary

**Machine Learning (ML)** is a process where we train a computer with a large amount of **data** so it can **identify patterns and predict an output**.

### Example: Flower Prediction 🌸

Inputs:

* Petal length
* Petal width
* Sepal length
* Sepal width

Output:

* Type of flower

### Traditional Programming

We could write many `if-else` conditions:

```text
If petal length = 4 and sepal width = 6
    → Rose

If petal width = 6 and sepal length = 2
    → Jasmine
```

The problem is that there can be **many possible combinations**, so maintaining endless `if-else` conditions becomes difficult.

### Machine Learning Approach

Instead:

```text
Large Dataset
     ↓
ML Algorithm
     ↓
Training
     ↓
Pattern Identification
     ↓
Mathematical Function
     ↓
Model
     ↓
Prediction
```

During **training**, the algorithm identifies patterns in the data and builds a **mathematical function**.

That mathematical function is called the **ML model**.

For example:

```text
Input:
Petal length = 3
Petal width  = 2
Sepal length = 3
Sepal width  = 3

        ↓

Trained Model

        ↓

Predicted flower type
```

### Important terms

| Term           | Meaning                                     |
| -------------- | ------------------------------------------- |
| **Dataset**    | Collection of data used for training        |
| **Algorithm**  | Method used to learn patterns from data     |
| **Training**   | Process of learning from the dataset        |
| **Model**      | Mathematical function created from training |
| **Prediction** | Output produced by the trained model        |

**Key point:**

> **Model ≠ dataset and Model ≠ algorithm. The model is the mathematical function produced after training an algorithm using data, and it is used for prediction.**

The quality of the **dataset and algorithm** affects the quality of the model's predictions.

---
