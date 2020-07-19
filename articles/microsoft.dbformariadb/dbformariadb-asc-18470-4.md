<properties
	pageTitle="Server could not be found"
	description="RCA - Server could not be found"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="haz"
	ms.author="haz"
	displayOrder="100"
	articleId="dbformariadb-asc-18470-4"
	diagnosticScenario="OrcasMariaDBServerNotFoundInBackend"
	selfHelpType="rca"
	supportTopicIds="32640117,32640118,32640120"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Can't connect MariaDB database server because the server could not be found

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for MariaDB. The Azure database for MariaDB service uses a gateway as the service endpoint to provide layered security, high availability, and elastic scaling of resources with minimal downtime. During our investigation we determined that connections to your database server are failing because the gateway cannot locate the server for the name specified as part of the user name.
<!--/issueDescription-->

## **Recommended Steps**

To fix this issue, please ensure you use {user_name}@{server_name} as the format for your user name. The {server_name} must be the name of the server you are trying to connect to. You can refer to [this article](https://docs.microsoft.com/azure/mariadb/howto-connection-string) for assistance with constructing a connection string for your Azure Database for MariaDB server.

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums)
