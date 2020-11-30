<properties
		pageTitle="Azure Backup unable to discover VM"
		description="Azure Backup SQL Config failures"
		service="microsoft.recoveryservices"
		resource="vaults"
		authors="srinathv"
		ms.author="srinathv"
		displayOrder=""
		selfHelpType="generic"
		supportTopicIds="32632804"
		resourceTags=""
		productPesIds="15207"
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="91077485-46e3-4c9f-a5ae-6d71eae1cf85"
	ownershipId="StorageMediaEdge_Backup"
/>
# Azure Backup SQL Config failures

## **Recommended Steps**

**Common error codes**
- **UserErrorVMInternetConnectivityIssue** - Establish network connectivity to Azure Backup services as described in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#establish-network-connectivity). If the issue still persists, follow the steps listed in this [troubleshooting article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorvminternetconnectivityissue). 
- **VMNotInRunningStateUserError** - [Ensure SQL Server is running](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#vmnotinrunningstateusererror)</br>
- **FabricSvcBackupPreferenceCheckFailedUserError** - [Backup preference for SQL Always On Availability Group cannot be met because some nodes of the Availability Group are not registered](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#fabricsvcbackuppreferencecheckfailedusererror)<br>
- **VMNotInRunningStateUserError** - [SQL Server VM is either shut down or not accessible to Azure Backup service](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#vmnotinrunningstateusererror)<br>
- **GuestAgentStatusUnavailableUserError** - [Azure Backup service uses Azure VM guest agent for doing backup, but guest agent is not available on the target server](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#guestagentstatusunavailableusererror)<br>
- **AutoProtectionCancelledOrNotValid** - [Auto-protection Intent was either removed or is no longer valid](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#autoprotectioncancelledornotvalid)

**Common questions**
- [Cannot discover VM? Check if the VM is registered to a different vault, unregistered it from the old Vault by following these steps](https://docs.microsoft.com/azure/backup/manage-monitor-sql-database-backup#unregister-a-sql-server-instance) then register it again to a new Vault.
- [When I protect a SQL Server instance, are future databases automatically added?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#are-future-databases-automatically-added-for-backup)</br>
- [If I delete a database from an autoprotected instance, what will happen to the backups?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#if-i-delete-a-database-from-an-autoprotected-instance-what-will-happen-to-the-backups)</br>
- [Can I protect SQL Always On Availability Groups where the primary replica is on-premises?](https://docs.microsoft.com/azure/backup/faq-backup-sql-server#can-i-protect-availability-groups-across-regions)</br>

## **Recommended Documents**

- [FAQ for SQL Server backup](https://docs.microsoft.com/azure/backup/faq-backup-sql-server)</br>
- [Troubleshooting issues related to backing up SQL Server to Azure](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot)</br>
- [Troubleshoot re-registration failures](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#re-registration-failures)
