<properties
	pageTitle="Managed Instance - Not enough IP addresses for scaling"
	description="Managed Instance - Not enough IP addresses for scaling"
	infoBubbleText="Managed Instance cannot be scaled because there are no enough available IP addresses in subnet"
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
	articleId="sqlmanagedinstance-provisioning-not-enough-ip-addresses-for-scaling"
	ownershipId="AzureData_AzureSQLMI"
/>
# Managed Instance - Not enough IP addresses for scaling

## **There aren't enough available IP addresses in the subnet for scaling**

<!--issueDescription-->
We ran diagnostics on instance **<!--$ServerName-->ServerName<!--/$ServerName-->** between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC and we found that scaling could not be performed because there aren't enough available IP addresses in the subnet.
<!--/issueDescription-->

## **Recommended Steps**

Currently there is no way to complete the scaling operation in case there aren't enough IP addresses available. You will have to create a new subnet and a new managed instance inside it. It is not possible to change the subnet address range if any resource exists in the subnet. It is also not possible to move managed instances from one subnet to another.

After the new instance is provisioned, you can manually back up and restore data between the old and new instances or perform [cross-instance point-in-time restore](https://docs.microsoft.com/azure/azure-sql/managed-instance/point-in-time-restore?tabs=azure-portal).

Careful planning of subnet size for your managed instance deployments is recommended. We suggest that the new subnet is created with more IP addresses allocated so future update operations will avoid similar situations. For more details visit: [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size).

## **Recommended Documents**

* [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size)
* [Networking requirements - FAQ](https://docs.microsoft.com/azure/azure-sql/managed-instance/frequently-asked-questions-faq#networking-requirements)
* [Connectivity architecture for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview)
* [Create a virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template)
* [Configure an existing virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-existing-add-subnet)
