<properties
	pageTitle="Connect to server failed because of Azure AD failure due to out of memory"
	description="RCA - Connect to server failed because of Azure AD failure due to out of memory"
	infoBubbleText="Found recent Azure AD connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="lufittl"
	authors="lfittl-msft"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-aad-out-of-memory"
	diagnosticScenario="OrcasPostgresAADOutOfMemory"
	selfHelpType="diagnostics"
	supportTopicIds="32742678, 32780959"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Can't connect to PostgreSQL server: Azure AD failure due to Out Of Memory

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because your server was out of memory whilst attempting to authenticate using Azure AD.
<!--/issueDescription-->

## **Recommended Steps**

Make sure that your server has sufficient memory available to handle new incoming connections. Note that you may be seeing this error when you are running very close to the memory limit of your server. 

* Reduce the number of idle connections. Query `SELECT * FROM pg_stat_activity` to see idle connections. Evaluate your application's connection model to avoid idle connections in the future.
* If high memory is a recurring issue, consider scaling up vCores to increase memory


## **Recommended Documents**

* [Monitor and tune Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-monitoring)
