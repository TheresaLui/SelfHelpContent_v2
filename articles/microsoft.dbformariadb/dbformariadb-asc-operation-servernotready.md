<properties
	pageTitle="Operation Timed Out"
	description="Operation timed out because the backend is not ready to perform it."
	infoBubbleText="Found operation on MariaDB server failed because the backend is not ready to perform it. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="Xin-Cheng"
	ms.author="chengxin"
	displayOrder="100"
	articleId="dbformariadb-asc-operation-servernotready"
	diagnosticScenario="OrcasMariaDBOperationFailure"
	selfHelpType="rca"
	supportTopicIds="32640111, 32640121, 32640134, 32640137, 32640151, 32640159"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Operation on MariaDB failed because the backend is not ready to perform it.

<!--issueDescription-->
Thank you for contacting Microsoft support team. We have detected that your operation on MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> is timed out because the backend is not ready to perform it. Please wait for the server to be in ready state and retry your operation.
<!--/issueDescription-->

## **Recommended Steps**

* If you are using Azure portal, please check the server "Activity log" menu and make sure your previous operation succeeded and try your operation again
* If you are using Azure CLI, you can use `az mariadb server show --resource-group <resource group name> --name <server name> --subscription <subscription id>` to get the state of your server
* Wait for "userVisibleState" to read "Ready"
* If you are using ARM template, please make sure you execute your operations in serial. If deployment order is not specified, the Resource Manager deploys them in parallel. See how to [Define the order for deploying resources in Azure Resource Manager Templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-define-dependencies).

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/en-us/home?forum=AzureDatabaseforMariaDB)
* [Azure CLI for MariaDB](https://docs.microsoft.com/cli/azure/mariadb?view=azure-cli-latest)
* [Define the order for deploying resources in Azure Resource Manager Templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-define-dependencies)
