# Kubeflow Pipelines

Please refer to the below gist for complete demo details.

https://gist.github.com/iam-veeramalla/0e569b5e9da68736e51eda78a895212d

mine - https://gist.github.com/SeshadriRC/b3b0d0f50c69e087ba81197d18c26c40

---

# Summarize 

## Kubeflow & MLOps — Summary

### 1. What is Kubeflow?

* **Kubeflow** is an MLOps platform that helps manage and automate the **machine learning lifecycle**.
* It provides different components for ML workflows.
* An important component is **Kubeflow Pipelines**, which is used to create and automate ML workflows.
* The video covers installation, a Hello World pipeline, and a real-world ML pipeline example. 

### 2. Software Development Lifecycle vs ML Lifecycle

Traditional software development typically involves:

**Planning → Requirements → Design → Development → Testing → Deployment → Monitoring**

This is iterative because new features and bugs cause the cycle to repeat. DevOps introduces tools and automation at these stages to reduce manual effort. 

ML has a similar but more iterative lifecycle:

**Problem Definition → Data Collection/Analysis → Feature Engineering → Model Training → Model Evaluation → Deployment → Monitoring → Retraining**

For example, an ML model may initially perform well, but as new data arrives, its effectiveness can decrease. The model therefore needs to be evaluated, tuned, retrained, and redeployed. 

### 3. Why MLOps?

The main problem is that ML workflows involve a lot of **manual and repetitive operations**.

Many ML engineers may successfully build models on their laptops but struggle to get those models into production because the ML lifecycle is highly iterative. 

**MLOps applies DevOps principles to machine learning.**

In simple terms:

> **MLOps = DevOps practices applied to the ML lifecycle**

It aims to automate/reduce operational effort around activities such as:

* Data processing
* Data analysis
* Model training
* Model evaluation
* Model deployment
* Model monitoring
* Model tuning
* Retraining

MLOps is therefore **more than CI/CD**; it also addresses continuous monitoring, tuning, and retraining of ML models. 

### 4. MLOps tools/platforms

There are two approaches:

**Individual tools**

* Use different tools for different stages of the ML lifecycle.

**Complete/standalone platforms**

* Use an integrated MLOps platform such as **Kubeflow**.
* **MLflow** is another MLOps platform mentioned in the source. 

### Key interview point

For your **DevOps → MLOps** learning:

**DevOps**

> Automates and operates the software development lifecycle.

**MLOps**

> Extends DevOps principles to automate and operate the machine learning lifecycle, including model training, evaluation, deployment, monitoring, tuning, and retraining.

**Kubeflow**

> A platform that provides components for implementing and automating ML workflows, with **Kubeflow Pipelines** being one of its key components. 

Available next action: Create a downloadable PDF file here in this chat containing the finalized decisions and immediate actions above

---

Kubeflow is presented as a more comprehensive, Kubernetes-based MLOps platform made up of several components:

- Kubeflow Pipelines: data loading, training, evaluation, and workflow automation
- Notebooks: interactive development and feature engineering
- Katib: hyperparameter tuning
- Training Operator: model training
- KServe: model deployment and serving
- Model Registry: storing and managing models
- Dashboard: a single interface for Kubeflow components
- Prometheus/Grafana integration: monitoring deployed models

The recommended learning approach is to study one component at a time—starting with Kubeflow Pipelines—rather than trying to learn all of MLOps or Kubeflow at once. Kubeflow components can be installed independently, so a company can choose only what it needs.

Kubeflow requires Kubernetes because its pipelines and ML tasks run as containers/pods in a Kubernetes cluster. For local setup, the text recommends using Kind with Docker Desktop to create a Kubernetes cluster.

---

This section explains how to set up Kubeflow Pipelines locally:

1. Install Docker Desktop.
2. Install Kind, which creates a local Kubernetes cluster.
3. Create a Kind cluster (named for the Kubeflow Pipelines demo) and confirm it is available with `kubectl get nodes`.
4. Follow Kubeflow’s official installation instructions to deploy Kubeflow Pipelines into the cluster.

Kubeflow Pipelines works by converting a Python ML workflow into a YAML configuration using the `kfp` Python package. Kubernetes then runs each pipeline stage—such as loading data, training a model, and evaluating it—as separate containers/pods.

The installation includes Kubernetes custom resource definitions and several Kubeflow-related pods. Internally, Kubeflow Pipelines uses Argo Workflows to coordinate those jobs.

If the standard installation fails on certain Windows or macOS systems, the documentation provides an alternative platform-independent installation command.

Finally, port forwarding exposes the ML Pipeline UI locally, allowing access to the Kubeflow Pipelines dashboard in a browser.

---
