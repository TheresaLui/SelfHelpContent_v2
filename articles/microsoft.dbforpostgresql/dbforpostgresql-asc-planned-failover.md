<properties
	pageTitle="Server planned failover"
	description="RCA - Server planned failover"
	infoBubbleText="Server planned failover detected"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="zhlian"
	ms.author="zhlian"
	displayOrder="100"
	articleId="dbforpostgresql-asc-planned-failover"
	diagnosticScenario="OrcasPostgresPlannedFailOver"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Can't connect to PostgreSQL server: planned failover

<!--issueDescription-->
Your server <!--$ServerName-->ServerName<!--/$ServerName--> was unavailable starting at <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) due to a planned failover: <!--$RCA-->RCA<!--/$RCA-->.
<!--/issueDescription-->

## **Recommended Steps**

1. In most of the cases, errors like the above are transient in nature and your database server will come back online automatically. Please try to reconnect to your server to see if the server is back online. 
2. You can also look at the Resource Health Check to see the current state of your server

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL)
* [Handling transient connectivity errors for Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-connectivity)
* [High availability](ttps://docs.microsoft.com/azure/postgresql/concepts-high-availability)

