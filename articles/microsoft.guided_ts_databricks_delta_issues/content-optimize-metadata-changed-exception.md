<properties
	pageTitle="Optimize operation on Delta table fails with com.databricks.sql.transaction.tahoe.MetadataChangedException"
	description="Optimize operation on Delta table fails with com.databricks.sql.transaction.tahoe.MetadataChangedException"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="45a24bc9-d13d-4a61-8e63-172b9fa41ff9"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Optimize operation on Delta table fails with MetadataChangedException

**Problem**

Jobs that run optimize command fails with error:

    Error in SQL statement: ExecutionException: com.databricks.sql.transaction.tahoe.MetadataChangedException: The metadata of the Delta table has been changed by a concurrent update. Please try the operation again. Conflicting commit: {"version":xxxx,"timestamp":xxx,"userId":"xxxx","userName":"xxxx@xxxx.com","operation":"SET TBLPROPERTIES","operationParameters":{"properties":{"delta.autoOptimize":"true"}},"notebook":{"notebookId":"xxxx"},"clusterId":"xxxx","readVersion":xxxx,"isolationLevel":"SnapshotIsolation","isBlindAppend":true} Refer to https://docs.azuredatabricks.net/delta/isolation-level.html#optimistic-concurrency-control for more details.

**Troubleshooting**

* Verify if there were other jobs running concurrently at the same time on the same cluster
* Verify if there were concurrent jobs running against the same Delta table in question

**Cause**

This error can occur when optimize and other operation concurrently try to update the delta table metadata. While this concurrent update on a delta table metadata happens, the optimize operation fails, leaving path to the other potentially business critical Delta operation to succeed, as per design.

**Solution**

It is always safe to retry the optimize operation. So in case you see the above exception, you can always re-submit the optimize operation, as this exception happens on purpose leaving way for the other business critical Delta query operation to succeed. You can also enclose the optimize job with retry, so that it automatically retries whenever this exception occurs.

