# azure-info

### Azure Data Factory

Description: cloud ETL service allows to create serverless data integration and data transformation with code-free UI.

Data Factory Pipeline:

Blod storage (csv file) --> Linked Service --> Dataset --> Copy Activity (Job) --> Dataset --> Linked Service --> SQL Server (table)

Integration Runtime runs all the jobs, pipeline orchestrator.

Data Factory - manages the Integration Runtime and the Pipeline.

![image](https://github.com/nikvolynets/azure-info/assets/151893648/a60a40f4-2a83-4cf5-9121-05a455df9984)

Pipeline often includes more than 1 copy activity.
Linked Service has information of how to connect to the data or a SQL database
