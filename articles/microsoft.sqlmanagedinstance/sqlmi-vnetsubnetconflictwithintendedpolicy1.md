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
We detected that a Managed Instance named **{ManagedInstanceResource}** in Resource Group **{RGname}** failed to deploy around **{eventTimestamp}** due to incorrect networking configuration on the subnet for Managed Instance, specifically with **{Message}**.
<!--/issueDescription-->

Azure SQL Database Managed Instance must be deployed within an Azure [virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-networks-overview) and the subnet dedicated for Managed Instances only. You can use the existing virtual network and subnet if it's configured according to the [Managed Instance virtual network requirements](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#network-requirements).

## **Recommended Steps**

If one of the following cases applies to you, you can validate and modify your network by using the script explained in [Configure an existing virtual network for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-configure-vnet-subnet): 

- You have a new subnet that's still not configured.
- You're not sure that the subnet is aligned with the [requirements](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#network-requirements).
- You want to check that the subnet still complies with the [network requirements](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#network-requirements) after you made changes.