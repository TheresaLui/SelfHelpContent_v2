<properties
	pageTitle="Server connection limit exhausted"
	description="Server ran out of available connections"
	infoBubbleText="Found recent connection failure. See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-merupg-connectivity-outofconnections"
	diagnosticScenario="OrcasMeruPGOutofConnectionsInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32639953"
	resourceTags=""
	productPesIds="17069"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Server connection limit exhausted

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because the server was already at its maximum number of connections.
<!--/issueDescription-->

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections 
* We recommend using a connection pooler like [PgBouncer](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/not-all-postgres-connection-pooling-is-equal/ba-p/825717) to manage connections
* Scale up to a compute tier that can support more connections
