<properties
  pagetitle="V2 - Copy Activity and Self-Hosted IR – Errors or unexpected results&#xD;"
  description="Troubleshoot Azure Data Factory copy activity issues."
  service="microsoft.datafactory"
  resource="factories"
  ms.author="shelfeng,brianwan"
  selfhelptype="Generic"
  supporttopicids="32629461"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="datafactorycopytroubleshooter"
  ownershipid="AzureData_DataFactory" />
# V2 - Copy Activity and Self-Hosted IR – Errors or unexpected results

Resolve issue related to Self-Hosted Integration Runtime (SHIR) using these steps.

## Recommended Steps

* If you use Self-Hosted IR and experience known SHIR problems, follow the steps on the [Self-IR troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide). Note the **Report ID** and provide it with the support request.

* If running **Copy Activity** throws an error or exception code, start by validating whether the error is in the [General Copy Activity errors documentation](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#general-copy-activity-error). This article contains most common errors from different data sources and actions to resolve them.

* For formatting errors, review the following sections:

   * Troubleshoot errors associated with CSV files or [Delimited Text format](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#delimited-text-format) in general
   * Troubleshoot errors related with [JSON format](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#json-format)
   * Troubleshoot errors when using [Parquet format](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#parquet-format)

* For errors on the most commonly associated data sources and sinks, review the following error troubleshooting guides:
   * [SQL connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-sql-data-warehouseazure-sql-databasesql-server)
   * [Azure Storage connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-blob-storage)
   * [ADLS Gen 1 connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen1)
   * [ADLS Gen 2 connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen2)
   * [Cosmos DB connector common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-cosmos-db)
   
## **Recommended Documents**

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide)
* [Copy Activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/copy-activity-overview)
* [Copy Activity performance and tuning guide](https://docs.microsoft.com/azure/data-factory/copy-activity-performance)
* [Schema mapping in copy activity](https://docs.microsoft.com/azure/data-factory/copy-activity-schema-and-type-mapping)
* [Fault tolerance of copy activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/copy-activity-fault-tolerance)
* [Parallel Copy](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#parallel-copy)
* [Integration runtime in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime#determining-which-ir-to-use)
* [Create and configure a self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime)

### **FAQ and Features request**

* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)