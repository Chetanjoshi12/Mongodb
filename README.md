# MongoDB
![image](https://github.com/user-attachments/assets/e2e99977-f662-4226-b16f-a9b09b7bcdb1)

# Table of Contents
1. [Introduction to MongoDB.](#MongoDB)
   - [What is MongoDB?](#MongoDB)
   - [JSON Vs BSON.](#json/bson)
   - [What is a Document Database?](#Document)
2. [More About MongoDB.](#moreknowledge)
3. [SQL vs NoSQL.](#Compare)
4. [Key Features of MongoDB.](#Keymongodb)
5. [Ordered and Unordered Inserts.](#ordered_unordered)
6. [What are Indexes?](#Indexes)
7. [Benefits of Indexes.](#Index_Benefit)
8. [CRUD operations in MongoDB?](#CRUD)
9. [How MongoDB Works.](#mongodb_works)
10. [Installing MongoDB.](#installing-mongodb)
11. [How do you perform operations in MongoDB?](#usemongodb)
12. [References.](#Reference)




 
 
### Introduction to MongoDB ============>

- ### What is MongoDB?

- MongoDB is an open-source, document-oriented NoSQL database management system. NoSQL databases are quite useful for working with large sets of distributed data. MongoDB is a tool that can manage document-oriented information, and store or retrieve information. 
- Designed for flexibility, scalability, and performance in handling unstructured or semi-structured data.
- NoSQL databases are more scalable and provide superior performance. MongoDB is such a NoSQL database that scales by adding more and more servers and increases productivity with its flexible document model.
- The data stored in the MongoDB is in the format of BSON documents. Here, BSON stands for Binary representation of JSON documents. In other words, in the backend, the MongoDB server converts the JSON data into a binary form that is known as BSON, and this BSON is stored and queried more efficiently.

- ### JSON Vs BSON
- In MongoDB, we write in JSON format only but behind the scene data is stored in BSON (Binary JSON) format, a binary representation of JSON.
- By utilizing BSON, MongoDB can achieve higher read and write speeds, reduced storage requirements, and improved data manipulation capabilities, making it well-suited for handling large and complex datasets while maintaining performance efficiency.

![Screenshot from 2024-08-13 16-01-08](https://github.com/user-attachments/assets/d6955b93-9e6c-420f-a021-20624913b3ac)



- ### What is a Document Database?
- A document database (also known as a document-oriented database or a document store) is a database that stores information in documents.


![image](https://github.com/user-attachments/assets/84bdf8ef-fe10-4aba-88a1-282d2f890f40)


### More About MongoDB ============>
It was created by a company called 10gen, which is now known as MongoDB, Inc. The company was founded by Eliot Horowitz and Dwight Merriman in 2007. The first version of MongoDB was released in 2009. The name is MongoDB is derived from the English word “HUMONGOUS”, which roughly means “Gigantic”.





### SQL vs NoSQL ============>

|                               **SQL**                                              |                                  **NoSQL**                          |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
|1- SQL databases are relational databases.                                          |1- NoSQL databases are non-relational databases. |
|2- They use structured tables to store data in rows and columns.                    |2- They provide flexibility in data storage, allowing varied data types and structures.|
|3- Suitable for applications with well-defined schemas and fixed data structures.   |3- Ideal for applications with dynamic or evolving data models. |
|4- E-commerce Platform, HR Management, etc.                                         |4- CMS, Social Media Platforms, Gaming, etc.|
|5- Examples: MySQL, PostgreSQL, Oracle.                                             |5- Examples: MongoDB, Cassandra, Redis. |


### Key Features of MongoDB ============>
1. **Flexible Schema Design**:-
- MongoDB allows dynamic, schema-less data structures.
- Easily accommodate changing data requirements.
2. **Scalability and Performance**:-
- Horizontal scaling supports large datasets and high traffic.
- Optimized read and write operations for fast performance.
3. **Document Oriented Storage**:-
- Data is stored in flexible, JSON-like BSON documents.
- Self-contained units with rich data types and nested arrays.
4. **Dynamic Queries**:-
- Rich query language with support for complex queries.
- Utilize indexes to speed up query execution.
5. **Aggregation Framework**:-
- Perform advanced data transformations and analysis.
- Process data using multiple pipeline stages.
6. **Open Source and Community**:-
- MongoDB is open source with a vibrant community.
- Regular updates, improvements, and support.

### Ordered and Unordered Inserts. ============>
When executing bulk write operations, "ordered" and "unordered" determine the batch behavior.
- Ordered Inserts
  The default behavior is ordered, where MongoDB stops on the first error.
  ```
  db.<collection-name>. insertMany([doc1, doc2, ....]);
  ```
- Unordered Inserts
  When executing bulk write operations with an unordered flag, MongoDB continues processing after encountering an error.
  ```
  db.<collection-name>. insertMany([doc1, doc2, ........1], {ordered: false});
  ```
  

### What are Indexes? ============>
Indexes are specialized data structures that optimize data retrieval speed in MongoDB.
- Indexes store a fraction of data in a more searchable format.
- They enable MongoDB to locate data faster during queries.
- Indexes are separate from collections and multiple indexes can exist per collection.

### Benefits of Indexes. ============>
- Faster Queries: Indexes drastically accelerate data retrieval, particularly for large collections.
- Improved Aggregation: Aggregation operations become more efficient with optimized indexes.
- Efficient sorting: Indexes facilities rapid sorting based on specific fields.
- Indexing on Multiple Fields: Complex queries can be executed efficiently by utilizing multiple fields in indexes.

### What is CRUD operation in MongoDB? ============>
CRUD operations describe the conventions of a user interface that let users view, search, modify parts, and delete the database. MongoDB provides an elegant way of performing CRUD operations with the programming language of your choice through its drivers.
MongoDB documents are modified by connecting to a server, querying the proper documents, and then changing the setting properties before sending the data back to the database to be updated.

### When it comes to the individual CRUD operations:===>

- **Create:** The create operation is used to insert new documents in the MongoDB database.
- **Read:** The read operation is used to query a document in the database.
- **Update:** The update operation is used to modify existing documents in the database.
- **Delete:** The delete operation is used to remove documents from the database.

### How MongoDB Works ============>

![Screenshot from 2024-08-14 12-03-56](https://github.com/user-attachments/assets/4087e81d-5018-4896-b651-96f21a072b48)



### Installing MongoDB Community Edition ============>
**1. To install MongoDB, run these commands in your terminal** ====>
```
sudo apt-get install gnupg curl
```

```
curl -fsSL https://www.mongodb.org/static/pgp/server-7.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
   --dearmor
```

**2. Create a list file for MongoDB** ====>
```
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
```

**3. Reload local package database** ====>
```
sudo apt-get update
```

**4. Install the MongoDB packages** ====>
```
sudo apt-get install -y mongodb-org
```
### Run MongoDB ============>
**1. Start MongoDB** ====>
```
sudo systemctl start mongod
```

**2. Verify that MongoDB has started successfully** ====>
```
sudo systemctl status mongod
```

### How to install MongoDB Compass ============>

- **Click on the link**-  https://www.mongodb.com/try/download/compass

- **After clicking the link, you will be directed to the official MongoDB Compass website. There, you need to select the version, platform, and package, then click on the download button.**

- **Go to the terminal and type this command to install.**
```
sudo dpkg -i (Paste the downloaded package here.)
```
# How do you perform operations in MongoDB? ============>

# How to Check the version of MongoDB? ============> 
```
mongod --version
```

# How to use MongoDB? ============>
To start the MongoDB shell we can do:
To open MongoDB in the terminal run this command:-
```
mongosh
```

# To see the list of all databases in MongoDB, run this command:-
To see the all list of databases in MongoDB we can do: 
```
show dbs
```
# How do you select a particular DB to work on?
To use a Database we can do:
```
use database_name
```
# How to add a new collection on MongoDB?
To create a new collection we can do:
```
db.createCollection ('collection_name')
```
# To see the list of all collections in MongoDB, run this command:-
```
show collections
```
# To Drop the collection in MongoDB, run this command:-
```
db.collection_name.drop()
```
# To Drop the Database in MongoDB, run this command:-
```
db.dropDatabase()
```
# To create a Document in MongoDB, run this command:- 
```
db.collection_name.insertOne({'key1': 'value1', key2: value2.........})
```
# To create multiple Documents in MongoDB, run this command:-
```
db.collection_name.insertMany([  {'key1': 'value1', key2: vlaue2}, {'key3': 'value3', key4: vlaue4}, {'key5': 'value5', key6: value6}  ])
```
# To read all Documents created in MongoDB, run this command:-
```
db.collection_name.find()
```
# To find documents in MongoDB, run this command:-
```
db.collection_name.find({'key1':'value1'})
```
```
db.collection_name.findOne({'key1':'value1'})
```

# When to use Quotes and when not to? ============>
- **Special characters:** If a field name contains special characters or spaces, or starts with a numeric digit, using quotes is necessary.
- **Reserved words:** If a field is a reserved keyword in MongoDB, use quotes to distinguish it from the reserved keyword.

  # Case Sensitivity in MongoDB ============>
  - Collection names are case-sensitive.
  - Field names within documents are also case-sensitive.
  ```
  db.Data.insertOne({'key1': 'value1', key2: value2});
  db.data.insertOne({'key1': 'value1', key2: value2});
  ```

  # To update operations in MongoDB, run these commands:-
  ```
  db.collection_name.updateOne({paste_document-ID}, {$set: {'key1': 'changing_value'}})
  db.collection_name.updateMany({'key1': 'privious_value'}, {$set: {'key1': 'new_value'}})
  ```
  # To Delete operations in MongoDB, run these commands:-
  ```
  db.collection_name.deleteOne({document_ID})
  db.collection_name.deleteMany({'key1': 'value1'})
  ```

  # References ============>
- https://en.wikipedia.org/wiki/MongoDB
- https://www.codewithharry.com/blogpost/mongodb-cheatsheet/
- https://www.w3schools.com/mongodb/
- https://www.geeksforgeeks.org/mongodb-an-introduction/
  




  


