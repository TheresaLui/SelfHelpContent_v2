<properties
	pageTitle="Login failed in Hub Database"
	description="Login failed in Hub Database"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_loginfailedinhub"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect a login failure in the following Hub Database(s):<br>

**<!--$LoginFailedHubList--> LoginFailedHubList <!--/$LoginFailedHubList-->**<br>

Please update the credentials for the hub(s).
<!--/issueDescription-->

## **Recommended Steps**

1. In [Azure Portal](https://portal.azure.com), navigate to the hub database
2. Select "Sync to other databases"
3. Select the sync group
4. Click on "Databases"
5. Select the Hub Database
6. Update the Username and Password
7. Click Save

You may now retry the operation, or wait for it to be automatically triggered by Data Sync (if applicable).
