<properties
	pageTitle="Data Sync - Invalid column name"
	description="Data Sync encountering missing columns during synchronization attempts"
	infoBubbleText="Data Sync encountering missing columns during synchronization attempts"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_invalidcolumnname"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Data Sync - Invalid column name

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect that Data Sync is facing errors during sync attempts due to columns not being present in the tables to be synchronized.

If sync schema tables are missing in the destination database, SQL Data Sync creates them with the columns you selected. However, if the table already exists, SQL Data Sync will not create the missing columns.

Data Sync is detecting missing columns on the following sync group(s):<br>

<!--$SyncGroupInvalidColumnNameList--> SyncGroupInvalidColumnNameList <!--/$SyncGroupInvalidColumnNameList-->

<!--/issueDescription-->

## **Recommended Steps**

* Create the missing columns manually in all databases

**Note:** SQL Data Sync auto-provisioning feature may not create a full-fidelity schema for the following reasons:

* Only columns you select are created in the destination table. Columns not selected are ignored.
* Only selected column indexes are created in the destination table. For columns not selected, those indexes are ignored.
* Indexes on XML type columns aren't created
* CHECK constraints aren't created
* Triggers on the source tables aren't created
* Views and stored procedures aren't created

Because of these limitations, we recommend the following things:

* For production environments, create the full-fidelity schema yourself
* When experimenting with the service, use the auto-provisioning feature
