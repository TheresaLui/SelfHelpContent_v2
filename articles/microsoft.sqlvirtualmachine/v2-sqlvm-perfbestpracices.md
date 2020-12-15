<properties
  pagetitle="SQL Server Performance Best Practices &#xD;"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="ujpat,vadeveka,amamun"
  selfhelptype="Generic"
  supporttopicids="32740099"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="28ab511a-0786-4f89-8fd2-a209fec4aea9"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Server Performance Best Practices 

If SQL Server is slow, most users can resolve issues by following the steps below.

## **Recommended Steps**

If you suspect SQL Server is slow or needs optimization, we strongly recommend that you follow the [Performance Guidelines for SQL Server on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices)

**Key points to verify**:

- For Production Workloads
  - Use VM sizes with 4 or more vCPU like [E4S_v3 ](https://docs.microsoft.com/azure/virtual-machines/ev3-esv3-series) or higher, or [DS12_v2](https://docs.microsoft.com/azure/virtual-machines/dv2-dsv2-series-memory) or higher
  - **Do not use a standard disk**, use a premier disk instead. For sub-millisecond latency, use an ultra-disk. 
- Use strip size of 64 KB for OLTP workloads and 256 KB for data warehousing workloads  
- Set **[disk caching to ReadOnly](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal) for disk hosting data** (mdf/ndf) files 
- Set **[disk caching to None](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal) for disks hosting the log** (ldf) file 
- Place page file [TempDB on the local SSD D:\ drive](https://cloudblogs.microsoft.com/sqlserver/2014/09/25/using-ssds-in-azure-vms-to-store-sql-server-tempdb-and-buffer-pool-extensions/) for mission critical SQL Server workloads (after choosing correct VM size)
- Move user and system databases, SQL logs, and trace files from OS (C:\) drive to data drives
- Update to the [latest SQL Server builds](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) to avoid any known issues 
- For slow synchronization of SQL AG and log shipping between Azure and on-premise/other clouds with sector size of 512 bytes, you may need to use [trace flag 1800 ](https://support.microsoft.com/help/3009974/fix-slow-synchronization-when-disks-have-different-sector-sizes-for-pr)
- Other areas to consider:
  - Enable database page compression 
  - Enable [instant file initialization](https://docs.microsoft.com/sql/relational-databases/databases/database-instant-file-initialization?view=sql-server-ver15) for data files 
  - Limit autogrowth of the database 
  - Disable autoshrink of the database 
  - Set max server memory at 90% or up to 50 GB left for the Operating System

To understand **best practice violations and guest VM performance issues** you can [run Performance diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics) and review results directly from the Azure portal. You can also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. See [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights).
If you create a support case, provide the PerfInsights logs to ensure a speedy resolution.

To check **VM or disk level IO capping**, you can check [this article](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics) 

### **Optimize SQL Server Instance**
We recommend that you continue to use the same database performance [tuning options](https://docs.microsoft.com/archive/msdn-magazine/2008/january/sql-server-uncover-hidden-data-to-optimize-application-performance) that are applicable to SQL Server in any environment: 
* Consider [adding missing indexes](https://gallery.technet.microsoft.com/Find-statements-for-13e8c2f4), which can help improve query performance
* Consider [updating statistics](https://docs.microsoft.com/sql/relational-databases/maintenance-plans/update-statistics-task-maintenance-plan?view=sql-server-ver15), if possible with Full Scan, for the tables of database(s) that are frequently modified 

## **Recommended Documents**

* [Performance guidelines for SQL Server on Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance/)
* [Security considerations for SQL Server on Azure Virtual Machines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/security-considerations-best-practices)
* [Application patterns and development strategies for SQL Server on Azure Virtual Machine](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/application-patterns-development-strategies)
* [Cluster configuration best practices (SQL Server on Azure VMs)](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/hadr-cluster-best-practices)
* [Storage configuration guidelines for SQL VM](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2018/09/25/storage-configuration-guidelines-for-sql-server-on-azure-vm/)
* [OS best practice configurations for SQL Server](https://blogs.msdn.microsoft.com/docast/2018/02/01/operating-system-best-practice-configurations-for-sql-server/)
* [Understanding Azure Virtual Machine IOPS, throughput and disk latency](https://docs.microsoft.com/archive/blogs/andrewc/understanding-azure-virtual-machine-iops-throughput-and-disk-latency)
* [Azure premium storage: designing for high performance](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)