<properties
    pageTitle="User gets Positional Parameters error while running the PowerShell"
    description="User gets Positional Parameters error while running the PowerShell"
    infoBubbleText="User gets Positional Parameters error while running the PowerShell"
    service="Microsoft.Storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="84471d67-7913-4776-b5b8-1b00feae49c2"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# User gets "Positional Parameters" error while trying to join Storage account to Active Directory Domain 

<!--issueDescription-->
User gets Positional Parameters error while trying to join Storage account to Active Directory Domain
<!--/issueDescription-->

## **Recommended Steps**

When the customer attempts to join an Azure Storage account using the Join-AzStorageAccountforAuth command they get the following error:  


**Error:** "Cannot bind positional parameters because no names were given" 


## **Root Cause/Mitigation**
This error is most likely triggered by a syntax error in the Join-AzStorageAccountforAuth command. Please make sure the customer is running the command exactly as [specified here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-enable#run-join-azstorageaccountforauth). Look for spelling mistakes or any special characters which could have got added while copy pasting the command. If needed, try manually typing the command and see if it helps resolve the issue. 
