<properties
	pageTitle="Operation Timed Out"
	description="Operation timed out because the backend is not ready to perform it."
	infoBubbleText="Found operation on MySQL server failed because the backend is not ready to perform it. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="Xin-Cheng"
	ms.author="chengxin"
	displayOrder="100"
	articleId="dbformysql-asc-operation-servernotready"
	diagnosticScenario="OrcasMySQLOperationFailure"
	selfHelpType="rca"
	supportTopicIds="32640044, 32640056, 32640071, 32640074, 32640089, 32640097"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Operation on MySQL failed because the backend is not ready to perform it.

<!--issueDescription-->
Thank you for contacting Microsoft support team. We have detected that your operation on MySQL server <!--$ServerName-->ServerName<!--/$ServerName--> is timed out because the backend is not ready to perform it. Please wait for the server to be in ready state and retry your operation.
<!--/issueDescription-->

## **Recommended Steps**

* If you are using Azure portal, please check the server "Activity log" menu and make sure your previous operation succeeded and try your operation again
* If you are using Azure CLI, you can use `az mysql server show --resource-group <resource group name> --name <server name> --subscription <subscription id>` to get the state of your server	
* Wait for "userVisibleState" to read "Ready"
* If you are using ARM template, please make sure you execute your operations in serial. If deployment order is not specified, the Resource Manager deploys them in parallel. See how to [Define the order for deploying resources in Azure Resource Manager Templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-define-dependencies).

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-us/home?forum=AzureDatabaseforMySQL)
* [Azure CLI for MySQL](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest)
* [Define the order for deploying resources in Azure Resource Manager Templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-define-dependencies)
