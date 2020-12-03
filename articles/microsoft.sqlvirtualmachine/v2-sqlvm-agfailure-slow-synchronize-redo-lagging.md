<properties
	pageTitle="Availability Group Failure, Failover, Sync issue"
	description="Availability Group Failure, Failover, Sync issue"
	infoBubbleText="Availability Group Failure, Failover, Sync issue"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,amamun,babarmav"	
	authors="ujpat,amamun,babarmav"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740064"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="26b3b0b0-2353-49d2-88b6-455ef4eb2120"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **AG is slow to synchronize or redo is lagging** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

- You have [followed Performance Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support) **to avoid [VM and disk IO throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics).**  
  - Use separate premium or ultra data disks for SQL data (mdf/ndf) and SQL log (ldf) files
  - Set [**disk caching to ReadOnly**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for **disks hosting data (mdf/ndf) files**
  - Set [**disk caching to None**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) **for disks hosting the log (ldf) file**
  - Place the [system page file](https://docs.microsoft.com/windows/client-management/introduction-page-file), [TempDB on the local SSD D:\ drive](https://cloudblogs.microsoft.com/sqlserver/2014/09/25/using-ssds-in-azure-vms-to-store-sql-server-tempdb-and-buffer-pool-extensions/) for mission-critical SQL Server workloads (after choosing the correct VM size)
  - Move user and system databases, and SQL logs and trace files, from the OS (C:) drive to data drives

- Update to the **[latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)** to avoid any known issues
- If you are seeing **VM level throttling**, moving to a [bigger size VM](https://docs.microsoft.com/azure/virtual-machines/sizes) may resolve the issue
- For hybrid environment like on-premise and Azure with different disk sector sizes, [apply latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) and [use trace flag 1800 as startup parameter](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si) 
- To check **Redo Latency**, review [Scenario 2: Redo Latency](https://support.microsoft.com/help/2922898/error-9002-the-transaction-log-for-database-full-due-to-availability)
