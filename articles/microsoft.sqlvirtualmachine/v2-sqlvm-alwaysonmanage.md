<properties
  pagetitle="Always On Availability Groups - Failure,Failover, Sync issues"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="amamun,babarmav,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740064"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="479bfcb0-d975-4810-b14e-1efc25532e7e"
  ownershipid="AzureData_AzureSQLVM" />
# Always On Availability Groups - Failure,Failover, Sync issues


## **Recommended Steps**

Most of users are able to resolve their issues using the following steps. 

### Availability Group fails, restarts, fails over, or the lease times out 

To know the root cause of the issue, review the logs using [this tool](https://techcommunity.microsoft.com/t5/sql-server/failover-detection-utility-availability-group-failover-analysis/ba-p/386021). 

To avoid the issue:
- Make sure Windows Cluster service is running and that [cluster network thresholds are relaxed](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster)
- [Follow Performance Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support) to avoid [VM and disk IO throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics)
   - Use separate premium or ultra data disks for SQL data (.mdf/.ndf) and SQL log (.ldf) files
   - Set [disk caching to **ReadOnly**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disks hosting data (.mdf/.ndf) files
   - Set [disk caching to **None**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disks hosting the log (.ldf) file
   - Place the [system page file](https://docs.microsoft.com/windows/client-management/introduction-page-file), [TempDB on the local SSD D:\ drive](https://cloudblogs.microsoft.com/sqlserver/2014/09/25/using-ssds-in-azure-vms-to-store-sql-server-tempdb-and-buffer-pool-extensions/) for mission-critical SQL Server workloads (after choosing the correct VM size)
   - Move user and system databases, and SQL logs and trace files, from the OS drive (C:\) to data drives
  
- Update to the [latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) to avoid any known issues
- If you are seeing VM level throttling, moving to a [bigger size VM](https://docs.microsoft.com/azure/virtual-machines/sizes) may resolve the issue
- You can temporarily mask the underlying issue by relaxing the [AG lease timeout](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-lease-healthcheck-timeout?view=sql-server-2017#lease-timeout) and [HealthCheckTimeout](https://docs.microsoft.com/sql/sql-server/failover-clusters/windows/configure-healthchecktimeout-property-settings?view=sql-server-ver15#TsqlExample) to a higher value than the default value, such as 60000 (60 seconds). This makes [FailureConditionLevel](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-lease-healthcheck-timeout?view=sql-server-2017#health-check-values) less restrictive (for example, changes it from the default 3 to 1 or 2).

### Event ID 1135 -node was removed from cluster membership, quorum lost, or Windows Cluster stops

- Ensure [cluster network thresholds are relaxed](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster)
- [Follow Performance Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support) to avoid [VM and disk IO throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics)
   - Use separate premium or ultra data disks for SQL data (.mdf/.ndf) and SQL log (.ldf) files
   - Set [disk caching to **ReadOnly**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disks hosting data (.mdf/.ndf) files
   - Set [disk caching to **None**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disks hosting the log (.ldf) file
   - Place the [system page file](https://docs.microsoft.com/windows/client-management/introduction-page-file), [TempDB on the local SSD D:\ drive](https://cloudblogs.microsoft.com/sqlserver/2014/09/25/using-ssds-in-azure-vms-to-store-sql-server-tempdb-and-buffer-pool-extensions/) for mission-critical SQL Server workloads (after choosing the correct VM size)
   - Move user and system databases, and SQL logs and trace files, from the OS (C:) drive to data drives

- Update to the [latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) to avoid any known issues
- If you are seeing VM level throttling, moving to a [bigger size VM](https://docs.microsoft.com/azure/virtual-machines/sizes) may resolve the issue


### **Unable to failover AG to another replica**
- Ensure that the [`NT AUTHORITY\SYSTEM` account is granted required privilege](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all the replicas of the AG
- Watch from the cluster manager while you do the failover. Does the IP address and Network name come online? If not, resolve the IP or network name issues.

### **Unable to connect to AG listener** 

- Ensure that [load balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer) is configured correctly.  
- Ensure that **[Floating IP (direct server return) is enabled](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#set-the-load-balancing-rules)** for the load balancer.
- Run the below powershell command

```
Param
(
    [Parameter(Mandatory = $true)]
    [ValidateNotNullOrEmpty()]
    [String]
    $AGName,

    [Parameter(Mandatory = $true)]
    [ValidateNotNullOrEmpty()]
    [String]
    $AGProbePort
);

Import-Module FailoverClusters;
write-Host ('The Probe Port Entered is $AGProbePort and AG Name is' + $AGName);
$AGValidate = Get-ClusterResource |  Where-Object -FilterScript {($_.ResourceType.Name -eq 'SQL Server Availability Group') -and ($_.Name -eq $AGName)};

if ($AGName -eq $AGValidate) 
{
    #AG is found
    Write-Host 'AG is found. Setting up your Listener/ILB Configuration...' 
    $MyClusterNetworkName = Get-ClusterNetwork  
    $ClusterNetworkName = $MyClusterNetworkName.Name # the cluster network name (Use Get-ClusterNetwork on Windows Server 2012 of higher to find the name)
    Write-Host ('Cluster Network is' + $ClusterNetworkName);
        
    $ClusterIPResourceName=Get-ClusterResource |  Where-Object -FilterScript {($_.ResourceType.Name -eq 'IP Address') -and ($_.OwnerGroup -eq $AGName) -and ($_.State -eq 'Online')  }
    $IPResourceName = $ClusterIPResourceName.Name  #Gets the IP Resource Name for this particular AG
    Write-Host ('IP Resource Name is' + $IPResourceName)
        
    $ListenerIP= Get-ClusterResource |  Where-Object -FilterScript {($_.ResourceType.Name -eq 'IP Address') -and ($_.OwnerGroup -eq $AGName)} | Get-ClusterParameter -Name 'Address'
    $ClusterCoreIP = $ListenerIP.Value #Gets listener IP for this particular AG
    Write-Host( 'Listener Ip is ' + $ClusterCoreIP)          
    
    Get-ClusterResource $IPResourceName | Set-ClusterParameter -Multiple @{'Address'='$ClusterCoreIP';'ProbePort'=$AGProbePort;'SubnetMask'='255.255.255.255';'Network'='$ClusterNetworkName';'EnableDhcp'=0}
    }  
else
{
    #AG is not found
    Write-Host 'AG: $AGName is not found'
}
```

**Note:** After you run the PowerShell to configure the cluster parameters, restart the AG Role.
 
- Ensure that all the ports required for the listener are open in [NSG](https://docs.microsoft.com/azure/virtual-machines/windows/nsg-quickstart-portal) and in [Windows Firewall](https://docs.microsoft.com/windows/security/threat-protection/windows-firewall/create-an-inbound-port-rule) for all replicas. For example, SQL instance port (1433), mirroring port (5022), Load balancer probe port (59999).
- Ensure that SQL Server service is up and running on the Primary replica

### **Why did Availability Group not Failover?**  

- Make sure to meet [Conditions for Automatic Failover](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/failover-and-failover-modes-always-on-availability-groups?view=sql-server-ver15#RequiredConditions). This means that every secondary database on the failover target is synchronized.
- Make sure that account [NT AUTHORITY\SYSTEM has required privileges](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012)
- Make sure that the `Maximum Failures in the Specified Period` value [is not exhausted](https://support.microsoft.com/help/2833707/kb2833707-troubleshooting-automatic-failover-problems-in-sql-server-20) 

### AG is Offline or Database are in Resolving State

- Make sure Windows Cluster service is running
- Make sure [cluster network thresholds are relaxed](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster)
- If [Cluster service was started with force quorum](https://docs.microsoft.com/sql/sql-server/failover-clusters/windows/force-a-wsfc-cluster-to-start-without-a-quorum?view=sql-server-ver15), you [must use following command](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/perform-a-forced-manual-failover-of-an-availability-group-sql-server?view=sql-server-ver15) in the correct replica to bring AG online:
 
   `ALTER AVAILABILITY GROUP AGName FORCE_FAILOVER_ALLOW_DATA_LOSS`

- Account [`NT AUTHORITY\SYSTEM` has required privileges](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012)
	
### AG is slow to synchronize or Redo is lagging
- [Follow Performance Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support) to avoid [VM and disk IO throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics)
    - Use separate premium or ultra data disks for SQL data (.mdf/.ndf) and SQL log (.ldf) files
    - Set [disk caching to **ReadOnly**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disks hosting data (.mdf/.ndf) files
    - Set [disk caching to **None**](https://docs.microsoft.com/learn/modules/caching-and-performance-azure-storage-and-disks/4-exercise-enable-and-configure-azure-vm-disk-cache-by-using-the-azure-portal?WT.mc_id=Portal-Microsoft_Azure_Support) for disks hosting the log (.ldf) file
    - Place the [system page file](https://docs.microsoft.com/windows/client-management/introduction-page-file), [TempDB on the local SSD D:\ drive](https://cloudblogs.microsoft.com/sqlserver/2014/09/25/using-ssds-in-azure-vms-to-store-sql-server-tempdb-and-buffer-pool-extensions/) for mission-critical SQL Server workloads (after choosing the correct VM size)
    - Move user and system databases, and SQL logs and trace files, from the OS drive (C:\) to data drives

- Update to the [latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) to avoid any known issues
- If you're seeing VM level throttling, moving to a [bigger size VM](https://docs.microsoft.com/azure/virtual-machines/sizes) may resolve the issue
- For hybrid environments, such as on-premises and Azure with different disk sector sizes, [apply the latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) and [use **trace flag 1800** as startup parameter](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si) 
- To check Redo latency, review [Scenario 2: Redo Latency](https://support.microsoft.com/help/2922898/error-9002-the-transaction-log-for-database-full-due-to-availability)

### **Event ID 157- Disk was Surprised-Removed** 
This can happen if the following conditions are present: 
- There is significant disk IO [throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics). Follow [Performance Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support) for SQL Server on Azure VM to avoid IO throttling. 
- The Storage Spaces property `AutomaticClusteringEnabled` is set to `True` for an AG Environment. Change it to `False.` 
- Running [Cluster validation Report](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134244%28v=ws.11%29#to-run-the-validate-a-configuration-wizard) with **Storage** option

### **AG DB log file unable to shrink or is growing** 
- Review  [this article](https://support.microsoft.com/help/2922898/error-9002-the-transaction-log-for-database-full-due-to-availability) to understand and manage the AG database log file.
- Review [factors that can delay log truncation](https://docs.microsoft.com/sql/relational-databases/logs/the-transaction-log-sql-server?view=sql-server-ver15#FactorsThatDelayTruncation)

### **Error There have been X misaligned log IOs** 
- This can happen in a hybrid environment, such as on-premises and Azure with [different disk sector sizes](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si). [Apply the latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds) and use **[trace flag 1800** as startup parameter](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si).

### **Unable to login after failover** 
- Ensure that you use the AG Listener name or the [DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-distributed-network-name-dnn-listener-configure) to connect 
- [Listener is set up with a load balancer correctly](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer)
- Appropriate logins are available in the new primary. [Use Method 2 in this article, under More Information](https://support.microsoft.com//help/918992/how-to-transfer-logins-and-passwords-between-instances-of-sql-server) to transfer logins from the previous primary to the new primary.

### **How do I setup AG** 

[Compare different ways](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-overview#deployment) to set up AG and use one of the following methods that best fits your environment:
  * [Configure Availability Group Pre-requisites](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-prerequisites-tutorial) and then set [Always On Configuration manually](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial)
  * [Use PowerShell or Azure CLI to configure an Availability Group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-az-commandline-configure?tabs=azure-cli)
  * [Use Azure Quick Start templates to configure an Availability Group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-quickstart-template-configure)
  * [Configure an Availability Group using Azure portal preview](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-azure-portal-configure?tabs=azure-cli)

## **Recommended Documents**

- [Monitor and troubleshoot Always On Availability Groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support) Availability Groups
- [Monitor performance](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/monitor-performance-for-always-on-availability-groups?view=sql-server-ver15) for Always On availability groups
- Troubleshoot: Availability Group exceeded [RPO](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-availability-group-exceeded-rpo?view=sql-server-ver15) or [RTO](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-availability-group-exceeded-rto?view=sql-server-ver15)
- [Changes from the primary replica are not reflected](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-primary-changes-not-reflected-on-secondary?view=sql-server-ver15) on secondary
- [Useful tools for Availability Group troubleshooting](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/useful-tools-for-troubleshooting?view=sql-server-ver15)
- [Recommendations for index maintenance](https://techcommunity.microsoft.com/t5/sql-server-support/recommendations-for-index-maintenance-with-alwayson-availability/ba-p/318518) with Availability Groups
