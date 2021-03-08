<properties
  pagetitle="Migrate to SQL VM &#xD;"
  description="Migrate to SQL VM"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740085"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="ae03e814-ee11-4998-9177-e29c8abd7ce8"
  ownershipid="AzureData_AzureSQLVM" />
# Migrate to SQL VM 

Most users are able to resolve issues concerning migrating to SQL VM by using the following steps. 

## **Recommended Steps** 

* **Migrate Databases or Export Data from On-Premises/Another Cloud to Azure VM** 

  Before you migrate, make sure you've followed the [Best Practice Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices) to optimize your SQL Server on Azure experience. 

  * [Migrate using High Availability and Disaster Recovery Solutions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/business-continuity-high-availability-disaster-recovery-hadr-overview#hybrid-it-disaster-recovery-solutions)
  * [Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url?redirectedfrom=MSDN&view=sql-server-ver15#complete) and [Restore](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql?view=sql-server-ver15#Azure_Blob) 
  * [AzCopy tool](https://azure.microsoft.com/documentation/articles/storage-use-azcopy/)
  * [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/) 
  * [Backup to Microsoft Azure Tool](https://blogs.technet.microsoft.com/dataplatforminsider/2014/07/24/get-started-backing-up-to-the-cloud-with-sql-server-backup-to-microsoft-azure-tool/) for SQL 2008/R2 version. 
  * [Azure Backup and Site Recovery](https://docs.microsoft.com/azure/backup/) 
  * [Convert on-premises machine to Hyper-V VHD](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image), upload to Azure Blob storage, and deploy a new VM using the VHD. 
  * [Migrate your hard drive using the Windows Import/Export service.](https://docs.microsoft.com/azure/import-export/storage-import-export-service) 

  If you **do not have a scheduled downtime** and want to migrate your databases, the only option is to [set up a hybrid Always-on group](https://docs.microsoft.com/previous-versions/azure/virtual-machines/windows/sqlclassic/virtual-machines-windows-classic-sql-onprem-availability#add-azure-replica-wizard) between your on-premises and Azure, and fail that over to Azure.   

* **Issues you may encounter after Migration**  

  * If you have installed SQL Server independently on Azure, make sure you [register IaaS Agent Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli) to [change your licensing to **AHUB**](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal), so that you won't be charged for SQL on Azure. 

  *  **Migration to another VNET/Resource Group** requires fresh [installation of IaaS Agent Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli) on the destination VM. If you installed SQL Server manually, make sure you update the [licensing information](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal) after installation.

   * Make sure you [transfer your logins from on-premises to SQL Server on Azure VM](https://docs.microsoft.com/troubleshoot/sql/security/transfer-logins-passwords-between-instances) after migration. Also [update the statistics](https://docs.microsoft.com/sql/t-sql/statements/update-statistics-transact-sql?view=sql-server-ver15) and [rebuild indexes](https://docs.microsoft.com/sql/relational-databases/indexes/reorganize-and-rebuild-indexes?view=sql-server-ver15#rebuild-an-index).

 * **Data Migration Assistant(DMA)** 

   * [DMA](https://www.microsoft.com/download/details.aspx?id=53595) enables you to upgrade to a modern data platform by detecting **compatibility issues** that can impact database functionality on your new version of SQL Server. DMA also **recommends performance and reliability improvements** for your target environment. It allows you to not only **move your schema and data, but also to move uncontained objects** from your source server to your target server. 

   * The source server supports SQL Server 2005 to SQL Server 2019, and the target server supports SQL Server 2012 to SQL Server 2019.  

   * Make sure you're not running transactions on your source server when migrating using DMA, because these transactions will not be migrated to the destination. 

## **Recommended Documents** 

* [Create SQL Server on Windows VM Azure portal](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-create-portal-quickstart) and [Overview of SQL Server on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-server-on-azure-vm-iaas-what-is-overview) 
* [Migrate your SQL Server Database to SQL Server on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/migrate-to-vm-from-sql-server) 
* [Migrate on-premises machine to Azure using Azure Migrate/Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/migrate-tutorial-on-premises-azure) 
* [Overview of Database Migration Assistant(DMA)](https://docs.microsoft.com/sql/dma/dma-overview?view=sql-server-ver15) 
* [Storage Configuration Guidelines for SQL VM ](https://docs.microsoft.com/archive/blogs/sqlserverstorageengine/storage-configuration-guidelines-for-sql-server-on-azure-vm)