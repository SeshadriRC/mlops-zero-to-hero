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

**How datascientist will do experiment tracking**

- clone the wine prediction repo

<img width="1210" height="183" alt="image" src="https://github.com/user-attachments/assets/9ffe9d13-36f8-45b3-948e-83df4a040204" />

- create a python virtual env and install dvc

```bash
py -3.12 -m venv .venv
source .venv/Scripts/activate
py -3.12 -m pip install dvc
py -3.12 -m pip install dvc_s3
```

- you can run `dvc pull` if in case you need to pull the dataset

<img width="1917" height="477" alt="image" src="https://github.com/user-attachments/assets/06b70553-c5dc-4964-810a-222adcb885cc" />

- There are no tracking information

<img width="1917" height="887" alt="image" src="https://github.com/user-attachments/assets/fb73518d-13a7-4faf-81b8-85dd78e38ead" />

- Now install python `requirements.txt` and run `train.py`

```bash
py -3.12 -m pip install -r requirements.txt
py -3.12 train.py
```

<img width="1916" height="292" alt="image" src="https://github.com/user-attachments/assets/a0ab2b12-eee2-4c3e-8958-98d7dc1aa470" />

