<properties
	pageTitle="Long running operations"
	description="Long running operations on Azure Database for PostgreSQL"
	infoBubbleText="Found long running operations on PostgreSQL server. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="Xin-Cheng"
	ms.author="chengxin"
	displayOrder="100"
	articleId="dbforpostgresql-asc-operation-longrunning"
	diagnosticScenario="OrcasPostgresOperation"
	selfHelpType="rca"
	supportTopicIds="32639966, 32639980, 32639988, 32639998, 32640024, 32640028, 32780989, 32780992, 32780995, 32780997, 32780998"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Long running operations on Azure Database for PostgreSQL

<!--issueDescription-->
Thank you for contacting Microsoft support team. We have detected that operation <!--$MsOperationType-->MsOperationType<!--/$MsOperationType--> with request ID <!--$RequestId-->RequestId<!--/$RequestId--> on Azure Database for PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> has lasted <!--$Duration-->Duration<!--/$Duration-->.
<!--/issueDescription-->

## **Recommended Steps**

* The most common reason when database is unavailable during a long running operation is that the database is going through recovery process. Please wait for the recovery to finish, you may monitor the recovery status using the Azure Database for PostgreSQL server logs.

## **Recommended Documents**
* [Restart Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-restart-server-portal)
* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-us/home?forum=AzureDatabaseforPostgreSQL)
* [Azure CLI for PostgreSQL](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest)
* [Logs in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-server-logs#diagnostic-logs)
