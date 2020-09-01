<properties
    pageTitle="Storage Account's AD Object is missing in AD"
    description="Storage Account's AD Object is missing in AD"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="1bd4e937-1518-4489-8a01-8414fcae3799"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Storage Account's AD Object could be missing

## Symptoms
The user attempts to mount and gets prompted for credentials. The user may or may not proceed to type in their credentials and get an error like "the username or password is incorrect"

## Description of Problem
Due to issues within a customer's domain environment, clients may have trouble getting Kerberos tickets to the storage account.

## How to detect

klist get cifs/<storageaccount>.file.core.windows.net

If the error is "The SAM database on the Windows Server does not have a computer account for this workstation trust relationship"
x. Run the following on the domain to validate the object exists:
 
     Get-AzStorageAccountADObject -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
     
y. If the object doesn't exist, rejoin the storage account via PowerShell.

z. If the object exists, take a WireShark trace while reproducing the issue. Escalate the issue through the Ava channel.
