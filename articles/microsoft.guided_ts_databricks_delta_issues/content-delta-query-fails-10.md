<properties
	pageTitle="Delta table query fails with ArrayIndexOutOfBoundsException or java.lang.RuntimeException: java.io.IOException: could not read page or org.apache.parquet.io.ParquetDecodingException"
	description="Delta table query fails with ArrayIndexOutOfBoundsException or java.lang.RuntimeException: java.io.IOException: could not read page or org.apache.parquet.io.ParquetDecodingException"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="22b56696-2204-4138-902f-304eeb507311"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Unable to query certain partitions of a Delta table or in some cases the Delta table becomes unusable

**Problem**	

Unable to query certain partitions of a Delta table or in some cases the Delta table becomes unusable getting error similar to:

    ArrayIndexOutOfBoundsException 
    java.lang.RuntimeException: java.io.IOException: could not read page 
    org.apache.parquet.io.ParquetDecodingException

**Troubleshooting**

* Verify if (select * from deltaTable limit 1) succeeds:
	* If it succeeds, it could be a delta data file corruption
	* If it fails, then it could be checkpoint file corruption issue	
* Try reading the Delta checkpoint parquet file and Delta data parquet file to confirm if it is one of the corruption issues

**Solution**

* Checkpoint file corruption issue can be fixed without any data loss by making the metadata file _delta_log/_last_checkpoint to point to the previous checkpoint version that is likely to be correct.
* Delta data file corruption issue can be fixed by deleting the data file and then running FSCK REPAIR TABLE on the Delta table to drop that file name from the log.
