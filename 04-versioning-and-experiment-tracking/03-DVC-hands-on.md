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

- How multiple datascientist will get to know which dataset we need to use --> By looking into `.dvc/config` file and checking the checksum `data/wine_sample.csv.dvc`

<img width="1917" height="760" alt="image" src="https://github.com/user-attachments/assets/7a2897de-8342-46cf-8fb2-60c4e738a426" />

<img width="1917" height="757" alt="image" src="https://github.com/user-attachments/assets/420975c1-4519-46ad-91c1-ee8544f9aaf1" />

---
# Practicals

<img width="1907" height="1031" alt="image" src="https://github.com/user-attachments/assets/dc911292-2a48-421e-8c3a-f6fa6da1b56d" />


- Now make a simple change to .csv and again give `dvc add`

<img width="1902" height="980" alt="image" src="https://github.com/user-attachments/assets/12f8a29d-a55a-49be-a219-6ec7d15f1415" />

- we can see that checksum is changed.

<img width="1895" height="947" alt="image" src="https://github.com/user-attachments/assets/774e2d0d-b8e6-4b30-99e8-030018939b89" />

- Push `wine_sample-my.csv` to the S3 and push `wine_sample-my.csv.dvc` to the git.

- Create a S3 bucket in aws

<img width="1912" height="593" alt="image" src="https://github.com/user-attachments/assets/0b28b5fb-c19a-410d-a8c7-14b4b60d5660" />

```bash
dvc remote add -d winremote s3://mlops-sesha-bucket
```

<img width="783" height="170" alt="image" src="https://github.com/user-attachments/assets/2dfe857a-9fcb-409b-b049-6bf4f07adebf" />

- Aws creds need to be set before pushing the file

```bash
# Install dependency first, so that you can able to push to S3
py -3.12 -m pip install dvc_s3
```

- `dvc push` to the S3

<img width="1627" height="315" alt="image" src="https://github.com/user-attachments/assets/513a6f45-58bb-4a28-95dd-4b47eafa2242" />

- `checksum` will be matching, you can also download and verify

<img width="1912" height="792" alt="image" src="https://github.com/user-attachments/assets/98fa4f75-1d8e-4ba8-9d9a-86319d775c4d" />

- i downloaded and verified, its matching.
- Now again modify and check the checksum

<img width="1917" height="556" alt="image" src="https://github.com/user-attachments/assets/193a706b-7e7d-4b5a-b709-5263a8da2efd" />

- checksum and git is matching

<img width="1917" height="536" alt="image" src="https://github.com/user-attachments/assets/4612a231-061e-4ec3-af6d-e30878a33220" />

<img width="1062" height="227" alt="image" src="https://github.com/user-attachments/assets/543d348c-7a8f-40a6-984a-90ee30be9129" />
