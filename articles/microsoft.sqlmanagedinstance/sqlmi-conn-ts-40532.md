<properties
    pageTitle="Error 40532: Cannot open server y requested by the login"
    description="Error 40532: Cannot open server y requested by the login"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32746124"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="3A2EF1AF-EC78-47A6-898B-4EA904F08D2A"
    ownershipId="AzureData_AzureSQLMI"
/>

# Cannot open server requested by the login

**Error 40532: Cannot open server {servername} requested by the login. The login failed.**

## **Recommended Steps**

Error 40532 is usually related to one of the following scenarios:

1. The username (login) contains the '@' symbol (e.g., a login of the form "user@mydomain.com").  If the {servername} value shown in the error is "mydomain.com" then you are encountering this scenario.  See [Handling Error 40532](https://techcommunity.microsoft.com/t5/azure-database-support-blog/providing-the-server-name-explicitly-in-user-names-for-azure-sql/ba-p/368942) for how to handle this.
