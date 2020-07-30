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

## **Recommended Steps**

### Error 18456: Login failed for user X

* Login failures may occur commonly for one or more of the following reasons -
  * Incorrect / empty passwords
  * Database requested by user does not exist
  * The connections were rejected due to DoS Guard protection
  * Insufficient permissions


* Troubleshoot this error using the [Azure SQL Database Connectivity troubleshooter](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database#unable-to-log-in-to-the-server-errors-18456-40531?WT.mc_id=pid:13491:sid:32745425/) <br>
