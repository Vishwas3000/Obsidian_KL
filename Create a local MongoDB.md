## Setup for installing needed packages

- `brew install mongodb-community@7.0`
- **Start MongoDB Server Locally**
	- `mongod --dbpath /path/to/data`
	- Replace `/path/to/data` with a folder where you want MongoDB to store data (e.g., `~/mongodb_data`).
- `mongosh` to connect to Local mongo DB
- start the service  `brew services start mongodb-community@7.0`
- To have a persistant data  `mongodump --out /backup/mongo`

## To Modify/Add data 

- `use mydatabase`
- Create a Collection & Insert Data
	- Insert a **single document**:
		- `db.users.insertOne({ name: "Alice", age: 25, city: "New York" })`
	- Insert **multiple documents**:
		- `db.users.insertMany([   { name: "Bob", age: 30, city: "Los Angeles" },   { name: "Charlie", age: 22, city: "Chicago" } ])`

## Import csv to mongo db

- `mongoimport --db mydatabase --collection users --type csv --headerline --file users.csv`
- `db.users.stats()` - provides meta data about the collections
- `db.users.deleteMany({})` - delete all 
	- `db.users.drop()`
- 

## Connect to this DB for python

```pyhton
from pymongo import MongoClient

client = MongoClient("mongodb://localhost:27017/")
db = client["mydatabase"]
collection = db["users"]

for user in collection.find():
    print(user)
```

