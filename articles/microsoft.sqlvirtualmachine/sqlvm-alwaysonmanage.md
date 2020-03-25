<properties
	pageTitle="alwayson hadr/alwayson manage"
	description="alwayson hadr/alwayson manage"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="yareyes"
	authors="yareyes"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32633487, 32633488"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	articleId="98ae2e56-780c-45ab-abe7-677f66ad56f9"
	ownershipId="AzureData_AzureSQLVM"
/>

# alwayson hadr/alwayson manage

### **Unable to connect to AG listener from anywhere except the Primary replica node**

There could be several different reasons related to setup which can cause this issue:

* **Are you able to connect to the current Primary using the replica name (e.g. SQLVM1) from the secondary?**

If not, please ensure that SQL Server service is up and running on the Primary replica. Ensure that all the ports required for the listener: SQL traffic (e.g. 1433), mirroring traffic (e.g. 5022), Load balancer probe port (e.g. 59999) are open in computer firewall and NSG for all replicas.<br>

* **Is the load balancer correctly configured?**

Please ensure that a load balancer rule corresponding to the AG listener is [correctly configured](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#add-backend-pool-for-the-availability-group-listener). In Azure, a load balancer rule must be created for each AG listener.<br>

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

Common setup issues are caused when there is a mismatch in Load balancer probe port and corresponding Probe port parameter setup on IP Resource for the listener on WSFC. Every AG listener will have corresponding Azure Load balancer rule and IP resource under the AG role.

**NOTE**: Values provided are sample values.

<table style="width:100%">
 <tr>
          <th>AG listener</th>
          <td>IP for listener<br> 10.0.0.17</td>
          <td colspan="2">SQL connection port<br> 1433</td>
          <td></td>
        </tr>
        <tr>
          <th>Azure LB rule</th>
          <td>Frontend IP<br> 10.0.0.17</td>
          <td>TCP Port<br> 1433</td>
          <td>Backend Port<br> 1433</td>
          <td>Health probe port<br> 59999</td>
        </tr>
        <tr>
          <th>WSFC IP resource for AG role</th>
          <td>Static IP address<br> 10.0.0.17</td>
          <td colspan="2">Not applicable</td>
          <td>Cluster parameter named - ProbePort<br> 59999</td>
        </tr>
      </table><br>

### **Warnings on WSFC validation report asks to include multiple NICs on Azure VM**

Please remove any additional NICs you may have on each VM. On a physical on-premises failover cluster, we recommend multiple NICs per server (cluster node) and separate subnets with separate switches to eliminate any single points of failure. On an Azure IaaS VM guest failover cluster, we recommend a single NIC per server (cluster node) and a single subnet. Azure networking has physical redundancy which makes additional NICs and subnets unnecessary on an Azure IaaS VM guest cluster. Although the cluster validation report will issue a warning that the nodes are only reachable on a single network, this warning can be safely ignored on Azure IaaS VM guest failover clusters.

### **Setup Always ON in Azure VM with Azure CLI**

You can [use CLI commands to setup Always ON](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-availability-group-cli) from scratch on participating nodes. These commands will create a WSFC between the nodes and setup AG listener for use. Note that you will be required to have [registered the VM with SQL VM Resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb#register-sql-server-vm-with-sql-resource-provider) prior to setting up Always ON.

### **Cannot setup SQL AG successfully**

Ensure that the *[NT AUTHORITY\SYSTEM]* account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on the participating replicas of the AG. This account is used by SQL Server AlwaysOn health detection to connect to the SQL Server node and to monitor health. 

### **Failed to join database to existing SQL AG**

This failure could happen when the primary and secondary replicas are not able to communicate with each other. Review [these common failures and remedies](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Create-Availability-Group-Fails-With-Error-35250-Failed-to-join/ba-p/317987).

### **Failed to create SQL AG Listener or bring it online**

Creation of AG listener could fail because of [insufficient permissions](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Create-Listener-Fails-with-Message-The-WSFC-cluster-could-not/ba-p/318235) to create or change AD computer object on Cluster Name object (CNO), invalid IP address provided for listener, domain policy violations etc.

### **Unable to manually failover AG to another replica**

Watch from the cluster manager while you do the failover. Does the IP address and Network name come online? If not, most probably issue is outside of the SQL Server. 
	
Ensure that the SQL service on participating nodes is running under the same domain account. Also, ensure that the [NT AUTHORITY\SYSTEM] account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all the participating replicas of the AG.

### **Failure in SQL AG due to nodes being removed from cluster membership**

Some time failures in cluster logs with error 1135 can occur causing SQL AG failures because of low monitoring thresholds of WSFC. On IaaS setup of WSFC, it is recommended to [relax these thresholds](https://techcommunity.microsoft.com/t5/SQL-Server-Support/IaaS-with-SQL-AlwaysOn-Tuning-Failover-Cluster-Network/ba-p/318322).

## **Recommended Documents**

* [Configure Always On Availability Group in Azure VM manually](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial)<br>
