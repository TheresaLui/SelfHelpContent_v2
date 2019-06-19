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
	cloudEnvironments="public"
/>

# Error UserErrorJobCancelledOnMachineReboot

<!--issueDescription-->
We have identified that your backup operations failed because the VM was rebooted.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue check if the VM was shutdown while processes were running, if yes then rerun the backup operation.
