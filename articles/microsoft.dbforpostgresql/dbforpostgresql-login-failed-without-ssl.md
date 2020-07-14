<properties
	pageTitle="SSL connection errors"
	description="RCA - SSL connection errors RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="seanliang"
	displayOrder="100"
	articleId="dbforpostgresql-login-failed-without-ssl"
	diagnosticScenario="OrcasPostgresSSLNotSpecified"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Can't connect PostgreSQL database server because of SSL connection errors

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for PostgreSQL. During our investigation we determined that connections to your database server are failing because the server was configured to require an SSL connection and connection attempts to the server were made without SSL enabled on the connections.
<!--/issueDescription-->

## **Recommended steps**

1. To fix this issue, please ensure SSL is configured correctly on the server. You can refer to [this article](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security) for assistance with configuring your client applications to connect to Azure Database for PostgreSQL using SSL. You can download application libraries and connection instructions for many common languages [here](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries).
2. You can also obtain system-generated connection strings for common application libraries by navigating to your database server in the [Azure Portal](https://portal.azure.com) and click on the "**Connection Strings**" blade.

## **Recommended documents**

[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)

[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
