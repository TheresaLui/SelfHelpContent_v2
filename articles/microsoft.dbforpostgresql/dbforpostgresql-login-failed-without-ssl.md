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
	supportTopicIds="32569392"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public"
/>
# Can't connect PostgreSQL database server because of SSL connection errors

<!--issueDescription-->
Thanks for contacting Microsoft support about your connection issues with Azure Database for PostgreSQL. During our investigation with you we determined that the database server was configured to require an SSL connection, but connection attempts to the server did not specify SSL resulting in a connection error and no connection.
<!--/issueDescription-->

## **Recommended steps**
1. To fix this issue please ensure SSL is configured correctly on the server, you can visit [this article](https://docs.microsoft.com/en-us/azure/postgresql/concepts-ssl-connection-security) for assistance and that your clients are configured to connected to Azure Database for PostgreSQL using SSL. Some common application libraries and instructions to do this are located [here](https://docs.microsoft.com/en-us/azure/postgresql/concepts-connection-libraries). 
2. You can also navigate to your database server on the [Azure Portal](https://portal.azure.com) and click on the **Connection Strings blade** to obtain some system generated connection strings for common application libraries

## **Recommended documents**
[Azure Database for PostgreSQL](https://azure.microsoft.com/en-us/services/postgresql/)

[Discussion forum](https://social.msdn.microsoft.com/Forums/azure/en-US/home?forum=ssdsgetstarted)