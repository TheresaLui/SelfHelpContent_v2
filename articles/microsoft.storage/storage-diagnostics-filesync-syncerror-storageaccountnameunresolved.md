<properties
pageTitle="Sync error - storage account name resolution
description="Sync error - storage account name resolution"
infoBubbleText="Sync error - storage account name resolution"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncError_StorageAccountNameUnresolved"
diagnosticScenario="Sync error - storage account name resolution"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# File Sync failed with error <!--$ErrorString-->[ErrorString]<!--/$ ErrorString -->: The Storage Account name used could not be resolved

<!--issueDescription-->
Azure Sync failed with error <!--$ErrorString-->[ErrorString]<!--/$ ErrorString -->: The Storage Account name used could not be resolved.

1. Make sure the Storage Account still exists.
2. In the Azure portal, check the Access Control (IAM) on the Storage Account and verify the Storage Sync Service role has access to the Storage Account.
<!--/issueDescription-->