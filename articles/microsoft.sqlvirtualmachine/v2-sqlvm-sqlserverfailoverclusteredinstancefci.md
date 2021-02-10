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

**SQL Failover Clustered Instance (FCI)**

**FCI Setup Steps**

1. Review [this document](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-overview#storage) to figure out which FCI storage solution works best for your needs. We recommend Azure shared disk for parity with on-premises environment.  
1. [Prepare VMs for FCI](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-prepare-vm) 
1. Relax [cluster network thresholds](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster)  
1. Use [single NIC on the VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-overview#considerations)
1. Create FCI using either [Azure Shared Disk](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-azure-shared-disks-manually-configure?tabs=windows2012) or [Storage Spaces Direct(S2D)](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-storage-spaces-direct-manually-configure?tabs=windows2012) or [Premium file share](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-premium-file-share-manually-configure?tabs=windows2012)  
1. Create client access using either [VNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure) or [DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-distributed-network-name-dnn-configure). For DNN, review [feature interoperability](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-dnn-interoperability)

**FCI Troubleshooting**  

- For **error 1206 - cluster resource could not be brought online due to an error bringing the dependency resource** or for **error 19471**, ensure [cluster name account does have the "Create Computer object" permission or you pre-stage the 'Pre-Stage' the VCO](https://techcommunity.microsoft.com/t5/sql-server-support/error-during-installation-of-an-sql-server-failover-cluster/ba-p/317873)
- For **Event ID 1135 (cluster node was removed from the active failover cluster membership)**,  make sure you have [relaxed cluster network thresholds](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster) and review [this article](https://docs.microsoft.com/windows-server/troubleshoot/troubleshooting-cluster-event-id-1135)
- If you are **unable to connect to FCI**, ensure that you have setup either using either [VNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure) or [DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-distributed-network-name-dnn-configure).
- If **using load balancer, you are unable to connect to FCI outside of active node**, ensure you [setup load balancer correctly](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure#create-load-balancer)  
- Used a free IP separate other than the cluster IP
- The probe port (such as 59999) used is free in all nodes
- [Floating IP (direct server return) for load- balancing rule](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure#set-load-balancing-rules) is **Enabled**
- You ran the [cluster probe PowerShell with correct values](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure#configure-cluster-probe) for your environment. To determine appropriate variables for [cluster probe PowerShell](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-vnn-azure-load-balancer-configure#configure-cluster-probe), use the following:
   * **Cluster Network Name:** In Failover Cluster Manager > Networks, right-click the network and select **Properties**. The correct value is under Name on the General tab.
   * **SQL Server FCI/AG listener IP Address Resource Name**: In Failover Cluster Manager > Roles, under the SQL Server FCI role, under Server Name, right-click the IP address resource and select **Properties**. The correct value is under Name on the General tab.
   * **ILBIP**: You can find it in Failover Cluster Manager on the same properties page where you located the <SQL Server FCI/AG listener IP Address Resource Name>.
   * **nnnnn**: The probe port that you configured in the load balancer's health probe (such as 59999). Any unused TCP port is valid.

- Run the following PowerShell command on any node of the cluster in the same Azure region. You have to update and run the script again in other regions if you have an Azure multi-region setup: 

   ```
   $ClusterNetworkName = "Cluster Network Name"
   $IPResourceName = "SQL Server FCI / AG Listener IP Address Resource Name" 
   $ILBIP = "n.n.n.n" 
   [int]$ProbePort = <nnnnn>
   Import-Module FailoverClusters
   Get-ClusterResource $IPResourceName | Set-ClusterParameter -Multiple @{"Address"="$ILBIP";
   "ProbePort"=$ProbePort;"SubnetMask"="255.255.255.255";"Network"="$ClusterNetworkName";"EnableDhcp"=0}         
   ```

**SQL IaaS Extension on FCI** 
FCI on Azure VM only supports lightweight management mode. [Learn more](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-azure-shared-disks-manually-configure?tabs=windows2012#register-with-the-sql-vm-rp) 


## **Recommended Documents**

- [Comparison of different FCI solutions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-overview#storage) on Azure VMs 
- [Prepare VMs for FCI](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-prepare-vm) 
- Create FCI using either [Azure Shared Disk](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-azure-shared-disks-manually-configure?tabs=windows2012) or [Storage Spaces Direct(S2D)](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-storage-spaces-direct-manually-configure?tabs=windows2012) or [Premium file share](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-premium-file-share-manually-configure?tabs=windows2012) 
- Create FCI client access using either VNN or DNN.
- [Upgrade FCI](https://docs.microsoft.com/sql/sql-server/failover-clusters/windows/upgrade-a-sql-server-failover-cluster-instance?view=sql-server-ver15)
- [High availability and disaster recovery](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/business-continuity-high-availability-disaster-recovery-hadr-overview) SQL Server on Azure VM