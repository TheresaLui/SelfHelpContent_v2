<properties
	pageTitle="sqlerror3204"
	description="sqlerror3204"
	infoBubbleText="Generic SQL User Error."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-sqlerror3204"
	diagnosticScenario="azurebackup-crc-sqlerror3204"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# SQL ErrorNumber: 3204 The backup or restore was aborted

<!--issueDescription-->
We have identified that your backup operation was aborted. This could be due to high IOPS or hitting throttling limit while taking backup.
<!--/issueDescription-->

## **Recommended Document**

Check the Event viewer for error message 'The I/O operation has been aborted because of either a thread exit or an application request'.

To resolve this issue, decrease the throughput by following the below steps:

- Distribute backup traffic, consider backing up different DBs at different times of the day and make sure the times don't overlap.
- You can throttle the rate at which the backup policy runs to minimize the impact on a SQL Server instance. for more information see, [Control concurrent backups run on the SQL server](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-control-how-many-concurrent-backups-run-on-the-sql-server)
