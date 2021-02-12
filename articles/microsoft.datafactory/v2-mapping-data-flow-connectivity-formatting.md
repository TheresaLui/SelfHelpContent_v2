<properties
  pagetitle="Mapping data flow - Source/Sink Format and Connector Issue"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="rakatuko"
  selfhelptype="Generic"
  supporttopicids="32633540,32633539"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="v2-mapping-data-flow-connectivity-formatting.md"
  ownershipid="AzureData_DataFactory" />
# Mapping data flow - Source/Sink Format and Connector Issue

Mapping data flows currently supports connecting to some common data sources and sinks. See current [sources](https://docs.microsoft.com/azure/data-factory/data-flow-source) and [sinks](https://docs.microsoft.com/azure/data-factory/data-flow-sink). If you are experiencing issues connecting to any of the supported data sources or sinks, review the following troubleshooting guides, which cover the most common errors and solutions.

**NOTE:** The Azure Data Factory team is making improvements to dataflow for the **"Validate schema"** option on connectivity (for CSV, Excel, XML, JSON, and Cosmos DB). 

If you are using Azure Data Factory V2 dataflow, you may receive one of the following errors when attempting to execute your dataflow pipeline if the option **Validate schema** is selected on connectivity source/sink (CSV, Excel, XML, JSON, and Cosmos DB) in the next several weeks. **Note:** As stated below, the deployment will start on February 1, 2021.

- Missing column _xxx_ 
- Validate schema failed. Source has 6 columns instead of 7 
- Column _xxx_ has missing fields in types (Found: yyy, Required: zzz) 

**Recommended Action:**
 
The deployment will start on February 1, 2021. Customers can take the following actions before the start of deployment to avoid the errors listed in the preceding section: 

- For dataflows, unselect the **Validate schema** option on source/sink of connectivity (CSV, Excel, XML, JSON, and Cosmos DB). 
- Manually update the source/sink schema of connectivity (CSV, Excel, XML, JSON, and Cosmos DB) and ensure there is a subset of your actual data to avoid a mismatch with schema column name or number. 

### **Troubleshooting guides for supported data sources/sinks**

* [SQL connector, Azure Synapse Analytics troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-sql-data-warehouseazure-sql-databasesql-server)
* [Azure Storage connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-blob-storage)
* [ADLS Gen 1 connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen1)
* [ADLS Gen 2 connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen2)
* [Cosmos DB connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-cosmos-db)

Azure Data Factory has access to over [90 native connectors](https://docs.microsoft.com/azure/data-factory/connector-overview). To include or write data to any of those other sources from your data flow, use the Copy Activity to load or move that data from one of the supported staging areas, before starting, or after completion of your data flow.

### **Formatting Troubleshooting**

If you are having issues with the format supported by the data sources, see the following troubleshooting guides that cover common errors and solutions for the following specific formats:
* [JSON common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#json-format)
* [Parquet common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#parquet-format)
* [Delimited text troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#delimited-text-format)

## **Recommended Documents**

For common errors and basic Mapping Data Flow activity troubleshooting, see the following documentation:
- [Data flow troubleshooting guide](https://docs.microsoft.com/azure/data-factory/data-flow-troubleshoot-guide)
- [Mapping Data Flows in Azure Data Factory Overview](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-overview)
- [Mapping Data Flow Datasets](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-datasets)
- [Create Azure Data Factory Data Flow](https://docs.microsoft.com/azure/data-factory/data-flow-create)
- [Mapping Data Flow Debug Mode](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-debug-mode)
- [Execute data flow activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/control-flow-execute-data-flow-activity)

**Data Flow Transformations**
- [Mapping Data Flow Source Transformation](https://docs.microsoft.com/azure/data-factory/data-flow-source)
- [Mapping Data Flow Schema Drift](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-schema-drift)
- [Mapping Data Flow Sink Transformation](https://docs.microsoft.com/azure/data-factory/data-flow-sink)

### **FAQ**

**Can I connect to Azure Analysis Services using Mapping Data Flow?**

You will need a copy activity in order to move the data to a staging supported data source from your Azure Analysis Services.

**I have a Linked Service for Azure SQL Database configured to use a Self-Hosted IR, can I use it with Mapping Data Flow?**

Mapping Data Flow only supports the Azure IR. if your Azure SQL Database Firewall configuration does not allow access to the Azure IR IP address, your mapping data flow will not be accessing the data. Resolve this by whitelisting the Azure IR IP addresses, or by copying the data to a staging supported data source if you cannot change your firewall configuration.

**My connection to Azure Synapse Analytics (Formerly Azure Data Warehouse) works when I test connectivity, but it fails when attempting to write data with a permissions error. What are the permissions required?**

To use PolyBase, the user loading data into SQL Data Warehouse must have the `CONTROL` permission on the target database. For more information, see the connector documentation.

To request a new feature, see [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory).

### **Common Issues**

- If you receive **The corpus path is null or empty**_ error message when using the `model.json` source type from Power BI or Power Platform dataflows, see [ADF Adds support for inline datasets and common data models](https://techcommunity.microsoft.com/t5/azure-data-factory/adf-adds-support-for-inline-datasets-and-common-data-model-to/ba-p/1441798)
