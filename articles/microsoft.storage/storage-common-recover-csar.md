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

Azure storage now provides users a self-service storage account recovery capability.

 ### [**Click Here > Recover Deleted Storage Account**](data-blade:Microsoft_Azure_Storage.RecoverStorageAccountBlade.subscriptionId.$subscriptionId)

### <span style="color:maroon">**Conditions for a storage account to be recoverable:**

- A new storage object with the same name has not been re-created since deletion.
- The storage account was deleted in the last 14 days including today. If was deleted prior to that, it can't be recovered.
- It is not a classic storage account.

### <span style="color:maroon">**Prerequisites:**
- Ensure the Resource Group is created first, if it has been deleted.
- Ensure KeyVault key is recovered first for storage accounts with CMK.<br>

### <span style="color:maroon">**Disclaimer:**
- It's best effort and not a guarantee that recovery will always succeed.
- We strongly recommend to use a combination of [ARM resource locks](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources ) and [Azure RBAC](https://docs.microsoft.com/azure/role-based-access-control/overview) permissions to prevent accidental account deletion.

