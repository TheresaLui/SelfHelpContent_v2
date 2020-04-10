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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorLatestFullPitIsOld

<!--issueDescription-->
We have identified that the log backup has failed, because the data sources of the recovery model have changed since the last successful backup.
<!--/issueDescription-->

## **Recommended Steps**

* If this error occurs during a scheduled backup, the Azure Backup Service will auto-heal this issue with a full backup 
* In case of an on-demand backup, manually trigger a full backup
