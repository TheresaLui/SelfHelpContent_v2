<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="janeng"
	displayOrder="100"
	articleId="dbforpostgresql-asc-18456-20-known"
	diagnosticScenario="OrcasPostgresBackendErrorKnownReasons"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public"
/>
# Can't connect PostgreSQL database server

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we determined that the server was restarted between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->, causing <!--$Count-->Count<!--/$Count--> connection attempts to fail. The server restarted because <!--$FailureCause-->FailureCause<!--/$FailureCause-->.
<!--/issueDescription-->

## **Recommended steps**

1. Errors like the above are transient in nature and your database server will come back online automatically. Please try to reconnect to your server to see if the server is back online.
2. As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/postgresql/concepts-high-availability) for more details.

## **Recommended documents**

[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)

[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)