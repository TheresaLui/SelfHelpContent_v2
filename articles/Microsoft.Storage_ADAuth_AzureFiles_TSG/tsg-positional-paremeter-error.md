<properties
    pageTitle="User gets Positional Parameters error while running the PowerShell"
    description="User gets Positional Parameters error while running the PowerShell"
    service="Microsoft.Storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public"
    articleId="84471d67-7913-4776-b5b8-1b00feae49c2"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# User gets "Positional Parameters" error while trying to join Storage account to Active Directory Domain 

## Symptoms
When the customer attempts to join an Azure Storage account using the Join-AzStorageAccountforAuth command they get the following error:  

![](Screenshots\PositionalParameters.png)

**Error:** "Cannot bind positional parameters because no names were given" 

## Root Cause/Mitigation
This error is most likely triggered by a syntax error in the Join-AzStorageAccountforAuth command.   

**Note:** In the original public document for enabling this feature there was a misspelled parameter this has since been updated.  It is possible that the customer saved the command from the public documentation prior to the update.  In the original document "-OrganizationalUnitName" was incorrectly shown as "-OrganizationUnitName".  OrganizationalUnitName is the correct spelling.