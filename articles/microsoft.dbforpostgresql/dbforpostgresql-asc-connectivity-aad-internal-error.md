<properties
	pageTitle="Connect to Server Failed Because of an Internal Error with Azure AD Authentication"
	description="RCA - Connect to Server Failed Because of an Internal Error with Azure AD Authentication"
	infoBubbleText="Found recent Azure AD connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="lufittl"
	authors="lfittl-msft"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-aad-internal-error"
	diagnosticScenario="OrcasPostgresAADInternalError"
	selfHelpType="diagnostics"
	supportTopicIds="32742678, 32780959"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Can't connect to PostgreSQL server: Internal error with Azure AD authentication

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because an internal error occurred whilst attempting to validate the Azure AD authentication token. 
<!--/issueDescription-->

## **Recommended Steps**

This error indicates that there was an internal problem validating your Azure AD authentication token. Please double check that your Azure AD token is retrieved correctly, and if it is, please create a support ticket for further investigation.

## **Recommended Documents**

* [How-to use Azure Active Directory for authenticating with PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-configure-sign-in-aad-authentication)
