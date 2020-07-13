<properties
	pageTitle="Connections closed - Azure Database for PostgreSQL"
	description="Connections closed - Azure Database for PostgreSQL"
	infoBubbleText="Found recent connection close event"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-forcecloseconnections"
	diagnosticScenario="OrcasPostgresForceCloseConnectionsV2TroubleShooter"
	selfHelpType="diagnostics"
	supportTopicIds="32731217, 32639977"
	cloudEnvironments="public, blackForest, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Connection close events

<!--issueDescription-->
Our telemetry indicates that your server recently experienced connection closed events. Your client or application logs may show intermittent errors such as: An IO error occurred while sending to the backend (or other messages that indicate a timeout, write failure, or pipe error). On the other hand, the PostgreSQL logs show an error like: could not receive data from client. An existing connection was forcibly closed by the remote host. 

These two events are interrelated and are typically caused by connection handling issues on the client.
<!--/issueDescription-->

## **Recommended Steps**
* Learn more about [the cause of these errors and how to troubleshoot](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/troubleshoot-postgresql-an-existing-connection-was-forcibly/ba-p/925164)