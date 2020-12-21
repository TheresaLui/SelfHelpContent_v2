<properties
		pageTitle="Azure Backup SQL Backup failures"
		description="Azure Backup SQL Backup failures"
		service="microsoft.recoveryservices"
		resource="vaults"
		authors="srinathv"
		ms.author="srinathv"
		displayOrder=""
		selfHelpType="generic"
		supportTopicIds="32605791"
		resourceTags=""
		productPesIds="15207"
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="296bcd6b-c2a2-42e2-8dd9-bf0c76bfa996"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup SQL Backup failures

## **Recommended Steps**

**Common error codes**
- **UserErrorSQLNoSysadminMembership** - Ensure your SQL Server instance has the required permissions as specified in this [article](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-vm-permissions) and retry the operation<br>
- **UserErrorVMInternetConnectivityIssue** - Establish network connectivity to Azure Backup services as described in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#establish-network-connectivity). If the issue still persists, then follow the steps listed in this [troubleshooting article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorvminternetconnectivityissue) <br>
- **GuestAgentStatusUnavailableUserError** - To resolve this issue, follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#guestagentstatusunavailableusererror)<br>
- **VMNotInRunningStateUserError** - Ensure both the VM host and the SQL Server instance are running <br>
- **UserErrorSQLPODoesNotSupportBackupType** - The SQL database does not support the requested backup type. Review [list of supported and unsupported backup types](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorsqlpodoesnotsupportbackuptype)<br>
- **UserErrorSQLPODoesNotExist** - To resolve this issue, follow the steps listed in this [troubleshooting article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorsqlpodoesnotexist)<br>
**WorkloadExtensionNotReachable** - To resolve this issue, follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#re-registration-failures) 

**Other error codes**
- **UserErrorOpeningSQLConnection** - [Azure Backup is not able to connect to the SQL instance](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererroropeningsqlconnection)<br>
- **UserErrorParentFullBackupMissing** - [First full backup is missing for this data source](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorparentfullbackupmissing)<br>
- **UserErrorBackupFailedAsTransactionLogIsFull** - [Cannot perform backup as transaction log for the data source is full](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorbackupfailedastransactionlogisfull)<br>
- **UserErrorCannotTakeBackupBasedOnBackupPreference** - Ensure all VMs and nodes of the AG are [registered](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#does-the-solution-retry-or-auto-heal-the-backups) with Azure Backup. For AG where replica nodes span across Azure geos, ensure nodes in the primary region meet the backup [preference](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-properties-new-availability-group-backup-preferences-page?view=sql-server-ver15)<br>

## **Recommended Documents**

- [FAQ for SQL Server backup](https://docs.microsoft.com/azure/backup/faq-backup-sql-server)<br>
- [Troubleshooting issues related to backing up SQL Server to Azure](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot)
- [Complete list of supported and unsupported actions and scenarios and known limitations](https://docs.microsoft.com/azure/backup/sql-support-matrix#feature-consideration-and-limitations)
