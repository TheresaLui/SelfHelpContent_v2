<properties
	pageTitle="Sync Group having problems when recording provision timestamps"
	description="Sync Group having problems when recording provision timestamps"
	infoBubbleText="Sync Group having problems when recording provision timestamps"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_provisiontimestamp"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Sync Group having problems when recording provision timestamps

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect that Data Sync provisioning related objects are in an inconsistent state for one or more sync groups. This is usually caused by usage of backup/restore, point-in-time restore, geo-replication, or manual modifications in the metadata tables.

The following sync group(s) are facing this issue:

<!--$SyncGroupProvisionTimestampDatabaseList--> SyncGroupProvisionTimestampDatabaseList <!--/$SyncGroupProvisionTimestampDatabaseList-->

<!--/issueDescription-->

## **Recommended Steps**

1. Remove the table from **all the sync groups**
2. Clean up the associated metadata objects for the table facing the issue in all databases using [this script](https://raw.githubusercontent.com/vitomaz-msft/DataSyncMetadataCleanup/master/cleanup%20data%20sync%20object%20V2.sql), which will find out which sync-related objects for the specific table (SP\trigger\UDTT\tracking table) still exist. Please note that this script will not remove the objects, will just generate the drop statements. You must manually run the generated statements.
3. Add the table back to the sync groups
4. Trigger a Sync (the table should be provisioned successfully)
