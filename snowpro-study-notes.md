# SnoPro Study Notes

Supported File Locations
*	Loading: Local Files, S3, Azure, Google Cloud Storage
*	Unloading: Local Files (with GET), S3, Azure, Google Cloud Storage
Supported File Locations Command
*	Loading: COPY INTO <table>
*	Unloading: COPY INTO <location>
Supported File Formats
*	Loading: Delimited, CSV, TSV, JSON, AVRO, ORC, Parquet, XML
*	Unloading: Delimited, CSV, TSV, JSON, Parquet
Supported File Encoding
*	Loading: 
o	Delimited = UTF-8 default, but can explicitly specify otherwise
o	JSON, Avro, Parquet, ORC, XML: UTF-8
*	Unloading: UTF-8
Uploading/Downloading files (uploading to Snowflake, Downloading to Local Machine)
*	Uploading: PUT
*	Downloading: GET
*	Unload from Snowflake table to External Stage : COPY INTO
Compression
*	Loading:
o	Uncompressed: gzip unless compression is explicitly disabled
o	Compressed:
?	Auto: gzip, bzip2, deflate, raw deflate
?	Manual: brotli, Zstandard
*	Unloading:
o	Gzip(default), bzip2, brotli, Zstandard
Encryption of Staged Files
*	Loading:
o	Unencrypted Files: 128-bit (256-bit requires extra configuration)
o	Encrypted Files: User-supplied key
*	Unloading:
o	Internal Location: 128-bit (256-bit requires extra configuration)
o	External Location: User-supplied key
Unloading Single File Size
*	Default: 16 MB
*	Max: 5 GB (For S3, Azure, Google Cloud Storage)
Unloading to only Single Output File:
*	SINGLE=True
Best File Size for Loading: ****Very important****
*	100-250 MB Compressed
Parquet Best Size for Loading
*	1 GB
Best File Size for Loading Using UI
*	50 MB or smaller
Snowpipe File Size: ****Very important****
*	100-250 MB Compressed
Semi-Structured Data Size Limitation
*	VARIANT Data Type: Max 16 MB compressed per row
Unloading Relational Table to JSON
*	OBJECT_CONSTRUCT
Bulk Loading Compute vs. Snowpipe Compute
*	Bulk Loading: User Provisioned
*	Snowpipe: Snowflake Provisioned
Load Metadata
*	Name of Files
*	File Size
*	Etag
*	Number of rows parsed
*	Timestamp of the last load for the file
*	Information about errors that occurred while loading
Load Metadata Expiration
*	64 days
Load History Expiration
*	14 days
Loading Files with Expired Metadata
*	LOAD_UNCERTAIN_FILES
JSON Null Values
*	“Null” string
Strip Null Values JSON
*	Makes JSON Nulls SQL Nulls
Deleting Files From Stages:
*	PURGE: While loading
*	REMOVE: After loading
Snowpipe Costs
*	0.06 credits per 1000 files queued
Max Tasks in Tree
*	1000
Max Child Tasks
*	100
How long does it take to make a pipe stale?
*	14 days
What statement does Snowpipe use?
*	COPY
What ecosystem supports cross-cloud support for Snowpipe?
*	AWS
Load History
*	Bulk: 64 days
*	Snowpipe: 14 days
Stages that support transforming while loading:
*	User, Named Internal, Named External
Stages that don’t support transforming while loading:
*	Table
Data Transformations During Load:
*	COPY COMMAND: Column Reordering, Column Omission, Truncation, Casts
o	Subsets: Cast, Concat, 
Default for Unloading Files:
*	SINGLE = FALSE
Stage References:
*	@~user
*	@%table
*	@internal named
Stages that don’t Support File Format
*	User, Table
S3 File Access Privileges
*	Get Object
*	Get ObjectVersion
*	ListBucket
Tables that can be Replicated
*	Permanent, Transient
*	Also, auto clustering of clustered tables, table constraints 
Things that can be Replicated
*	Permanent and Transient Tables
*	Materialized and Standard Views
*	File Formats
*	UDF’s, Stored Procs, Policies
Database Objects that cannot be Replicated
*	Temporary Tables
*	External Tables
*	Pipes
*	Stages
*	Streams
*	Tasks
Object Parameter that is Replicated
*	DATA_RETENTION_TIME_IN_DAYS
Causes of Replication Failure
*	Primary DB is Enterprise or Higher and at least one replication account is a lower edition
*	Primary DB has business association agreement and at least one replication account doesn’t
*	Policy in Primary DB is referring to a policy in another DB
*	Primary DB has an external table
Can DB’s from Shares be Replicated?
*	NO
Database Replication Billing
*	Data Transfer
*	Compute Resources
Is Reclustering Performed on Replicated Tables?
*	No
What do Refresh Operations do on Materialized View in a Replication?
*	Replicate view definitions and NOT data
Objects that can be Shared
*	Tables
*	External Tables
*	Secure Views
*	Secure Materialized Views, Secure UDFs
Secure Data Sharing Not Supported
*	VPS
What state are tasks in by default?
*	Suspended
Stream Metadata Columns
*	METADATA$ACTION
*	METADATA$ROW_ID
*	METADATA$ISUPDATE
Types of Streams
*	Insert-Only
*	Append-Only
*	Standard
Column Level Security (Enterprise and Above Only)
*	External Tokenization
*	Dynamic Data Masking
COPY transformations
*	Loading: Truncation, Column Reordering, Column Omission, Casts
*	Unloading: all of loading AND join!
Snowflake Authentication
*	MFA, OAuth, SSO
COPY INTO Statement Objects
*	File Format, Stage, Table
Cloud Services Layer
*	User Authentication
*	Metadata Storage
*	Data Security
*	Metadata Management
*	Infrastructure Management
*	Query parsing and optimization
Unique Snowflake Object
*	Pipe, Stage
Role that has Notifications
*	ACCOUNTADMIN
Recommended Column Number for Cluster Keys
*	3-4
Types of Caches
*	Results, Metadata, Warehouse
Amount of Data Micropartitions Hold
*	50-500 MB Uncompressed
Micropartition Metadata
*	Number of Distinct Values
*	Range of Values in Columns
*	Optimization/Query Processing info
Clustering Info Maintained
*	Total Number of Micropartitions
*	Depth of overlapping micropartitions
*	Number of Overlapping Micropartitions
MFA can be used With
*	ODBC, JDBC, SnowSQL, WebUI, Python
Transactions are NEVER
*	Nested
How Many Sessions Support a Transaction
*	Single
Types of Field Enclosures
*	Single Quote, Double Quote, None
Comment Notation
*	// and - -
What does each Trial Account Start With
*	Two Databases
*	Two Inbound Shares
Offset is Measured in
*	Seconds
Clone Table Privileges
*	Select
Number of Resource Monitors Per Warehouse
*	One
Stages Where Encryption is Optional
*	External
UNDROP Command Criteria
*	CREATE Privileges on Schema
*	Ownership on Table
*	Must be restored to same schema
Resource Monitor Actions
*	NOTIFY
*	NOTIFY & SUSPEND
*	NOTIFY & SUSPEND IMMEDIATELY
Resource Level Monitoring Account vs. Warehouse Property
*	MONITOR LEVEL
Resource Monitor Notification Options
*	Web UI
*	Email
Multi-Cluster Warehouses are Designed to Handle
*	Queuing issues
*	Many Concurrent Queries
*	Many Concurrent Users
Role that Receives Resource Monitor Notifications
*	ACCOUNTADMIN
Periodic Rekeying Edition
*	Enterprise and Above
Hierarchical Key Model Keys
*	Root, Account Master, File, Table Master
Max Query Partition =
*	Warehouse credit amount
Is Blocked or Allowed IP Addresses Applied First?
*	Blocked
Does Snowflake Support Schema-Less Storage?
*	Yes
Types of Transient Objects
*	Tables, Databases, and Schemas
Object Security
*	RBAC and DAC
Snowpipe REST API Endpoints
*	insertFiles
*	insertReport
*	loadHistoryScan
VARCHAR Size is limited to 
*	16 MB 
BOOLEAN = true requires what type of value
*	Non-zero
Cloning a Database Clones
*	DB, Schemas, Tables, and all cloneable schema objects
o	This includes file formats, streams, tasks, udfs, pipes, stored procs, sequences
Non-Cloneable Objects,
*	External Tables
*	Internal Named Stages
*	Pipes that reference Internal Named Stages
Roles that can Access Account
*	SECURITYADMIN, ACCOUNTADMIN
Clustering Depth
The clustering depth for a table is not an absolute or precise measure of whether the table is well-clustered. 
Ultimately, query performance is the best indicator of how well-clustered a table is:
*	If queries on a table are performing as needed or expected, the table is likely well-clustered.
*	If query performance degrades over time, the table is likely no longer well-clustered and may benefit from 
clustering.
