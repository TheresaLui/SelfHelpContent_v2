<properties
    pageTitle="Unable to login to the server"
    description="Unable to login to the server"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745428"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="3859900D-B935-4C93-98A8-EA8F7BE3165E"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Unable to login to the server

* **Login failures** with error code 18456 indicates that your packet has reached the Azure SQL services, but was rejected due to one or more of the following reasons:

  * Incorrect or empty passwords: *The client tool / application connecting to the database has incorrect or blank password. Please ensure that you have provided the valid password.*
  * Expired or invalid token: *You might get this error if the token has expired, if the token issuer is invalid, if no object Id is present in the token, if the token signature is incorrect or invalid or if SQL Server was unable to get the token from ADAL.*
  * Database requested by user does not exist on the specified server: *If you are connecting from client application, please ensure that the connection string has the correct database name.* OR *If you are connecting from a client tool (SSMS), click the 'Options' button in the connection dialog to expose additional connection options, and verify that the 'Connection Properties' tab has a "Connect to database" value of default selected.*
  * The connections were rejected due to DoSGuard protection: *DoSGuard actively tracks failed logins from IP addresses. If there are multiple failed logins from a specific IP address within a period of time, the IP address is blocked from accessing any resources in the service for a pre-defined time period.*
  * Insufficient permissions: *The user does not have enough authorization to login to the database. Please ensure that the user is granted the necessary permissions to login.*

* To increase security, the error message that is returned to the client deliberately hides the nature of the authentication error

## **Recommended Documents**

- [DoSGuard](https://docs.microsoft.com/azure/security/fundamentals/infrastructure-sql?WT.mc_id=pid:13491:sid:32745428/#dosguard)
- [Login Errors with state and description](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?WT.mc_id=pid:13491:sid:32745428&view=sql-server-ver15)
