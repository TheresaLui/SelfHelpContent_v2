<properties
	pageTitle="Server is Busy with Other Operations"
	description="Operation is failed because server is busy with other operations."
	infoBubbleText="Found operation on PostgreSQL server failed because server is busy with other operations. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="Xin-Cheng"
	ms.author="chengxin"
	displayOrder="100"
	articleId="dbforpostgresql-asc-operation-serverbusy"
	diagnosticScenario="OrcasPostgresOperationFailure"
	selfHelpType="rca"
	supportTopicIds="32639966, 32639980, 32639988, 32639998, 32640024, 32640028"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Operation on PostgreSQL failed because server is busy with other operations.

<!--issueDescription-->
Thank you for contacting Microsoft support team. We have detected that your operation on Azure Database for PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> is failed because your server is currently busy with other operations. Please wait for the server to be in ready state and retry your operation.
<!--/issueDescription-->

## **Recommended Steps**

* If you are using Azure portal, please check the server "Activity log" menu and make sure your previous operation succeeded and try your operation again.
* If you are using Azure CLI, you can use the following command to get the state of your server:
	`az postgres server show --resource-group <resource group name> --name <server name> --subscription <subscription id>`
and wait for the "userVisibleState" to be in ready state: 
	`"userVisibleState": "Ready"`

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-us/home?forum=AzureDatabaseforPostgreSQL)
* [Azure CLI for PostgreSQL](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest)
