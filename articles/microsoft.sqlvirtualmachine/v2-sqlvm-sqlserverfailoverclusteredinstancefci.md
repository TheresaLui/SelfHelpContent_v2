<properties
  pagetitle="AlwaysOn, High Availability, Disaster Recovery - SQL Server Failover Clustered Instance"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740097"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="ac1b7d53-9698-4f2a-9e6b-126c2e38ed2c"
  ownershipid="AzureData_AzureSQLVM" />
# AlwaysOn, High Availability, Disaster Recovery - SQL Server Failover Clustered Instance


Resolve issues with SQL Failover Clustered Instance (FCI) using these steps.


## Recommended Steps

To set up FCI:

1. Review [this document](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-overview#storage) to figure out which FCI storage solution works best for your needs. We recommend Azure shared disk for parity with on-premises environment.  
1. [Prepare VMs for FCI](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-prepare-vm) 
1. Relax [cluster network thresholds](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster)  
1. Use [single NIC on the VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-overview#considerations)
1. Create FCI using one of the following:
   - [Azure Shared Disk](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-azure-shared-disks-manually-configure?tabs=windows2012)
   - [Storage Spaces Direct(S2D)](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-storage-spaces-direct-manually-configure?tabs=windows2012)
   - [Premium file share](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-premium-file-share-manually-configure?tabs=windows2012)
1. Create client access using [VNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure) or [DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-distributed-network-name-dnn-configure). For DNN, review [feature interoperability](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-dnn-interoperability).

## FCI troubleshooting

- For **error 1206 - cluster resource could not be brought online due to an error bringing the dependency resource** or for **error 19471**, ensure [cluster name account does have the "Create Computer object" permission or you pre-stage the 'Pre-Stage' the VCO](https://techcommunity.microsoft.com/t5/sql-server-support/error-during-installation-of-an-sql-server-failover-cluster/ba-p/317873)
- For **Event ID 1135 (cluster node was removed from the active failover cluster membership)**,  make sure you have [relaxed cluster network thresholds](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster) and review [this article](https://docs.microsoft.com/windows-server/troubleshoot/troubleshooting-cluster-event-id-1135)
- If you are **unable to connect to FCI**, ensure that you have setup either using either [VNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure) or [DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-distributed-network-name-dnn-configure).
- If **using load balancer, you are unable to connect to FCI outside of active node**, ensure you [setup load balancer correctly](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure#create-load-balancer)  
- Used a free IP separate other than the cluster IP
- The probe port (such as 59999) used is free in all nodes
- [Floating IP (direct server return) for load- balancing rule](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure#set-load-balancing-rules) is **Enabled**
- Run the following PowerShell command. After you run the PowerShell to configure the cluster parameters, restart the AG Role:

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


### SQL IaaS Extension on FCI
FCI on Azure VM only supports lightweight management mode. [Learn more](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-azure-shared-disks-manually-configure?tabs=windows2012#register-with-the-sql-vm-rp).


## **Recommended Documents**

- [Comparison of different FCI solutions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-overview#storage) on Azure VMs 
- [Prepare VMs for FCI](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-prepare-vm) 
- Create FCI using either [Azure Shared Disk](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-azure-shared-disks-manually-configure?tabs=windows2012) or [Storage Spaces Direct(S2D)](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-storage-spaces-direct-manually-configure?tabs=windows2012) or [Premium file share](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-premium-file-share-manually-configure?tabs=windows2012) 
- [Upgrade FCI](https://docs.microsoft.com/sql/sql-server/failover-clusters/windows/upgrade-a-sql-server-failover-cluster-instance?view=sql-server-ver15)
- [High availability and disaster recovery](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/business-continuity-high-availability-disaster-recovery-hadr-overview) SQL Server on Azure VM
