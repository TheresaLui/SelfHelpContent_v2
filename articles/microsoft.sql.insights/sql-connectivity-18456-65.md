<properties
	pageTitle="Login failed because password did not match that for the user provided"
	description="Login failed because password did not match that for the user provided"
	infoBubbleText="Login failed because password did not match that for the user provided"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_65"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13491,16259"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Connectivity"
/>
# We ran diagnostics on your resource and found an issue

## **Login failed because password did not match that for the user provided**

<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and we were able to detect login failures.
<br>

<!--$FailedLogins18456State65--> FailedLogins18456State65 <!--/$FailedLogins18456State65-->
<!--/issueDescription-->
<br>

## **Recommended Steps**

The error returned usually means that the login attempt was made using a **contained user** that exists, the database is correct, but the **password is invalid**.   
This can also happen if you use a SQL login to connect to a contained database that has a contained user with the same name but a different password.   
To resolve this issue, contact your service administrator for valid credentials.   

## **Recommended Documents**

- [Authorize database access to SQL Database, SQL Managed Instance, and Azure Synapse Analytics](https://docs.microsoft.com/azure/azure-sql/database/logins-create-manage)

- [Contained Database Users - Making Your Database Portable](https://docs.microsoft.com/sql/relational-databases/security/contained-database-users-making-your-database-portable)