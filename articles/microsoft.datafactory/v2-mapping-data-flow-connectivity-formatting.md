<properties
  pagetitle="Mapping data flow - Source Format and Connector Issue Common Solutions&#xD;"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="grorcai,rakatuko"
  selfhelptype="Generic"
  supporttopicids="32633540"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="v2-mapping-data-flow-connectivity-formatting.md"
  ownershipid="AzureData_DataFactory" />
# Mapping data flow - Source Format and Connector Issue Common Solutions


Review the following troubleshooting steps for common scenarios with Dataflow sources.

### File-based connectors (Data Lake Storage Gen2, Blob Storage): Source with wildcard path has performance issues and/or unaccounted time in metrics
_**Causes**_: File discovery time is not reported in the metrics currently. A wider wildcard path pointing to folders with a lot of files can take a long time to discover files.<br>
_**Recommendations**_: To improve performance, make sure that the wildcard path is as targeted as possible<br>

### Common Data Model (CDM): Data with date and time is not loaded correctly or is null
_**Causes**_: The correct date/time format might not be configured at schema options<br>
_**Recommendations**_:<br>
- Ensure that the correct date/time format is chosen at projection
- Go to **Projection** > **Schema options** > **Infer drifted column types** to configure the format from the options in the drop-down list
- If the format is missing:
   - Make sure that the format you are expecting is a valid Java SimpleDateFormat
   - If it is valid, edit format in dataflow script manually as a workaround: select any format from the drop-down list, then select the script at the top right to edit
        
### CDM and Delimited dataset: - Column values are read as null even if defined in the schema 
_**Causes**_: Delimited data set expects a correct number of delimiters in all the data rows. For example, for `N` columns defined, `N-1` delimiters are expected.<br>
_**Recommendations**_: Ensure that the data is correct with N-1 delimiters in all the rows/files. Any tool used to generate the delimited dataset should produce the right number of delimiters even when containing null column values.

### Some data values/columns/characters are not showing the correct values
_**Causes**_: Incorrectly configured encoding can read the data incorrectly<br>
_**Recommendations**_: Ensure that the encoding used to create the dataset is supported by ADF Dataflow. Confirm that the same encoding is used at the dataset configuration.<br>

### Error: "The corpus path is null or empty"
_**Recommendations**_: If you receive this error when using the `model.json` source type from Power BI or Power Platform dataflows, see [ADF Adds support for inline datasets and common data models](https://techcommunity.microsoft.com/t5/azure-data-factory/adf-adds-support-for-inline-datasets-and-common-data-model-to/ba-p/1441798).

### **FAQ**

**Can I connect to Azure Analysis Services using Mapping Data Flow?**

You'll need a copy activity to move the data to a staging supported data source from your Azure Analysis Services.

**I have a Linked Service for Azure SQL Database configured to use a Self-Hosted IR, can I use it with Mapping Data Flow?**

Mapping Data Flow only supports the Azure IR. if your Azure SQL Database Firewall configuration does not allow access to the Azure IR IP address, your mapping data flow will not be accessing the data. Resolve this by allow-listing the Azure IR IP addresses, or by copying the data to a staging supported data source if you cannot change your firewall configuration.

### **Performance-related documentation for sources**
See this [general guide to optimize sources](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-performance#optimizing-sources). Here are a few quick notes:
- File-based sources are already highly optimized for reading. Any partitioning using [optimized tab](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-performance#file-based-sources) will slow performance.
- For file-based sources, if you are using a wildcard path, scope it to the minimum level, because file discovery is a time-consuming process. For example, looking for all files in a particular directory takes a long time, compared to using `**/myfiles*.csv utilize myDirectory/myFiles*.csv`.
- SQL source should use the [source-based partitioning](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-performance#azure-sql-database-sources). This enables Dataflow to read from SQL using multiple partitions. Make sure not to overwhelm the SQL server by adding too many partitions.
- For sources like [Azure Synapse Analytics utilize staging](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-performance#azure-synapse-analytics-sources), it's best to land data first in Azure storage to boost the overall performance. This option is on by default.

## **Recommended Documents**

* [Troubleshoot common error codes and messages](https://docs.microsoft.com/azure/data-factory/data-flow-troubleshoot-guide)
* [Configure dataflow sources](https://docs.microsoft.com/azure/data-factory/data-flow-source)
* [Request a new feature](https://feedback.azure.com/forums/270578-azure-data-factory)
