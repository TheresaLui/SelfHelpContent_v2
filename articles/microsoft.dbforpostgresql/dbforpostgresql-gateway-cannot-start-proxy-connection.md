<properties
	pageTitle="Gateway can't start proxy connection to host"
	description="RCA - Gateway can't start proxy connection to host RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="seanliang"
	displayOrder="100"
	articleId="dbforpostgresql-gateway-cannot-start-proxy-connection"
	diagnosticScenario="OrcasPostgresGatewayCannotStartProxyConneciton"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Gateway can't start proxy connection to host

<!--issueDescription-->
To provide layered security and service scalability connections from clients to your database server are made via a gateway. Our internal service telemetry detected an unusually high number(<!--$Count-->count<!--/$Count-->) of login attempted failures indicating that a gateway process was failing to make a proxy connection to your host database server. Our support engineering team restarted the process and observed connections succeeding as expected. Our engineering team has been made aware of the failed process and will monitor gateways to determine a permanent fix.
<!--/issueDescription-->

## **Recommended documents**

[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)

[Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
