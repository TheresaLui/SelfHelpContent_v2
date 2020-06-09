<properties
	pageTitle="Failed to create instance due to incorrect networking configuration"
	description="Failed to create instance due to incorrect networking configuration due to NSG, RouteTable or ServiceEndpoints"
	infoBubbleText="Failed to create instance due to incorrect networking configuration due to NSG, RouteTable or ServiceEndpoints"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="vnetsubnetconflictwithintendedpolicy1"
	diagnosticScenario="sqlmi-vnetsubnetconflictwithintendedpolicy1"
	selfHelpType="diagnostics"
	supportTopicIds="32637218,32637232,32637269,32674897,32637301,32637315"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI"
/>
# We ran diagnostics on your subscription and found an issue

<!--issueDescription-->  
We detected that a Managed Instance named <!--$ManagedInstanceResource-->ManagedInstanceResource<!--/$ManagedInstanceResource--> in Resource Group <!--$RGname-->RGname<!--/$RGname--> failed to deploy around <!--$eventTimestamp-->eventTimestamp<!--/$eventTimestamp--> due to incorrect networking configuration on the subnet for Managed Instance, specifically with <!--$Message-->Message<!--/$Message-->
<!--/issueDescription-->

Azure SQL Database Managed Instance must be deployed within an Azure [virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-networks-overview) and the subnet dedicated for Managed Instances only. You can use the existing virtual network and subnet if it's configured according to the [Managed Instance virtual network requirements](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#network-requirements).

## **Recommended Steps**

## Validate and modify an existing virtual network

If you want to create a Managed Instance inside an **existing subnet**, we recommend the following PowerShell script to prepare the subnet:

```
$scriptUrlBase = 'https://raw.githubusercontent.com/Microsoft/sql-server-samples/master/samples/manage/azure-sql-db-managed-instance/delegate-subnet'

$parameters = @{
    subscriptionId = '<subscriptionId>'
    resourceGroupName = '<resourceGroupName>'
    virtualNetworkName = '<virtualNetworkName>'
    subnetName = '<subnetName>'
    }

Invoke-Command -ScriptBlock ([Scriptblock]::Create((iwr ($scriptUrlBase+'/delegateSubnet.ps1?t='+ [DateTime]::Now.Ticks)).Content)) -ArgumentList $parameters
```
The script prepares the subnet in three steps:

1. Validate: It validates the selected virtual network and subnet for Managed Instance networking requirements
2. Confirm: It shows the user a set of changes that need to be made to prepare the subnet for Managed Instance deployment and asks for consent
3. Prepare: It properly configures the virtual network and subnet

## Service-aided subnet configuration

To address customer security and manageability requirements Managed Instance is transitioning from manual to service-aided subnet configuration.

With service-aided subnet configuration user is in full control of data (TDS) traffic while Managed Instance takes responsibility to ensure uninterrupted flow of management traffic in order to fulfill SLA.

Service-aided subnet configuration builds on top of virtual network [subnet delegation](https://docs.microsoft.com/azure/virtual-network/subnet-delegation-overview) feature to provide automatic network configuration management and enable service endpoints. Service endpoints could be used to configure virtual network firewall rules on storage accounts that keep backups / audit logs.

### Network requirements 

Deploy a managed instance in a dedicated subnet inside the virtual network. The subnet must have these characteristics:

- **Dedicated subnet:** The managed instance's subnet can't contain any other cloud service that's associated with it, and it can't be a gateway subnet. The subnet can't contain any resource but the managed instance, and you can't later add other types of resources in the subnet.
- **Subnet delegation:** The managed instance's subnet needs to be delegated to `Microsoft.Sql/managedInstances` resource provider
- **Network security group (NSG):** A NSG needs to be associated with the managed instance's subnet. You can use an NSG to control access to the managed instance's data endpoint by filtering traffic on port 1433 and ports 11000-11999 when managed instance is configured for redirect connections. Service will automatically provision and keep current [rules](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#mandatory-inbound-security-rules-with-service-aided-subnet-configuration) required to allow uninterrupted flow of management traffic.
- **User defined route (UDR) table:** A UDR table needs to be associated with the managed instance's subnet. You can add entries to the route table to route traffic that has on-premises private IP ranges as a destination through the virtual network gateway or virtual network appliance (NVA). Service will automatically provision and keep current [entries](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#user-defined-routes-with-service-aided-subnet-configuration) required to allow uninterrupted flow of management traffic.
- **Sufficient IP addresses:** The managed instance subnet must have at least 16 IP addresses. The recommended minimum is 32 IP addresses. For more information, see [Determine the size of the subnet for managed instances](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-determine-size-vnet-subnet).   

You can deploy managed instances in [the existing network](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-configure-vnet-subnet) after you configure it to satisfy [the networking requirements for managed instances](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#network-requirements). Otherwise, create a [new network and subnet](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-vnet-subnet).
