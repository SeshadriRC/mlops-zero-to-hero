Please refer to the below repository for this lecture.

https://github.com/iam-veeramalla/Wine-Prediction-Model


```bash
mkdir mlflow-connect
cd mlflow-connect

py -3.12 -m venv .venv
source .venv/Scripts/activate
py -3.12 -m pip install mlflow

import mlflow
mlflow.set_tracking_uri("http://localhost:7004")
mlflow.set_experiment("my-first-experiment-mlflow")

```

**Before creating experiment**

<img width="1917" height="613" alt="image" src="https://github.com/user-attachments/assets/6cfeec52-a7cb-46e4-a046-8e7943997a92" />

**After creating experiment**
<img width="1917" height="395" alt="image" src="https://github.com/user-attachments/assets/5d2fd472-af5e-4c20-bfb3-9991001276b9" />

<img width="1917" height="492" alt="image" src="https://github.com/user-attachments/assets/e26596dd-ee34-4e42-a5e0-d1b59572c10a" />

