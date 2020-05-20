<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="100"
	articleId="dbforpostgresql-asc-40613-16"
	diagnosticScenario="OrcasPostgresGatewayCannotStartProxyConneciton"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect PostgreSQL database server

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for PostgreSQL. The Azure database for PostgreSQL service uses a gateway as the service endpoint to provide layered security, high availability, and elastic scaling of resources with minimal downtime. During our investigation we found that the gateway was failing to establish connections to your host database server preventing you from connecting to your server. We have restarted the gateway and subsequently observed that connections are succeeding as expected. The issue has been forwarded to the engineering team for further monitoring and determining a permanent fix.
<!--/issueDescription-->

## **Recommended Steps**

* As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
