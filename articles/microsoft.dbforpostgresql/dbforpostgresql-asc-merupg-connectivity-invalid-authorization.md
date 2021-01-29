<properties
	pageTitle="Failed connections - invalid authorization specification"
	description="Failed connections - invalid authorization specification"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-merupg-connectivity-invalid-authorization"
	diagnosticScenario="OrcasMeruPGInvalidAuthorizationInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32639953, 32780838"
	productPesIds="17069"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Failed connections due to invalid authorization specification

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because of an invalid authorization specification. This error typically indicates a mismatch between the SSL settings on the Postgres server and the client making the connection.
<!--/issueDescription-->

## **Recommended Steps**

* Check the SSL settings on the client and server to confirm they correspond 