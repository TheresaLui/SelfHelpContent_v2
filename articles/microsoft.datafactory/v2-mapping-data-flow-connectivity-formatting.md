<properties
 pageTitle="V2 - Mapping Data Flow Connectivity Troubleshooting"
 description="V2 - Mapping Data Flow Connectivity Troubleshooting"
 service="microsoft.datafactory"
 resource="factories"
 authors="hecepeda"
 ms.author="hecepeda"
 displayOrder=""
 selfHelpType="generic"
 supportTopicIds="32633540,32633539"
 resourceTags=""
 productPesIds="15613"
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="v2-mapping-data-flow-connectivity-formatting.md"
 ownershipId="AzureData_DataFactory"
/>

# Mapping data flow - Source/Sink Format and Connector Issue

Mapping data flows currently support connecting to some common data sources and sinks (see current [sources](https://docs.microsoft.com/azure/data-factory/data-flow-source) and [sinks](https://docs.microsoft.com/azure/data-factory/data-flow-sink)), if you are experiencing issues connecting to any of the supported data sources or sinks, make sure you review the following troubleshooting guides which contain most of the common errors and solutions, while connecting to these data sources.

### **Troubleshooting guides for supported data sources/sinks**

* [SQL connector, Azure Synapse Analytics troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-sql-data-warehouseazure-sql-databasesql-server)
* [Azure Storage connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-blob-storage)
* [ADLS Gen 1 connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen1)
* [ADLS Gen 2 connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen2)
* [Cosmos DB connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-cosmos-db)

Azure Data Factory has access to over [90 native connectors](https://docs.microsoft.com/azure/data-factory/connector-overview). To include or write data to any of those other sources from your data flow, use the Copy Activity to load or move that data from one of the supported staging areas, before starting, or after completion of your data flow.

### **Formatting Troubleshooting**

If you are having problems with the format supported by the data sources, review the following troubleshooting guides containing common errors and solutions for the formats below:

* [JSON common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#json-format)
* [Parquet common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#parquet-format)
* [Delimited text troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#delimited-text-format)

## **Recommended Documents**

For common errors and basic Mapping Data Flow activity troubleshooting please review the [data flow troubleshooting guide](https://docs.microsoft.com/azure/data-factory/data-flow-troubleshoot-guide).

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

**Q: Can I connect to Azure Analysis Services using Mapping Data Flow?**
**A:** You will need a copy activity, to move the data to a staging supported data source from your Azure Analysis Services.

**Q: I have a Linked Service for Azure SQL Database configured to use a Self-Hosted IR, can I use it with Mapping Data Flow?**
**A:** Mapping Data Flow only supports the Azure IR, if your Azure SQL Database Firewall configuration does not allow access to the Azure IR IP address, your mapping data flow will not be access the data, you can resolve this by whitelisting the Azure IR IP addresses, or by copying the data to a staging supported data source in case you cannot change your firewall configuration.

**Q: My connection to Azure Synapse Analytics (Formerly Azure Data Warehouse) works when I test connectivity, but it fails when attempting to write data with a permissions error, what are the permissions required?**
**A:** To use PolyBase, the user that loads data into SQL Data Warehouse must have "CONTROL" permission on the target database. For more information refer to the connector documentation

To request a new feature visit [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory).
