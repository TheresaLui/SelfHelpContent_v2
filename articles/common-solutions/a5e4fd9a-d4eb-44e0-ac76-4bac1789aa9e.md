<properties
  pagetitle="Connector Unexpected Behavior or Errors"
  service="microsoft.datafactory"
  resource="datafactories"
  ms.author="shelfeng"
  selfhelptype="Generic"
  supporttopicids="32784319"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  disableclouds=""
  articleid="a5e4fd9a-d4eb-44e0-ac76-4bac1789aa9e"
  ownershipid="AzureData_DataFactory" />
# Connector Unexpected Behavior or Errors

Resolve unexpected behavior or errors in Connector using the following steps.

## **Recommended Steps**
* If Connector throws an error or exception code, start by validating whether the error is in the [Copy Activity errors documentation](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide). This article contains most common errors from different data sources and actions to resolve them.

* If this is a transient issue, such as an instable network connection, add `retry` to your [activity policy](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities#activity-policy).

* Review the specific connector’s document from [Data Store connectors](https://docs.microsoft.com/azure/data-factory/copy-activity-overview?WT.mc_id=Portal-Microsoft_Azure_Support#supported-data-stores-and-formats) for more details.  If error or exception is thrown from 3rd party driver (ODBC Connector), please review documents from 3rd party.

* If you use **Self-Hosted IR**, follow the steps in the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory).

* For errors on the most commonly associated data sources and sinks, review the following error troubleshooting guides:
   * [SQL connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-sql-data-warehouseazure-sql-databasesql-server)
   * [Azure Storage connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-blob-storage)
   * [ADLS Gen 1 connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen1)
   * [ADLS Gen 2 connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen2)
   * [Cosmos DB connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-cosmos-db)

* For formatting errors, review the following sections:

   * Troubleshoot errors associated with CSV files or [Delimited Text format](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#delimited-text-format) in general
   * Troubleshoot errors related with [JSON format](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#json-format)
   * Troubleshoot errors when using [Parquet format](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#parquet-format)
   
## **Recommended Documents**

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide)
* [Copy Activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/copy-activity-overview)
* [Schema mapping in copy activity](https://docs.microsoft.com/azure/data-factory/copy-activity-schema-and-type-mapping)
* [Fault tolerance of copy activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/copy-activity-fault-tolerance)
* [Integration runtime in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime#determining-which-ir-to-use)
* [Create and configure a self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime)

### **FAQ and Features request**

* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
