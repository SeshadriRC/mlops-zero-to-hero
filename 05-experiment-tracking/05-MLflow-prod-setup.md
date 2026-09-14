Please refer to the below document for the next lecture

https://community-charts.github.io/docs/charts/mlflow/postgresql-backend-installation

## setup postgress db

```bash
RDS --> Postgress --> Easy create --> provide name to db --> enter and confirm master password

4:19 pm
```

<img width="1917" height="823" alt="image" src="https://github.com/user-attachments/assets/4619a77f-33bd-4f0a-9b8d-4215f08e3c9b" />


- DB is in AWS network and you are trying to connect from personal lap psql client, so make DB as public accessible

```bash
modify --> Additional options --> Publicly accessible --> continue --> apply immediately
```

<img width="1917" height="731" alt="image" src="https://github.com/user-attachments/assets/f455fd80-9a4d-4ffc-8731-ee5a4af3e527" />

- Open the port in security group as well

<img width="1917" height="625" alt="image" src="https://github.com/user-attachments/assets/3b0b37ef-52ce-402c-8f45-7ba8c397fcb7" />

- It will ask for the password, so that we can make sure it is able to connect.

<img width="1832" height="733" alt="image" src="https://github.com/user-attachments/assets/d097310e-c557-4df1-a1ca-ec9a77635dd6" />


- connect to database and run below

```bash
create database mlflow;
create user mlflow_user with password 'mlflow_password';
grant all privileges on database mlflow to mlflow_user;
grant all privileges on schema public to mlflow_user;
```

```bash
psql -h database-1.c5k88omakd8d.ap-south-1.rds.amazonaws.com \
     -p 5432 \
     -U postgres \
     -d mlflow

GRANT USAGE, CREATE ON SCHEMA public TO mlflow_user;
```

```bash
kubectl create ns mlflow

helm install mlflow community-charts/mlflow \
  --namespace mlflow \
  --set backendStore.databaseMigration=true \
  --set backendStore.postgres.enabled=true \
  --set backendStore.postgres.host=database-1.c5k88omakd8d.ap-south-1.rds.amazonaws.com \
  --set backendStore.postgres.port=5432 \
  --set backendStore.postgres.database=mlflow \
  --set backendStore.postgres.user=mlflow_user \
  --set backendStore.postgres.password=mlflow_password
```
