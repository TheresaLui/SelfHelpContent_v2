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

**Error 40532: Cannot open server {servername} requested by the login. The login failed.**

## **Recommended Steps**

Error 40532 is usually related to one of the following scenarios:

1. The username (or login) contains the '@' symbol (e.g., john@mydomain.com).  If the {servername} value in the error references "mydomain.com" then you are encountering this scenario.  See [Handling Error 40532](https://techcommunity.microsoft.com/t5/azure-database-support-blog/providing-the-server-name-explicitly-in-user-names-for-azure-sql/ba-p/368942?WT.mc_id=pid:13491:sid:32745429/) for how to handle this scenario.

1. You use VNet firewall rules. This occurs when a VNet firewall rule was set for one subnet and the user is trying to access from another subnet on the same VNet. It is important to understand the configuration is per subnet inside a VNet and not the whole VNet. Please ensure the same to fix the issue.
