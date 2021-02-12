<properties
	pageTitle="Backup considerations"
	description="Backup considerations"
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
	articleId="dcb81262-7cd3-4c68-9262-35c21b996187"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Backup considerations

<!--issueDescription-->

1. Scheduling: To reduce backup traffic, back up different VMs at different times of the day and make sure the times don't overlap. Backing up VMs at the same time causes traffic jams.
2. Preparing backups: Keep in mind the time needed to prepare the backup. The preparation time includes installing or updating the backup extension and triggering a snapshot according to the backup schedule.
3. Data transfer: Consider the time needed for Azure Backup to identify the incremental changes from the previous backup.
    1. In an incremental backup, Azure Backup determines the changes by calculating the checksum of the block. If a block is changed, it's marked for transfer to the vault. 
    2. The service analyzes the identified blocks to attempt to further minimize the amount of data to transfer. 
    3. After evaluating all the changed blocks, Azure Backup transfers the changes to the vault.


<!--/issueDescription-->

## Recommended Documents

1. [Backup and restore considerations](https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-introduction#backup-and-restore-considerations)