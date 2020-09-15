<properties
	pageTitle="Managed Instance - Not enough IP addresses"
	description="Managed Instance - Not enough IP addresses"
	infoBubbleText="Managed Instance cannot be created or scaled because there are no enough available IP addresses in subnet"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="a-nsehov"
	authors="a-nsehov"
	displayOrder=""
	diagnosticScenario="SqlMIProvisioning_NotEnoughIpAddresses"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-provisioning-not-enough-IP-addresses"
	ownershipId="AzureData_AzureSQLMI"
/>
# Managed Instance - Not enough IP addresses

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> doesn't have enough available IP addresses in its subnet so scaling or create operation in the subnet could not be performed.
<!--/issueDescription-->

## **Recommended Steps**

Careful planning of subnet size for your managed instance deployments is recommended. You can't resize the subnet after you deploy the resources inside. For more details visit: [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size).

* If you are trying to create a managed instance in the subnet with existing instances, create new subnet with more IP addresses allocated and deploy managed instance in the new subnet
* If you are trying to create a managed instance in an empty subnet, remove that subnet and create new one with enough IP addresses allocated. By design, a managed instance needs a minimum of 32 IP addresses in a subnet. As a result, you can use minimum subnet mask of /27 when defining your subnet IP ranges.
* If you are trying to scale managed instance, you will have to create a new subnet and a new managed instance inside it. We also suggest that the new subnet is created with more IP addresses allocated so future update operations will avoid similar situations. After the new instance is provisioned, you can manually back up and restore data between the old and new instances or perform [cross-instance point-in-time restore](https://docs.microsoft.com/azure/azure-sql/managed-instance/point-in-time-restore?tabs=azure-portal).

## **Recommended Documents**

* [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size)
* [Networking requirements - FAQ](https://docs.microsoft.com/azure/azure-sql/managed-instance/frequently-asked-questions-faq#networking-requirements)
* [Connectivity architecture for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview)
* [Create a virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template)
* [Configure an existing virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-existing-add-subnet)
