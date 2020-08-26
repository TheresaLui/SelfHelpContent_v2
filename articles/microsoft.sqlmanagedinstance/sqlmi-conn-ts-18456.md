<properties
    pageTitle="Error 18456: Login failed"
    description="Error 18456: Login failed"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32746123"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="3859900D-B935-4C93-98A8-EA8F7BE3165E"
    ownershipId="AzureData_AzureSQLMI"
/>

# Error 18456: Login failed

**Error 18456: Login failed**

Error 18456 indicates that Azure SQL Managed Instance rejected a login request for one or more of the following reasons:

- Incorrect or empty password: *The client tool / application has incorrect or blank password. Please ensure that you have provided the correct password.*
- Database does not exist: *Please ensure that the connection string has the correct database name.  If you are connecting from a SQL Server Management Studio, click the 'Options' button in the connection dialog to expose additional connection options, and verify that the 'Connection Properties' tab has a "Connect to database" value of default selected.*
- Insufficient permissions: *The user does not have CONNECT permissions to the database. Please ensure that the user is granted the necessary permissions to login.*
- Expired or invalid AAD token: *You might get this error if the token has expired, if the token issuer is invalid, if no object Id is present in the token, if the token signature is incorrect or invalid or if SQL Server was unable to get the token from ADAL.*

The reason for a login failure is indicated by the State code of the error.  However, the error message that is returned to the client deliberately overrides the state code so as to not give hackers any authentication-related information. Running the diagnostics (above) may return a more detailed message indicating specifically why your logins are failing.


## **Recommended Documents**
[Login Errors with state and description](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error)
