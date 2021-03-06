<properties
	pageTitle="Login failed - the specified AAD user could not be found"
	description="Login failed because the specified AAD user could not be found"
	infoBubbleText="We ran diagnostics on your resource and found that login failed because the specified AAD user could not be found"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_62_aad_mi"
	diagnosticScenario="SqlMILoginError18456"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI"
/>
# We ran diagnostics on your resource and found an issue

## **Login failed, the specified Azure Active Directory user could not be found**

<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and we were able to detect login failures.
<br>
The returned error indicates that the Azure Active Directory (AAD) user was not found.  

SQL Managed Instance supports Azure AD server principals (logins). Using contained database users is not required. Azure AD server principals (logins) enable you to create logins from Azure AD users, groups, or applications.  

This error may occur if you are trying to connect with an AAD user (other than the server administrator that owns the database), but there is no Azure AD-based login created for that AAD user/group/application.  
<br>

<!--$FailedLogins18456State62AADMI--> FailedLogins18456State62AADMI <!--/$FailedLogins18456State62AADMI-->
<!--/issueDescription-->

## **Recommended Steps**

**If you're using Azure AD server principals (logins), check that the user exists:**

1. Connect to master database
2. Run the following query: `select * from sys.server_principals where name = 'insert the username here'`
3. If the query returns no record, [create the login](https://docs.microsoft.com/azure/azure-sql/managed-instance/aad-security-configure-tutorial#create-an-azure-ad-server-principal-login-using-ssms) in the database
4. If the user exists, verify that the last 4 digits in the SID are the same as the last 4 digits of the Object ID for that AAD user


**If you're using contained database users, check that the user exists and verify that containment is not set to NONE:**

1. Connect to the database
2. Verify that the containment is not set to NONE using `select containment_desc FROM sys.databases where [name] = 'insert database name here'`. See more at [Contained Database Users](https://docs.microsoft.com/sql/relational-databases/security/contained-database-users-making-your-database-portable?view=sql-server-ver15#managed-instance).
3. Run the following query: `select * from sys.database_principals where name = 'insert the username here'`
4. If the query returns no record, [create the login](https://docs.microsoft.com/sql/t-sql/statements/create-login-transact-sql?view=azuresqldb-mi-current#azure-sql-managed-instance) in the database
5. If the user exists, verify that the last 4 digits in the SID are the same as the last 4 digits of the Object ID for that AAD user
6. Confirm that you are explicitly setting the database name while trying to connect


## **Recommended Documents**

* [Tutorial: Security in Azure SQL Managed Instance using Azure AD server principals (logins)](https://docs.microsoft.com/azure/azure-sql/managed-instance/aad-security-configure-tutorial#create-an-azure-ad-server-principal-login-using-ssms)

* [Create contained users mapped to Azure AD identities](https://docs.microsoft.com/azure/azure-sql/database/authentication-aad-configure?tabs=azure-powershell#create-contained-users-mapped-to-azure-ad-identities)

* [CREATE LOGIN](https://docs.microsoft.com/sql/t-sql/statements/create-login-transact-sql?view=azuresqldb-mi-current#azure-sql-managed-instance)
