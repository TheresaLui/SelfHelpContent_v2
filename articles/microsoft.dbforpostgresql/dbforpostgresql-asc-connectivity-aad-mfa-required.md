<properties
	pageTitle="Connect to Server Failed Because Azure AD token is missing multi-factor"
	description="RCA - Connect to Server Failed Because Azure AD token is missing multi-factor"
	infoBubbleText="Found recent Azure AD connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="lufittl"
	authors="lfittl-msft"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-aad-mfa-required"
	diagnosticScenario="OrcasPostgresAADMFARequired"
	selfHelpType="diagnostics"
	supportTopicIds="32742678, 32780959"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Can't connect to PostgreSQL server: Azure AD token is not authenticated with multi-factor authentication

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because of an Azure AD token that was not validated using multi-factor authentication.
<!--/issueDescription-->

## **Recommended Steps**

When fetching the Azure AD token for connecting to your database, make sure that you acquire the token in a session that is validated using multi-factors authentication (Windows Hello, phone authentication, etc).

## **Recommended Documents**

* [How-to use Azure Active Directory for authenticating with PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-configure-sign-in-aad-authentication)
