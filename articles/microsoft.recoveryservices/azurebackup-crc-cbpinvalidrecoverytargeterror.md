<properties
	pageTitle="CBPInvalidRecoveryTargetError"
	description="CBPInvalidRecoveryTargetError"
	infoBubbleText="The recovery destination selected for one or more files to be recovered is invalid."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpinvalidrecoverytargeterror"
	diagnosticScenario="azurebackup-crc-cbpinvalidrecoverytargeterror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPInvalidRecoveryTargetError

<!--issueDescription-->
We have identified that your backup operation failed because the scratch space specified does not match with the actual location of the scratch space folder.
<!--/issueDescription-->

## **Recommended Steps**

* To resolve this issue, ensure the actual location of the scratch space folder and the space specified for DPM/MABS is valid and matched
