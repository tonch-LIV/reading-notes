# 301_Read_11 - MongoDB and Mongoose

- [NoSQL vs SQL](#nosql-vs-sql)
  - [SQL](#sql-relational-databases)
  - [NoSQL](#nosql-databases)
  - [Features](#features)
  - [Answers.1](#answers1)
- [SQL vs NoSQL - [Video]](#video---sql-vs-nosql)

This is important because...  
Databases solve the problem of data disappearing when the application stops running, by adding the functionality of persistent data. SQL and NoSQL are two approaches to data are two database approaches; each with their individual strengths, weaknesses, and uses cases for different type of applications.

## [NoSQL vs SQL](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

Not competitors or a matter of one being better than the other. The choice of which type of database one uses and makes, ultimately comes down to the type of application one is making and the data that will nedd to be stored, since each solve a different type of problem.  

### SQL (Relational Databases)  

SQL databases are made up of data organized into tables consisting of rows and columns.  
Relationships between tables are established through keys, which allow data to be connected across multiple tables.  
SQL databases are highly organized and excel at maintaining data consistency, because the structure is predefined.  

SQL could be considered a collection of interconnected spreadsheets where every sheet follows strict rules about what data belongs in each column.  

### NoSQL Databases  

NoSQL databases are non-relational and generally store data as documents, key-value pairs, graphs, or column families rather than tables.  
The schemas used are much more flexible and allow records to have different structures even within the same collection.  
This flexibility makes them useful when data changes frequently or isn't easily represented in rows and columns.  

MongoDB is a document database that stores information in JSON-like documents.  

### Features

**Structured vs Unstructured Data**  

- **SQL** databases are best suited for structured data where the format is clearly defined ahead of time and followed throughout the database; every record follows the same schema.

- **NoSQL** databases are somewhat more flexible; they can handle structured, semi-structured, and unstructured data. `Documents` can contain different fields without following the same structure as the rest of the database.  

**Scalability**  

- **SQL** traditionally scales vertically, which means upgrading components like CPU, RAM, and/storage per server.

- **NoSQL** databases scale horizontally; meaning that rather than components, they add more servers and in turn grow easier when handling largw amounts of data.  

**Flexibility / Consistency**  

Wheras **SQL** values consistency, and reliable data through strict schemas and inter-relationships; **NoSQL** has the benefit of being flexible, allowing rapid development and scalability; traits that make it the attractive choice for *web development* and *applications* with evolving requirements.  

### Answers.1

1. Fill in the chart below with five differences between SQL and NoSQL databases:

   | SQL            | NoSQL              |
   | -------------- | -------------------|
   | Relational     | non-Relational     |
   | Fixed schema   | Flexible schema    |
   | Structured     | un/semi-structured |
   | Vertical Scale | Horizontal scale   |

2. What kind of data is a good fit for an SQL database?
    - data with clearly defined relationships and format.
3. Give a real world example.
    - Bank records, (transactions, client, shops, loans, and payment types).  
    - Inventory, (product type, supply, demand, source, shipping).  
    - etc.
4. What kind of data is a good fit a NoSQL database?
    - unstructured or semi-structured that needs constant flexibility.
5. Give a real world example.
    - Product catalogs,  
    - user profiles, (content, information, interactions).  
6. Which type of database is best for hierarchical data storage?
    - NoSQL; represent nested and hierarchical structures through embedded docs and arrays.  
7. Which type of database is best for scalability?  
    - NoSQL; horizontal scaling allows additional servers to be added per demand.

## [[Video] - SQL vs NoSQL](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

**SQL is** used to communicate with relational databases, which store information in tables and establish relationships between said tables.  
    - A major characteristics of SQL databases is their use of schemas; a defined structure for what the data each tables contains and how it's organized; made before any data is stored; creates consistency, but reduces flexibility.

**NoSQL** stores data as `documents` (similar to JS objects and resembles JSON), rather than in tables with strict relationships that SQL uses (MongoDB). This offers the flexibility for documents to have different fields / content.

```js
{
    name: "yoink_B",
    certs: ["ITF+", "A+", "Network+", "GICW JS Web Development"]
},
{
    name: "tonch'Opp",
    age: 54,
    city: "Portland"
}
```

The flexibility comes at a cost though; without strict schemas:
data can become too inconsistent.  
validating the integrity of the data becomes more important,  
relationships between data can be harder to manage.  

Enter Mongoose. Mongoose adds a layer of structure and validation over MongoDB.

### Answers.2

  1. What does SQL stand for?  
      - Structured Query Language.
  2. What is a relational database?  
      - information stored in tables, with tables relating to one or another in one way (key) or other.
  3. What type of structure does a relational database work with?  
      - Tables w/ rows and columns.
  4. What is a 'schema'?  
      - Defines the type of data held by each table, how it's organized.
  5. What is a NoSQL database?  
      - Not Only SQL; non-relational database that uses flexible structures to store data.
  6. How does it work?  
      - no tables; flexible structures such as documents, Key:value pairs, graphs, etc. are used to store data.
  7. What is inside of a MongoDB database?  
      - collections containing documents.
  8. Which is more flexible - SQL or MongoDB? and why?  
      - MongoDB; uses flexible schema that allows documents to contain different fields and structures w/o having to re-design the database.
  9. What is the disadvantage of a NoSQL database?  
      - lack of strict or 'rigid' structure can lead to inconsistent data; relationships between data can become difficult to manage.

## Bookmark and Review

- [mongoose api](https://mongoosejs.com/docs/api.html#Model)
- [React Router](https://reactrouter.com/en/6.20.1/router-components/browser-router)

## Things to Learn More About
