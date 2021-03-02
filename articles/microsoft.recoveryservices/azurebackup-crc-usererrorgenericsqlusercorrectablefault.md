<properties
	pageTitle="UserErrorGenericSQLUserCorrectableFault"
	description="UserErrorGenericSQLUserCorrectableFault"
	infoBubbleText="Generic SQL User Correctable Error."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorgenericsqlusercorrectablefault"
	diagnosticScenario="azurebackup-crc-usererrorgenericsqlusercorrectablefault"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorGenericSQLUserCorrectableFault

<!--issueDescription-->
We have identified that your operation failed because of an underlying issue with the SQL Server.  
<!--/issueDescription-->

## **Recommended Document**

To solve this issue, refer to additional details section for recommendations specific to SQL Server to resolve the SQL System Errors. <br>Follow the link for more information: <https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/cc645603(v=sql.105)>.

**Common error code** : **SQL ErrorNumber: 3204 The backup or restore was aborted**

Check the Event viewer for error message "The I/O operation has been aborted because of either a thread exit or an application request". This could be due to high IOPS or hitting throttling limit while taking backup.

To resolve this issue, decrease the throughput by following the below steps:

- Distribute backup traffic, consider backing up different DBs at different times of the day and make sure the times don't overlap.
- You can throttle the rate at which the backup policy runs to minimize the impact on a SQL Server instance. for more information see, [Control concurrent backups run on the SQL server](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-control-how-many-concurrent-backups-run-on-the-sql-server)
