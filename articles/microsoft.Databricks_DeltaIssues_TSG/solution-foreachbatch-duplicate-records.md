<properties
	pageTitle="Writing to a Delta table using a streaming job with foreachBatch() results in duplicate records"
	description="Writing to a Delta table using a streaming job with foreachBatch() results in duplicate records"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6da6a0f8-5e4f-4d52-9b16-1a262b916687"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Writing to a Delta table using a streaming job with foreachBatch() results in duplicate records

<!--issueDescription-->

Based on provided details and initial investigation, please find a summary of issue as below:

## **Problem**

When you write streaming job results to a delta table using foreachBatch(), you see duplicate records in the delta table.

## **Cause**

Duplicates in delta table when writing streaming job results using foreachBatch() can occur because of multiple reasons:

* It could happen if the source itself is emitting duplicate events
* This could also happen when the streaming read option "ignoreChanges" is set to "false", which means any changes to the data source are not ignored and will be streamed to the sink. When the updated record is streamed, it streams the whole file (containing the updated records), which results in streaming of unchanged records (within the file) as well. This results in duplicate records being inserted into the target delta table.

## **Solution**

To avoid duplicate records being inserted into the delta table, we can incorporate a deduplication logic in the foreachBatch().


<!--/issueDescription-->
