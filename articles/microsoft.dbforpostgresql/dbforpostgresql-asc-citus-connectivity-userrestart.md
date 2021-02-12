<properties
	pageTitle="User restart"
	description="Connections failing because of user restart"
	infoBubbleText="Found recent connection failure: See details on the right."
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="v-basanj"
	displayOrder=""
	articleId="dbforpostgresql-asc-citus-connectivity-userrestart"
	diagnosticScenario="OrcasCitusUserRestartInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32731217, 32639977"
	productPesIds="17068"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforCitus"
/>

# User restart

<!--issueDescription-->
Your Hyperscale (Citus) server <!--$ServerName-->ServerName<!--/$ServerName--> was unavailable starting at <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) due to a user-initiated restart.
<!--/issueDescription-->

## **Recommended Steps**
* Servers typically return quickly after a restart. You can retry your connection.
* If the server was quite busy when restarted, it has more to do in recovery and may take longer to return
