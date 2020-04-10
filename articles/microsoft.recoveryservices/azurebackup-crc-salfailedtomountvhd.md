<properties
	pageTitle="SalFailedToMountVhd"
	description="SalFailedToMountVhd"
	infoBubbleText="Backup could not be started because of virtual hard drive named %FileName could not be mounted"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-salfailedtomountvhd"
	diagnosticScenario="azurebackup-crc-salfailedtomountvhd"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error SalFailedToMountVhd

<!--issueDescription-->
We have identified that your backup operation failed because the MARS agent is not able to mount the metadata VHD (stored in scratch space).
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the below steps:

* Ensure the scratch space configured for backup is located in an unencrypted and uncompressed folder
* Restart Virtual Disk service and retry backup operation
