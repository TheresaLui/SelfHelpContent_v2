<properties
pageTitle="Sync error - cannot access external storage account"
description="Sync error - cannot access external storage account"
infoBubbleText="Sync error - cannot access external storage account"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncError_CannotAccessExternalStorageAccount"
diagnosticScenario="Sync error - cannot access external storage account"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **Sync failed with error [<!--$ErrorString-->[ ErrorString]<!--/$ ErrorString -->  :Sync can't access the Azure File Share specified in the Cloud Endpoint.**

<!--issueDescription-->

1. Make sure the Azure file share still exists.
2. Ensure the Azure subscription containing the file share is not suspended.
3. Ensure access from all networks to the storage account is allowed. Azure File Sync does not yet support firewalls and virtual networks for a storage account.
4. Check the Role Based Access Control list on the Storage Account. It must include list key permissions for Azure File Sync.

Regards,<br>
Microsoft Azure Team

<!--/issueDescription-->