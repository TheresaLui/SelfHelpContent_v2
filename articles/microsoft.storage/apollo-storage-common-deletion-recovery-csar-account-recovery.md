<properties
pageTitle="Recover deleted Storage Account Account"
description="Recover deleted Storage Account Apollo Solutions"
ms.author="annayak"
displayOrder=""
articleId="e9b9f540-5337-43b1-9b8f-3a7460f4c2bb"
selfHelpType="Apollo"
supportTopicIds="5bea99a4-5ba9-8f06-ebb9-00ac608021d2,3ba0cdba-5c03-22bf-e777-7f1cc711153c,fa13d9a7-464b-667e-8eb7-1bd0c450476c,d4ac1605-dd7d-12be-317b-6a7210155d52"
productPesIds="15629,16459,16460,16598,16462,16461"
cloudEnvironments="public"
ownershipId="StorageMediaEdge_XStore"
/>

# Troubleshooting authentication and authorization failures using Apollo

## Recover Deleted Storage Account

:::Section Recommended solutions:::

### Initiate Account Recovery
Select the following button to initiate storage account recovery. Make sure the right subscription is selected because the diagnostic runs in the context of the current subscription only.

<span style="color:red">Note</span> : If you intend to recover specific containers, blobs, files, and so on, go back to the **Basics** tab and select **Recover deleted storage data** as the problem subtype instead.

<Insight>
<symptomId>Storage_Account_Recovery_Portal_Insight</symptomId>
<executionText>We are running a quick check to find recently deleted storage account</executionText>
<timeoutText>We stopped the check, as it was taking too long</timeoutText>
<noResultText>No recoverable storage account was found. If you intend to recover specific containers, blobs, files, and so on, go back to the "Basics" tab and select "Recover deleted storage data" as the problem subtype instead.</noResultText>
<additionalInputsReq>false</additionalInputsReq>
</Insight>

### <span style="color:red">**Conditions for a storage account to be recoverable:**

- A new storage object with the same name has not been re-created since deletion.
- The storage account was deleted in the last 14 days, including today. If the storage account was deleted prior to that, it cannot be recovered.
- It is not a classic storage account.

### <span style="color:red">**Prerequisites:**

- Ensure that the Resource Group is created first, if it has been deleted.
- Ensure that the KeyVault key is associated with the storage account if it is encrypted with a customer-managed key (CMK). Failing to do so would result in HTTP 403 failures when accessing the endpoints (currently, blob and file) of the recovered account.

### <span style="color:red">**Disclaimer:**

- There's no guarantee that recovery will always succeed. Recovery is a best effort rather than a guarantee.
- We strongly recommend using a combination of [ARM resource locks](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources) and [Azure RBAC](https://docs.microsoft.com/azure/role-based-access-control/overview) permissions to prevent accidental account deletion.
