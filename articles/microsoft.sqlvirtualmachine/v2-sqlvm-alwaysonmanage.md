<properties
	pageTitle="AlwaysOn Availability Groups - Manage or Troubleshoot"
	description="AlwaysOn Availability Groups - Manage or Troubleshoot"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740064"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="479bfcb0-d975-4810-b14e-1efc25532e7e"
	ownershipId="AzureData_AzureSQLVM"
/>

# AlwaysOn Availability Groups - Manage or Troubleshoot

### **Unable to manually failover AG to another replica**

	
Ensure that the [NT AUTHORITY\SYSTEM] account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all the participating replicas of the AG.<br>
Watch from the cluster manager while you do the failover. Does the IP address and Network name come online? If not, most probably issue is outside of the SQL Server. 

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


## **Recommended Documents**

* [Monitor and troubleshoot availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15)<br>
