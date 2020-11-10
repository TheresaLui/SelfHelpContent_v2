<properties
	pageTitle="SSL connection errors"
	description="RCA - SSL connection errors RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="janeng"
	authors="jan-eng"
	displayOrder="100"
	articleId="dbforpostgresql-asc-18456-100"
	diagnosticScenario="OrcasPostgresSSLNotSpecified"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect PostgreSQL database server because of SSL connection errors

<!--issueDescription-->
There have been failed connections to your database server because the server was configured to require an SSL connection and connection attempts to the server were made without SSL enabled on the connections.
<!--/issueDescription-->

## **Recommended Steps**

* To fix this issue, please ensure SSL is configured correctly on the server. You can refer to [this article](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security) for assistance with configuring your client applications to connect to Azure Database for PostgreSQL using SSL. You can download application libraries and connection instructions for many common languages [here](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries).
* You can also obtain system-generated connection strings for common application libraries by navigating to your database server in the [Azure Portal](https://portal.azure.com) and click on the "**Connection Strings**" blade.
* As a part of our maintenance activity, we are working on changing out gateway certificate used to [connect to the server using SSL](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security). Refer to the steps to mitigate the issue in [this article](https://docs.microsoft.com/azure/postgresql/concepts-certificate-rotation)

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
