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
	cloudEnvironments="public, blackForest, fairfax, mooncake"
/>
# Can't connect PostgreSQL database server because of running out connections

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> connection to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> failed during period of <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because server ran out of connections.
<!--/issueDescription-->

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections. We recommend using a connection pooler like PgBouncer to manage connections.
* Ensure you have chosen a compute tier that can support the maximum number of connections required by the application

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
