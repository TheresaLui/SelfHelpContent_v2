<properties
	pageTitle="Login failed in Hub Database"
	description="Login failed in Hub Database"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="vitomaz"
	displayOrder=""
	articleId="sql_datasync_loginfailedinhub"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32574329"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We were able to detect a login failure in the following Hub Database(s):<br>
**<!--$LoginFailedHubList--> LoginFailedHubList <!--/$LoginFailedHubList-->**
<!--/issueDescription-->

Please update the credentials for this hub(s).<br>

Using the portal you can:<br>
1. Navigate to the hub database<br>
2. Select 'Sync to other databases'<br>
3. Select the sync group<br>
4. Click on 'Databases'<br>
5. Select the Hub Database<br>
6. Update the Username, Password and save<br>
<br>
Based on your goal you may retry the operation now or wait for it to be automatically triggered by Data Sync if applicable.​