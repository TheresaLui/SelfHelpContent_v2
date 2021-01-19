<properties
	pageTitle="java.io.FileNotFoundException: No such File or Directory: scheme://Delta-path/partition=HIVE_DEFAULT_PARTITION/part-xxxxx.parquet"
	description="java.io.FileNotFoundException: No such File or Directory: scheme://Delta-path/partition=HIVE_DEFAULT_PARTITION/part-xxxxx.parquet"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c74a1bb8-b020-4bb1-b933-50f749ea17eb"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Getting java.io.FileNotFoundException: No such File or Directory: scheme://Delta-path/partition=HIVE_DEFAULT_PARTITION/part-xxxxx.parquet 

<!--issueDescription-->

Based on provided details and initial investigation, please find a summary of issue as below:

## **Problem**

Getting below error message when trying to query a Delta table:

    java.io.FileNotFoundException: No such File or Directory: scheme://Delta-path/partition=HIVE_DEFAULT_PARTITION/part-xxxxx.parquet 

## **Cause**

This most likely can happen because of previous write, followed by incorrect deletion of the data. For example, if user writes to delta table with partition column having null values then it will go to HIVE_DEFAULT_PARTITION. Later if the user realizes that it is no longer needed and if user deletes it directly from the storage using file system commands or from storage UI, then this issue can happen. 

This is because it will be removed from underlying storage, but the transaction log still references the file. Any operation to Delta table needs to happen through Delta commands. For example, DELETE FROM table can be used to remove any files from Delta table.

## **Solution**

* Using Delta DELETE command, delete the data in partition using WHERE condition HIVE_DEFAULT_PARTITION
* Using fsck repair table command, delete any reference to HIVE_DEFAULT_PARTITION in transaction log, that is not in underlying storage
* Refresh the table using Refresh table command, to refresh any cached entries
* Perform all the above operations using the same cluster
* Wait for few minutes, and then run the command/job, to avoid any consistency issues. Now it should work fine.


<!--/issueDescription-->
