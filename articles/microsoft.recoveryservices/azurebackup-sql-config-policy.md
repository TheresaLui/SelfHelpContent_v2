<properties
		pageTitle="Azure Backup SQL Config issue modifying backup policy"
		description="Azure Backup SQL Config issue modifying backup policy"
		service="microsoft.recoveryservices"
		resource="vaults"
		authors="srinathv"
		ms.author="srinathv"
		displayOrder=""
		selfHelpType="generic"
		supportTopicIds="32632802"
		resourceTags=""
		productPesIds="15207"
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="11a1ff7d-64de-409f-93a6-a02a691f27fd"
	ownershipId="StorageMediaEdge_Backup"
/>
# Azure Backup SQL Config issue modifying backup policy

## **Recommended Steps**

- **UserErrorVMInternetConnectivityIssue** - Establish network connectivity to Azure Backup services as described in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#establish-network-connectivity). If the issue still persist, then follow the steps listed in this [troubleshooting article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorvminternetconnectivityissue) <br>
- **VMNotInRunningStateUserError** - Ensure both the VM host and the SQL Server instance are running <br>
- [How to configure backup for SQL server in Azure VM?](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#configure-backup)
- Steps to [modify backup policy](https://docs.microsoft.com/azure/backup/manage-monitor-sql-database-backup#modify-policy) to update backup frequency or retention
- [Back up behavior with Always On availability groups](https://docs.microsoft.com/azure/backup/sql-support-matrix#back-up-behavior-with-always-on-availability-groups)
- [How to unregister the protected SQL server instance?](https://docs.microsoft.com/azure/backup/manage-monitor-sql-database-backup#unregister-a-sql-server-instance)

## **Recommended Documents**

- [Troubleshooting permission issues](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#sql-server-permissions)
- [Frequently Asked Questions](https://docs.microsoft.com/azure/backup/faq-backup-sql-server)
- [Enable Auto Protection](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#enable-auto-protection)
- [Capabilities and limitations](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#feature-consideration-and-limitations)
- [Discover SQL Server databases](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#discover-sql-server-databases)
- [Back up behavior with Always on availability groups](https://docs.microsoft.com/azure/backup/sql-support-matrix#back-up-behavior-with-always-on-availability-groups)
- [Troubleshoot discover and configure issues](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#troubleshoot-discover-and-configure-issues)
