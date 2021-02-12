<properties
	pageTitle="How to questions: Virtual network or subnet configuration"
	description="How to questions: Virtual network or subnet configuration"
	infoBubbleText="Virtual networkor subnet configuration"
	service="microsoft.sql"
	resource="managedinstances"
	authors="srdan-bozovic-msft"
	ms.author="srbozovi"
	displayOrder=""
	articleId="ce5fb03d-13f4-4a46-b084-b00be90d4043"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637317,32637316,32748006"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	ownershipId="AzureData_AzureSQLMI"
/>

# Virtual network/subnet configuration

Azure SQL Managed Instance must be deployed within an Azure virtual network and the subnet dedicated for managed instances only. You can use the existing virtual network and subnet if they're configured according to the SQL Managed Instance virtual [network requirements](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview#service-aided-subnet-configuration).

If you have a new subnet that's still not configured, you're not sure that the subnet is aligned with the requirements or you want to check that the subnet still complies with the network requirements after you made changes, we recommend the [PowerShell script to validate and prepare the subnet](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-existing-add-subnet).

You can also create a [new network and subnet using a template](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template).

When you set up a failover group between SQL Managed Instances in two different regions, each instance is isolated using an independent virtual network. To allow replication traffic between these VNets ensure [these prerequisites](https://docs.microsoft.com/azure/azure-sql/database/auto-failover-group-overview?tabs=azure-powershell#enabling-geo-replication-between-managed-instances-and-their-vnets) are met.

There are a few scenarios (for example, [db mail](https://docs.microsoft.com/sql/relational-databases/database-mail/database-mail?view=sql-server-ver15), linked servers to other SQL Server instances in your cloud or hybrid environment) that require private host names to be resolved from SQL Managed Instance. In this case, you need to configure a [custom DNS inside Azure](https://docs.microsoft.com/azure/azure-sql/managed-instance/custom-dns-configure).

[Configuring SQL Managed Instance to function as a publisher and/or a distributor](https://docs.microsoft.com/azure/azure-sql/managed-instance/replication-between-two-instances-configure-tutorial) for transactional replication requires port 445 (TCP outbound) is open in the security rules of NSG for the managed instances to access the Azure file share.

[This article](https://docs.microsoft.com/azure/azure-sql/managed-instance/connect-application-instance) describes how to connect an application to Azure SQL Managed Instance in a number of different application scenarios.

## **Recommended Documents**

- [Connectivity architecture for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview)
- [Create a virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template)
- [Configure an existing virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-existing-add-subnet)