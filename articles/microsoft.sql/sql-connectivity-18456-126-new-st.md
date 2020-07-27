<properties
	pageTitle="Login failed - database could not be found"
	description="Login failed because the database specified was not found on the server"
	infoBubbleText="We ran diagnostics on your resource and found that login failed because the database specified was not found on the server"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_126-new-st"
	diagnosticScenario="SqlLtsFailedLogin"
	selfHelpType="diagnostics"
	supportTopicIds="32745425"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Login failed - the database specified was not found on the server

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> we were able to detect login failures:<br>
<!--$FailedLogins18456State126--> FailedLogins18456State126 <!--/$FailedLogins18456State126-->

<!--/issueDescription-->

<br>
The error returned indicated that the database was not found. This may occur if the database name is incorrect or does not exist on the specified server.
<br>

## **Recommended Steps**

* Please check the application connection string contains the correct server and database name, i.e. `Server=tcp:my-server.database.windows.net,1433;Initial Catalog=mydatabase;Persist Security Info=False;User...`
* To access the correct connection string please do the following: 

	1. [Azure Portal](https://portal.azure.com), navigate to the correct database
	2. Select 'Connection Strings'
	3. Review the settings for Server and Catalog
 
