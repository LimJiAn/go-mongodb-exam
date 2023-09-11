# go-mongodb-exam
[![Go](https://img.shields.io/badge/go-1.21-blue.svg?style=for-the-badge&logo=go&logoColor=white)](https://go.dev/dl/)

> #### 🎯 docker-compose, fiber 를 사용한 mongodb project setup example 입니다.
> #### 🎯 API with Golang + MongoDB + Fiber: Project Setup

## ⚙️ Installation
```shell
$ git clone https://github.com/LimJiAn/go-mongodb-exam
```
## 👀 Usage
#### 1. Run Server (mongo, mongo-express)
```bash
$ docker compose build
```
```bash
$ docker compose up
```
#### 2. Wait 1-2 minutes
```console
[+] Running 2/0
 ✔ Container mongo-expressre  Created                                                                    0.0s
 ✔ Container mongodb          Created                                                                    0.0s
Attaching to mongo-expressre, mongodb
...
...
...
...
mongodb  | {"t":{"$date":"2023-09-11T08:08:27.951+00:00"},"s":"I",  "c":"NETWORK",  "id":23016,   "ctx":"listener","msg":"Waiting for connections","attr":{"port":27017,"ssl":"off"}}
mongo-expressre  | Mongo Express server listening at http://0.0.0.0:8081
```
#### 3. You can see useful mongo-express dashboard at [localhost:8081](http://localhost:8081)
![mongo-express](https://github.com/LimJiAn/go-mongodb-exam/assets/85569173/c7218d0b-9658-49d9-a912-1dd65652dc18)

#### 4. Run bash in mongo container
```bash
$ docker exec -it mongodb /bin/bash
```


#### 5. Connect mongo
###### 1.
```bash
$ mongo -u rootuser -p rootpass
```
> ##### mongoDB 버전에 따라 mongo가 아닌 mongosh 명령어로 접속해야 정상적으로 실행
> ##### The mongo shell is removed from MongoDB 6.0. The replacement is mongosh.
###### 2.
```bash
$ mongosh -u rootuser -p rootpass
```

```console
root@cbf0dbac41ea:/# mongosh
Current Mongosh Log ID:	64fec4ae8bcdddeccdc2e54e
Connecting to:		mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+1.10.6
Using MongoDB:		7.0.1
Using Mongosh:		1.10.6

For mongosh info see: https://docs.mongodb.com/mongodb-shell/

test>
```
