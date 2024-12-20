layout: true

.signature[@algogrit]

---

class: center, middle

# Dealing with Data

Gaurav Agarwal

---
class: center, middle

Data is simple. Extracting knowledge from it is complicated.

---

class: center, middle

![Me](assets/images/me.png)

Software Engineer & Product Developer

Director of Engineering & Founder @ https://codermana.com

ex-Tarka Labs, ex-BrowserStack, ex-ThoughtWorks

---

class: center, middle

*What we wanted*

![In-class Training](assets/images/professional-training-courses.jpg)

---

class: center, middle

*What we got*

![WFH](assets/images/wfh.jpg)

---

## As a instructor

- I promise to

  - make this class as interactive as possible

  - use as many resources as available to keep you engaged

  - ensure everyone's questions are addressed

---

## What I need from you

- Be vocal

  - Let me know if there any audio/video issues ASAP

  - Feel free to interrupt me and ask me questions

- Be punctual

- Give feedback

- Work on the exercises

- Be *on mute* unless you are speaking

---
class: center, middle

## Class progression

![Learning Curve](assets/images/learning-curve.jpg)

---
class: center, middle

Here you are trying to *learn* something, while here your *brain* is doing you a favor by making sure the learning doesn't stick!

---

### Some tips

- Slow down => stop & think
  - listen for the questions and answer

- Do the exercises
  - not add-ons; not optional

- There are no dumb questions!

- Drink water. Lots of it!

---

### Some tips (continued)

- Take notes
  - Try: *Repetitive Spaced Out Learning*

- Talk about it out loud

- Listen to your brain

- *Experiment!*

---
class: center, middle

### 📚 Content ` > ` 🕒 Time

---
class: center, middle

## Show of hands

*Yay's - in Chat*

---
class: center, middle

## Poll: What databases have you worked with?

---
class: center, middle

## Classification of Databases

---
class: center, middle

Broadly classified as: Relational, Columnar, KV, Graph, Time-series, etc.

---
class: center, middle

### Relational Databases

---
class: center, middle

since 1970s

---

- multiple, related tables

- stored in rows and columns

---
class: center, middle

![Relational](assets/images/relational.png)

---
class: center, middle

#### RDBMS (Relational database management systems)

---

- set-theory based systems

- interacting with queries: SQL (Structured Query Language)

- Data values are typed, have schema

- tables can join

---
class: center, middle

