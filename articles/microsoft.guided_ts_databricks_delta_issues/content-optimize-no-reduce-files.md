<properties
	pageTitle="Running Optimize command on a Delta table doesn’t seem to reduce the number of files"
	description="Running Optimize command on a Delta table doesn’t seem to reduce the number of files"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="cf04452b-0406-4ff1-8e5a-2d2a1907c258"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Running Optimize command on a Delta table doesn’t seem to reduce the number of files

**Problem**

When you run optimize command on Delta table, it doesn’t seem to compact and reduce the number of files. Under the file system storage, you could still see a large number of small files.	

**Troubleshooting**

* Verify if the storage location still has small files, even after optimize command is run
* Try listing the directory using filesystem commands to see if the small files still exist

**Cause**

Even if the smaller files were compacted to larger files, the smaller files will not be completely removed, instead they will just be removed from the latest state of the transaction log. Since the stale data files are no longer referenced in the delta transaction log, they will not be retrieved in the query results.

This is by design that the stale data files are retained until default retention period of 7 days. The configuration property ""delta.deletedFileRetentionDuration"" determines how long the stale data files are kept before they are removed by Vacuum command.

**Solution**

Check if the compacted large file is also available along with the small files. If so, this is as per design. The stale data files are kept to prevent any long running or streaming jobs accessing this delta table from failing.  

Running vacuum command on the delta table with retain 0 hours, will essentially remove all the stale data files:

    VACUUM delta.`/data/events` RETAIN 0 hours

However, if there were any long running or streaming jobs that were concurrently accessing the stale data files, then those operations will fail. So the recommendation here is to leave it as is and notice that the small files will no longer be there after 7 days."

**Recommended Documents**

* [Vacuum a Delta table](https://docs.microsoft.com/azure/databricks/spark/latest/spark-sql/language-manual/vacuum#--vacuum-a-delta-table-delta-lake-on-azure-databricks)