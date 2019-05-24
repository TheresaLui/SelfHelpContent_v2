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
	cloudEnvironments="public"
/>

# Error UserErrorCannotFindServerCertificateWithThumbprint

<!--issueDescription-->
We have identified that your restore job failed because Azure backup cannot find the server certificate with the thumbprint on the target. This is mostly like due to Master database on the destination instance doesn't have a valid encryption thumbprint.
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue follow this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorcannotfindservercertificatewiththumbp).
