# Learn DVC using a project

Please refer to the below repository for this lecture.

https://github.com/iam-veeramalla/Wine-Prediction-Model

## commands used
```bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install dvc dvc_s3
dvc init
dvc add data/winse_sample.csv
ls data/  #win_sample.csv(stored in s3) wine_sample.csv.dvc (checksum file stored in github)

#create an s3 bucket and add as remote for dvc
#configure aws cli cred locally.

dvc remote add -d wineremote s3://bucketname/foldername   ---> saved to .dvc/config --> should be saved to git.
dvc push

#saved to s3 as bucketname/foldername/md5/version_count/checksumvalueasfilename
```

---
# Practicals

<img width="1907" height="1031" alt="image" src="https://github.com/user-attachments/assets/dc911292-2a48-421e-8c3a-f6fa6da1b56d" />


- Now make a simple change to .csv and again give `dvc add`

<img width="1902" height="980" alt="image" src="https://github.com/user-attachments/assets/12f8a29d-a55a-49be-a219-6ec7d15f1415" />

- we can see that checksum is changed.

<img width="1895" height="947" alt="image" src="https://github.com/user-attachments/assets/774e2d0d-b8e6-4b30-99e8-030018939b89" />
