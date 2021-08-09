# nosql vs sql


 | SQL | NoSQL |
 |-----------|--------|
  |SQL databases are primarily called as Relational Databases (RDBMS)| NoSQL database are primarily called as non-relational or distributed database|
   |SQL databases are table based databases|NoSQL databases are document based, key-value pairs, graph databases or wide-column stores|
 |SQL databases have predefined schema|NoSQL databases have dynamic schema for unstructured data|
 |SQL databases are vertically scalable|NoSQL databases are horizontally scalable|
 |SQL databases uses SQL ( structured query language ) for defining and manipulating the data|In NoSQL database, queries are focused on collection of documents|

 ## kind of data is a good fit a SQL database
 
_If your data is highly structured and associations among the program entities are clearly defined (for instance, if you are developing a point of sale system where you need to store customer orders and product records), **conventional SQL** based databases are the best fit._

 ## The kind of data is a good fit a NoSQL database

 _NoSQL database fits better for the **hierarchical data** storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose_

5-  NoSQL database fits better for the hierarchical data storage

6- SQL databases are vertically scalable

## Part 2:

1- What does SQL stand for?

**Structured Query Language**

2- What is a realational database?

**(RDBMS) A relational database is a type of database that stores and provides access to data points that are related to one another.**

3- What type of structure does a relational database work with?

**A traditional and widely-used data structure is called "B-tree." B-tree structures are a standard part of computer science textbooks and are used in most (if not all) RDBMS products.**

4- What is a ‘schema’?

**A schema, or scheme, is an abstract concept proposed by J. Piaget to refer to our, well, abstract concepts. Schemas (or schemata) are units of understanding that can be hierarchically categorized as well as webbed into complex relationships with one another.**

5- What is a NoSQL database?

**NoSQL databases come in a variety of types based on their data model. The main types are document, key-value, wide-column, and graph**

6- How does it work?

**Each type of NoSQL database would be designed with a specific customer situation in mind, and there would be technical reasons for how each kind of database would be organized. The simplest type to describe is the document database, in which it would be natural to combine both the basic information and the customer information in one JSON document. In this case, each of the SQL column attributes would be fields and the details of a customer’s record would be the data values associated with each field.**

7- What is inside of a Mongo database?

**MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.**

8- Which is more flexible - SQL or MongoDB? and why.

**While MongoDB is more flexible and ensures high and diverse data availability, a SQL Database operates with the ACID (Atomicity, Consistency, Isolation, and Durability) properties and ensures greater reliability of transactions.**

9- What is the disadvantage of a NoSQL database?

**Disadvantages. NoSQL databases don't have the reliability functions which Relational Databases have (basically don't support ACID). This also means that NoSQL databases offer consistency in performance and scalability.**

