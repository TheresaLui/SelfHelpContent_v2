<properties
	pageTitle="UserErrorSkuNotAvaialable"
	description="UserErrorSkuNotAvaialable"
	infoBubbleText="VM creation failed as VM size selected is not available."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorskunotavaialable"
	diagnosticScenario="azurebackup-crc-usererrorskunotavaialable"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error UserErrorSkuNotAvaialable

<!--issueDescription-->
We have identified that your Create New VM restore operation failed because the VM size selected is not available.
<!--/issueDescription-->

## **Recommended Step**
To resolve this issue, use [Restore Disks](https://aka.ms/VMrestore-restore-disk) option to restore. Use the restored disks to create a VM with a different size using PowerShell cmdlets.
