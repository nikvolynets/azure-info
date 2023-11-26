# azure-info

### Cloud info

#### Cloud Service Models:
* Infrustrusture as a Service (IaaS) - user doesn't conrol hardware but has full control over operation systems, storage and applications (AWS, Azure, GCP, Virtual Machines)
* Platfrom as a Service (PaaS) - doesn't manage hardware, operation systems and storage but has control over application and configuration environment (ADF, Synapse, Azure Databricks)
* Software as a Service (SaaS) - control only of limited specific application configurations (Snowflake, Salesforce)

#### Big Data - 3 V's 
* Volume - huge data size
* Velocity - high speed of data flow, change and processing
* Variety - various data sources

#### Data Classification
* Structured - SQL DB, csv, tabular, spreadsheets
* Semi-structured - NoSQL, JSON, YAML
* Unstructured - media files, text, office files

### Azure General

![image](https://github.com/nikvolynets/azure-info/assets/151893648/faf1a881-ff96-4e74-a210-e3859fdfdeaf)

### Azure storage

#### Two account types:
* Standard
* Premium

#### Four data types:
* Blob - all types of files (most commonly used)
  * Data Lake Storage Gen2 - Hierarchical blob storage, can criete directories (integrated with Hadoop)
* File
* Queue - meesages between applications
* Table - semi-structured NoSQL data

#### Three tiers for storing:
* Hot - friquently accessed data
* Cool - at least 30 days
* Archive - store at least 180 days

#### Azure Data Lake Gen2 = Blob storage + Data Lake Gen1 (Hadoop)
* Access tiers - hot, cool, archive
* Monitoring services - create rules to manage blob access tiers
* Security
* Life Cycle policy
* Redundancy

### Azure Data Factory (ADF)

Description: cloud ETL service allows to create serverless data integration and data transformation with code-free UI.

Data Factory Pipeline:

Blod storage (csv file) --> Linked Service --> Dataset --> Copy Activity (Job) --> Dataset --> Linked Service --> SQL Server (table)

Integration Runtime runs all the jobs, pipeline orchestrator.

Data Factory - manages the Integration Runtime and the Pipeline.

![image](https://github.com/nikvolynets/azure-info/assets/151893648/a60a40f4-2a83-4cf5-9121-05a455df9984)

Pipeline often includes more than 1 copy activity.
Linked Service has information of how to connect to the data or a SQL database

#### Key ADF concepts:

* Pipeline - logical grouping of activities that performs a unit of work.
* Activity - processing step in a pipeline.
* Datasets - data structures that is reference of data in the activities as inputs or outputs.
* Linked services - connection strings which define the connections between external resources.
* Integration Runtime - bridge between the activity and linked services. Compute unit to run activity while meeting security and compliance rules.
* Triggers (scheduler) - determine when a pipeline execution needs to be kicked off.

#### Integration Runtimes - compute infrustructure in ADF

Three types:
- Azure integration runtime - used between Azure services
- Self-hosted integration runtime - run copy activities between on-premisis (private VNET) solutions and cloud data store.
- Azure-SQL Server Integration Services (SSIS) - run SSIS packages

#### Activity types:

- Data movement
- Data transformation
- Control flow

#### Triggers types:

* Schedule trigger - invokes a pipeline on a wall-clock schedule.
* Tumbling window trigger - operates on a periodic interval, while also retaining state.
* Event-based trigger - a trigger that responds to an event.

#### Mapping Data Flows - visually designed data transformations in ADF

Debug mode allows to see the results of each transformation step while you build and debug your data flows.
Monitoring Data Flows

### Azure Synapse Analytics - signle unified service blending big data analytics (Databricks), data warehousing (SQL DW, Data Lake Storage) and data integration (ADF)

![image](https://github.com/nikvolynets/azure-info/assets/151893648/b8f6f1dd-7786-4de5-adc7-defceb0be492)

* OLTP - online transational processing
* OLAP - online analytics processing
* MPP - massively parallel processing

#### 2 types of pools:
* SQL pool - RunTime for SQL scripts
* Apache Spark pool - RineTime for Notebooks (Python, Scala etc.)

#### Key features:
* Integration
* Management
* Monitoring
* Security
