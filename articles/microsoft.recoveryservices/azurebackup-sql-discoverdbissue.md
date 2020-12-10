<properties
		pageTitle="Azure Backup unable to discover DB"
		description="Azure Backup SQL Config failures"
		service="microsoft.recoveryservices"
		resource="vaults"
		authors="srinathv"
		ms.author="srinathv"
		displayOrder=""
		selfHelpType="generic"
		supportTopicIds="32632803"
		resourceTags=""
		productPesIds="15207"
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="590f2f11-423e-4bbe-a601-276b6bc0e3c7"
	ownershipId="StorageMediaEdge_Backup"
/>
# Azure Backup SQL Config failures

## **Recommended Steps**

**Common error codes**
- **VMNotInRunningStateUserError** - [Ensure the SQL Server is running](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#vmnotinrunningstateusererror)</br>
- **UserErrorSQLNoSysadminMembership** - Ensure your SQL Server instance has the required permissions as specified in this [article](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-vm-permissions) and retry the operation
- **UserErrorVMInternetConnectivityIssue** - Establish network connectivity to Azure Backup services as described in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#establish-network-connectivity). If the issue still persists, then follow the steps listed in this [troubleshooting article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorvminternetconnectivityissue). <br>
- **GuestAgentStatusUnavailableUserError** - [Azure Backup service uses Azure VM guest agent for doing backup but guest agent is not available on the target server](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#guestagentstatusunavailableusererror)<br>
- **UserErrorDotNetVersionUpgradeRequired** - Ensure latest .NET Framework is installed on the VM. [Learn more](https://docs.microsoft.com/azure/backup/sql-support-matrix#scenario-support)
- **AutoProtectionCancelledOrNotValid** - [Auto-protection Intent was either removed or is no longer valid](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#autoprotectioncancelledornotvalid)
- **FabricSvcBackupPreferenceCheckFailedUserError** - [Backup preference for SQL Always On Availability Group cannot be met as some nodes of the Availability Group are not registered](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#fabricsvcbackuppreferencecheckfailedusererror)<br>

**Common questions**
- [When I protect a SQL Server instance are future databases automatically added?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#are-future-databases-automatically-added-for-backup)</br>
- [Can I protect SQL Always On Availability Groups across regions?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-protect-availability-groups-across-regions)</br>
- [Complete list of supported and unsupported actions and scenarios and known limitations](https://docs.microsoft.com/azure/backup/sql-support-matrix#feature-consideration-and-limitations)

## **Recommended Documents**

- [Frequently asked questions](https://docs.microsoft.com/azure/backup/faq-backup-sql-server)</br>
- [Troubleshooting issues related to backup SQL Server to Azure](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot)</br>
- [Troubleshoot discover and configure issues](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#troubleshoot-discover-and-configure-issues)
- [Troubleshoot re-registration failures](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#re-registration-failures)
