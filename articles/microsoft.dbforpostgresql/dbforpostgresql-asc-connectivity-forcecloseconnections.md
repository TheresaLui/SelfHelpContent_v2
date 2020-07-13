<properties
	pageTitle="Connections closed - Azure Database for PostgreSQL"
	description="Connections closed - Azure Database for PostgreSQL"
	infoBubbleText=""
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

Our telemetry indicates that your server recently experienced connection closed events. Your application logs may show intermittent errors such as “*An I/O error occurred while sending to the backend*” or other error messages that indicate a timeout, write failure, or a pipe error. On the other hand, the PostgreSQL logs show an error like *could not receive data from client: "An existing connection was forcibly closed by the remote host"*. 

These two events are interrelated and are typically caused by connection handling issues on the client.

## **Recommended Steps**
* Learn more about [the cause of these errors and how to troubleshoot](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/troubleshoot-postgresql-an-existing-connection-was-forcibly/ba-p/925164)