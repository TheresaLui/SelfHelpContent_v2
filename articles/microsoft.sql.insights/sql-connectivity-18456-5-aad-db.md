<properties
	pageTitle="Login failed - the specified AAD user could not be found"
	description="Login failed because the specified AAD user could not be found"
	infoBubbleText="We ran diagnostics on your resource and found that login failed because the specified AAD user could not be found"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_5_aad_sql"
	diagnosticScenario="SqlLoginError18456"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Connectivity"
/>
# We ran diagnostics on your resource and found an issue

## **Login failed, the specified Azure Active Directory user could not be found**

<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and we were able to detect login failures.
<br>
The error returned indicates that the Azure Active Directory (AAD) user was not found.
This may occur if you are trying to connect with an AAD user (other than the server administrator that owns the database) but there is no Azure AD-based contained database user created inside the database.  
<br>
If you are connecting using tools like SSMS you may also need to specify the database you want to connect to. By default, SSMS will try to connect to master database, AAD users are created as contained database users inside each user database but may not have been created in master database.
<br>

<!--$FailedLogins18456State5AADDB--> FailedLogins18456State5AADDB <!--/$FailedLogins18456State5AADDB-->
<!--/issueDescription-->

## **Recommended Steps**

* Check that the user exists:

    1. Connect to the database
    2. Run the following query: `select * from sys.database_principals where name = 'insert the username here'`
    3. If the query returns no record, [create the user](https://docs.microsoft.com/azure/azure-sql/database/authentication-aad-configure?tabs=azure-powershell#create-contained-users-mapped-to-azure-ad-identities) in the database
    4. If the user exists, please verify if the last 4 digits in the sid are the same as the last 4 digits of the Object ID for that AAD user


## **Recommended Documents**

* [Create contained users mapped to Azure AD identities](https://docs.microsoft.com/azure/azure-sql/database/authentication-aad-configure?tabs=azure-powershell#create-contained-users-mapped-to-azure-ad-identities)
