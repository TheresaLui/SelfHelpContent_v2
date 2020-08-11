<properties
    pageTitle="Cannot open server requested by the login"
    description="Cannot open server requested by the login"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745429"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="3A2EF1AF-EC78-47A6-898B-4EA904F08D2A"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Cannot open server requested by the login

## **Recommended Steps**

<br>

The error 40532 occurs due to one of the following scenarios:

<br>

* Scenario 1: When an invalid server name or username used to connect to the database. For example, if the username includes the '@' symbol then any characters after the '@' symbol will be considered as a part of the server name and will fail with error code 40532 "Cannot open server requested by the login". To troubleshoot this error, please follow the [instructions here](https://techcommunity.microsoft.com/t5/azure-database-support-blog/providing-the-server-name-explicitly-in-user-names-for-azure-sql/ba-p/368942).

<br>

* Scenario 2: When using VNet firewall rules configuration to connect to the database. This can occur when VNet firewall rule was set for one subnet and the user is trying to access from another subnet on the same VNet. It is important to understand the configuration is per subnet inside a VNet and not the whole VNet. Please ensure the same to fix the issue. <br>
