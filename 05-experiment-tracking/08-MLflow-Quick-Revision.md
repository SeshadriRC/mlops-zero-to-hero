### MLflow – Quick Revision

**Problem:**

* Data Scientists run multiple experiments by changing:

  * Parameters
  * Algorithms
  * Hyperparameters
* They need to **track and compare different runs** to identify the best model.
* Maintaining this manually in Excel is **time-consuming and unreliable**.

### How MLflow helps

MLflow provides a centralized platform for **experiment tracking and artifact management**.

**Two responsibilities:**

| Role               | Responsibility                                                   |
| ------------------ | ---------------------------------------------------------------- |
| **MLOps Engineer** | Set up and maintain MLflow in a production environment           |
| **Data Scientist** | Integrate MLflow into Python code and log experiment information |

### What MLflow tracks

* Parameters
* Metrics
* Model information
* Experiment/run details
* Artifacts such as:

  * CSV files
  * Trained models
  * Other output files

### Typical Flow

```text
Data Scientist
      ↓
Python ML Code
      ↓
MLflow Python Library
      ↓
MLflow Server
      ↓
Experiment Tracking + Artifact Storage
      ↓
MLflow UI
      ↓
Compare Multiple Runs
```

### Interview Answer

> **MLflow is an MLOps platform used mainly for experiment tracking and artifact management. Data Scientists integrate MLflow into their Python code to automatically log parameters, metrics, models, and other artifacts. MLOps engineers are responsible for setting up and maintaining the MLflow platform. Through the MLflow UI, teams can compare different runs and identify the best-performing model.**
