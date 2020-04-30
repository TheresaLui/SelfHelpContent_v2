<properties
	pageTitle="UserErrorCannotFindServerCertificateWithThumbprint"
	description="UserErrorCannotFindServerCertificateWithThumbprint"
	infoBubbleText="Database with same name already exists at the target location."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorcannotfindservercertificatewiththumbprint"
	diagnosticScenario="azurebackup-crc-usererrorcannotfindservercertificatewiththumbprint"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorCannotFindServerCertificateWithThumbprint

<!--issueDescription-->
We have identified that your restore job failed because Azure Backup cannot find the server certificate with the thumbprint on the target. This is mostly like due to the Master database on the destination instance not having a valid encryption thumbprint.
<!--/issueDescription-->

## **Recommended Document**

* To resolve this issue follow this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorcannotfindservercertificatewiththumbprint)
