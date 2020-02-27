<properties
	pageTitle="Connect to Server Failed Because of VNET"
	description="RCA - Connect to Server Failed Because of VNET RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="zhlian"
	authors="seanzqliang"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-vnet"
	diagnosticScenario="OrcasPostgresVnet"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public, blackForest, fairfax, mooncake"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect PostgreSQL database server because of VNET

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> during period of <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because of VNET. Virtual Network (VNET) service endpoints and rules extend the private address space of a Virtual Network to your Azure Database for PostgreSQL server.
<!--/issueDescription-->

## **Recommended Steps**

* If the Azure resources being connected via service endpoints are across two subscriptions, make sure that the two subscriptions are in same Active directory tenant and both of them have **Microsoft.SQL** resource provider registered

## **Recommended Documents**

* [How-to create user in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-create-users)
* [Azure Database for PostgreSQL Virtual network service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet)
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal)
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli)
