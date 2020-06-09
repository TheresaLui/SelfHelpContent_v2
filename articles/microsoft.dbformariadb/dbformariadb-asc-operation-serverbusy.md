<properties
	pageTitle="Server is Busy with Other Operations"
	description="Operation is failed because server is busy with other operations."
	infoBubbleText="Found operation on MariaDB server failed because server is busy with other operations. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="Xin-Cheng"
	ms.author="chengxin"
	displayOrder="100"
	articleId="dbformariadb-asc-operation-serverbusy"
	diagnosticScenario="OrcasMariaDBOperationFailure"
	selfHelpType="rca"
	supportTopicIds="32640111, 32640121, 32640134, 32640137, 32640151, 32640159"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Operation on MariaDB failed because server is busy with other operations.

<!--issueDescription-->
Thank you for contacting Microsoft support team. We have detected that your operation on Azure Database for MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> is failed because your server is currently busy with other operations. Please wait for the server to be in ready state and retry your operation.
<!--/issueDescription-->

## **Recommended Steps**

* If you are using Azure portal, please check the server "Activity log" menu and make sure your previous operation succeeded and try your operation again
* If you are using Azure CLI, you can use `az mariadb server show --resource-group <resource group name> --name <server name> --subscription <subscription id>` to get the state of your server
* Wait for "userVisibleState" to read "Ready"

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/en-us/home?forum=AzureDatabaseforMariaDB)
* [Azure CLI for MariaDB](https://docs.microsoft.com/cli/azure/mariadb?view=azure-cli-latest)
