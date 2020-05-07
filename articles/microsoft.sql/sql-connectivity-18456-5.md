<properties
	pageTitle="Login failed - the specified user could not be found"
	description="Login failed because the specified user could not be found"
	infoBubbleText="We ran diagnostics on your resource and found that login failed because the specified user could not be found"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_5"
	diagnosticScenario="SqlLtsFailedLogin"
	selfHelpType="diagnostics"
	supportTopicIds="32630429"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# Login failed - the specified user could not be found

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> we were able to detect login failures:<br>

<!--$FailedLogins18456State5--> FailedLogins18456State5 <!--/$FailedLogins18456State5-->

<!--/issueDescription-->

<br>
The error returned indicates that the user was not found. This may occur if the username specified in the application connection string is incorrect, or if there is no corresponding login or contained database user inside the database.
<br>

## **Recommended Steps**

* Check that the application connection string contains the correct username
* If you are using a SQL login, check that the login exists:

	1. Connect to the master database
	2. Run the following query `select * from sys.sql_logins where name = 'insert the username here'`
	3. If the query returns no record, please create the login

* If you are using contained database users, check that the user exists:
	
	1. Connect to the database
	2. Run the following query: `select * from sys.database_principals where name = 'insert the username here'`
	3. If the query returns no record, please create the user

## **Recommended Documents**

* [Create SQL Login and SQL User on your Azure SQL DB – Azure SQL Database Support](https://blogs.msdn.microsoft.com/azuresqldbsupport/2016/10/05/create-sql-login-and-sql-user-on-your-azure-sql-db/)
