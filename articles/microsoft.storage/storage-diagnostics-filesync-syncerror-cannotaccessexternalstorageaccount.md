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

# **File Sync failed with error [<!--$ErrorString-->[ ErrorString]<!--/$ ErrorString -->  : Sync cannot access the Azure File Share specified in the Cloud Endpoint.**

<!--issueDescription-->
Sync failed because it cannot access the Azure File Share specified in the Cloud Endpoint.

1. Verify the Azure File Share still exists
2. Ensure the Azure subscription containing the File Share is not suspended
3. Ensure access from all networks to the Storage Account is allowed. Azure File Sync does not yet support [firewalls and virtual networks](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-firewall-and-proxy) for a Storage Account. You can check the configuration in the Azure portal by going to the Storage Account and then clicking on the <!--'Firewalls and virtual networks' tab [Is the only to check for #3 is firewall & VNet? If so, please remove the statement about "ensure access from all network..."]-->
4. In the Azure portal, check the Access Control (IAM) on the Storage Account and verify the Storage Sync Service role has access to the Storage Account

<!--/issueDescription-->