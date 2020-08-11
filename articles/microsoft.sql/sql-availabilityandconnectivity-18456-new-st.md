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

* Login failed with error code 18456 indicates that your packet has reached the Azure SQL services, but was rejected due to one or more of the following reasons:

  * Incorrect / empty passwords
  * Database requested by user does not exist
  * The connections were rejected due to DoS Guard protection
  * Insufficient permissions

* To increase security, the error message that is returned to the client deliberately hides the nature of the authentication error

