<properties
	pageTitle="AlwaysOn Availability Groups - Setup Listener and Load Balancer"
	description="AlwaysOn Availability Groups - Setup Listener and Load Balancer"
	infoBubbleText="AlwaysOn Availability Groups - Setup Listener and Load Balancer"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740063,32740109"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="1d6f8725-f391-4668-9a5b-7d352b7806e7"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 


<!--issueDescription--> 
Most users can find sufficient information for **Setting up Listener and a load balancer for Availability Groups** by using the following steps.


<!--/issueDescription--> 

## **Recommended Steps** 

* **Configuring Listener for Availability Groups** 

1. [Configure Listener](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#configure-listener). If you are using SQL 2019 CU8+ on Windows 2016, you can use [DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-distributed-network-name-dnn-listener-configure) instead of a load balancer. 

2. If the **Create Listener fails or you are unable to bring Listener online** with error message 19471, "The WSFC cluster could not bring the Network Name resource online," review [this document](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online). 

3. **Listener may not show up** in SSMS. Make sure you [add Listener dependency](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#configure-listener) to AG Resource to ensure that it shows up in SSMS. 


- **Configuring Load Balancer using Azure Portal** 

1. On Azure virtual machines, a SQL Server availability group requires a [Load Balancer to be configured](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer). Make sure Floating IP is enabled when you configure the Load Balancing Rule. 

2. Run the below helper script. 

	```
	Import-Module FailoverClusters;
	$AGName = $ScopingAGName;
	$AGProbePort = $ScopingAGProbePort;
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


* **Things to Keep in Mind when Configuring Listener or Load Balancer** 

  * Multiple listeners can [use the same port (example 1433)](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-listener-overview?view=sql-server-ver15#SelectListenerPort), but they must use a different probe port (for example, 59999 or 59998) 
   * The load balancer probe port (for example, 59999) must use a free port. 
   *  Make sure that the SQL instance port (for example, 1433), mirroring endpoint (for example, 5022), probe port (for example, 59999) are open in [NSG](https://docs.microsoft.com/azure/virtual-machines/windows/nsg-quickstart-portal#create-an-inbound-security-rule) and [Firewall](https://docs.microsoft.com/windows/security/threat-protection/windows-firewall/create-an-inbound-port-rule). You can [telnet](https://docs.microsoft.com/windows-server/administration/windows-commands/telnet) to the port or use [Test-NetConnection](https://docs.microsoft.com/powershell/module/nettcpip/test-netconnection?view=win10-ps#example-3--test-tcp-connectivity-and-display-detailed-results) to check that the connections are not blocked at **NSG or Windows Firewall**.  


## **Recommended Documents** 

* [Create Standard SKU Load Balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-load-balancer-portal-configure) 
* [Configure load balancer for AG VNN listener](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-vnn-azure-load-balancer-configure) 
