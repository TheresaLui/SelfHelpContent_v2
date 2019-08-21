<properties
pageTitle="Unable to create storage account with CMK enabled"
description="Unable to create storage account with Customer Managed Key enabled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_AccountCreationIssue_CMK"
diagnosticScenario="Unable to create storage account with CMK enabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Unable to create storage account with CMK enabled

<!--issueDescription-->

Storage account <!--$ResourceName-->[ResourceName]<!--/$ResourceName--> creation failed at <!--$IssueTime-->[IssueTime]<!--/$IssueTime--> because customer-managed key (CMK) is being enabled without Azure Key Vault (AKV) provisioned. 
<!--/issueDescription-->
Please ensure that [prerequisite for enabling customer-managed keys](https://docs.microsoft.com/en-us/azure/storage/common/storage-encryption-keys-cli?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) are met before enabling it on storage account.

## **Recommended Documents**

* [Configure customer-managed keys for Azure Storage encryption from the Azure portal](https://docs.microsoft.com/azure/storage/common/storage-encryption-keys-portal?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)
* [Configure customer-managed keys for Azure Storage encryption from PowerShell](https://docs.microsoft.com/azure/storage/common/storage-encryption-keys-powershell?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)
* [Configure customer-managed keys for Azure Storage encryption from Azure CLI](https://docs.microsoft.com/en-us/azure/storage/common/storage-encryption-keys-cli?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)

