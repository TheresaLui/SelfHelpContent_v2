<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText=""
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="janeng"
	displayOrder="100"
	articleId="dbforpostgresql-asc-40613-16"
	diagnosticScenario="OrcasPostgresGatewayCannotStartProxyConneciton"
	selfHelpType="rca"
	supportTopicIds="32569391, 32569392"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public"
/>
# Can't connect PostgreSQL database server

<!--issueDescription-->
hank you for contacting Microsoft support about your connection issues with Azure Database for MySQL. The Azure database for PostgreSQL service uses a gateway as the service endpoint to provide layered security, high availability, and elastic scaling of resources with minimal downtime. During our investigation we found that the gateway was failing to establish connections to your host database server preventing you from connecting to your server. We have restarted the gateway and subsequently observed connections succeeding as expected. The issue has been forward to the engineering team for further monitoring and to determine a permanent fix.
<!--/issueDescription-->

## **Recommended steps**

1. Because the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement re-try logic. Please refer to our [documentation](https://docs.microsoft.com/azure/postgresql/concepts-high-availability) for more details.

## **Recommended documents**

[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)