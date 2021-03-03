<properties
	pageTitle="Failed connections - invalid authorization specification"
	description="Failed connections - invalid authorization specification"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="raagyema"
	displayOrder=""
	articleId="dbforpostgresql-asc-citus-connectivity-invalid-authorization"
	diagnosticScenario="OrcasCitusInvalidAuthorizationInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32639953"
	productPesIds="17068"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforCitus"
/>

# Failed connections due to invalid authorization specification

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to Hyperscale (Citus) server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because of an invalid authorization specification. This error typically indicates a mismatch between the SSL settings on the Hyperscale (Citus) server and the client making the connection.
<!--/issueDescription-->

## **Recommended Steps**

* Check the SSL settings on the client and server to confirm they correspond 