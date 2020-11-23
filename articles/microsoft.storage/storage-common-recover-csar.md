<properties
    pageTitle="Recover deleted Storage Account"
    description="Recover deleted Storage Account Troubleshooting"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storage"
    authors="annayak"
    ms.author="annayak"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32783981,32783979,32783980,32783576"
    resourceTags="recovery"
    productPesIds="15629,16459,16460,16598"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    articleId="d9aafbaf-c810-4df5-92f7-7dc4a8c3d178"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# **Recommended Steps**

## **Self-service Recovery**

**Azure storage now provides a self-service recovery directly from the portal.**

### **Conditions for a storage account to be recoverable:**

- A new storage object with the same name has not been re-created since deletion.
- The storage account was deleted in the last 14 days.
- It is not a classic storage account.

### **Pre-requisites**
- Ensure the Resource Group is created first it it has been deleted.
- Ensure KeyVault key is recovered for accounts with CMK. It's customers resonsibility to ensure CMK is present in KeyVault.<br>

## [**Click Here > Recover a deleted storage account**](data-blade:Microsoft_Azure_Storage.RecoverStorageAccountBlade.subscriptionId.$subscriptionId)