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

# **File Sync failed to upload <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount-->  files as they contain one or more unsupported characters for Server Endpoint <!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->**

<!--issueDescription-->
These Server Endpoints are failing to upload files as they contain one or more unsupported characters: 
<br>
<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->: <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> files failing to sync
<br>

For these files to sync, you must remove or rename the characters at fault from the respective files. 
To do so, run the "FileSyncErrorsReport.ps1" PowerShell script (located in the agent installation directory of the Refresh 2 or GA Azure File Sync agent) to identify files that failed to sync. 
Individual files can fail to sync for various reasons; you should look for error codes 0x7b and 0x8007007b to find the ones that are failing to sync due to unsupported characters. 
The ItemPath field tells you the location of the file in relation to the root sync directory. Note that PowerShell will likely print these characters as question marks or empty rectangles since most of these characters have no standard visual encoding. 
For more information, see [this document](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot#handling-unsupported-characters).
