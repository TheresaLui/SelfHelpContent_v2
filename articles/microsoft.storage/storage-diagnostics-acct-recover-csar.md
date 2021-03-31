<properties
    pageTitle="Recover deleted Storage Account"
    description="Recover deleted Storage Account Troubleshooting"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storage"
    authors="annayak"
    ms.author="annayak"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32783981,32783979,32783980,32783576"
    resourceTags="recovery"
    productPesIds="15629,16459,16460,16598"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    articleId="50bbc8cf-27ea-4359-aacc-9ca621fcb009"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Recover Deleted Storage Account
## **Recommended Steps**
Select the button below to list the storage accounts where best effort recovery is possible. If a storage account doesn't show up on the list, then it can't be recovered anymore as it's purged.<br>

**Note** : All conditions, prerequisites and disclaimer below apply to every recovery attempt.

[Initiate Storage Account Recovery](button-data-context:Microsoft_Azure_Storage.RecoverStorageAccountBlade.subscriptionId.$subscriptionId)​​

##### **Conditions for a storage account to be recoverable**
- A new storage account with the same name has not been re-created since deletion.
- The storage account was deleted in the last 14 days, including today. If the storage account was deleted prior to that, it cannot be recovered.
- It is not a classic storage account.

##### **Prerequisites**
- Ensure that the Resource Group is created first, if it has been deleted.
- Ensure that the KeyVault key is associated with the storage account if it is encrypted with a customer-managed key (CMK). Failing to do so would result in HTTP 403 failures when accessing the endpoints (currently, blob and file) of the recovered account.

##### **Disclaimer**
- There's no guarantee that recovery will always succeed. Recovery is a best effort rather than a guarantee.
- We strongly recommend using a combination of [ARM resource locks](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources) and [Azure RBAC](https://docs.microsoft.com/azure/role-based-access-control/overview) permissions to prevent accidental account deletion.
