**1. What is ETL?**
ETL stands for extract, transform, and load.
- Extract the data from its original source, whethere that is another database or an application
- Transform data by cleaning it up, deduplicating it, combining it, and otherwise getting ready to...
- Load the data into the target database

The benefits of ETL (CCPA)
- Context: ETL helps businesses gain deep historical context with data
- Consolidation: it provides a consolidated view of data, for easier analysis and reporting
- Productivity: it improves productivity with repeatable processes that don't require heavy hand-coding
- Accuracy: it improves data accuracy and audit capabilities that most businesses require for compliance with regulations and standards.
[Additional Sources](https://www.matillion.com/what-is-etl-the-ultimate-guide/)

**2. What is data normalization and why it is important?**
It is a process of analyzing the given relation schemas based on their functional dependencies and primary keys to achieve the following desirable properties:
- Minimizing Redundancy
- Mnimimizing the Insertion, Deletion, and Update Anomalies
Relation schemas that do not meet the properties are decomposed into smaller relation schemas that could meet desirable properties

**3. What is Data Schemas**
A database schema is a blueprint or architecture of how our data will look. It doesn't hold data itselt, but instead describes the shape of the data an dhow it might relate to other tables or models.

A data base schema will include:
- All important or relevant data
- Consistent formatting for all data entries
- Unique keys for all entries and database objects
- Each column in a table has a name and data type

There are two main database schema types that define different parts of the schema: logical and physical. 
A logical database schema represents how the data is organized in terms of tables. It also explains how attributes from tables are linked together. 
Different schemas use a different syntax to define the logical architecture and constraints. To create a logical database schema, we use tools to illustrate relationships between components of your data.
This is called entity-relationship modeling (ER Modeling). It specifies what the relationships between entity types are.
The physical database schema represents how data is stored on disk storage.
In oter words, it is the actual code that will be used to create the structure of your database.
[Additional Sources](https://www.educative.io/blog/what-are-database-schemas-examples)

**4. What is Data Cleansing**
Data cleaning is the process of preparing data for analysis by removign or modifying data that is incorrect, incomplete, irrelevant, duplicated, or improperly formatted.

**5. How do You Evaluate Data Profile**
Data profiling is the process of reviewing source data, understanding structure, content and interrelationships, and identifying potential for data projects.
Data profiling can uncover data quality issues.

Data profiling and data quality analysis best practices <br>
Basic: <br>
- Distinct count and percent: identifies natural keys, distinct values in each column that can help process inserts and updates. Handy for tables without headers.
- Percent of zero/blank/null values: identifies missing or unknown data, Helps ETL architects setup appropriate default values
- Minimum / maximum / average string length: helps select appropriate data types and sizes in target database. Enables setting column widths just wide enough for the data, to improve performance.
Advanced: <br>
- Key integrity: ensures keys are always present in the data, using zero/blank/null analysis. Also, helps identify orphan keys, which are problematic for ETL and future analysis.
- Cardinality: checks relationships like one-to-one, one-to-many, many-to-many, between related data sets. This helps BI tools perform inner or outer joins correctly.
- Pattrn and frequency distributions: checks for data fields are formatted correctly.
[Additional Source](https://panoply.io/analytics-stack-guide/data-profiling-best-practices/)

**2. RANK VS DENSE_RANK**
`RANK()` gives you the ranking within your ordered partition. Ties are assigned the same rank, with the next ranking(s) skipped. So, if you have 3 items at rank 2, the next rank listed would be ranked 5.

`DENSE_RANK()` again gives you the ranking within your ordered partition, but the ranks are consecutive. No ranks are skipped if there are ranks with multiple items.