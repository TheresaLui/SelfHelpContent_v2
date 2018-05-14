<properties
pageTitle="Sync error - storage account name resolution"
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

# File Sync failed with error <!--$ErrorString-->[ErrorString]<!--/$ErrorString-->: The Storage Account name used could not be resolved

<!--issueDescription-->
Azure File Sync failed on Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** with error <!--$ErrorString-->[ErrorString]<!--/$ErrorString-->: The Storage Account name used could not be resolved.<br><br>

1. Make sure the Storage Account **<!--$StorageAccountName-->[StorageAccountName]<!--/$ServerEndpointName-->** still exists.<br>
2. In the Azure portal under the Storage Account, go to the 'Access Control (IAM)' tab and verify the Storage Sync Service role has access to the Storage Account. The scope for 'Hybrid File Sync Service' must be set to 'This Resource'.
<!--/issueDescription-->
