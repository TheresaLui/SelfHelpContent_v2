<properties
	pageTitle="Connect to Server Failed Because of Invalid Azure AD Token"
	description="RCA - Connect to Server Failed Because of Invalid Azure AD Token"
	infoBubbleText="Found recent Azure AD connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="lufittl"
	authors="lfittl-msft"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-aad-bad-token"
	diagnosticScenario="OrcasPostgresAADBadToken"
	selfHelpType="diagnostics"
	supportTopicIds="32742678"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Can’t connect to PostgreSQL server: Invalid Azure AD token received by database server

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because of invalid Azure AD authentication tokens.
<!--/issueDescription-->

## **Recommended Steps**

Ensure that you are connecting to your PostgreSQL database server with a new Azure AD token that is retrieved shortly before making the connection. Azure AD tokens need to be requested for the resource `https://ossrdbms-aad.database.windows.net/`.

When connecting from an application, make sure that the Azure AD token retrieval is retrieved just in time when you are connecting to your database, instead of being only retrieved once when your application starts. In particular, pay attention to connection retry behavior, as a retry would need to fetch a new Azure AD token before connecting to the database.

## **Recommended Documents**

* [How-to use Azure Active Directory for authenticating with PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-configure-sign-in-aad-authentication)
* [How-to connect with Managed Identity to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-connect-with-managed-identity)
