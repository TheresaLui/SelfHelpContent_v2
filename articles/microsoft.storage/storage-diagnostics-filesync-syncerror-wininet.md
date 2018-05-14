<properties
pageTitle="Sync error - wininet error"
description="Sync error - wininet error"
infoBubbleText="Azure File Sync error - wininet error"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncError_Wininet"
diagnosticScenario="Sync error - wininet error"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **File Sync failed with error <!--$ErrorString-->[ErrorString]<!--/$ErrorString-->  : A connection with the service could not be established.**

<!--issueDescription-->
Azure File Sync failed on Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** with error <!--$ErrorString-->[ErrorString]<!--/$ErrorString-->  : A connection with the service could not be established.<br><br>

1. Check to make sure the server **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** is online.<br>
2. Verify the service 'FileSyncSvc.exe' is not blocked by a [Firewall](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy) on your server.<br>
3. Verify [port 443](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy#ports) is open to outgoing connections.
<br>

<!--/issueDescription-->