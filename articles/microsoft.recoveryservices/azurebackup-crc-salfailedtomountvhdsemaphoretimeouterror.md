<properties
	pageTitle="SalFailedToMountVhdSemaphoreTimeoutError"
	description="SalFailedToMountVhdSemaphoreTimeoutError"
	infoBubbleText="Backup could not be started because of virtual hard drive named %FileName could not be mounted"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-salfailedtomountvhdsemaphoretimeouterror"
	diagnosticScenario="azurebackup-crc-salfailedtomountvhdsemaphoretimeouterror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error SalFailedToMountVhdSemaphoreTimeoutError

<!--issueDescription-->
We have identified that your backup operation failed because the backup is unable to access the network.
<!--/issueDescription-->

## **Recommended Steps**

* [Check if the server time is correctly synced to resync system time](https://docs.microsoft.com/azure/virtual-machines/windows/time-sync)
