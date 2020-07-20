<properties
    pageTitle="Hybrid module install issues or Join issues?"
    description="Hybrid module install issues or Join issues?"
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
    articleId="5e97723d-3c6c-4d3b-af06-172f5d3f19f5"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Check if the customer is facing issues with PowerShell module installation or with domain joining the storage account. 

* PowerShell Module Installation issues refer to issues customers get while running **".\CopytoPSPath.ps1"** or **"Import-Module -name AzFilesHybrid"** command. This could also mean issues they get while running into manual installation steps as [specified here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-enable#checking-environment). 

* Domain Join issues refer to issues customers get while running **"Join-AzStorageAccountforAuth"** command or the issues customers face while domain joining storage account manually as [specified here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-enable#option-2-manually-perform-the-enablement-actions)
