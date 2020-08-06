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
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect to PostgreSQL server because of maximum connection limit

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because the server was already at its [maximum number of connections](https://docs.microsoft.com/azure/postgresql/concepts-limits).
<!--/issueDescription-->

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections. We recommend using a connection pooler like [PgBouncer](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/not-all-postgres-connection-pooling-is-equal/ba-p/825717) to manage connections.
* Ensure you have chosen a compute tier that can support the maximum number of connections required by the application. See the [limits article](https://docs.microsoft.com/azure/postgresql/concepts-limits) for more information.

## **Recommended Documents**

* [Not all Postgres connection pooling is equal](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/not-all-postgres-connection-pooling-is-equal/ba-p/825717)
* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
