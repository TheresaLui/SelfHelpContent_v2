<properties
	pageTitle="Timeout while running Refresh Schema"
	description="A timeout ocurred while running Refresh Schema"
	infoBubbleText="A timeout ocurred while running Refresh Schema"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_timeout_refresh_schema"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Timeout while running Refresh Schema

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect timeout during Refresh Schema:<br>
**<!--$TimeoutRunningRefreshSchemaInsightIdDatabaseList--> TimeoutRunningRefreshSchemaInsightIdDatabaseList <!--/$TimeoutRunningRefreshSchemaInsightIdDatabaseList-->**
<!--/issueDescription-->

## **Recommended Steps**

This timeout is usually associated with lack of performance on the Sync Metadata Database to process the results.
Please scale-up the Sync Metadata Database and try again.
You may scale back down after Refresh Schema completes with success.