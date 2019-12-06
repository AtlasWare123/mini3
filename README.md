## What is MySQL

MySQL is a popular open-source relational database management system (RDBMS) that is developed, distributed and supported by Oracle Corporation. Like other relational systems, MySQL stores data in tables and uses structured query language (SQL) for database access. In MySQL, you predefine your database schema based on your requirements and set up rules to govern the relationships between fields in your tables. Any changes in schema necessitates a migration procedure that can take the database offline or significantly reduce application performance.



## What is MongoDB

MongoDB is an open, non-tabular database developed by MongoDB, Inc. MongoDB stores data as documents in a binary representation called BSON (Binary JSON). Related information is stored together for fast query access through the MongoDB query language. Fields can vary from document to document; there is no need to declare the structure of documents to the system, as documents are self-describing. If a new field needs to be added to a document, then the field can be created without affecting all other documents in the collection, without updating a central system catalog, and without taking the system offline. Optionally, [schema validation](https://docs.mongodb.com/manual/core/schema-validation/index.html)can be used to enforce data governance controls over each collection.



## Which to choose

**MySQL**: There are many use cases for a relational database like MySQL. Any type of application that requires multi-row transactions such as an accounting system, would be better suited for a relational database. MongoDB is not an easy replacement for legacy systems that were built for relational databases.

**MongoDB**: On the other hand, there are a variety of use cases where MongoDB is well-suited. Some of these include real-time analytics, content management, the internet of things, mobile, and other types of applications that are new and can take advantage of what MongoDB has to offer.



## User story for storing data 

In order to win the election, the election team wants to track the altitude of the public towards their candidate, and therefore need to store people's setiments and make analysis on which part to change.



## MySQL Procedure

The MySQL table shows the result and the sentiment.



```python
import pymysql

connection = pymysql.connect(host='localhost',
                             port=3306,
                             user='root',
                             password='root',
                             db='demo',
                             charset='utf8')
```



```python
cursor = connection.cursor()
    
effect_row = cursor.executemany(
    
  	for(e in group):
  	'INSERT INTO `search` (`candidates`, `searchDate`, sentiment)  [
        (cadidate, searchDate,sentiment),
    ])
    
connection.commit()

```




## MongoDB Procedure

```python
import pymongo

myclient = pymongo.MongoClient("mongodb://localhost:27017/")

mydb = myclient["search"]


#check if database exist
dblist = myclient.list_database_names()
if "search" in dblist:
  print("The database exists.")

mydb = myclient["search"]
mycol = mydb["customers"]
#insergt
mydict = { "candidate": "", "searchDate","sentiment":}
x = mycol.insert_one(mydict)
```



## Picture
![](https://github.com/AtlasWare123/mini3/blob/master/img/Figure_1.png）








