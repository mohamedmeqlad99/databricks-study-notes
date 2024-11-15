we use apply **apply changes into** avoids writing of duplicate records so we use it instead of **insert into** in some situations

 In PySpark, which of the following commands can you use to query the Delta table **employees** created in Spark SQL?

we can use 
```sql
spark.table("employees")
```
to query a table in pyspark 
***
 what of the following statement describe Auto loader 
`Auto loader monitors a source location, in which files accumulate, to identify and ingest only new arriving files with each command run. While the files that have already been ingested in previous runs are skipped.`
***
 The data engineer team has a DLT pipeline that updates all the tables once and then stops. The compute resources of the pipeline continue running to allow for quick testing.
Which of the following best describes the execution modes of this DLT pipeline ?

**The DLT pipeline executes in Triggered Pipeline mode under Development mode.**

note that --> A **DLT (Delta Live Table) pipeline** is a data pipeline in Databricks that is designed for building and managing data processing workflows in a simpler, scalable, and more reliable manner.

***
Which of the following code blocks can a data engineer use to query the existing streaming table **events** ?
```sql
  
spark.readStream.table("events")
```
 ***
 A data engineer has the following query in a Delta Live Tables pipeline:
```sql
CREATE LIVE TABLE aggregated_sales
AS
SELECT store_id, sum(total)
FROM cleaned_sales
GROUP BY store_id
```
The pipeline is failing to start due to an error in this query
Which of the following changes should be made to this query to successfully start the DLT pipeline ?

```sql
CREATE LIVE TABLE aggregated_sales
AS
SELECT store_id, sum(total)
FROM LIVE.cleaned_sales
GROUP BY store_id
```
 ***
 Which of the following is the benefit of using the Auto Stop feature of Databricks SQL warehouses ?

**Minimizes the total running time of the warehouse**

***
The data engineer team has a DLT pipeline that updates all the tables at defined intervals until manually stopped. The compute resources terminate when the pipeline is stopped.
Which of the following best describes the execution modes of this DLT pipeline ?

**The DLT pipeline executes in Continuous Pipeline mode under Production mode.**

***
A data engineer wants to create a relational object by pulling data from two tables. The relational object must be used by other data engineers in other sessions on the same cluster only. In order to save on storage costs, the date engineer wants to avoid copying and storing physical data.
Which of the following relational objects should the data engineer create?

**Global Temporary view**

***
Which of the following tasks is not supported by Databricks Repos (Git folders), and must be performed in your Git provider ?

 **delete branches**
 ***
 
 which of the following data engineer using to create a new table a long with a comment
```sql
CREATE TABLE payments
COMMENT "This table contains sensitive information"
AS SELECT * FROM bank_transactions
```

***
**Delta lake** -->One of the foundational technologies provided by the Databricks Lakehouse Platform is an open-source, file-based storage format that brings reliability to data lakes.
Which of the following technologies is being described in the above statement?

***
**JSON** --> is the primary format for the transaction log files
***
A junior data engineer uses the built-in Databricks Notebooks versioning for source control. A senior data engineer recommended using Databricks Repos (Git folders) instead.
Which of the following could explain why Databricks Repos is recommended instead of Databricks Notebooks versioning?

**Databricks Repos supports creating and managing branches for development work.**

***
A data engineer has a database named **db_hr**, and they want to know where this database was created in the underlying storage.
Which of the following commands can the data engineer use to complete this task?

**DESCRIBE EXTENDED db_hr**

****
Given the following commands:
```sql
CREATE DATABASE db_hr;
USE db_hr;
CREATE TABLE employees;
```
where the new table ***employees*** will be stored 

**dbfs:/user/hive/warehouse/db_hr.db**
***

Which of the following statements best describes the usage of `CREATE SCHEMA` command ?


**It’s used to create a database**

note that --> in HIVE in data bricks  **schemas** and **databases** are essentially the same concept, with the terms used interchangeably. Both commands create a namespace for tables and other objects within the environment.

SO create data db = create  schema database 
***
Which of the following statements is **Not** true about CTAS statements ?

**CTAS statements support manual schema declaration**


