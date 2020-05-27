<properties
	pageTitle="Create or Drop Resources/Virtual cluster"
	description="Create or Drop Resources/Virtual cluster"
    infoBubbleText="Create or Drop Resources/Virtual cluster"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32637315"
    resourceTags=""	
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="d4295119-cb4d-495f-b99f-df8e109b4689"
	ownershipId="AzureData_AzureSQLMI"
/>

# Delete Virtual Cluster

Managed instance at a high level is a set of service components hosted on a dedicated set of isolated virtual machines that run inside the customer’s virtual network subnet forming a [virtual cluster](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#high-level-connectivity-architecture).

## **Recommended Steps**

Each virtual cluster can contain multiple managed instances in the same subnet. Upon deletion of the last managed instance in the same subnet, the virtual cluster that has contained these instances is kept for customers free of charge for the next 12 hours. This behavior is provided by design to enable faster creation of managed instance in the same subnet. During this period, the subnet associated with the virtual cluster can't be deleted.
 
Immediate release of the subnet used by an empty virtual cluster is now possible through option to manually delete the virtual cluster using [Azure Portal](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-delete-virtual-cluster) and [API](https://docs.microsoft.com/rest/api/sql/virtualclusters/delete). This allows for immediate release of subnet used by managed instances hosted in the virtual cluster.

## **Recommended Documents**

* [Managed instance high-level connectivity architecture](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connectivity-architecture#high-level-connectivity-architecture)
* [Delete subnet after deleting Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-delete-virtual-cluster)
