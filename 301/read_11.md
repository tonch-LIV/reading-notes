# 301_Read_11 - MongoDB and Mongoose

This is important because...  

## [NoSQL vs SQL](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

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
      - no tables; flexible structures such as documents, ley:value pairs, graphs, etc. are used to store data.
  7. What is inside of a MongoDB database?  
      - collections containing documents.
  8. Which is more flexible - SQL or MongoDB? and why?  
      - MongoDB; uses flexibla schema that allows documents to contain different fields and structures w/o having to re-design the database.
  9. What is the disadvantage of a NoSQL database?  
      - lack of strict or 'rigid' structure can lead to inconsistent data; relationships between data can become difficult to manage.

## Bookmark and Review

- [mongoose api](https://mongoosejs.com/docs/api.html#Model)
- [React Router](https://reactrouter.com/en/6.20.1/router-components/browser-router)

## Things to Learn More About
