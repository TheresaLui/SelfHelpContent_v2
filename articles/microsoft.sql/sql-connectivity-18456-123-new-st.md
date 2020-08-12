<properties
	pageTitle="Login failed - Empty username or password"
	description="Login failed because the provided login contains an empty username or password"
	infoBubbleText="We ran diagnostics on your resource and found that login failed because the provided login contains an empty username or password"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_123-new-st"
	diagnosticScenario="SqlLtsFailedLogin"
	selfHelpType="diagnostics"
	supportTopicIds="32745428"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# Login failed - Empty username or password

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> we were able to detect login failures:<br>
<!--$FailedLogins18456State123--> FailedLogins18456State123 <!--/$FailedLogins18456State123-->

<!--/issueDescription-->

<br>
The error returned indicated that the corresponding login contains either an empty username or password.
<br>

## **Recommended Steps**

* Retry the login entering both username and password
