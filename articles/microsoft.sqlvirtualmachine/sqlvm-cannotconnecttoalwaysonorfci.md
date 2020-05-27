<properties
  pageTitle="cannot connect to sql server/alwayson or fci"
	description="cannot connect to sql server/alwayson or fci"
	infoBubbleText=""
	service="microsoft.compute"
	resource="virtualmachines"
	authors="vadeveka"
	ms.author="vadeveka"
	displayOrder=""
	articleId="sqlvirtualmachine-cannot connect to sql server-alwayson or fci"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32639652"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="AzureData_AzureSQLVM"
/>

# cannot connect to sql server/alwayson or fci

### **Unable to connect to AG listener from anywhere except the Primary replica node**

There could be several different reasons related to setup which can cause this issue:

* **Are you able to connect to the current Primary using the replica name (e.g. SQLVM1) from the secondary?**

  If not, please ensure that SQL Server service is up and running on the Primary replica. Ensure that all the ports required for the listener: SQL traffic (e.g. 1433), mirroring traffic (e.g. 5022), Load balancer probe port (e.g. 59999) are open in computer firewall and NSG for all replicas.<br>

* **Is the load balancer correctly configured?**

  Please ensure that a load balancer rule corresponding to the AG listener is [correctly configured](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#add-backend-pool-for-the-availability-group-listener). In Azure, a load balancer rule must be created for each AG listener.<br>

* **Have you ensured that the correct configuration changes have been made at WSFC level for the Load balancer and AG listener?**

  Please ensure that you have [run the PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#configure-listener) with correct variables as below.

  **NOTE**: After you run the PowerShell to configure the cluster parameters, you must take the AG resource offline and online to ensure modifications take effect. You need to run the PowerShell on one node (VM) of the cluster only.

  ```
  $ClusterNetworkName = "<MyClusterNetworkName>" # the cluster network name (Use Get-ClusterNetwork on Windows Server 2012 of higher to find the name)
  $IPResourceName = "<IPResourceName>" # the IP Address resource name
  $ListenerILBIP = "<n.n.n.n>" # the IP Address of the Internal Load Balancer (ILB). This is the static IP address for the load balancer you configured in the Azure portal.
  [int]$ListenerProbePort = <nnnnn>

  Import-Module FailoverClusters
  Get-ClusterResource $IPResourceName | Set-ClusterParameter -Multiple @{"Address"="$ListenerILBIP";"ProbePort"=$ListenerProbePort;"SubnetMask"="255.255.255.255";"Network"="$ClusterNetworkName";"EnableDhcp"=0}
  ```

* **Are the probe ports setup correctly for load balancer and the IP resource for listener?**

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
      <td>Cluster parameter named ProbePort<br> 59999</td>
    </tr>
  </table>
<br>


## **Recommended Documents**

* [Configure availability group on Azure SQL Server VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial)
* [Configure an availability group on Azure SQL Server VM in different regions](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-dr)
* [Connection Timeouts in Multi-subnet Availability Group](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Connection-Timeouts-in-Multi-subnet-Availability-Group/ba-p/318334)
* [Troubleshooting Availability Group Listener in Azure SQL VM](https://techcommunity.microsoft.com/t5/Premier-Field-Engineering/Trouble-shooting-Availability-Group-Listener-in-Azure-SQL-VM/ba-p/371317)
* [IaaS with SQL AlwaysOn - Tuning Failover Cluster Network Thresholds](https://techcommunity.microsoft.com/t5/SQL-Server-Support/IaaS-with-SQL-AlwaysOn-Tuning-Failover-Cluster-Network/ba-p/318322)
* [Guidelines for lease, cluster and health check timeouts](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-lease-healthcheck-timeout)

