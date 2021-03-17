<properties
	pageTitle="Queue time is high"
	description="Queue time is high"
	service=""
	resource=""
	authors="TestAuthor"
	ms.author="TestAuthor"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9aae642e-fa22-48c2-be68-5b5fd04af60a"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Queue time is high

<!--issueDescription-->

There might be a lag between taking the snapshot and copying it to vault.<br>
<br>
At peak times, it can take up to eight hours for backups to be processed. The backup time for a VM will be less than 24 hours for the daily backup.<br>
<br>
Follow best practices: <br>
<br>
Modify the default schedule times that are set in a policy. For example, if the default time in the policy is 12:00 AM, increment the timing by several minutes so that resources are optimally used.<br>
<!--/issueDescription-->

# Recommended Documents
[Backup and restore considerations](https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-introduction#backup-and-restore-considerations)
