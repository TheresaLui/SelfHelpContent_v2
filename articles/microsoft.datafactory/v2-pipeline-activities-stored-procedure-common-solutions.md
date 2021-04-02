<properties
  pagetitle="Stored Procedure Common Solutions&#xD;"
  description="Stored Procedure Common Solutions"
  service=""
  resource=""
  ms.author="dfandel,gayang"
  selfhelptype="Generic"
  supporttopicids="32680904"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="d7bb0bbe-5679-4c5d-b4a7-d22ea545bbf6"
  ownershipid="AzureData_DataFactory" />
# Stored Procedure Common Solutions

## **Recommended Steps**

### Common errors

**A transport-level error occurs when receiving results from the server**
<br>This usually happens when there are transient network errors between ADF and SQL Server. 
1. Set a larger connection timeout (> 60s) and rerun the pipeline
2. Set up the activity level [retry](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities#activity-policy) to improve the stability

**An error code of 2402 (Execution fail against SQL Server) indicates a SQL error**
- Use the SQL Error number shown to debug the SQL issue. For details, see [SQL help documentation](https://docs.microsoft.com/sql/relational-databases/errors-events/database-engine-events-and-errors?view=sql-server-2017).

**Connection timeout**
<br>The problem could be a SQL database transient failure.
- Retry the operation to update the linked service connection string with a larger connection [timeout](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-code-sqlopenconnectiontimeout) value (specifically, > 60s)

**Slow performance**
<br>If Stored Procedure performance is slow, troubleshoot the cause by following these steps:
1. Check the queued duration for SHIR. If pending in queue, check your SHIR captivity and increase your captivity if you have many concurrent jobs.
2. Run the same Stored Procedure in SSMS to see whether the issue is same. If yes, the issue must be out of ADF.
3. Check Stored Procedure run history in SQL database, following the [documentation](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-exec-procedure-stats-transact-sql?view=sql-server-ver15). Follow up with the SQL team, if you need additional help.

### Known limitations

**Stored Procedure only supports SQL Server and Azure SQL Database**
<br>Other data stores (Oracle, Postgre, Snowflake, BigQuery, and so on) are not supported. 
- You can ask for the new feature or [vote](https://feedback.azure.com/forums/270578-data-factory) if the feature request is already there.

**Stored Procedure can't return any values**
<br>If you need to call the Stored Procedure to return values, follow this workaround, which uses [lookup activity](https://docs.microsoft.com/azure/data-factory/control-flow-lookup-activity).

### Best practices

**Running Stored Procedure more than once**
<br>Usually this happens because of a batch VM reboot, like a forced OS upgrade. The occurrence of this happening is very low (< 0.001%). 
- A best practice is to design your stored procedure to be [idempotent](https://docs.microsoft.com/azure/azure-sql/database/elastic-jobs-overview#idempotent-scripts).

**SQL error details are not in the activity output**rmatio
<br>A Data Factory pumps all activity run events to Azure Monitor, including error details. You can set up email alerts from those events. For more information, see [Alert and Monitor data factories using Azure Monitor](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor).

## **Recommended Documents**

* Activities documentation, including:
   * [Stored Procedure Activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/transform-data-using-stored-procedure)

**Azure Data Factory information** 
* [Azure Data Factory Updates](https://azure.microsoft.com/updates/?query=factory)
* [Azure Data Factory Blog](https://techcommunity.microsoft.com/t5/azure-data-factory/bg-p/AzureDataFactoryBlog)
* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
* [Azure Data Factory Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide)
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
