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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPMaxParallelBackupJobsReached

<!--issueDescription-->
We have identified that your backup operation failed because multiple backup operations were triggered, which exceeded the maximum allowed parallel backup jobs.
<!--/issueDescription-->

## **Recommended Steps**

The MAB agent can handle a maximum of 8 parallel job requests from DPM server. However, during a sync mismatch, the DPM can send more than 8 jobs, which will result in a backup job failure. 

To resolve this issue, we recommend setting the maximum number of parallel jobs to **5** by running the below command from the elevated command prompt:

`REG ADD "HKLM\Software\Microsoft\Microsoft Data Protection Manager\Configuration\DPMTaskController\MaxRunningTasksThreshold" /v 6e7c76f4-a832-4418-a772-8e58fd7466cb /t REG_DWORD /d 5 /f`

**Note**: `6e7c76f4-a832-4418-a772-8e58fd7466cb` is the cloud backup verb-id, and is a fixed value for all users.
