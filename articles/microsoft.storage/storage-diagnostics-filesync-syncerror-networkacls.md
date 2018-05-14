<properties
pageTitle="Sync error - network ACLs"
description="Sync error - network ACLs"
infoBubbleText="Sync error - network ACLs"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncError_NetworkACLs"
diagnosticScenario="Sync error - network ACLs"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# File Sync failed because the Storage Account has a Firewall or Virtual network configured

<!--issueDescription-->
File Sync failed on Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** because the Storage Account **<!--$StorageAccountName-->[StorageAccountName]<!--/$StorageAccountName-->** has a Firewall or Virtual Network configured.<br><br>

Ensure access from all networks to the Storage Account is allowed. Azure File Sync does not yet support [Firewalls and Virtual Networks](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-firewall-and-proxy) for a Storage Account. You can check the configuration in the Azure Portal by going to the Storage Account and then clicking on the 'Firewalls and Virtual Networks' tab.<br>

<!--/issueDescription-->