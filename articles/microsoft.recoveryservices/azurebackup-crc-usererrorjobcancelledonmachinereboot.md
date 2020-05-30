<properties
	pageTitle="UserErrorJobCancelledOnMachineReboot"
	description="UserErrorJobCancelledOnMachineReboot"
	infoBubbleText="Job was cancelled because the machine rebooted."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorjobcancelledonmachinereboot"
	diagnosticScenario="azurebackup-crc-usererrorjobcancelledonmachinereboot"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorJobCancelledOnMachineReboot

<!--issueDescription-->
We have identified that your backup operations failed because the VM was rebooted.
<!--/issueDescription-->

## **Recommended Steps**

* Check if the VM was shut down while processes were running
* If yes, then rerun the backup operation
