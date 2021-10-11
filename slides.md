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

Strength: traversing through nodes by following relationships

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

Code
https://github.com/algogrit/presentation-dealing-with-data

Slides
https://dealing-with-data.slides.algogrit.com
