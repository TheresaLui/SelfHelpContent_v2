<properties
	pageTitle="java.io.FileNotFoundException: dbfs:/delta/delta-path/part-xxxx.snappy.parquet"
	description="java.io.FileNotFoundException: dbfs:/delta/delta-path/part-xxxx.snappy.parquet"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="fc5b7053-2fd2-49fd-a8aa-dd97d8453f70"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Getting java.io.FileNotFoundException: dbfs:/delta/delta-path/part-xxxx.snappy.parquet

**Problem**

A file referenced in the transaction log cannot be found. This occurs when data has been manually deleted from the file system rather than using the table DELETE statement.

**Troubleshooting**

* Verify if there is any file system rm commands used to remove the underlying data directory
* Ask customer if they have deleted and recreated the Delta table

**Cause**

This can occur when you delete and recreate a delta table on the same data path. Or if you delete a data file directly from the data directory using file system rm -r command, instead of using DELETE FROM syntax. 

What happens is the data file will be removed from the data directory, however, the reference to that data file will still be there in the transaction log. So when we query the Delta table, it tries to look for the data file that is in the transaction log. Since the data file no longer exists in the data directory, it will throw file not found exception.

**Solution**

To temporarily resolve the issue, you can run FSCK repair table command. This command will repair the table, by syncing the transaction log with the actual details of the data directory. 

The permanent solution will be to change the process, so that you no longer delete the underlying data files of a Delta table, using filesystem commands. If your use case needs deleting/recreating Delta table, you should overwrite the Delta table instead. Overwriting Delta table is preferred over deleting/recreating it.
