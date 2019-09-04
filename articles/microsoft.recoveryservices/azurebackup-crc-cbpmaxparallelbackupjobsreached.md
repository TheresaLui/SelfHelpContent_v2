<properties
	pageTitle="CBPMaxParallelBackupJobsReached"
	description="CBPMaxParallelBackupJobsReached"
	infoBubbleText="The operation attempted cannot be performed at this time because maximum number of parallel backup jobs are already running."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpmaxparallelbackupjobsreached"
	diagnosticScenario="azurebackup-crc-cbpmaxparallelbackupjobsreached"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error CBPMaxParallelBackupJobsReached

<!--issueDescription-->
We have identified that your backup operation failed because multiple backup operations are triggered which exceeded the maximum allowed parallel backup jobs.
<!--/issueDescription-->

## **Recommended Steps**

The MAB agent can handle only 8 parallel job request from DPM server, however during sync mismatch the DPM sending more than 8 jobs, resulting in the this backup job failure.
To resolve this issue, set the number of parallel jobs up to 5 (less than 8 jobs) by running the below command from the elevated command prompt:

`REG ADD "HKLM\Software\Microsoft\Microsoft Data Protection Manager\Configuration\DPMTaskController\MaxRunningTasksThreshold" /v 6e7c76f4-a832-4418-a772-8e58fd7466cb /t REG_DWORD /d 5 /f`

> [!NOTE]
>  6e7c76f4-a832-4418-a772-8e58fd7466cb is cloud-backup verb-id and this is a fixed value for all the users.
