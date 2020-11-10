<properties
	pageTitle="Sync group is out-of-date"
	description="Sync group is out-of-date"
	infoBubbleText="Sync group is out-of-date"
	service="microsoft.sql"
	resource="servers"
	ms.author="ferno"
	authors="ferno-ms"
	displayOrder=""
	articleId="sql_datasync_outofdate"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Sync group is out-of-date

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
When using Data Sync, if a sync group is not synced for a long period of time or some changes in a sync group continuously fail to apply for a long period, data that was not yet synced might be cleaned up. In this case, the sync group will no longer be able to sync and must be deleted and recreated.<br>
Make sure that all changes are successfully synced regularly to avoid sync groups from becoming out-of-date.<br>

The following sync groups are out of date:<br>
**<!--$SyncGroupOutOfDateList--> SyncGroupOutOfDateList <!--/$SyncGroupOutOfDateList-->**
<!--/issueDescription-->

## **Recommended Steps**

To delete the out-of-date sync group in the [Azure Portal](https://portal.azure.com), you can go to the Overview page for the Azure SQL database that is the hub of the sync group.

To delete a sync group from the database overview page:

1. Click **Sync to other databases** in the left-hand menu under Settings
2. Click on the name of the outdated sync group under Sync Group
3. Click **Delete** on the toolbar and confirm

If needed, the sync group may be recreated after this is done by clicking on **New Sync Group** on the toolbar from the **Sync to other databases** page.