<properties
pageTitle="One or more servers have recalled a large amount of data"
description="One or more servers have recalled a large amount of data"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="jeffpatt"
ms.author="passap"
displayOrder=""
articleId="FileSync_RecallVolumeHigh"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# One of more Azure File Sync servers have recalled a large amount of data. 

<!--issueDescription-->
The following server(s) under the Storage Sync Service **<!--$StorageSyncServiceName-->[StorageSyncServiceName]<!--/$StorageSyncServiceName-->** have recalled a large amount of data in the time window from **<!--$startTime-->[startTime]<!--/$startTime-->** to **<!--$endTime-->[endTime]<!--/$endTime-->**. Below is the list of servers with high recall volume in GB: <br><!--$ServerNameList-->[ServerNameList]<!--/$ServerNameList-->.

If the recall activity is not expected, follow the guidance in the recommended steps section.
<!--/issueDescription-->

## **Recommended steps**

Antivirus, backup, and other applications that read large numbers of files cause unintended recalls unless they respect the offline attribute and skip reading the content of those files. Skipping offline files for products that support this option helps avoid unintended recalls during operations like antivirus scans or backup jobs.

Consult with your software vendor to learn how to configure their solution to skip reading offline files.

Unintended recalls might also occur in other scenarios, like when you are browsing files in File Explorer. Opening a folder that has cloud-tiered files in File Explorer on the server might result in unintended recalls. This is even more likely if an antivirus solution is enabled on the server. 

To help identify the application that's causing recalls on the server, use [Process Monitor](https://docs.microsoft.com/sysinternals/downloads/procmon).
