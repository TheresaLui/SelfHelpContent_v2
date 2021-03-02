<properties
	pageTitle="Setup Availability Group"
	description="Setup Availability Group" 
	ms.author="vadeveka,amamun,ujpat, vasivara"
	articleId="c66d04df-8a03-4bd1-aa29-3b813d3cacaf" 
	selfHelpType="Apollo" 
  supportTopicIds="cbc61367-a1a4-0071-698c-df2a9d7ab579" 
  productPesIds="14745,16342" 
	cloudEnvironments="public,fairfax,usnat,ussec,blackforest,mooncake" 
	ownershipId="AzureData_AzureSQLVM" 
/>
# Setup Availability Group

## Resolve issues with Setup Availability Group

:::Section Metrics and Diagnostics:::  

### AG Failure diagnostics

<insight>
    <symptomId>SqlVmHADRPortalInsight</symptomId>
    <executionText>We are running a few performance checks on your VM</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>true</additionalInputsReq>
    <maxInsightCount>1</maxInsightCount>
    <failedText>We ran into an issue and could not complete this check</failedText>
</insight>

Most customers can resolve issues regarding setting up Always On Availability Group (AG) by using the following steps.


## **Recommended Steps**

:::Section Different ways to configure Availability Groups in Azure VMs:::
### Different ways to configure Availability Groups in Azure VMs

The following articles show the different ways to configure AGs. Review a [comparison of these configuration methods](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-overview#deployment).

* [Configure availability group pre-requisites](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-prerequisites-tutorial) and follow the steps for [Always on manual configuration](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial)
* [Use PowerShell or Az CLI to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-az-commandline-configure?tabs=azure-cli)
* [Use Azure Quick-start templates to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-quickstart-template-configure)
* [Configure availability group using Azure portal](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-azure-portal-configure?tabs=azure-cli)


:::Section Steps to avoid errors when configuring Availability Groups and Listener:::
### Steps to avoid errors when configuring Availability Groups and Listener

1. If you cannot join the database to the existing AG, review [this documentation](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Create-Availability-Group-Fails-With-Error-35250-Failed-to-join/ba-p/317987)

1. Make sure **Port** 1433 (SQL Port), 5022 (Endpoint Port) and 59999 (Load balancer Probe Port) are not blocked at NSG or Windows Firewall on all replicas. Try to create Inbound/Outbound rules accordingly.
 
1. Ensure that the NT AUTHORITY\SYSTEM account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all replicas participating in the availability group for Health Detection and for failing over your AG to another replica. 

1. If the **Create listener** fails with Message 19471 ("The WSFC cluster could not bring the Network Name resource online), see [this documentation](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online).

:::Section Unable to connect to AG listener from anywhere except the Primary replica node:::
### Unable to connect to AG listener from anywhere except the Primary replica node

1. Ensure that a load balancer rule corresponding to the AG listener is [configured](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#add-backend-pool-for-the-availability-group-listener). In Azure, a load balancer rule must be created for each AG listener. Ensure that **Floating IP** (direct server return) is enabled for the load balancer.<br>

1. Run the below powershell command
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

:::Section Recommended Documents:::
## **Recommended Documents**
* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15)
* [Configure a SQL Server Always On availability group across different Azure regions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-multiple-regions) to setup the Disaster Recovery Site.
* [Monitor and troubleshoot availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15)
