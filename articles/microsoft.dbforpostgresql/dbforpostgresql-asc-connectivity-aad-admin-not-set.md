<properties
	pageTitle="Connect to Server Failed Because Azure AD administrator is not set"
	description="RCA - Connect to Server Failed Because Azure AD administrator is not set"
	infoBubbleText="Found recent Azure AD connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="lufittl"
	authors="lfittl-msft"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-aad-admin-not-set"
	diagnosticScenario="OrcasPostgresAADAdminNotSet"
	selfHelpType="diagnostics"
	supportTopicIds="32742678"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Can’t connect to PostgreSQL server: Azure AD administrator is not set

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) that attempted to use Azure AD authentication, but the Azure AD administrator is not set.
<!--/issueDescription-->

## **Recommended Steps**

Set the Azure AD administrator for this database, login using the Azure AD administrator credentials, and then create appropriate database roles to grant Azure AD users and groups access to your database.

## **Recommended Documents**

* [How-to use Azure Active Directory for authenticating with PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-configure-sign-in-aad-authentication)
