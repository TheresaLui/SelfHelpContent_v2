<properties
		pageTitle="Azure Backup SQL Config failures"
		description="Azure Backup SQL Config failures"
		service="microsoft.recoveryservices"
		resource="vaults"
		authors="srinathv"
		ms.author="srinathv"
		displayOrder=""
		selfHelpType="generic"
		supportTopicIds="32605793"
		resourceTags=""
		productPesIds="15207"
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="3534cf32-a14c-4ba9-83ab-650f9005b548"
	ownershipId="StorageMediaEdge_Backup"
/>
# Azure Backup SQL Config failures

## **Recommended Steps**

- **Perform this step first:** To successfully configure SQL backup, ensure that all the [prerequisites](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#prerequisites) are met

**Common error codes**
- **UserErrorVMInternetConnectivityIssue** - Establish network connectivity to Azure Backup services as described in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#establish-network-connectivity). If the issue still persist, then follow the steps listed in this [troubleshooting article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorvminternetconnectivityissue)
- **VMNotInRunningStateUserError** - Ensure both the VM host and the SQL Server instance are running <br>
- **GuestAgentStatusUnavailableUserError** - Follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#guestagentstatusunavailableusererror)
- **UserErrorSQLNoSysadminMembership** - Ensure your SQL Server instance has the required permissions as specified in this [article](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-vm-permissions) and retry the operation<br>

**Common questions**
- [Can I control how many concurrent backups run on SQL Server?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-control-how-many-concurrent-backups-run-on-the-sql-server)
- [Are newly added databases automatically added for backup?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#are-future-databases-automatically-added-for-backup)
- [Can I protect Availability Groups across regions?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-protect-availability-groups-across-regions)</br>
- [Back up behavior with Always on availability groups](https://docs.microsoft.com/azure/backup/sql-support-matrix#back-up-behavior-with-always-on-availability-groups)
- [Troubleshoot discover and configure issues](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#troubleshoot-discover-and-configure-issues)

## **Recommended Documents**

- [FAQs](https://docs.microsoft.com/azure/backup/faq-backup-sql-server)</br>
- [Troubleshooting issues related to backing up SQL Server to Azure](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot)</br>
- [Troubleshoot re-registration failures](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#re-registration-failures)
