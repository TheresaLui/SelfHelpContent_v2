<properties
    pageTitle="Check ASC to see if AD Auth is enabled on the storage account"
    description="Check ASC to see if AD Auth is enabled on the storage account"
    service="Microsoft.Storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="f2c7cb52-4416-4fe9-9bc4-c426b7628d7b"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Use ASC to verify if the customer has AD Auth enabled on the storage account

Go to storage account resource under ASC resource explorer to verify if the AD Auth feature is enabled on the storage account. 

![ASC](C:\Users\yagohel\Pictures\Screenshot_2.png)

Value "**AD**" for "**Identity-based Directory Service for Azure File Authentication**" property confirms customer has AD Auth enabled on the storage account.