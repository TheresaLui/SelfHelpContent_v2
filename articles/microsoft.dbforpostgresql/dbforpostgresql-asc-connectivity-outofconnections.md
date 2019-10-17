<properties
	pageTitle="Running Out of Connections"
	description="RCA - Running Out of Connections RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="janeng"
	ms.author="janeng"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-outofconnections"
	diagnosticScenario="OrcasPostgresOutofConnectionsInsightV2TroubleShooter"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public"
/>
# Can't connect PostgreSQL database server because of running out connections

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that <!--$Count-->Count<!--/$Count--> connection attempts to fail due to connections to your database server have been running out between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->.
<!--/issueDescription-->

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections. We recommend using a connection pooler like PgBouncer to manage connections.
* Ensure you have chosen a compute tier that can support the maximum number of connections required by the application

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
