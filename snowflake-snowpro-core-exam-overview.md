# [SNOWPRO CORE CERTIFICATION](https://www.snowflake.com/certifications/)

![snopro](images/snopro.png)

- The SnowPro Core Certification demonstrates an individual’s knowledge to apply core expertise implementing and migrating to Snowflake.

## Steps to Success

1. [ ] [Review Exam Guide](https://learn.snowflake.com/courses/course-v1:snowflake+CERT-SPC-GUIDE+B/about?_ga=2.22288187.1493617847.1661798572-1202842695.1661265529)
2. [x] [Download Study Guide](https://learn.snowflake.com/courses/course-v1:snowflake+SPSG-CORE+B/about?_ga=2.35208737.1493617847.1661798572-1202842695.1661265529)
3. [ ] [CHeck out the paid on-demand prep course](https://training.snowflake.com/?_ga=2.35208737.1493617847.1661798572-1202842695.1661265529)
4. [ ] [Review exam registration instructions](https://learn.snowflake.com/courses/course-v1:snowflake+CERT-SPC-GUIDE+B/about?_ga=2.35208737.1493617847.1661798572-1202842695.1661265529)
5. [ ] [Register](https://home.pearsonvue.com/snowflake)

---

## Core Certification Candidate (New version of exam September 2022)

- Data Loading and Transformation in Snowflake
- Virtual Warehouse Performance and Concurrency
- DDL and DML Queries
- Using Semi-Structured and Unstructured Data
- Cloning and Time Travel
- Data Sharing
- Snowflake Account Structure and Management

## Exam Format

- Exam Version: COF-C02
- Total Number of Questions: 100
- Question Types: Multiple Select, Multiple Choice
- Time Limit: 115 minutes
- Languages: English
- Registration Fee: $175 USD
- Passing Score: 750 + Scaled Scoring from 0 - 1000
- Unscored Content: Exams may include unscored items to gather statistical information. These items are not identified on the form and do not affect - your score, and additional time is factored in to account for this content.
- No Prerequisites
- Delivery Options:
  - Online Proctoring
  - Onsite Testing Centers

## Exam Domain Breakdown

| Domain                                                  | Estimated Percentage Range |
| :------------------------------------------------------ | :------------------------: |
| Snowflake cloud data platform features and architecture |           20-25%           |
| Account access and security                             |           20-25%           |
| Performance concepts                                    |           10-15%           |
| Data loading and unloading                              |           5-10%            |
| Data transformations                                    |           20-25%           |
| Data protection and data sharing                        |           5-10%            |

### Domain 1.0: Snowflake Data Platform Features and Architecture

- 1.1 Outline key features of the Snowflake Cloud Data Platform.
  - Elastic Storage
  - Elastic Compute
  - Snowflake’s three distinct layers
  - Data Cloud/ Data Exchange/ Partner Network
  - Cloud partner categories
- 1.2 Outline key Snowflake tools and user interfaces.
  - Snowflake User Interfaces (UI)
  - Snowsight
  - Snowflake connectors
  - Snowflake drivers
  - SQL scripting
  - Snowpark
- 1.3 Outline Snowflake’s catalog and objects.
  - Databases
  - Schemas
  - Tables Types
  - View Types
  - Data types
  - User-Defined Functions (UDFs) and User Defined Table Functions (UDTFs)
  - Stored Procedures
  - Streams
  - Tasks
  - Pipes
  - Shares
- 1.4 Outline Snowflake storage concepts.
  - Micro partitions
  - Types of column metadata clustering
  - Data Storage Monitoring
  - Search Optimization Service

### Domain 2.0: Account Access and Security

- 2.1 Outline compute principles.
  - Network security and policies
  - Multi-Factor Authentication (MFA)
  - Federated authentication
  - Single Sign-On (SSO)
- 2.2 Define the entities and roles that are used in Snowflake.
  - Outline how privileges can be granted and revoked
  - Explain role hierarchy and privilege inheritance
- 2.3 Outline data governance capabilities in Snowflake.
  - Accounts
  - Organizations
  - Databases
  - Secure views
  - Information schemas
  - Access history and read support

### Domain 3.0: Performance Concepts

- 3.1 Explain the use of the Query Profile.
  - Explain plans
  - Data spilling
  - Use of the data cache
  - Micro-partition pruning
  - Query history
- 3.2. Explain virtual warehouse configurations.
  - Multi-clustering
  - Warehouse sizing
  - Warehouse settings and access
- 3.3 Outline virtual warehouse performance tools.
  - Monitoring warehouse loads
  - Query performance
  - Scaling up compared to scaling out
  - Resource monitors
- 3.4 Optimize query performance.
  - Describe the use of materialized views
  - Use of specific `SELECT` commands

### Domain 4.0: Data Loading and Unloading

- 4.1 Define concepts and best practices that should be considered when loading data.
  - Stages and stage types
  - File size
  - File formats
  - Folder structures
  - Adhoc/bulk loading using the Snowflake UI
- 4.2 Outline different commands used to load data and when they should be used.
  - `CREATE PIPE`
  - `COPY INTO`
  - `GET`
  - `INSERT/INSERT OVERWRITE`
  - `PUT`
  - `STREAM`
  - `TASK`
  - `VALIDATE`
- 4.3 Define concepts and best practices that should be considered when unloading data.
  - File formats
  - Empty strings and `NULL` values
  - Unloading to a single file
  - Unloading relational tables
- 4.4 Outline the different commands used to unload data and when they should be used.
  - `LIST`
  - `COPY INTO`
  - `CREATE FILE FORMAT`
  - `CREATE FILE FORMAT … CLONE`
  - `ALTER FILE FORMAT`
  - `DROP FILE FORMAT`
  - `DESCRIBE FILE FORMAT`
  - `SHOW FILE FORMAT`

### Domain 5.0: Data Transformation

- 5.1 Explain how to work with standard data.
  - Estimating functions
  - Sampling
  - Supported function types
  - User-Defined Functions (UDFs) and stored procedures
- 5.2 Explain how to work with semi-structured data.
  - Supported file formats, data types, and sizes
  - VARIANT column
  - Flattening the nested structure
- 5.3 Explain how to work with unstructured data.
  - Directory tables
  - SQL file functions
  - Rest API
  - Create User-Defined Functions (UDFs) for data analysis

### Domain 6.0: Data Protection and Data Sharing

- 6.1 Outline Continuous Data Protection with Snowflake.
  - Time Travel
  - Fail-safe
  - Data Encryption
  - Cloning
  - Replication
- 6.2 Outline Snowflake data sharing capabilities.
  - Account types
  - Data Marketplace and Data Exchange
  - Private data exchange
  - Access control options
  - Shares

---

## Recommended Training

As preparation for this exam, we recommend a combination of hands-on experience, instructor-led training, on demand training courses and the utilization of self-study assets.

- [ ] Instructor-Led Course recommended for this exam: 
  - [Snowflake Fundamentals](https://training.snowflake.com/lmt/clmsCourse.prCourseDetails?site=sf&in_userid=-34570704459&in_language_identifier=en-us&in_region=us&in_rcoId=96497380&in_from_module=XLR8LOGIN.LOGIN)
- [ ] Paid Self Study recommended for this exam:
  - [SnowPro Core Certification Preparation Course](https://training.snowflake.com/)
- [ ] Free Self Study recommended for this exam:
  - [Pro Core Study Guide](https://learn.snowflake.com/courses/course-v1:snowflake+SPSG-CORE+A/about?_ga=2.129876622.384067162.1638810354-1102816095.1633962341&_gac=1.94989934.1636477023.CjwKCAiA1aiMBhAUEiwACw25MQQ63tax_d-N-8PQHNss-TzoRqgklwxqDR6S9uiW_Axs6c4O9-aARxoCVxYQAvD_BwE)
  - [Snowflake Hands on Essentials & Level Up Series](https://learn.snowflake.com/tracks)
  - [Snowflake in 20 Minutes](https://docs.snowflake.com/en/user-guide/getting-started-tutorial.html)

