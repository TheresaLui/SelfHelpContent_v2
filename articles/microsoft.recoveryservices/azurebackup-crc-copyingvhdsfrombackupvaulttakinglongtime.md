<properties
	pageTitle="CopyingVHDsFromBackUpVaultTakingLongTime"
	description="CopyingVHDsFromBackUpVaultTakingLongTime"
	infoBubbleText="Backup failed because of system file errors.This could be due to one or more actions pending on this server"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-copyingvhdsfrombackupvaulttakinglongtime"
	diagnosticScenario="azurebackup-crc-copyingvhdsfrombackupvaulttakinglongtime"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error CopyingVHDsFromBackUpVaultTakingLongTime

<!--issueDescription-->
We have identified that your backup operation is taking longer than expected.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, try the following: 

* Consider staggering backup times of involved VMs by about an hour or so to see if issue resolves. Stagger more if required.
* Consider limiting on the number of disks per storage account relative to how heavily the disks are being accessed. 
* If protected disks that are undergoing incremental backup have a daily churn of more than 200 GB, backup can take a long time (more than eight hours) to complete.
* If changes are spread out and fragmented across a disk, backup operation will be slower. Consider performance defragmentation.

## **Recommended Document**
For more information, refer [Backup performance](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#backup-performance) and [Best practices](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices).
