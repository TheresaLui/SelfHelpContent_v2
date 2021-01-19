<properties
	pageTitle="When querying a Delta table, only partial records are retrieved"
	description="When querying a Delta table, only partial records are retrieved"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5275e7a3-c5b3-4ade-adeb-7433ea66eb0b"
   	ownershipId="AzureData_AzureDatabricks"
/>

# When querying a Delta table, only partial records are retrieved

<!--issueDescription-->

Based on provided details and initial investigation, please find a summary of issue as below:

## **Problem**

When you run a read query on delta table, you may see only partial records getting retrieved. For example, you may see records from a specific date. The records inserted prior to a specific date may not be retrieved using a read query to delta table. However, the historical files may still exist in the underlying dataset directory.

## **Cause**

This can happen due to accidental deletion of the _delta_log directory from the Delta table by someone or it could happen if the initial dataset was written in parquet format, and then subsequent write operations were done using delta format (after creating an empty _delta_log directory). This is most likely a user error.

This results in a dataset directory where all the data files are available , however, the _delta_log transaction log only has version from a specific date. Any delta query can bring results only from the earliest version available in the _delta_log directory.

## **Solution**

* Move the delta log out of the dataset directory. Then the directory becomes a normal parquet directory. 
* Apply [Convert to Delta](https://docs.microsoft.com/azure/databricks/spark/latest/spark-sql/language-manual/convert-to-delta). This recreates the delta transaction log with all the commits. 
* Query command on the directory to fix the delta log transaction log issued to delta table should fetch all the records.

## **Recommended Documents**

* [Delta Transaction Log Protocol](https://github.com/delta-io/delta/blob/master/PROTOCOL.md#delta-transaction-log-protocol)
* [Unpacking The Transaction Log](https://databricks.com/blog/2019/08/21/diving-into-delta-lake-unpacking-the-transaction-log.html)


<!--/issueDescription-->