Relational Examples: `Microsoft SQL Server`, `Oracle Database`, `MySQL`, `PostgreSQL`, `IBM DB2`, [`Cloud SQL`](https://cloud.google.com/sql), [`Spanner`](https://cloud.google.com/spanner), etc.

---
class: center, middle

*ACID*!

---
class: center, middle

#### Performance & optimization of RDBMS?

---

- Retrieve

- Insert

- Schema change

- Delete

---
class: center, middle

What about sparse data?

---
class: center, middle

### Columnar Databases

---
class: center, middle

aka `column data stores`

---
class: center, middle

data from a given column stored together

---
class: center, middle

Let's visualize...

---
class: center, middle

Columnar Examples: [`Google BigQuery`](https://cloud.google.com/bigquery/), `Cassandra`, `HBase`, `MariaDB`, `Azure SQL Data Warehouse`, `MonetDB`

---
class: center, middle

#### Performance & optimization of Columnar Databases?

---

- Retrieve

- Insert

- Schema change

- Delete

---
class: center, middle

When you’re querying a columnar database, it essentially ignores all of the data that doesn’t apply to the query.

---
class: center, middle

## Wide column databases

---
class: center, middle

aka `column-family stores`

---
class: center, middle

A Columnar data store will store each column separately on disk

---
class: center, middle

A Wide-column database is a type of columnar database that supports a column family stored together on disk, not just a single column.

---

Ideal use cases:

- Log data

- IoT (Internet of Things) sensor data

- Time-series data, such as temperature monitoring or financial trading data

- Attribute-based data, such as user preferences or equipment features

- Real-time analytics

---
class: center, middle

Wide-column store examples: `Apache Cassandra`, `Scylla`, `Apache HBase`, [`Google BigTable`](https://cloud.google.com/bigtable), `Microsoft Azure Cosmos DB`

---
class: center, middle

### Document Databases

---
class: center, middle

store *documents*

---
class: center, middle

Typically *schemaless*

---

- has a unique ID field

- can store nested strucutres

- can be indexed, replicated

---
class: center, middle

Document Database examples: `MongoDB`, `Amazon DocumentDB`, `Apache CouchDB`, [`Cloud Firestore`](https://firebase.google.com/docs/firestore)

---
class: center, middle

Document databases are simple and scalable, making them useful for mobile apps that need fast iterations.

---
class: center, middle

### Key-Value Stores

---
class: center, middle

simplest type of NoSQL databases

---
class: center, middle

save data as a group of key-value pairs

---
class: center, middle

Some KV implementations permit complex value types: hashes, list, etc.

---
class: center, middle

KV Examples: `Amazon DynamoDB`, `Redis`, `Riak`, [`Cloud Datastore`](https://cloud.google.com/datastore)

---
class: center, middle

Key-value databases are highly scalable and can handle high volumes of traffic, making them ideal for processes such as session management for web applications, user sessions for massive multi-player online games, and online shopping carts.

---
class: center, middle

### Graph Databases

---
class: center, middle

based on *graph theory*

---
class: center, middle

graph databases excel at dealing with highly interconnected data

---
class: center, middle

A graph database consists of nodes and relationships between nodes.

---
class: center, middle

![Graph](assets/images/person-cinema.png)

---
class: center, middle

Both nodes and relationships can have properties -- typically key-value pairs -- to store data.

---
class: center, middle

*Strength*: traversing through nodes by following relationships

---
class: center, middle

Graph database examples: `Datastax Enterprise Graph`, `Neo4J`, `Dgraph`, `ArangoDB`, `Amazon Neptune`

---
class: center, middle

### Time-series database

---
class: center, middle

A time series database is a database optimized for time-stamped, or time series, data.

---
class: center, middle

Time-series db examples: `Druid`, `eXtremeDB`, `InfluxDB`

---
class: center, middle

## OLTP vs OLAP

---
class: center, middle

### OLTP: Online Transaction Processing

---
class: center, middle

An OLTP system captures and maintains transaction data in a database.

---
class: center, middle

Each transaction involves individual database records made up of multiple fields or columns.

---

OLTP systems:

- Handles a large number of small transactions

- Simple standardized queries

- Based on `INSERT`, `UPDATE`, `DELETE` commands

- Response Time in Milliseconds

- Industry-specific, such as retail, manufacturing, or banking

- Regular backups required to ensure business continuity and meet legal and governance requirements

- Normalized databases for efficiency

---
class: center, middle

## OLAP: Online Analytics Processing

---
class: center, middle

OLAP applies complex queries to large amounts of historical data, aggregated from OLTP databases and other sources, for data mining, analytics, and business intelligence projects.

---
class: center, middle

In OLAP, the emphasis is on response time to these complex queries.

---

OLAP systems:

- Handles large volumes of data with complex queries

- Complex queries

- Based on SELECT commands to aggregate data for reporting

- Seconds, minutes, or hours depending on the amount of data to process

- Subject-specific, such as sales, inventory, or marketing

---

OLAP systems (continued):

- Purpose is to plan, solve problems, support decisions, discover hidden insights

- Data periodically refreshed with scheduled, long-running batch jobs

- Generally large due to aggregating large datasets

- Denormalized databases for analysis (Flat tables!)

---
class: center, middle

The data from one or more OLTP databases is ingested into OLAP systems through a process called extract, transform, load (ETL).

---
class: center, middle

## Data Warehouse

---
class: center, middle

A data warehouse is a type of data management system that is designed to enable and support business intelligence (BI) activities, especially analytics.

---
class: center, middle

Data warehouses are solely intended to perform queries and analysis and often contain large amounts of historical data.

---

- centralizes and consolidates large amounts of data from multiple sources

- analytical capabilities allow organizations to derive valuable business insights to improve decision-making

---
class: center, middle

## Data Lake vs Data Mart

---
class: center, middle

A data lake is the place where you dump all forms of data generated in various parts of your business.

.content-credits[https://cloud.google.com/learn/what-is-a-data-lake]

---
class: center, middle

Use Cloud Storage as Data Lake

.content-credits[https://cloud.google.com/architecture/build-a-data-lake-on-gcp]

---
class: center, middle

A data warehouse usually only stores data that's already modeled/structured.

.content-credits[https://cloud.google.com/architecture/bigquery-data-warehouse]

---
class: center, middle

A data-mart is a subsection of the data-warehouse, designed and built specifically for a particular department/business function.

---

3 Types of Data Mart:

- Dependent Data Marts - A dependent data mart is constructed from an existing data warehouse. It has a top-down approach that begins with storing all your business data in one centralized location, then withdraws a defined portion of the data when needed for analysis.

- Independent Data Marts - An independent data mart is a stand-alone system, which is created without the use of a data warehouse and focuses on one business function. The data is released from internal or external data sources, refined, then loaded to the data mart, where it is saved until needed or business analysis.

- Hybrid Data Marts - A hybrid data mart integrates data from a current data warehouse and additional operational source systems. It combines speed and end-user focus of a top-down approach with the assistance of the enterprise-level integration of the bottom up method.

---
class: center, middle

## Batch vs Stream processing

---
class: center, middle

### Batch Processing

---
class: center, middle

Batch processing refers to processing of high volume of data in batch within a specific time span.

---

- It processes large volume of data all at once.

- Batch processing is used when data size is known and finite.

- It takes little longer time to processes data.

- It requires dedicated staffs to handle issues.

- Batch processor processes processes data in multiple passes.

- When data is collected overtime and similar data batched/grouped together then in that case batch processing is used.

---

- Data is collected over time

- Once data is collected, it’s sent for processing

- Batch processing is lengthy and is meant for large quantities of information that aren’t time-sensitive

---
class: center, middle

### Stream Processing

---
class: center, middle

Under the streaming model, data is fed into analytics tools piece-by-piece.

---
class: center, middle

The processing is usually done in real time.

---

- Data streams continuously

- Data is processed piece-by-piece

- Stream processing is fast and is meant for information that’s needed immediately

---
class: center, middle

![Stream processing](assets/images/stream-processing.png)

---
class: center, middle

Stream processing has become a must-have for modern applications.

---
class: center, middle

#### Window processing

---
class: center, middle

Windowing functions divide unbounded collections into logical components, or windows.

---
class: center, middle

![Window streaming](assets/images/window-processing.png)

---
class: center, middle

Stream processing examples: `Apache Spark`, `Apache Storm`

---

### Batch vs Stream Processing

- Ingestion
  - Delivery of Data

- Processing (Eg: DataFlow (Apache Beam -> Spark, DataFlow), DataProc, CloudFunction, BigQuery, compute engine)
  - Analytics of Data

- Storage (Eg: CloudSQL, Cloud Storage, Spanner, BigTable, BigQuery, Raw-Disk/Object based Storage - like GCS)

---
class: center, middle

Stream processing can be windowed too: *Fixed*, *Sliding*

---
class: center, middle

## `CAP` vs `BASE` vs `PACLEC`

.content-credits[https://medium.com/@ali.gelenler/distributed-system-trade-offs-cap-vs-base-vs-pacelc-1a3bcac04a7b]

---
class: center, middle

### CAP theorem

defines the limitations and trade-offs in a distributed system

![CAP Theorem](assets/images/cap-theorem.png)

---

It suggests that distributed computer systems can only deliver two out of the following three guarantees:

**Consistency**: Every node sees the same data even when concurrent updates occur

**Availability**: All requests receive responses on whether it was a success or a failure

**Partition tolerance**: The system will keep operating even if there is a network partition in communication between different nodes

---
class: center, middle

In the case of a network partition, the CAP theorem forces a trade-off between *Consistency* and *Availability*.

---

A system must either:

- Maintain consistency, but sacrifice availability (not all requests are responded to).

- Maintain availability, but sacrifice consistency (some responses may be outdated).

---
class: center, middle

### BASE

is an acronym that represents an alternative to strict `ACID` properties

![BASE Model](assets/images/base-model.png)

---
class: center, middle

ACID properties

(**A**tomicity, **C**onsistency, **I**solation, **D**urability)

---

class: center, middle

It focuses on availability and performance over strong consistency.

---

- Basically Available (BA): The system is guaranteed to be available, but not necessarily consistent.

- Soft State (S): The state of the system may change over time, even without input (because of eventual consistency).

- Eventual Consistency (E): The system will become consistent eventually, once all updates have propagated.

---
class: center, middle

BASE is a practical strategy to design systems that are highly available and partition tolerant, at the cost of immediate consistency.

---
class: center, middle

It is often used in distributed, NoSQL systems, which prioritize scalability and availability.

---
class: center, middle

### PACLEC

is an Extension to the CAP theorem

![PACLEC](assets/images/paclec.png)

---
class: center, middle

It acknowledges that network partitions are not the only factor affecting system performance and behavior.

---
class: center, middle

It also considers the trade-offs between latency and consistency during normal operations, which the CAP theorem does not address.

---

- *PAC*: If there is a Partition, you must choose between Availability and Consistency (this is the CAP theorem)

- *ELC*: Else, when the system is running normally (no partition), you must choose between Latency and Consistency

---

In other words:

- If there’s a partition, the system must decide between availability and consistency.

- If there’s no partition, the system must decide between minimizing latency (faster responses) and ensuring strong consistency.

---
class: center, middle

Code
https://github.com/algogrit/presentation-dealing-with-data

Slides
https://dealing-with-data.slides.algogrit.com
