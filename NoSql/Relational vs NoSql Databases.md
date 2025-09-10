# 🗄️ Relational Databases (RDBMS) Vs NoSQL Databases

A **Relational Database Management System (RDBMS)** is a database that organizes data into **tables** consisting of **rows** and **columns**, and connects them through relationships.  

It is governed by **constraints** and **rules** to ensure:
- **Data Integrity**  
- **Consistency**  
- **Security**
---

## 📌 Key Characteristics

### 📐 Fixed Schema
- Data is stored according to a **predefined schema** (table structure).  
- Each table has **well-defined columns** with specific data types.  
- If new data does not match the existing structure, the **schema must be modified** first.  

💡 **Example**:  
If we want to store a new field like `PhoneNumber` for the `Customers` table, we must run:  

ALTER TABLE Customers ADD PhoneNumber VARCHAR(20);

## 🖥️ Interaction with Relational Databases

Relational Databases are interacted with using **SQL (Structured Query Language)**, which is the standard language to create, read, update, and delete data (CRUD).  

When we connect to a database, interaction happens in two main ways:

### 1. Data Definition
We use SQL commands to **define and manage the structure** of the database.  
- `CREATE TABLE` → make new tables  
- `ALTER TABLE` → modify existing tables  
- `DROP TABLE` → delete tables  

This layer ensures the database has the correct schema before inserting data.

## ⚖️ ACID Properties

Relational Databases (RDBMS) ensure **data reliability** through the **ACID principles**:

- **Atomicity** → Every transaction is **all-or-nothing**.  
- **Consistency** → The database always transitions from one **valid state to another**.  
- **Isolation** → Transactions run **independently**, without interfering with each other.  
- **Durability** → Once **committed**, data is permanently saved, even if the system crashes.  

--
ve data that does not fit well into the rigid, tabular structure of relational databases.  
They are schema-less or schema-flexible, which makes them ideal for handling **unstructured, semi-structured, and rapidly changing data**.

---

## 📌 Key Characteristics
- **Flexible Schema** → No fixed schema, new fields can be added without altering existing data.  
- **Horizontal Scalability** → Scales out across multiple servers (distributed systems).  
- **High Performance** → Optimized for large volumes of data and high-velocity reads/writes.  
- **BASE Properties** (instead of ACID):  
  - **Basically Available**  
  - **Soft state** (data may change over time, even without input)  
  - **Eventual consistency** (data becomes consistent across nodes eventually, not instantly)  

---

## 🗂️ Types of NoSQL Databases
1. **Document Stores**  
   - Store data as JSON-like documents.  
   - Example: MongoDB, CouchDB  
   - 📌 Use case: User profiles, content management systems.  

2. **Key-Value Stores**  
   - Data stored as key-value pairs.  
   - Example: Redis, DynamoDB  
   - 📌 Use case: Caching, session management.  

3. **Column-Oriented Stores**  
   - Store data in columns instead of rows.  
   - Example: Apache Cassandra, HBase  
   - 📌 Use case: Time-series data, big data analytics.  

4. **Graph Databases**  
   - Store nodes and edges to represent relationships.  
   - Example: Neo4j, Amazon Neptune  
   - 📌 Use case: Social networks, recommendation systems.  

---
## 🗣️ Query Languages in NoSQL

Unlike RDBMS, where we use **SQL** (a standard language across all relational systems),  
there is **no universal query language** for NoSQL databases.  
Each system has its **own way of interacting** with data:

- **MongoDB** → Uses **MongoDB Query Language (MQL)**, based on JSON-like syntax.  
- **Cassandra** → Uses **CQL (Cassandra Query Language)**, similar to SQL but limited.  
- **Neo4j** → Uses **Cypher Query Language** for graph traversals.  
- **Redis** → Uses command-based operations (`SET key value`, `GET key`).  
- **CouchDB** → Uses **MapReduce** functions written in JavaScript. 


---
## ⚖️ RDBMS vs NoSQL (Quick Comparison)

| Feature            | RDBMS (Relational)                | NoSQL (Not Only SQL)                   |
|--------------------|-----------------------------------|----------------------------------------|
| **Schema**         | Fixed schema (tables, columns)    | Flexible or schema-less                |
| **Transactions**   | Strong ACID guarantees            | BASE (eventual consistency)            |
| **Scalability**    | Vertical (scale up)               | Horizontal (scale out)                 |
| **Best For**       | Structured data, OLTP workloads   | Unstructured data, Big Data, OLAP      |
| **Examples**       | MySQL, PostgreSQL, Oracle, SQLSrv | MongoDB, Cassandra, Redis, Neo4j       |

---

## 🚀 When to Use NoSQL?
- When data is **unstructured or semi-structured**.  
- When applications require **real-time performance**.  
- When dealing with **massive scale (big data)**.  
- When relationships are complex (use graph DBs).  
- When schema changes frequently.  

---

## 🔑 Summary
- **RDBMS** → Best for structured, consistent, transactional workloads.  
- **NoSQL** → Best for flexibility, scalability, and handling diverse or unstructured data.  
- Modern systems often use a **polyglot approach** (both RDBMS + NoSQL) depending on requirements.  









