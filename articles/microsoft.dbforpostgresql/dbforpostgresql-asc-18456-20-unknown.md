<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="janeng"
	displayOrder="100"
	articleId="dbforpostgresql-asc-18456-20-unknown"
	diagnosticScenario="OrcasPostgresBackendErrorUnKnownReasons"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect PostgreSQL database server

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our initial investigation we determined that the server was restarted between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->, causing <!--$Count-->Count<!--/$Count--> connection attempts to fail. We have forwarded the issue to the PostgreSQL engineering team for further investigation. We will reach back out to you with more information shortly.
<!--/issueDescription-->

## **Recommended Steps**

* As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) for more details.

## **Recommended Documents**

*[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
*[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
