<properties
	pageTitle="VNET Is Not Supported on Basic Tier"
	description="RCA - VNET Is Not Supported on Basic Tier RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="zhlian"
	authors="seanzqliang"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-vnet-basic"
	diagnosticScenario="OrcasPostgresVnetBasic"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect to PostgreSQL server because of VNET

<!--issueDescription-->
PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> is a Basic tier server and does not support virtual network service endpoints. There are <!--$Count-->Count<!--/$Count--> failed connections to this server between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) as a result.
<!--/issueDescription-->

## **Recommended Steps**

* Use the General Purpose and Memory Optimized tiers in Azure Database for PostgreSQL, since they support virtual network rules.

## **Recommended Documents**

* [Pricing tiers in Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)
* [Azure Database for PostgreSQL Virtual network service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet)
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal)
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli)
