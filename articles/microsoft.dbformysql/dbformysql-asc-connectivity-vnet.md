<properties
	pageTitle="Connect to Server Failed Because of VNET"
	description="RCA - Connect to Server Failed Because of VNET"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	ms.author="conwan"
	authors="congwang"
	displayOrder="100"
	articleId="dbformysql-asc-connectivity-vnet"
	diagnosticScenario="OrcasMySQLVnet"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect to MySQL server because of VNET

<!--issueDescription-->
During our investigation we found that your server <!--$ServerName-->ServerName<!--/$ServerName--> has connectivity issues between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC) because of VNET configuration errors. 
<!--/issueDescription-->

## **Recommended Steps**
* If the Azure resources being connected via service endpoints are across two subscriptions, make sure that the two subscriptions are in the same Active Directory tenant and both of them have **Microsoft.SQL** resource provider registered

## **Recommended Documents**

* [Azure Database for MySQL Virtual network service endpoints](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet)
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli)
