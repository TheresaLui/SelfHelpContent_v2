<properties
	pageTitle="CBPSendDataFailure"
	description="CBPSendDataFailure"
	infoBubbleText="The operation failed because of a protection agent failure"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpsenddatafailure.md"
	diagnosticScenario="azurebackup-crc-cbpsenddatafailure.md"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPSendDataFailure

<!--issueDescription-->
We have identified that your backup operation failed because of a metadata validation failure or previous job still running. 
<!--/issueDescription-->

## **Recommended Steps**

* Check if there is another scheduled backup job that is still running
* If you are using antivirus on the protected machine, then add [necessary exclusion rules](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#another-process-or-antivirus-software-blocking-access-to-cache-folder)
* Restart the MARS agent and retry the backup operation

