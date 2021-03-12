<properties
	pageTitle="AlwaysOn Availability Groups - Configuration - Common Errors"
	description="AlwaysOn Availability Groups - Configuration - Common Errors"
	infoBubbleText="AlwaysOn Availability Groups - Configuration - Common Errors"
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
	articleId="d68de188-b871-4571-8af2-7bb4c8cbe8ed"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 

 
<!--issueDescription--> 

Most users can resolve **Common errors encountered when Configuring Availability Groups** by using the following information.

<!--/issueDescription--> 

 
## **Recommended Steps** 

* **Steps to Follow to Avoid any Errors when Configuring Availability Groups and Listener** 

1. If you cannot **Join the database to existing AG**, see [this documentation](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Create-Availability-Group-Fails-With-Error-35250-Failed-to-join/ba-p/317987) 

2. Make sure Port 1433 (SQL Port), 5022 (endpoint port), and 59999 (load balancer probe port) are not blocked at NSG or Windows Firewall on all replicas. Try to create Inbound/Outbound rules accordingly. 

3. Ensure that the **[NT AUTHORITY\SYSTEM]** account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all replicas participating in Availability Group for Health Detection, and for failing over your AG to another replica. 

4. If the **Create Listener** fails with error message 19471, "The WSFC cluster could not bring the Network Name resource online," review [this document](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online). 

 * **Unable to connect to AG listener from anywhere except the Primary replica node** 

1. Ensure that a load balancer rule corresponding to the AG listener is [configured](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#add-backend-pool-for-the-availability-group-listener). In Azure, a load balancer rule must be created for each AG listener. Ensure that **floating IP** (direct server return) is enabled for the load balancer.<br> 

 2. Run the below powershell command to correctly setup your AG listener

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

## **Recommended Documents** 

* [Monitor and troubleshoot availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15) 
* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15) 
* [Use Cloud Witness For Quorum](https://docs.microsoft.com/windows-server/failover-clustering/deploy-cloud-witness) 
* [Add a Replica to Always On](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/use-the-add-replica-to-availability-group-wizard-sql-server-management-studio?view=sql-server-ver15) 
* [Join a Secondary Replica to Always On AG](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/join-a-secondary-replica-to-an-availability-group-sql-server?view=sql-server-ver15) 

