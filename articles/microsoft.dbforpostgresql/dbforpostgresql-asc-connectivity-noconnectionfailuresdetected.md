<properties
	pageTitle="No connection failures detected within Azure Database for PostgreSQL"
	description="No connection failures detected within Azure Database for PostgreSQL"
	infoBubbleText="No connection failures detected within Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-noconnectionfailuresdetected"
	diagnosticScenario="OrcasPostgresNoSystemErrorsV2TroubleShooter"
	selfHelpType="diagnostics"
	supportTopicIds="32731217, 32639977"
	cloudEnvironments="public, blackForest, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# No connection failures detected within Azure Database for PostgreSQL

<!--issueDescription-->
Thank you for contacting Microsoft Support about connection issues to your PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->. Please note that we have checked our backend telemetry and noticed that there were no database-side errors in the provided time range <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC).
<!--/issueDescription-->

## **Recommended Steps**

Consider reviewing your client and application for potential connectivity issues or errors, like:

* Application-side firewall blocking outbound connections to port 5432 or to the Azure Database for PostgreSQL IP address. Consider temporarily testing connectivity with a public network.
* High resource utilization on the application
* Connection pool settings for maximum active and idle connections, timeouts
* DNS resolution issues
* [Client driver](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries)
