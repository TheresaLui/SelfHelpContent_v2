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

# Error 18456: Login failed

**Error 18456: Login failed**

Error 18456 indicates that Azure SQL DB rejected a login request for one or more of the following reasons:

- Incorrect or empty password: *The client tool / application has incorrect or blank password. Please ensure that you have provided the correct password.*
- Database does not exist: *Please ensure that the connection string has the correct database name.  If you are connecting from a SQL Server Management Studio, click the 'Options' button in the connection dialog to expose additional connection options, and verify that the 'Connection Properties' tab has a "Connect to database" value of default selected.*
- Insufficient permissions: *The user does not have CONNECT permissions to the database. Please ensure that the user is granted the necessary permissions to login.*
- Expired or invalid AAD token: *You might get this error if the token has expired, if the token issuer is invalid, if no object Id is present in the token, if the token signature is incorrect or invalid or if SQL Server was unable to get the token from ADAL.*
- Connections rejected due to DoSGuard protection: *[DoSGuard](https://docs.microsoft.com/azure/security/fundamentals/infrastructure-sql?WT.mc_id=pid:13491:sid:32745428/#dosguard) actively tracks failed logins from IP addresses. If there are multiple failed logins from a specific IP address within a period of time, the IP address is blocked from accessing any resources in the service for a pre-defined time period--even if the password and other permissions are correct.*

* The reason for the login failure is indicated by the State code of the error.  However, the error message that is returned to the client deliberately overrides the state code so as to not give hackers any authentication-related information. Running the connectivity troubleshooter above may return a more detailed message indicating specifically why your logins are failing.


## **Recommended Documents**
- [Login Errors with state and description](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?WT.mc_id=pid:13491:sid:32745428&view=sql-server-ver15)
