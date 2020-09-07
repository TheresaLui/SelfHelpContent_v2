<properties
	pageTitle="Operation Timed Out"
	description="Operation timed out because the backend is not ready to perform it."
	infoBubbleText="Found operation on PostgreSQL server failed because the backend is not ready to perform it. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="Xin-Cheng"
	ms.author="chengxin"
	displayOrder="100"
	articleId="dbforpostgresql-asc-operation-servernotready"
	diagnosticScenario="OrcasPostgresOperationFailure"
	selfHelpType="rca"
	supportTopicIds="32639966, 32639980, 32639988, 32639998, 32640024, 32640028"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Operation on PostgreSQL failed because the backend is not ready to perform it.

<!--issueDescription-->
Thank you for contacting Microsoft support team. We have detected that your operation on PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> is timed out because the backend is not ready to perform it. Please wait for the server to be in ready state and retry your operation.
<!--/issueDescription-->

## **Recommended Steps**

* If you are using Azure portal, please check the server "Activity log" menu and make sure your previous operation is succeeded and try your operation again.
* If you are using Azure CLI, you can use the following command to get the state of your server:
	`az postgres server show --resource-group <resource group name> -name <server name> --subscription <subscription id>`
and wait for the "userVisibleState" to be in ready state: 
	`"userVisibleState": "Ready"`
* If you are using ARM template, please make sure you execute your operations in serial. (If deployment order is not specified, the Resource Manager deploys them in parallel.)  See how to [Define the order for deploying resources in Azure Resource Manager Templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-define-dependencies).

## **Recommended Documents**
* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-us/home?forum=AzureDatabaseforPostgreSQL)
* [Azure CLI for PostgreSQL](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest)
* [Define the order for deploying resources in Azure Resource Manager Templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-define-dependencies)
