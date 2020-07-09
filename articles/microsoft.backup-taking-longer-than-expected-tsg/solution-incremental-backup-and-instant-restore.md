<properties
	pageTitle="Incremental backup and instant restore"
	description="Incremental backup and instant restore"
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
	articleId="0403c531-eb0e-42bd-8f1e-36017e3c6ed3"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Incremental backup and instant restore

<!--issueDescription-->

In an incremental backup, Azure Backup determines the changes by calculating the checksum of the block. If a block is changed, it's marked for transfer to the vault. The service analyzes the identified blocks to attempt to further minimize the amount of data to transfer. After evaluating all the changed blocks, Azure Backup transfers the changes to the vault.
<br>
If churn shown here is more than (2-5% of original disk size) or number of changed blocks is really high, then backups can be slow. But still depending upon scenario we should be able to complete backup.<br>
<br>
Instant restore will allow backups to keep running while copy or other job is still  happening. <br>
<br>
Currently, the backup job consists of two phases:<br>
<br>
1. Taking a VM snapshot.<br>
2. Transferring a VM snapshot to the Azure Recovery Services vault.<br>

A recovery point is considered created only after phases 1 and 2 are completed. As a part of this upgrade, a recovery point is created as soon as the snapshot is finished and this recovery point of snapshot type can be used to perform a restore using the same restore flow. 


<!--/issueDescription-->

## Recommended Documents

1. [Backup instant restore](https://docs.microsoft.com/en-us/azure/backup/backup-instant-restore-capability)
