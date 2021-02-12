<properties
  pagetitle="Windows Failover Cluster Service&#xD;"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740116"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="f5bd2334-5581-416e-91d7-5c125cf29d8d"
  ownershipid="AzureData_AzureSQLVM" />
# Windows Failover Cluster Service

Most customers are able to resolve their Windows Failover Cluster issues using the following steps. Most of the errors listed here can be found in the event viewer or cluster log.

## **Recommended Steps**

* **Event 1135:** Cluster node was removed from the cluster membership.

   Relax the [Cluster Network Threshold](https://techcommunity.microsoft.com/t5/sql-server-support/iaas-with-sql-alwayson-tuning-failover-cluster-network/ba-p/318322) and validate the communication between the nodes. Also check network connectivity or latency issues and make sure you have configured the [Windows Cluster Network](https://docs.microsoft.com/archive/blogs/askcore/configuring-windows-failover-cluster-networks).

* **Event 1196**: Network name resource failed registration of associated DNS name

     * Check the NIC settings for each of your cluster nodes to make sure there are no external DNS records present

    * Ensure the A record for your cluster exists on your internal DNS servers. If not, create a new A Record manual in DNS Server for the Cluster Access Control object and check the Allow any authenticated users to update DNS Records with the same owner name.
    
   * Take the Resource "Cluster Name" with IP Resource offline and fix it.

* **Availability Group Lease Timeout Error:**
    
  Relax the four [Cluster timeout values](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-lease-healthcheck-timeout?view=sql-server-ver15#updating-cluster-and-always-on-timeout-values). This issue can happen if you are having performance issues on your server. Upsizing the VM/Disk can also help. You can check for any [Disk/VM Throttling using Metrics](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows) on Azure Portal. [Learn more](https://docs.microsoft.com/archive/blogs/alwaysonpro/improved-alwayson-availability-group-lease-timeout-diagnostics#what-kind-of-health-issues-cause-lease-timeout).

* **Event 157 :** Disk has been surprised removed.

  This can happen if the Storage Spaces property `AutomaticClusteringEnabled` is set to `True` for an AG environment. Change it to `False`. Also, running a Validation Report with Storage option can trigger the disk reset or surprise removed event. The storage system [Throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics) can also trigger the disk surprise remove event.

* **Event 1206:** Cluster network name resource cannot be brought online. The computer object associated with the resource could not be updated in the domain.

   Make sure you have [appropriate permissions](https://techcommunity.microsoft.com/t5/sql-server-support/error-during-installation-of-an-sql-server-failover-cluster/ba-p/317873)

*    You may encounter issues while setting up a Windows failover cluster or its connectivity if you don't have [Cluster Service Ports open for communication](https://docs.microsoft.com/troubleshoot/windows-server/networking/service-overview-and-network-port-requirements#cluster-service)

   * If you are on Windows Server 2019 and you do not see a Windows Cluster IP, you have configured [Distributed Network Name](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-distributed-network-name-dnn-configure), which is only supported on SQL Server 2019. If you have previous versions of SQL Server, you can remove and [Recreate the Cluster using Network Name](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-the-cluster).

* **Failover [Clustering Events Errors and their Solutions](https://docs.microsoft.com/windows-server/failover-clustering/system-events)** are documented.

## **Recommended Documents**

* [Create Windows Failover Cluster](https://docs.microsoft.com/windows-server/failover-clustering/create-failover-cluster) and  [How to Troubleshoot Create Cluster Failures](https://techcommunity.microsoft.com/t5/failover-clustering/how-to-troubleshoot-create-cluster-failures/ba-p/371780)
* [SQL Failover Cluster Troubleshooting](https://docs.microsoft.com/sql/sql-server/failover-clusters/windows/failover-cluster-troubleshooting?view=sql-server-ver15)
 * [Premium File Share]( https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-premium-file-share-manually-configure?tabs=windows2012), [Storage Spaces Direct](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-storage-spaces-direct-manually-configure?tabs=windows2012) and [Azure Shared Disks](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/failover-cluster-instance-azure-shared-disks-manually-configure?tabs=windows2012)
