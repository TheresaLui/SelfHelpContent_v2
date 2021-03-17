<properties
	pageTitle="Different ways of Database migration to Azure"
	description="Different ways of Database migration to Azure"
	infoBubbleText="Different ways of Database migration to Azure"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740094"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="5849398f-efcc-4f82-8b70-9487076b01b0-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
You can migrate your databases to Azure with different ways listed below 
<!--/issueDescription-->

## **Recommended Steps**
If you have a planned downtime to migrate your databases, then you can use the below options:  
- **Backup to URL feature**: You can use this feature to backup databases to **Storage account** on Azure and then restore them from the storage account on your Azure VM. You will need to open outbound port 443 to backup from on Prem to azure. 
- **AzCopy tool**: AzCopy is a Windows command-line utility designed for copying data to and from Microsoft Azure Blob, File, and Table storage using simple commands with optimal performance. This is preferred option for databases in terabytes. 
- **Azure Storage Explorer**:  If you already have backup files on the disk, you can download azure storage explorer and upload these files to the storage account on Azure and run restore from SSMS to restore the databases. 
- **Backup for SQL 2008/R2**: You can backup databases for SQL 2008/R2 using Backup to Microsoft Azure Tool 
- **Azure Backup and Site Recovery**: Backup Service on azure helps in backing up on prem or azure database/VM’s and Site recovery is a business continuity and disaster recovery solution 

If you do not have a downtime and want to migrate your databases, then you can use the below option: 

- If you want to migrate databases without a downtime then the only option to go with is setting up a hybrid Always on  group between your on prem and Azure and fail that over to Azure. 
- Making sure Application connection string only points to Azure once the failover is done and decommissioning your on-premise server. 
 
## **Recommended Documents**

* [Perform a full database backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url?redirectedfrom=MSDN&view=sql-server-ver15#complete)
* [Restoring from the Microsoft Azure Blob storage service](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql?view=sql-server-ver15#Azure_Blob)
* [Get started with AzCopy](https://azure.microsoft.com/documentation/articles/storage-use-azcopy/)
* [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/)
* [Get started backing up to the cloud with SQL Server Backup to Microsoft Azure Tool](https://blogs.technet.microsoft.com/dataplatforminsider/2014/07/24/get-started-backing-up-to-the-cloud-with-sql-server-backup-to-microsoft-azure-tool/)
* [Azure Backup service documentation](https://docs.microsoft.com/azure/backup/)
* [About Site Recovery](https://docs.microsoft.com/azure/site-recovery/site-recovery-overview)
* [Configure Azure VM as a secondary replica in an availability group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/use-the-add-azure-replica-wizard-sql-server?view=sql-server-ver15 )