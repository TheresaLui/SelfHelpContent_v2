<properties
	pageTitle="VNET Is Not Supported on Basic Tier"
	description="RCA - VNET Is Not Supported on Basic Tier"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	ms.author="conwan"
	authors="congwang"
	displayOrder="100"
	articleId="dbformariadb-asc-connectivity-vnet-basic"
	diagnosticScenario="OrcasMariaDBVnetBasic"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public, blackForest, fairfax, mooncake"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Can't connect to MariaDB server because of VNET

<!--issueDescription-->
MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> is a Basic tier server and does not support virtual network service endpoints. There are <!--$Count-->Count<!--/$Count--> failed connections to this server between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC) as a result.
<!--/issueDescription-->

## **Recommended Steps**

* Use the General Purpose and Memory Optimized tiers in Azure Database for MariaDB, since they support virtual network rules.

## **Recommended Documents**

* [Pricing tiers in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers)
* [Azure Database for MariaDB Virtual network service endpoints](https://docs.microsoft.com/azure/mariadb/concepts-data-access-and-security-vnet)
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-using-portal)
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-using-cli)
