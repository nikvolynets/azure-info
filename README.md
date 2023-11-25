# azure-info

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
