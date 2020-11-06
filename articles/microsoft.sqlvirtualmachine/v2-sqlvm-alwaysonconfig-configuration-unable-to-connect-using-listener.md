<properties
	pageTitle="AlwaysOn Availability Groups - Unable to connect using Listener"
	description="AlwaysOn Availability Groups - Unable to connect using Listener"
	infoBubbleText="AlwaysOn Availability Groups - Unable to connect using Listener"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740063"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="7acae9d0-64ac-41d2-9d8a-181212c60482"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you.

<!--issueDescription-->
Below Steps can help you to troubleshoot why you are not able to connect to the Listener
<!--/issueDescription-->

## **Recommended Steps**

- **90 Percent of Listener connectivity issues are Resolved by following the Below**

   * On Azure virtual machines, a SQL Server Availability Group requires a Load Balancer to be configured correctly or else listener connectivity may fail. Please check the [Load balancer Configuration](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer)

   * Make sure **Floating IP** is enabled when you configure the Load Balancing Rule.

   * To avoid issues with Listener Connectivity, Make sure **Ports** **1433** (SQL Instance Port), **5022** (Mirroring Endpoint), **59999** (Probe Port). You can [Telnet](https://docs.microsoft.com/windows-server/administration/windows-commands/telnet) to the Port or use [Test-NetConnection](https://docs.microsoft.com/powershell/module/nettcpip/test-netconnection?view=win10-ps#example-3--test-tcp-connectivity-and-display-detailed-results) to check
  are not blocked at **NSG or Windows Firewall**. Make sure SQL instance is not using [Dynamic Ports](https://docs.microsoft.com/sql/tools/configuration-manager/tcp-ip-properties-ip-addresses-tab?view=sql-server-ver15#dynamic-ports)


   * Most of the times Listener connectivity fails if you haven't supplied the correct values when you [Run the PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#configure-listener). Please make sure you have supplied the correct values in the below script:
    
     ```
     $ClusterNetworkName = "<MyClusterNetworkName>" # the cluster network name (Use Get-ClusterNetwork on Windows Server 2012 of 
     higher to find the name)
     $IPResourceName = "<IPResourceName>" # the IP Address resource name
     $ListenerILBIP = "<n.n.n.n>" # the IP Address of the Internal Load Balancer (ILB). This is the static IP address for the load 
     balancer you configured in the Azure portal.
     [int]$ListenerProbePort = <nnnnn>

     Import-Module FailoverClusters
     Get-ClusterResource $IPResourceName | Set-ClusterParameter -Multiple 
     @{"Address"="$ListenerILBIP";"ProbePort"=$ListenerProbePort;"SubnetMask"="255.255.255.255";
     "Network"="$ClusterNetworkName";"EnableDhcp"=0}
     ```
      **NOTE**: After you run the PowerShell to configure the cluster parameters, you must take the AG resource offline and online to ensure modifications take effect. You need to run the PowerShell on one node (VM) of the cluster only.
       
   * If you are connecting outside from a different network or On-Premise, make sure that your company firewall is not blocking these connections(Check with your **Network Admin**).

   * Make Sure your instance is enabled for TCP/IP Communication and has the [Listen All](https://docs.microsoft.com/sql/tools/configuration-manager/tcp-ip-properties-ip-addresses-tab?view=sql-server-ver15#options) property set. Make sure browser service is running.

   * If you are not able to connect to listener then you can try to connect using SSMS WITH various combinations like (Listener name ,Port) or (Listener IP, Port) to make sure you are not having and DNS name resolution issues. Check on DNS Server, the record for the Listener still exists and is pointing to the correct IP Address.

  * You may see issues connecting to listener if your AG Failed over and does not come online due to [Lease Timeout](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-lease-healthcheck-timeout?view=sql-server-ver15#updating-cluster-and-always-on-timeout-values) or if you are having issues with [SQL Performance](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices) or [Disk or VM Throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows). Check SQL Error log to find out more.
  

## **Recommended Documents**

* [Configure Load Balancer and Listener Correctly](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer)
* [Configure load balancer for AG VNN listener](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-vnn-azure-load-balancer-configure)

