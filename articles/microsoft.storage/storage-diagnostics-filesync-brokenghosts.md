<properties
pageTitle="FileSync broken tiered files"
description="There are broken tiered files on the server endpoint"
infoBubbleText="See details on right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncPerItemError_BrokenGhosts"
diagnosticScenario="FileSync broken ghosts"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **File Sync failed to upload <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> broken tiered file(s) for Server Endpoint '<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->'**

<!--issueDescription-->
Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** contains <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> broken tiered file(s). These tiered files have been rendered non-functional as the server endpoint was deleted without first recalling all the tiered data to the server. These files cannot be synced, and must be cleaned up. Please follow the troubleshooting steps [documented here](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot#i-deleted-and-recreated-my-server-endpoint-and-now-files-arent-syncing).
<br> 
<!--/issueDescription-->
