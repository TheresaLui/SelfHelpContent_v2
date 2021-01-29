<properties
	pageTitle="Login failed due to empty username"
	description="Login failed because the provided login contains an empty username"
	infoBubbleText="We ran diagnostics on your resource and found that login failed because the provided login contains an empty username"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_58"
	diagnosticScenario="SqlMILoginError18456"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI_Connectivity"
/>
# We ran diagnostics on your resource and found an issue

## **Login failed due to empty username**

<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and we were able to detect login failures.
<br>

The error returned indicated that the corresponding login contains an empty username.
<br>

<!--$FailedLogins18456State58--> FailedLogins18456State58 <!--/$FailedLogins18456State58-->
<!--/issueDescription-->

## **Recommended Steps**

- Retry the login entering an username.   

Please note that connection strings with keyword **Integrated Security=True** (Windows Authentication) are **not supported**.   
Only SQL authentication and Azure Active Directory Authentication are currently supported.

## **Recommended Documents**

- [Authorize database access to SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/database/logins-create-manage)
- [Configure and manage Azure Active Directory authentication with SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?tabs=azure-powershell#provision-an-azure-active-directory-administrator-for-your-managed-instance)
