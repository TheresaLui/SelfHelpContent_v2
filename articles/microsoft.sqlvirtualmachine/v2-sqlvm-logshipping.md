<properties
  pagetitle="AlwaysOn, High Availability, Disaster Recovery/Log shipping"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="ujpat,vadeveka,amamun"
  selfhelptype="Generic"
  supporttopicids="32740083"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="a75851ec-7a21-469d-8c11-75c9e481b203"
  ownershipid="AzureData_AzureSQLVM" />
# AlwaysOn, High Availability, Disaster Recovery/Log shipping


**Log Shipping**

**To setup Log Shipping** 

- Ensure the following:
  - Database is in full or bulk-logged recovery model
  - Secondary server has at least the same primary Server SQL edition and version  
  - For hybrid environments like on-premises and Azure with different disk sector sizes, apply the [latest SQL Server build](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)  and use trace flag 1800 as the startup parameter to avoid [slow synchronization issues](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si) 
 - Follow the [Configure Log Shipping](https://docs.microsoft.com/sql/database-engine/log-shipping/configure-log-shipping-sql-server?view=sql-server-ver15) guidelines
 - To use **log shipping with availability groups**, set [backup preference to primary replica](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-backup-on-availability-replicas-sql-server?view=sql-server-ver15) 
 
**To Troubleshoot Log Shipping issues**

- **Error 9004 -while backup is restored via Standby Mode**: Update to the [latest SQL Server build](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) and  [enable trace flag 3057](https://support.microsoft.com/help/4058700/kb4058700-fix-9004-errors-when-restoring-backup-via-standby-mode-in-sq) 
- **Error: 14421 - secondary database  is out of sync**: Follow the guidance in this [article](https://docs.microsoft.com/archive/blogs/mdegre/logshipping-secondary-server-is-out-of-sync-and-lsrestore-job-failing)  
- **Error 41381 while restoring the database**: Ensure that the secondary server has at least same primary Server SQL edition.
- If log shipping fails while using with availability groups 
  - **[Error: 14420 -database has not performed a backup log operation](https://support.microsoft.com/help/2872854/kb2872854-fix-error-14420-when-you-enable-log-shipping-on-databases-th)**: Update to the [latest SQL Server build](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)
  - **[Error - backup operation on database was skipped](https://support.microsoft.com/help/4056821/kb4056821-log-shipping-fails-when-using-with-always-on-availability-gr)**: update to the [latest SQL Server build](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)
- If log shipping **restore job fails on standby mode**, follow the guidance in [this article](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms189572(v=sql.105))  
- If **log shipping jobs are not running**, ensure that SQL agent service is running and backup/copy/restore jobs are enabled  
- To avoid any known issues, update to the [latest SQL Server build](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)

To avoid **slow synchronization or performance issues** for log shipping environment, 

- For hybrid environments like Azure and on-premises with different disk sector sizes: apply the [latest SQL Server build](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) and use [trace flag 1800 as startup parameter](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si)
- Follow the [Performance Guidelines for SQL Server on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support)
  - Use separate premium or ultra data disks for SQL data (mdf/ndf) and SQL log (ldf) files
  - Set [disk caching to ReadOnly](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disk hosting data (mdf/ndf) files
  - Set [disk caching to None](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disks hosting the log (ldf) file
  - Place the page file [TempDB on the local SSD D:\ drive](https://cloudblogs.microsoft.com/sqlserver/2014/09/25/using-ssds-in-azure-vms-to-store-sql-server-tempdb-and-buffer-pool-extensions/) for mission-critical SQL Server workloads (after choosing the correct VM size)
  - Move user and system databases, and SQL logs and trace files, from the OS (C:) drive to data drives
  - Update to the [latest SQL Server build](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) to avoid any known issues
 



## **Recommended Documents**

* [Log shipping secondary server is out of sync and Restore job is failing](https://blogs.technet.microsoft.com/mdegre/2009/08/08/logshipping-secondary-server-is-out-of-sync-and-lsrestore-job-failing/)
* [Configure Log Shipping](https://docs.microsoft.com/sql/database-engine/log-shipping/configure-log-shipping-sql-server?view=sql-server-ver15)
* [High availability and disaster recovery for SQL Server in Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-high-availability-dr)
