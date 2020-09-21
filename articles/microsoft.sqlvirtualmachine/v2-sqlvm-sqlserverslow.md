<properties
  pagetitle="SQL Server is Slow"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="yareyes,AbdullahMSFT,amamun"
  selfhelptype="Generic"
  supporttopicids="32740098"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="7647ab12-e478-4fca-a2f0-c6df8cfe753b"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Server is Slow

## **Recommended Steps**

If you suspect **SQL Server is slow or needs optimization, we strongly recommend** that you follow the [Performance Guidelines for SQL Server on Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance?WT.mc_id=Portal-Microsoft_Azure_Support). 

Key points to verify - 
- For production workloads 
  - Use VM sizes with 4 or more vCPU like [E4S_v3](https://docs.microsoft.com/azure/virtual-machines/ev3-esv3-series) or higher, or [DS12_v2](https://docs.microsoft.com/azure/virtual-machines/dv2-dsv2-series-memory) or higher
  - **do not use standard disk**, use premier disk. For sub-millisecond latency use ultra-disk. 
- Use strip size of 64 KB for OLTP workloads and 256 KB for data warehousing workloads  
- Use a minimum of 2 [premium](https://docs.microsoft.com/azure/virtual-machines/disks-types#premium-ssd) SSD disks (1 for log file and 1 for data files). Stripe multiple Azure data disks to get increased storage throughput if needed 
- Set **[disk caching to ReadOnly](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal) for disk hosting data** (mdf/ndf) files 
- Set **[disk caching to None](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal) for disks hosting the log** (ldf) file 
- Place page file, [TempDB on the local SSD D:\ drive](https://cloudblogs.microsoft.com/sqlserver/2014/09/25/using-ssds-in-azure-vms-to-store-sql-server-tempdb-and-buffer-pool-extensions/) for mission critical SQL Server workloads (after choosing correct VM size). 
- Move user and system databases and SQL log and trace files to data disks 
- Update to the [latest SQL Server builds](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) to avoid any known issues  
- For slow synchronization of SQL AG and log shipping between Azure and on-premise/other clouds with sector size of 512 bytes, you may need to use [trace flag 1800 ](https://support.microsoft.com/help/3009974/fix-slow-synchronization-when-disks-have-different-sector-sizes-for-pr)
- Other areas to consider 
  - Enable database page compression 
  - Enable [instant file initialization](https://docs.microsoft.com/sql/relational-databases/databases/database-instant-file-initialization?view=sql-server-ver15) for data files 
  - Limit autogrowth of the database 
  - Disable autoshrink of the database 
  - Set max server memory at 90% or up to 50 GB left for the Operating System. 

To understand **best practice violations and guest VM performance issues** you can [run Performance diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics) and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. See [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights).
To ensure a speedy resolution, please provide us the PerfInsights logs if you create a support case.

### **Other Things to Consider**
We recommend that you continue using the same database performance [tuning options](https://docs.microsoft.com/archive/msdn-magazine/2008/january/sql-server-uncover-hidden-data-to-optimize-application-performance) that are applicable to SQL Server in any SQL server environment: 
* Consider adding [missing indexes](https://gallery.technet.microsoft.com/Find-statements-for-13e8c2f4) which can help improve query performance
* Consider [updating statistics](https://docs.microsoft.com/sql/relational-databases/maintenance-plans/update-statistics-task-maintenance-plan?view=sql-server-ver15) if possible with Full Scan and for all tables of the database(s) of interest


## **Recommended Documents**

* [Performance Best practices for SQL VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance/)
* [Storage configuration guidelines for SQL VM](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2018/09/25/storage-configuration-guidelines-for-sql-server-on-azure-vm/)
* [OS best practice configurations for SQL Server](https://blogs.msdn.microsoft.com/docast/2018/02/01/operating-system-best-practice-configurations-for-sql-server/)
* [Azure VM Storage performance and throttling demystified](https://blogs.technet.microsoft.com/xiangwu/2017/05/14/azure-vm-storage-performance-and-throttling-demystify/)
* [Designing for high performance](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)