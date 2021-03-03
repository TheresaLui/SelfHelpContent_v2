<properties
	pageTitle="User restart"
	description="Connections failing because of user restart"
	infoBubbleText="Found recent connection failure: See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-merupg-connectivity-userrestart"
	diagnosticScenario="OrcasMeruPGUserRestartInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32731217, 32639977, 32780960, 32780962"
	productPesIds="17069"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# User restart

<!--issueDescription-->
Your Postgres server <!--$ServerName-->ServerName<!--/$ServerName--> was unavailable starting at <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) due to a user-initiated restart.
<!--/issueDescription-->

## **Recommended Steps**
* Servers typically return quickly after a restart. You can retry your connection.
* If the server was quite busy when restarted, it has more to do in recovery and may take longer to return