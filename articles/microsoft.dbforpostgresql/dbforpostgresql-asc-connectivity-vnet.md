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
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect to PostgreSQL server because of VNET

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because of VNET configuration errors. 
<!--/issueDescription-->

## **Recommended Steps**
* If the Azure resources being connected via service endpoints are across two subscriptions, make sure that the two subscriptions are in same Active Directory tenant and both of them have **Microsoft.SQL** resource provider registered

## **Recommended Documents**

* [Azure Database for PostgreSQL Virtual network service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet)
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal)
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli)
