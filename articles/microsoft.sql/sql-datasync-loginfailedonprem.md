<properties
	pageTitle="Login failed in on-premises member"
	description="Login failed in on-premises member"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authorAlias="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_loginfailedonprem"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32574329"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We were able to detect a login failure in the following On-Premises Member Database(s):<br>
**<!--$LoginFailedOnPremList--> LoginFailedOnPremList <!--/$LoginFailedOnPremList-->**
<!--/issueDescription-->

Please update the credentials for the database(s).

## **Recommended Steps**

1. Open the "Microsoft SQL Data Sync Agent 2.0" application
2. Select the database
3. Click on "Edit Credentials"
4. Update the credentials
5. Test Connection and Save

You may now retry the operation, or wait for it to be automatically triggered by Data Sync (if applicable).