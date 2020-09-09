<properties
	pageTitle="Connect to Server Failed Because Azure AD failure due to Out Of Memory"
	description="RCA - Connect to Server Failed Because Azure AD failure due to Out Of Memory"
	infoBubbleText="Found recent Azure AD connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="lufittl"
	authors="lfittl-msft"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-aad-out-of-memory"
	diagnosticScenario="OrcasPostgresAADOutOfMemory"
	selfHelpType="diagnostics"
	supportTopicIds="32742678"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Can’t connect to PostgreSQL server: Azure AD failure due to Out Of Memory

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because your server was out of memory whilst attempting to authenticate using Azure AD.
<!--/issueDescription-->

## **Recommended Steps**

Make sure that your server has sufficient memory available to handle new incoming connections. Note that you may be seeing this error when you are running very close to the memory limit of your server. If this is a recurring issue we recommend increasing the size of your database server.

## **Recommended Documents**

* [Monitor and tune Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-monitoring)
