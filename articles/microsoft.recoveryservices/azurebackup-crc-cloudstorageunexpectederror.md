<properties
	pageTitle="CloudStorageUnexpectedError"
	description="CloudStorageUnexpectedError"
	infoBubbleText="Storage service unexpected error"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cloudstorageunexpectederror"
	diagnosticScenario="azurebackup-crc-cloudstorageunexpectederror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CloudStorageUnexpectedError

<!--issueDescription-->
## We have identified that backup operation was failed because a Protection Group was created with a special character (such as @#$/\)
<!--/issueDescription-->

## **Recommended Steps**

Protection Groups (PG) with special characters are currently not supported for backup. If any PG has a special character, then the sync operation will fail leading to portal not consistent with on-premise server state.

To resolve this issue, rename the PG (without special characters) and restart the agent service by following the below steps:

* Go to **Run** > **services.msc**, in the **Services** window, stop the service Microsoft Azure Recovery Services Management Agent
* Go to the folder **<Microsoft Azure Recovery Services Agent>** under **Program Files** in your system drive and delete **checkpoint Folder**
* Rename the **Protection group** and ensure it doesn't have any special characters
* Go to **Run** > **services.msc**, in the **Services** window, start the service **Microsoft Azure Recovery Services Management Agent**
* The resync operation will be triggered, and all the artifacts should be reflected in the portal within 30 minutes
