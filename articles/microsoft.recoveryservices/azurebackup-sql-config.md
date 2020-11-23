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

- START HERE: To self-resolve common SQL backup configuration issues, ensure all the [prerequisites](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#prerequisites) are met

**Common error codes**
- **UserErrorVMInternetConnectivityIssue** - Establish network Connectivity to Azure Backup services as described in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#establish-network-connectivity). If the issue still persist, then follow the steps listed in this [troubleshooting article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorvminternetconnectivityissue). 
- **VMNotInRunningStateUserError** - Ensure both the VM host and the SQL Server instance are running <br>
- **GuestAgentStatusUnavailableUserError** - Follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#guestagentstatusunavailableusererror)
- **UserErrorSQLNoSysadminMembership** - Ensure your SQL Server instance have the required  permissions as specified in this [article](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-vm-permissions) and retry the operation<br>

**Common questions**
- [Can I control as to how many concurrent backups run on the SQL server?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-control-how-many-concurrent-backups-run-on-the-sql-server) </br>
- [Are newly added databases automatically added for backup?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#are-future-databases-automatically-added-for-backup)</br>
- [Can I protect availability groups across regions?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-protect-availability-groups-across-regions)</br>

## **Recommended Documents**

- [FAQs](https://docs.microsoft.com/azure/backup/faq-backup-sql-server)</br>
- [Troubleshooting issues related to back up SQL Server to Azure](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot)</br>
