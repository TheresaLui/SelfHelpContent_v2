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
	productPesIds="16222"
	cloudEnvironments="public, blackForest, fairfax, mooncake"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect PostgreSQL database server because of VNET

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> failed during the period of <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because of VNET. Client connections to Basic tier servers through Virtual Network Service Endpoints are not supported. Virtual Network Service Endpoints are supported for General Purpose and Memory Optimized severs.
<!--/issueDescription-->

## **Recommended Steps**

* Ensure that your Azure Database for PostgreSQL is deployed in General Purpose and Memory Optimized servers. The Basic tier does not support VNet service endpoints.

## **Recommended Documents**

* [Pricing tiers in Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)
* [Azure Database for PostgreSQL Virtual network service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet)
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal)
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli)
