<properties
	pageTitle="VNET Is Not Supported on Basic Tier"
	description="RCA - VNET Is Not Supported on Basic Tier"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	ms.author="conwan"
	authors="congwang"
	displayOrder="100"
	articleId="dbformysql-asc-connectivity-vnet-basic"
	diagnosticScenario="OrcasMySQLVnetBasic"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect to MySQL server because of VNET

<!--issueDescription-->
During our investigation we found that your server <!--$ServerName-->ServerName<!--/$ServerName--> has connectivity issues between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC) because of VNET configuration errors. <!--$ServerName-->ServerName<!--/$ServerName--> is a Basic tier server and does not support virtual network service endpoints.
<!--/issueDescription-->

## **Recommended Steps**

* Use the General Purpose and Memory Optimized tiers in Azure Database for MySQL, since they support virtual network rules.

## **Recommended Documents**

* [Pricing tiers in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)
* [Azure Database for MySQL Virtual network service endpoints](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet)
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli)
