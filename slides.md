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

## Data Mart vs Data Lake

---



---
class: center, middle

Code
https://github.com/algogrit/presentation-dealing-with-data

Slides
https://dealing-with-data.slides.algogrit.com
