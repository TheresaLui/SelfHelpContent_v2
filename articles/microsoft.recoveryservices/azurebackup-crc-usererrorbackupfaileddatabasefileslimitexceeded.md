<properties
	pageTitle="UserErrorBackupFailedDatabaseFilesLimitExceeded"
	description="UserErrorBackupFailedDatabaseFilesLimitExceeded"
	infoBubbleText="Backup failed as the number of files in the database exceeded the limit. Databases with number of files greater than 1000 are not supported"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbackupfaileddatabasefileslimitexceeded"
	diagnosticScenario="azurebackup-crc-usererrorbackupfaileddatabasefileslimitexceeded"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorBackupFailedDatabaseFilesLimitExceeded

<!--issueDescription-->
We have identified that your log backup is failing because the number of files in the database is greater than 1000 (the maximum supported limit).  
<!--/issueDescription-->

## **Recommended Steps**

* [Reduce the number of files in the database](https://go.microsoft.com/fwlink/?linkid=2077170) for the backup operation to complete successfully
