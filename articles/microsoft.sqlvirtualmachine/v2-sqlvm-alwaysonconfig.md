<properties
	pageTitle="AlwaysOn Availability Groups - Configuration"
	description="AlwaysOn Availability Groups - Configuration"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740063"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="3798c572-ddbe-495f-bb6a-894b9ad9efeb"
	ownershipId="AzureData_AzureSQLVM"
/>


# AlwaysOn Availability Groups - Configuration

### **Unable to Setup AG**

* **Error 35250: Failed to join database to existing SQL AG**

This failure could happen when the primary and secondary replicas are not able to communicate with each other. Review [these common failures and remedies](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Create-Availability-Group-Fails-With-Error-35250-Failed-to-join/ba-p/317987).


 * **Message 41131: Cannot setup SQL AG successfully**

Ensure that the *[NT AUTHORITY\SYSTEM]* account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on the participating replicas of the AG. This account is used by SQL Server AlwaysOn health detection to connect to the SQL Server node and to monitor health. 

### **Unable to Setup Listener**

If the create listener fails with Message 19471 'The WSFC cluster could not bring the Network Name resource online' please review [this document](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online).

### **Unable to connect to AG listener from anywhere except the Primary replica node**

There could be several different reasons related to setup which can cause this issue:

* **Are you able to connect to the current Primary using the replica name (e.g. SQLVM1) from the secondary?**

If not, please ensure that SQL Server service is up and running on the Primary replica. Ensure that all the ports required for the listener: SQL traffic (e.g. 1433), mirroring traffic (e.g. 5022), Load balancer probe port (e.g. 59999) are open in computer firewall and NSG for all replicas.<br>

* **Is the load balancer correctly configured?**

Please ensure that a load balancer rule corresponding to the AG listener is [correctly configured](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#add-backend-pool-for-the-availability-group-listener). In Azure, a load balancer rule must be created for each AG listener. Please ensure that Floating IP (direct server return) is enabled for the load balancer.<br>

* **Have you ensured that the correct configuration changes have been made at WSFC level for the Load balancer and AG listener?**

Please ensure that you have [run the PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#configure-listener) with correct variables as below:

```
$ClusterNetworkName = "<MyClusterNetworkName>" # the cluster network name (Use Get-ClusterNetwork on Windows Server 2012 of higher to find the name)
$IPResourceName = "<IPResourceName>" # the IP Address resource name
$ListenerILBIP = "<n.n.n.n>" # the IP Address of the Internal Load Balancer (ILB). This is the static IP address for the load balancer you configured in the Azure portal.
[int]$ListenerProbePort = <nnnnn>

Import-Module FailoverClusters
Get-ClusterResource $IPResourceName | Set-ClusterParameter -Multiple @{"Address"="$ListenerILBIP";"ProbePort"=$ListenerProbePort;"SubnetMask"="255.255.255.255";"Network"="$ClusterNetworkName";"EnableDhcp"=0}
```

**NOTE**: After you run the PowerShell to configure the cluster parameters, you must take the AG resource offline and online to ensure modifications take effect. You need to run the PowerShell on one node (VM) of the cluster only.

### **Unable to manually failover AG to another replica**
	
Ensure that the [NT AUTHORITY\SYSTEM] account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all the participating replicas of the AG. Watch from the cluster manager while you do the failover. Does the IP address and Network name come online? If not, most probably issue is outside of the SQL Server. 

## **Recommended Documents**

* [Configure Always On Availability Group in Azure VM manually](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial)<br>
* [Monitor and troubleshoot availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15)<br>
