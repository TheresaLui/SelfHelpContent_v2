<properties
	pageTitle="Initial backup and disk added"
	description="Initial backup and disk added"
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
	articleId="2bc1d966-431c-4a90-a9b2-e53ad06fd44d"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Initial backup and disk added

<!--issueDescription-->

Dear Customer,

Although the total backup time for incremental backups is less than 24 hours, that might not be the case for the first backup. The time needed for the initial backup will depend on the size of the data and when the backup is processed. Similarly this will happen if a VM is undergoing incremental backup and a new disk is added, the backup time will increase. The total backup time might last more than 24 hours because of initial replication of the new disk along with delta replication of existing disks.


Thank you

## Recommended Documents
https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-introduction#backup-and-restore-considerations
https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-introduction#backup-performance

<!--/issueDescription-->

