<properties
	pageTitle="UserErrorLatestFullPitIsOld"
	description="UserErrorLatestFullPitIsOld"
	infoBubbleText="Latest full Pit is very old. Will force create a Full Pit."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorlatestfullpitisold"
	diagnosticScenario="azurebackup-crc-usererrorlatestfullpitisold"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error UserErrorLatestFullPitIsOld

<!--issueDescription-->
We have identified that the log backup failed because the data source's of the  recovery model has changed since the last successful backup.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue perform the below steps based on the type of backup and retry the operation.

* If this error occur during scheduled backup then Azure Backup service will Autoheal this issue with a full backup. 
* In case of on-demand back, trigger a full backup.
