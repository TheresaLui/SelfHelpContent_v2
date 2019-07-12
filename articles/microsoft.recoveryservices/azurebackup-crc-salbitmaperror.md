<properties
	pageTitle="SalBitmapError"
	description="SalBitmapError"
	infoBubbleText="Unable to find changes in a file. This could be due to various reasons. Please retry the operation"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-salbitmaperror"
	diagnosticScenario="azurebackup-crc-salbitmaperror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error SalBitmapError

<!--issueDescription-->
We have identified that your operation failed because MARS agent was unable to detect chnages in file.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the below steps:

1. If the issue transient then subsequent retry operation could resolve the issue
2. Ensure the VM has [latest backup agent](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)
3. Check event logs for storage issues potentially impacting backup scratch space, resolve them, and retry the backup operation
