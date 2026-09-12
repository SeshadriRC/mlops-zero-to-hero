# How Data Scientists Create a Simple Model

Now that you know what machine learning is and what a model is, the next step is understanding how data scientists actually build one.
Think of this as the “hello world” of ML.

### Start with a Small Dataset

Every model begins with data.

Example:
You want to predict flower species based on features like:

Petal length

Petal width

Sepal length

Sepal width

This dataset will have:

Inputs (features): the measurements

Output (label): the species name

### Split the Data: Train vs Test

Before training, data scientists split the dataset into:

Training data (usually ~80%)
The part the model learns from.

Testing data (usually ~20%)
The part used later to check if the model learned properly.

Why?
Because you should never test a student with questions they already memorized.

### Choose a Simple Model

For beginners, data scientists usually start with a simple algorithm, like:

Logistic Regression (for classification)

Decision Tree

k-Nearest Neighbors (KNN)

For the flower species example, Logistic Regression or Decision Tree works great.

### Train the Model

Training means:

Give the model training data

Let it “learn” patterns between measurements and flower species

Internally, the model adjusts itself to reduce mistakes

You don’t manually code patterns.
The model learns them automatically.

### Test the Model

Now, evaluate it using the test data.

The goal is to see:

How many predictions are correct?

Where is the model making mistakes?

This step tells you if the model is ready or needs improvement.

### Improve (If Needed)

Beginners usually follow simple improvement steps:

Remove noisy or incorrect data

Try a different model

Tune settings (called hyperparameters)

Add more training samples

Even small changes can boost accuracy.

### Save the Model

Once the model performs well, you save it as a file.
Example formats:

.pkl

.joblib

.onnx

This saved model can now be used by:

Apps

Websites

Backend microservices

MLOps pipelines

This is what gets deployed.

---

# Udemy summarize

### How Data Scientists Create an ML Model — Summary

<img width="4000" height="1800" alt="IMG_20260912_065323" src="https://github.com/user-attachments/assets/c91b5fa4-7c28-4092-9627-381757b78081" />


The typical process can be understood in **8 steps**:

```text
Dataset
   ↓
Split Dataset
   ↓
Choose Algorithm
   ↓
Train Model
   ↓
Test Model
   ↓
Retrain / Improve if needed
   ↓
Package Model
   ↓
Deploy / Consume through API
```

### 1. Collect Dataset

The dataset contains **input features + actual output**.

Example:

| Petal Length | Petal Width | Sepal Length | Sepal Width | Flower  |
| -----------: | ----------: | -----------: | ----------: | ------- |
|            4 |           3 |            5 |           6 | Rose    |
|            5 |           4 |            2 |           3 | Jasmine |

---

### 2. Split the Dataset

Typically:

* **80% → Training data**
* **20% → Testing data**

The 80% is used to train the algorithm, while the remaining 20% is kept for testing the trained model.

---

### 3. Choose an Algorithm

Examples mentioned:

* Logistic Regression
* Decision Tree
* K-Nearest Neighbor (KNN)

The **Data Scientist** decides which algorithm is appropriate.

---

### 4. Train the Model

The algorithm learns from the **80% training data**.

It identifies patterns between the input features and the actual output.

```text
Training Data
     ↓
Algorithm
     ↓
Pattern Identification
     ↓
Mathematical Function
     ↓
Model
```

The **model is the output of the training process**.

---

### 5. Test the Model

The model is tested using the **20% data that was not used during training**.

The purpose is to check whether the model produces accurate predictions.

---

### 6. Improve / Retrain

If the model gives poor results, the Data Scientist may:

* Improve/change the dataset
* Choose a different algorithm
* Retrain the model

This process continues until acceptable performance is achieved.

---

### 7. Package the Model

Once the model is satisfactory, it needs to be saved/package for use.

Common formats mentioned:

* `.pkl`
* **Joblib**
* **ONNX**

---

### 8. Deploy / Consume the Model

Software developers or ML engineers can create an **API/application around the model**.

```text
User/Application
       ↓
      API
       ↓
    ML Model
       ↓
   Prediction
```

The model can then be used by a **website, mobile application, or other software application**.

### 🎯 Interview-ready answer

> **“A typical ML model creation process starts with collecting a dataset, splitting it into training and testing data, selecting an algorithm, training the algorithm, testing the resulting model, retraining if the performance is poor, packaging the final model, and finally exposing it through an API or application for consumption.”**

**For MLOps:** Your main interest comes **after/beyond the Data Scientist's model-building work**—automating and managing the training, packaging, deployment, monitoring, and retraining lifecycle.

---
