<properties
	pageTitle="Login failed in on-premises member"
	description="Login failed in on-premises member"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_loginfailedonprem"
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
We were able to detect a login failure in the following On-Premises Member Database(s):<br>
**<!--$LoginFailedOnPremList--> LoginFailedOnPremList <!--/$LoginFailedOnPremList-->**
<!--/issueDescription-->

Please update the credentials for the database(s).

## **Recommended Steps**

1. Open the "**Microsoft SQL Data Sync Agent 2.0**" application
2. Select the database
3. Click on "**Edit Credentials**"
4. Update the credentials
5. Test the connection and **Save**

In case the failing task is Sync, please review the credentials for the hub:<br>

1. In [Azure Portal](https://portal.azure.com), navigate to the hub database
2. Select "**Sync to other databases**"
3. Select the sync group
4. Click on "**Databases**"
5. Select the hub database
6. Update the username and password
7. Click **Save**

You may now retry the operation, or wait for it to be automatically triggered by Data Sync (if applicable).
