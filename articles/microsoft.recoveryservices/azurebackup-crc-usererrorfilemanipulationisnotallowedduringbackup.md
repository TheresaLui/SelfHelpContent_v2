<properties
	pageTitle="UserErrorFileManipulationIsNotAllowedDuringBackup"
	description="UserErrorFileManipulationIsNotAllowedDuringBackup"
	infoBubbleText="Backup, file manipulation operations (such as ALTER DATABASE ADD FILE) and encryption changes on a database must be serialized."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorfilemanipulationisnotallowedduringbackup"
	diagnosticScenario="azurebackup-crc-usererrorfilemanipulationisnotallowedduringbackup"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorFileManipulationIsNotAllowedDuringBackup

<!--issueDescription-->
We have identified that backup operation failed because another process was manipulating files. SQL server is not able to run backup in parallel with that operation.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, when Backup operation is in progress:

* Do not add or drop files to a database
* Do not shrink files
