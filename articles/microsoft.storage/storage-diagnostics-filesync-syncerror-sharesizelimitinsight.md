<properties
pageTitle="Sync error - share size limit reached"
description="Sync error - share size limit reached"
infoBubbleText="Sync error - share size limit reached"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncError_ShareSizeLimitReached"
diagnosticScenario="Sync error - share size limit reached"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# File Sync failed because the Azure File Share storage limit has been reached

<!--issueDescription-->

Azure File Sync failed because the File Share **<!--$CloudEndpointName-->[CloudEndpointName]<!--/$CloudEndpointName-->** exceeded the [maximum capacity limit (5 TB)](https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits) in Storage Account **<!--$StorageAccountName-->[StorageAccountName]<!--/$StorageAccountName-->** based on its current size of  <!--$AFSShareSize-->[AFSShareSize]<!--/$AFSShareSize--> TB.<br>

Consider making each subfolder you are currently syncing a Server Endpoint in a separate Sync Group. This way each subfolder will sync to individual Azure File Shares. 
<!--/issueDescription-->
