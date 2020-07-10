<properties
	pageTitle="Server could not be found"
	description="RCA - Server could not be found"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	ms.author="jan-eng"
		displayOrder="100"
	articleId="dbformysql-asc-18470-4"
	diagnosticScenario="OrcasMySQLServerNotFoundInBackend"
	selfHelpType="rca"
	supportTopicIds="32628367"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect MySQL database server because the server could not be found

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for MySQL. The Azure database for MySQL service uses a gateway as the service endpoint to provide layered security, high availability, and elastic scaling of resources with minimal downtime. During our investigation we determined that connections to your database server are failing because the gateway cannot locate the server for the name specified as part of the username.
<!--/issueDescription-->

## **Recommended Steps**

To fix this issue, please ensure you use {user_name}@{server_name} as the format for your username. The {server_name} must be the name of the server you are trying to connect to. You can refer to [this article](https://docs.microsoft.com/azure/mysql/howto-connection-string) for assistance with constructing a connection string for your Azure Database for MySQL server.

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
