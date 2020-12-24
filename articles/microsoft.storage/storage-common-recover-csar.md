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
# Customer-Controlled Storage Account Recovery
## **Recommended Steps**

Azure Storage now provides users a self-service storage account recovery capability.

### <span style="color:maroon">**Conditions for a storage account to be recoverable:**

- A new storage object with the same name has not been re-created since deletion.
- The storage account was deleted in the last 14 days, including today. If the storage account was deleted prior to that, it can't be recovered.
- It is not a classic storage account.

### <span style="color:maroon">**Prerequisites:**
- Ensure that the Resource Group is created first, if it has been deleted.
- Ensure that the KeyVault key is recovered first for storage accounts with CMK.<br>

### <span style="color:maroon">**Disclaimer:**
- There's no guarantee that recovery will always succeed. Recovery is a best effort rather than a guarantee.
- We strongly recommend using a combination of [ARM resource locks](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources) and [Azure RBAC](https://docs.microsoft.com/azure/role-based-access-control/overview) permissions to prevent accidental account deletion.

<a href="data-blade:Microsoft_Azure_Storage.RecoverStorageAccountBlade.subscriptionId.$subscriptionId"><button type="button" style="background-color:#1E90FF;color:white;width:330px; height:40px;"><b>Customer-Controlled Storage Account Recovery</button></a>
