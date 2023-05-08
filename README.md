# backend (node.js)

- [Node.js doc](https://nodejs.org/en/docs)
- [Express.js doc](https://expressjs.com/en/starter/installing.html)
- [MongoDB doc](https://www.mongodb.com/docs/atlas/)
- [Mongoose doc](https://mongoosejs.com/docs/guide.html)

---

## Node.JS

- Node.js allows you to run JavaScript on the server
- Node.js is an open-source. cross platform. JS runtime environment.
- It is not a language.
- It is not a framework.
- It is built on the V8 JavaScript engine used by Google Chrome
- `Node.js = Runtime Environment + JavaScript Library`

#### What Can Node.js Do?

- Node.js can generate dynamic page content
- Node.js can create, open, read, write, delete, and close files on the server
- Node.js can collect form data
- Node.js can add, delete, modify data in your database

#### Download Node.js

- The official Node.js website has installation instructions for Node.js: [node.js](https://nodejs.org)
- If you want to make sure node.js is installed, Type this command in the command screen

```sh
  > node -v
```

#### Browser vs Node.js

- Node.js and a browser are both software environments used to execute JavaScript code.
- Node.js supports both the <b> commonJS </b> and <b>ES module</b> systems
- Browser we are Starting to see teh <b>ES module </b>standard being implemented
- Node.js is designed for server-side JavaScript programming,
- browser is designed for client-side web application development and content rendering.
- In the browser, we don't have all the nice APIs that node.js provides through its modules.
- In node.js, we don't have the <b>document </b>, <b>window</b> and all the other objects that are provided by the browser.

#### Module

- A module is an encapsulated and reusable chunk of code that has its own context.
- In node.js, each file is treated as a separate module.

#### Types of modules:

1. Local modules:
   - modules that we create in our application
2. Built-in modules:
   - modules that Node.JS ships with out of the box.
3. third Party modules:
   - modules written by other developers that we can use in our application.

## MongoDB

### What is mongoDB

- MongoDB is an open source **NoSQL** database management program.
- MongoDB works on concept of collection and document.

### SQL vs Document Databases

- SQL databases are considered relational databases. They store related data in separate tables.
- When data is needed, it is queried from multiple tables to join the data back together.
- MongoDB is a document database which is often referred to as a non-relational database. This does not mean that relational data cannot be stored in document databases
- It means that relational data is stored differently. A better way to refer to it is as a non-tabular database.
- MongoDB stores data in flexible documents. Instead of having multiple tables you can simply keep all of your related data together. This makes reading your data very fast.

### Collection

- Collection is a group of MongoDB documents.
- A collection exists within a single database.
- Collections do not enforce a schema.
- Documents within a collection can have different fields.

### Document

- A document is a set of **key-value pairs**.
- Documents have **dynamic schema**.
- **Dynamic schema** means that documents in the same collection do not need to have the same set of fields or structure, and common fields in a collection's documents may hold different types of data.

### Why Use MongoDB?

- Document Oriented Storage:- Data is stored in the form of JSON style documents.
- Index on any attribute
- Replication and high availability
- Auto-Sharding
- Rich queries
- Fast in-place updates
- Professional support by MongoDB

### Install MongoDB

- To install MongoDB, first download the latest release of MongoDB [Download](https://www.mongodb.com/download-center)
- To verify that it has been installed properly, open your terminal and type:

```sh
> mongosh --version
```

### MongoDB Basics

- Data formats

  - In MongoDB, you will often deal with **JSON** and **BSON formats**. Therefore, it’s important to fully understand them.

- JSON

  - JSON stands for JavaScript Object Notation. JSON syntax is based on a subset of JavaScript

- A JSON document is a collection of fields and values in a structured format. For example:

```sh
{
   "first_name": "John",
   "last_name": "Doe",
   "age": 22,
   "skills": ["Programming","Databases", "API"]
}
```

### Create Database

#### The use Command:

- MongoDB **use DATABASE_NAME** is used to create database. The command will create a new database if it doesn't exist, otherwise it will return the existing database.

```sh
> use DATABASE_NAME
switched to db mydb
```

- If you want to check your databases list, use the command **show dbs**.

```sh
> show dbs
local        0.78125GB
test         0.23012GB
```

### Drop Database

#### The dropDatabase() Method

- MongoDB **db.dropDatabase()** command is used to drop a existing database.

```sh
> db.dropDatabase()
- This will delete the selected database. If you have not selected any database,
then it will delete default 'test' database.
```

### Create Collection

#### The createCollection() Method

- MongoDB **db.createCollection(name, options)** is used to create collection.

```sh
> db.createCollection(name, options)
- In the command, name is name of collection to be created.Options is a document and is used to specify configuration of collection.
```

- **Options parameter** is optional, so you need to specify only the name of the collection. Following is the list of options you can use :-

| Field       | Type    | Description                                                                 |
| ----------- | ------- | --------------------------------------------------------------------------- |
| autoIndexId | Boolean | If true, automatically create index on \_id field.s Default value is false. |

```sh
> use test
switched to db test
> db.createCollection("mycollection")
{ "ok" : 1 }
```

- You can check the created collection by using the command **show collections**.
```sh
> show collections
mycollection
```

### Drop Collection

#### The drop() Method
- MongoDB's **db.collection.drop()** is used to drop a collection from the database.

```
 > db.COLLECTION_NAME.drop() 
 ```
-  check the available collections into your database mydb.
```
> use mydb
switched to db mydb

> show collections
mycol
mycollection
system.indexes
tutorialspoint
```
- Now drop the collection with the name mycollection.

```
> db.mycollection.drop()
true
```
- Again check the list of collections into database.
```
> show collections
mycol
system.indexes
tutorialspoint
```

### Datatypes

| DataType | Description|
|----------| -----------|
|String| This is the most commonly used datatype to store the data. String in MongoDB must be UTF-8 valid.|
|Integer| This type is used to store a numerical value. Integer can be 32 bit or 64 bit depending upon your server.| 
|Boolean|This type is used to store a boolean (true/ false) value. | 
|Double| This type is used to store floating point values.| 
|Arrays| This type is used to store arrays or list or multiple values into one key.| 
|Object| This datatype is used for embedded documents.| 
|Null| This type is used to store a Null value.| 
|Date|This datatype is used to store the current date or time in UNIX time format.| 
|Object ID|This datatype is used to store the document’s ID.| 
|Code|This datatype is used to store JavaScript code into the document.| 
|Regular expression|This datatype is used to store regular expression.| 


