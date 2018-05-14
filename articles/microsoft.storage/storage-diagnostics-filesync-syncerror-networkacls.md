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

# File Sync failed because the Storage Account has a firewall or virtual network configured

<!--issueDescription-->
File Sync failed because the Storage Account has a firewall or virtual network configured.<br>

Ensure access from all networks to the Storage Account is allowed. Azure File Sync does not yet support [firewalls and virtual networks](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-firewall-and-proxy) for a Storage Account.
<br>

<!--/issueDescription-->