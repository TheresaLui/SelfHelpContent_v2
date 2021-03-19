<properties
	pageTitle="Managed Instance - Not enough IP addresses for creation"
	description="Managed Instance - Not enough IP addresses for creation"
	infoBubbleText="Managed Instance cannot be created because there are no enough available IP addresses in subnet"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="a-nsehov"
	authors="a-nsehov"
	displayOrder=""
	diagnosticScenario="SqlMIProvisioning"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-provisioning-not-enough-ip-addresses-for-creation"
	ownershipId="AzureData_AzureSQLMI"
/>
# Managed Instance - Not enough IP addresses for creation

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
You tried to create Managed Instance on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> in subnet that doesn't have enough available IP addresses, so create operation could not be performed.
<!--/issueDescription-->

## **Recommended Steps**

Careful planning of subnet size for your managed instance deployments is recommended. You can't resize the subnet after you deploy the resources inside. For more details visit: [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size).

* If you are trying to create a managed instance in the subnet with existing instances, create new subnet with more IP addresses allocated and deploy managed instance in the new subnet
* If you are trying to create a managed instance in an empty subnet, remove that subnet and create new one with enough IP addresses allocated. By design, a managed instance needs a minimum of 32 IP addresses in a subnet. As a result, you can use minimum subnet mask of /27 when defining your subnet IP ranges.

## **Recommended Documents**

* [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size)
* [Networking requirements - FAQ](https://docs.microsoft.com/azure/azure-sql/managed-instance/frequently-asked-questions-faq#networking-requirements)
* [Connectivity architecture for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview)
* [Create a virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template)
* [Configure an existing virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-existing-add-subnet)
