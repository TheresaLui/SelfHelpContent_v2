<properties
pageTitle="Sync error - invalid characters"
description="Sync is failing for some files because they contain unsupported characters"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncPerItemError_InvalidCharacters"
diagnosticScenario="Sync error - invalid characters"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **File Sync failed to upload <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> file(s) due to unsupported characters for Server Endpoint <!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->**

<!--issueDescription-->
These Server Endpoints failed to upload files that contain one or more unsupported characters: 
<br>
<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->: <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> file(s) failing to sync
<br>

For these files to sync, you must remove or rename the files with unsupported characters. 
See [this document](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cportal#how-do-i-see-if-there-are-specific-files-or-folders-that-are-not-syncing) for details on unsupported characters and how to identify the files.
